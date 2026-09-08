<p align="center">
  <img src="desktop/assets/cymple_icon.png" alt="Cymple Streamer" width="112">
</p>

<h1 align="center">Cymple Streamer</h1>

<p align="center">
  把电脑桌面和 SteamVR 游戏带进头显<br>
  Bring your PC desktop and SteamVR games into your headset
</p>

<p align="center">
  <a href="#简体中文">简体中文</a> ·
  <a href="#english">English</a> ·
  <a href="https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest">下载 / Download</a>
</p>

## 简体中文

Cymple Streamer 是基于 [ALVR](https://github.com/alvr-org/ALVR) 扩展的 VR 串流项目，提供 Windows 电脑端和 Android 头显端。通过无线或受支持的 USB 连接，在头显中操作电脑、进入 SteamVR，并使用眼追、帧生成和本地语音工具。

### 特点功能

| 功能 | 简介 |
| --- | --- |
| **注视点串流** | 清晰区域跟随有效眼追，减少外围画面的处理与传输负担；无眼追时使用画面中心 |
| **帧生成** | 支持 FidelityFX 与 NVIDIA Optical Flow，补充中间帧，让运动画面更连贯 |
| **桌面与 SteamVR 切换** | 连接后先显示电脑桌面，再从头显启动 SteamVR；支持手柄操作与虚拟键盘 |
| **WIFI / USB 连接** | 在头显中直接选择电脑及连接路线，USB 需设备系统支持 |
| **画质与性能调整** | 分辨率、刷新率、码率、编码、全局 FSR、锐化与周边压缩等常用设置 |
| **音频与追踪** | 电脑音频、头显麦克风直通，以及受支持的手部、面部和全身追踪 |
| **本地语音与翻译** | 中、英、日、韩、俄五语识别与翻译，可通过 OSC 输出到 VRChat 聊天框；支持中英文朗读 |
| **实时状态与排障** | 查看实际视频帧率、分段延迟和码率，提供驱动维护、防火墙配置与运行日志 |

帧生成当前用于 **Windows SteamVR SDR** 串流，可能产生重影或增加延迟；实际显示受头显刷新率与处理能力限制。眼追、面捕和全身追踪需要对应硬件、权限及接收软件支持。本地语音模型首次下载后可离线使用。

### 下载

前往 **[Cymple Streamer 下载页](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest)**，在 Assets 中获取配套版本：

- **电脑端：**`Cymple_Streamer_Setup_v*.exe`
- **头显端：**`cymple_streamer_android_v*.apk`

电脑安装 EXE，头显安装 APK。使用同一发行版的配套文件，安装后在两端「关于」核对版本。

### 使用条件

- Windows 10 / 11 电脑，显卡支持所选格式的硬件编码；玩 PC VR 时需安装 Steam 与 SteamVR。
- 可运行本项目 APK 的 Android VR 头显，具体功能取决于型号和系统能力。
- 无线连接时，电脑与头显处于同一局域网；建议电脑接网线、头显使用 5 GHz / 可用的 6 GHz Wi-Fi。
- 当前自动 USB 网络路径用于系统支持的 Meta / Oculus 头显，要求 Android 12 / API 31 或更新系统；PICO 当前使用无线连接。

### 快速开始

1. 在电脑安装并打开 Cymple Streamer，在头显安装并打开配套 APK。
2. 无线接入同一局域网；使用受支持的 USB 连接时，插入数据线并允许头显的 USB 网络请求。
3. 在头显「电脑」页选择 `电脑名 (WIFI)` 或 `电脑名 (USB)`。
4. 看到电脑桌面后，打开头显菜单，点击「启动 STEAMVR」，再启动游戏。
5. 先用较低分辨率、自适应码率和自动编码验证连接，再逐项尝试注视点串流、帧生成等功能。

**先看桌面，再进游戏；每次只调整一项设置。**分辨率、首选刷新率、帧生成等设置更改后，按提示重启 SteamVR。

### 教程与问题反馈

- [小白使用教程](desktop/docs/小白使用教程.md)：连接步骤、设置速查、音频与追踪配置、常见问题排查。
- [PDF 使用教程](output/pdf/Cymple_Streamer_小白使用教程_v0.3.1.pdf)：适合离线阅读和分享，按 0.3.1 整理。
- [桌面端与构建说明](desktop/README.md)：开发、打包和功能实现说明。
- [提交问题](https://github.com/Dominocs/cymple_Streamer/issues)：请附两端版本、头显 / 显卡型号、连接方式、复现步骤和日志。

遇到问题，先看电脑「状态面板」和「运行日志」。日志可通过「打开日志目录」获取，也可在资源管理器打开 `%LOCALAPPDATA%\Cymple Streamer\logs`。

### 开源与致谢

本项目基于 ALVR 修改与扩展，感谢 ALVR 维护者及开源社区的贡献。项目采用 [MIT 许可证](vr/LICENSE)，第三方组件及模型遵循各自随附的许可证。

---

## English

Cymple Streamer is a VR streaming project built on [ALVR](https://github.com/alvr-org/ALVR), with a Windows desktop application and an Android headset client. Connect over Wi-Fi or supported USB networking to use your PC desktop, play SteamVR games, and access gaze tracking, frame generation, and local speech tools.

### Features

| Feature | Overview |
| --- | --- |
| **Gaze-based foveated streaming** | Keeps the gaze region sharp while reducing peripheral processing and transmission load; falls back to the image center without valid eye tracking |
| **Frame generation** | Supports FidelityFX and NVIDIA Optical Flow to generate intermediate frames for smoother motion |
| **Desktop and SteamVR switching** | Start on your PC desktop, then launch SteamVR from the headset; includes controller input and a virtual keyboard |
| **Wi-Fi and USB connections** | Select your computer and connection route in the headset; USB requires system support |
| **Image and performance controls** | Adjust resolution, refresh rate, bitrate, codec, Global FSR, sharpening, and peripheral compression |
| **Audio and tracking** | Stream PC audio, use the headset microphone, and forward supported hand, face, and body tracking |
| **Local speech and translation** | Recognize and translate Chinese, English, Japanese, Korean, and Russian; send text to VRChat through OSC and read Chinese or English text aloud |
| **Live diagnostics** | Monitor delivered video frame rate, latency stages, and bitrate, with driver maintenance, firewall configuration, and logs |

Frame generation currently supports **Windows SteamVR SDR** streaming. It may introduce artifacts or additional latency, and displayed frame rates remain limited by headset refresh rate and processing capacity. Eye, face, and body tracking require compatible hardware, permissions, and receiving software. Local speech models work offline after their initial download.

### Download

Visit the **[Cymple Streamer download page](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest)** and get a matching pair from Assets:

- **Windows:** `Cymple_Streamer_Setup_v*.exe`
- **Headset:** `cymple_streamer_android_v*.apk`

Install the EXE on your PC and the APK on your headset. Use the files provided together in the same release and check the installed versions under About on both devices.

### Requirements

- A Windows 10 / 11 PC with hardware encoding support for the selected codec. Steam and SteamVR are required for PC VR games.
- An Android VR headset capable of running this project's APK. Feature availability depends on the device and its system capabilities.
- For Wi-Fi, connect the PC and headset to the same local network. An Ethernet connection for the PC and 5 GHz / available 6 GHz Wi-Fi for the headset are recommended.
- The current automatic USB networking path targets supported Meta / Oculus systems running Android 12 / API 31 or newer. PICO currently uses Wi-Fi.

### Quick start

1. Install and open Cymple Streamer on your PC, then install and open the matching APK on your headset.
2. Join the same local network, or connect a data cable and accept the headset's USB networking prompt on a supported device.
3. On the headset's Computer page, select `PC name (WIFI)` or `PC name (USB)`.
4. Once the desktop appears, open the headset menu, choose **Start SteamVR**, and launch your game.
5. Start with a modest resolution, adaptive bitrate, and automatic codec selection. Enable foveated streaming, frame generation, and other features one at a time after the connection is stable.

**Check the desktop first, then launch your game. Change one setting at a time.** Restart SteamVR when prompted after changing settings such as resolution, preferred refresh rate, or frame generation.

### Documentation and support

- [Beginner guide (Chinese)](desktop/docs/小白使用教程.md): connection steps, settings, audio and tracking setup, and troubleshooting.
- [PDF guide (Chinese)](output/pdf/Cymple_Streamer_小白使用教程_v0.3.1.pdf): an offline guide based on version 0.3.1.
- [Desktop and build documentation (Chinese)](desktop/README.md): development, packaging, and implementation notes.
- [Report an issue](https://github.com/Dominocs/cymple_Streamer/issues): include both app versions, headset and GPU models, connection type, reproduction steps, and logs.

For troubleshooting, start with **Overview** and **Logs** in the desktop app. Choose **Open log folder**, or open `%LOCALAPPDATA%\Cymple Streamer\logs` in File Explorer.

### License and acknowledgments

This project modifies and extends ALVR. Thanks to the ALVR maintainers and the open-source community for their work. The project uses the [MIT license](vr/LICENSE); third-party components and models retain their respective licenses.
