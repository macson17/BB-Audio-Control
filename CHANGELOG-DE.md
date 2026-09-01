# Änderungsprotokoll

[English](CHANGELOG.md) | [Deutsch](CHANGELOG-DE.md)

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
