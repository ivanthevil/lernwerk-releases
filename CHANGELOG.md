# Versionshinweise

## 0.2.3

- Dateibasierte Differenzupdates: 17,3 MB statt 326,8 MB für dieses Update. 967 unveränderte Programmdateien werden auf dem PC weiterverwendet und mit SHA-256 geprüft.
- Der Installer lädt eine fehlende oder beschädigte Basis bei Bedarf automatisch nach. Bei Erstinstallationen ist daher eine Internetverbindung erforderlich. Ältere veröffentlichte Versionen bleiben als Basis verfügbar.
- Der Veröffentlichungsablauf verwendet beim nächsten Build den verifizierten Stand der zuletzt veröffentlichten Version und entfernt vor der Freigabe alle temporären Uploadteile.
- Enthält die folgenden Verbesserungen der nicht veröffentlichten Version 0.2.2:

- Update-Downloads setzen nach Verbindungsabbrüchen bereits geladene Daten fort, auch nach einem Neustart. Größe und SHA-256 des vollständigen Installers werden vor der Installation geprüft.
- Module können im Überblick mit Bestätigung ihres Namens gelöscht werden. Die Löschung wird mit dem Lernpartner synchronisiert; beide benötigen Version 0.2.2 oder neuer. Quelldateien und ältere Drive-Sicherungspakete bleiben als Sicherheitskopien erhalten.
- Zusätzliche Lernmodelle: GPT-5 Mini, GPT-5.4 Mini und GPT-5.4. Verständliche Modellprüfung, wenn nur Bildmodelle freigegeben sind.
- Schnellere direkte Google-Verbindungen unter Windows bei nicht erreichbarem IPv6, mit Rückfall auf die normale Netzwerkauswahl bei Verbindungsfehlern.
- Vorhandene Proxy-Einstellungen bleiben erhalten.
- Verständliche Meldung nach 90 Sekunden ohne Antwort bei der Ordnerauswahl.
- Konten, Lernunterlagen und Einstellungen bleiben erhalten.

## 0.2.0

- Windows-Installer mit Startmenü-Eintrag und optionaler Desktop-Verknüpfung.
- Update-Hinweise, manuelle und automatische Versionsprüfung sowie geprüfter Download in der App.
- Installationsschutz bei laufenden Aufgaben und Sprachgesprächen; der Installer wartet auf das Ende der App.
- Bestehende Konten, Lernmaterial und Einstellungen bleiben bei Aktualisierung und Deinstallation erhalten.
- PDF-Verarbeitung mit PDFium; Medienverarbeitung mit einem LGPL-FFmpeg-Paket.
- Erforderliche Bibliotheksquellen und Lizenzhinweise separat verfügbar.
