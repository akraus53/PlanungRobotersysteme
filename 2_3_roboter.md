## 2.3 Parallele Roboter und Seilroboter

### Eigenschaften

- Leichtbau durch optimale Belastung: Statt Biegung/Torsion nur Zug/Druck.
- **Geringe Masse, hohe Dynamik**
- **Kleinerer Arbeitsraum aber große Traglast**
- **Parallele Roboter sind steifer und genauer als serielle Roboter**
- Die Kinematik ist komplexer, da die Position von mehreren Gelenken gleichzeitig abhängt.

### Bauarten und Antriebe

| Antriebsart | Drehgelenk | Schubgelenk | Linearschlitten | Seilwinde |
| --- | --- | --- | --- | --- |
| Bauart | **Delta-Roboter** | **Stewart-Plattform** | **Hexaglide** | **Seilroboter** |
| Beschreibung | 3-4 Beine mit "Kniegelenken" | Plattform auf 6 Beinen | wie Delta-3D-Drucker | Ein Seil in jede Ecke des Raums |
| Steuerungstechnik | elektrischer Antrieb mit großer Übersetzung | elektrischer oder hydraulischer Antrieb | Antrieb über Lineardirektantrieb der Kugelgewindetrieb, Stab rein passiv | Elektrischer Antrieb, einfache Umsetzung mit Standardkomponenten |
| **Eigenschaften** | räumlich/flächig paralleler Roboter mit 3-4 Beinen + opt. Zusatzachse | vollbewegliche Plattform | 3/6 Linearantriebe auf 3 Schienen | TCP hängt an 4/8 Seilen, die die Position klar bestimmen |
| **Vorteile** | **hohe Dynamik, Struktur ist passiv** | **hohe Steifigkeit, Nutzlast und Genauigkeit, aber beschränkte Rotation** | **geringe Emissionen im Bauraum** | **Simpler Maschinenbau, Krantechnik aufrüstbar** |
| **Branchen** | Lebensmittel, Pharma, Elektronik | hochbelastete oder hochgenaue Aufgaben, Bewegungssimulatoren | Handling | Handling, SpiderCam, Hochregallager |

### Entwicklung paralleler Roboter

#### Anforderungen aus Applikation

- Translatorischer Arbeitsraum
- Rotatorischer Arbeitsraum
- Bauraum und Störkonturen
- Freiheitsgrade
- Traglast
- Dynamik

#### Relevante Kriterien für die Roboterauslegung

- Eigenkollisionen
- Singularitäten
- Hub der Aktoren
- Antriebsdimensionierung
- Seile unter Spannung

#### Steuerungstechnik

- Benutzerspezifische kinematische Transformationen
- Echtzeitfähigkeit

### Ausblick

- Leistungssteigerung zu erwarten
  - Dynamik
  - Arbeitsraumgröße
  - Genauigkeit
- Leistungsfähige Steuerungstechnik ermöglicht den Betrieb komplexer Kinematiken
- Energie- und Ressourceneffizienz
