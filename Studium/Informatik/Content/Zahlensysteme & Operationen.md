# Ganze Zahlen
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
