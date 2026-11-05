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

=> „Lokales Netz“ bezieht sich nicht auf LAN oder WLAN der Sicherungsschicht. Es ist ein Begriff in der Sprache der Netzwerk- / Vermittlungsschicht und bezeichnet alle Netze der Sicherungsschicht.

## Datenpaket
- Nachricht mit beschränkter Länge.
	- Praxis: ca. 1500 Byte (wg. Ethernet), aber auch mehr (z.B. Glasfaser, Jumbo Frames).
- Enthält die eigentliche zu übermittelnde Nachricht.
- Enthält Informationen zu Sender- & Empfängeradressen.
- Enthält Verwaltungsdaten, z.B. wie lange es unterwegs ist.
- Netzwerkschicht teilt zu große Pakete auf und fasst zusammengehörige kleine Pakete zusammen.
## Ermittlung des Paketwegs
- Jeder Knoten besitzt eine Tabelle, auf der Ziele und mögliche Wege verzeichnet sind: *Routingtabelle*.
- *Arten von Tabelleneinträgen:*
	- *Direkt verbundene Netze:* alle Knoten im gleichen lokalen Netz.
	- *Statische Wege:* Vom Administrator vorgegeben, um bestimmte Wege zu erzwingen.
	- *Dynamisch ermittelte Wege:* Informationen über weiter entfernt liegende Knoten (-> Routingalgorithmen & Protokolle).
## Netzwerkschnittstelle
- Ein Knoten kann in mehr als einem lokalen Netz liegen.
	- Pro Netzwerk ein eigener Zugang.
	- Netzwerkadresse bezieht sich nicht auf Knoten, sondern die Netzwerkschnittstelle.
- Zwei Netzwerkschnittstellen können im gleichen lokalen Netz liegen.
	- Sinnvoll z.B. bei WAN: Zwei Computer sind durch unterschiedlich verlaufende Lichtwellenleiter verbunden.
## Routingalgorithmen
- Zur Ermittlung der Routingtabelle.
- Im "Backbone" besonders relevant.
	- "Backbone" verknüpft lokale Netze (und ist selbst ein lokales Netz).
	- Bei Internet-Providern, WAN, MAN (Metropolitan Area Network), große Unternehmensnetze.
- Datenpaket hat Feld "Time To Live".
- Beispielalgorithmen:
	- Flooding/Broadcasting, Hot Potato.
	- Backward Learning.
	- Link-State Routing.
## Netzwerkschicht im Internet
- Internet Protocol (IP).
- Adressen:
	- IPv4: 32 Bit, d.h. $2^{32} \approx 4.3 \cdot 10^9$ Adressen.
	- IPv6: 128 Bit, d.h. $2^{128} \approx 3.4 \cdot 10^{38}$ Adressen.
	- Routing über Teiladressen.
- Spezielle Adressen, z.B. für eigener Rechner.
- Reservierte IPv4-Adressen für private Netze.
	- Z.B. 192.168.0.0 bis 192.168.255.255.
	- *Network Address Translation (NAT)* als Notlösung für IPv4.
- Adresszuweisung statisch oder dynamisch.
# Transportschicht
## Aufgabe
- Aufbau von logischen Verbindungen zwischen zwei Anwendungen.
- Datenpakete in einen Datenstrom umwandeln -> Paketreihenfolge.
	- ggf. verlorene Pakete nachsenden, doppelt empfangene Pakete ignorieren.
- Sicherstellung der Dienstgüte (*Quality of Service*).
	- Angleichung: Sende- und Empfangsraten.
- "End-zu-End" zwischen zwei Anwendungen.
## Logische Verbindungen
- Werden zur Sicherstellung der Dienstgüte benötigt.
    - Kommunikationspartner „verabreden“ benötigte Qualität
- Einer der Partner initiiert Verbindungsaufbau.
- Der andere Partner wartet auf Wünsche zum Verbindungsaufbau.
- Eigene Adresse benötigt, da abhängig von der Anwendung.
    - Nicht vom Computer, nicht von der Netzwerkschnittstelle.
## Verbindungsaufbau
- Wichtig: Datenpakete können verloren gehen.
- Ablauf (*Three Way Handshake*)
    1. A sendet B Datenpaket mit Aufbauwunsch.
    2. B sendet A Bestätigung des Wunsches.
    3. A sendet B Quittung.
- Was kann passieren?
    - Erstes Paket geht verloren → A wartet und wiederholt.
    - Zweites Paket geht verloren → A wartet und wiederholt, B ignoriert und bestätigt erneut.
    - Drittes Paket geht verloren → B wartet und wiederholt, A ignoriert dies.
- Weitere Herausforderungen.
	- C sendet Pakete im Namen von A oder B -> Sequenznummern.
	- A ist "böse" und antwortet nach dem ersten Paket nicht mehr -> SYN Floodin.
- Verbesserung: Mit dem dritten Paket kann A schon Daten senden.
![[Pasted image 20261105110013.png|363]]
## Paketreihenfolge
- Routing (Netzwerkschichten) kann bewirken, dass Datenpakete in unterschiedlicher Reihenfolge ankommen.
- Jedes Paket bekommt Sequenznummer.
## Doppelte Pakete
- Empfänger merkt sich, welche Sequenznummern schon empfangen wurden.
- Trifft Paket mit empfangener Nummer ein → ignorieren.
- Ist nicht trivial umzusetzen, wenn Anzahl Nummern sehr begrenzt ist.
## Verlorene Pakete
- Fehlende Sequenznummer, wie bei falscher Reihenfolge.
- Es wird gewartet:
	- Nach Ablauf der Zeit, wird Paketverlust angenommen.
	- Schwierig: Wenn nach Ablauf der Zeit das Paket noch ankommt.
- Wie lange muss der Sender Pakete bereit halten?
- Lösung:
	- Empfänger sendet *Quittungen*.
	- "Bis zur Sequenznummer SEQ wurden alle Pakete empfangen".
	- Wenn Sender Quittung nicht innerhalb bestimmter Zeit empfangen hat, Wiederholung Datenpaket(e).
	- Wenn zu viele Quittungen fehlen → Annahme Stau in Route.
## Sende- VS. Empfangsrate
- Z.B. großer Server mit 10 GBit/s sendet an altes Mobiltelefon mit 100 KBit/s.
- Zwischenspeicher, um kleine Schwankungen auszugleichen.
	- Werden sowieso für Quittungen & Co benötigt.
- Lösung:
	- Empfänger teilt Sender mit, wie viele Datenpakete gesendet werden dürfen.
	- Wenn Datenpakete quittiert -> Datenpakete senden.
	- Zu Beginn wird eine Anzahl ausgehandelt (-> Verbindungsaufbau).
	- Später kann die Zahl durch Empfänger geändert werden.
- -> Sliding Windows.
## Transportschicht im Internet
- *Transmission Control Protocol (TCP):*
	- Anwendungen werden über Port adressiert (2 Byte).
	- Jede Verbindung wird über IP-Adressen und Port beider Partner identifiziert.
	- Eine Anwendung kann mehrere Ports nutzen.
- *User Datagram Protocol (UDP):*
	- De facto IP-Pakete mit Portnummern.
	- Für bestimmte Anwendungen sind Verbindungen überflüssig.
# Sitzungsschicht
## Aufgabe
- Synchronisation zwischen zwei Anwendungen.
	- Z.B. nach Abbruch der logischen Verbindung.
	- ... von Daten.
	- ... von internen Zuständen.
- Damit nach einem Abbruch nicht von vorne begonnen werden muss.
- Simplex, Halbduplex oder Vollduplex.
## Sitzungsschicht im Internet
- De facto nicht vorhanden.
- Muss von den Anwendungen selbst geregelt werden.
# Darstellungsschicht
## Aufgabe
- Kommunikationspartner können jeweils eigene Datencodierung verwenden.
	- Wichtig bei heterogenen Systemen.
- Datenkompression & Verschlüsselung.
- -> Kommunikationspartner "verstehen" sich auf syntaktischer Ebene.
## Darstellungsschicht im Internet
- De facto nicht vorhandne.
- Muss von den Anwendungen selbst geregelt werden.
- Verschlüsselung auf Ebene TCP (Transportschicht):
	- SSL (veraltet) oder TLS.
	- Programmierschnittstelle (fast) gleich wie TCP.
# Anwendungsschicht
## Aufgabe
- Unterstützt Anwendungen bei ihren Aufgaben.
- Beispiele:
	- Authentifizierung, Autorisierung.
	- Ausführung von Operationen auf anderen Computern.
	- Koordination von Opera