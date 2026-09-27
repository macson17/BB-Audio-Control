<p align="center">
  <img src="screenshots/bb-audio-control-logo.png" width="190" alt="BB Audio Control">
</p>

<h1 align="center">BB Audio Control</h1>

<p align="center">
  <strong>Your Windows audio mixer on a tablet or smartphone.</strong><br>
  Control volume, audio outputs, microphone, and media directly over your local network.
</p>

<p align="center">
  <img alt="Version 1.0.0" src="https://img.shields.io/badge/Version-1.0.0-ff9f0a?style=for-the-badge">
  <img alt="Windows 10 and 11 x64" src="https://img.shields.io/badge/Windows-10%20%7C%2011-1672d4?style=for-the-badge&logo=windows11&logoColor=white">
  <img alt="Local network without cloud" src="https://img.shields.io/badge/Connection-Local%20without%20cloud-16b985?style=for-the-badge">
</p>

<p align="center">
  <a href="https://github.com/macson17/BB-Audio-Control/releases/tag/v1.0.0"><strong>Download BB Audio Control 1.0.0</strong></a>
  ·
  <a href="#installation">Installation</a>
  ·
  <a href="CHANGELOG.md">Changelog</a>
  ·
  <a href="README-DE.md">Deutsch</a>
</p>

<p align="center">
  <img src="screenshots/v1.0.0-tablet-dashboard.png" alt="BB Audio Control 1.0.0 tablet dashboard" width="100%">
</p>

## A responsive mixer for your Windows PC

BB Audio Control turns an iPad, Android tablet, or smartphone into a direct
remote control for a Windows PC. No cloud account is required: the PC and
mobile device communicate directly on the local network.

| Control each application | Route audio freely | Control active media |
|---|---|---|
| Adjust volume and mute for up to five active applications | Switch the main output or assign a separate output to an individual app | View title, artist, and artwork and control Spotify, YouTube, and other active media |

## Get started in three steps

1. Download and install the current Windows setup from the [1.0.0 release](https://github.com/macson17/BB-Audio-Control/releases/tag/v1.0.0).
2. Open BB Audio Control and scan the QR code with the tablet or smartphone.
3. Enter the displayed six-digit PIN and optionally add the interface to the home screen.

> [!NOTE]
> The PC and mobile device must be on the same reachable network. Communication
> stays local; BB Audio Control does not require an external cloud service.

> [!WARNING]
> The installer is not digitally signed yet. Windows SmartScreen may display
> an “Unknown publisher” warning. Only use files downloaded from this repository.

## Version 1.0.0 at a glance

<table>
  <tr>
    <td width="50%"><img src="screenshots/v1.0.0-tablet-app-output.png" alt="Choose an output for an individual application"></td>
    <td width="50%"><img src="screenshots/v1.0.0-tablet-edit-mode.png" alt="Customize outputs and applications in Edit mode"></td>
  </tr>
  <tr>
    <td align="center"><strong>Output per application</strong><br>Follow the system default or route an individual application to another device.</td>
    <td align="center"><strong>Customizable interface</strong><br>Reorder, rename, style, show, or hide outputs and applications.</td>
  </tr>
  <tr>
    <td width="50%"><img src="screenshots/v1.0.0-tablet-color-picker.png" alt="Custom colors and brightness"></td>
    <td width="50%"><img src="screenshots/v1.0.0-tablet-background-picker.png" alt="Choose a background color or custom image"></td>
  </tr>
  <tr>
    <td align="center"><strong>Colors and brightness</strong><br>Use a preset or select any custom color and brightness.</td>
    <td align="center"><strong>Your own background</strong><br>Use a preset, custom color, or image on every paired device.</td>
  </tr>
</table>

<details>
<summary>Smartphone and earlier interface views</summary>

![Phone portrait layout](screenshots/v0.10.0-phone-portrait.png)
![Phone landscape layout](screenshots/v0.10.0-phone-landscape.png)
![Earlier large tablet layout](screenshots/v0.10.0-tablet.png)
![Earlier compact tablet layout](screenshots/v0.10.0-compact-tablet.png)

</details>

## Features

- Master volume and master mute across active outputs, restoring their previous mute states
- Per-application volume and mute for each audio output
- Switch the Windows default audio output
- Select an optional output for an application by tapping its app icon; System default continues to follow the main output buttons
- Control the active Windows media session with artwork, title, artist, previous,
  next, and immediately responding state-aware play/pause controls; this can
  also pause YouTube in a browser
- Mute and unmute the microphone
- Change the microphone input by holding the microphone button
- Show, hide, and reorder up to five applications
- Global and per-application fader colors with custom colors and brightness
- Custom output names, icons, and colors
- Four background presets, custom background colors with brightness, and a
  centrally stored custom background image for paired devices
- German and English interface
- PIN pairing and a locally generated QR code
- CPU, GPU, and RAM information on tablets where supported by the system
- Responsive controls over WebSocket on the local network
- Select any active local IPv4 address in the Windows settings window; QR code, copy, and browser actions follow the selection

## Requirements

- Windows 10 build 19041 or later, or Windows 11
- 64-bit Windows on an x64-compatible system
- Tablet or smartphone with a current web browser
- PC and tablet on the same reachable private network

No separate .NET runtime installation is required on the target PC.

## Installation

1. Download `BB-Audio-Control-Setup-v1.0.0.exe` from the
   [1.0.0 release](https://github.com/macson17/BB-Audio-Control/releases/tag/v1.0.0).
2. Start the setup file and select German or English.
3. If SmartScreen displays a warning, select "More info" and then "Run
   anyway" only if the file came from this repository.
4. Disable the preselected startup option if you do not want the app to start
   with Windows.
5. Confirm the Windows prompt for the private-network firewall rule.
6. In the PC settings window, scan the QR code or open the displayed local
   address on the tablet.
7. Enter the six-digit pairing code.

See the [English installation guide](README-Installation.md) or the
[German installation guide](README-Installation-DE.md) for more details.

## Updates

Run a newer setup file over the existing installation. Settings and the
pairing code are retained. A normal uninstall also keeps these personal
settings for a later reinstall.

## Security and privacy

BB Audio Control does not use a cloud service. Communication stays on the
local network, and control access requires a six-digit pairing code. Creating
a new code disconnects existing clients and immediately invalidates the old
code.

Communication currently uses HTTP and WebSocket without transport encryption.
The pairing code and control commands could be observed on a compromised local
network. Only use the application on a trusted private network.

See [SECURITY.md](SECURITY.md) for details.

## Known limitations

User-reported display checks passed on **iPad, TABWEE T80, iPhone 16 Pro, and
Samsung Galaxy S21 Ultra**. These are display checks, not a claim that every
audio, hardware, or PWA scenario was tested.

On tablets, title and artist information plus media controls are shown for the
active Windows media session. Tap an application's icon to choose its optional
audio output. The complete media section remains hidden on phones.

- Snapdragon/ARM systems have not yet been fully tested.
- GPU usage and temperature depend on Windows and the graphics driver.
- `– °C` means that no supported temperature value is available.
- Phones do not display output tiles or CPU, GPU, and RAM information.
- On phones, holding Sound opens the output selection; tapping it mutes or
  unmutes the sound.
- The normal tablet view does not scroll; Edit mode and very short phone viewports may scroll when necessary.
- Version 1.0.0 uses direct Windows D3DKMT adapter enumeration for GPU
  temperatures; the application path was practically verified on an AMD
  Radeon 780M.
- A maximum of five applications can be displayed at the same time.
- Applications appear only after Windows reports an active audio session.
- Guest-network isolation, VPN software, or a firewall may block the tablet
  connection.
- The local PC address may change after switching networks.
- The installer is not digitally signed yet.
- Automatic updates are not available yet.

See the [changelog](CHANGELOG.md) for further changes.

## Issues and feature requests

Use [GitHub Issues](https://github.com/macson17/BB-Audio-Control/issues) for
reproducible bug reports and feature requests. Never publish pairing codes,
real local IP addresses, computer names, user paths, or other personal data.

## Source code and third-party components

This public repository is intended only for product information, support, and
binary downloads. The BB Audio Control source code is proprietary and is not
published. This is not an open-source project, and this repository deliberately
does not provide an open-source license for the application's own code.

The installer includes the required license and copyright notices for its
third-party components, including NAudio, QRCoder, and the bundled .NET runtime.
