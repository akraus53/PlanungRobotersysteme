# Zusammenfassung "Planung von Robotersystemen"

**Stand: WS 2023/24**

Dieses Repository enthält eine Zusammenfassung der Vorlesung "Planung von Robotersystemen" für das Wintersemester 2023/24. Falls Du Verbesserungsvorschläge oder Aktualisierungen hast, zögere nicht, sie beizusteuern. Dein Beitrag ist immer willkommen!

## Wie arbeite ich mit Markdown?

Markdown ist eine coole und einfache Auszeichnungssprache, die uns hilft, Texte strukturiert zu gestalten. Falls Du noch nicht vertraut damit bist, keine Sorge – es ist super leicht zu lernen. Für die Bearbeitung der Zusammenfassung empfehle ich die Verwendung von Visual Studio Code (VS Code). Falls Du das nicht hast, kannst Du es [hier](https://code.visualstudio.com/) herunterladen.

## Markdown-Converter-Extension

Um die Markdown-Datei in HTML zu verwandeln, benutze die Markdown-Converter-Extension für VS Code. Hier sind die Schritte, um sie einzurichten:

1. Öffne VS Code und klicke auf das Extensions-Symbol in der linken Leiste und installiere die Extension "Markdown-Converter" von manuth.
1. Öffne die Einstellungs-Datei von Visual Studio Code indem du in die Leiste oben in der Mitte klickst und ">JSON" eingibst. Wähle "Einstellungen: Öffnen (JSON)".
1. Füge unten an die Datei (aber innerhalb der geschweiften Klammer) eine weitere Einstellung an, damit Markdown-Converter unsere Zusammenfassung in HTML umwandelt:
   ```json
   "markdownConverter.ConversionType": ["HTML"],
   ```
1. Klicke die Leiste oben in der Mitte von VS Code und tippe ">" um den Befehl "Markdown: Convert Document" zu finden.
1. Drücke Enter und warte auf den Abschluss des Prozesses.

Ärgerlicherweise respektiert die Erweiterung (wegen einem Chromium-Bug) die CSS-Regeln nicht, die wir in der HTML-Datei verwenden. Deshalb müssen wir die HTML-Datei im Browser öffnen und von dort aus drucken.

## HTML im Browser drucken

Die generierte HTML-Datei kannst Du einfach im Webbrowser öffnen. Achte darauf, dass der Markdown-Converter die CSS-Regeln richtig interpretiert, damit das Layout korrekt angezeigt wird. Anschließend kannst Du die Zusammenfassung im Browser öffnen und als PDF drucken.

## Feedback und Mitarbeit

Falls Du Ideen zur Verbesserung oder Aktualisierung hast, nur zu! Erstelle einen Fork dieses Repositories, mache Deine Änderungen und reiche einen Pull-Request ein. Gemeinsam machen wir diese Zusammenfassung noch besser!

Danke für Deine Unterstützung! 🚀
