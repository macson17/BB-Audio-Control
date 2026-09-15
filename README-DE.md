# BB Audio Control

Aktuelle Testversion: **0.11.2 Beta** (Pre-Release).

[English](README.md) | [Deutsch](README-DE.md)

BB Audio Control macht Tablets und Smartphones im lokalen Netzwerk zu einem
übersichtlichen Audiomischpult für einen Windows-PC. Lautstärke,
Stummschaltung, Audioausgänge und Mikrofon lassen sich bedienen, ohne das
aktuelle Spiel oder Programm zu verlassen.

> **Beta-Version:** BB Audio Control befindet sich noch in der Testphase. Der
> aktuelle Installer ist nicht digital signiert. Windows SmartScreen kann
> deshalb „Unbekannter Herausgeber“ anzeigen.

## Download

Die aktuelle Testversion steht unter
[Pre-Release 0.11.2 Beta](https://github.com/macson17/BB-Audio-Control/releases/tag/v0.11.2)
als einzelne Setup-Datei bereit. Bitte ausschließlich Dateien aus diesem
offiziellen Repository verwenden.

## Screenshots

### Tablet-Oberfläche — 0.11.0 Beta

Die aktuelle Galerie beginnt mit der abgenommenen Tablet-Oberfläche.

![Tablet-Mixer mit Mediensteuerung](screenshots/v0.11.0-tablet-main.png)
![Programm-Mute auf dem Tablet](screenshots/v0.11.0-tablet-app-mute.png)
![Audioausgang pro App auswählen](screenshots/v0.11.0-tablet-app-output.png)
![Bearbeiten-Modus auf dem Tablet](screenshots/v0.11.0-tablet-edit.png)

### Smartphone

![Smartphone im Hochformat](screenshots/v0.10.0-phone-portrait.png)
![Smartphone im Querformat](screenshots/v0.10.0-phone-landscape.png)

<details>
<summary>Frühere Ansichten anzeigen</summary>

### Frühere Tablet-Ansichten

![Großes Tablet-Layout](screenshots/v0.10.0-tablet.png)
![Kompaktes Tablet-Layout](screenshots/v0.10.0-compact-tablet.png)
![BB Audio Control mit mehreren Programmen](screenshots/mixer.png)
![Bearbeiten-Modus von BB Audio Control](screenshots/edit-mode.png)

### Hintergrundauswahl

![Hintergrundauswahl von BB Audio Control](screenshots/backgrounds.png)

### Faderfarbauswahl

![Faderfarbauswahl von BB Audio Control](screenshots/fader-colors.png)

</details>

## Funktionen

- Master-Lautstärke und Master-Mute über alle aktiven Ausgänge mit Wiederherstellung der vorherigen Mute-Zustände
- Lautstärke und Mute je aktivem Programm und Audioausgang
- Wechsel des Windows-Standardausgangs
- Optionaler Audioausgang pro App durch Antippen des App-Icons; Systemstandard folgt weiterhin den Hauptausgangstasten
- Mediensteuerung der aktiven Windows-Mediensitzung mit Vor, Zurück und statusabhängigem Play/Pause; damit lässt sich auch YouTube im Browser pausieren
- Mikrofon stumm- und einschalten
- Mikrofoneingang durch langen Druck auf die Mikrofon-Taste wechseln
- Bis zu fünf frei sortier- und ausblendbare Programme
- Global und pro Programm wählbare Faderfarben
- Anpassbare Ausgangsnamen, Symbole und Farben
- Fünf Hintergrunddesigns
- Deutsch und Englisch
- PIN-Kopplung und lokaler QR-Code
- CPU-, GPU- und RAM-Anzeige auf Tablets, soweit vom System unterstützt
- Direkte Bedienreaktion über WebSocket im lokalen Netzwerk
- Auswahl aller aktiven lokalen IPv4-Adressen im Windows-Fenster; QR-Code, Kopieren und Browseröffnung folgen der Auswahl

## Voraussetzungen

- Windows 10 ab Build 19041 oder Windows 11
- 64-Bit-Windows auf einem x64-kompatiblen System
- Tablet oder Smartphone mit einem aktuellen Webbrowser
- PC und Tablet im selben erreichbaren privaten Netzwerk

Auf dem Ziel-PC muss keine separate .NET-Laufzeit installiert werden.

## Installation

1. `BB-Audio-Control-Setup-v0.11.2.exe` aus dem Pre-Release laden.
2. Die Setup-Datei starten und Deutsch oder Englisch auswählen.
3. Bei einer SmartScreen-Warnung „Weitere Informationen“ und anschließend
   „Trotzdem ausführen“ wählen, wenn die Datei aus diesem Repository stammt.
4. Den standardmäßig aktivierten Autostart bei Bedarf abwählen.
5. Die Windows-Abfrage für die private Firewall-Regel bestätigen.
6. Im Einstellungsfenster den QR-Code scannen oder die angezeigte lokale
   Adresse auf dem Tablet öffnen.
7. Den sechsstelligen Pairing-Code eingeben.

Weitere Einzelheiten stehen in der
[deutschen Installationsanleitung](README-Installation-DE.md). Die
[englische Installationsanleitung](README-Installation.md) ist ebenfalls
verfügbar.

## Update

Eine neuere Setup-Datei wird einfach über die vorhandene Version installiert.
Einstellungen und Pairing-Code bleiben erhalten. Eine normale Deinstallation
lässt diese persönlichen Einstellungen ebenfalls bestehen.

## Sicherheit und Datenschutz

BB Audio Control verwendet keinen Cloud-Dienst. Die Kommunikation bleibt im
lokalen Netzwerk und erfordert für die Steuerung einen sechsstelligen
Pairing-Code. Ein neuer Code trennt bestehende Verbindungen und macht den alten
Code sofort ungültig.

Die Übertragung erfolgt derzeit über HTTP und WebSocket und ist nicht
transportverschlüsselt. Pairing-Code und Steuerbefehle könnten in einem
kompromittierten lokalen Netzwerk mitgelesen werden. Die Anwendung sollte nur
in einem vertrauenswürdigen privaten Netzwerk verwendet werden.

Weitere Hinweise stehen in [SECURITY-DE.md](SECURITY-DE.md).

## Bekannte Einschränkungen

Die Darstellung wurde nach Nutzerprüfung auf **iPad, iPhone 16 Pro und Samsung
Galaxy S21 Ultra erfolgreich geprüft**. Der **TABWEE-T80-Betatest steht noch
aus**. Das bestätigt die Darstellung, nicht sämtliche Audio-, Hardware- oder PWA-Funktionen.

Auf Tablets erscheinen Titel und Interpret sowie die Mediensteuerung der aktiven
Windows-Mediensitzung. Ein Tipp auf das App-Icon öffnet die optionale
Audioausgangswahl. Auf Smartphones bleibt die komplette Musiksektion verborgen.

- Snapdragon-/ARM-Systeme sind noch nicht abschließend getestet.
- GPU-Auslastung und GPU-Temperatur hängen von Windows und dem Grafiktreiber ab.
- `– °C` bedeutet, dass kein unterstützter Temperaturwert bereitgestellt wird.
- Smartphones zeigen keine Ausgangskacheln und keine CPU-, GPU- oder RAM-Werte.
- Auf Smartphones öffnet langes Drücken auf „Sound“ die Ausgangswahl; kurzes
  Drücken schaltet den Ton stumm oder wieder ein.
- Die normale Tablet-Ansicht scrollt nicht; Bearbeiten-Modus und sehr kurze Smartphone-Viewports dürfen bei Bedarf scrollen.
- Version 0.11.2 verwendet die direkte Windows-D3DKMT-Adapterenumeration für GPU-Temperaturen; die praktische Prüfung in der Anwendung auf der diagnostizierten AMD Radeon 780M steht noch aus.
- Es werden maximal fünf Programme gleichzeitig angezeigt.
- Programme erscheinen erst, wenn Windows eine aktive Audio-Session meldet.
- Gastnetz-Isolation, VPN oder Firewall können die Tablet-Verbindung blockieren.
- Die lokale PC-Adresse kann sich nach einem Netzwerkwechsel ändern.
- Der Installer ist noch nicht digital signiert.
- Es gibt noch keine automatische Updatefunktion.

Weitere Änderungen sind im [Änderungsprotokoll](CHANGELOG-DE.md) aufgeführt.

## Probleme und Wünsche

Für nachvollziehbare Fehlerberichte und Funktionswünsche können die
[GitHub Issues](https://github.com/macson17/BB-Audio-Control/issues) verwendet
werden. Bitte niemals Pairing-Codes, echte lokale IP-Adressen, Rechnernamen,
Benutzerpfade oder andere persönliche Daten veröffentlichen.

## Quellcode und Drittanbieterkomponenten

Dieses öffentliche Repository ist ausschließlich für Produktinformationen,
Support und Binär-Downloads bestimmt. Der eigene Quellcode von BB Audio Control
ist proprietär und wird nicht öffentlich bereitgestellt. Dieses Repository ist
kein Open-Source-Projekt und enthält bewusst keine Open-Source-Lizenz für den
eigenen Programmcode.

Der Installer enthält die erforderlichen Lizenz- und Copyright-Hinweise für
die verwendeten Drittanbieterkomponenten, darunter NAudio, QRCoder und die
eingebettete .NET-Laufzeit.
