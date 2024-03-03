## 6.1 Zusammenfassungsvorlesung

### Roboterdefinition

- Nach ISO 8373: Ein Roboter ist ein programmierbarer Manipulator mit drei oder mehr Achsen für industrielle Anwendungen
- Roboter erzeugen automatisch eine durch ein Programm beschriebene Bewegung, so dass sich einmal festgelegte Abläufe ohne Personaleinsatz reproduzieren lassen
- Der Roboter ist eine universell einsetzbare Maschine, die für verschiedene Prozesse verwendet werden kann

### Roboterzelle

- Roboter (mechanische Struktur)
- End-Effektor (Greifer Oder Werkzeug)
- Steuerungstechnik (Roboter, Zelle, Sicherheit, Anbindung an übergeordnete Leittechnik)
- Sicherheitseinrichtung
- Zuführ-, Vereinzelungs-, Bereitstellungseinrichtungen
- Sensorik

### Grundlagen Roboter

| Kinematik | Serielle Roboter |  |  | Parallele und andere Roboter |
| --- | --- | --- | --- | --- |
| Bauform | Knickarm | SCARA | Portal | Delta, Seilroboter |
| Vorteile | Zugänglichkeit, Beweglichkeit, Traglast |  | Sehr große Reichweite und Nutzlast | Hohe Steifigkeit, Genauigkeit, Dynamik |
| Nachteile | Mäßige abs. Genauigkeit | eingeschränkte Beweglichkeit, kleiner Arbeitsraum, kleine Traglast |  |  |
| Typische Prozesse | Schweißen, Kleben, handling | Montage, Pick&Place | Pick&Place, Regalbedienung, Kommissionierung | Pick&Place, Sonderaufgaben |
| Traglast [kg] | 5-1000 | 0.5-5 | 0.5-X000 | 0.5-X000 |
| Dynamik | mittlere Geschw. und Beschl. | sehr große Geschw. und Beschl. | je kleiner, desto schneller | sehr große Geschw. und Beschl. |

### End-Effektoren

- Ein Endeffektor ist die Funktionseinheit eines Robotersystems, die den zu automatisierenden Prozess bewirkt
- Der Prozess bestimmt den Endeffektor
- Ein Endeffektor ist das Bindeglied zwischen Roboter und Werkstück und ist am Flansch des Roboters angebracht
- Endeffektoren lassen sich einteilen in
  - Greifer
  - Werkzeuge
  - Mess- und Prüfmittel
- Die Entwicklung oder Auswahl von Greifern und Werkzeugen unterliegt vielen Einflussfaktoren
- Einfache Aufgaben: es existieren Komponenten und Baukästen. Immer ist mindestens die Auswahl und Integration notwendig.
- Komplexere Aufgaben: Oft Sonderanfertigung oder komplette Neuentwicklung

$\rightarrow$ Greifer und Werkzeuge sind Anpass- oder Sonderkonstruktionen

### Steuerungstechnik

- Die Steuerung beinhaltet die Überwachung, den Betrieb, die Kommunikation und die Bedienung des Robotersystems
- Sie baut auf auf den Anwender, den Roboter und den Prozess
- Die Steuerungstechnik einer Anlage muss vorab sorgsam geprüft werden
- Robotersteuerungen sind zum Betrieb einer einfachen Roboterzelle ausreichend
- Erweiterung um eine übergeordnete Soft-SPS erhöht Flexibilität und Größe der Zellensteuerung
- Erweiterung um Technologiepakete erlaubt die Beeinflussung der Roboterbewegung

### Programmierung

1. Abbilden der Roboterzelle in einem CAD-Programm (Herstellerdatenbank für Roboter, CAD-Modelle des Werkstücks und der Zelle)
1. Definieren der Bewegungen und des Prozessablaufs
1. Definieren der I/Os und der Parameter
1. Simulation auf Kollisionen, Erreichbarkeit, Taktzeiten, ...
1. Exportieren des Programms in die Robotersteuerung
1. Laden des Programms in die Robotersteuerung
1. Testen des Programms und ggf. Anpassen

### Toolkits und Software-Integration

- Komplexe Roboteranlagen benötigen vielfältige Integration von Sensorik. Komponenten und Algorithmen
- Hohe Wiederverwendbarkeit von Entwicklungen senkt mittelfristig Entwicklungskosten
- Entwicklung von Wiederverwendbaren Komponenten erzeugt allerdings zusätzlichen Aufwand
- Middlewares werden für die Integration benötigt und helfen auf wettbewerbsrelevante Entwicklungen zu fokussieren
- Umstellung auf und Einstieg in neue Middlewares kostet Zeit und Energie

### Kalibrierung von Robotern

1. Mathematisches **Robotermodell**
1. Auswahl der wichtigsten Modellparameter
1. Auswahl der **Messposen** (Ziel: gute numerische Kondition/Rauschunterdrückung, einfacher Messaufbau)
1. Anfahren der verschiedenen Roboterposen
1. **Messgrößenerfassung**
1. Berechnung der zugehörigen Modellwerte
1. **Parameteridentifikation** durch Minimierung der Fehlerfunktion
1. **Anpassung** der Parameter in der Steuerung

### Strukturierte Vorgehensweise beim Planen (VDI 2221)

1. Klären und präzisieren der Aufgabenstellung (liefert: Anforderungsliste)
1. Ermitteln von Funktionen und deren Strukturen (liefert: Funktionsstrukturen)
1. Suchen nach Lösungsprinzipien und deren Strukturen (liefert: prinzipielle Lösungen)
1. Gliedern in realisierbare Module (liefert: modulare Strukturen)
1. Gestalten der maßgebenden Module (liefert: Vorentwürfe)
1. Gestalten des gesamten Produkts (liefert: Gesamtentwurf)

### Sicherheit von Robotern

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
