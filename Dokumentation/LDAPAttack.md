# LDAP Attack

## 1. Man-in-the-Middle 

### **ARP Spoofing + DNS-Paket-Verwerfung mit ettercap**

#### ARP Spoofing Setup:

**ARP Spoofing** sorgt dafür, dass der gesamte Verkehr des Zielsystems (Windows-PC) über dein Kali Linux-System geleitet wird, sodass du die DNS-Pakete abfangen und manipulieren kannst.

##### Schritte:

1. **ARP Spoofing aktivieren**:
   Du wirst ettercap verwenden, um ARP-Spoofing zu konfigurieren, damit der Netzwerkverkehr des Zielsystems (Windows) über dein Kali-System fließt. Hierfür verwendest du die folgende Syntax:   

```bash
sudo ettercap -T -M arp:remote /<Windows IP>// /<Router IP>//
```

   - Ersetze <Windows IP> mit der IP-Adresse des Zielsystems (Windows).
   - Ersetze <Router IP> mit der IP-Adresse des Routers (Gateway).

> Dadurch wird dein Kali-Rechner zum "Man-in-the-Middle", der alle Netzwerkpakete zwischen dem Windows-PC und dem Router abfängt.

2. **Netzwerkverkehr überwachen**:
   Jetzt kannst du den Netzwerkverkehr in Echtzeit überwachen. Wenn du die GUI von ettercap verwendest, kannst du DNS-Pakete und andere Daten anzeigen lassen.

3. **DNS-Anfrage blockieren**:
   Um ein DNS-Paket zu verwerfen, kannst du entweder den DNS-Verkehr vollständig blockieren oder gezielt DNS-Antworten manipulieren. Ein schneller Weg, DNS-Pakete zu blockieren, ist, dies direkt über iptables zu tun (im nächsten Abschnitt beschrieben).


### 2. **Verwendung von iptables zur DNS-Verkehrsblockierung**

Wenn du ein spezifisches DNS-Anfragepaket verwerfen möchtest, kannst du mit **iptables** auf deinem Kali-System gezielt DNS-Anfragen (Port 53) blockieren.

### Schritte:

1. **iptables verwenden, um DNS-Pakete zu blockieren**:
   Um sicherzustellen, dass DNS-Anfragen (Port 53) vom Zielgerät blockiert werden, kannst du folgende iptables-Regeln anwenden:

   - Blockiere alle eingehenden und ausgehenden DNS-Pakete:
     
```bash
# Hinzufügen der Block Regel
sudo iptables -A FORWARD -p udp --dport 53 -j DROP

# Entfernen der Block Regel
iptables -D FORWARD 1
```
   - Dies blockiert den DNS-Verkehr auf Port 53 sowohl von als auch zu deinem Zielsystem (Windows).

2. **Verkehr überprüfen**:
   Teste den DNS-Block, indem du versuchst, vom Windows-PC auf eine Webseite zuzugreifen. Die DNS-Anfrage wird nicht weitergeleitet, und die Verbindung sollte fehlschlagen.

3. **Ergebnisse überprüfen**:
   Verwende tcpdump oder Wireshark auf deinem Kali-System, um zu sehen, ob DNS-Anfragen abgefangen und abgelehnt werden. Du kannst auch die Statusmeldungen von iptables überwachen, um sicherzustellen, dass die Anfragen wirklich blockiert werden.

## Weitere Hinweise:

- **Testing-Umgebung**: Stelle sicher, dass du nur in einer isolierten Testumgebung arbeitest. Tests auf echten Netzwerken oder ohne ausdrückliche Erlaubnis sind illegal und unethisch.
- **Ethical Hacking**: Diese Methoden sollten nur in einer kontrollierten, sicheren Umgebung angewendet werden (z.B. für Penetrationstests oder Labor-Experimente).
- **Schutzmaßnahmen**: Verwende Tools wie ARP-Spoofing-Schutz und DNSSEC, um Netzwerke und DNS-Anfragen zu schützen.

---


Verwendete Tools:
- Ettercap
- iptables
- Responder [GH](https://github.com/SpiderLabs/Responder)