# 771 Screenshot Tool（独立版）

从 **柒柒壹工具箱** 里单独拆出来的截图工具：**只有一个 exe，双击即用**，不依赖工具箱、也不用安装任何东西。
常驻后台，随时用快捷键截图。

当前版本：**v1.20**（2026-10-09）· Windows 10 / 11（64 位）

**从 v1.19 起带联网自动更新**：启动后会在后台查一次新版本（失败静默），发现新版会弹窗问你要不要更新，
下载后自动校验（Ed25519 签名 + SHA-256）再替换并重启。也可以手动到 Releases 下载。

> 2026-10-09 起本工具改名：原名「柒柒壹截图工具」→ **771 Screenshot Tool**，
> 仓库也从 `771JIETU` 迁到 `771ScreenshotTool`，exe 文件名 `771ScreenshotTool.exe`。

## 下载

到 [Releases](https://github.com/L1ngYueSheng/771ScreenshotTool/releases) 页面：

| 文件 | 说明 |
| --- | --- |
| `771ScreenshotTool.exe` | 单文件，双击即用（建议放到固定目录，例如 `D:\RJIAN\GJU\JT`） |
| `771ScreenshotTool_v1.20.zip` | 上面那个 exe + 使用说明（想连说明一起保存就下这个） |

> 资产名只能是 ASCII（GitHub 会把非 ASCII 字符剥掉），所以这里叫 `771ScreenshotTool.exe`。

## 快捷键（默认值，可在界面里改）

| 功能 | 默认键 |
| --- | --- |
| 区域截图（拖选后就地标注） | `Ctrl+Alt+A` |
| 全屏截图 | `Ctrl+Alt+S` |
| 窗口截图 | `Ctrl+Alt+W` |
| 取色器 | `Ctrl+Shift+C` |
| 屏幕标尺 | `Ctrl+Shift+M` |
| 标注最近一张 | `Ctrl+Alt+N` |
| 贴图工具窗 | `Ctrl+Shift+P` |

## 功能

- **区域截图 + 就地标注**：拖完范围，工具栏直接出现在选区旁，可画矩形 / 椭圆 / 箭头 / 铅笔 / 文字 / 马赛克 / 高亮 / 序号，五色可选、线宽可调，带撤销 / 重做 / 清空。`Enter` 保存并复制、`Ctrl+S` 只保存、`Ctrl+C` 只复制、`Esc` 取消。
- **窗口截图**：鼠标悬停高亮窗口边框，点一下截那个窗口；产物是窗口自己的内容，不会被别的窗口挡住。
- **滚动长图**：框选可滚动区域后自动逐帧拼接成长图（失败不留半成品）。
- **取色器 / 屏幕标尺**：放大镜取色（HEX / RGB，点一下复制）、拖框量宽高并显示刻度。
- **贴图**：把截图钉在桌面上，可拖动、拖任意边或角改大小、`Ctrl+滚轮` 调透明度。
- 截图后自动复制到剪贴板，并可在界面里改保存目录（文件名为 `shot_年月日_时分秒.png`）。

配置与热键存在 `%APPDATA%\柒柒壹工具箱\screenshot_cfg.json`；开机自启会在
`HKCU\Software\Microsoft\Windows\CurrentVersion\Run` 里写一条名为 `771 Screenshot Tool` 的启动项。
更新日志写在 `%APPDATA%\柒柒壹工具箱\update_log.txt`（与工具箱共用；想换镜像可在同目录的
`update_mirrors.txt` 里按 `前缀` 或 `url=完整清单地址` 写一行）。

## 最近几版

- **v1.19** 加**联网自动更新**（与工具箱同一套：Ed25519 验签清单 + SHA-256 校验 + .bat 助手替换重启）；体积 12.9 → 16.0 MB（联网栈回来了）。
- **v1.18** 改名：产品名与窗口标题 → `771 Screenshot Tool`，exe → `771ScreenshotTool.exe`；开机自启项自动迁移。
- **v1.17** 体积优化：单文件 12.9 MB（原 20.2 MB），摘掉用不到的 AVIF 插件与整条网络栈，功能未动。

## 相关

完整版（格式转换 / 批量改名 / 视频下载 / 压缩解压 / 截图 五合一）：<https://github.com/L1ngYueSheng/771Toolbox>
