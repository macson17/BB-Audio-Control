# BB Audio Control

BB Audio Control macht ein iPad oder Android-Tablet im lokalen Netzwerk zu
einem übersichtlichen Audiomischpult für einen Windows-PC. Lautstärke,
Stummschaltung, Audioausgänge und Mikrofon lassen sich bedienen, ohne das
aktuelle Spiel oder Programm zu verlassen.

> **Beta-Version:** BB Audio Control befindet sich noch in der Testphase. Der
> aktuelle Installer ist nicht digital signiert. Windows SmartScreen kann
> deshalb „Unbekannter Herausgeber“ anzeigen.

## Download

Die aktuelle Testversion steht unter
[GitHub Releases](https://github.com/macson17/BB-Audio-Control/releases/latest)
als einzelne Setup-Datei bereit.

Bitte ausschließlich Dateien aus diesem offiziellen Repository verwenden.

## Funktionen

- Master-Lautstärke und Master-Mute
- Lautstärke und Mute je aktivem Programm und Audioausgang
- Wechsel des Windows-Standardausgangs
- Mikrofon stumm- und einschalten
- Mikrofoneingang durch langen Druck auf die Mikrofon-Taste wechseln
- Bis zu fünf frei sortier- und ausblendbare Programme
- Global und pro Programm wählbare Faderfarben
- Anpassbare Ausgangsnamen, Symbole und Farben
- Fünf Hintergrunddesigns
- Deutsch und Englisch
- PIN-Kopplung und lokaler QR-Code
- CPU-, GPU- und RAM-Anzeige, soweit vom System unterstützt
- Direkte Bedienreaktion über WebSocket im lokalen Netzwerk

## Voraussetzungen

- Windows 10 ab Build 19041 oder Windows 11
- 64-Bit-Windows auf einem x64-kompatiblen System
- iPad oder Android-Tablet im Querformat
- PC und Tablet im selben erreichbaren privaten Netzwerk

Auf dem Ziel-PC muss keine separate .NET-Laufzeit installiert werden.

## Installation

1. Die aktuelle `BB-Audio-Control-Setup-v0.9.9.exe` aus den Releases laden.
2. Die Setup-Datei starten und Deutsch oder Englisch auswählen.
3. Bei einer SmartScreen-Warnung „Weitere Informationen“ und anschließend
   „Trotzdem ausführen“ wählen, wenn die Datei aus diesem Repository stammt.
4. Den standardmäßig aktivierten Autostart bei Bedarf abwählen.
5. Die Windows-Abfrage für die private Firewall-Regel bestätigen.
6. Im Einstellungsfenster den QR-Code scannen oder die angezeigte lokale
   Adresse auf dem Tablet öffnen.
7. Den sechsstelligen Pairing-Code eingeben.

Eine ausführlichere Anleitung steht in
[README-Installation.md](README-Installation.md).

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

Weitere Hinweise stehen in [SECURITY.md](SECURITY.md).

## Bekannte Einschränkungen

- Snapdragon-/ARM-Systeme sind noch nicht abschließend getestet.
- GPU-Auslastung und GPU-Temperatur hängen von Windows und dem Grafiktreiber ab.
- `– °C` bedeutet, dass kein unterstützter Temperaturwert bereitgestellt wird.
- Es werden maximal fünf Programme gleichzeitig angezeigt.
- Programme erscheinen erst, wenn Windows eine aktive Audio-Session meldet.
- Gastnetz-Isolation, VPN oder Firewall können die Tablet-Verbindung blockieren.
- Die lokale PC-Adresse kann sich nach einem Netzwerkwechsel ändern.
- Der Installer ist noch nicht digital signiert.
- Es gibt noch keine automatische Updatefunktion.

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
