## 3.1 Greifer, Werkzeuge, Messmittel

### Endeffektor = Funktionseinheit eines Robotersystems

- Der Prozess bestimmt die Auswahl des Endeffektors
- ein Prozess ist entweder werkzeuggeführt (z.B. Schweißen) oder werkstückgeführt (z.B. Montage, Handhabung)
- Bei Werkstückführung ist der Endeffektor ein Greifer (oder Spannmittel)
- Das Wirkelement erfüllt die Hauptfunktion des Endeffektors, es bewirkt den Prozess. Das sind Greifer, Werkzeuge, Mess- und Prüfmittel
- Das Zubehör erfüllt eine Hilfsfunktion, es unterstützt den Prozess. Hierzu gehören Wechselsysteme, Ausgleichssysteme, Messsysteme.
- Die Peripherie ist die Umgebung des Roboters, sie ermöglicht den Prozess. Hierzu gehören Kabelschutz, Wechselstationen, Reinigungssysteme. Sie sind keine Bestandteile des Endeffektors.
- Größe, Kosten, Gewicht und Komplexität variieren bis zum Faktor 1000.

### Greifer

- Es wirken statische, dynamische und prozessbedingte Kräfte auf den Greifer
- Es gibt viele unterschiedliche Greiferarten, die sich in der Art des Greifens, der Anzahl der Greifpunkte und der Art der Aktuierung unterscheiden
- Greifprinzipien: Klemmgreifer, Sauggreifer, Magnetgreifer, Nadelgreifer, Aufwälzgreifer, Ultraschall/Bernoulli-Greifer
- Flexible Greifer haben unterschiedliche Greifbacken an einem Finger oder wechselbare Finger oder können sich (aktiv oder passiv) verformen
- Die Bereitstellung der zu greifenden Teile ist ein wichtiger Bestandteil der Greiferwahl/-konstruktion
- Die Greifplanung kann einerseits vordefiniert sein, andererseits kann sie auch adaptiv gelöst werden (Automatisierung der Automatisierung)
- Griffpositionen können manuell oder automatisch am Bauteil bestimmt werden oder ohne Modell der Bauteil(lage) bestimmt werden. Greifstrategien hängen von den jeweiligen Greifprinzipien ab.

### Werkzeuge, Mess- und Prüfmittel

- Roboterwerkzeuge basieren meist auf Handwerkzeugen (Schweißpistole) oder Maschinenwerkzeugen (Frässpindel), sie können aber auch speziell für den Roboter entwickelt werden (z.B. Wickeln von Sattelspulen)
- Zusätzliche Achsen und Sensoren ermöglichen eine Prozessregelung

| Arbeitsschritt | Werkzeug |
| --- | --- |
| Schweißen | Schweißpistole, Schweißzange, Schweißlaser |
| Bearbeiten | Frässpindel, Entgratspindel, Schleifwerkzeug, Strahlpistole |
| Beschichten, Kleben | Lackierpistole, Klebepistole, Spritzpistole |
| Messen, Prüfen | Laserkamera, Ultraschall, Röntgen |

### Zubehör

| Funktion    | Zweck                                                    |
| ----------- | -------------------------------------------------------- |
| Wechseln    | Austauschen von Effektoren für unterschiedliche Prozesse |
| Schützen    | Durch Auslenken bei Kollisionen/Notabschaltung           |
| Ausgleichen | Kompensieren von Toleranzen und Verformungen             |
| Messen      | Erfassen von Prozessgrößen (Kräfte, Momente)             |
| Durchführen | Elektrik, Pneumatik, Hydraulik, Datenübertragung         |

### Peripherie

- Die Peripherie ermöglicht den Betrieb des Endeffektors
- Kabel und Schläuche
  - müssen schleppkettentauglich bzw. robotertauglich sein
  - sollen in Kabelschutzschläuchen oder Schleppketten geführt werden
- Sensor- und Aktorverteiler reduzieren die Kabelanzahl und erleichtern Inbetriebnahme, Wartung, Reparatur

### Fazit

- Die Entwicklung oder Auswahl von Greifern und Werkzeugen unterliegt vielen Einflussfaktoren und ist daher anwendungsspezifisch
- Einfache Aufgaben:
  - es existieren Komponenten und Baukästen
  - immer ist mindestens die Auswahl und Integration notwendig
- Komplexere Aufgaben:
  - Oft Sonderanfertigung oder komplette Neuentwicklung $\rightarrow$ Greifer und Werkzeuge sind Anpass- oder Sonderkonstruktionen
