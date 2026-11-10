# EVIL Collector Releases

Fertige Collector-Pakete und signierte Update-Informationen für SimHub. Collector-Quellen, Website/API, Zugangsdaten und private Schlüssel bleiben privat. Debug-Dateien werden nicht ausgeliefert.

## RC.16 – Vorschau

**Aktuelle Vorschau: 0.3.23-iracing-rc.16.** Korrigiert iRacing-Sektoren bei verzögertem Uhrenreset, den Kontext von Offline-Tests und die vorhandene Access-Anmeldung für lokale IBT-Aufzeichnungen. [Änderungen und Prüfumfang](release-notes/rc16.md) · [Prüfnachweis](release-notes/rc16-evidence.json).

### Update direkt in SimHub

Für vorhandene RC.13-, RC.14- oder RC.15-Installationen mit Helfer 2.0.0:

1. LMU und iRacing vollständig schließen. SimHub öffnen.
2. **Additional plugins → EVIL Motorsport Telemetry → Updates** öffnen.
3. **Vorschau – RC-Versionen (bewusst wählen)** auswählen.
4. **Nach Updates suchen** drücken. Angezeigt werden muss **0.3.23-iracing-rc.16**.
5. **Herunterladen und prüfen** drücken.
6. **Update installieren** drücken und die Bestätigung lesen. SimHub wird geordnet geschlossen und wieder gestartet; eine erforderliche Windows-Freigabe bitte bestätigen.
7. Nach dem Neustart die installierte Version **0.3.23-iracing-rc.16** kontrollieren.

Stable ist weiterhin vorausgewählt. Suchen, Laden und Installieren sind getrennte ausdrückliche Schritte. Gleiche oder ältere Versionen werden nicht installiert. Alte Plugin-Dateien werden gesichert; Einstellungen und wartende Uploads bleiben erhalten. Es wird hier keine Installation automatisch gestartet.

### Vollständiges Installationspaket

[RC.16-Installationspaket herunterladen](https://raw.githubusercontent.com/ACID19/EVIL-Collector-Releases/e1839271b3749189e4912278ba3bc7239e955bc5/artifacts/d05471ad9ef4542b5e00ce8ada5e672ea7bba18aecc3de0627a202ae24c1d008/0.3.23-iracing-rc.16-bootstrap.zip) · [Signierte Paketinformation](artifacts/d05471ad9ef4542b5e00ce8ada5e672ea7bba18aecc3de0627a202ae24c1d008/0.3.23-iracing-rc.16-bootstrap.signed.json).

RC.11/RC.12 haben einen älteren Helfer und benötigen dieses neue vollständige Installationspaket. Der direkte Updateversuch wird dort mit einem Hinweis auf den benötigten Helfer abgelehnt. SimHub und Spiele schließen, das ZIP vollständig in einen kurzen neuen Ordner entpacken und `Install.cmd` starten. Das Paket prüft die passenden SimHub-Bibliotheken vor Änderungen. Es sind keine GitHub-Zugangsdaten erforderlich.

## Signierte Auslieferung

- `channels/<sdk-id>/prerelease.json`: signierte Vorschau für die passenden SimHub-Bibliotheken.
- `artifacts/<sdk-id>/`: unveränderliche Paketdateien und signierte Paketinformationen.
- Die Signatur bindet einen festen Commit-Verweis, genaue Länge und SHA-256. Der Helfer prüft den fest eingebauten öffentlichen Schlüssel.
- Nur der Vorschaukanal wird aktualisiert. RC.16 ist keine FINAL-/Teamfreigabe; die frische Fahrabnahme und bestätigte IBT-Serverzuordnung stehen noch aus.

Die bisherige [RC.11-Dokumentation](release-notes/rc11.md) und ihre Artefakte bleiben erhalten. Änderungen am Helfer oder Prüfschlüssel erfordern ein neues geprüftes vollständiges Installationspaket.
