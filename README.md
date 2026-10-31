# EVIL Collector Releases

Fertige EVIL-Motorsport-Collector-Pakete und signierte Update-Informationen für SimHub.

Dieses öffentliche Repository enthält keine Collector-Quellen, Website-/API-Quellen, Zugangsdaten oder privaten Signaturschlüssel. Debug-Dateien mit lokalen Pfaden werden nicht ausgeliefert.

- `channels/<sdk-id>/stable.json`: signierte Informationen zum freigegebenen Stable-Stand.
- `channels/<sdk-id>/prerelease.json`: signierte Informationen zu ausdrücklich gewählten Vorschauversionen.
- `artifacts/<sdk-id>/`: fertige Pakete; die signierten Informationen verweisen auf einen unveränderlichen Commit und enthalten Länge sowie SHA-256.

SimHub sucht und installiert nur auf ausdrücklichen Wunsch. Paketsignatur, Prüfsumme, Version, Update-Helfer und exakte SimHub-Bibliotheken werden geprüft. Gleiche oder ältere Versionen werden nicht installiert. Vor dem Austausch werden die bisherigen Plugin-Dateien gesichert und nach dem Neustart geprüft. Einstellungen und ausstehende Uploads bleiben erhalten.

Für die erstmalige Einrichtung wird das passende Bootstrap-Paket benötigt. Vorschauversionen sind keine Stable-/Teamfreigabe. Änderungen am Update-Helfer oder Prüfschlüssel erfordern einen neuen geprüften Bootstrap.
