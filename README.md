# 干掉刘海 · Hide the MacBook Notch

**English** · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt-BR.md)

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)
![No network](https://img.shields.io/badge/network-none-success)

**Make the notch disappear.** A tiny open-source macOS menu bar app that blacks out the top bar so the notch blends into one solid black edge — your wallpaper is never touched. Optionally rounds the corners of the desktop.

![The menu bar becomes one solid black edge, the desktop below gets rounded corners](docs/screenshot-1.jpg)
![The status bar icon, one click to toggle](docs/screenshot-2.jpg)

---

## Why another notch app?

Most notch apps go the other way: they turn the notch into a Dynamic Island — music controls, timers, file shelves. This one does the opposite. It removes the notch from view, the way you'd hide a bezel.

**Unlike wallpaper-based fixes, nothing is baked into an image:**

- Your wallpaper stays yours — **dynamic wallpapers keep working**
- One click to turn it off, and your screen is exactly as it was
- No screen recording, no accessibility permission, no network, no telemetry

## Features

- **Solid black menu bar** — the notch merges into the top edge and stops drawing attention
- **Rounded screen corners** — the content area becomes one rounded rectangle; radius adjustable 8–48 pt
- **Full-screen aware** — disappears automatically for full-screen video, games and presentations, comes back when you leave
- **Multi-display safe** — only acts on displays that actually have a notch; external monitors keep their square corners
- **Resolution aware** — adapts when you switch to a "below the notch" scaled mode
- **Space aware** — corners slide in and out with your desktops, no flicker during the transition
- **No permissions** — no accessibility, no screen recording, no camera
- **Universal binary** — Apple Silicon and Intel in one app

## How it compares

|  | This app | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| Hides the notch | ✅ | ✅ via wallpaper | ❌ makes it useful | ❌ makes it useful |
| Wallpaper modified | **Never** | Yes | – | – |
| Dynamic wallpapers | ✅ | ❌ | – | – |
| Rounded screen corners | ✅ live overlay | ✅ baked into wallpaper | ❌ | ❌ |
| Open source | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| Price | Free | Free | Paid | Free |

*Comparison reflects public information as of November 2026; corrections welcome via issues.*

## Install

1. Download `FuckBangs-1.3.3.dmg` from [Releases](../../releases/latest)
2. Drag the app into **Applications**
3. First launch is blocked by Gatekeeper (the app isn't notarized — no Apple Developer account). Fix it in **System Settings → Privacy & Security → "Open Anyway"**, then confirm with your password.

> The old right-click → Open trick stopped working in macOS 15 Sequoia. The Settings route above is the only way now.

**Requirements:** macOS 13 Ventura or later. A MacBook with a notch (14"/16" MacBook Pro, MacBook Air M2 and later). On other Macs the app installs fine but does nothing.

## Usage

- **Status bar icon, left click** — quick panel with all six switches
- **Status bar icon, right click** — menu: open settings, disable, quit
- **Dock icon** — opens the settings window

## FAQ

<details>
<summary><b>Can the notch actually be removed?</b></summary>

No — it's a camera cutout, physical hardware. What this app removes is the *visual* discomfort: by making the whole top bar pure black, the notch stops reading as a gap. On a mini-LED display the black levels match so closely that the notch effectively vanishes.
</details>

<details>
<summary><b>Does it change my wallpaper?</b></summary>

No. The black bar and the rounded corners are live overlay windows drawn above the desktop and below your app windows. Your wallpaper file is never read or written, so dynamic wallpapers keep animating.
</details>

<details>
<summary><b>Will it interfere with full-screen apps or games?</b></summary>

No. The overlays sit below normal windows, so full-screen content covers them completely. The top bar additionally detects full-screen mode and gets out of the way by itself.
</details>

<details>
<summary><b>Does it work on external monitors?</b></summary>

It only acts on displays with a notch. External monitors are usually square-cornered, so they're left alone on purpose.
</details>

<details>
<summary><b>Is it safe? Does it phone home?</b></summary>

There is no networking code in the app at all. It requests no accessibility or screen-recording permission. Everything it stores is six switch states and one window position, in local `UserDefaults`.
</details>

<details>
<summary><b>Why does macOS say "cannot verify the developer"?</b></summary>

The app is signed locally (ad-hoc) because Apple notarization requires a paid developer account. The steps under [Install](#install) get you past it once, permanently.
</details>

## Build from source

No Xcode project needed — just the command line tools:

```bash
./build.sh     # cross-compiles arm64 + x86_64, merges with lipo, installs to /Applications
./package.sh   # produces dist/FuckBangs-VERSION.dmg
```

Regenerate the icon:

```bash
swift tools/make_icon.swift Assets/icon_1024.png
```

## Implementation notes

- The top bar is an `NSWindow` at `CGWindowLevelForKey(.mainMenuWindow) - 1`: below the menu bar, above normal windows, with `ignoresMouseEvents` so clicks pass through
- The corners are drawn by a second window at level `-1`, filling `evenOdd(screen rect − content rect)`
- That window **must** use `.fullScreenNone`. With `.fullScreenAuxiliary` it follows into full-screen Spaces, and whether it slides back with the desktop then depends on WindowServer's occlusion culling — Chrome culls it, Safari doesn't, and the same bug shows up as "depends on which app you came from"
- Full-screen detection can't rely on `visibleFrame`; when matching layer-0 windows, accept both "covers the whole screen" and "sits below the notch (`safeAreaInsets.top` shorter)"
- Use a plain `NSWindow` for the corner overlay — a subclass overriding `canBecomeKey = false` ends up not being composited at all

## Debug flags

| Flag | Purpose |
|---|---|
| `--selftest` | prints screen geometry, notch width, login item state and exits |
| `--render <dir>` | renders the quick panel and settings window to PNG (`NB_DARK=1` for dark) |
| `--show-window` | opens the settings window on launch |
| `--show-quick` | opens the quick panel on launch |

## License

MIT — see [LICENSE](LICENSE).
