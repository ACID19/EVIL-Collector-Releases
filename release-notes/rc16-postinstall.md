# RC.16: tatsächliches SimHub-Update geprüft

Am 10.11.2026 um 09:44:42 Uhr (Europe/Berlin) wurde das manuell über SimHub gestartete Update erfolgreich abgeschlossen. Die installierte DLL entspricht exakt dem signierten RC.16-Paket. Status und Journal melden `complete` / `UPDATE_INSTALLED`; Neustartbestätigung, Controller und DLL-Prüfsumme passen zusammen. SimHub läuft und reagiert, der neue Collector-Start ist protokolliert. Keine Warnung/Fehler im aktuellen SimHub-Startlog und kein Collector-ERROR seit dem RC.16-Start.

Alte DLL und Debug-Datei sind nach Prüfsumme korrekt gesichert. Einstellungen und geschützte Upload-Warteschlangen stimmen weiterhin mit dem Gesamtfingerabdruck vor dem Austausch überein. Helfer und SimHub-Schnittstellen sind unverändert.

## Offener IBT-Befund

Der korrigierte Access-Zugang funktioniert: Fähigkeiten-GET mit installierter RC.16 ergibt HTTP 200. Der IBT-Dienst hat alle sechs bereits vor dem Update vorhandenen Originaldateien vollständig als 28 Abschnitte übernommen, 130.729 Originalframes ohne Lücken. Alle 28 Abschnitte bestehen die aktuelle API-Datenprüfung und stimmen mit den Originaldateihashes überein.

Der Server stellt die Übertragung mit HTTP 409 zurück. Diese Route verwendet 409 bei fehlender oder mehrdeutiger Zuordnung zu einer Serversitzung. Der vorhandene Collector-Log enthält den genauen Antwortcode nicht; welcher Unterfall vorliegt, ist damit noch nicht bestätigt. Alle sechs Originaldateien teilen dieselbe native Sitzungskennung. Die 28 Abschnitte bleiben lokal erhalten; noch kein bestätigter IBT-Dateiupload. Die normale Rundenupload-Warteschlange ist leer.

Frische RC.16-Fahrdaten für Sektoren und Offline-Test-Kontext stehen noch aus. Die Installationsprüfung hat keinen zusätzlichen Datei-POST und keine Serveränderung ausgeführt. [Maschinenlesbarer Prüfnachweis](rc16-evidence.json).
