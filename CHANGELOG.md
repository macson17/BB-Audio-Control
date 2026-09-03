# Changelog

[English](CHANGELOG.md) | [Deutsch](CHANGELOG-DE.md)

## 0.10.0 Beta — 2026-09-03

Pre-release for further testing, not a stable/final release.

### New and retained

- Responsive layouts for different tablet sizes, including a compact layout for smaller or lower-resolution tablets.
- New phone interface in portrait and landscape orientations.
- No CPU, GPU, or RAM display and no individual output buttons on phones.
- Hold Sound to choose an output; a short press still mutes/unmutes sound.
- Microphone input selection remains available by holding the microphone button.
- Horizontal master-volume fader on phones, without an extra label.
- Phone Edit menu with relevant program and appearance functions.
- Still up to five visible programs, without process IDs.
- Global and individual fader colors and existing tablet controls retained.
- Pairing/PIN and immediate WebSocket commands retained; PWA cache/assets updated.

### Test status

User-reported display checks: iPad, iPhone 16 Pro, and Samsung Galaxy S21 Ultra
passed. TABWEE T80 testing is pending. Windows x64 release/installer builds and
isolated responsive browser checks passed. One local upgrade from 0.9.9 retained
settings/PIN. No broader device, audio, hardware, or PWA test coverage is claimed.
Very short viewports may need vertical scrolling. Existing security and hardware
limitations still apply; the installer remains unsigned.

### Download integrity

`BB-Audio-Control-Setup-v0.10.0.exe` — 61,995,166 bytes.

SHA-256: `DCBEFCD16BB7E2E1670F652D94D152A5BF76B84203498FA83B50B349811E9B19`

[Download pre-release](https://github.com/macson17/BB-Audio-Control/releases/tag/v0.10.0).

## 0.9.9 Beta

First publicly available test version.

### New and changed

- Global fader color can be selected under Appearance
- An individual fader color can be assigned to each application
- Removed the redundant Live indicator and separator lines from the application area
- GPU usage now uses native Windows performance data
- GPU temperature now includes an additional NVIDIA driver fallback
- Removed LibreHardwareMonitor completely
- Added third-party and .NET license notices to the installer
- Updated the PWA cache and version information to v0.9.9

### Update

v0.9.9 can be installed over an existing installation. Settings and the
pairing code are retained.

### Known limitations

- Snapdragon/ARM support has not yet been fully tested
- GPU information may be unavailable depending on Windows, hardware, and driver
- A maximum of five applications can be visible at the same time
- Applications require an active Windows audio session
- Local network communication currently has no transport encryption
- The installer is not digitally signed yet
- Automatic updates are not available
