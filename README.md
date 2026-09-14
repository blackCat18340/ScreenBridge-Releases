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

Create up to four independent Windows displays and assign each one to a
different Android device. Every display has its own resolution, refresh rate,
codec, bitrate, transport, orientation, and touch configuration.

- Native device resolution and landscape or portrait display modes
- <code>50</code>, <code>60</code>, <code>90</code>, <code>120</code>,
  <code>144</code>, and <code>165 FPS</code> options, capped by the receiver's
  native refresh rate
- DXGI Desktop Duplication and D3D11 processing with H.264 or HEVC hardware
  encoding
- Android MediaCodec hardware decoding with aspect-preserving presentation
- Direct touch input with Windows cursor feedback
- Independent USB or local Wi-Fi sessions

ScreenBridge has been tested on NVIDIA GeForce RTX 3070 Ti, NVIDIA GeForce
RTX 5080, and Intel Iris Xe Graphics. Achievable resolution and refresh rate
still depend on the hardware encoder, Android decoder, power mode, and link
quality.

**Virtual display demo**

https://github.com/user-attachments/assets/a8c16f68-1d61-40cc-97c3-aa55971791f8

### Touchpad

Use an Android touchscreen as a dedicated Windows touchpad without creating a
virtual display.

- Pointer acceleration, tap-to-click, tap-and-drag, and optional three-finger
  drag
- High-resolution two-finger scrolling, pinch zoom, and haptic feedback
- Browser back and forward navigation
- Three- and four-finger Windows gestures
- Palm rejection, physical-size calibration, and adaptive pointer filtering
- Virtual HID input on elevated Windows surfaces and secure confirmation
  prompts

### Media Panels

Turn one or more USB-connected Android devices into persistent media panels
for a PC case, desk, or other fixed installation. Media panels do not create a
Windows display or run the desktop video encoder.

- Multiple saved panels with persistent device assignments
- Managed image, animation, and video library
- Layered layouts with position, size, rotation, opacity, crop, and fit controls
- Automatic startup and USB reconnect
- Independent content and layout for every panel

**Media panel demo**

https://github.com/user-attachments/assets/e3a7b35f-6b84-472d-9483-05761e4b38f4

### Connections and Android Receiver Management

- Direct USB transport and low-latency local Wi-Fi transport
- Six-digit first-connection pairing with separate remember choices on
  Windows and Android
- Authenticated Wi-Fi pairing with encrypted control and video traffic
- Receiver discovery and user-confirmed installation over USB
- Local QR download for installing the Android receiver without a USB cable
- Receiver version discovery and authenticated in-app updates over Wi-Fi
- Persistent display, touchpad, media panel, and device assignments

### Performance and Diagnostics

- Event-driven capture and a bounded shared GPU texture pool that avoid
  duplicate idle frames and stale-frame backlogs
- Paced Wi-Fi video transport with packet reordering and adaptive Reed-Solomon
  packet-loss recovery
- End-to-end Wi-Fi metrics that separate transport, MediaCodec decode, and
  Android presentation latency
- Structured logs with severity, component, session, transport, time, and text
  filters in the Windows settings dialog

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
