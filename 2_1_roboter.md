## 2.1 Überblick und Industrieroboter

### Roboterkinematiken

| Kinematik | Serielle Roboter |  |  | Parallele und andere Roboter |
| --- | --- | --- | --- | --- |
| Bauform | Knickarm | SCARA | Portal | Delta, Seilroboter |
| Marktanteil | **66%** | 19% | 10 % | 1% |
| Vorteile | Zugänglichkeit, Beweglichkeit, Traglast |  | Sehr große Reichweite und Nutzlast | Hohe Steifigkeit, Genauikeit, Dynamik |
| Nachteile | Mäßige abs. Genauigkeit | eingeschränkte Beweglichkeit, kleiner Arbeitsraum, kleine Traglast |  |  |
| Typische Prozesse | Schweißen, Kleben, handling | Montage, Pick&Place | Pick&Place, Regalbedienung, Kommissionierung | Pick&Place, Sonderaufgaben |
| DOF | 5-6 | 3-4 | 3 | 3-6 |
| Form des Arbeitsraums | Kugel | Zylinder | Quader | Komplex |
| Radius des Arbeitsraums | 0.5-3m | 0.5-1m | 0.1-100m | 0.1-10m |
| Traglast [kg] | 5-1000 | 0.5-5 | 0.5-X000 | 0.5-X000 |
| Dynamik | mittlere Geschw. und Beschl. | sehr große Geschw. und Beschl. | je kleiner, desto schneller | sehr große Geschw. und Beschl. |

### Einsatzbereiche

- **Handling (44%)**: Materialtransport, Palettieren, Entpalettieren, Verpacken, Sortieren
- **Welding (19%)**: Punktschweißen, Lichtbogenschweißen, Laserstrahlschweißen
- **Assembly (12%)**: Bauteilmontage, Endmontage, Schrauben, Nieten
- **Clean Room (6%)**: Reinraum, Lebensmittel, Pharma
- **Machining (2%)**: Fräsen, Bohren, Schleifen
- **Dispensing (2%)**: Kleben, Dichten, Lackieren

### Steuerungen

Die Steuerung besteht aus:

1. Energieversorgung
1. Motorcontroller der Achsen
1. Untergeordnete Steuerungen der Sensoren und Aktoren

- Die Robotersteuerung wird in der Regel vom Roboterhersteller bereitgestellt und erfolgt in einer einfachen, für den jeweiligen Hersteller spezifischen Programmiersprache.
- Steuerungen bieten in der Regel Schnittstellen zur Integration weiterer Sensoren und Aktoren und SPS an.
- Technologiepakete für spezielle Anwendungen (z.B. Schweißen, Lackieren) sind verfügbar.

### Leistungsdaten und Eigenschaften von Robotern

- Freiheitsgrade: Anzahl der unabhängigen Bewegungsmöglichkeiten des Roboters. Können linear oder rotatorisch sein.
- Singularitäten: Punkte im Arbeitsraum, an denen der Roboter seine Beweglichkeit verliert, z.B. wenn zwei Gelenke in einer Linie liegen.
- Arbeitsraum und Begrenzungen: Der Bereich, in dem der Roboter seine Aufgaben ausführen kann, und eventuelle Einschränkungen.
- Dynamik: Die Fähigkeit des Roboters, sich schnell und präzise zu bewegen.
- Traglast: Maximales Gewicht, das der Roboter tragen kann, an jedem Punkt im Arbeitsraum, wenn es direkt am Flansch befestigt ist.
- Genauigkeit: Maß für die Präzision, mit der der Roboter seine Aufgaben ausführt.
- Kollisionen: Situationen, in denen der Roboter mit anderen Objekten oder Hindernissen kollidieren kann.
- Steifigkeit: Reversible Verformung des Roboters unter Last.
- Kinematische Transformation: Umrechnung zwischen verschiedenen Koordinatensystemen des Roboters, speziell zwischen Gelenk- und Arbeitsraumkoordinaten.
- Kosten: Gesamtkosten für den Kauf, die Installation und den Betrieb des Roboters.

### Formen der Genauigkeit

- **Wiederholgenauigkeit** gibt an, wie genau eine Pose innerhalb von vielen Zyklen erreicht werden kann. Bei vielen Industrierobotern bis zu 0.05 mm.
- **Absolutgenauigkeit** gibt an, wie genau die Raumkoordinaten bezogen auf das Basissystem des Roboters erreicht werden; hier sind Industrieroboter vergleichsweise ungenau.
- **Bahngenauigkeit** gibt die Abweichung von der programmierten Bahn an.
- Die Genauigkeit ändert sich unter wechselnder Last aufgrund der relativ geringen Steifigkeit.
- Robotergenauigkeit kann nicht pauschal durch eine einzige Kenngröße beschrieben werden.
