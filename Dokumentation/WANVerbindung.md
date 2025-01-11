# WAN Verbindung

Author: Lukas Oschmann

## Allgemein

Die Anbindung der Firewall an das Internet ist, da wir die Projektumgebung in der Schule aufgebaut haben, 
nur über das Schulnetz möglich. Leider war im Netzwerklabor keine Kabelgebundene Internetverbindung möglich, 
weshalb wir die Anbindung per WLAN realisieren mussten.Die Firewall hat keine WiFi Schnittstelle, also mussten wir auf einen WLAN-zu-Kabel Adapter zurückgreifen. 

Das verwendete Gerät ist ein [BrosTrend AX1500](https://www.amazon.de/dp/B0C4DKZVCM?ref=ppx_yo2ov_dt_b_fed_asin_title). Wir haben uns für diesen entschieden, da er über einen Gigabit RJ45 Port verfügt. 

## Einrichtung

> Das Passwort für die Managmentoberfläche des Verstärkers steht im KeePass

1. Gerät in die Steckdose stecken und per LAN-Kabel verbinden.
2. In der Adresszeile des Browsers die Seite *http://brostrendwifi.com* aufrufen
3. Passwort vergeben für WebUI
4. Modus des Gerätes auswählen: *Extender Mode / WiFi to Ethernet Adapter Mode*
5. WiFi Netz, welches verwendet werden soll, auswählen
6. Es gab die Möglichkeit die SSIDs der Netzwerke zu verändern, die der Verstärker ausstraht. Das habe ich jedoch nicht getan und die Standardeinstellungen beibehalten.
7. Neustart des Verstärkers und aufwählen auf der Managmentoberfläche über den RJ45 Port
8. WiFi-Settings -> Ausstrahlende Netzwerke versteckt

