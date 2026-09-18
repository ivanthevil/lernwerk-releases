# Versionshinweise

## 0.2.5

- Mathematikdarstellung in Tutor, Zusammenfassungen, Aufgaben, Quiz-Optionen und Karteikarten: Brüche, Wurzeln, Indizes, Integrale, Summen, Matrizen und griechische Zeichen. Mehrere übliche LaTeX-Begrenzungen werden erkannt.
- Berechnete 2D-Funktionsgraphen und Diagramme aus Wertepaaren mit mehreren Datenreihen, Achsen und einsehbaren Gleichungen/Werten.
- PDF-Exporte und druckbare Karten behalten Formeln und Diagramme. Fehlerhafte Formeln und überfüllte Karten werden vor dem Druck gemeldet.
- Zusammenfassungen fragen nicht länger nach einer Fragen-/Kartenanzahl.
- Differenzupdate auf Basis von 0.2.4; Lernmaterial, Konten und Einstellungen bleiben erhalten.

## 0.2.4

- Quiz-Antworten werden direkt nach der Auswahl ausgewertet: richtige Antwort grün, falsche Auswahl rot, mit zusätzlichen Textkennzeichnungen.
- Die Erklärung erscheint sofort und benötigt keinen zusätzlichen KI-Aufruf. Die erste Auswahl bleibt für den Versuch bestehen; zur nächsten Frage geht es erst auf Wunsch.
- „Diese Antwort mit dem Tutor besprechen“ setzt eine passende Frage ins Eingabefeld. Der Tutor kennt die gewählte Antwort und den richtigen Lösungsweg. Gesendet wird erst mit „Fragen“.
- Rückmeldungen bleiben beim Wechseln zwischen Fragen und nach erneutem Öffnen des gespeicherten Versuchs sichtbar.
- Probeklausuren behalten ihre Prüfungsbedingungen. Kleines Differenzupdate auf Basis von 0.2.3.

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
