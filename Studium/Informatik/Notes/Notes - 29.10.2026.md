# Rechnerarchitektur
## Ebenen
- Physikalische Umsetzung: Silikon; Wafer.
- Digitale Schaltung: Transistoren; Kondensatoren; Schaltwerke.
- Mikroarchitektur: Rechenwerk; Steuerwerk; Register.
- Befehlssatz: CISC; RISC; armv7; i386; i686.
- CPU: CPU-Kerne; Cache; Bus.
- Computer: Speicher; I/O; GPU.
- Cluster: Netzwerke.
## Von Neumann Architektur
### Steuerwerk
- Zentrale Kontrolle über CPU.
- Liest Befehle nacheinander aus dem Speicher und interpretiert diese.
- Sprungbefehle u.ä. werden direkt ausgeführt.
- Ebenso Adressberechnungen für Lesen nächster Befehlen.
- Ansonsten Delegation an Rechenwerk bzw. I/O-Einheiten.
### Rechenwerk
- ALU - Arithmetic Logic Unit
- Führt arithmetische und logische Berechnungen durch.
- Zwei Eingangsregister, ein Ausgangsregister und ein Statusregister.
- Meist: Akkumulator als Register für einen Operanden und das Ergebnis.
- Ein-Address-Maschine: Ein Akkumulator (implizit), häufiges Zwischenspeichern nötig.
- Zwei-Address-Maschine: Viele Akkumulatoren.
- Drei-Address-Maschine: Eingang und Aufgang beliebig.
### Speicherwerk
- Enthält Befehle in Maschinensprache.
- Dauerhaft gespeicherte Befehle werden im ROM abgelegt.
	- EEPROM - Electrically Erasable Programmable Read Only Memory.
- Daten meist im RAM (Random Access Memory).
	- Manche Daten auch im EEPROM.
- Daten und Befehle werden gleich behandelt.
	- Befehle können im RAM abgelegt werden.
### Ein- und Ausgabeeinheiten
- Datenaustausch und Peripheriegeräte.
	- Tastatur, Maus.
	- Display, Drucker.
	- Externe Speicher: "Festplatten", Magnetbänder.
	- Netzwerk.
- Meist: langsam.
- Häufig: eigener Prozess, der per DMA auf Speicherwerk zugreift.
![[Pasted image 20261029092440.png|460]]
## Operationsprinzip
Kleinste Dateneinheit ist ein _Wort_, ein beliebiges Bitmuster definierter Länge. Ein Wort kann folgendes kodieren:
- Einen Maschinenbefehl.
- Ein Datum / Wert zum Verarbeiten.
- Die Adresse eines Speicherplatzes.
Dem Wort kann nicht angesehen werden, welche Bedeutung es hat → abhängig vom Zustand der Maschine.
## Befehlsbearbeitung
![[Pasted image 20261029092606.png|493]]
## Beobachtung
- Gemeinsamer Speicher für Daten und Programm.
- Daten sind Programme sind Daten.
- Programme sind durch andere Programme änderbar.
- Programme und Daten werden über die gleichen Verbindungen übertragen.
- Serielle Abarbeitung.
## Harvard-Architektur
![[Pasted image 20261029092733.png|600]]
# Desktop-Architektur
![[Pasted image 20261029095219.png|570]]
## CPU
- Häufig "amd64", d.h. Intel 4004 -> 8008 -> 8080 -> 8086 -> 80386 -> AMD Operation
	- Intel Core i3, i5, i7, i9 (Gen 14); AMD Ryzen.
	- Ether CISC, etwas RISC.
	- Wintel.
- Aufstrebend: "ARM": "Acorn RISC Machines" -> "Advanced RISC Machines".
	- Apple M1-M6; Qualcomm.
	- RISC.
	- Keine eigene Fertigung, nur Lizenzen und IP-Cores.
## CPU (2)
- Taktraten 1-6 GHz.
	- Ab ca. 3 GHz steigt Stromverbrauch signifikant an.
- Unterschiedliche CPU-Kerne.
	- Performance-Kerne.
	- Effizienz-Kerne.
- Co-Rechenkerne für "KI-Anwendungen".
## Hauptspeicher
- DDR-SDRAM ("Double Data Rate Synchronous Dynamic Random Access Memory).
	- DDR3, DDR4, DDR5.
- Meist 8-32 GiB.
- Latenzzeit DDR5 typisch 30ns.
## Grafikkarte
- Einfache Berechnungen, massiv parallel.
	- Beispiel: Jedes Pixel auf dem Bildschirm eine Stelle verschieben.
	- Auch: Training neuronaler Netze.
- Eigener Grafikchip: Graphics Processing Unit (GPU).
- Hoher Stromverbrauch.
- Teilweise mit CPU auf einen Chip integriert.
- NVIDIA, AMD.
## Sekundärspeicher
- Festplatte, SSD.
- Wg. Durchsatzmaximierung direkt angeschlossen (SATA, PCIe, ...).
	- DMA (Direct Memory Access).
- Große Festplatte: > 4 TB, Latenz ca 2-5 ms, Durchsatz: 150 MB/s, Preis 25€/TB -> 50€/TB.
- Große SSD: 512 GB - 4 TB, Latenz ca. 250 us, Durchsatz 500 MB/s, Preis 70€/TB -> 150€/TB.
## Sonstige Peripherie
- Maus, Tastatur, Monitor, Mikrofon, Kamera, Scanner, Audio, LAN, WLAN.
- Häufig USB ("Universal Serial Bus"):
	- USB 3.2: Durchsatz 20 GiBit/s = 667 MB/s.
	- USB 4 vereinigt USB 3.2 mit Thunderbold 3.
- HDMI, DIsplayPort für Monitor.
- Thunderbolt für Monitor und externen Sekundärspeicher.
- LAN: Durchsatz 1-10 GiBit/s.
- WLAN: Durchsatz 100 MiBit/s - 2400 MiBit/s.
## Klassifikation nach Flynn
### Single Instruction Single Data
- Jeweils ein Befehls- und Datenstrom.
- Von Neumann Architektur.
- Verbesserungen:
	- 64 Bit Wortbreite, d.h. Verarbeitung von 8 Byte pro Befehl.
	- Pipelining: Aufteilung von Befehlen, die mit Hilfe eines Fließbands ausgeführt werden.
	- Skalar (mit Pipelining): pro Takt einen Befehl starten.
	- Super-Skalar: Mehr als einen Befehl pro Takt starten und ausführen.
- Probleme: Insbesondere bedingte Sprünge leeren die Pipeline.
### Single Instruction Multiple Data
- Ein Befehlsstrom.
- Viele Datenströme, auf denen Befehle gleichzeitig angewendet werden.
- Array- und Vektorrechner.
- Grafikprozessoren.
### Multiple Instruction Single Data
- Nur für Spezialstanwendungen.
- Datum wird x-Mal gelesen, die Kopien jeweils anders bearbeitet und zum Schluss zu einem Ergebnis zusammengefügt.
- Datum eher klein: binärlogische Operationen → direkt in Hardware realisieren.
- Datum eher sehr groß (z.B. Suche) → passen selten in CPU.
- Merksatz: „MISD ist meistens Mist, aber nicht immer“.
### Multiple Instruction Multiple Data
- Viele Datenströme werden durch viele Befehlsströme verarbeitet.
- (Hardseitiges) Multithreading:
    - Thread = Faden = Befehlsstrom.
    - Mehrere Steuer- und Rechenwerksteile in einem CPU-Kern.
    - Teilen sich ggf. aufwendige Rechenwerke, z.B. Gleitkommaberechung.
- Multi-Core Architekturen, d.h. eine CPU besteht aus mehreren CPU-Kernen.
- Theoretisch auch Computer-Cluster.
    - In der Praxis haben diese nicht ein gemeinsames Betriebssystem, sondern auf dem Computer eine autonome Kopie.
### Parallelität in einer CPU
#### Pipelining
- Aktivitäten / Takte zur Ausführung von Befehlen (RISC):
    1. Befehl aus dem Speicher holen, Befehlszähler erhöhen.
    2. Befehl dekodieren, relevante Operanden laden.
    3. Befehl ausführen.
    4. Speicherzugriff (Lesen oder Schreiben).
    5. Ergebnis in Register schreiben, ggf. in Hauptspeicher.
- Ohne Pipeline: 5 Takte pro Befehl.
- Mit Pipeline: Ein Befehl pro Takt (ideal).
- Probleme:
	- 