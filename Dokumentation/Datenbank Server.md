
# Datenbank-Server-Konfiguration (MariaDB auf Debian)

**Author:** Ioannis Vavritsas


## Allgemein

Ein Datenbank-Server wurde auf einem Debian-Container eingerichtet, um die zentrale Speicherung und Verwaltung von Daten im Netzwerk zu ermöglichen. Der Datenbank-Server verwendet MariaDB, eine leistungsstarke und zuverlässige Open-Source-Datenbanklösung.

Der Fokus lag auf der Basisinstallation, der Sicherstellung des SSH-Zugriffs sowie der Zuweisung einer statischen IP-Adresse, um den Server stabil und jederzeit erreichbar zu machen. Diese Konfiguration ermöglicht eine einfache Verwaltung und Nutzung durch alle Projektbeteiligten.


## Was wurde eingerichtet?
1. DB-Container erstellt: Der Server wurde in einem neuen Debian-Container eingerichtet, um eine saubere und isolierte Umgebung für die Datenbank bereitzustellen.

2. SSH-Zugriff konfiguriert: Der SSH-Zugriff wurde eingerichtet und geprüft, um die Fernwartung des Datenbank-Servers sicherzustellen.

3. MariaDB installiert: MariaDB wurde auf dem Container installiert und so konfiguriert, dass eine Anmeldung möglich ist und die vorhandenen Datenbanken aufgelistet werden können.

4. Statische IP-Adresse vergeben: Eine statische IP-Adresse wurde eingerichtet, um die dauerhafte Erreichbarkeit des Servers im Netzwerk sicherzustellen.


## Warum wurde diese Konfiguration gewählt?

- Datenbank-Container: Ein isolierter Container ermöglicht eine saubere Trennung von Anwendungen und Datenbanken, was die Sicherheit und Stabilität erhöht.

- MariaDB als Datenbank: MariaDB ist eine zuverlässige und weit verbreitete Open-Source-Datenbank, die sich für Testumgebungen und produktive Szenarien gleichermaßen eignet.

- SSH-Zugang: Der SSH-Zugang erlaubt eine einfache Verwaltung des Datenbank-Servers aus der Ferne, ohne physisch auf den Container zugreifen zu müssen.

- Statische IP-Adresse: Die Vergabe einer statischen IP-Adresse sichert die Konsistenz in der Netzwerkkommunikation, besonders bei mehreren Clients und Diensten.


## Wie wurde es eingerichtet?

- DB-Container erstellt: Ein neuer Container wurde erstellt, um den Datenbank-Server zu hosten.

- Netzwerkzugriff (DHCP): Der Netzwerkzugriff wurde zunächst über DHCP hergestellt, um den Container ins Netzwerk einzubinden.

- SSH-Zugriff konfiguriert: Nach der Anpassung der Netzwerk-Bridge und Konfiguration wurde der SSH-Zugriff erfolgreich getestet.

- MariaDB-Installation: Nach der Installation wurde die Anmeldung überprüft und die Liste vorhandener Datenbanken abgerufen, um die Funktionalität sicherzustellen.

- Statische IP-Adresse vergeben: Die statische IP-Adresse wurde konfiguriert, um die dauerhafte Erreichbarkeit zu gewährleisten.


## Konfigurationsanleitung

[klicke hier](https://www.digitalocean.com/community/tutorials/how-to-install-mariadb-on-debian-11)
