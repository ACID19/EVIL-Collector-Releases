# EVIL Collector Releases

Fertige Collector-Pakete und signierte Update-Informationen für SimHub. Collector-Quellen, Website/API, Zugangsdaten und private Schlüssel bleiben privat. Debug-Dateien werden nicht ausgeliefert.

## RC.11 – Vorschau

[Passenden Bootstrap herunterladen](https://raw.githubusercontent.com/ACID19/EVIL-Collector-Releases/3309cca7c9cf1019bbef48888f04f2c4fd35ac10/artifacts/d05471ad9ef4542b5e00ce8ada5e672ea7bba18aecc3de0627a202ae24c1d008/0.3.23-iracing-rc.11-bootstrap.zip) · [Anleitung und Prüfumfang](release-notes/rc11.md)

SimHub und Spiele schließen, das ZIP vollständig in einen kurzen Ordner entpacken und `Install.cmd` starten. Danach SimHub öffnen: **Additional plugins → EVIL Motorsport Telemetry → Updates**. Vor der Installation wird die Übereinstimmung der SimHub-Bibliotheken geprüft. Es werden keine GitHub-Zugangsdaten benötigt.

Stable ist vorausgewählt. Für RC.11 bewusst **Vorschau** wählen. Nur der Vorschaukanal ist zunächst veröffentlicht; es gibt noch keine neue FINAL-/Teamfreigabe.

## Signierte Auslieferung

- `channels/<sdk-id>/prerelease.json`: signierte Vorschauinformationen für die passenden SimHub-Bibliotheken.
- `artifacts/<sdk-id>/`: fertige Pakete und signierte Paketinformationen.
- Die signierten Informationen enthalten einen unveränderlichen Commit-Verweis, genaue Länge und SHA-256.
- Der Helfer prüft den fest eingebauten öffentlichen Schlüssel; die Schlüsseldatei im Repo ist reine Dokumentation.

Suchen, Laden und Installieren sind ausdrückliche Schritte. Gleiche/ältere Versionen werden nicht installiert. Die bisherigen Plugin-Dateien werden gesichert und der Start geprüft; Einstellungen und ausstehende Uploads bleiben erhalten. Änderungen am Helfer oder Prüfschlüssel erfordern einen neuen geprüften Bootstrap.
