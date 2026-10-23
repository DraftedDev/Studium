# Natürliche Zahlen
## Dezimalsystem
Eine natürliche Zahl $\geq 0$ wird als Summe von Potenzen zur Basis $B_{dez} = 10$ dargestellt:

$z = a_{n} 10^n + a_{n-1} 10^{n - 1} + \dots + a_{1} 10 ^1 + a_{0} 10^0$
Dabei sind $a_{0}, a_{1}, a_{2}, \dots, a_{n} \in G_{dez} = \{0, 1, 2, 3, 4, 5, 6, 7, 8, 9\}$

## Dualsystem
- In digitalen DV-Anlagen muss alles durch die Zustände "an" und "aus" dargestellt werden.
- In DV-Anlagen können Dezimalzahlen als Dualzahlen/Binärzahlen dargestellt werden.
- Nun ist: $B_{bin} = 2\text{ und } G_{bin} = \{0, 1\}$

$z = a_{n}2^n + a_{n-1}2^{n-1} \dots a_{1}\cdot 2^1 + a_{0}\cdot 2^0$
Dabei sind $a_{0}, a_{1}, a_{n-1}, a_{n} \in G_{bin}$
Beispiel: $1101_{bin} = 1\cdot 2^3 + 1\cdot 2^2 + 0\cdot 2^1 + 1\cdot 2^0 = 8 + 4 + 0 + 1 = 13_{dez}$

## Dezimalzahl zu Dualzahl
Beispiel mit $1097$:
$$
1097 : 2 = 548 \text{ Rest } 1 \\
548 : 2 = 274 \text{ Rest } 0 \\
274 : 2 = 137 \text{ Rest } 0 \\
137 : 2 = 68 \text{ Rest } 1 \\
68 : 2 = 34 \text{ Rest } 0 \\
34 : 2 = 17 \text{ Rest } 0 \\
17 : 2 = 8 \text{ Rest } 1 \\
8 : 2 = 4 \text{ Rest } 0 \\
4 : 2 = 2 \text{ Rest } 0 \\
2 : 2 = 1 \text{ Rest } 0 \\
1 : 2 = 0 \text{ Rest } 1 \\ \\
1097_{bin} = 10001001001
$$
## Weitere Zahlensysteme

| **Dual** | **Oktal** | **Hexa** | **Dez** | **Dual** | **Oktal** | **Hexa** | **Dez** |
| -------- | --------- | -------- | ------- | -------- | --------- | -------- | ------- |
| *0000*   | 0         | 0        | 0       | *1000*   | 10        | 8        | 8       |
| *0001*   | 1         | 1        | 1       | *1001*   | 11        | 9        | 9       |
| *0010*   | 2         | 2        | 2       | *1010*   | 12        | A        | 10      |
| *0011*   | 3         | 3        | 3       | *1011*   | 13        | B        | 11      |
| *0100*   | 4         | 4        | 4       | *1100*   | 14        | C        | 12      |
| *0101*   | 5         | 5        | 5       | *1101*   | 15        | D        | 13      |
| *0110*   | 6         | 6        | 6       | *1110*   | 16        | E        | 14      |
| *0111*   | 7         | 7        | 7       | *1111*   | 17        | F        | 15      |

# Rationale Zahlen
## Dezimalbrüche
Natürliche Zahl $\geq 0: z = a_{n}10^n + a_{n-1}10^{n-1} + \dots + a_{1} 10^1 + a_{0} 10^0$
Erweiterung um Exponenten $< 0$ ergibt Dezimalbrüche.

$r = a_{n} 10^n + a_{n-1} 10^{n-1} + \dots + a_{1} 10^1 + a_{0} 10^0 + 10_{-1} + 10^{-1} + \dots + a_{-m} 10^{-m}$
$n = \text{Anzahl Vorkommastellen}$
$m = \text{Anzahl Nachkommastellen}$

Beispiel: $123,76 = 1\cdot 10^2 + 2\cdot 10^1 + 3\cdot 10^0 + 7\cdot 10^{-1} + 6\cdot 10^{-2}$
## Dualbrüche
$r = a_{n}2^n + a_{n-1} 2 ^{n-1} + \dots + a_{1} 2^1 + a_{0} 2^0 + a_{-1} 2^{-1} + \dots + a_{-m} 2^{-m}$

Beispiel: $11,01_{bin} = 1\cdot 2^1 + 1\cdot 2^0 + 0\cdot 2^{-1} + 1\cdot 2^{-2} = 2 + 1 + 0 + 0,25 = 3,25_{dez}$
## Dezimalzahl zu Dualbruch
$$
2 \cdot 0,6875 = 1,375 \quad R=1 \\
2 \cdot 0,375 = 0,75 \quad R=0 \\
2 \cdot 0,75 = 1,5 \quad R=1 \\
2 \cdot 0,5 = 1 \quad R=1 \\ \\
0,6875_{dez} = 0,1011_{bin}
$$
## Periodische Brüche
- Nicht alle Brüche lassen sich exakt darstellen.
- Rationale Zahl $\frac{p}{q}\text{ mit } ggT(p, q) = 1$, d.h. $p$ und $q$ sind teilerfremd.
- Wenn *alle* Primfaktoren von $q$ auch Primfaktoren der Basis sind => Exakte Darstellung möglich.
- Basis 10 => Primfaktoren $2$ und $5$: $1/3$, d.h. $q = 3$.
- Basis 2 => Primfaktoren $2$: $1/10$, d.h. $q = 10$ mit Primfaktoren $2$ und $5$.
## Konsequenzen
- Nicht jede rationale Zahl lässt sich auf einem IT-System exakt darstellen.
- *Reelle* Zahlen sowieso nicht.
- *Jeder Dualbruch* lässt sich als Dezimalbruch darstellen.
- *Nicht jeder Dezimalbruch* lässt sich als Dualbruch darstellen.
# Logische Operationen
## Aussagenlogik
- $\text{Wahr}=1;\text{ Falsch} = 0$
- $\land \text{ ("und")}$
	- $0 \land 0 = 0$
	- $0 \land 1 = 0$
	- $1 \land 0 = 0$
	- $1 \land 1 = 1$
- $\lor\text{ ("oder")}$
	- $0 \lor 0 = 0$
	- $0 \lor 1 = 1$
	- $1 \lor 0 = 1$
	- $1 \lor 1 = 1$
- $\lnot\text{ ("not")}$
	- $\lnot 0 = 1$
	- $\lnot 1 = 0$
- $\overline{\land}\text{ ("nand")} \to \lnot (a \land b)$
- $\overline{\lor}\text{ ("nor")} \to \lnot (a \neq b)$
- Insgesamt 16 logische Operationen.
## Binäres Rechnen
### Addition & Subtraktion
- *Addition* von zwei Binärziffern:
	- $0 + 0 = 0$
	- $0 + 1 = 1$
	- $1 + 0 = 1$
	- $1 + 1 = 0; \text{ Übertrag } 1$
- *Subtraktion* von zwei Binärziffern:
	- $0 - 0 = 0$
	- $0 - 1 = 1;\text{ Übertrag } -1$
	- $1 - 0 = 1$
	- $1 - 1 = 0$
- Bis auf Übertrag, identisch zu XOR.
- Lässt sich einfach auf Dualbrüche erweitern.
## Multiplikation & Division
- *Multiplikation* von zwei Binärziffern:
	- $0\cdot 0=0$
	- $0\cdot 1=0$
	- $1\cdot 0=0$
	- $1\cdot 1=1$
- Identisch zu AND.
- Mehrstellig: Wie im 10er-System:
![[Pasted image 20261021160046.png]]
## Schiebeoperationen
- Erhöhung/Verringern des Exponenten in der Bruchdarstellung.
	- $\text{SL }1010 = 10100$
	- $\text{SR }1010 = 101; \text{ SR }1001 = 100,1$
# Ganze Zahlen
## Negative Zahlen
- Negative Zahlen haben Sign-Bit.
- Problem: Es gibt $0$ und $-0$.
### Sign-Bit an erster Stelle
- Problem: Wo ist die erste Stelle?
- Lösung: Binärzahlen mit definierter Länge.
	- Üblich: 64 (aktuell); 32; 16; 8.
- Problem: Dualbrüche.
- Problem: $5 = 000101; -5 = 100101 \implies 000101 + 100101 = 101010 = -10$
### Sign-Bit an letzter Stelle
- Beispiel: $5_{dez} = 1010; -5_{dez} = 1011$.
- Problem: $5 + (-5) = 1010 + 1011 = 10101 = -10$
- Problem: Wo ist die letzte Stelle bei Dualbrüchen?
## Komplementdarstellung
- Binärzahl definierter Länge.
- Erstes Bit gibt Vorzeichen an.
- Negative Zahl => restliche Bits werden invertiert.
- Beispiel: $5 = 000101; -5 = 11101010$
	- Problem: $5 + (-5) = 111111 = -0$
	- Problem: $3 + (-2) = 0$ aber $2 + (-3) = -1$
## Zweierkomplement
- Wie Komplement, aber nach dem Invertieren wird die Zahl um eins erhöht.
- Beispiel: $5 = 000101; -5 = 111011$
	- $5 + (-5) = 000101 + 111011 = 000000 = 0$
	- $3 + (-2) = 000011 + 111110 = 000001 = 1$
- Es gibt nur eine $0$.
- Es gibt eine negative Zahl mehr als positive Zahlen:
	- $01111111 = 127$
	- $10000001 = -127$
	- $10000000 = -128$
### Rechnen im Zweierkomplement
- Definition der Länge notwendig.
	- Bit erhalten Nummerierung über Exponenten.
- Addition & Subtraktion fast problemlos.
- Multiplikation & Division wie vorher, Vorzeichenbehandlung nötig.
- Schiebeoperationen nach rechts: Bits an erster Stelle muss erhalten bleiben.
- Schiebeoperationen nach links: Unproblematisch.
## Überlauf
- Beispiel: $127 + 1 = 01111111 + 00000001 = 10000000 = -128$
- *Ignorieren:*
	- Normalverhalten in vielen CPUs.
	- Explosion der Ariane 5.
	- Verwendung sicherer Bibliotheken.
- *CPU bricht Verarbeitung ab:*
	- Für kritische Anwendungen, spezieller CPU notwendig.
- *Spezialwert "Fehler":*
	- Idealerweise bei $10000000$.
	- Software muss Ergebnisse prüfen, um Fehlerort zu bestimmen.
# Darstellung von Dualbrüchen
$r = (a_{n} 2^0 + a_{n-1} 2^{-1} + \dots + a_{1} 2^{n+1} + a_{0} 2^{-n} + a_{-1} 2^{n-1} + \dots + a_{-m} 2^{-n-m})\cdot 2^n$
- Probleme: Ableger im Speicher.
	- $n = \text{Anzahl der Vorkommastellen}$
	- $m = \text{Anzahl der Nachkommastellen}$
- Definierte Länge: $n + m$ muss konstant sein.
## Halblogarithmische Darstellung
- Beispiel: $\text{Lichtgeschwindigkeit} = 299792458 \frac{m}{s} = 299792,458 \frac{km}{s}$
	- $2,99792458\cdot 105 \frac{km}{s} = 2,99792458\cdot 108 \frac{m}{s} = 2,99792458\cdot 1010 \frac{cm}{s}$
	- Genau eine Vorkommastelle, Rest Nachkomma, Skalierung über Exponenten.
- Rundungsfehler bleiben relativ klein, können aber absolut groß werden.
## Binäre Gleitkommazahlen
- Auch: *Floating Point Number*; *Gleitpunktzahlen*.
- Nach *IEEE754* genormt.
- $r = (-1)^v\cdot 1,m\cdot 2^e$
- Dabei ist $v$ das Vorzeichenbit; $1,m$ die binäre *Mantisse* und $e$ der Exponent.
- $v = 0 \implies (-1)^v = 1; v = 0 \implies (-1)^v = -1$
- $m$ ist Bitsequenz definierter Länge, interpretiert als Nachkommastellen.
- $e$ wird als positive Zahl $c$ ("Charakteristik") gespeichert, mit $e = c - B$.
	- $B$ ist ein konstanter Wert für die Verschiebung (*Bias*).
	- $c$ ist Bitsequenz definierter Länge.
- $m$ und $c$ besitzen definierter Länge (genannt $\#m$ und $\#c$).
- Der Rest sind Konstanten: $(-1), 2, B$.
- Nullwert bei $c = 0$ und $m = 0$ => $+0$ und $-0$.
- Wenn $c = 0$, aber $m > 0$, gibt es alternative Darstellungen:
	- "denormalisierte Gleitkommazahlen" => "Unterlauf".
- Wenn $c = 2^B-1$:
	- $m = 0; r = \pm \infty$
	- $m > 0; r = NaN$
![[Pasted image 20261015105051.png|445]]
## Rechnen mit Gleitkommazahlen
- **Addition und Subtraktion**
	- Zuerst Charakteristik angleichen, durch Schiebeoperation; Dabei können Stellen verloren gehen.
	- Mantissen addieren bzw. subtrahieren.
- **Multiplikation**
	- Exponenten addieren.
	- Mantissen multiplizieren.
- **Division**
	- Exponent ergibt sich aus Differenz der Exponenten von Dividend und Divisor.
	- Mantissen dividieren.
- Nach jeder Operation muss Mantisse evtl. normalisiert und das Ergebnis auf Überlauf/Unterlauf geprüft werden.
- *Assoziativ-* und *Distributivgesetze* gelten nicht uneingeschränkt.
