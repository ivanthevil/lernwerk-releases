# Lernwerk für Windows

Lernwerk begleitet das Selbststudium: Module und Prüfungstermine, Lernunterlagen, Transkription von Seminaraufnahmen, Zusammenfassungen, Aufgaben, Karteikarten, Quiz und Probeklausuren. Für die KI-Funktionen wird ein eigener OpenAI-API-Schlüssel benötigt. Lokale Transkription und Texterkennung funktionieren ohne kostenpflichtigen KI-Aufruf.

## Download und Installation

**[Aktuellen Windows-Installer herunterladen](https://github.com/ivanthevil/lernwerk-releases/releases/latest)**

Windows 10 22H2 oder Windows 11, 64 Bit. Den Installer öffnen und dem Assistenten folgen. Die Installation erfolgt für das eigene Windows-Konto; Administratorrechte sind nicht nötig. Ein Startmenü-Eintrag wird angelegt, eine Desktop-Verknüpfung ist optional.

Vor der Installation eine bereits laufende Lernwerk-Version über **Lernwerk → Lernwerk vollständig beenden** schließen. Laufende Verarbeitungen vorher abschließen lassen. Eine alte portable Version muss für den ersten Wechsel einmal mit diesem Installer aktualisiert werden.

Das Paket ist derzeit nicht mit einem Code-Signing-Zertifikat signiert; Windows kann deshalb einen Hinweis auf einen unbekannten Herausgeber anzeigen. Die Datei nur aus diesem Repository beziehen. Für die Prüfung der heruntergeladenen Datei liegt jeder Version `SHA256SUMS.txt` bei.

## Updates

Ab Version 0.2.0 prüft die Windows-App nach dem Start und anschließend alle sechs Stunden auf neue Versionen. In **Einstellungen → Lernwerk aktualisieren** lässt sich die Prüfung auch manuell starten oder abschalten.

Eine neue Version wird in der App angezeigt. **Herunterladen & installieren** lädt den Installer, prüft seine SHA-256-Prüfsumme und öffnet den Installationsassistenten. Lernwerk schließt sich dazu. Laufende Aufgaben und Sprachgespräche müssen vorher beendet werden. Updates werden nicht ohne Klick installiert.

Ab Version 0.2.2 können unterbrochene Downloads fortgesetzt werden, auch nach einem Neustart. Falls der Download in einer älteren Version hängen bleibt, den aktuellen Installer über den Download-Link oben herunterladen und nach dem vollständigen Beenden von Lernwerk ausführen.

Konten, Lernfortschritt, Dateien und Einstellungen liegen getrennt vom Programm. Updates und die Deinstallation behalten diese Daten. Standardordner: `%LOCALAPPDATA%\Lernwerk`; eine vorhandene, von Windows umgeleitete Datenablage wird wiederverwendet. Regelmäßige eigene Datensicherungen sind möglich, indem die App beendet und der gesamte Datenordner kopiert wird.

## Gemeinsames Lernen

Google Drive kann direkt aus Lernwerk verbunden werden; Drive Desktop ist nicht erforderlich. Beide Personen richten ihr eigenes lokales Konto ein und verbinden denselben freigegebenen Lernordner. Module, Quellen und Lernmaterial können geteilt werden. Persönlicher Lernfortschritt und lokale Anmeldung bleiben getrennt. Die einmalige Google-OAuth-Einrichtung ist in der mitinstallierten Anleitung beschrieben.

## Inhalt dieses Repositorys

Dieses Repository enthält ausschließlich Downloads, Versionsinformationen und erforderliche Quellen sowie Lizenzhinweise der mitgelieferten Open-Source-Bibliotheken. Der Lernwerk-Anwendungscode wird hier nicht veröffentlicht. Lernunterlagen, Konten, API-Schlüssel und Google-Anmeldedaten sind nicht Bestandteil des Downloads.

Die Update-Funktion fragt die öffentliche GitHub-Release-API ab; dafür ist keine GitHub-Anmeldung nötig. KI-Inhalte gehen bei angeforderten KI-Aktionen an den konfigurierten Anbieter. Google Drive und Outlook werden nur nach Einrichtung verwendet.

[Versionshinweise](CHANGELOG.md) · [Open-Source-Bibliotheken](THIRD-PARTY.md)
