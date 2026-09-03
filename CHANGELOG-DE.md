# Änderungsprotokoll

[English](CHANGELOG.md) | [Deutsch](CHANGELOG-DE.md)

## 0.10.0 Beta — 2026-09-03

Pre-Release für weitere Tests, keine stabile oder endgültige Version.

### Neu und beibehalten

- Responsive Darstellung für unterschiedliche Tabletgrößen, mit kompaktem Layout für kleinere beziehungsweise niedrig aufgelöste Tablets.
- Neue Smartphone-Oberfläche im Hoch- und Querformat.
- Keine CPU-, GPU- oder RAM-Anzeige und keine einzelnen Ausgangsbuttons auf Smartphones.
- Sound lang öffnet die Ausgangswahl; kurzer Druck schaltet weiterhin stumm/ein.
- Mikrofoneingang weiterhin durch langes Drücken auf die Mikrofontaste auswählbar.
- Horizontaler Hauptlautstärkefader auf Smartphones, ohne Zusatzbeschriftung.
- Smartphone-Bearbeiten-Menü mit relevanten Programm- und Darstellungsfunktionen.
- Weiterhin maximal fünf sichtbare Programme ohne Prozess-ID.
- Globale und individuelle Faderfarben sowie bestehende Tablet-Bedienung bleiben erhalten.
- Pairing/PIN und unmittelbare WebSocket-Steuerung erhalten; PWA-Cache/Assets aktualisiert.

### Teststatus

Darstellung nach Nutzerprüfung auf iPad, iPhone 16 Pro und Samsung Galaxy S21
Ultra erfolgreich geprüft. TABWEE T80: Betatest noch ausstehend.
Windows-x64-Release-/Installer-Build und isolierte responsive Browserprüfungen
bestanden. Ein lokales Upgrade von 0.9.9 erhielt Einstellungen/PIN.
Darüber hinaus werden keine Geräte-, Audio-, Hardware- oder PWA-Tests behauptet.
Bei sehr geringer Höhe kann vertikales Scrollen nötig sein. Bisherige Sicherheits-
und Hardwareeinschränkungen gelten weiter; der Installer ist unsigniert.

### Download-Prüfung

`BB-Audio-Control-Setup-v0.10.0.exe` — 61.995.166 Byte.

SHA-256: `DCBEFCD16BB7E2E1670F652D94D152A5BF76B84203498FA83B50B349811E9B19`

[Pre-Release herunterladen](https://github.com/macson17/BB-Audio-Control/releases/tag/v0.10.0).

## 0.9.9 Beta

Erste öffentlich bereitgestellte Testversion.

### Neu und geändert

- Globale Faderfarbe unter „Darstellung“ wählbar
- Abweichende Faderfarbe pro Programm möglich
- Überflüssige Live-Anzeige und Trennlinien im Programmbereich entfernt
- GPU-Auslastung über Windows-native Leistungswerte
- GPU-Temperatur mit zusätzlichem NVIDIA-Treiber-Fallback
- LibreHardwareMonitor vollständig entfernt
- Drittanbieter- und .NET-Lizenzhinweise in den Installer aufgenommen
- PWA-Cache und Versionsangaben auf v0.9.9 aktualisiert

### Update

v0.9.9 kann über eine vorhandene Installation installiert werden. Einstellungen
und Pairing-Code bleiben erhalten.

### Bekannte Einschränkungen

- Snapdragon-/ARM-Unterstützung noch nicht abschließend getestet
- GPU-Werte können je nach Windows-Version, Hardware und Treiber fehlen
- Maximal fünf Programme gleichzeitig sichtbar
- Programme benötigen eine aktive Windows-Audio-Session
- Kommunikation im lokalen Netzwerk derzeit ohne Transportverschlüsselung
- Installer noch nicht digital signiert
- Keine automatische Updatefunktion
