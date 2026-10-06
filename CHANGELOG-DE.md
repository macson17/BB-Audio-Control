# Änderungsprotokoll

[English](CHANGELOG.md) | [Deutsch](CHANGELOG-DE.md)

## 1.2.0 — 2026-10-06

GitHub-Updateprüfung beim Start, täglich und manuell. Jetzt installieren/Später, SHA-256-Prüfung sowie Erhalt von PIN, Einstellungen, Programmbelegungen und Autostartwahl. Der Installer ist derzeit nicht digital signiert.

## 1.1.0 — 01.10.2026

Fünf Tablet-Programmstarter mit Windows-Icons, App-Suche in den Windows-Einstellungen, anpassbaren Namen und Farben. Drei Sekunden halten beendet zugeordnete Apps zwangsweise; ungespeicherte Arbeit kann verloren gehen. Tabletgrenze 1107 × 710 CSS-Pixel; Smartphoneansicht ohne Startertasten. Aktualisierte Mediensteuerung, dimmbare Hintergründe, Fader-Markierungen und Pairingdarstellung. Updates erhalten Einstellungen und Belegungen.

## 1.0.0 — 27.09.2026

Erstes stabiles Release.

- Responsive Tablet- und Smartphone-Layouts einschließlich kompakter
  Android-Tablets.
- Höchstens vier Hauptausgänge in der normalen Tablet-Ansicht und bis zu fünf
  Programme mit responsiven Fadern.
- Optionaler Audioausgang pro App durch Antippen des Icons; „Systemstandard“
  folgt weiterhin dem gewählten Hauptausgang.
- Mediensteuerung mit Cover, Titel, Interpret, Vor, Zurück und unmittelbar
  reagierendem statusabhängigem Play/Pause; auch Browsermedien wie YouTube
  lassen sich steuern.
- Freie Fader- und Hintergrundfarben mit Leuchtkraft sowie ein gemeinsames
  eigenes Hintergrundbild für gekoppelte Geräte.
- Neu angeordneter Tablet-Bearbeiten-Modus und unten verankerte
  CPU-/GPU-/RAM-Leiste.
- AMD-GPU-Temperatur über Windows/D3DKMT, praktisch auf einer Radeon 780M
  bestätigt.
- Windows-x64-Build, Installer, lokales Upgrade, Einstellungserhalt, Autostart,
  installierte Dateien, geschützte Webassets und finale Tablet-Oberfläche geprüft.

Installer: `BB-Audio-Control-Setup-v1.0.0.exe`

SHA-256: `8DA42AB63AF51D558361A929A3FA11B4E03D4ADD6740649241AE253041DD7A3A`

## 0.11.2 Beta — 2026-09-15

Pre-Release für den gezielten AMD-GPU-Temperaturtest, keine stabile oder endgültige Version.

- GPU-Adapter werden zusätzlich direkt über `D3DKMTEnumAdapters2` ermittelt und über ihre Windows-LUID geöffnet.
- Alle von Windows gemeldeten physischen Adapterindizes werden auf plausible Temperaturen geprüft.
- Der bisherige Display-Device-Pfad und der NVIDIA-NVML-Fallback bleiben erhalten.
- Offizieller Windows-x64-Release und Installer wurden ohne Compilerwarnungen oder Fehler erstellt. Der Anwendungstest auf der diagnostizierten AMD Radeon 780M steht noch aus.

## 0.11.1 Beta — 2026-09-15

Pre-Release für weitere Tests, keine stabile oder endgültige Version.

- Die normale Tablet-Oberfläche scrollt auch auf kurzen iPad-Viewports nicht mehr.
- Medientasten entsprechen farblich den Programm-Mute-Tasten und behalten ohne aktive Medien ihre Position.
- Das Windows-Einstellungsfenster listet alle aktiven lokalen IPv4-Adressen auf; QR-Code, Kopieren und Browseröffnung folgen der Auswahl.
- Die GPU-Abfrage wiederholt fehlgeschlagene Windows-Zählerinitialisierungen und berücksichtigt Render-/Hybrid-GPUs. Der AMD-Hardwaretest steht noch aus.
- Lokales Windows-Upgrade, Einstellungserhalt, 18 installierte Release-Dateien, iPad-Korrektur und Netzwerkauswahl wurden bestätigt.

## 0.11.0 Beta — 2026-09-13

Pre-Release für weitere Tests, keine stabile oder endgültige Version.

- Tablet-Mediensteuerung der aktiven Windows-Mediensitzung mit Titel, Interpret, Vor, Zurück und statusabhängigem Play/Pause; damit lässt sich auch YouTube im Browser pausieren.
- Ein Tipp auf das App-Icon öffnet die optionale Ausgangswahl; „Systemstandard“ folgt weiter den Hauptausgangstasten.
- Programmfader und Programm-Mute wirken auf den zugewiesenen Ausgang.
- Der globale Sound-Mute umfasst alle aktiven Ausgänge und stellt deren vorherige Mute-Zustände wieder her.
- Größere, tiefer angeordnete Mediensteuerung auf Tablets; auf Smartphones bleibt die Musiksektion vollständig verborgen.
- Responsive Tablet-/Smartphone-Layouts, Pairing, WebSocket-Steuerung, Einstellungserhalt und die Begrenzung auf fünf Programme bleiben erhalten.

Windows-x64-Release-/Installer-Build, Upgrade über 0.10.4, bytegenauer
Einstellungserhalt, 18 installierte Release-Dateien und isolierte Browserchecks
bestanden. Der Installer ist nicht digital signiert.

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
