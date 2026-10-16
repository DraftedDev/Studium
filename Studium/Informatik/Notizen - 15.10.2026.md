# Zahlensysteme & Operationen
## Darstellung von Ganzen Zahlen
### Dezimalsystem
![[Pasted image 20261015083901.png]]
### Dualsystem
![[Pasted image 20261015083947.png]]
### Dezimalzahl => Dualzahl
![[Pasted image 20261015084239.png|193]]!
### Umwandlung in andere Zahlensysteme
![[Pasted image 20261015085817.png|252]]![[Pasted image 20261015085833.png|252]]
## Darstellung von rationalen Zahlen
### Dezimalbrüche
![[Pasted image 20261015091516.png|463]]
### Dualbrüche
![[Pasted image 20261015091549.png|484]]
### Umwandlung Dezimalbruch => Dualbruch
![[Pasted image 20261015092132.png]]
0,6875 => 0,1011
### Rationale Zahlen
- Lassen sich nicht durch endliche Brüche darstellen.
- Beispiel: 1 / 3 = 0.3333333...
- In einem endlichen Speicher lässt sich also nicht jede rationale Zahl ablegen
- Nach m Nachkommastellen wird abgeschnitten => Genauigkeitsverlust
- Beispiel m = 4: 1/3 = 0,3333, d.h. Genauigkeit 10-4
    - 0,3333 · 3 = 0,9999
    - Notlösung: Rundung, z.B. auf drei Nachkommastellen
### Umwandlung Dezimalbruch => Dualbruch
![[Pasted image 20261015092602.png|221]]
0,1 => 0,00011001100110011
### Periodische Brüche
- Nicht alle Brüche lassen sich exakt darstellen
- Rationale Zahl p/q (ggT(p, q) = 1, d.h. p und q sind teilerfremd
- Wenn _alle_ Primfaktoren von q auch Primfaktoren der Basis sind => exakte Darstellung
- Basis 10 => Primfaktoren 2 und 5: 1/3, d.h. q = 3
- Basis 2 => Primfaktor 2: 1/10, d.h. q = 10 mit Primfaktoren 2 und 5
### Konsequenzen
- Nicht jede rationale Zahl lässt sich auf einem IT-System exakt darstellen
- Reelle Zahlen sowieso nicht
- Jeder Dualbruch lässt sich als Dezimalbruch darstellen
- Viele Dezimalbrüche lassen sich nicht als Dualbruch darstellen
    - Kaufmännische Anwendungen problematisch, w.g. 1/10
## Logische Operationen
### Aussagenlogik
- Wahr = 1; Falsch = 0
- ∧ („und“), ∨ („oder“) und ¬ („nicht“)
- ∧ => **AND**|0 AND 0 = 0|0 AND 1 = 0|1 AND 0 = 0|1 AND 1 = 1|
- ∨ => **OR**|0 OR 0 = 0|0 OR 1 = 1|1 OR 0 = 1|1 OR 1 = 1|
- ¬ => **NOT**|NOT 0 = 1|NOT 1 = 0|---
Beispiel: 1100 AND 0101 = 0100; 1100 OR 0101 = 1101; NOT 1100 = 0011
### Weitere Operationen
- Mittels AND, OR und NOT lassen sich alle weiteren logischen Operationen durchführen
- AND und OR lassen sich nicht gut mit Transistorschaltkreisen in CPUs realisieren
    - Beim Schalten eines Transistors erfolgt immer eine Invertierung
- a NAND b = NOT (a AND b)
- a NOR b = NOT (a OR b)
- a XOR b = NOT (a = b)
- Insgesamt 16 logische Operationen.
### Binäres Rechnen
#### Addition & Subtraktion
- Addition von zwei Binärziffern
    - 0 + 0 = 0
    - 0 + 1 = 1
    - 1 + 0 = 1
    - 1 + 1 = 0, Übertrag 1
- Subtraktion von zwei Binärziffern
    - 0 - 0 = 0
    - 0 - 1 = 1, Übertrag -1
    - 1 - 0 = 1
    - 1 - 1 = 0
- Bis auf Übertrag identisch zu XOR
- Lässt sich einfach auf Dualbrüche erweitern
#### Multiplikation & Division
- Rechenregeln für zwei Binärziffern
    - 0 · 0 = 0
    - 0 · 1 = 0
    - 1 · 0 = 0
    - 1 · 1 = 1
- Identisch zu AND
- Mehrstellig: wie im 10er-System
![[Pasted image 20261015100805.png|136]]
10000010 = 130 = 10 · 13
- Division erfolgt analog zur Division im 10er-System
#### Schiebeoperationen
- Teil von Algorithmen zur Multiplikation und Division
- Erhöhen / Verringern des Exponenten in der Bruchdarstellung
- Beispiel:
    - SL 1010 = 10100
    - SR 1010 = 101, SR 1001 = 100,1
- (Analog 10er-System)
## Darstellung ganzer Zahlen
### Negative Zahlen
- Bisher können keine Zahlen < 0 dargestellt werden
- Ansatz: 1 Bit für das Vorzeichen
#### Sign-Bit an erster Stelle
- Problem 1: wo ist die erste Stelle?
- Lösung: Binärzahlen mit definierter Länge
    - Üblich: 64 (aktuell), 32, 16, 8
    - Größte Zahl: 263 (aktuell), 231, 215, 27
    - Problem 1a: Dualbrüche
- Beispiel, Länge 6: 5 = 000101; -5 = 100101
    - Problem 2: 5 + (-5) = 000101 + 100101 = 101010 = -10
#### Sign-Bit an letzter Stelle
- Beispiel 5dez = 1010; -5dez = 1011
- Problem 1: 5 + (-5) = 1010 + 1011 = 10101 = -10
- Problem 2: Wo ist die letzte Stelle bei Dualbrüchen?

Weiteres Problem: es gibt eine zusätzliche Zahl „-0“ (1, bzw. 10000)
### Komplementdarstellung
- Binärzahl definierter Länge
- Erstes Bit gibt Vorzeichen an
- Negative Zahl => restliche Bits werden invertiert
- Beispiel (Länge 6): 5 = 000101; -5 = 111010
    - Problem 1: 5 + (-5) = 000101 + 111010 = 111111 = -0
    - Problem 2: 3 + (-2) = 000011 + 111101 = 000000 = 0
    - Aber: 2 + (-3) = 000010 + 111100 = 111110 = -1
### Zweierkomplement
- Wie Komplement, aber nach dem Invertieren wird die Zahl um eins erhöht
- Beispiel (Länge 6): 5 = 000101; -5 = 111011
    - 5 + (-5) = 000101 + 111011 = 000000 = 0
    - 3 + (-2) = 000011 + 111110 = 000001 = 1
    - 2 + (-3) = 000010 + 111101 = 111111 = -1
- Es gibt nur eine 0
- Es gibt eine negative Zahl mehr als positive Zahlen
    - 01111111 = 127
    - 10000001 = -127
    - 10000000 = -128
### Rechnen im Zweierkomplement
- Definition der Länge notwendig
    - Bit erhalten Nummerierung über Exponenten
- Addition problemlos (fast)
- Subtraktion durch Addition umgesetzt
- Multiplikation, Division: wie vorher, Vorzeichenvorbehandlung nötig
- Schiebeoperation nach rechts: Bit an erster Stelle muss erhalten werden
- Schiebeoperation nach links: unproblematisch
### Überlauf
- Beispiel (Länge 8): 127 + 1 = 01111111 + 00000001
- Ignorieren → 127 + 1 = 10000000 = -128
    - => Explosion der Ariane 5 bei ihrem Jungfernflug
    - Normalverhalten in vielen CPUs
    - Muss ggf. durch Implementierung der Programmiersprache geprüft werden
    - Verwendung „sicherer“ Bibliotheksfunktionen
- CPU bricht Verarbeitung ab, signalisiert Fehler
    - Für kritische Anwendungen, spezielle CPU notwendig
- Spezialwert „Fehler“ (ideal wäre 10000000)
    - Jede Operation mit diesem Wert ergibt diesen Wert
    - Anwendungssoftware muss Ergebnisse prüfen, um Fehlerort leichter zu bestimmen
## Darstellung von Dualbrüchen
### Dualbrüche
![[Pasted image 20261015104146.png]]
- Problem: Ablegen im Speicher
	- Zwei Variablen n und m
	    - Anzahl der Vorkomma- und der Nachkommastellen
	- Definierte Länge: n + m muss konstant sein
### Halblogarithmische Darstellung
- Beispiel: Lichtgeschwindigkeit = 299792458 m/s = 299792,458 km/s
	- 2,99792458·105 km/s = 2,99792458·108 m/s = 2,99792458·1010 cm/s
	- Genau eine Vorkommastelle, Rest Nachkomma, Skalierung über Exponent
- Rundungsfehler bleiben relativ klein, können aber absolut groß werden.
![[Pasted image 20261015104358.png]]
### Binäre Gleitkommazahlen
- Auch: Gleitpunktzahlen, *floating point number*
- Nach IEEE754 genormt
![[Pasted image 20261015104800.png|148]]
- Dabei ist „v“ das Vorzeichenbit; „1,m“ die binäre _Mantisse_ und „e“ der Exponent.
- v = 0 => (-1)^v = 1; v = 0 => (-1)^v = -1
- m ist Bitsequenz definierter Länge, interpretiert als Nachkommastellen
- e wird als positive Zahl c („Charakteristik“) gespeichert, mit e = c - B
    - B ist ein konstanter Wert für die Verschiebung (_Bias_)
    - c ist Bitsequenz definierter Länge
- v benötigt 1 Bit
- m und c besitzen definierte Länge (genannt `#m` und `#c`)
- Der Rest sind Konstanten: (-1), 2, B

![[Pasted image 20261015105051.png]]
- Nullwert bei c = 0 und m = 0 => +0 und -0
- Wenn c = 0, aber m > 0, gibt es alternative Darstellungen:
	- "denormalisierte Gleitkommazahlen" => "Unterlauf"
- Wenn c = 2^B -1
	- m = 0; r = +/- Unendlich
	- m > 0; r = NaN
### Rechnen mit Gleitkommazahlen
- **Addition und Subtraktion**
	- Zuerst Charakteristik angleichen, durch Schiebeoperation; dabei können Stellen verloren gehen.
	- Mantissen addieren bzw. subtrahieren
- **Multiplikation**
	- Exponenten addieren
	- Mantissen multiplizieren
- **Division**
	- Exponent ergibt sich aus Differenz der Exponenten von Dividend und Divisor
	- Mantissen dividieren
- Nach jeder Operation muss Mantisse evtl. normalisiert und das Ergebnis auf Überlauf/Unterlauf geprüft werden
- Da endliche Darstellung, kommt es auf Reihenfolge der Berechnungen an
- Assoziativ- und Distributivgesetze gelten nicht uneingeschränkt
- Beispiel (binary-32)
    - a = 2^1, b = 2^-23 
    - (a + b) + b = (a + 0) + b = a
    - a + (b + b) = a + 2^-22 = 1,00000000000000000000001·21
# Fazit
- Zahlensysteme erlauben die Darstellung von Zahlen
- Dualzahlen erlauben die Verarbeitung von Zahlen in IT-Systemen
- Zu Ein-/Ausgabe müssen Dualzahlen konvertiert werden
- Zahlensysteme mit einer 2er-Potenz fassen Bits von Dualzahlen zusammen
- Manche endlichen Dezimalbrüche können nicht als endliche Dualbrüche dargestellt werden
- Die Aussagenlogik lässt sich ebenfalls gut in IT-Systeme übertragen
- Jenseits von AND, OR, NOT gibt es weitere wichtige logische Operationen
- Binäres Rechnen mit ganzen Zahlen ähnelt dem Dezimalrechnen, sofern Zahl < 0 angemessen dargestellt werden
- Binäres Rechnen ist auf CPUs nur mit definierte Anzahl an Bits sinnvoll
- IEEE754 erlaubt das datensparsame Speichern von binären Gleitkommazahlen
- Bei allen Gleitkommazahlen mit definierter Länge spielt die Reihenfolge der Operationen eine essentielle Rolle.