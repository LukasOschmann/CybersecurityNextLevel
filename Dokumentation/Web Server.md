
# Webserver-Konfiguration (Apache2 auf Debian)

**Author:** Ioannis Vavritsas


## Allgemein

Um die Bereitstellung von Webinhalten und Anwendungen sicherzustellen, wurde ein Apache2-Webserver auf einem Debian-Container eingerichtet. Der Apache2-Server dient als zuverlässige und skalierbare Lösung, um Webseiten oder Webanwendungen in einem Netzwerk verfügbar zu machen.

Der Fokus lag auf der Basisinstallation, der Absicherung des Zugangs und der Netzwerkstabilität durch die Vergabe einer statischen IP-Adresse. Diese Konfiguration stellt sicher, dass der Webserver in einer produktiven Umgebung fehlerfrei arbeitet und einfach verwaltet werden kann.


## Was wurde eingerichtet?

1. Apache2-Installation: Der Apache2-Webserver wurde installiert und so konfiguriert, dass die Standard-Webseite erfolgreich geladen wird.

2. SSH-Zugriff: Der SSH-Zugriff wurde sichergestellt, um die Fernwartung und Verwaltung des Webservers zu ermöglichen.

3. Statische IP-Adresse: Eine statische IP-Adresse wurde vergeben, um die Netzwerkkommunikation stabil und konsistent zu gestalten.


## Warum wurde diese Konfiguration gewählt?

Apache2 als Webserver: Apache2 ist ein weit verbreiteter, stabiler und flexibler Webserver, der für viele Anwendungen geeignet ist. Er bietet eine solide Grundlage für die Bereitstellung von Webdiensten.

SSH-Zugang: Durch die Einrichtung des SSH-Zugriffs kann der Server einfach aus der Ferne verwaltet und bei Bedarf angepasst werden.

Statische IP-Adresse: Die Zuweisung einer statischen IP-Adresse stellt sicher, dass der Server im Netzwerk immer unter derselben Adresse erreichbar ist, was besonders in produktiven Umgebungen wichtig ist.


## Wie wurde es eingerichtet?

Apache2: Nach der Installation wurde überprüft, dass die Standard-Webseite korrekt angezeigt wird, um die Funktionsfähigkeit des Servers zu bestätigen.

SSH-Zugriff: Nach der Installation wurden notwendige Konfigurationen vorgenommen, um den Zugriff zu ermöglichen. Nach Abschluss der Änderungen wurde die Funktion überprüft.

Statische IP-Adresse: Die statische IP-Adresse wurde im Netzwerk des Containers festgelegt, um eine dauerhafte Erreichbarkeit zu gewährleisten.

## Konfigurations-Anleitung

[klicke hier](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-debian-11)
