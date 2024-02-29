## 5.2 Sicherheit und Arbeitsschutz für Roboteranlagen

### Sicherheitsaspekte bei der Anlagenentwicklung

#### Ziele und Definitionen von Sicherheitsbetrachtungen

- **Sicherheit einer Maschine**: Fähigkeit einer Maschine, ihre vorgesehene Funktion während ihrer Lebensdauer auszuführen, woebei das Risiko hinreichend verringert wurde
- **Risiko** = Schadensausmaß $\cdot$ Eintrittswahrscheinlichkeit

#### CE-Kennzeichnung und Überblick über die Normung

- CE-Zertifizierung ist Pflicht für Maschinenhersteller
- Mit ihr wird bestätigt, dass
  - die Maschine den grundlegenden Sicherheits- und Gesundheitsanforderungen der EG-Richtlinien entspricht
  - ein durch die EG-Richtlinien vorgeschriebenes Konformitätsbewertungsverfahren durchgeführt wurde
  - die vorgeschriebene Dokumentation erstellt und ein Dokumentationsverantwortlicher benannt wurde
- Maschinenrichtlinie 2006/42/EG stellt Anforderungen an die Sicherheit und Gesundheitsschutz
- Die Durchführung einer Risikobeurteilung zur Feststellung aller mit dem Betrieb der Maschine verbundenen Risiken ist der zentrale Arbeitspunkt für den Nachweis einer Konformität mit der Maschinenrichtlinie
- Ein Roboter allein ist keine vollständige Maschine, sondern ein Maschinenbauteil, daher ist die CE-Kennzeichnung nicht für den Roboter selbst, sondern für die gesamte Anlage erforderlich $\rightarrow$ Die Verantwortung für die CE-Kennzeichnung liegt beim Integrator

#### Vorgehen zur Gewährleistung der Anlagensicherheit

Iterativer Prozess, bei dem jede Lösung auf ihre Gefährdungen überprüft wird. Wenn die Risiken nicht akzeptabel sind, muss die Lösung angepasst werden.

1. **Entwurf der Maschine**
2. **Definition der Maschinengrenzen**: Definiert Umfang der Analyse
3. **Identifikation der Gefährdungen**: Alle Tätigkeiten in allen Lebenszyklusphasen der Maschine, auch Fehlbedienungen
4. **Risikobeurteilung**: Risiko = Schadensausmaß $\cdot$ Eintrittswahrscheinlichkeit $\rightarrow$ Risikomatrix oder Risikograph

   - **Schadensausmaß**: Schwere der Verletzung
   - **Eintrittswahrscheinlichkeit**: Wahrscheinlichkeit, dass die Gefährdung eintritt
   - **Risikomatrix**: Einteilung in Risikoklassen
   - **Risikograph**: Einteilung in Risikostufen nach Schwere, Häufigkeit und Vermeidbarkeit

5. **OK?**: Wenn nein, (6.) Wenn ja, (7.)
6. **Risikominderung**: Verringerung des Risikos durch
   - Inhärent sichere Konstruktion
   - technische Schutzmaßnahmen
   - organisatorische Schutzmaßnahmen (z.B. Schulung)
   - weiter mit (2.)
7. **Ende**

### Häufige Probleme mit kollaborativen Robotern

- Nutzung nicht sicherer Funktionen für die Risikominderung (Langsamfahrt)
- Vergessen des Werkzeugs als Gefährdung
- Weiche Umhüllungen des Arms hilft wenig, wenn das Werkzeug scharfkantig ist
- Möglichkeit der Kollision mit dem Kopf sorgt für sehr niedrige Kraftgrenzwerte/Geschwindigkeiten $\rightarrow$ unbrauchbare Taktzeiten

$\rightarrow$ Kollaborativer Betrieb rechnet sich in speziellen Anwendungen, ist aber nicht immer die beste Lösung

### Gefährdungsbeurteilung und Einteilung von Schutzmaßnahmen

Es wird vom Betreiber erwartet, dass er sicherstellt:

- Eignung der Maschine für den vorgesehenen Verwendungszweck
- Definition und Umsetzung von Schutzmaßnahmen nach dem TOP-Prinzip (Technische, Organisatorische, Personenbezogene Maßnahmen)
- Bedienungsanleitung und Schulung des Bedienpersonals (v.a. mit Hinblick auf die Gefahren, die von der Maschine ausgehen)
- Festlegung von Wartungs- und Instandhaltungsmaßnahmen
