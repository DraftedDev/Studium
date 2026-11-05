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
