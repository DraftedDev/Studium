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