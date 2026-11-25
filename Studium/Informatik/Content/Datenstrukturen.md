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
- Zugriff auf Elemente meist mittels *Namen*.
- Werden seltenst von der CPU als Ganzes verarbeitet.
## Referenzen (Zeiger)
- *Ziel:* Speicheradresse einer Struktur verarbeiten.
- Vermeidung von *Kopien*, Aufbau *komplexerer* Strukturen.
- *Operationen:* Adresse einer Datenstruktur, Datenstruktur unter einer Adresse.
## Speicherplatzzuweisung
### Anforderung
- *Funktion* oder *Sprachelement*, um zur Laufzeit Speicher einer definierten Größe anzufordern.
- Speicher wird durch *interne Mechanismen* verwaltet.
- Speicher kann wieder *zurückgegeben* werden.
- `void* malloc(size_t size)`; `new`; `make`.
### Freigabe von Speicher
- Wenn das Programm Speicher nicht mehr benötigt, wird er *freigegeben*.
- Wiederverwendung von freiem Speicher.
- `void free(void* ptr)`.
# Sequentielle Datenstrukturen
## Lineare Listen (Linked List)
- *Homogene* Datenstrukturen.
- Das erste Element hat *keinen* Vorgänger, alle anderen haben genau *einen* Vorgänger.
- Das letzte Element hat *keinen* Nachfolger, alle anderen haben genau *einen* Nachfolger.
- Jedes Element besitzt einen *Zeiger* auf seinen Nachfolger. Der vom letzten Element zeigt auf *nichts*.
- Die Liste ist ein *Zeiger* auf das *erste* Element.
- *Alternative:* Doppelt-Verlinkte-Liste
- *Operationen:* Einfügen, Löschen, Suchen, Traversieren.
## Ringlisten
- *Endliche* Anzahl von Elementen.
- Jedes Element besitzt genau *einen* Nachfolger & *einen* Vorgänger.
- Einfach oder doppelt verkettet.
## Stapel (Stack)
- Häufiger Anwendungsfall: Aufgaben zurückstellen.
	- Daten bisheriger Aufgaben müssen *zwischengespeichert* werden.
- Auf zuletzt *zurückgestellte* Daten muss nach Beendigung der neuen Aufgaben zugegriffen werden.
- *LIFO:* Last-In-First-Out.
- *Operationen:* `push`, `pop`, `empty`, `top`.
## Warteschlange (Queue)
- *Anwendungsf*