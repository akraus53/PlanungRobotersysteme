## 3.3 Roboterprogrammierung und Zellsimulation

### Roboterprogrammierung Grundlagen

- Ziel ist , die Aufgabe des Roboter zu definieren und **Planungsdaten** zu erhalten (z.B: Taktzeiten)
- Programmierung kann **online** (vor Ort, Handgerät/Vormachen) oder **offline** (von einem anderen Ort, ohne Roboter. Simulativ oder automatisch) erfolgen
- Zeitaufwand: Faustregel 1min/Punkt bei **Online-Programmierung** mit Handgerät

### Online-Programmierung

#### Programmierhandgerät

- Definieren der Bewegung durch anzufahrende Punkte, Bewegungsart (PTP, Bogen, ...) und Bewegungsparameter (Geschwindigkeit, Beschleunigung, ...)
- Definieren des Prozessablaufs (meist durch warten auf Signale, setzen von Ausgängen, ...)
- Unterschiedliche Handgeräte: Touchscreen, Tastatur, Joystick, 3D-Maus, ...
- Bei üblichen Werkstücken kann mit einem Tag **Programmieraufwand** pro Werkstück gerechnet werden (450 Punkte entsprechen 7,5h **Programmieraufwand**)

#### Programmieren durch Vormachen

- Statt die Punkte einzugeben, kann der Roboterführer die Bewegungen vormachen, indem er den Roboterarm führt und mit dem Handgerät die Punkte speichert
- Ziel: Reduzierung des **Programmieraufwands**, geringerer Schulungsaufwand

### Offline-Programmierung

1. Abbilden der Roboterzelle in einem CAD-Programm (Herstellerdatenbank für Roboter, CAD-Modelle des Werkstücks und der Zelle)
1. Definieren der Bewegungen und des Prozessablaufs
1. Definieren der I/Os und der Parameter
1. **Simulation** auf Kollisionen, Erreichbarkeit, Taktzeiten, ...
1. Exportieren des Programms in die Robotersteuerung
1. Laden des Programms in die Robotersteuerung
1. Testen des Programms und ggf. Anpassen

#### Simulation

- **Erreichbarkeiten** und Kollisionen frühzeitig erkennen
- Singularitäten und Achsbeschränkungen erkennen
- Taktzeiten und Prozessabläufe optimieren

#### Wofür wird simuliert?

- Industrierobotik: Überwiegend Nutzung von in der Entwicklung bekannten geometrischen Eigenschaften
- Vorstudien: Machbarkeit, Erreichbarkeit, Taktzeiten, Kosten
- Grundlage für virtuelle Methoden bei der Entwicklung: Layoutplanung, **Offline-Programmierung**, Ableitung von Planungsunterlagen

#### Offline: Aufwandsbetrachtung Zeit

Ohne konkrete Randbedingungen nur schwer zu beantworten

- Anschaffung von **Softwarelizenzen**
- Eventuell Adaption der Software durch das Systemhaus
- Hardware: vergleichbar mit CAD-Arbeitsplatz
- Schulung eines am besten in 3D-Arbeiten vorgebildeten Mitarbeiters
- Zeitaufwand für die Datenkonvertierung
- Zeitaufwand für die **Offline-Programmierung**
- Zeitaufwand für das Nachteachen

#### Intuitive Programmierung

- Block-basierte **Programmierung**, Blöcke haben vorprogrammierte Funktionen
- Steuerungsablauf wird aus den Blöcken zusammengesetzt
- Vorteil: Einfache Programmierung, auch für ungeübte Anwender

### Sensorintegration ("Roboter lernen sehen")

- Sinn und Zweck: Anpassung des Prozesses an Toleranzen und Varianten
- Beispiele: Lageerkennung, Nahtverfolgung, Kraftsensoren, Qualitätskontrolle (Fehlerbilder)
- Programmierung: Viel komplexer, Problemquellen sind Schnittstellen, Programmablauf und Fehlerbehandlung

### Auswahl von Komponenten und Tools

| Kriterium | **Online-Programmierung** | **Offline-Programmierung** |
| --- | --- | --- |
| Soll die Anlage bereits im Vorfeld simuliert werden? | Nicht möglich | Ermöglicht die Optimierung der Anlage |
| Wechselt mein Produkt/Variante oft? | Häufiger Stillstand durch Programmieren | Höhere Produktivität |
| Verfügbarkeit von CAD-Daten | Nicht notwendig | Notwendig |
| Sind die CAD-Daten aus verschiedenen Quellen? |  | Erschwert die **Offline-Programmierung** |
| Wie hoch ist meine Zellenauslastung? | Bei geringer Auslastung stört die Blockierung durch Programmierung nicht | Höhere Zellenauslastung möglich |
| Hab ich qualifiziertes Personal? | eher praktische Erfahrung notwendig | theoretische und praktische Erfahrung notwendig |
