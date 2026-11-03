# 干掉刘海 · Hide the MacBook Notch

[English](README.md) · **简体中文** · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt-BR.md)

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.3.3-lightgrey)
![No network](https://img.shields.io/badge/network-none-success)

**让刘海消失。** 一个极轻量的 macOS 菜单栏工具：把顶部整条填成纯黑，让刘海融进一条完整的黑边——**不动你的壁纸**。可选给桌面加圆角。

![顶部是一条完整的黑，正文区域四角统一收圆](docs/screenshot-1.jpg)
![菜单栏右侧的状态栏图标，点一下即可开关](docs/screenshot-2.jpg)

---

## 为什么又做一个刘海工具

市面上的刘海工具大多反着来：把刘海变成「灵动岛」，塞音乐、计时器、文件托盘。这个只做一件事——**让刘海消失**，就像遮住屏幕边框那样。

**和改壁纸的方案不同，这里什么都不写进图片：**

- 壁纸还是你的，**动态壁纸照常播放**
- 一键关掉，屏幕立刻回到原样
- 不要录屏权限、不要辅助功能权限，不联网、不上报

## 特点

- **顶部纯黑**——刘海融进上边框，不再抢注意力
- **模拟屏幕圆角**——正文区域整体是一个圆角矩形，半径 8–48 点可调
- **全屏自动让位**——全屏看视频、玩游戏、做演示时自动收起，退出后恢复
- **多显示器安全**——只对带刘海的屏生效，外接显示器保持直角
- **分辨率自适应**——切到「刘海下方」的档位也能正确适配
- **切换桌面跟随**——圆角随桌面一起滑入滑出，转场期间不闪
- **零权限**——不需要辅助功能、录屏、摄像头
- **通用二进制**——Apple 芯片与 Intel 同一个安装包

## 和同类工具对比

|  | 本工具 | TopNotch | NotchNook | Boring Notch |
|---|---|---|---|---|
| 让刘海消失 | ✅ | ✅ 靠改壁纸 | ❌ 让它有用 | ❌ 让它有用 |
| 改动壁纸 | **从不** | 会 | – | – |
| 动态壁纸 | ✅ | ❌ | – | – |
| 屏幕圆角 | ✅ 实时浮层 | ✅ 写进壁纸 | ❌ | ❌ |
| 开源 | ✅ MIT | ❌ | ❌ | ✅ GPL-3.0 |
| 价格 | 免费 | 免费 | 付费 | 免费 |

*对比基于 2026 年 11 月的公开信息，欢迎通过 issue 指正。*

## 安装

1. 从 [Releases](../../releases/latest) 下载 `FuckBangs-1.3.3.dmg`
2. 把应用拖进「应用程序」
3. 首次打开会被 Gatekeeper 拦下（没有 Apple 开发者账号，未做公证）。到**系统设置 → 隐私与安全性 → 「仍要打开」**，输密码确认即可。

> 网上流传的「右键 → 打开」在 macOS 15 Sequoia 之后已经失效，只能用上面这条路。

**系统要求**：macOS 13 Ventura 或更高。带刘海的 MacBook（14/16 寸 MacBook Pro、M2 起的 MacBook Air）。没有刘海的机器可以装，但不会产生任何效果。

## 使用

- **状态栏图标左键**——快捷面板，六个开关直接切
- **状态栏图标右键**——菜单：打开主界面 / 停用 / 退出
- **程序坞图标**——打开主界面

## 常见问题

<details>
<summary><b>刘海能真的去掉吗？</b></summary>

不能——那是摄像头开孔，物理硬件。这个工具去掉的是*视觉上的不适*：把整条顶栏做成纯黑后，刘海不再被读成"缺了一块"。在 mini-LED 屏上黑色足够纯，效果接近消失。
</details>

<details>
<summary><b>会改我的壁纸吗？</b></summary>

不会。黑条和圆角都是浮在桌面之上、窗口之下的实时窗口，壁纸文件既不被读取也不被写入，动态壁纸照常运行。
</details>

<details>
<summary><b>会影响全屏应用或游戏吗？</b></summary>

不会。浮层在普通窗口之下，全屏内容会完整盖住它；顶部黑条还会主动检测全屏并让位。
</details>

<details>
<summary><b>外接显示器为什么没有效果？</b></summary>

它只对带刘海的屏生效。外接显示器绝大多数是直角边框，保持直角才自然，所以刻意不做处理。
</details>

<details>
<summary><b>安全吗？会上传数据吗？</b></summary>

应用里没有任何网络代码，不申请辅助功能或录屏权限。本地只保存六个开关状态和一个窗口位置。
</details>

<details>
<summary><b>为什么提示"无法验证开发者"？</b></summary>

因为没有买 Apple 开发者账号做公证，用的是本地签名。按上面「安装」的步骤允许一次即可，之后永久有效。
</details>

## 从源码构建

不需要 Xcode 工程，装好命令行工具即可：

```bash
./build.sh     # 交叉编译 arm64 + x86_64，lipo 合并，安装到 /Applications
./package.sh   # 生成 dist/FuckBangs-VERSION.dmg
```

重新生成图标：

```bash
swift tools/make_icon.swift Assets/icon_1024.png
```

## 实现要点

- 顶部黑条是一个 `NSWindow`，层级 `CGWindowLevelForKey(.mainMenuWindow) - 1`：垫在菜单栏下面、普通窗口上面，`ignoresMouseEvents` 让点击穿透
- 圆角由另一个窗口绘制，层级 `-1`，填充 `evenOdd(整屏矩形 − 正文矩形)`
- 这个窗口**必须用 `.fullScreenNone`**。声明 `.fullScreenAuxiliary` 会让它跟进全屏 Space，返回桌面时能否随桌面滑入就取决于 WindowServer 的遮挡剔除——Chrome 会剔除、Safari 不会，同一个 bug 表现为"看应用下菜"
- 全屏检测不能靠 `visibleFrame`；匹配 layer 0 窗口时，高度要同时接受"覆盖整屏"和"刘海下方（少 `safeAreaInsets.top`）"
- 圆角窗口要用原生 `NSWindow`，做成重写 `canBecomeKey = false` 的子类会导致内容不参与合成

## 调试参数

| 参数 | 作用 |
|---|---|
| `--selftest` | 打印屏幕参数、刘海宽度、登录项状态后退出 |
| `--render <dir>` | 把快捷面板和主界面渲染成 PNG（`NB_DARK=1` 出深色版） |
| `--show-window` | 启动后直接打开主界面 |
| `--show-quick` | 启动后直接弹出快捷面板 |

## 许可

MIT，见 [LICENSE](LICENSE)。
