# Notch ausblenden · Hide the MacBook Notch

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · **Deutsch** · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt-BR.md)

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)

**Den Notch verschwinden lassen.** Eine winzige Open-Source-Menüleisten-App für macOS, die die obere Leiste durchgehend schwarz füllt, sodass der Notch mit dem schwarzen Rand verschmilzt – **ohne das Hintergrundbild anzufassen**. Optional mit abgerundeten Ecken für den Desktop.

![Die Menüleiste wird zu einem durchgehenden schwarzen Rand, der Desktop darunter bekommt runde Ecken](docs/screenshot-1.jpg)

## Warum noch eine Notch-App?

Die meisten Notch-Apps machen das Gegenteil: Sie verwandeln den Notch in eine Dynamic Island mit Musik, Timern und Dateiablage. Diese App macht nur eins – **den Notch aus dem Sichtfeld entfernen**, so wie man einen Displayrahmen kaschiert.

Der Unterschied zu Wallpaper-Lösungen:

- Dein Hintergrundbild bleibt deins – **dynamische Wallpaper laufen weiter**
- Ein Klick, und alles ist wie vorher
- Keine Bildschirmaufnahme-, keine Bedienungshilfen-Berechtigung, keine Netzwerkverbindung

## Funktionen

- **Durchgehend schwarze Menüleiste** – der Notch geht in der Oberkante auf
- **Abgerundete Bildschirmecken** – der Inhaltsbereich wird zu einem einzigen abgerundeten Rechteck, Radius 8–48 pt
- **Vollbild-freundlich** – weicht bei Vollbildvideos, Spielen und Präsentationen automatisch
- **Externe Monitore unberührt** – wirkt nur auf Displays mit Notch
- **Auflösungs- und Space-fähig** – Ecken gleiten mit dem Desktop mit
- **Keine Berechtigungen, kein Netzwerk**

## Vergleich

|  | Diese App | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| Notch ausblenden | ✅ | ✅ übers Wallpaper | ❌ macht ihn nützlich | ❌ macht ihn nützlich |
| Wallpaper verändert | **Nie** | Ja | – | – |
| Dynamische Wallpaper | ✅ | ❌ | – | – |
| Abgerundete Ecken | ✅ Live-Overlay | ✅ ins Wallpaper gebrannt | ❌ | ❌ |
| Open Source | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| Preis | Kostenlos | Kostenlos | Kostenpflichtig | Kostenlos |

## Installation

1. `FuckBangs-1.3.3.dmg` von [Releases](../../releases/latest) herunterladen
2. In den Ordner **Programme** ziehen
3. Der erste Start wird von Gatekeeper blockiert (keine Notarisierung). Unter **Systemeinstellungen → Datenschutz & Sicherheit → „Dennoch öffnen"** freigeben.

**Voraussetzungen:** macOS 13 Ventura oder neuer. Ein MacBook mit Notch (14"/16" MacBook Pro, MacBook Air ab M2). Auf Macs ohne Notch lässt sich die App installieren, bewirkt aber nichts.

Ausführliche Dokumentation, Build aus dem Quellcode und Implementierungshinweise: [English README](README.md).

## Lizenz

MIT – siehe [LICENSE](LICENSE).
