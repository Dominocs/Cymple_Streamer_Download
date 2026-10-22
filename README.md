<p align="center">
  <img src="desktop_d3d11/assets/cymple_icon.png" alt="Cymple Streamer" width="112">
</p>

<h1 align="center">Cymple Streamer</h1>

<p align="center">
  在头显中使用电脑桌面、畅玩 SteamVR、语音交流<br>
  Your PC desktop, SteamVR games, and voice tools in VR
</p>

<p align="center">
  <a href="https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest">下载安装</a> ·
  <a href="docs/使用指南.md">完整使用指南</a> ·
  <a href="#english">English</a>
</p>

## 简体中文

Cymple Streamer 将 Windows 电脑桌面和 SteamVR 游戏串流到头显，提供画质调整、帧生成、音频与追踪，以及本地语音识别、翻译和朗读功能。

本文档按 **0.16.6** 的使用界面整理，更新于 **2026 年 10 月 22 日**。不同头显可用的功能有所不同，请以连接后的选项与提示为准。

### 按功能查阅

| 想做什么 | 使用说明 |
| --- | --- |
| 第一次安装，连接电脑 | [安装与首次连接](docs/使用指南.md#setup) |
| 使用 Wi-Fi、Quest USB 或 PICO USB | [连接方式](docs/使用指南.md#connection) |
| 在 Steam Frame 上使用 | [Steam Frame 安装与启动](docs/使用指南.md#steam-frame) |
| 操作电脑、切换显示器、输入文字 | [桌面操作与虚拟键盘](docs/使用指南.md#desktop) |
| 玩 PC VR 游戏，在游戏与桌面间切换 | [SteamVR 游戏](docs/使用指南.md#steamvr) |
| 调整清晰度、刷新率和码率 | [画质与流畅度](docs/使用指南.md#picture) |
| 调整注视区域 | [注视点串流](docs/使用指南.md#gaze) |
| 使用动态／静态、内插／外推帧 | [帧生成](docs/使用指南.md#frame-generation) |
| 收听电脑声音，使用头显麦克风 | [音频与语音](docs/使用指南.md#audio) |
| 使用手部、眼面和全身追踪 | [输入与追踪](docs/使用指南.md#tracking) |
| 说话转文字、五语翻译、发送聊天框、文字朗读 | [语音与翻译](docs/使用指南.md#speech) |
| 查看帧率和延迟，解决连接或画面问题 | [性能面板](docs/使用指南.md#performance) · [常见问题](docs/使用指南.md#troubleshooting) |
| 更新、维护或提交反馈 | [更新与维护](docs/使用指南.md#maintenance) · [问题反馈](docs/使用指南.md#feedback) |

### 下载与使用条件

从 [Cymple Streamer 下载页](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest) 获取配套版本：

| 设备 | 安装文件 |
| --- | --- |
| Windows 电脑 | `Cymple_Streamer_Setup_v版本号.exe` |
| Android VR 头显 | `cymple_streamer_android_v版本号.APK` |
| Steam Frame | 专用安装器 `CympleStreamerSteamFrameSetup.exe`，在 Windows 上运行；获取方式见[专用指南](docs/使用指南.md#steam-frame) |

需要 Windows 10 / 11 电脑和兼容头显；玩 PC VR 游戏还需安装 Steam 与 SteamVR。电脑显卡、头显及所选视频格式需相互兼容。无线连接建议电脑接网线，头显连接同一局域网的 5 GHz 或受支持的 6 GHz Wi-Fi。

眼动、面部和全身追踪需要对应设备与权限，游戏和虚拟形象也需支持。帧生成用于 SteamVR SDR，实际流畅度取决于整套设备，可能产生重影或增加延迟。语音识别与翻译支持中、英、日、韩、俄五种语言；朗读支持中文和英文，所需模型下载完成后可离线使用。

### 第一次使用

1. 在电脑和头显安装、打开配套程序。Steam Frame 按专用指南安装。
2. 将电脑与头显接入同一局域网，或完成对应设备的 USB 连接准备。
3. 在头显「电脑」页选择带有 `WIFI` 或 `USB` 标记的电脑。
4. 确认桌面显示和操作正常，点击头显菜单中的「启动 STEAMVR」，再打开游戏。
5. 需要调整时，从电脑「串流设置」开始，每次修改一项；出现重启提示时先保存游戏进度。

详细步骤和设置说明见[完整使用指南](docs/使用指南.md)。遇到问题，可在电脑「问题反馈」提交说明或导出诊断包。

## English

Cymple Streamer brings your Windows desktop and SteamVR games into a compatible VR headset. It includes controller-based desktop interaction, a virtual keyboard, image settings, frame generation, audio, supported tracking features, and local speech tools.

This guide covers the **0.16.6** interface and was updated on **October 22, 2026**. Available features depend on your headset and connected PC.

### Download and connect

1. Get matching Windows and Android installers from the [download page](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest). Steam Frame uses a separate Windows-based installer; see the [Steam Frame guide in Chinese](docs/使用指南.md#steam-frame) for availability and setup.
2. Install and open the apps. For wireless streaming, connect both devices to the same local network. Supported USB connections require device-specific setup.
3. Select your computer on the headset's **Computer** page.
4. Check desktop streaming, then choose **Start SteamVR** and open a game.
5. Adjust **Streaming** settings one at a time. Save your game before accepting a SteamVR restart prompt.

### Features

| Feature | What you can do |
| --- | --- |
| Desktop | Use controllers to point, click, switch displays, and type with the virtual keyboard |
| Image settings | Adjust resolution, refresh rate, bitrate, codec, clarity, Global FSR, and gaze-region settings |
| Frame generation | Choose dynamic or static scheduling and interpolation or extrapolation for SteamVR SDR |
| Audio | Hear PC audio and use the headset microphone in PC applications |
| Tracking | Use supported hand, eye, face, and body tracking with compatible hardware and applications |
| Speech | Recognize and translate Chinese, English, Japanese, Korean, and Russian; send text to VRChat's chatbox; read Chinese and English text aloud |
| Diagnostics | View the headset performance overlay, read logs, and export or submit feedback |

Frame generation can introduce artifacts or latency; its displayed frame rate is not the game's own frame rate. Tracking requires compatible devices and permissions. Local speech tools work offline after downloading the required models.

See the [complete user guide in Chinese](docs/使用指南.md) for controls, settings, and troubleshooting. In the Windows app, **Feedback** lets you describe a problem or export a diagnostic bundle.

## 致谢 / Acknowledgments

本项目基于 [ALVR](https://github.com/alvr-org/ALVR) 修改与扩展，感谢项目维护者与开源社区。第三方组件遵循各自随附的许可证。

Based on [ALVR](https://github.com/alvr-org/ALVR). Thanks to its maintainers and the open-source community. Third-party components retain their respective licenses.
