# Versionshinweise

## 0.3.1

Lernwerk 0.3.1 ergänzt die Wiederherstellung des eigenen Kontozugangs.

- **Passwort vergessen?** ist direkt in der Anmeldung erreichbar. Bestätigung in der lokalen Windows-App oder ein zuvor gespeicherter Wiederherstellungscode erlaubt das Festlegen eines neuen Passworts.
- **Anmeldename vergessen:** Bei der Bestätigung in Windows kann das vorhandene lokale Konto ausgewählt werden. Nach erfolgreicher Wiederherstellung wird der Anmeldename angezeigt.
- **Mein Konto & Passwort** in den Einstellungen: Passwort ändern und einen persönlichen Wiederherstellungscode erstellen oder erneuern. Der Code wird einmal angezeigt und kann als Textdatei gesichert werden. Er wird nur gehasht gespeichert und nicht über Drive geteilt.
- Die Wiederherstellung verwendet die Datenbank des laufenden Lernbereichs. Konto-ID, Module, Dateien und Lernfortschritt bleiben erhalten. Alte Anmeldungen und Wiederherstellungscodes werden nach einer Passwortänderung ungültig.
- Native Bestätigungen sind auf lokale Anfragen beschränkt, müssen im Windows-Fenster ausdrücklich bestätigt werden und verfallen nach fünf Minuten. Codes sind nur einmal verwendbar. Fehlversuche werden begrenzt.

Ein E-Mail-Versand wird nicht benötigt. Ohne vorherigen Code muss die lokale Windows-App auf dem PC des Kontos laufen. Das Passwort wird vom Nutzer selbst eingegeben; ein vergessenes Passwort kann nicht ausgelesen werden.

Differenzupdate auf Basis von 0.3.0. Der bestehende Zugang wird beim Update nicht geändert. Anmeldung, Wiederherstellung und Datenerhalt wurden mit isolierten Testkonten geprüft.


## 0.3.0

Lernwerk 0.3.0 verbindet Seminarorganisation, Rechenübungen und einen interaktiven Lehrer.

- **Module und Quellen:** „Modul bearbeiten“ und „Modul löschen“ stehen direkt im Modulkopf. Das Löschen gemeinsamer Module bleibt dem Verwalter vorbehalten. Quellen lassen sich verschieben oder mit Dateinamenbestätigung aus dem Lernbereich entfernen. Löschungen werden abgeglichen; ältere Materialien und Originaldateien bleiben erhalten.
- **Prüfungstipps:** eigener Reiter für Hinweise und Altklausuren. Neue Lernmaterialien berücksichtigen diese als Niveauvorlage. Für Prüfungen reservierte Quellen bleiben vom normalen Üben ausgeschlossen.
- **Seminarplan und Schulaufgaben:** Termine aus Organisationsunterlagen werden als prüfbare Vorschläge angelegt. Manuelle Termine und Uploads pro Seminar sind möglich. Die KI kann belegte Arbeitsaufträge mit Fristen erkennen; Erledigt-Haken gelten pro Person. Automatische Erkennung nach passenden Uploads lässt sich unter Einstellungen → Budget & Nutzung abschalten. Sie nutzt den API-Schlüssel und das Budget.
- **Aktuelle Prüfungsvorbereitung:** Quellenänderungen aktualisieren bestehende offene Pläne. Ältere Lernmaterialien werden gekennzeichnet; neue Übungen nutzen den aktuellen Stand. Bereits erledigte Einheiten bleiben erhalten.
- **Rechenaufgaben:** vollständige Aufgabenstellungen, Zahlenergebnis mit Einheit, optionale Formel-Eingabe mit Vorschau, Ergebnisprüfung oder Musterlösung auf Wunsch. Ohne Sofortprüfung erfolgt Rückmeldung bei Abgabe. Zahlenresultate werden lokal geprüft; Rechenwege bleiben für den Tutor erhalten, erhalten in diesem Modus aber keine automatischen Teilpunkte.
- **KI-Lehrer:** Dialog mit schrittweiser Tafel, Formeln, Pfeilen und Grundlagen. Textantworten fließen in den nächsten Unterrichtsschritt und persönlichen Lernschwerpunkt ein. Ein bestehender offener Lernplan wird angepasst. Der Sprachlehrer kann Tafelschritte zeigen und auch Texteingaben entgegennehmen. Sprache benötigt separat verfügbaren Realtime-Modellzugang; bestehende Zeit- und Budgetgrenzen gelten weiter.
- **Vorlesungsmodus (Vorschau):** in der lokalen Windows-App ein geöffnetes Teams-Präsentationsfenster wählen, ausschließlich die Folienfläche markieren und ein Wiedergabegerät wählen. Ton und zugeschnittenes Bild werden fortlaufend auf Festplatte gespeichert. Pausen, reiner Ton, Ausblenden des Bildes, Wiederaufnahme gespeicherter Daten und Übergabe an Transkription/Bildanalyse sind vorgesehen. Optionale KI-Notizen entstehen abschnittsweise, ungefähr alle fünf Minuten. Bei Rückstand wird nicht jeder Abschnitt live analysiert; die vollständige Datei wird anschließend verarbeitet.

Die Aufnahme erkennt Teilnehmerbilder nicht automatisch. Beim Ende der Präsentation „Bild ausblenden“ wählen; Teams nicht minimieren. Der Ton enthält sämtliche Stimmen und Wiedergaben auf dem gewählten Gerät. Eine garantierte Trennung der Dozentenstimme ist nicht enthalten. Nur erlaubte Aufnahmen starten. Der Vorlesungsmodus und die neue Sprachtafel sind noch nicht in einer echten Teams-Sitzung bzw. bezahlten Realtime-Sitzung erprobt; Medienverarbeitung, Abbruchrettung und Oberflächen wurden mit synthetischen Daten getestet.

Beide PCs auf 0.3.0 aktualisieren, bevor neue Seminardaten abgeglichen werden. Konten, Schlüssel und Lernfortschritt bleiben lokal. Das Differenzupdate basiert auf 0.2.5 und enthält geänderte/neue Dateien; fehlende Zwischenversionen werden bei Bedarf nachgeladen.

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
