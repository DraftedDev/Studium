## Frühe Computer
Konrad Zuse: 1941 Z1, Z2 & **Z3** (erstes zuverlässiger, programmierter Computer)
Z3: 2600 Relais & 64 Speicherplätze mit je 22 bits
Plankalkül als erstes Sprachenkonzept von Zuse (ab 1945)
Z4 als erster kommerzieller Computer

Leibniz: 1674 Rechenmaschine mit Stafelwalze (Konzept Binärformat)

Charles Babbage: Analytical Engine Konzept 1838 mit Lochkartenplättchen

- Elektronische Röhrenrechner (ab ca. 1946)
    - ENIAC, >1000ops
- Transistorrechner (ab ca. 1955)
- Microchips mit hochintegrierten Schaltkreisen (ab ca. 1964)
    - IBM System/360, Taschenrechner Anfang 1970
- MOS-Technologie (ab ca. 1970)
    - Intel 4004
- Parallelverarbeitung, Vernetzung und KI (ab ca. 1981)
    - RISC, CISC, Transputer, …, GPU, NPU, …
## EVA & von Neumann
EVA-Prinzip: Eingabe, Verarbeitung, Ausgabe.
John von Neumann: Entwicklung 1940er Grundlagen für Rechenlagen.
- Rechner besteht aus:
	- Steuerwerk
	- Rechenwerk
	- Speicher
	- Ein-/Ausgabeeinheiten
	- Verbindungssystem
- Programm ist eine Kette logischer Binärentscheidungen (seriell)
- Programm abgelegt im gleichen Speicher wie Daten

![[Pasted image 20261008085727.png]]

## Mooresches Gesetz
- Nach Gordon Moore (Mitgründer von Intel)
- Etwa alle 18 Monate verdoppelt sich die Anzahl der Transitoren eines Mikroprozessors
    - (→ Legende um die Erfindung des Schachspiels)
- Entspricht grob Verdoppelung der CPU-Leistungsfähigkeit
- Bis 2030 gesichert
- Heute nur noch über Parallelisierung zu erreichen
    - Warum?
    - Aber: „Amdahls Gesetz“ begrenzt Parallelisierung
    - (Siehe: _Rechnerarchitekturen_)

## Einsatzgebiete der Informatik (S.31)
- Kommerzielle Rechner
    - Ein-/Ausgabe von großen Datenmengen
    - Einfache, interne Berechnungen
- Wissenschaftliche Rechner
    - Komplexe, langwierige Rechnungen
    - Wenig Ein-/Ausgabe
- Prozess-/Echtzeit-Rechner
    - Steuerung oder Überwachung
    - Physikalische, chemische oder technische Prozesse
    - Zeitaspekt
## Aufteilung Informatik

### Theoretische Informatik
- Automatentheorie und formale Sprachen
	- Abstrakte Maschinen
	- Theorie der Programmiersprachen
- Berechenbarkeitstheorie
	- Was kann berechnet werden, was nicht?
	- Halteproblem
	- Sind Rechenmodelle gleichwertig, z.B. math. Funktionen & Turing Maschine
	- (vgl. Diagonalverfahren von Cantor zur Nicht-Aufzählbarkeit der reellen Zahlen)
- Komplexitätstheorie
	- Zeitaufwand von Algorithmen, Speicheraufwand, Kommunikationsaufwand.
	- Trade-off (vgl. Mult.-Tabelle)
## Praktische Informatik
- Programmiersprachen, Compiler und Interpreter
- Algorithmen und Datenstrukturen
- Betriebssysteme
- Datenbanken
## Technische Informatik
- Mikroprozessortechnik
- Rechnerarchitektur
- Rechnerkommunikation
## Angewandte Informatik
- Wirtschaftliche, kommerzielle Anwendungen
    - Buchhaltung, Rechnungswesen
    - Büro-Software
- Technisch-wissenschaftliche Anwendungen
    - Simulationen
    - Steuerungen
## Interdisziplinäre Gebiete der Informatik (Auswahl)
- Künstliche Intelligenz
    - Selbständiges Lösen von Problemen; Lernen
    - Expertensysteme, Sensorik, Robotik, Mustererkennung
    - Verarbeitung natürlicher Sprache, → Computerlinguistik
- Computervisualistik
    - Bilderzeugung, -verarbeitung, -gestaltung
    - Auch: Computergrafik, Simulation, Visualisierung, Computerspiele
- Bioinformatik
    - Entschlüsselung Erbgut, Funktion lebender Zellen, Gen-Editing
    - DNA-Analyse, Visualisierung, Simulation
- Wirtschaftsinformatik
    - Planung, Entwicklung, Betrieb von Informationsverarbeitungssystemen für Geschäftsprozesse
## Modelle
- Modelle sind stets Modelle
- Abbildung, Repräsentation natürlicher oder künstlicher Orginale
- Die selbst wieder Modelle sein können
- Repräsentieren nur relevante Aspekte des Originals
## Funktion des Modells
- Logisches Modell
	- Original und Modell liegen als System von Zeichen vor
	- Nur der logische Inhalt von Interesse
- Erkenntnistheoretische Modellierung
	- Erkenntnisgewinn zu einem realen Original
	- Erfolgt durch Experimentieren, Simulieren, Prüfen & Analysieren
- Technische Modellierung
	- Modell & Original sind materiell-realer Natur
	- Durch möglichst vollständige Analogie wird Modell zum Ersatz für das Original
- Maschinelle "natürliche" Modelle
	- Modell ist ein Muster, das sich auf die Gestaltung des Originals auswirkt
### Klassifikation
- mathematisch-logisch
- immateriell
- materiell
    - ikonisch   
        - statisch
        - dynamisch
    - symbolisch
        - statisch / dynamisch
        - diskret / kontinuierlich
    - enaktiv
        - simulierend
        - registrierend
        - regelnd
        - autonom
### Darstellung
- Graphische Modelle
    - Meist zweidimensional
    - Aus dem Bereich des Wahrnehmens, Vorstellens und gedanklicher Operationen
    - Ikonisch = repräsentieren unmittelbar ihre Bedeutung
    - Symbolisch = Bedeutung / Code muss noch zugeordnet werden
- Technische Modelle
    - Meist dreidimensional, raum-zeitliche und materiell-energetisch
    - Pysiko-, bio-, psycho- und soziotechnische Modelle
- Semantische Modelle
    - Kommunikationssysteme, die ein Subjekt zur informationellen Verarbeitung seiner Wirklichkeit verwendet
    - Unterscheidung zwischen internen Modellen (Perzeption, Denken)
    - und externen Modellen (Zeichen, Zeichenkombinationen)
### Perspektive (Informatiksysteme)

Maschinenperspektive
- Maschinen sind nur von Experten zu durchschauen (Rechner, EVA, elektronisches Fließband)
Systemperspektive
- Benutzer und Computer werden als gleichwertig hinsichtlich der Informationsverarbeitung angesehen (Büro-Metapher)
Kommunikationsperspektive
- Benutzer und Computer werden als gleichberechtigte Sender und Empfänger angesehen (Dialogpartner, Hilfedialog)
Werkstattperspektive
- Gibt den Benutzern einen Expertenstatus (Werkzeug, Editor, Compiler, Debugger, Programmierumgebung)
Medienperspektive
- Computer ist lediglich ein Mittel für Koordinations- und Organisationsaufgaben (E-Mail, Wiki, SM)
### Architekturmodelle
- Theoretisches Maschinenmodell
	- Rechnerarchitekturen (SISD, MIMD, ...); Turingmaschine; Automatenmodelle
- Rechenmodell
	- Imperativ/prozedural; Funktional/applikativ; logisch/deklarativ; objektorientiert; zustandsorientiert
- Programmiermodell
	- Kommunikationsmodell; Kooperationsmodell
- Referenzmodell
	- OSI-Referenzmodell; Client/Server-Modell; Farbmodell
- Zeitmodell
### Entwurfsmodelle
- Systemmodell (Modellierungssprache)
- Aufgabenmodell
- Datenbankmodell: Rationales Datenmodell (Entity-Relationship-Modell)
- Objektmodell; Komponentenmodell
- Prozessmodell
- Zustandsmodell; Ereignismodell; Verhaltensmodell
### Untersuchungsmodelle
- Mathematisches Modell
- Analytisches Modell
- Simulationsmodell
### Mentale Modelle
- Konzeptuelles Modell
- Modellwelt
- Modellvorstellung
- Modellklasse: Schichtenmodell; Basismodell / Grundmodell
### Bildmodelle
- Bild, Abbild: Monitorbild; Holographie
- Teilschematische Abbildung: Piktogramm; Computerkunst
- Vollschematische Abbildung: CAD Darstellung
### Darstellungsmodelle (Symbolisch)
- Diagramm: Performance-Chart; Excel-Diagramm
- Darstellungsgraph: ER-Datenmodell; Suchbaum; Syntaxdiagramm.
- Flussdiagramm
    - Physikotechnisches Flussdiagramm: Zustandsdiagramm; Struktogramm
    - Organogramm: Datenflussdiagramm; Petri-Netz
    - Soziodiagramm: Interaktionsdiagramm; Kollaborationsdiagramm
- Schaltbild
    - Vollständiges Schaltbild: logische Schaltgitterpläne
    - Blockschaltbild: z.B. Von-Neumann-Architektur; Turingmaschine
### Technische Modelle
- Mechanische Modelle: Statische (z.B. Abakus); Dynamische (z.B. Rechenmaschine) Modelle
- Elektrotechnische Modelle: Elektromechanisch, Elektrotechnisch, Elektrochemisch
- Psychotechnische Modelle: Tele-Learning; Blended Learning
- Soziotechnische Modelle: Office-Modell; Mensch-Maschinen-Modell
- Biotechnische Modelle: DNA; Gedächtnischip