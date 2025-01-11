# Produktivnetz einrichten

Autoren: Lukas Oschmann, Fabian Hertel

## Allgemein

Bei der Einrichtung des Netzes haben wir auf der Firewall ein eigenes Interface anlegen müssen. Diese Schnittstelle liegt auf einem der Hardware Ports der Firewall.

Folgender Traffic wird ausgehend erlaubt:
- DNS
- HTTP
- HTTPS
- ICMP

Zudem wurde der Switch und der VM-Host mit dem Produktivnetz verbunden. Auf dem VM-Host laufen die für das Projekt notwendigen Services und diese wiederrum müssen in das Produktivnetzwerk, weshalb eine der Hardware Schnittstellen des VM-Hosts physisch mit dem Produktivnetz verbunden ist. 