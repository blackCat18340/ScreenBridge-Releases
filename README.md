<p align="center">
  <img
    src="assets/screenbridge-windows.png"
    alt="ScreenBridge"
    width="180">
</p>

<h1 align="center">ScreenBridge Downloads</h1>

<p align="center">
  <strong>Turn an Android device into a Windows display, touchpad, or media panel.</strong>
</p>

<p align="center">
  <strong>English</strong> |
  <a href="README.zh-TW.md">繁體中文</a>
</p>

## Download

Download the latest <code>ScreenBridge-&lt;version&gt;-win-x64-setup.exe</code>
from [ScreenBridge Releases](https://github.com/blackCat18340/ScreenBridge-Releases/releases/latest).

The self-contained installer includes the Windows application, ScreenBridge
virtual display and input drivers, Android receiver, USB transport tools, and
uninstaller. Setup does not require users to install a separate .NET runtime.

## Features

### Virtual Displays

- Up to four independent Windows virtual displays
- USB or authenticated local Wi-Fi transport
- Native Android resolution with landscape and portrait modes
- H.264 and HEVC hardware encoding
- High-refresh-rate streaming and direct Android touch input

**Virtual display demo**

https://github.com/user-attachments/assets/a8c16f68-1d61-40cc-97c3-aa55971791f8

### Touchpad

- Pointer movement, clicking, dragging, scrolling, and pinch zoom
- Browser back and forward navigation
- Three- and four-finger Windows gestures
- Palm rejection, haptic feedback, and optional three-finger drag
- Virtual HID input for elevated Windows surfaces and secure prompts

### Media Panels

- Multiple independent USB media panels
- Managed image, animation, and video library
- Layered layout editor with crop and fit controls
- Persistent device assignments, automatic startup, and USB reconnect

**Media panel demo**

https://github.com/user-attachments/assets/e3a7b35f-6b84-472d-9483-05761e4b38f4

## Requirements

- Windows 11 x64
- Android 11 or later
- A GPU with hardware H.264 encoding support; HEVC requires compatible
  hardware on both Windows and Android
- A data-capable USB connection with Android USB debugging, or both endpoints
  connected to the same local IPv4 network
- Administrator access for driver installation

For Wi-Fi, use a low-contention 5 GHz or 6 GHz local connection.

> [!NOTE]
> The Windows setup executable is not Authenticode-signed. ScreenBridge
> virtual display and input drivers use a development test certificate, while
> the bundled Android receiver uses the stable ScreenBridge release signature.

Source code, build instructions, and architecture documentation are available
in the [ScreenBridge repository](https://github.com/blackCat18340/ScreenBridge).
