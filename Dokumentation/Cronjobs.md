
# Cronjob-Konfiguration

**Author:** Ioannis Vavritsas


## Allgemein

Um die Systemstabilität und Verfügbarkeit sicherzustellen, wurde für die Systeme Jumphost und Web Server ein regelmäßiger Neustart mittels Cronjobs eingerichtet.

Cronjobs ermöglichen die automatisierte Ausführung von Aufgaben zu vordefinierten Zeiten und stellen sicher, dass die Systeme in regelmäßigen Abständen neu gestartet werden, um Speicherlecks und andere potenzielle Probleme zu vermeiden.

Diese Maßnahmen dienen der Wartung und erhöhen die Zuverlässigkeit der Systeme, insbesondere in produktiven Umgebungen.


## Verwendung

1. Systempflege: Regelmäßiger Neustart sorgt für eine stabile und performante Laufzeit der Systeme.
2. Automatisierung: Kein manueller Eingriff notwendig, da die Neustarts automatisch gemäß Zeitplan erfolgen.
3. Fehlervermeidung: Reduziert die Wahrscheinlichkeit von Problemen durch langfristige Systemausführung.


## Zeitpläne:

- Jumphost: Sonntag, 01:00 Uhr
- Web Server: Sonntag, 00:00 Uhr
