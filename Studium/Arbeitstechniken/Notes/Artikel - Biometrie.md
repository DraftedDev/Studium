# Konzept
- **Ziel:** Entwicklung Authentifizierungssystem anhand von Gangart.
- **Annahme:** Aktive Nutzer-Phase besser als Flache Phase.
- **Metriken:**
	- Vertikale Bewegung $V$.
	- Laterale/seitliche Bewegung $L$.
	- Anterior-Posterior-Beschleunigung (Vorwärts, Rückwärts) $A$.
		- Unterteilt in:
			- Statisch $S$.
			- Dynamisch $D$.
	- *Jerk:* $J = \frac{\Delta \text{Acceleration}}{\Delta \text{Time}} = \frac{ACC_{t_{1}} - ACC_{t_{2}}}{\text{Sampling Rate (30ms)}}$
	- *Threshold:* Schwellenwert aus 100 aufeinanderfolgende Abtastwerte.
	- *Normalisierte euklidische Distanz* (Abstand Testmetrik und Trainingsreferenzen).
- Klassifikation mit *KNN* (k = 1): Suche Nutzer mit geringster Distanz.
# W-Fragen
- **Wer:** 
	- *Autoren:* Sangil Choi, Ik-Hyun Youn, Richelle LeMay, Scott Burns und Jong-Hoon Youn (von der University of Nebraska at Omaha sowie der Lincoln Pius X High School).
	- *Probanden:* 5 Männer + 5 Frauen.
- **Was:** Biometrische Gangerkennung mit KNN.
- **Wann:** Februar 2024.
- **Wo:** Universität Nebraska Omaha.
- **Wie:** Messung von 3-Achsen-Beschleunigung.
- **Warum:** Um schwächere Methoden zu umgehen. Läuft im Hintergrund ab.
# Kritik
- Studie nur mit 10 Personen.
- Test nur mit KNN (k = 1) und konstanter Menge an Personen möglich.
- Kontrollierte Testumgebung, statt freie Umgebung.
- Feste Heuristik, anstatt dynamisches Formular.
- Angriffsmöglichkeiten & Spoofing möglich.