# Cymple Streamer User Guide

Applies to **0.16.6** · Updated **October 22, 2026**

Cymple Streamer lets you use your Windows desktop, play SteamVR games, and access audio, tracking, speech recognition, and translation tools in a VR headset. This guide is organized by feature and uses the names shown in the English interface.

[简体中文](user-guide.zh-CN.md) · [English](user-guide.en.md) · [Home](../README.md#english) · [Download](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest)

## Find a feature

| Feature | What this section covers |
| --- | --- |
| [Installation and first connection](#setup) | Requirements, Windows and Android installation, first launch |
| [Steam Frame](#steam-frame) | Dedicated installer, updates, launching from the headset library |
| [Connection options](#connection) | Wi-Fi, Quest USB, PICO USB, switching connections |
| [Desktop controls](#desktop) | Controller buttons, multiple displays, keyboard, size, passthrough |
| [SteamVR games](#steamvr) | Starting games, returning to the desktop, closing SteamVR |
| [Image quality and smoothness](#picture) | Resolution, refresh rate, codec, bitrate, clarity, buffering |
| [Foveated streaming](#gaze) | Requirements, gaze region, peripheral compression, gaze display |
| [Frame generation](#frame-generation) | Enabling it, scheduling, generation methods, checking the results |
| [Audio and voice](#audio) | PC audio, headset microphone, volume, muting |
| [Input and tracking](#tracking) | Hand, eye, face, and full body tracking |
| [Speech and translation](#speech) | Recognition, translation, VRChat chatbox, text to speech |
| [Performance overlay](#performance) | Frame rate, latency, bitrate, device information |
| [Updates and maintenance](#maintenance) | Updates, driver maintenance, firewall, uninstalling |
| [Troubleshooting](#troubleshooting) | Checks organized by symptom |
| [Feedback](#feedback) | Logs, diagnostic exports, submitting feedback |

<a id="setup"></a>

## 1. Installation and first connection

### 1.1 What you need

| Item | Requirements |
| --- | --- |
| PC | Windows 10 / 11, with a GPU that can run your chosen game and supports the selected video format |
| PC VR games | Steam, SteamVR, and the game you want to play |
| Android headset | A VR headset compatible with this project's APK, such as a supported Quest or PICO device |
| Steam Frame | The dedicated installer; follow the [next section](#steam-frame) |
| Wireless network | The PC and headset on the same local network; Ethernet for the PC and 5 GHz or supported 6 GHz Wi-Fi for the headset are recommended |
| USB connection | A cable that supports data transfer, with the permissions required for your headset |

Available refresh rates, resolutions, video formats, passthrough, and tracking features vary by device. Connect the headset before choosing settings and follow the app's compatibility notices. Greyed-out options and items marked unsupported are not available for the current device.

### 1.2 Install the Windows app

1. Download `Cymple_Streamer_Setup_vVERSION.exe` from the [download page](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest).
2. End any active stream and close SteamVR. Run the installer and follow its instructions. Allow the Windows permission prompt for installation.
3. If the installer asks you to restart Windows after installing the virtual audio device for the first time, do so before continuing.
4. Open Cymple Streamer. To play PC VR games, make sure Steam and SteamVR are installed.
5. If Windows asks for network access, allow the app to communicate on the network you use for streaming.

### 1.3 Install the Android headset app

1. Download the matching `cymple_streamer_android_vVERSION.APK`.
2. Follow your headset manufacturer's instructions to enable developer features, then install the file with an APK installation tool that supports your device.
3. Find Cymple Streamer in the headset's app list. Apps installed this way may appear under a category such as **Unknown Sources**.
4. Open the app. Grant microphone, eye, face, or body tracking permissions when you want to use those features.

Use the PC and headset files provided together in the same release whenever possible. Steam Frame uses its dedicated installer, not the Android APK.

### 1.4 Start your first stream

1. Open the PC and headset apps.
2. Complete the [Wi-Fi or USB setup](#connection).
3. On the headset's **Computer** page, point at the desired PC and press the trigger.
4. Check that the desktop appears and that you can move the pointer and click a window. Then check PC audio.
5. To play a game, open the headset menu and select **Start SteamVR**.

Keep the default settings for your first connection. If the stream stutters, lower the resolution or bitrate. Once the connection is stable, adjust image quality, foveated streaming, and frame generation one setting at a time.

<a id="steam-frame"></a>

## 2. Steam Frame installation and launch

Steam Frame uses `CympleStreamerSteamFrameSetup.exe`, a dedicated installer that runs on Windows. **As of this guide's update date, the [public download page](https://github.com/Dominocs/Cymple_Streamer_Download/releases/tag/latest) lists the Windows PC installer and Android APK, but does not yet list the Steam Frame installer.** Obtain a matching dedicated installer from the publisher before following this section. Check the release page for future availability.

### 2.1 Install

1. On Steam Frame, open **Steam Settings → System** and enable Developer Mode. The installer's **Developer Mode guide** also provides instructions.
2. Connect the headset to the PC with a USB data cable. Keep the headset awake with Steam running, and accept a USB debugging authorization prompt if one appears.
3. Open the dedicated installer on Windows and click **Refresh devices**.
4. Confirm that Steam Frame is detected. Enter a **Devkit Game name**, or keep the default `Cymple_Streamer`.
5. Click **Install** and wait for the completion message.
6. On the headset, go to **Library → Non-Steam** and open `Devkit Game: Cymple_Streamer`. If you changed the name, open that entry instead.
7. Open the Windows PC app, then manually select the PC on the headset's **Computer** page.

Launch the app yourself from the headset library after installation. Successful installation over USB does not by itself establish a streaming connection; select an available connection on the **Computer** page.

### 2.2 Update or uninstall

Connect the headset in the same way and select **Update** or **Uninstall** in the installer. Use **Update** for an existing installation and **Install** when the app is not installed. Keep the headset awake, the cable connected, and Steam running until the operation finishes.

For detection or installation failures, read the **Operation log** or click **Open log**. If no device appears, check the cable, Developer Mode, and any authorization prompt in the headset.

### 2.3 Things to check

- Select a PC manually after launching the Steam Frame app.
- Use H.264 or HEVC. Do not follow Android-specific instructions to enable AV1, HEVC-10Bit, or HDR on this client.
- The headset's own per-application quality and refresh-rate settings also affect the experience. Check them if the image or refresh rate is not what you expected.
- See [desktop controls](#desktop) for switching views and keyboard shortcuts. Follow the app's notices for features that are absent or unavailable.

<a id="connection"></a>

## 3. Connection options

### 3.1 Wi-Fi

1. Connect the PC and headset to the same local network.
2. Open both apps and wait for the PC to appear on the headset's **Computer** page.
3. Select the entry marked `WIFI`.

Use Ethernet for the PC where possible and keep the headset near the router. Guest Wi-Fi, device isolation, or some VPN settings may prevent discovery. Check these first if the PC does not appear.

### 3.2 Quest USB

1. Connect the headset to the PC with a USB cable that supports data transfer.
2. Open both apps and accept the headset's USB networking prompt.
3. Wait for a PC entry marked `USB` on the **Computer** page, then select it.

The headset system must support this connection method. If the status shows **Unsupported**, **Unavailable**, or remains at **Waiting for cable**, check the system version, cable, and PC USB port. Use Wi-Fi if the device cannot provide a USB connection.

### 3.3 PICO USB

1. Use matching, up-to-date PC and PICO apps.
2. Enable developer options and USB debugging on the PICO headset.
3. Connect a USB data cable and authorize the PC in the headset.
4. Open both apps and select the PC entry marked `USB` on the headset's **Computer** page.

A PICO USB entry may show `127.0.0.1` as its address. Select it by the PC name and `USB` label; you do not need to replace that address with a Wi-Fi address. A USB status of **Detected** or **Connected** can be usable even when no Mbps value is shown.

### 3.4 Switch PCs or connection types

The same PC may appear as separate `WIFI` and `USB` entries. Open the **Computer** page and select the connection you want. The picture may pause briefly during the switch.

The list refreshes automatically. After disconnecting a cable or changing networks, wait for an available entry to reappear and select it. Connection speed describes the link; it is not the actual video bitrate and does not guarantee continuous streaming at that rate.

<a id="desktop"></a>

## 4. Desktop controls and virtual keyboard

### 4.1 Common controls

These controls apply to desktop mode. In a game, follow that game's SteamVR controller bindings.

| Action | Common Quest / PICO controllers | Steam Frame controllers |
| --- | --- | --- |
| Move the pointer | Point a controller at the desktop | Point a controller at the desktop |
| Left-click | Trigger, or right-hand A | Trigger, or right-hand A |
| Right-click | Right-hand B | Right-hand B |
| Drag a window | Hold the left-click control and move the pointer | Hold the left-click control and move the pointer |
| Scroll | Point at the desktop and move a thumbstick | Point at the desktop and move a thumbstick |
| Show / hide the menu | Press Menu once | Press the View menu button once |
| Switch Desktop / SteamVR view | Quickly press the same Menu button twice | Quickly press the same View menu button twice |
| Return from a game to the desktop menu | Hold Menu for about 1 second | Hold View for about 1 second |
| Open / close the virtual keyboard | Left-hand X in desktop mode | Right-hand X in desktop mode |
| Switch PC displays | Left-hand Y in desktop mode | Right-hand Y in desktop mode |
| Show / hide the performance overlay | Click both thumbsticks together | Click both thumbsticks together |

If a shortcut does not respond after reconnecting or switching modes, release the button and press it again. Button names may vary by controller; also check the headset menu's instructions.

Double-pressing Menu switches the view. Use the menu's SteamVR buttons when you want to start or close SteamVR itself.

### 4.2 Multiple displays and desktop size

When the PC has several displays, you can view the desktop in the headset and use the display-switching shortcut. Windows continues to manage the desktop windows.

Use the size toolbar above the desktop to make the desktop larger or smaller, where available. The supported range is 0.5–2×. If the toolbar is absent, first check that both apps are matching versions.

On the PC, **Streaming → Display settings → Keep desktop resolution** preserves the Windows resolution, refresh rate, and display arrangement. Enable it if you want your PC display settings to stay the same while connected. This is separate from the desktop's physical size in the headset.

### 4.3 Virtual keyboard

1. Click the field where you want to type on the desktop.
2. Use the keyboard shortcut or select **Virtual keyboard** in the menu.
3. Point at a key and press the trigger to type.
4. Close the keyboard when finished.

The keyboard includes Chinese and English layouts, navigation keys, copy and paste, and combinations using Shift, Ctrl, Alt, or Win. Modifier keys apply to the next key press. Chinese text entry also requires a suitable input method on the PC. Drag the handle below the keyboard to reposition it.

### 4.4 Passthrough

In the headset's **Settings**, enable either option as needed:

- **Passthrough when disconnected** shows your surroundings behind the connection menu.
- **Desktop passthrough** shows your surroundings outside the desktop window.

Passthrough requires device and system support. You cannot enable it when the option is unavailable. Desktop passthrough does not automatically turn SteamVR games into mixed reality applications.

<a id="steamvr"></a>

## 5. SteamVR games

### Start a game

1. Install Steam and SteamVR on the PC and sign in to Steam.
2. Connect the headset and check that desktop streaming works.
3. Open the headset menu, select **Start SteamVR**, and wait for SteamVR to be ready.
4. Start the game from Steam, SteamVR, or the desktop.

If SteamVR is already running when you connect, the headset may show the current game view immediately. Use the view-switching controls when you need the desktop.

### Return to the desktop or finish playing

- **Temporarily use the PC:** hold Menu for about 1 second in the game to return to the desktop and open the menu.
- **Return to a running game:** double-press Menu to switch to the SteamVR view.
- **Close SteamVR:** save and exit the game first, then use **Stop SteamVR** or SteamVR's exit control on the PC.

Changes such as resolution or preferred refresh rate may show a **SteamVR restart required** prompt. Choose **Later** to keep the current session, then save your game and restart SteamVR when ready to apply the new settings.

<a id="picture"></a>

## 6. Image quality and smoothness

Open **Streaming → Display settings** on the PC.

### 6.1 Common settings

| Setting | What it does and how to adjust it |
| --- | --- |
| Resolution | Higher tiers retain more detail and demand more from the PC and headset. Connect the headset to see the relevant sizes. Avoid tiers marked red as unsupported |
| Preferred framerate | Select the refresh rate you want. Higher rates require the whole system to deliver more frames consistently; actual headset support takes precedence |
| Video codec | Choose image-quality and compatibility options from the table below. Changing it reconnects the stream |
| Bitrate | Sets the VR video bitrate budget. Higher values may retain more detail but need a more stable connection; actual traffic varies with the picture |
| Automatically adjust VR bitrate | Adjusts to available network capacity when enabled; otherwise uses the selected budget. Keep it enabled for initial setup or a fluctuating connection |
| Desktop streaming bitrate | Sets a separate desktop bitrate limit, up to 150 Mbps. Actual bitrate can still drop when the connection is insufficient |
| Clarity enhancement | Disabled / Balanced / Sharp. Balanced is subtler; Sharp emphasizes detail. Available for SteamVR SDR, not desktop or HDR |
| Gamma fine-tuning | 1.00 keeps the original midtones; higher values brighten them and lower values darken them. Keep 1.00 if the image looks correct |
| Global FSR | Trades some detail for reduced graphics load. Quality options favor clarity; Performance favors smoothness. Not available for HDR |
| Video buffering | Helps with network fluctuations when enabled. Disabling it may reduce latency but can make an unstable connection stutter more |
| Missing-frame smoothing | Reduces visible interruptions when video arrives late. It does not replace a stable connection or improve the game's own performance |
| Keep desktop resolution | Preserves Windows display settings; see [desktop controls](#desktop) |

Global FSR offers Highest quality, Ultra quality, Quality, Balanced, and Performance. The multipliers in the interface distinguish quality levels; they are not promised frame-rate increases.

### 6.2 Choose a video format

| Format | When to use it |
| --- | --- |
| HEVC | The default, balancing image quality and bandwidth |
| H.264 | An option to try when you encounter compatibility problems |
| H.264+ | Offers higher selectable bitrates and needs sufficient network and device capacity |
| HEVC-10Bit | Provides 10-bit color without enabling HDR. If ordinary HEVC has compatibility problems, try this only when your devices support it |
| AV1 | Requires support from both the PC GPU and headset |

Connect the headset to check available formats and compatibility notices. Steam Frame currently uses H.264 / HEVC. A format's name alone does not guarantee better image quality or lower latency.

### 6.3 Adjust for your goal

| Goal | Things to try, in order |
| --- | --- |
| Establish a stable stream | Keep defaults → enable automatic VR bitrate adjustment → lower bitrate or resolution |
| Read desktop text more clearly | Check Windows display resolution and scaling → adjust desktop size in the headset → moderately raise desktop bitrate |
| Improve game detail | Moderately raise resolution → try Balanced clarity enhancement → raise bitrate if the connection allows |
| Help a game that struggles to run | Lower the game's quality or resolution → select a lower refresh rate → try Global FSR |
| Handle occasional network fluctuations | Enable automatic VR bitrate adjustment and video buffering, lower bitrate, and improve the wireless connection |
| Reduce input delay | First reduce excessive resolution or bitrate; once the connection is stable, compare with buffering or frame generation disabled |

Change one setting at a time. In the same game scene, check text, quick head turns, hand movement, and input response. If a setting causes ghosting, worse image quality, or more noticeable delay, restore the previous value.

<a id="gaze"></a>

## 7. Foveated streaming

Open **Streaming → Display settings → Foveated streaming** on the PC.

This feature prioritizes detail around your gaze while allowing reduced peripheral detail. It can follow valid eye tracking; without valid gaze data, it uses the center of the image. Available behavior depends on the headset and PC.

### Set it up

1. If you use an eye-tracking device, enable eye tracking and complete calibration in the appropriate software or headset settings.
2. Under **Foveated streaming**, select **Latency and bitrate priority** or **Clarity priority**.
3. Read the status text to check whether gaze following is active or the image center is being used.
4. Start with a medium gaze region, then adjust the options below while checking text and scene detail.

| Option | Effect |
| --- | --- |
| Disabled | Turns the feature off |
| Latency and bitrate priority | Favors responsiveness and bandwidth savings |
| Clarity priority | Favors detail around the gaze region |
| Gaze region size | Very small to Very large. Larger regions help with quick glances; smaller regions use less bandwidth |
| Peripheral compression strength | 0–50. Higher values may make the periphery blurrier; 0 is the lowest compression |
| Gaze region clarity | 0–12. Higher values emphasize gaze-region detail and may increase bitrate; 0 preserves the original quality |
| Gaze debug | Shows a cyan outline of the clear region on supported streams so you can check its position and size |

For an external Cymple eye tracker, enable precise mode and complete precise calibration in Cymple. If the clear region does not match your gaze, check permissions, calibration, and the status message. Turn the outline off after checking it.

<a id="frame-generation"></a>

## 8. Frame generation

Open **Streaming → Display settings → Frame generation** on the PC.

Frame generation can make motion appear more continuous. It currently applies to **SteamVR SDR game streaming**, not desktop mode or HDR. It does not increase the game's own speed by the same factor and cannot guarantee that stutter will disappear.

### Set it up

1. Start with frame generation disabled and check that the game and connection are stable.
2. Set **Frame generation** to **Enabled** and wait for the brief reconnection.
3. Select **Frame generation scheduling** and **Frame generation method**. For a first comparison, start with **Dynamic + Frame interpolation**.
4. Compare quick head turns, hand movements, thin lines, subtitles, and menus, as well as input response.

| Option | What changes |
| --- | --- |
| Scheduling: Dynamic | Keeps the game's original target frame rate while trying to improve visual smoothness |
| Scheduling: Static | Sets the game's target rate to half the headset refresh rate: for example, 45 FPS at 90 Hz. It may increase input delay |
| Method: Frame interpolation | Adds transitions between game frames. Fast movement and occlusion may still show ghosting |
| Method: Frame extrapolation | Attempts to add upcoming motion. Sudden direction changes or fast actions may show prediction errors |

Static mode's target does not guarantee the game will sustain that rate or that the headset will always show a full refresh rate of new images. If hands leave trails, text distorts, the image flickers, or response feels slower, disable frame generation and compare again.

<a id="audio"></a>

## 9. Audio and voice

Open **Streaming → Audio and voice** on the PC.

### 9.1 Hear PC audio in the headset

1. Enable **Computer audio**.
2. Play something on the PC and check that you can hear it in the headset.
3. Adjust **VR volume** and check the headset's own volume.

**Automatically mute PC speakers/headphones** is enabled by default: the PC is muted while connected and the headset keeps playing. The previous state returns after disconnecting or exiting. Disable this option if you want both the PC and headset to play sound.

### 9.2 Use the headset microphone in a game

1. Allow Cymple Streamer to use the headset microphone.
2. Enable **Microphone passthrough**.
3. Select an available **Virtual microphone**. With the default VB-CABLE device, choose **CABLE Output** as the recording device in the game.
4. Test recording in the game or chat app and check its mute or push-to-talk settings.

The first VB-CABLE installation may require a Windows restart. If the device is unavailable, finish installation and restart if requested, then click **Refresh devices**.

With **Automatically select microphone** enabled, streaming automatically selects the corresponding Windows default recording device. Disabling it still allows headset microphone audio, but you must select the microphone in the game yourself. After streaming ends, Cymple restores the selection it changed while preserving any device choice you made manually during the session.

If you use an existing VoiceMeeter or similar setup, enable the required channels in that software as well.

### 9.3 Speech recognition versus a game's microphone

When **Extra features** uses **VR (headset microphone)** as its audio input, keep the stream connected, allow microphone access, and enable microphone transmission. You do not need to select a Windows virtual microphone on the speech-recognition page. To let a PC game hear the microphone, select the game's recording device as described above.

<a id="tracking"></a>

## 10. Input and tracking

Open **Streaming → Input and tracking** on the PC.

| Feature | How to use it | Requirements and limits |
| --- | --- | --- |
| Hand tracking | Allow hand tracking in the headset system, then enable Hand tracking in the app | The device and game must support it. Seeing finger movement does not mean every game supports playing without controllers |
| Eye and face tracking | Grant permissions, calibrate the device, and select the appropriate Face tracking output | Capabilities depend on the hardware. An eye tracker alone does not provide full facial expressions |
| Full body tracking | Pair and calibrate the supported device or trackers, then enable Full body tracking | Complete body calibration in the game too. Enabling the option does not add real full body tracking to a device without that capability |

**Face tracking** offers:

- **VRChat Eye OSC:** for compatible VRChat eye movement features. Enable OSC as required by the game.
- **VRCFaceTracking (Cymple):** requires VRCFaceTracking, its corresponding Cymple plugin, and an avatar that supports the relevant expressions.

Foveated streaming, avatar eye movement, and facial expressions are separate features. Check the clear region, eye movement, and expressions separately. A PC-side switch alone does not establish that a tracking feature is available on Steam Frame or another headset.

<a id="speech"></a>

## 11. Speech and translation

Open **Extra features → Speech and translation** on the PC.

| Feature | Languages |
| --- | --- |
| Speech to text | Chinese, English, Japanese, Korean, Russian |
| Text translation | Translation between those five languages |
| VRChat chatbox output | One or more of those five languages |
| Text to speech | Chinese, English, and mixed Chinese / English text |

Download the required models from the page before first use. Recognition, translation, and speech playback can then work offline. Device and feature preferences are saved; transcripts and translation input and output are not stored in settings. Copy any text you want to keep.

### 11.1 Download what you need

| What you want to do | Prepare this on the page |
| --- | --- |
| Manually select Chinese, English, Japanese, or Korean recognition | The Chinese / English / Japanese / Korean recognition model |
| Manually select Russian recognition | The Russian and automatic-detection recognition model |
| Detect the spoken language automatically | Both recognition models above |
| Translate text or send translated chatbox messages | Download translation model |
| Read text aloud | The Chinese / English model under Text to speech |

Retry a failed download. If downloaded content does not work, use **Reinstall model**. Recognition, translation, and text to speech are separate features; prepare only the parts you plan to use.

### 11.2 Speech to text

1. Check **Enable speech to text**.
2. Choose **Audio input**: use **VR (headset microphone)** for the headset, or **System default microphone** / a specific PC device.
3. Choose **Input language**. Select it manually if automatic detection struggles with short or mixed-language phrases.
4. Confirm the models are downloaded, then click **Start recognition** or hold your selected controller shortcut.
5. Speak normally and pause briefly between sentences. Release the shortcut to stop recording and finish the last sentence.

The default shortcut is **left-hand X**. You can change it to left-hand Y, right-hand A, or right-hand B. It continues to work while connected if you switch pages or minimize the PC app. After reconnecting, release the button before holding it again.

The page retains the last five recognized sentences. Use **Copy text**, **Clear**, or **Use in text to speech** as needed. Unchecking **Enable speech to text** stops recording. Short phrases, accents, and mixed languages can cause recognition errors; check the text when accuracy matters.

### 11.3 Translate text manually

1. Under **Translate between five languages**, download the translation model.
2. Choose different **From** and **To** languages.
3. Type or paste text, or click **Use transcript**. Manual input is limited to 512 characters per request; split longer text into sections.
4. Click **Translate**, then copy or edit the result. Chinese and English translations can be sent to **Use in text to speech**.

The page also provides **Cancel translation** and **Release memory**. Start with the default settings. If you already have **Hy-MT2 · Local server** configured, select it under **Translator** and enter its address. This option requires you to prepare the service yourself; follow the page's **Server setup** link.

### 11.4 Send recognized speech to the VRChat chatbox

1. In VRChat's Action Menu, enable **OSC → Enabled**. See the [official VRChat instructions](https://docs.vrchat.com/docs/osc-overview#enabling-it).
2. In Cymple Streamer, enable **Send directly to VRChat over OSC**.
3. Select at least one **Output language**. Download the translation model first if you want languages other than the recognized source language.
4. Hold the speech shortcut, say a sentence, and pause to check the chatbox result.

You can select several output languages. Long messages appear over multiple pages. A sentence may not be sent if part of its translation fails; check the page for an error. Turning OSC off or changing output settings cancels older pending messages.

Even when the app reports that a message was sent, check that it actually appears in the game. Whether other players see it also depends on VRChat's chatbox settings. Recognized speech may be shared directly with other players, so use a short test sentence before normal use.

### 11.5 Text to speech

1. Download the model required by **Text to speech**.
2. Enter Chinese, English, or mixed Chinese / English text, up to 2,000 characters at a time.
3. Choose **Output device** and **Speech language**, then adjust speed and volume as needed.
4. Click **Play speech**. Use **Stop playback** to interrupt it.

To let VRChat or another game hear the speech, select a virtual audio device's playback endpoint as the output, then select its recording endpoint in the game. For example, send speech to **CABLE Input** and select **CABLE Output** as the game microphone. To listen privately, select ordinary headphones or speakers.

<a id="performance"></a>

## 12. Performance overlay

Use **Settings → Performance Overlay** in the headset, or click both thumbsticks together. Release both thumbsticks before clicking them again to toggle it.

| Item | How to read it |
| --- | --- |
| Framerate | The rate of new video images shown in the headset. It may include generated images when frame generation is enabled, so it is not the game's own FPS |
| Target framerate | The target refresh rate. Choosing 90 Hz does not guarantee the game runs at 90 FPS |
| Latency | The streaming latency reported by the app; consider it alongside actual input response |
| Game / Encoding / Networking / Decoding | Related latency measurements that help identify which part changed |
| Frame queue / Display wait | Image waiting times; do not judge the overall experience by one value alone |
| Bitrate | Actual video bitrate, which changes with the scene and connection |
| Max bitrate | The configured bitrate budget, shown separately from actual bitrate |
| Connection | Connection type and the link speed when available |
| Graphics Quality / Render resolution | Current quality tier and rendering settings |
| Frame generation / Video buffering | Current generation and buffering status |
| GPU / Headset / Software version | Device and version information to include in a problem report |

A value of `--` usually means valid data is not currently available. Compare settings in the same game, scene, and viewing position, considering image quality, smoothness, latency, and interruptions together. A higher overlay frame rate alone does not prove better game performance.

<a id="maintenance"></a>

## 13. Updates and maintenance

### Update the apps

- **Windows:** when an update appears, select **Download update**. Save your game, end the stream, and close SteamVR before running the new installer.
- **Android:** when the headset-app update prompt appears, download the matching APK and install it on the headset. Downloading alone does not install it.
- **Steam Frame:** connect the device to the dedicated installer and select **Update**.

Check versions under **About** on both devices. After updating, confirm that the apps are matching versions and reconnect.

### Drivers and firewall

The PC app's **Installation** page provides **Install / update streaming driver** and **Add firewall rules**. If SteamVR does not recognize the headset, close SteamVR before installing or updating the driver. If the PC cannot be discovered, check the firewall rules.

Windows may request permission for these actions. End the current game before driver maintenance and avoid removing unrelated device drivers.

### Uninstall

- Remove the Windows PC app through Windows' installed-apps list.
- Remove the Android app through the headset's app manager.
- Use **Uninstall** in the dedicated Steam Frame installer.

The shared VB-CABLE audio device is not automatically removed with the PC app. Keep it if other software still uses it.

<a id="troubleshooting"></a>

## 14. Troubleshooting

| Symptom | Check first |
| --- | --- |
| The headset cannot find the PC | Is the PC app open? Are both devices on the same local network? Check guest Wi-Fi, device isolation, firewall access, and VPN interference |
| USB only charges; no PC entry appears | Try a data cable or another PC USB port. Keep the headset awake. Check Quest USB networking prompts or PICO USB debugging authorization |
| PICO USB shows no connection speed | Look for a USB PC entry and Detected / Connected status. A missing Mbps value does not necessarily mean the connection is unavailable |
| The Steam Frame installer cannot find the device | Enable Developer Mode, check the cable and authorization, click Refresh devices, and read the operation log |
| Steam Frame does not open automatically after installation | Launch its Devkit Game from Library → Non-Steam, then select a PC manually |
| Audio works but the image is black or incorrect | Lower the resolution, check video-format support, try HEVC or H.264, confirm matching app versions, and reconnect |
| SteamVR will not start or does not recognize the headset | Check desktop streaming first. Close SteamVR and install / update the streaming driver from Installation. Check whether SteamVR has blocked the Cymple add-on |
| Desktop works but games stutter | Lower game quality, resolution, or target refresh rate. Check the game's own performance and temporarily disable frame generation for comparison |
| High network latency or frequent interruptions | Enable automatic VR bitrate adjustment and lower bitrate. Use Ethernet for the PC, move nearer the router, and pause large network transfers |
| Blurry desktop text | Check Windows resolution and scaling, adjust desktop size in the headset, and moderately increase desktop bitrate |
| Ghosting around hands or text with frame generation | Compare another generation method or disable it. Do not judge the result only by the overlay's frame rate |
| The clear region does not follow gaze or is misplaced | Check eye-tracking hardware, permissions, calibration, and whether the app is using the image center. Check precise mode for an external Cymple tracker |
| The PC is silent but the headset has sound | Check Automatically mute PC speakers/headphones; disable it to hear the PC |
| No PC audio in the headset | Enable Computer audio and check VR volume, headset volume, and whether the PC app playing sound is muted |
| The game cannot hear the headset microphone | Check permissions and Microphone passthrough, confirm the virtual device is available, and choose CABLE Output for the default setup |
| Speech recognition will not start | Enable speech to text, download the required models, and check the input source. VR input requires an active stream and microphone transmission |
| Automatic language detection is often wrong | Select the language manually and avoid very short or continuously mixed-language phrases |
| Nothing appears in the VRChat chatbox | Check VRChat OSC and chatbox settings, Cymple's OSC switch and output languages, and translation-model readiness or page errors |
| Only you can hear text-to-speech output | Send speech to the virtual playback endpoint and choose its recording endpoint in the game, such as CABLE Input / CABLE Output |
| A changed setting has no effect | Check for a reconnection or SteamVR restart prompt. Save your game before restarting, and verify device support |
| Logs show warnings and errors but not the full sequence | The PC Logs page shows important messages. Use Open log folder or export a diagnostic bundle for more information |

If the problem remains, note when it happened and the steps that caused it, then follow the feedback section. Save relevant logs promptly before they expire.

<a id="feedback"></a>

## 15. Logs and feedback

### View and save logs

The PC app's **Logs** page provides **Refresh**, **Copy all**, and **Open log folder**. The headset's **Log** page shows connection information. For Steam Frame installation problems, use the installer's **Operation log**.

Application logs on Windows, Android, and Steam Frame are retained for the most recent **48 hours**. Save relevant records promptly when investigating a problem.

### Export or send feedback

Open **Feedback** on the PC.

1. Select **Bug report** or **Improvement suggestion**.
2. Describe the symptoms, reproduction steps, and expected result. Contact details are optional.
3. Add screenshots or other attachments if useful. The page explains which logs and settings the diagnostic bundle includes.
4. To inspect it first, click **Export bundle (no email)**, then **Open bundle folder**.
5. When ready to send, check the contents and attachments, select the consent checkbox, and click **Send feedback**.

Logs and settings can contain device, network, and local path information. Additional attachments are sent as their original files. Check what you intend to share. If delivery cannot be confirmed, contact the maintainer before immediately sending again.

Include the following when reporting a problem:

- PC and headset app versions.
- Headset and GPU models, and whether the connection is Wi-Fi or USB.
- Desktop or SteamVR mode, and the game name where relevant.
- Resolution, refresh rate, codec, bitrate, and whether frame generation or foveated streaming is enabled.
- The time of the problem, reproduction steps, relevant screenshots, and the diagnostic bundle.
