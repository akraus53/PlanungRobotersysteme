## 4.3 Werkstücklokalisierung durch 3D-Bildverarbeitung

### Problemstellung

- Heutzutage mehr Varianten und kürzere Produktionszyklen bei kleineren Losgrößen
- Reduktion der Abhängigkeit von Vorrichtungen für größere Flexibilität: Ein **Roboter-Arm** kann immer gleich bleiben, auch wenn das Werkstück wechselt. Eine Vorrichtung müsste für jedes Werkstück neu angepasst werden.
- Optische Werkstücklokalisierung: Anpassung an unterschiedliche Werkstücke durch **Softwarekonfiguration**, kürzere Rüstzeiten
- Werkstücklokalisierung ist die Bestimmung der Lage einzelner Werkstücke in einem Raum. Sowohl die Position als auch die Orientierung des Werkstücks sind relevant.
- Sie ist eine Voraussetzung für die Vereinzelung, lagerichtige Zuführung, Palettierung und Montage von Werkstücken.
- Bei der Handhabung ist die **Geschwindigkeit** wichtiger, be Montage und Bearbeitung die **Genauigkeit**. In allen Fällen ist die **Zuverlässigkeit** sehr wichtig.

### 3D-Sensorik

| Sensor | Stereovision | Laufzeit 2D | Laufzeit 3D | Lasertriangulation | Punktuell messende Systeme |
| --- | --- | --- | --- | --- | --- |
| 2D/3D | 3D | 2D | 3D | 2D |  |
| Hinweise | Sichtbare Strukturen nötig (oder projizierte Muster) | **Linienscanner** | **Time-of-Flight** | meist Laserlinie | **Marker** oder Messeinheit nötig |
| Geschwindigkeit | **schnell** | **schnell** | ok | ok | **langsam** |
| Genauigkeit | **hoch** | **niedrig** | ok | **hoch** | **sehr hoch** |
| Robustheit | ok | ok | **hoch** | **hoch** | **hoch** |
| Sichtbarkeit | **gut** | **gut** | **gut** | **gut** | **gut** |

### Lokalisierungsverfahren

#### Objektbasiert

- Verwendung einer vollständigen **3D-Geometrie** des Werkstücks
- Beinhaltet Kanten, Kurven, Flächen und Volumen

#### Ansichtenbasiert

- Generierung einer **Ansichtendatenbank**, in dieser wird dann nach der gegebenen Ansicht gesucht
- Beinhaltet Formen, Merkmale, Strukturen
- Redundante Ansichten können entfernt werden, trotzdem großer Speicherbedarf
- Rechenzeit vs. Rotationsauflösung: Je mehr Ansichten, desto genauer, aber auch **langsamer**

#### Datengetrieben mit KI

- Funktionsweise: **CNN** (Convolutional Neural Network)
- Automatisches Einlernen über ein **CAD-Modell**
- Lagebestimmung durch heuristische (nicht-deterministische) modellbasierte Suche in Punktwolke und Modell
- Greifpunkt kann manuell oder automatisch bestimmt werden
- Kolliosionsvermeidung durch Greifpunktbestimmung
- Lernen kann durch **Simulationen** und echte Daten erfolgen

### Integration in Robotersysteme

- Typischerweise wird die Sensorik von einem **externen Rechner** ausgewertet. Das ist flexibel, erfordert aber zusätzliche Schnittstellen
- Eine Integration in die Robotersteuerung ist auch möglich, das wird momentan aber nur für **2D** angewandt

#### Auge-Hand-Kalibrierung

- Bestimmung der Transformation zwischen Kamera und Roboter
- Ziel: Korrektur von Fehlern der Sensorik und des Roboters
- Verwendet meist ein **Kalibrierungsmuster/-körper**

### Hürden bei der Umsetzung

- Sensorik: Transparenzen, Glanz, Reflexionen, Schatten
- Lokalisierung: Biegeschlaffheit, bewegliche Teile (Scharniere)
- Handhabung: Verhaken/Verklemmen (Trennungsstrategie?)
- Sensorbasierte Lokalisierung für Roboter führen zu Aneinanderreihung vieler **Einzeltoleranzen**
- Ursachenfindung bei Ungenauigkeiten ist schwierig $\rightarrow$ **Komponententests**

### Umsetzungsbeispiele

- Griff in die Kiste
- Lokalisierung von Waren in der Logistik
- Bearbeitung von Werkstücken