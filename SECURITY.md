# Security

[English](SECURITY.md) | [Deutsch](SECURITY-DE.md)

## Supported version

Security fixes are currently considered only for the latest beta version of
BB Audio Control.

## Security model

BB Audio Control operates exclusively on the local network and does not use a
cloud service. Control access requires a six-digit pairing code. Creating a
new code disconnects existing clients and immediately invalidates the old code.

The connection currently uses HTTP and WebSocket without transport encryption.
The pairing code and control commands can be observed on a compromised local
network. Only use BB Audio Control on a trusted private network.

## Report a security issue

Do not publish confidential details in a public issue. This includes:

- Pairing codes
- Real local IP addresses
- Computer names and user names
- Local file paths
- Logs containing personal information

If private vulnerability reporting is available for this repository, use that
option. Otherwise, create a public issue without sensitive technical details
and ask for a private contact method.

## Scope

General connection problems, usage questions, and feature requests belong in
regular GitHub Issues. A missing GPU temperature is not automatically a
security issue or application defect; the graphics driver must provide a
supported sensor value.
