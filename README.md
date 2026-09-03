# BB Audio Control

Current test version: **0.10.0 Beta** (pre-release).

[English](README.md) | [Deutsch](README-DE.md)

BB Audio Control turns an iPad, Android tablet, or smartphone on your local network into a
clean audio mixer for a Windows PC. Control volume, mute states, audio outputs,
and the microphone without leaving your current game or application.

> **Beta:** BB Audio Control is still being tested. The current installer is
> not digitally signed, so Windows SmartScreen may display an "Unknown
> publisher" warning.

## Download

The latest test version is available as a single setup file on the
[0.10.0 Beta pre-release](https://github.com/macson17/BB-Audio-Control/releases/tag/v0.10.0)
page. Only download files from this official repository.

## Screenshots

### Responsive interface — 0.10.0 Beta

These screenshots use synthetic example data, not personal device data.

![Large tablet layout](screenshots/v0.10.0-tablet.png)
![Compact tablet layout](screenshots/v0.10.0-compact-tablet.png)
![Phone portrait layout](screenshots/v0.10.0-phone-portrait.png)
![Phone landscape layout](screenshots/v0.10.0-phone-landscape.png)

The earlier screenshots below remain available for reference.

### Mixer

![BB Audio Control mixer with multiple applications](screenshots/mixer.png)

### Edit mode

![BB Audio Control edit mode](screenshots/edit-mode.png)

<details>
<summary>More interface views</summary>

### Background selection

![BB Audio Control background selection](screenshots/backgrounds.png)

### Fader color selection

![BB Audio Control fader color selection](screenshots/fader-colors.png)

</details>

## Features

- Master volume and master mute
- Per-application volume and mute for each audio output
- Switch the Windows default audio output
- Mute and unmute the microphone
- Change the microphone input by holding the microphone button
- Show, hide, and reorder up to five applications
- Global and per-application fader colors
- Custom output names, icons, and colors
- Five background themes
- German and English interface
- PIN pairing and a locally generated QR code
- CPU, GPU, and RAM information on tablets where supported by the system
- Responsive controls over WebSocket on the local network

## Requirements

- Windows 10 build 19041 or later, or Windows 11
- 64-bit Windows on an x64-compatible system
- iPad or Android tablet; smartphone in portrait or landscape orientation
- PC and tablet on the same reachable private network

No separate .NET runtime installation is required on the target PC.

## Installation

1. Download `BB-Audio-Control-Setup-v0.10.0.exe` from the pre-release.
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

User-reported display checks passed on **iPad, iPhone 16 Pro, and Samsung
Galaxy S21 Ultra**. The **TABWEE T80 beta test is still pending**. These are
display checks, not a claim that every audio, hardware, or PWA scenario was tested.

Phones hide output tiles and CPU/GPU/RAM metrics. Hold Sound to choose an
output; tap Sound to mute/unmute. Holding Microphone still selects the input.
The phone master fader is horizontal; its Edit menu contains relevant program
and appearance settings. Tablet controls, up to five program rows without
process IDs, and global/per-program fader colors are retained. Short viewports
may require vertical scrolling. See the [changelog](CHANGELOG.md).

- Snapdragon/ARM systems have not yet been fully tested.
- GPU usage and temperature depend on Windows and the graphics driver.
- `– °C` means that no supported temperature value is available.
- A maximum of five applications can be displayed at the same time.
- Applications appear only after Windows reports an active audio session.
- Guest-network isolation, VPN software, or a firewall may block the tablet
  connection.
- The local PC address may change after switching networks.
- The installer is not digitally signed yet.
- Automatic updates are not available yet.

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
