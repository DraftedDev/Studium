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
### Operationsprinzip
Kleinste Dateneinheit ist ein _Wort_, ein beliebiges Bitmuster definierter Länge. Ein Wort kann folgendes kodieren:
- Einen Maschinenbefehl.
- Ein Datum / Wert zum Verarbeiten.
- Die Adresse eines Speicherplatzes.
Dem Wort kann nicht angesehen werden, welche Bedeutung es hat → abhängig vom Zustand der Maschine.
### Befehlsbearbeitung
![[Pasted image 20261029092606.png|493]]
### Beobachtung
- Gemeinsamer Speicher für Daten und Programm.
- Daten sind Programme sind Daten.
- Programme sind durch andere Programme änderbar.
- Programme und Daten werden über die gleichen Verbindungen übertragen.
- Serielle Abarbeitung.
### Harvard-Architektur
![[Pasted image 20261029092733.png|600]]
