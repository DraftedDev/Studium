"Two Routes to Alzheimer's Disease Based on Differential Structural Changes in Key Brain Regions" authors:
- Yasmin Hollenbenders
- Monika Pobiruchin
- Alexandra Reichenbach year: 2023 journal: Journal of Alzheimer's Disease doi: 10.3233/JAD-221061 tags:
# Two Routes to Alzheimer's Disease (Hollenbenders et al., 2023)

## 1. Hintergrund, Ziel, Methoden & Resultate
### Hintergrund
- **Früher Beginn:** Neuropathologische Veränderungen (Atrophie) gehen klinischen Alzheimer-Symptomen um bis zu **zwei Jahrzehnte** voraus (beginnend oft in Hippocampus und entorhinalem Kortex).
- **Heterogenität:** Klinische Diagnosen (nach NINCDS-ADRDA) führen zu heterogenen Krankheitsbildern, was Frühdiagnose und gezielte Therapieentwicklung erschwert.
- **Lücke bestehender Modelle:** Viele Verlaufsmodelle setzen eine feste Baseline (z. B. Diagnosezeitpunkt) voraus, schränken Zustände ein oder verwerfen unvollständige Datensätze.
### Ziel der Studie
- Datengetriebene Identifikation von **Zwischenstadien der Alzheimer-Progression** und deren Vorläufern anhand neuroanatomischer Merkmale (Atrophie der grauen Substanz), ohne feste Startzeitpunkte oder vordefinierte Zustandsvorgaben.
- Überprüfung der klinischen Relevanz dieser Stadien durch Verknüpfung mit kognitiven Teilfunktionen und Biomarkern.
### Methoden
- **Datenbasis:** Längsschnittliche Daten der _Alzheimer's Disease Neuroimaging Initiative_ (ADNI) von $N = 1.017$ **Teilnehmenden** (324 HC, 572 MCI, 121 AD) mit insgesamt $4.383$ **jährlichen Besuchen** (Sequenzlänge 3–11 Jahre).
- **Features (14 Merkmale):** Aus strukturellen MRTs (sMRI, FreeSurfer) wurden beidseitig 7 Schlüsselregionen extrahiert:
    - _Subkortikales Volumen:_ Amygdala (AM), Hippocampus (Hip).
    - _Kortikale Dicke:_ Parahippocampus (PHip), entorhinaler Kortex (EC), Precuneus (PreC), inferiorer (IT) und mittlerer Temporalkortex (MT).
- **Modellierung:** Training unüberwachter **Gaußscher Hidden Markov Models (HMM)** (Baum-Welch-Algorithmus) für 2 bis 15 Zustände; Dekodierung über den Viterbi-Algorithmus. Die optimale Zustandszahl wurde über Cluster-Stabilität (_Adjusted Rand Score_ über 10 Random Seeds) ermittelt.
- **Validierung/Charakterisierung:** Vergleich der Zustände hinsichtlich kognitiver Subscores (**ADAS-cog 11**), _APOE-ε4_-Genotyp sowie CSF- (Aβ, Tau, p-Tau) und PET-Markern (FDG, AV45).
### Resultate
- **8 Krankheitsstadien (Zustände 0–7):** Das Modell zeigt ein stabiles 8-Zustands-System, in dem Teilnehmende aller klinischen Diagnosen (HC, MCI, AD) vorkommen, AD aber in späten Stadien dominiert.
- **Zwei parallele Verlaufsrouten** (mit einer frühen Kreuzung von Zustand 2 nach 3 bei $>5\,\%$ Übergangswahrscheinlichkeit und Zusammenführung im Endstadium 7):
    - **Limbische Route (**$2 \rightarrow 4 \rightarrow 6 \rightarrow 7$**):** Frühe Atrophie in limbischen Regionen (AM, Hip, PHip, EC). Stärkere kognitive Einbußen (insbesondere Gedächtnis: Wortabruf, Orientierung, Worterkennung), höherer Anteil an AD-Diagnosen und signifikant mehr Träger von zwei _APOE-ε4_-Allelen.
    - **Kortikale Route (**$0 \rightarrow 1 \rightarrow 3 \rightarrow 5 \rightarrow 7$**):** Frühe, anhaltende Atrophie in nicht-limbischen kortikalen Regionen (PreC, IT, MT). Insgesamt bessere Gedächtnisleistung, aber spezifisch stärkere Defizite bei Befehlen (_commands_) und Konstruktion (_construction_) in späteren Vergleichen sowie höhere Anteile an HC/MCI.
- **Biomarker:** In den frühen Stadien der limbischen Route zeigen sich signifikant niedrigere CSF-Aβ-Werte und ein geringerer Glukosestoffwechsel (FDG-PET) als in der kortikalen Route.
## 2. W-Fragen
- **Wer?** Yasmin Hollenbenders, Monika Pobiruchin und Alexandra Reichenbach (Universität Heidelberg & Hochschule Heilbronn) auf Basis der ADNI-Datenbank.
- **Was?** Räumlich-zeitliche Modellierung der Atrophie der grauen Substanz mittels HMM zur Identifikation von Alzheimer-Subtypen und Krankheitsstadien.
- **Wann?** Datenabruf im Oktober 2018; Annahme der Publikation am 8. Februar 2023, Veröffentlichung 2023 (_Journal of Alzheimer's Disease_, Bd. 92).
- **Wo?** Forschung der Autorinnen in Heidelberg/Heilbronn (Deutschland); multi-zentrische ADNI-Kohorte aus den USA und Kanada.
- **Warum?** Um die Heterogenität von Alzheimer-Verläufen datengetrieben abzubilden, atypische (nicht primär gedächtnisgetriebene) Verläufe früher zu erkennen und Prognosen sowie stratifizierte Therapien zu ermöglichen.
- **Wie?** Längsschnittliche sMRI-Auswertung (14 ROIs) $\rightarrow$ unüberwachtes Gaußsches HMM $\rightarrow$ Stabilitätsanalyse (_Adjusted Rand Score_) $\rightarrow$ statistische Gruppenvergleiche für Kognition, Genetik und Biomarker.
## 3. Mögliche Kritikpunkte (Diskussionsgrundlage)
### Methodische & inhaltliche Kritik
- **Reduktion auf 7 Regionen / nur sMRI im Modell:** Das HMM nutzt ausschließlich 14 anatomische Merkmale; wichtige andere Kortexareale (z. B. für weitere Subtypen wie bei Young et al., 2018) sowie Kognition und Biomarker flossen nicht direkt in die Modellbildung ein.
- **Unvollständige Biomarker-Daten:** CSF- und PET-Werte lagen nur für ca. **27 % bis 46 %** der Datenpunkte vor – Vergleiche zu Amyloid/Tau/FDG zwischen den Routen sind daher weniger belastbar als die MRT-Ergebnisse.
- **Stichproben-Bias (ADNI):** Die Kohorte ist nicht repräsentativ für die Allgemeinbevölkerung (94 % weiß, durchschnittlich 16 Bildungsjahre, gezielte klinische Rekrutierung).
- **Diskretisierung & Interpolation:** Kontinuierliche biologische Prozesse werden in diskrete Jahresintervalle und 8 feste Zustände gepresst; fehlende Zwischenwerte wurden linear interpoliert.
- **Sensitivität des ADAS-cog:** Der klassische ADAS-cog 11 ist für fortgeschrittene Demenz konzipiert, bildet aber subtile Veränderungen in frühen Prä-Demenz-Stadien nur eingeschränkt ab.
### Limitationen laut den Autorinnen
- **Fehlende externe Validierung:** Ergebnisse müssen an unabhängigen Kohorten außerhalb von ADNI repliziert werden.
- **Widersprüche bei Amyloid-Markern:** Unterschiede in den Amyloid-Befunden im Vergleich zu früheren Studien (z. B. Goyal et al., 2018) müssen in kombinierten multimodalen Studien geklärt werden.
- **Eingeschränkte klinische Praxistauglichkeit:** Hochauflösende sMRI-Scans sind teuer und die aufwendige FreeSurfer-Vorverarbeitung ist aktuell noch nicht für die klinische Routine geeignet (exploratives Forschungsstadium).