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
