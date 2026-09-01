# BB Audio Control v0.9.9 Beta – Installation

## Installation

1. Unter [GitHub Releases](https://github.com/macson17/BB-Audio-Control/releases/latest)
   die Datei `BB-Audio-Control-Setup-v0.9.9.exe` herunterladen.
2. Die Setup-Datei doppelt anklicken.
3. Deutsch oder Englisch auswählen.
4. Falls Windows SmartScreen „Unbekannter Herausgeber“ anzeigt, zunächst
   „Weitere Informationen“ und anschließend „Trotzdem ausführen“ wählen.
5. „BB Audio Control mit Windows starten“ ist standardmäßig aktiviert und kann
   bei Bedarf abgewählt werden.
6. Die Installation abschließen.
7. Die Windows-Abfrage zum Einrichten der programmspezifischen Firewall-Regel
   für private Netzwerke bestätigen.

Die App installiert sich für den aktuellen Windows-Benutzer. Eine separate
.NET-Installation ist nicht notwendig.

## Tablet verbinden

1. PC und Tablet mit demselben privaten Netzwerk verbinden.
2. Das BB-Audio-Control-Einstellungsfenster am PC öffnen. Dazu das Symbol neben
   der Windows-Uhr doppelt anklicken.
3. Den QR-Code mit dem Tablet scannen oder die angezeigte Adresse manuell im
   Browser öffnen, zum Beispiel `http://192.168.x.x:5179`.
4. Den im PC-Fenster angezeigten sechsstelligen Pairing-Code eingeben.
5. Optional die Seite zum Home- beziehungsweise Startbildschirm hinzufügen.

Der QR-Code enthält nur die lokale Adresse und nicht den Pairing-Code.

## Grundbedienung

- Der große linke Fader steuert die Gesamtlautstärke.
- Die Ausgangstasten wechseln den Windows-Standardausgang.
- „Sound“ schaltet die Gesamtausgabe stumm oder wieder ein.
- Ein kurzer Druck auf die Mikrofon-Taste schaltet das Mikrofon stumm.
- Ein langer Druck auf die Mikrofon-Taste öffnet die Eingangsauswahl.
- Programmfader steuern aktive Windows-Audio-Sessions.
- Unter „Bearbeiten“ lassen sich Ausgänge und Programme anpassen.
- Unter „Darstellung“ lassen sich Sprache, Hintergrund und Faderfarbe ändern.

Programme werden erst angezeigt, nachdem Windows für sie eine aktive
Audio-Session erkannt hat. Falls ein Programm fehlt, dort zunächst Ton
abspielen.

## Update

Eine neue Setup-Datei über die vorhandene Installation ausführen. Das Setup
beendet die laufende App, ersetzt die Programmdateien und startet anschließend
auf Wunsch die neue Version.

Folgende Daten bleiben erhalten:

- Pairing-Code
- Geräte- und Programmanpassungen
- Faderfarben und Hintergrund
- Programmlautstärke und Mute pro Audioausgang
- Spracheinstellungen

## Wenn keine Verbindung möglich ist

- Prüfen, ob BB Audio Control auf dem PC läuft.
- Prüfen, ob PC und Tablet im selben erreichbaren Netzwerk sind.
- Die aktuell im PC-Fenster angezeigte Adresse verwenden.
- Die private Windows-Firewallregel für BB Audio Control kontrollieren.
- Gast-WLAN, Client-Isolation und VPN testweise ausschließen.
- Nach einem Netzwerkwechsel den aktuellen QR-Code erneut scannen.

## Deinstallation

Unter `Windows-Einstellungen > Apps > Installierte Apps` den Eintrag
**BB Audio Control** deinstallieren.

Programmdateien, Autostart-Eintrag und Firewall-Regel werden entfernt.
Persönliche Einstellungen und Pairing-Code bleiben für eine spätere
Neuinstallation erhalten.

## Sicherheitshinweis

Die Verbindung ist auf ein vertrauenswürdiges privates Netzwerk ausgelegt.
Sie verwendet derzeit HTTP und WebSocket ohne Transportverschlüsselung. Den
Pairing-Code nur Personen geben, die den PC steuern dürfen, und bei Verdacht im
PC-Fenster einen neuen Code erzeugen.
