# BB Audio Control 0.11.1 Beta — Installation

[English](README-Installation.md) | [Deutsch](README-Installation-DE.md)

## Installation

1. Download `BB-Audio-Control-Setup-v0.11.1.exe` from
   [the pre-release](https://github.com/macson17/BB-Audio-Control/releases/tag/v0.11.1).
2. Double-click the setup file.
3. Select German or English.
4. If Windows SmartScreen displays "Unknown publisher," select "More info"
   and then "Run anyway."
5. "Start BB Audio Control with Windows" is enabled by default and can be
   disabled if preferred.
6. Complete the installation.
7. Confirm the Windows prompt that creates the application-specific firewall
   rule for private networks.

The app is installed for the current Windows user. A separate .NET installation
is not required.

## Connect a tablet or smartphone

1. Connect the PC and tablet to the same private network.
2. Open the BB Audio Control settings window on the PC by double-clicking its
   icon next to the Windows clock.
3. Select the matching local IPv4 address if multiple networks are listed,
   then scan the QR code or manually open that address in
   the browser, for example `http://192.168.x.x:5179`.
4. Enter the six-digit pairing code shown in the PC window.
5. Optionally add the page to the Home screen.

The QR code contains only the local address, not the pairing code.

## Basic controls

- On tablets, the large fader on the left controls the master volume; on phones it is horizontal.
- On tablets, output buttons change the Windows default audio output; on phones, hold Sound to open the output selection.
- The Sound button mutes all active outputs and restores their previous mute states.
- A short press on the microphone button mutes or unmutes the microphone.
- Holding the microphone button opens the input selection.
- Application faders control active Windows audio sessions on their assigned output.
- Tap an application's icon to select an optional output. System default keeps following the main output buttons.
- Tablet media controls operate the active Windows media session. They can control music applications and pause YouTube in a browser.
- Tablet Edit mode lets you customize outputs and applications. Phone Edit mode contains program and appearance options, without output-tile editing.
- Appearance settings control the language, background, and fader color.

Applications appear only after Windows detects an active audio session. If an
application is missing, play some audio in it first.

Phones hide CPU/GPU/RAM information and individual output buttons. Both phone
orientations are supported. Up to five program rows are shown, without process
IDs; global and individual fader colors remain available. Very short viewports
may scroll vertically.

## Update

0.11.1 Beta can update an existing installation. Local Windows upgrades completed successfully
and kept settings, including the pairing code, byte-for-byte after startup.
This is not a guarantee for every PC. Check the startup option during setup.
Reload the mobile page afterwards and check for **v0.11.1 Beta** below the logo.

Display checks reported by the user passed on iPad, iPhone 16 Pro, and Samsung
Galaxy S21 Ultra. TABWEE T80 remains a pending beta test.

Run a new setup file over the existing installation. Setup closes the running
app, replaces its program files, and can restart the new version afterwards.

The following data is retained:

- Pairing code
- Device and application customizations
- Fader colors and background
- Per-output application volume and mute state
- Language setting

## If the tablet cannot connect

- Check that BB Audio Control is running on the PC.
- Check that the PC and tablet are on the same reachable network.
- Use the address currently displayed in the PC window.
- Check the private Windows firewall rule for BB Audio Control.
- Temporarily rule out guest Wi-Fi, client isolation, and VPN software.
- Scan the current QR code again after changing networks.

## Uninstall

Open `Windows Settings > Apps > Installed apps` and uninstall
**BB Audio Control**.

Program files, the startup entry, and the firewall rule are removed. Personal
settings and the pairing code remain for a later reinstall.

## Security notice

The connection is intended for a trusted private network. It currently uses
HTTP and WebSocket without transport encryption. Only share the pairing code
with people who are allowed to control the PC, and create a new code in the PC
window if you suspect unauthorized access.
