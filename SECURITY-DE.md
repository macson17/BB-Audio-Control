# Sicherheit

[English](SECURITY.md) | [Deutsch](SECURITY-DE.md)

## Unterstützter Stand

Sicherheitskorrekturen werden derzeit nur für die jeweils aktuelle
Beta-Version von BB Audio Control betrachtet.

## Sicherheitsmodell

BB Audio Control arbeitet ausschließlich im lokalen Netzwerk und verwendet
keinen Cloud-Dienst. Steuerzugriff erfordert einen sechsstelligen Pairing-Code.
Wird ein neuer Code erzeugt, werden bestehende Verbindungen getrennt und der
alte Code sofort ungültig.

Die Verbindung verwendet derzeit HTTP und WebSocket und ist nicht
transportverschlüsselt. Pairing-Code und Steuerbefehle können innerhalb eines
kompromittierten lokalen Netzwerks mitgelesen werden. BB Audio Control sollte
deshalb nur in einem vertrauenswürdigen privaten Netzwerk eingesetzt werden.

## Sicherheitsproblem melden

Bitte keine vertraulichen Details in einem öffentlichen Issue veröffentlichen.
Das gilt insbesondere für:

- Pairing-Codes
- echte lokale IP-Adressen
- Rechner- und Benutzernamen
- lokale Dateipfade
- Protokolle mit persönlichen Daten

Falls GitHub für dieses Repository eine private Sicherheitsmeldung anbietet,
bitte diesen Weg verwenden. Andernfalls kann zunächst ein öffentliches Issue
ohne technische Geheimnisse erstellt und darin um einen privaten Kontaktweg
gebeten werden.

## Abgrenzung

Allgemeine Verbindungsprobleme, Bedienungsfragen und Funktionswünsche gehören
in die normalen GitHub Issues. Eine fehlende GPU-Temperatur ist nicht
automatisch ein Sicherheits- oder Programmfehler; der jeweilige Treiber muss
einen unterstützten Sensorwert bereitstellen.
