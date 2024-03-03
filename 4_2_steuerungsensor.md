## 4.2 Beherrschung von Toleranzen in der Robotik

### Potenziale und Einsatzgrenzen

- **Handling (44%)**: Greifgenauigkeit bestimmt Prozessgenauigkeit des darauffolgenden Prozesses
- **Welding (19%)**: Ungenauigkeiten führen zu hohen Nachprogrammierzeiten
- **Assembly (12%)**: Eher geringe Anforderungen an Genauigkeit
- **Clean Room (6%)**: Hohe Anforderungen an Genauigkeit
- **Machining (2%)**: Prozesskräfte am Endeffektor führen zu Genauigkeitsverlust
- **Dispensing (2%)**: Hohe Anforderungen an Bahngenauigkeit

### Ursprung von Toleranzen

- **Umgebung**: Aufspannung, Anregung, Temperatur
- **Mechanik**: Spiel, Nachgiebigkeit, Schwerkraft
- **Signalverarbeitung**: Kinematik, Bahnplanung und -führung
- **Prozess**: Durchbiegung, dynamische Effekte

### Fehlerausgleichsstrategien

- **Ausgangspunkt**: Standard-Industrieroboter (Wiederholgenauigkeit) $\rightarrow$ 0,8 mm
- **Intrinsische Korrektur**:
  - Modellbasierte DH-Parameter-Kompensation (DH = Denavit-Hartenberg) $\rightarrow$ 0,5 mm
  - Zusätzliche Achsencoder $\rightarrow$ 0,3 mm
- **Extrinsische Korrektur**:
  - Motion Tracking $\rightarrow$ 0,1 mm

### Genauigkeitsdefinitionen

- **Wiederholgenauigkeit**: Abweichung des Endeffektors bei mehrmaliger Anfahrt desselben Punktes (Relevant für Teach-in, Online-Programmierung)
- **Absolutgenauigkeit**: Abweichung des Endeffektors bei Anfahrt eines Punktes (= Koordinaten, Relevant bei Offline-Programmierung)
- **Bahngenauigkeit**: Abweichung des Endeffektors bei Bahnfahrt (Relevant bei Schweißen, Kleben, Lackieren). Typischerweise 1-5 mm Abweichung.
- **Porengenauigkeit**: Abweichung des Endeffektors bei Anfahrt eines Punktes (Relevant bei Positioniergenauigkeit, z.B. bei Montage)

### Verbesserungsmöglichkeiten

- **Hardware:** Ressourceneinsatz, Hardwareanpassungen sind zeit- und kostenintensiv. Wiederverwendbarkeit nicht gegeben.
- **Software:** Ressourcenfrei reproduzierbar, Flexibilität, algorithmische Verbesserungen, Robustheit durch Selbstadaptation. Leistungsgrenze durch Antriebe und Sensoren begrenzt.

$\rightarrow$ Da Code sehr günstig ist, kann eine große Verbesserung der Genauigkeit bei geringem Investitionsaufwand erreicht werden.

### Vorgehensweise zur Kalibrierung von Robotern

1. Mathematisches **Robotermodell**
1. Auswahl der wichtigsten Modellparameter
1. Auswahl der **Messposen** (Ziel: gute numerische Kondition/Rauschunterdrückung, einfacher Messaufbau)
1. Anfahren der verschiedenen Roboterposen
1. **Messgrößenerfassung**
1. Berechnung der zugehörigen Modellwerte
1. **Parameteridentifikation** durch Minimierung der Fehlerfunktion
1. **Anpassung** der Parameter in der Steuerung

### Modellierungsansätze von Toleranzen

- **Parametrisches physikalisches Modell**/White-Box-Modell: Modellierung der kinematischen und dynamischen Eigenschaften des Roboters. Hoher Modellierungsaufwand, Beschränkung auf die wesentlichen Parameter.
- **Generisches mathematisches Modell**/Black-Box-Modell: Modellierung der kinematischen und dynamischen Eigenschaften des Roboters. Hoher Rechenaufwand, komplexes Ein-/Ausgangsverhalten.
- **Hybride Modellierung**/Grey-Box-Modell: Kombination aus parametrischem und generischem Modell. Kann zum Beispiel durch Kombination von kinematischer Berechnung und neuronalem Netzwerk realisiert werden.

$\rightarrow$ Modellierung kann entweder durch Vorwissen oder durch Messungen erfolgen. Je weniger man vom einen hat, desto mehr muss man vom anderen haben.

### Bewertungskriterien für die Auswahl von System-Komponenten

- **Sensorik**: Auflösung, Rauschen, Messfrequenz, Verfügbarkeit, Kosten
- **Modell**: Genauigkeit, Rechenzeit, Robustheit, Anpassbarkeit
- **Steuerung**: Echtzeitfähigkeit, Open-Source/Closed-Source, Schnittstellen, Toolchains, Benutzerdefinierte Kinematiken

### Messwerterfassung durch Sensorik

- **Lasertracker**: Lasertracker, bis 150 m Entfernung, 0,02 mm Auflösung, 1000 Messpunkte/Sekunde, SDK für Softwareintegration, präzise Vermessung von Robotern und Anlagen, Reflektoren erforderlich, optionale 6D Posenmessung.
- **Indoor GPS**: Lokalisierungssystem, beliebiges Messvolumen. Alle Komponenten in einem Referenzsystem. Online-Kompensation
- **Laser-Scanner**: Unterschiedliche Genauigkeiten, Messpunktwolken. Echtzeitreferenzierung von mobilen Robotern, Objektlagenerkennung
- **Mechanische und optische Messtaster**: Arbeitsbereich bis 15cm, Auflösung bis 1 $\mathrm{\mu m}$. Für parametrische Modelle wie serielle Kinematiken, Online-Kompensation möglich.
- **Interne Sensorik**: Direkte und indirekte Messung, Online-Kompensation, Automatische Kalibrierung. Günstig, da bereits vorhanden.

### Zusammenfassung

- Die meisten Roboter sind ohne Weiteres ungenau
- Differenzierung zwischen Absolut, Wiederhol-, Posen- und Bahngenauigkeit
- Auswahl geeigneter Hardware, z.B. für Sensoren
- Flexibilität durch Ressourceneffizienz: Hardware durch den Einsatz leistungsfähiger Software an die Grenzen der Leistungsfähigkeit zu bringen
- Kalibrierung und Referenzieren sind wesentliche Bausteine für die Erreichung der geforderten Leistungsdaten
