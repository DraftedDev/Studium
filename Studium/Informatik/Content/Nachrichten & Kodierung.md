# Definitionen
## Definition Nachricht
**=> Eine Nachricht ist eine Folge von Zeichen, die von einem Sender in irgendeiner Form an einen Empfänger übertragen werden.**
- Zeichen stammen immer aus einem *Alphabet*.
- Zeichenfolge ist *abzählbar*, aber *nicht immer endlich*.
- Dadurch können Zeichen identifiziert werden.
# *TODO: Bild aus Notes in Mermaid*
## Definition Alphabet
Besteht aus:
- Einer *abzählbaren* Menge von Zeichen.
- Einer *Ordnungsrelation* der Zeichen.
- Menge ist oft *endlich*, kann aber auch *unendlich* sein.
- Ordnungsrelation definiert Reihenfolge der Zeichen.
# Nachrichtenraum
-  *Menge* aller Nachrichten, die mit den Zeichen eines *Alphabets* $A$ gebildet werden können, heißt $\text{Nachrichtenraum } N(A)$ über $A$.
- Wird auch als $A^*$ dargestellt.
- Betrachtet man nur Nachrichten einer *maximalen Länge* $s$, wird der Nachrichtenraum als $A_{s}$ dargestellt.
# Information
Sender *übersetzt* Information in Nachricht
=> Empfänger muss Information aus empfangener Nachricht *extrahieren*.
=> Setzt eine *Zuordnung* von Informationen voraus: *Interpretation*.
## Interpretation
- Keine Abbildung im mathematischen Sinne.
- *Nicht* unbedingt *eindeutig*.
- Subjektiv und abhängig vom *Kontext*:
- *Interpretationsvorschrift* muss nicht öffentlich sein.
## Informationsgehalt
- Statistisch in Bezug auf Nachricht aus $A^*$.
- *Informationstheorie* nach *Shannon*:
	- Je *seltener* ein Zeichen $x$ auftritt, desto *größer* soll sein Informationsgehalt sein:
		- $P(x)=\text{Eintrittswahrscheinlichkeit}$
		- $I(x) = \text{Informationsgehalt} = \frac{1}{P(x)}$
		- $P(x_{1},x_{2}) = P(x_{1}) \cdot P(x_{2}) \land I(x_{1},x_{2}) = I(x_{1}) + I(x_{2})$ *???*
		- $P(x)=1 \implies I(x)=0$
		- $I(x)$ wird nur als Logarithmusfunktion erfüllt.
		- $I(x)=\log_{b}\left( \frac{1}{P(x)} \right) = -\log_{b}(P(x))$
### Informationsgehalt in binären Systemen
- $A = {0, 1} \to b = 2$
- $I(x) = -\log_{b}(P(x)) = -\log_{2}(P(x)) = -ld(P(x))$ *???*
- Angenommen $P(x_{1})=P(x_{2})$ für alle $x_{1},x_{2} \in A^s$
	- $P(x) = 1 : 2^s$
	- $I(x) = -ld(1 : 2^s)$