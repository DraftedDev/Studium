# Struktur
1. Deckblatt (inkl. Modul-Einleitung KI, HS Heilbronn, Thema B01, Team).
2. Inhaltsverzeichnis.
3. Hauptteil (3 Blöcke à ca. 7 Seiten = ca. 21 Seiten) mit expliziter Kennzeichnung der Hauptverantwortung pro Block.
4. Eidesstattliche Erklärung. Jeder auf die gleiche.
5. Übersicht der KI-Tools & Modifikationen.
6. Literaturverzeichnis (Crawford 2021, Longpre et al. 2024 sowie ggf. herangezogene Sekundär-/Rechtsquellen aus den Papern).
# Inhaltsangabe
- **Block A:**
	- **1.1 Einleitung & Fragestellung (1,5 Seiten):**
		- *Leitfrage:* Was bedeutet "im Internet stehen" rechtlich, ethisch & technisch? "Data Commons" mit frei verfügbaren Daten in der Theorie VS. Praxis.
		- *Crawfords kartografische Perspektive (Atlas of AI):* KI ist weder künstlich, noch intelligent, sondern eine material-, energie-, arbeits- & datenintensive Industrie ("Megamachine").
		- *Analogie* (Mythe) zum menschlichen Geist.
	- **1.2 Historische Datengier & "Image of Infrastructure" (2 Seiten):**
		- *Vom Regelwerk zur statistischen Masse:* Übergang von symbolischen/regelbasierte Ansätzen zu datenhungrigen statistischen/probalistischen Verfahren (u.a. IBM-Spracherkennung, Penn Treebank, Enron-Korpus). Reduktion von Sprache & Bedeutung auf statistische Muster.
		- *Biometrische & visuelle Archive als Vorläufer:* Vom FERET-Datensatz (mit Einwilligung) zu NIST Special Database 32 (Polizei-Mugshots ohne Einwilligung).
		- *"Shift from Image to Infrastructure":* Wie persönliche Bilder, soziale Interaktionen & sensible Kontexte entkontextualisiert & zu scheinbar neutraler "Ground Truth" erklärt werden.
	- **1.3 Web-Scraping, ImageNet & Ende von Consent (2 Seiten):**
		- *Das Internet als natürliche Ressource:* Massenhaftes Scraping von Suchmaschinen, sozialen Netzwerken & Plattformen ohne Wissen oder Einwilligung der Betroffenen sowie verknüpft mit unterbezahlter Crowdwork (Amazon Mechanical Turk).
		- *Fallbeispiele fehlender Einwilligung & Re-Identifikation:* DukeMTMC (unbemerkte Campus-Aufnahme & Weiternutzung), NYC Taxi-Datensatz (Deanonymisierung & "predictive privacy harms"), sowie Royal Free NHS/DeepMind (Datenschutzvertoß trotz öffentlicher/institutioneller Zwecke).
		- *Metaphern der Extraktion & "Ethics at Arm's Length":* Rhetorik von "Data is the new oil" und Datenkapitalismus (Fourcade & Healvy, Sadowski). Warum technische/mathematische Distanz und fehlende Ethikprüfung (IRBs) schädliche Datennutzung begünstigen.
	- **1.4 Klassifikation als Machtakt & "Capture of the Commons" (1,5 Seiten):**
		- *Taxonomien sind nicht neutral:* Wie Datensätze (wie ImageNet/WordNet oder UTKFace) soziale, geschlechtliche & rassifizierte Kategorien festschreiben & verstärken ("epistemic machinery", Knorr Cetina: "looping effect", Hacking; "digital epidermalization", Browne).
		- *Capture of the Commons:* Privatisierung öffentlichen Wissens durch geschlossene Modelle & proprietäre Vorteile. Der öffentliche Raum wird ausgenutzt, während der "Metawert" (Modelle, Produkte, Macht) privatisiert wird.
		- *Überleitung zu Block 2:* Während Crawford die strukturelle & historische Logik der Datenextraktion freilegt, untersuchen Longpre et al. (2024), wie Website-Betreiber im Web aktiv auf diese Nutzung reagieren & warum bestehende technische/rechtliche Signale bröckeln.
- **Block B:**
	- **2.1 Ausgangslage & Forschungsdesign des Audits (1,5 Seiten):**
		- *Problemstellung:* Web-Korpora (C4, RefinedWeb, Dolma, abgeleitet aus Common Crawl) bilden das Rückgrat moderner Foundation Models (GPT-4o, Gemini), kollidieren aber zunehmend mit Einwilligung, Urheberrecht & Monetarisierung.
		- *Korpora & Stichproben (2016-April 2024 über die Wayback Machine):* Analyse von ca. 14.000 Webdomains insgesamt. $HEAD_{All}$ (Vereinigung der Top-2000-Domains nach Tokenzahl aus den drei Korpora, ca. 3,95k Domains; dazu $HEAD_{C4}$), $RANDOM_{10k}$ (aus 10.136.147 Schnittmengen-Domains) und $RANDOM_{2k}$ für manuelle Annotation.
		- *Mehrschichtige Annotation:* Kombination aus menschlichen Annotation (14 Crowdworker, ca. 25-30 USD/Std., Modalitäten, Nutzerinhalte, Paywalls, Werbung, Domainzweck) & automatisierter LLM-Klassifikation (GPT-4o) von Terms of Service mit Taxonomien für Competing Services, License Type sowie Crawling & AI (inkl. Gold-Standard-Prüfung, 85%-92% Precision/Recall).
	- **2.2 Rasante Zunahme von Restriktionen & SARIMA-Prognosen (2 Seiten):**
		- *Ende der Default-Offenheit:* Sinkender Anteil von Domains ohne robots.txt (von ca. 20%) bzw. ohne ToS (von ca. 80%) im $HEAD_{C4}$ seit 2016 auf nahezu null.
		- *Sprunghafter Anstieg nach Mid-2023 (GPTBot, Google-Extended):* Vollständige robots.txt-Sperren steigen innerhalb eines Jahres (April 2023 bis April 2024) im Gesamtbestand der drei Korpora von ca. 1% auf ca 5-7% der Tokens (+500% + relativer Anstieg bei C4 und RefinedWeb), im kritischen $HEAD_{All}$ von <3% auf ca. 20-33% (in C4 ca. 5%+ gesamt bzw. 28% im Head).
		- *Terms of Service & Zeitreihenprognose:* 2024 verbreiten sich explizite Anti-KI-Klauseln. Run 45-55% der Korpus-Tokens weisen irgendeine ToS-Beschränkung auf. SARIMA-Prognosen bis April 2025 erwarten weitere +2-4 Prozentpunkte Vollblockierung durch robots.txt im Gesamtkorpus (+7-11 Prozentpunkte im Head) & +6-10 Prozentpunkte bei restriktiven ToS.
	- **2.3 Asymmetrien zwischen KI-Anbietern & "Unrecognized Agents" (1,5 Seiten):**
		- *Ungleiche Blockierquoten:* Im $HEAD_{C4}$ (April 2024) trifft die Blockierung durch robots.txt OpenAI mit 25,9% der Tokens deutlich stärker als Anthropic & Common Crawl (je 13,3%), Google Extended (9,8%), Cohere (4,9%), Meta (4,1%), Internet Archive (3,2%) & Google Search (1,0%).
		- *Bedingte Wahrscheinlichkeiten:* Ist mindestens ein AI-Anbieter blockiert, wird OpenAI in 91,5% der Fälle mitgesperrt, Common Crawl & Anthropic in 52,2% - während Internet Archive (32,3%) & Google Search (17,1%) häufiger ausgenommen bleiben (Unterscheidung KI-Training, Suche, Archivierung).
		- *Nicht anerkannte / fiktive User-Agents:* Auftreten nicht offiziell bestätigter Agenten wie `anthropic-ai` oder `Claude-Web` (FALSE ANTHROPIC, in 4,5% der Websites blockiert, während der offizielle `ClaudeBot` teils fehlt) als Beleg für Fragmentierung & Überforderung von Domain-Betreibern.
	- **2.4 Widersprüche zwischen robots.txt & Terms of Service sowie Protokollkritik (2 Seiten):**
		- *Technische vs. rechtliche Ebene:* Der Robots Exclusion Protocol (REP / robots.txt RFC 9309) ist maschinenlesbar, aber nicht rechtsverbindlich & von 1995. Terms of Service sind rechtliche Vereinbarung mit feineren Klauseln (Non-Complete, No-Re-Distribution, Non-Commercial), werden aber von Crawlern oft nicht automatisch gelesen.
		- *Diskrepanzen & Kollisionen:* Häufige Inkosistenzen, etwa anti-crawling/anti-AI-ToS ohne robots.txt (35,1%), restriktive robots.txt ohne ToS (20,3%) oder Nicht-Kommerzklauseln mit robots.txt-Sperren, die unbeabsichtigt auch Forschung/nicht-kommerzielle Crawls treffen.
		- *Umgehung & Ruf nach neuen Standard:* Vorwürfe, wonach Anbieter robots.txt-Opt-outs für Trainingsdaten umgehen, indem sie Inhalte zur Inferenz-/Retrieval-Zeit abrufen (z.B. ChatGPT-User vs. GPTBot oder unregistrierte Retrieval-Crawler). Forderung nach standardisierten, maschinenlesbaren Nutzungs-/Zwecksignalen statt bloßer Agenten-Listen.
		- *Überleitung zu Block 3:* Wie verändern diese Sperren & Datenstrukturen die Qualität & Repräsentativität der Trainingsdaten & wie passt das zu dem, was Menschen mit KI tatsächlich tun?
- **Block C:**
	- **3.1 Head vs. Long Tail: Kommerzialisierung, Multimodalität & Sperrwellen (2 Seiten):**
		- *Strukturelle Divergenz:* Das breite Web ($RANDOM_{2k}$) besteht überwiegend aus Organisations-/Persönlichen Websites, Blogs & E-Commerce, während der Token-lsatige Head ($HEAD_{All}$) stark von Nachrichten/Periodika, sozialen Medien/Foren & Enzyklopädien geprägt ist.
		- *Monetarisierung & Multimodalität im Head:* Domains im $HEAD_{All}$ weisen deutlich häufiger Werbung (+47,5%) & Paywalls (+24,1%) sowie Bild- (+4,4), Video- (+39,8%) & Audioinhalte (38,4%) auf.
		- *Verschiebung der Korpuszusammensetzung:* Da Nachrichten (fast 45% im $HEAD_{All}$ per robots.txt blockiert gegenüber 3% im Jahr 2023), Foren & soziale Medien überproportional sperren, droht bei Beachtung der Opt-outs eine Verschiebung hin zu älteren Inhalten sowie zu Organisations- & E-Commerce-Seiten.
	- **3.2 Mismatch zwischen Trainingsdaten & realer KI-Nutzung (WildChat) (2 Seiten):**
		- *Empirischer Vergleich:* Abgleich der Service-Kategorien aus $HEAD_{C4}$ mit realen ChatGPT-Konversationen aus dem WildChat-Datensatz (1 Mio. Interaktionen; Manuelle Clusterung von 100 Logs + GPT-4o-Klassifikation von 1000 Logs).
		- *Kreative & sexuelle Nutzungen vs. Web-Repräsentation:* Über 30% der WildChat-Anfragen betreffen kreative Texte/Rollenspiele (Creative Composition) & ca. 12% sexuelle Rollenspiele/Inhalte, obwohl kreative Formate im Webkorpus schwach vertreten sind & explizite/sensible Inhalte (<1% im $HEAD_{C4}$) stark herausgefiltert werden.
		- *Nachrichten vs. Fair Use (17 U.S.C. § 107):* Während Nachrichten-Domains fast 40% der Tokens im $HEAD_{C4}$ ausmachen, entfallen <1% der WildChat-Anfragen auf aktuelle Nachrichten - ein Befund, der für die Fair-Use-Prüfung (Marktwirkung, Substituierung) relevant ist, aber aufgrund von Stichproben- & Taxonomie-Limiationen (WildChat auf HuggingFace Spaces, GPT-3.5-Turbo/GPT-4, implizite Nutzung von News-Wissen in allgemeinen Antworten) vorsichtig interpretiert werden muss.
	- **3.3 Kollateralschäden für Forschung, Archive & "Wallad Gardens" (1,5 Seiten):**
		- *Nicht-kommerzielle Akteure als "Secondary Victims":* Pauschale Wildcard-Sperren (`*`) oder das Blockieren gemeinnütziger Archive wie Common Crawl über (10000 zitierte Forschungsarbeiten) & Internet Archive treffen akademische Forschung, Transparenz & nicht-kommerzielle KI.
		- *Kommerzialisierung & "Wallet Gardens":* Wirtschaftliche Ängste & fehlende feingranulare Steuerungsmechanismen treiben Anbieter hinter Paywalls, Logins oder in geschlossene Plattformen, was die offene Web-Allmende weiter verengt & kleinere Akteure benachteiligt.
		- *Spannungsfeld "Consent" vs. "Right to Read & Learn":* Abwägung zwischen Urheberrecht, Privatsphäre & Monetarisierung einerseits (inkl. des Problems, dass Plattformen/Admins oft nicht identisch mit den ursprünglichen Urhebern sind).
	- **3.4 Synthese & Fazit: Dürfen KI-Systeme mit allem trainiert werden, was im Internet steht? (1,5 Seiten):**
		- *Direkte Antwort auf die Leitfrage:* Nein, weder normativ (Urheberrecht, Datenschutz, Einwilligung, Verteilungs- & Klimagerechtigkeit bei Crawford) noch praktisch-infrastrukturell (zerfallender Consent, Protokoll-Inkompatibilitäten und Walled Gardens bei Longpre et al.) lässt "alles im Internet" als bedingungsloses Selbstbedienungslager rechtfertigen.
		- *Zusammenführung der Perspektiven:* Crawford zeigt die tiefe extraktive & klassifikatorische Machtlogik hinter der Datengewinnung. Longpre et al. belegen empirisch den aktuellen Vertrauens- & Protokollbruch im Web sowie die Diskrepanz zwischen Trainingsquellen & realen Nutzungsmustern.
		- *Ausblick für Praxis, Governance & Technik:* Bedarf an klaren, maschinenlesbaren & durchsetzbaren Einwilligungs-/Nutzungsprotokollen, transparenter Datendokumentation (Datasheets/Provenance) sowie rechtlichen Rahmenbedingungen, die Urheber schützen & zugleich Forschung sowie offene/gemeinwohlorientierte KI nicht ersticken.