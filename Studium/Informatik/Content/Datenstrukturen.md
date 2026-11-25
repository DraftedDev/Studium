# Elementare Datenstrukturen
## Skalare Daten
- *"skalar"* -> Angabe einer Zahl.
- Einzelner Zahlenwert, nicht weiter unterteilbar -> *atomar*.
- *Boolean Type:* "falsch" = 0; "wahr" != 0.
- Meist als 1-16 Byte im CPU/Speicher.
## Felder (Arrays)
- *Ziel:* Mehr als ein Exemplar einer Datenstruktur hintereinander im Speicher ablegen.
- Ein Feld ist eine *homogene* zusammengesetzte Datenstruktur, deren Elemente über eine *Position* angesprochen werden.
- Elemente eines Feldes werden konsekutiv im *Speicher* abgelegt.
- Nur kleine Felder können von der CPU als Ganzes verarbeitet werden (-> *SIMD*).
- Position ist meist eine Zahl $\geq 0$.
## Verbundene (Records, Strukturen)
- *Ziel:* Unterschiedliche Datenstrukturen, unter einem Dach, zusammenfassen.
- 