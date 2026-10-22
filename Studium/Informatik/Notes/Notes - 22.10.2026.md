# Nachrichten & Kodierung
## Nachricht
Eine Nachricht kann als Folge von Zeichen aufgefasst werden, die von einem Sender in irgendeiner Form einen Empfänger übertragen werden.
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
- 