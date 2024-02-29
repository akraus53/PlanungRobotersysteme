## 4.1 Toolkits, Plattformen und Integrationen zur Steuerung und Sensorintegration

- Komplexe Roboteranlagen benötigen vielfältige Integration von Sensorik,Komponenten und Algorithmen
- Hohe Wiederverwendbarkeit von Entwicklungen senkt mittelfristig Entwicklungskosten
- Entwicklung von wiederverwendbaren Komponenten erzeugt allerdings zusätzlichen Aufwand
- Middlewares werden für die Integration benötigt und helfen auf wettbewerbsrelevante Entwicklungen zu fokussieren
- Umstellung auf und Einstieg in neue Middlewares kostet Zeit und Energie

### Motivation zum Einsatz von Middleware in der Robotik

- Vereinfachung der SW Integration
- Wiederverwendbarkeit der SW Module
- Vereinheitlichung der Modul-kommunikation und Prozessausführung
- Herstellerunabhängigkeit ermöglicht die Nutzung und Kombination von am Markt verfügbaren Technologien
- Fokus auf wettbewerbsrelevante Entwicklung
- Verteilte Rechnersysteme Kommunikation über Rechnergrenzen hinweg
  - Heterogene Rechner
  - Bedienung, Ferndiagnose/-wartung

Vielfältige Vernetzung, Informationsaustausch, Eigenständige Anlagen und Informationsspeicherung ermöglichen die Vision: Dezentrale Selbstorganisation in Echtzeit in der Industrie 4.0

### In der Robotik verbreitete Toolkits

- ROS (Robot Operating System): Flexibles Framework für Robotersoftware-Entwicklung, erleichtert Kommunikation und Koordination.
- OPC UA (Open Platform Communications Unified Architecture): Offener Standard für industrielle Automatisierung, ermöglicht nahtlose Integration, sichere Kommunikation.
- OpenCV (Open Source Computer Vision Library): Open-Source-Bibliothek für Computer Vision, unterstützt Objekterkennung, Tracking und Bildanalyse.
- OpenRAVE (Open Robotics Automation Virtual Environment): Open-Source-Plattform für Robotersystem-Simulation und -Planung, fördert Bewegungsablaufentwicklung.
- TensorFlow (Open Source Machine Learning Framework): Framework für maschinelles Lernen, in der Robotik für Bilderkennung, Sprachverarbeitung und Bewegungssteuerung verwendet.

### Open Source Software

**Motivation:** Nutzung standardisierter Schnittstellen und Protokolle, Anbieter-Unabhängigkeit, Wiederverwendbarkeit/Anpassbarkeit, Kosteneinsparung

| Aspekt | Vorteil | Nachteil |
| --- | --- | --- |
| Verfügbarkeit des Codes | Quellcode verfügbar | Ggf. keine ausreichende Dokumentation |
| Verfügbarkeit des Frameworks | Fokussierung auf wettbewerbsrelevante Entwicklung | Festlegung auf und Abhängigkeit von Framework |
| Lock-in | Keine Anbieterabhängigkeit | Keine Haftung oder Gewährleistung |
| Kosten | Keine Lizenzkosten | Lizenz muss eingehalten werden |
| Anpassbarkeit | Quellcode kann angepasst werden | Ggf. muss Änderung freigegeben werden |
| Kommerzielle Services | Ggf. Teil des Finanzierungsmodells | Fehlende Service-Level-Agreements |
| Community | Ggf. starke, aktive Community | Keinen rechtl. Anspruch auf Support |

### Übersicht Softwarelizenzen

- Copyleft besagt, dass abgeleitete Werke unter der gleichen Lizenz veröffentlicht werden müssen. Permissive Lizenzen erlauben die Verwendung des Codes in abgeleiteten Werken, ohne dass diese unter der gleichen Lizenz veröffentlicht werden müssen.

- Copyright besagt, dass der Urheber des Codes das Recht hat, die Verwendung und Verbreitung des Codes zu kontrollieren. Open Source Lizenzen erlauben die Verwendung und Verbreitung des Codes unter bestimmten Bedingungen, die in der Lizenz festgelegt sind.
