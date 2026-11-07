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
- 