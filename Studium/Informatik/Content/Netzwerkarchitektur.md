# Übertragungsmedium
- *Kabelgebunden:* Seriell, parallel, Bus, Punkt-zu-Punkt.
- *Funk:* WLAN, Bluetooth, NFC, Telefonie.
- *Licht:* Glasfaser, Infrarot.
- Ton oder physischer Transport von Daten.
# Charakteristiken
- Datenvolumen, Bandbreite, Übertragungsrate, Latenz.
- Echtzeit, Synchron, Asynchron, Reichweite.
- *Simplex* (Einweg), *Halbduplex* (Mehrweg, aber nicht gleichzeitig), *Vollduplex* (Mehrweg, gleichzeitig), *Dual Simplex* (zwei Simplex Leitungen).
# Begriffe
## Rechnernetz
=> Ein Rechnernetz ist eine *Menge von Knoten*, die jeweils über *ein oder mehrere Übertragungsmedium* kommunizieren können.
## Übertragungsmedium & Kanal
- Medium enthält einen oder mehrere Kanäle.
- Pro Kanal können *unabhängige* Nachrichten übertragen werden.
- *Multiplexing:* Nutzung eines Kanals durch mehrere Teilnehmer.
- Kanal besitzt Übertragungsrate (Bit/s).
## Übertragungsrate VS Bandbreite
- *Bandbreite* kommt aus analoger Signalverarbeitung.
	- Wird häufig in Hz gemessen.
- *Übertragungsrate* meist übertragene Daten in Bits/s.
## Reichweite & Latenz
- Signale werden mit zunehmender Entfernung schwächer => Störungen nehmen zu.
- Lichtgeschwindigkeit begrenzt Nachrichten: Benötigen *Mindestlaufzeit*.
- Zwischenknoten *verzögern* Mindestlaufzeiten.
- *Laufzeit* äquivalent zu *Latenz*.
## Protokoll
- Regelung der Kommunikation:
	- Wer darf wann was wie senden?
	- Wer muss wann wie auf eine empfange Nachricht reagieren?
=> Ein Kommunikationsprotokoll ist eine Menge von *Regeln*, welche die *Syntax*, die *Semantik*, die *Pragmatik* und die *Synchronisation* der Kommunikation bestimmt.
- *Syntax:* Beschreibt den Aufbau von Nachrichten.
- *Semantik:* Beschreibt die Bedeutung von Nachrichten.
- *Pragmatik:* Beschreibt die Einsatzszenarien von Nachrichten.
- *Synchronisation:* Beschreibt das zeitliche Verhalten bei der Übertragung von Nachrichten.
# ISO/OSI Referenzmodell
- Modell zur Datenkommunikation in offenen Systemen.
- *ISO-Norm 7498* für *Open System Interconnection* (OSI).
- *Ziel:* Kommunikation über unterschiedlichste technische Systeme hinweg zum beschreiben.
- Sieben logische Schichten:
	- Jede Schicht stellt *Dienste* für *bestimmte Aufgaben* zur Verfügung.
	- Schicht $N$ unterstützt Schicht $N+1$.
	- Schicht $N$ nutzt Schicht $N-1$.
- Nicht jede Schicht muss in jeder Anwendung verwendet werden.
## Schichten
1. *Physical Layer (Bitübertragungsschicht):* Codierung und Übermittlung von Bitströmen.
2. *Link Layer (Sicherungsschicht):* Steuerung Datenübertragung, Fehlererkennung.
3. *Network Layer (Netzwerkschicht):* Routing von Datenpaketen.
4. *Transport Layer (Transportschicht):* End-zu-End Steuerung.
5. *Session Layer (Sitzungsschicht):* (Prozess-) Synchronisation.
6. *Presentation Layer (Darstellungsschicht):* Übersetzung von Datenformaten.
7. *Application Layer (Anwendungsschicht):* allg. Dienste, Anwendungen, Netzwerkmanagement.
## Protokolle & Mehr
- Für jede Schicht wurden *eigene Protokolle* und sonstige Datenformate spezifiziert und standardisiert.
- Standardisierung durch *Internationale Fernmeldeunion* (ITU).
## Arpanet & Nachfolger
- *Separate Aktivität* für ein *dezentrales Computernetz* (ab 1968).
	- Advanced Research Projects Agency Network.
	- *Konzept:* Paketevermittlung, Routing.
- *Ab 1971:* E-Mail, Telnet, FTP, TCP.
- *1981:* Spezifikation von IPv4, ICMP (Management), TCP.
- Implementierung in UNIX/C.
- Nutzung an Hochschulen -> *Usenet*.
## ISO/OSI Modell Heute
- Modell hat sich *nicht* technisch durchgesetzt.
- TCP/IP war schon implementiert.
## Referenzmodell
- Nutzung als *Modell*, um andere Modelle zu vergleichen.
- Aufteilung in Schichten ist meist sinnvoll.
- Entkopplung von Komponenten (-> *Softwaretechnik*).
- Half, Internetprotokolle in die Welt der ITU zu integrieren.
	- Kommunikationsnetze auf *Schicht 1* gehören meist *Telekommunikationsunternehmen*.
## Bitübertragungsschicht
- Zugang zum Übertragungsmedium.
### Übertragungsmedium
- *Twisted Pair:* Zwei oder mehr verdrillte isolierte Kupferadern.
- *Koaxial Kabel:* Eine Ader in der Mittel, Isolator, leitende Abschirmung.
- *Lichtwellenleiter:* Glasfaser, Laserdiode als Sender, Photodiode als Empfänger.
- *Funk im freien Raum:* Signal wird auf Trägerfrequenz moduliert.
	- Amplitude-, Frequenz-, Phasenmodulation.
- Modulation funktioniert auch bei Twisted Pair und Koaxial Kabel.
### Leitungscodierung
- Wie soll $\{0,1\}$ über eine Leitung übertragen werden.
- *Idee:* 1 = High-Pegel = 3 V; 0 = Low Pegel = -3 V.

![[Pasted image 20261105100010.png|521]]
### Multiplexing
- Gemeinsamer Nutzung eines Übertragungsmedium.
	- *Raummultiplex:* (eigentlich Kanäle) -> MIMO bei WLAN.
	- *Zeitmultiplex:* Aufteilung in exklusive, disjunkte Zeitintervalle.
	- *Frequenzmultiplex:* Nutzung unterschiedlicher Frequenz.
	- *Codemultiplex:* Nutzung von Alphabet mit Länge $2^n$ statt Binärcode.
### Netztopologien
- Kanäle werden über *Knoten* zu *Netzen* zusammengeschalten.
- 