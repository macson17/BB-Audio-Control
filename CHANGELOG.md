# Changelog

[English](CHANGELOG.md) | [Deutsch](CHANGELOG-DE.md)

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
