## Login

- Die Funktion „Angebotsaufforderung“ darf nur von angemeldeten Nutzern verwendet werden.
- Wenn ein nicht eingeloggter Nutzer auf „Anbieter auswählen“ klickt, soll ein Dialogfenster erscheinen.
- Das Dialogfenster soll den Nutzer dazu auffordern, sich anzumelden, bevor er die Funktion nutzen kann.
- Das Dialogfenster muss eine klare Call-to-Action enthalten, z. B. „Zum Login“.
- Der Dialog soll einen Schließen-Button haben, um zur Seite zurückzukehren, ohne den Login-Vorgang zu starten.
- Der Zustand „angemeldet / nicht angemeldet“ soll über ein visuelles Icon in der Topbar angezeigt werden.
- Eingeloggte Nutzer sollen direkt in den Auswahlmodus gelangen können, ohne dass das Dialogfenster erscheint.
- Nicht eingeloggte Nutzer sollen den Login-Dialog erhalten, bevor Auswahl- und Angebotsaktionen möglich sind.

## Anbieterverzeichnis

- Im Anbieterverzeichnis soll ein eigener Bereich mit dem Titel „Angebotsaufforderung“ ergänzt werden.
- Dieser Bereich wird nach Klick auf „Anbieter auswählen“ erweitert und zeigt die Auswahlsteuerung.
- Im erweiterten Zustand sollen folgende Elemente sichtbar sein:
  - „Alle gefilterten auswählen“
  - „Auswahl leeren“
  - „Auswahl beenden“
  - Anzeige der Anzahl aktuell ausgewählter Anbieter
- Sobald mindestens ein Anbieter ausgewählt wurde, soll zusätzlich der Button „Angebotsaufforderung erstellen“ eingeblendet werden.
- Der Button „Angebotsaufforderung erstellen“ darf nur sichtbar sein, wenn mindestens ein Anbieter markiert ist.
- Die Auswahlsteuerung soll auch nach Paginationwechseln bestehen bleiben und den aktuellen Modus beibehalten.
- Der erweiterte Bereich darf keine vollständige Seitenaktualisierung auslösen, sondern muss inline in der bestehenden Seite erscheinen.
- Die Steuerungsleiste soll prominent genug sein, um das Auslösen von Aktionen wie „Alle gefilterten auswählen“ oder „Auswahl beenden“ direkt möglich zu machen.
- Das Login-Dialogfenster soll als Overlay mit leicht getöntem Hintergrund erscheinen.
- Das Overlay darf die Seite nicht verlassen, wenn der Nutzer nur den Schließen-Button verwendet.
- Der Anbieterverzeichnisbereich soll nach Aktivierung reduziert Platz einnehmen, wenn er zusammengeklappt ist.
- Der aktive Auswahlmodus soll jederzeit erkennbar sein, z. B. durch zusätzliche Kopfzeile, farbige Markierung oder Text.
- Innerhalb des Auswahlmodus sollen Aktionen wie „Auswahl beenden“ und „Auswahl leeren“ immer erreichbar bleiben.
- Wenn der Nutzer die Seite verlässt oder den Modus beendet, soll der Status der eingeloggenen Session erhalten bleiben, damit der Auswahlmodus bei Rückkehr nicht unerwartet gesperrt ist.
- Nicht eingeloggte Nutzer dürfen keine Auswahl treffen; der Zugang zu allen Auswahlaktionen ist erst nach Login verfügbar.

## Auswahlverhalten

- Nach Aktivierung von „Anbieter auswählen“ sollen alle Anbieter-Cards visuell leicht ausgegraut dargestellt werden.
- Auf jeder Card soll oben links eine Checkbox eingeblendet werden.
- Die gesamte Fläche einer Card soll klickbar sein, nicht nur die Checkbox.
- Klick auf eine Card toggelt den Auswahlzustand des Anbieters.
- Ausgewählte Cards sollen hervorgehoben werden, indem sie die vorherigen Farben einnehmen.
- Ausgewählte Anbieter müssen beim Wechsel über die Pagination hinweg erhalten bleiben.
- Beim Zurückkehren auf eine Seite mit bereits ausgewählten Anbietern muss dieser Status korrekt wiedergegeben werden.
- Checkboxen sollen nur im aktiven Auswahlmodus angezeigt werden.
- Beim Beenden des Auswahlmodus („Auswahl beenden“) kehrt die Seite in den normalen Zustand zurück; die Auswahl bleibt weiterhin im Hintergrund bestehen, bis sie explizit gelöscht wird.
- „Auswahl leeren“ entfernt alle aktuellen Selektionen und setzt den Zähler auf 0.
- „Alle gefilterten auswählen“ wählt alle aktuell sichtbaren Anbieter aus dem aktuellen Filter- und Sucheergebnis aus.
- Der Zähler der ausgewählten Anbieter aktualisiert sich sofort bei jedem Auswahl- oder Deselektionsvorgang.
- Die Auswahl von Anbietern muss seitenübergreifend persistent bleiben, solange der Auswahlmodus aktiv ist.
- Der Status der ausgewählten Anbieter soll pagination-unabhängig im State gehalten werden.
- Das State-Modell soll eine Liste eindeutiger Anbieter-IDs oder Vergleichskennzahlen enthalten.
- Pagination, Filter und Suche dürfen die Auswahl nicht zurücksetzen.
- Die Benutzeroberfläche muss den aktiven Auswahlmodus klar signalisiert haben.
- Inaktivere Elemente außerhalb des Auswahlmodus (z. B. „Angebotsaufforderung erstellen“) sollen nicht sichtbar oder deaktiviert sein.
- Für prototypische Zwecke müssen alle interaktiven Elemente verständliche Beschriftungen und klare visuelle Zustände besitzen.
- Die wichtigsten Aktionen im Auswahlmodus müssen auch über Tastaturbedienung erreichbar sein.

## Angebotsaufforderungs-Seite

- Die Angebotsaufforderungs-Seite soll nur über den aktiven Auswahlmodus des Anbieterverzeichnisses zugänglich sein.
- Auf der Seite müssen ausgewählte Anbieter, Kontaktinformationen und Angebotsdetails klar strukturiert sein.
- Die Seite soll als mehrstufiger Prozess umgesetzt werden:
  - Schritt 1: Darstellung der ausgewählten Anbieter
  - Schritt 2: Bedarf beschreiben mit text-input field
  - Schritt 3: Kontaktdaten, die per Button aus Profil übernommen werden können
  - Schritt 4: Rahmenbedingungen mit optionalem text-input field
  - Schritt 5: Optionaler Scope und Systemlandschaft Bereich
  - Schritt 6: Veröffentlcihung und Matching mit CTA Button
- Es muss klar angezeigt werden, wie viele Anbieter in der Angebotsaufforderung enthalten sind.
- Die Kontaktdaten sollen optional aus dem Nutzerprofil geladen werden können und gleichzeitig manuell editierbar sein.
- Pflichtfelder für den Angebotsweg müssen klar gekennzeichnet sein (z. B. Name, E-Mail, Telefonnummer, Unternehmen).
- Bei unvollständigen Kontaktdaten muss eine freundliche Fehlermeldung angezeigt werden, bevor der nächste Schritt aktiviert wird.
- Die Seite soll den Nutzer über den Verlauf des Prozesses informieren (rechte Seitenleiste mit Schritten-Übersicht).
- Der Button „Angebotsaufforderung erstellen“ ist durchgehend aktiv, bei Ausführung des Buttons bei fehlenden Pflichtfeldern werden diese markiert und es wir automatisch zu diesen "gesprungen"
- Beim Erstellen der Angebotsaufforderung sollen die getätigten Eingaben des Anwenders mit den Inhalte zusammengefasst als PDF Dokument an die jeweiligen ausgewählten Anbieter per Mail geschickt werden.
- Jeder PDF-Eintrag soll die Anbieterbezeichnung, Kontaktdaten, Angebotsdetails und ggf. Angebotsvalidierung enthalten.
- Es muss eine Bestätigungsmeldung geben, nachdem die Angebotsaufforderungen versendet wurden.
- Die Seite sollte eine Möglichkeit bieten, zur Anbieterübersicht zurückzukehren, ohne den aktuellen Fortschritt zu verlieren.
- Bei Abbruch des Ausfüllens des Formulars soll der Status erhalten bleiben, wenn der Nutzer zurückkehrt.
- Der Nutzer darf nicht in der Angebotsaufforderungs-Seite landen, wenn keine Anbieter ausgewählt wurden.
- Technisch soll die Angebotsaufforderungs-Seite die ausgewählten Anbieter, der ausgewählten Filter und die ausgewählten Themenfelder aus dem Anbieterverzeichnis übernehmen.
- Validierung und Formatprüfung der Angaben sollen clientseitig erfolgen, um schnelle Rückmeldung zu ermöglichen.
- Dem Nutzer soll es ermöglicht werden in der Angebotsaufforderungs-Seite die Unternehmen nachträglich noch zu entfernen, dadurch werden die zusammengehörigen Themenfelder ebenfalss entfernt, falls andere ausgewählte Unternehmen diese nicht besitzen.

