# Übertragungsmedien
- Kabelgebunden: Seriell, parallel, Bus, Punkt-zu-Punkt.
- Funk: WLAN, Bluetooth, NFC, Telefonie.
- Licht: Glasfaser, Infrarot.
- Ton.
- Physischer Transport von Daten.
# Charakteristiken
- Datenvolumen, Bandbreite, Übertragungsrate, Latenz.
- Echtzeit, Synchron, Asynchron, Reichweite.
- Simplex, Halbduplex, Vollduplex, Dual Simplex.
# Begriffe
## Rechnernetz
=> Ein _Rechnernetz_ ist eine Menge von _Knoten_ (Teilnehmern), die jeweils über ein oder mehrere _Übertragungsmedien_ kommunizieren können.
![[Pasted image 20261105085522.png]]
## Übertragungsmedium & Kanal
- Hilfsmittel zur Übertragung von Nachrichten.
- Enthält einen oder mehrere Kanäle.
- Pro Kanal können unabhängig Nachrichten übertragen werden.
	- Beispiel: UKW-Radio mit vielen Sendern auf unterschiedlichen Funkfrequenzen.
- Multiplexing: Nutzung eines Kanals durch mehrere Teilnehmer.
- Kanal besitzt Übertragungsrate (Bit/s).
## Übertragungsrate VS Bandbreite
- Bandbreite kommt aus analoger Signalverarbeitung.
	- Wird häufig in Hz gemessen.
	- Beispiel: WLAN nutzt Frequenzen 2412 MHz - 2417 MHz -> Bandbreite 5 MHz.
- Übertragungsrate meist übertragene Daten in Bits/s.
## Reichweite & Latenz
- Signale werden mit zunehmender Entfernung schwächer, Störungen nehmen zu.
	- Nachrichten können irgendwann nicht mehr erkannt werden.
- Jedes Medium hat maximale Reichweite.
	- NFC: cm; Glasfaser: km.
- Lichtgeschwindigkeit ist endlich.
	- Nachrichten benötigen Mindestlaufzeiten.
- Zwischenknoten verzögern Nachrichten.
- Selbst bei Glasfaser oder Funk kann terrestrische Kommunikation dauern.
- Laufzeit = Latenz.
- Große Latenz: Kommunikation wird schwierig (z.B. Telefon, ab ca. 400 ms Latenz).
## Protokoll
- Kommunikation bedeutet Austausch muss geregelt werden.
- Dieser Austausch muss geregelt werden:
	- Wer darf wann was wie senden?
	- Wer muss wann wie auf eine empfangene Nachricht reagieren?
- *Ein Kommunikationsprotokoll ist eine Menge von Regeln, welche die Syntax, die Semantik, die Pragmatik und die Synchronisation der Kommunikation bestimmt.*
- Ein Netzwerkprotokoll ist ein Protokoll zur Kommunikation in Rechnernetzen.
- *Syntax* beschreibt den Aufbau von Nachrichten.
- *Semantik* beschreibt die Bedeutung von Nachrichten.
- *Pragmatik* beschreibt die Einsatzszenarien von Nachrichten.
- *Synchronisation* beschreibt das zeitliche Verhalten beim Übertragen von Nachrichten.
# ISO/OSI Referenzmodell
## Allgemeines
- Ein Modell zur Datenkommunikation in offenen Systemen.
- ISO-Norm 7498 für Open System Interconnection (OSI).
- *Ziel:* Kommunikation über unterschiedlichste technische Systeme hinweg zu beschreiben, inkl. Weiterentwicklung.
- Sieben logische Schichten ("Layer").
	- Jede Schicht stellt Dienste für bestimme Aufgaben zur Verfügung.
	- Unabhängig von anderen Schichten.
	- Schicht N unterstützt Schicht N+1.
	- Schicht N nutzt Schicht N-1.
- Nicht jede Schicht muss in jeder Kommunikationsanwendung verwendet werden.
## Schichten
1. *Physical Layer (Bitübertragunsschicht):* Codierung und Übermitteln von Bitströmen.
2. *Link Layer (Sicherungsschicht):* Steuerung Datenübertragung, Fehlererkennung.
3. *Network Layer (Netzwerkschicht):* Routing von Datenpaketen.
4. *Transport Layer (Transportschicht):* End-zu-End-Steuerung.
5. *Session Layer (Sitzungsschicht):* (Prozess-) Synchronisation.
6. *Presentation Layer (Darstellungsschicht):* Übersetzung von Datenformaten.
7. *Application Layer (Anwendungsschicht):* allg. Dienste, Anwendungen, Netzwerkmanagement.
## Protokolle & mehr
- Für jede Schicht wurden eigene Protokolle und sonstige Datenformate spezifiziert und standardisiert.
- Standardisierung durch Internationale Fernmeldeunion (ITU).
    - 1980er, teilweise 1990er.
    - knapp 200 Staaten, damals ca. 400 Organisationen (heute: ca. 1000).
    - Sehr offiziell (gegr. 1865, jetzt Teil UN): top → down.
## Arpanete & Nachfolger
- Separate Aktivität für ein dezentrales Computernetz (ab 1968).
	- Advanced Research Projects Agency Network.
	- Konzept der Paketvermittlung/Routin.
- Ab 1971: E-Mail, Telnet, FTP, TCP.
- 1981: Spezifikation von IPv4 ("Internet Protocol", Routing), ICMP (Management), TCP.
	- -> Integration Arpanet in "Internet".
- Implementierung in UNIX/C -> portabel.
- Nutzung an Hochschulen -> Usenet.
## ISO/OSI Modell Heute
- Modell hat sich nicht technisch durchgesetzt.
	- Es gibt Ausnahmen, z.B. ASN.1 aus Darstellungsschicht zur Kodierung von Zertifikaten.
- TCP/IP war schon implementiert, als Arbeit an OSI-Modell begonnen hat.
### Referenzmodell
- Nutzung als Modell, um andere Modelle zu vergleichen.
- Aufteilung in Schichten ist meist sinnvoll.
- Entkopplung vom Komponenten (-> Softwaretechnik).
- Half, Internetprotokolle in die Welt der ITU zu integrieren.
	- Kommunikationsnetze auf Schicht 1 (oder: 0) gehören meist Telekommunikationsunternehmen.
# Bitübertragunsschicht
## Aufgabe
- Zugang zum Übertragungsmedium.
![[Pasted image 20261105095427.png|472]]
## Übertragungsmedien
- *Twisted Pair:* zwei oder mehr verdrillte isolierte Kupferadern.
- *Koaxial-Kabel:* Eine Ader in der Mitte, Isolator, leitende Abschirmung.
- *Lichtwellenleiter:* Glasfaser, Laserdiode als Sender, Photodiode als Empfänger.
- *Funk im freien Raum:* Signal wird auf Trägerfrequenz moduliert.
	- Amplituden-, Frequenz-, Phasenmodulation.
- Modulation funktioniert auch bei Twisted Pair und Koaxial Kabel.
## Leitungscodierung
- Wie soll $\{0, 1\}^*$ über eine Leitung übertragen werden?
- *Idee:* 1 = High-Pegel = 3 V; 0 = Low Pegel = -3 V -> Im Mittel 0 V.
![[Pasted image 20261105100010.png|521]]
## Multiplexing
- Gemeinsame Nutzung eines Übertragungsmedium.
	- Beispiel: WLAN.
	- *Raummultiplex:* (eigentlich: Kanäle) -> MIMO bei WLAN.
	- *Zeitmultiplex:* Aufteilung in exklusive, disjunkte Zeitintervalle ("Zeitschlitze").
	- *Frequenzmultiplex:* Nutzung unterschiedlicher Frequenzen.
	- *Codemultiplex:* Nutzung von Alphabet mit Länge $2^n$ statt Binärcode.
## Netztopologien
- Kanäle werden über Knoten zu Netzen zusammengeschaltet.
- *Liniennetze* sind häufig Busse, Leitungsausfall problematisch.
- *Ringnetze* eher auf regionaler, globaler Ebene.
- *Stern- und Baumstruktur* besitzen zentrale Knoten (z.B. Home-Router).
- (Teil-) Vermaschte Netze für hohe Ausfallsicherheit.
- Achtung: physische vs logische Ebene.
![[Pasted image 20261105101117.png|543]]
# Sicherungsschicht
## Aufgabe
- Steuerung & Überwachung der Datenübertragung auf Abschnitten zwischen Knoten des Netzes.
- Knoten müssen sich gegenseitig direkt über ein Übertragungsmedium erreichen können.
- Wer darf auf das gemeinsame Übertragungsmedium zugreifen.
	- Opt. Teilschichten: *Media Access Control* (MAC) & *Link Control* (LLC).
- Erkennung von Übertragungsfehlern (-> Codesicherung).
- *Ziel:* Daten werden sicher zwischen zwei benachbarten Knoten übertragen.
- -> Abhängig von der Größe des Netzes, d.h. Knotenabstand.
## Nahbereich: PAN & WPAN
- (Wireless) Personal Area Network.
	- Z.B. Peripheriegeräte mit Smartphone oder Laptop verbinden.
- Bluetooth: bis 10 m, preiswerte Hardware, geringer Stromverbrauch, Multimediadaten, Master-Slave.
- Bluetooth Low Energy (BLE): 40–200 m, geringerer Stromverbrauch, 1–2 MBit/s, sporadische Kommunikation.
- RFID (Radio Frequency Identification): sendet nur eine Identifikation (Ursprung) Freund/Feind-Erkennung), Heute: Strom per Magnetfeld.
- NFC (Near Field Communication): 10 cm, bis ca. 400 KiBit/s, Strom per Magnetfeld.
## Lokaler Bereich: LAN & WLAN
- (Wireless) Local Area Network.
- *Ethernet:*
	- Datenpakete mit 64 bis ca. 1500 Byte.
	- Ursprünglich Bussystem mit 10 MBit/s und Koaxial-Kabel.
	- Heute: > 10 GBit/s und Twisted Pair in Stern Topologie (meistens Switch, sonst Hub).
- *WLAN / WiFi:*
	- Datenfunk, Frequenzband 2.6 GHz, 5 GHz, 6 GHz.
	- Access Point (AP) ist ein spezieller Router.
	- Kommunikation verschlüsselt.
## Zugriff auf gemeinsame Medien
- „Man muss sich absprechen, wer wann kommunizieren darf. Dazu müsste man kommunizieren können.“.
- CSMA-Verfahren: *Carrier Sense, Multiple Access*.
### CSMA/CD
- Collision Detection.
- CS = Hören, ob Medium frei ist.
- CD = Wenn Medien frei -> aber zugleich hören.
- Kollisionserkennung wenn andere / ungültige Daten gelesen werden.
- Nur Vollduplex.
### CSMA/CA
- Collision Avoidance.
- CS = Hören, ob Medium frei ist.
- CA = Wenn Medium frei -> Zufallszeit warten, hören -> Senden.
- Funk meistens Halbduplex.
## Regionalbereich: Internetzugang
- Viele Technologien, häufig historisch gewachsen.
- Analoge Telefonverbindung (Audiomodulation, 56.6 KBit/s); ISDN (128 KBit/s -> 2 MBit/s).
- *DSL (Digital Subscriber Line):* Telefonleitung mit 1-35 MHz Bandbreite -> Splitter.
- *Kabelanschluss:* grob DSL über Fernsehkabel.
- *Glasfaser:* Backbone-Technologie "to the Home".
- *Mobil:* 2G, 3G, LTE (4G), 5G.
	- 2G grob Analogtelefon.
	- Ab 3G IP-basiert: jeweils "geschicktes" Multiplexing.
	- Ab 5G mit Techniken von WLAN, z.B. MIMO.
- Satelliteninternet: Richtfunk.
- Gemeinsames Zugangsprotokoll: PPP "simuliert" Ethernet-Pakete mit MAC-Addressen.
## Global: WAN
- Wide-Area-Network.
- Meist: Glasfaserbündel, hochwertige Lichtwellenleiter.
- Oder: Geostationäre Satelliten, breitbandiger Richtfunk.
- Datenübertragungsraten > 1 TBit/s.
# Netzwerkschicht
## Aufgabe
- Übermitteln von Datenpaketen zwischen zwei beliebigen, indirekt verbundenen Knoten.
	- Überbrücken unterschiedlicher Transportmedium.
- Jedes Datenpaket kann eine eigene Route nehmen.
- Benachbarte Knoten müssen Informationen über möglichen Routen austauschen.
- "End-zu-End" zwischen Rechnerknoten.
- Auch: Vermittlungsschicht.
## Weitervermittlung
- Sicherungsschicht stellt Übertragung zwischen zwei Geräten in einem konkreten Medium sicher.
	- D.h. in einem lokalen Netz.
- Wie können Nachrichten zwischen mehreren Netzen übertragen werden.
	- "zwischen" - lat. "inter" -> Internet.
- *Lösungsansatz:*
	- Knoten bekommen global eindeutige Adressen.
	- Nachrichten werden in endliche Datenpakete aufgeteilt.
	- Pakete werden unabhängig in Richtung Zieladresse weitergeleitet.
- Paket soll einen Weg (Route) zum Ziel nehmen.
- Bestimmte Knoten können mehrere Adressen haben, wenn sie mit mehreren lokalen Netzen verbunden sind.