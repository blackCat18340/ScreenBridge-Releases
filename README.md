<p align="center">
  <img src="assets/screenbridge-windows.png" alt="ScreenBridge" width="160">
</p>

<h1 align="center">ScreenBridge</h1>

<p align="center">
  <strong>Turn your Android device into a second screen, touchpad, media panel, or control deck for Windows.</strong>
</p>

<p align="center">
  <strong>English</strong> | <a href="README.zh-TW.md">繁體中文</a>
</p>

<p align="center">
  <a href="https://github.com/blackCat18340/ScreenBridge-Releases/releases/download/v0.9.0/ScreenBridge-0.9.0-win-x64-setup.exe">Download for Windows · 0.9.0</a>
</p>

ScreenBridge gives your Android phone or tablet another job at your desk.
Extend your Windows desktop, control the pointer with touch, display media
and hardware readings, or build a control deck for the apps you use every day.
The Deck also works directly on Windows.

Current release: **0.9.0**. [What's new](https://github.com/blackCat18340/ScreenBridge-Releases/releases/tag/v0.9.0)
· [All releases](https://github.com/blackCat18340/ScreenBridge-Releases/releases)

## Features

### Second screen

Create up to four independent Windows displays, each assigned to an Android
device. Set the resolution, orientation, refresh rate, and image quality for
each screen. Connect over USB or local Wi-Fi and use the touchscreen to
interact with Windows.

- Native device resolutions, in landscape or portrait
- 50, 60, 90, 120, 144, and 165 FPS options, limited by the device's refresh rate
- H.264 and HEVC on supported hardware

**Virtual display demo**

https://github.com/user-attachments/assets/d35894fd-10f0-4a94-9480-b9b4f3ed1321

### Touchpad

Use your Android touchscreen as a Windows touchpad, with tap-to-click,
dragging, two-finger scrolling and zoom, browser navigation, and three- and
four-finger gestures. Pointer controls also work on elevated Windows screens.

### Media panels

Give a USB-connected Android device a permanent place on your desk or inside
your PC case. Combine images, animations, and video in layered layouts, and
add hardware readings for CPU, GPU, memory, storage, and network activity.
Save multiple panels with their own content and reconnect them automatically.

**Media panel demo**

https://github.com/user-attachments/assets/100bfb60-0fad-40a2-a161-0e92730b7cb8

### Control deck

Put shortcuts, music, sound effects, lights, and hardware readings within
reach. Arrange your own keys, pages, icons, and labels, then switch layouts
automatically when you change Windows apps.

- Launch apps, type text, run shortcuts, and control OBS scenes or recording.
- Browse Spotify tracks, control playback, and adjust volume.
- Play sound effects with your voice through your original microphone.
- Switch smart lights and adjust brightness, temperature, and colour.
- Set separate short-press, double-press, and long-press actions for each key.
- Back up and share layouts with `.sbdeck` files.

Use the Deck on Android over USB or encrypted Wi-Fi, or press
`Ctrl+Shift+Space` to bring up the always-on-top desktop Deck at your pointer.
Desktop Key Size adjusts the desktop Deck without changing the phone layout.

**Virtual Deck demo**

https://github.com/user-attachments/assets/66043f70-a838-4114-9e4b-23f26a99b960

## Install and start

1. Download [ScreenBridge-0.9.0-win-x64-setup.exe](https://github.com/blackCat18340/ScreenBridge-Releases/releases/download/v0.9.0/ScreenBridge-0.9.0-win-x64-setup.exe)
   and run the installer.
2. Connect Android over USB with USB debugging enabled, or put Windows and
   Android on the same local network. ScreenBridge can install the receiver
   over USB; without a cable, open **Settings > Android app > Get app** and
   scan the QR code.
3. Keep the Android receiver open. In ScreenBridge, select `+` and choose
   **Display**, **Touchpad**, **Media Panel**, or **Virtual Deck**.
4. Select the device and settings, start the session, and confirm the matching
   pairing code on both devices when connecting for the first time.

The installer includes the Windows app, display and input drivers, microphone
audio components, Android receiver, and USB tools. A separate .NET runtime
installation is not required.

### Sound effects in voice apps

Select your physical microphone in Deck settings and keep the same microphone
selected in your voice app. Add sounds to your Deck keys. Each sound action
supports 0–200% volume; the computer-wide soundboard master in Deck settings
supports 0–100%. Local playback follows the Windows default output.

### Connect Spotify

Register an app in the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/create)
using your Spotify Premium account. Set its Redirect URI to
`http://127.0.0.1:28187/spotify/`, then enter its Client ID in ScreenBridge's
**Connect Spotify** dialog and authorise your account.

## Requirements

- Windows 11 x64
- Android 11 or later for phone and tablet modes
- Administrator access for installation
- A data-capable USB cable with USB debugging, or a shared local IPv4 network
- For virtual displays: a GPU with H.264 hardware encoding; HEVC also requires
  decoding support on Android

For Wi-Fi streaming, use a local 5 GHz or 6 GHz connection with low interference.
Media panels use USB.

> [!NOTE]
> The Windows installer is not Authenticode-signed. Display and input drivers
> use a development test certificate; the Android receiver uses the ScreenBridge
> release signature.

Installer hashes and the packaged file manifest are available with the
[v0.9.0 release attachments](https://github.com/blackCat18340/ScreenBridge-Releases/releases/tag/v0.9.0).
