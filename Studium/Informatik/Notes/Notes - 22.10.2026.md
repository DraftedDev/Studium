# Nachrichten & Kodierung
## Nachricht
Eine Nachricht kann als Folge von Zeichen aufgefasst werden, die von einem Sender in irgendeiner Form an einen Empfänger übertragen werden.
![[Pasted image 20261022083452.png]]
## Definition Nachricht
=> Eine _Nachricht_ ist eine aus den _Zeichen eines Alphabets_ gebildete Zeichenfolge.
- Zeichenfolge ist abzählbar, aber nicht notwendig endlich.
- Dadurch können Zeichen identifiziert werden.
## Definition Alphabet
Ein Alphabet besteht aus:
- Einer abzählbaren Menge von Zeichen.
- Einer Ordnungsrelation der Zeichen.
- Menge ist oft endlich, kann aber auch unendlich sein.
- Ordnungsrelation definiert Reihenfolge der Zeichen.
## Nachrichtenraum
- Menge aller Nachrichten, die mit den Zeichen eines Alphabets $A$ gebildet werden können, heißt $\text{Nachrichtenraum } N(A)$ über $A$.
- Er wird auch als $A*$ dargestellt.
- Betrachtet man nur Nachrichten einer maximalen Länge $s$, wird der Nachrichtenraum als $A_{s}$ dargestellt.
## Information
Sender übersetzt Information in Nachricht, Empfänger muss die Information aus der empfangenen Nachricht extrahieren.
Das setzt eine Zuordnung von Nachricht und Information voraus: _Interpretation_.
## Interpretation
- Interpretation ist keine Abbildung im mathematischen Sinne.
- Sie ist nicht unbedingt eindeutig.
- Sie ist subjektiv und abhängig vom Kontext.
    - Beispiel: Nachricht „Raupe“
    - Tier; Baumaschine; Fahrgeschäft auf Jahrmärkten; Gleiskette; Codewort
- Interpretationsvorschrift muss nicht öffentlich sein.
## Definition: Information
- „Information“ ist zu vielschichtig, kaum mathematisch in allen Facetten fassbar.
- Im Sinne der Informatik kein exakt definierbares abstraktes Objekt.
- Begriff „Informationsverarbeitung“ problematisch.
- „Nachrichtenverarbeitung“ korrekter.
- Wenn man Nachrichten mit „Daten“ identifiziert: „Datenverarbeitung“.
## Informationsgehalt
- Statistisch in Bezug auf Nachricht aus $A*$.
- "Entscheidungsinformation".
- Informationstheorie nach Shannon:
	- Je seltener ein Zeichen $x$ auftritt, desto größer soll sein Informationsgehalt sein.
		- $P(x) = \text{Eintrittswahrscheinlickeit}; I(x) = \text{Informationsgehalt} = \frac{1}{P(x)}$
		- $P(x_{1},x_{2}) = P(x_{1})\cdot P(x_{2}) \land I(x_{1},x_{2})=I(x_{1})+I(x_{2})$
		- $P(x)=1 \implies I(x)=0$
	- $I(x)$ wird nur als Logarithmusfunktion erfüllt.
	- $I(x)= \log_{b}\left( \frac{1}{P(x)} \right) = -\log_{b}(P(x))$
## Informationsgehalt in binären Systemen
![[Pasted image 20261022085559.png|527]]
## Informationsgehalt von Nachrichten
![[Pasted image 20261022085628.png]]
## Codierung
![[Pasted image 20261022085706.png]]
### Ziele
Angemessene Codierung:
- Möglichst wenig Zeichen.
- Unempfindlich gegenüber Störungen.
- Leicht zu verarbeiten.
## Wortlänge & Redundanz
![[Pasted image 20261022090919.png|446]]
## BCD-Codierung
- "Binary Coded Decimal".
- Die neun Ziffern werden in vier Bit umgewandelt.
- I/O einfacher, weniger Fehler -> finanzmathematische Anwendungen.
- Abwandlung: Stibitz-Code: BCD+3, Neunerkomplement durch invertieren.
![[Pasted image 20261022091138.png|319]]
Die Bitsequenzen 1010, 1011, 1100, 1101, 1110, 1111 werden nicht vergeben.
Beispiel BCD: $1097_{dez} = 0001000010010111_{bcd} = 1097_{hex}$
## ASCII
![[Pasted image 20261022091243.png|561]]
## Unicode
- Ziel: Darstellung aller relevanten Zeichen (inkl. ASCII).
- Wortlänge:
	- Version 1.0: ~7.100 Zeichen -> 16 Bit reichen.
	- Version 15.1: ~150.000 Zeichen -> Mehr als 16 Bit.
- Zweistufiger Code:
	- Jedes Zeichen erhält einen "Code Point", z.B. $A=65_{dez}; Ä=196_{dez}; ∈=8712_{dez}$
	- Code point wird gemäß einer eigenen Codierung in Bits/Bytes dargestellt.
	- UTF-8 (L=1-6, 4 genutzt), UTF-16 (L=1-2), UTF-32 (Wortlänge L=1), Punycode (für DNS-Namen, ASCII), ...
- Unicode codiert abstrakte Zeichen, nicht deren Darstellung ("Glyphen").
	- $Ä=A+^{..}$, aber $Ä=C4_{hex}, A=41_{hex}, ^{..}=308_{hex}$
## UTF-8
- Codiert Code points mittels Byte-Sequenz:
	- 0-127: Ein Byte, sieben Bit (Bit 7 = `0xxxxxxx`).
	- 128-2047: Zwei Byte, fünf+sechs Bit (`110xxxxxx 10xxxxxx`).
	- 2048-65535: Drei Byte, vier+sechs+sechs Bit (`1110xxxx 10xxxxxx 10xxxxxx`).
	- 65536-2097151: Vier Byte, drei+sechs+sechs+sechs Bit Bit (`11110xxx 10xxxxxx 10xxxxxx 10xxxxxx`).
- Eigenschaften:
	- Selbstsynchronisierend: ersten beiden Bits ansehen reicht (`0x = ASCII, 11 = Start+Anzahl, 10 = Rest`).
	- Fehlerkontrolle durch Anzahl-Bits nach 11.
	- Vergleich zweier codierter Code Points einfach zu realisieren.
	- Codiert bis zu $2^{31}$ Zeichen.
- Mittlere Wortlänge bei westlichen Texten gering.
- Beispiele: *siehe Beispiele Folie (Fehler eingeschlichen)*
![[Pasted image 20261022100639.png|454]]
**[UTF-8 is a Brilliant Design](https://iamvishnu.com/posts/utf8-is-brilliant-design)** studieren!!!
## Diskretisierung
### Problem
- Reale Welt kennt keine Nachricht im Sinne der Informatik.
- Mittels Sensoren können kontinuierliche, biologische Nachrichten erfassen.
	- Kontinuierlich = Zeichenfolge beliebiger Dichte -> Nachricht ist reelle Funktion.
	- Meist stetige Funktion, bzw. beschränkte Änderung.
- Muss in eine diskrete, d.h. abzählbare Form überführt werden.
- -> Form der Modellbildung
### Abtastung
- Sensorwerte werden zu bestimmten Stellen erfasst.
	- Stelle meist Zeitpunkt.
- Abtasttheorem von Shannon/Nyquist-Bedingung.
	- Wenn $\text{Abtastrate}>2\cdot\text{Grundfrequenz}$, dann lassen sich die Sensordaten exakt rekonstruieren.
![[Pasted image 20261022101250.png|506]]
### Quantisierung
- Sensorwerte sind ebenfalls reell, d.h. kontinuierlich.
- Umwandlung in diskrete Nachrichten führt zu Fehlern.
- In Rückwandlung ist dies als "Rauschen" erlebbar.
- Audio/Video: AD-Wandler mit 10,12 oder 16 Bit, jedes zusätzliche Bit verringert Rauschen um die Hälfte (d.h. ca. 6 dB).
- Technische Anwendungen meist 8 Bit.
### Komprimierung
- Ziel: Minimierung der mittleren Wortlänge.
	- D.h. Minimierung Redundanz.
	- Eindeutiges Decodieren.
	- Meist: Aufwand Decodierung $\ll$ Aufwand Kodierung.
- Variable Wortlänge -> Huffman Algorithmus.
- Beispiele:
	- Lauflängen-Codierung (Run-Length-Coding), z.B. Windows-Bitmap.
	- Differenz-Codierung, z.B. diskretisierte Audio-Signale.
	- LZW-Codierung, via Zeichenhäufigkeit im konkreten Dokument.
	- Via Fourier-Transformation (JPEG, MP3).
## Codesicherung
- Codierung mit expliziter Redundanz.
- Meist: Code zweier Zeichen sollen sich durch möglichst viele Bits unterscheiden.
- Auch: Zwei aufeinanderfolgende Zeichen sollen sich in möglichst wenig Bits unterscheiden.
### Hamming Distanz
- Hamming: Distanz h: minimale paarweise Bit Distanz.
	- h = 0: Nachrichten sind gleich ⊥
	- h = 1: keine sichernde Redundanz
	- h = 2: ein fehlerhaftes Bit kann erkannt werden
	- h = 3: ein fehlerhaftes Bit kann korrigiert werden, zwei fehlerhafte Bit werden erkannt
	- Allgemein: h-1 fehlerhafte Bits werden erkannt, (h-1)/2 fehlerhafte Bits können korrigiert werden
- Spezialfall: Parität
	- 7 Bit Daten, achtes Bit sorgt dafür, dass die Anzahl der 1er-Bits gerade / ungerade ist.
	- Grund für 7 Bit bei ASCII.
### Gray-Codes
- Einschrittige Codes, d.h. Änderung von einem Bit führt zu benachbarten Code.
- Verringert Fehlerauswirkung, gerade bei DA/AD-Wandlern.
![[Pasted image 20261022104624.png|228]]
### CRC-Codes
- Problem: Häufig sind viele Bits hintereinander fehlerhaft.
- Lösung 1: Bits der gesendeten Nachricht werden vor Kommunikation permutiert.
	- Wahrscheinlichkeit sinkt.
- Lösung 2: Zusätzliche Prüfsumme PR(N) der Nachricht N.
	- Grob: $N_{neu}=N++PR(N)$
	- Ggf. auch Prüfsummen alle n Bits.
- Grundlage: Primpolynome.
- Beispiele:
	- CRC8, CRC16, CRC32...
	- Bestimmte "Hash-Funktionen", wie SHA1, SHA256.
### Verschlüsselung
- Ziel: Jede Teilmenge der codierten Nachricht hat die gleiche Vorkommenswahrscheinlichkeit.
	- D.h. u.a. minimale Entropie.
	- Nicht vollständig lösbar.
- Es gibt eine Umkehrcodierung.
- Codierungs- und Decodierungsalgorithmus werden mittels separater Nachrichten gesteuert.
	- "Schlüsse".
#### Anforderungen
- Vertraulichkeit: Einem Unbefugten soll es nicht möglich sein, ausgetauschte Nachrichten zu entschlüsseln und mitzulesen.
- Integrität: Einem Unbefugten soll es nicht möglich sein, abgefangene Nachrichten zu verändern.
- Authentizität: Sender und Empfänger wollen die Gewissheit über die Identität des Kommunikationspartners haben.
- Schlüsselverwaltung: Die Art und Weise wie Schlüssel erzeugt, verwahrt, weitergegeben und wieder gelöscht werden, muss sicher sein.
# Fazit
- Nachrichten / Daten sind das zentrale Element der Informatik.
- Information ist ein vager Begriff, der mit Informationsgehalt, Entropie nur teilweise beschrieben werden kann.
- Eine Codierung ist eine spezielle Form von Nachrichtenmengen.
- Binäre Alphabete sind von speziellem Interesse, wenn es um Verarbeitung durch Computer geht.
- Neben anderen Codes lohnt sich das Studium von UTF-8.
- Codierung soll möglichst „klein“ sein, wenig fehleranfällig und leicht verarbeitbar.
- Analoge Signal müssen zu Computerverarbeitung in binäre Codierungen diskretisiert („digitalisiert“) werden.
- Bei der Diskretisierung gibt es Fehler durch Abtastung und Quantisierung.
- Codesicherung hilft, diese Fehler zu erkennen bzw. Auswirkungen zu verringern.
- Verschlüsselung ist Codierung, um Vertraulichkeit, Integrität und Authentizität von Nachrichten herzustellen.