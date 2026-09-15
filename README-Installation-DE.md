# BB Audio Control 0.11.2 Beta – Installation

[English](README-Installation.md) | [Deutsch](README-Installation-DE.md)

## Installation

1. Unter [Pre-Release 0.11.2 Beta](https://github.com/macson17/BB-Audio-Control/releases/tag/v0.11.2)
   die Datei `BB-Audio-Control-Setup-v0.11.2.exe` herunterladen.
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

## Tablet oder Smartphone verbinden

1. PC und Tablet mit demselben privaten Netzwerk verbinden.
2. Das BB-Audio-Control-Einstellungsfenster am PC öffnen. Dazu das Symbol neben
   der Windows-Uhr doppelt anklicken.
3. Bei mehreren Netzwerken zuerst die passende lokale IPv4-Adresse auswählen,
   dann den QR-Code scannen oder diese Adresse manuell im
   Browser öffnen, zum Beispiel `http://192.168.x.x:5179`.
4. Den im PC-Fenster angezeigten sechsstelligen Pairing-Code eingeben.
5. Optional die Seite zum Home- beziehungsweise Startbildschirm hinzufügen.

Der QR-Code enthält nur die lokale Adresse und nicht den Pairing-Code.

## Grundbedienung

- Auf Tablets steuert der große linke Fader die Gesamtlautstärke; auf Smartphones liegt er horizontal.
- Auf Tablets wechseln Ausgangstasten den Windows-Standardausgang; auf Smartphones öffnet langes Drücken auf Sound die Ausgangswahl.
- „Sound“ schaltet alle aktiven Ausgänge stumm und stellt deren vorherige Mute-Zustände wieder her.
- Ein kurzer Druck auf die Mikrofon-Taste schaltet das Mikrofon stumm.
- Ein langer Druck auf die Mikrofon-Taste öffnet die Eingangsauswahl.
- Programmfader steuern aktive Windows-Audio-Sessions auf ihrem zugewiesenen Ausgang.
- Ein Tipp auf das App-Icon öffnet die optionale Ausgangswahl. „Systemstandard“ folgt weiter den Hauptausgangstasten.
- Die Medientasten auf Tablets steuern die aktive Windows-Mediensitzung. Damit lassen sich Musik-Apps sowie YouTube im Browser pausieren.
- Auf Tablets lassen sich unter „Bearbeiten“ Ausgänge und Programme anpassen. Auf Smartphones enthält das Menü Programm- und Darstellungsoptionen, keine Ausgangskachel-Bearbeitung.
- Unter „Darstellung“ lassen sich Sprache, Hintergrund und Faderfarbe ändern.

Programme werden erst angezeigt, nachdem Windows für sie eine aktive
Audio-Session erkannt hat. Falls ein Programm fehlt, dort zunächst Ton
abspielen.

Smartphones blenden CPU-/GPU-/RAM-Werte und einzelne Ausgangsbuttons aus.
Hoch- und Querformat werden unterstützt. Maximal fünf Programmzeilen ohne
Prozess-ID sowie globale und individuelle Faderfarben bleiben erhalten.
Bei sehr geringer Höhe kann vertikales Scrollen nötig sein.

## Update

0.11.2 Beta kann eine vorhandene Installation aktualisieren. Lokale Windows-Upgrades früherer Testversionen wurden
erfolgreich durchgeführt; Einstellungen einschließlich PIN waren auch nach
dem Start bytegenau unverändert. Das ist keine Garantie für jeden PC.
Die Autostart-Auswahl beim Setup beachten. Anschließend die Mobilseite neu
laden und auf **v0.11.2 Beta** unter dem Logo achten.

Nach Nutzerprüfung ist die Darstellung auf iPad, iPhone 16 Pro und Samsung
Galaxy S21 Ultra erfolgreich geprüft. Der TABWEE-T80-Betatest steht noch aus.

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
