# Axiomatische Kontinuumsökonomik

## Eine vollständige ökonomische Theorie aus zehn Axiomen

---

**Maximilian Schmeer · Tristan Schmeer**

Universität des Saarlandes

2025

---

## Zusammenfassung

Diese Monographie entwickelt eine geschlossene ökonomische Theorie aus zehn Axiomen. Die Axiome — drei Erhaltungssätze, ein Flussprinzip, drei Verhaltenspostulate, eine biologische Kopplung, eine Gütertaxonomie und eine Informationskostenbedingung — erzeugen ein System von 75 Differentialgleichungen, das die Dynamik aller ökonomischen Observablen bestimmt: Preise, Mengen, Verteilungen, Flüsse, Erwartungen und institutionelle Reaktionen. Das System ist strukturell vollständig im Sinne der Hadamard-Bedingungen (Existenz, Eindeutigkeit, stetige Abhängigkeit) und kausal geschlossen — jede endogene Variable wird durch die Systemgleichungen bestimmt, jede exogene Variable ist als solche benannt.

Die Theorie trennt strikt zwischen *axiomatischer Struktur* (unveränderlich), *allgemeinen Gleichungen* (eine eindeutige Form pro Variable) und *Modellierungswahlen* (austauschbare funktionale Formen). Spezifische Funktionalformen — Cobb-Douglas, CRRA, logistische Diffusion — sind keine Bestandteile der Theorie, sondern Elemente eines Baukastens, aus dem der Anwender je nach Kontext wählt. Die qualitativen Eigenschaften (Stabilität, Spezialfälle, kausale Struktur) hängen nur von den axiomatischen Eigenschaften ab, nicht von der Formwahl.

Unter geeigneten Grenzübergängen reproduziert das System die Modelle von Solow, Ramsey, Arrow-Debreu, Hicks (IS-LM), Sharpe (CAPM), Mundell-Fleming, Minsky, Fisher, Piketty, Stigler, Akerlof, Grossman-Stiglitz und Granovetter als Spezialfälle. Darüber hinaus beschreibt es spezifische Märkte (Arbeit, Immobilien, Kredit, Plattformen), klassifiziert Marktversagen systematisch als messbare Abweichung vom Gleichgewicht und löst konkrete Probleme, die kein Einzelmodell beantworten kann — darunter die optimale Bankenanzahl, den kritischen Blasen-Schwellenwert und die Bedingung fiskalischer Tragfähigkeit.

Die numerische Validierung erfolgt durch eine Weltsimulation mit 30 Länderprofilen (2000–2050), Krisensimulationen (Finanzkrise 2008, Pandemie) und empirische Proxy-Tests gegen Weltbank-, IWF- und UNDP-Daten.

---

## Vorwort

Die ökonomische Wissenschaft besitzt kein Standardmodell. In der Physik beschreiben wenige Gleichungen — Maxwell, Einstein, Schrödinger, das Standardmodell — die bekannten Phänomene vollständig und konsistent. In der Ökonomik existiert stattdessen ein Archipel spezialisierter Modelle: Solow für Wachstum, IS-LM für Konjunktur, CAPM für Finanzmärkte, Mundell-Fleming für offene Volkswirtschaften, Minsky für Krisen. Jedes Modell beschreibt einen Aspekt der Realität, keines beschreibt alle. Die Modelle widersprechen einander in ihren Annahmen, sind nicht kombinierbar und lassen fundamentale Fragen offen — etwa warum Finanzkrisen auftreten, obwohl Kapital im Arrow-Debreu-Gleichgewicht effizient alloziert sein sollte.

Diese Monographie unternimmt den Versuch, die Fragmente zu einem konsistenten Ganzen zusammenzufügen. Nicht durch Eklektizismus — das Nebeneinanderstellen unvereinbarer Modelle — sondern durch Axiomatisierung: Wir formulieren zehn Grundannahmen, aus denen sich ein einziges Gleichungssystem ergibt. Die bekannten Modelle entstehen daraus als Grenzfälle unter vereinfachenden Annahmen, so wie die Newtonsche Mechanik aus der Allgemeinen Relativitätstheorie bei kleinen Geschwindigkeiten folgt.

Der Anspruch ist nicht, die Ökonomie zur Physik zu machen. Die Unterschiede sind fundamental: Agenten sind heterogen, Institutionen veränderlich, Erwartungen reflexiv. Aber die *Methode* — aus wenigen Axiomen ein geschlossenes System abzuleiten und seine Konsequenzen rigoros zu prüfen — ist übertragbar. Ob sie trägt, entscheidet sich an der Frage, ob das resultierende System die bekannten Phänomene reproduziert und darüber hinaus neue, testbare Vorhersagen erzeugt.

Die Monographie richtet sich an Ökonomen, die bereit sind, gewohnte Modellgrenzen zu überschreiten, an Physiker, die ökonomische Systeme als dynamische Systeme ernst nehmen, und an Mathematiker, die an der Struktur gekoppelter stochastischer Differentialgleichungen mit Sprüngen und Regimewechseln interessiert sind.

**Maximilian Schmeer & Tristan Schmeer**
*Saarbrücken, 2025*

---

# TEIL I — GRUNDLAGEN

---

# Kapitel 1: Einleitung — Warum eine axiomatische Ökonomie?

---

## 1.1 Das Fragmentierungsproblem

Die moderne Ökonomik besteht aus einer großen Zahl spezialisierter Modelle, die jeweils einen Ausschnitt der wirtschaftlichen Realität beschreiben. Die Standardlehrbücher präsentieren diese Modelle als getrennte Theorien mit eigenen Annahmen, eigenen Variablen und eigenen Schlussfolgerungen:

| Modell | Erklärt | Annahmen | Ignoriert |
|--------|---------|----------|-----------|
| Solow (1956) | Langfristiges Wachstum | 1 Gut, 1 Agent, exogene Sparquote | Geld, Verteilung, Finanzmärkte, Information |
| Ramsey (1928) | Optimales Sparen | 1 Gut, 1 Agent, perfekte Voraussicht | Geld, Heterogenität, Unsicherheit |
| Arrow-Debreu (1954) | Allgemeines Gleichgewicht | Vollständige Märkte, perfekte Information | Dynamik, Geld, Krisen, Herding |
| IS-LM (Hicks 1937) | Konjunktur | Geschlossene Volkswirtschaft, feste Preise | Wachstum, Erwartungen, Finanzmärkte |
| CAPM (Sharpe 1964) | Assetpreise | 1 Periode, Mean-Variance-Nutzen | Produktion, Geld, Realwirtschaft |
| Mundell-Fleming (1962/63) | Offene Volkswirtschaft | Kleine offene VW, perfekte Kapitalmobilität | Herding, Information, Verteilung |
| Minsky (1986) | Finanzinstabilität | Informell, kein geschlossenes Modell | Alles außer Kreditzyklen |
| DSGE (Kydland-Prescott ff.) | Konjunktur | Repräsentativer Agent, rationale Erwartungen | Heterogenität, Finanzmärkte, Krisen |

Die Tabelle zeigt das Kernproblem: Jedes Modell erkauft seine analytische Klarheit durch Annahmen, die die meisten anderen Phänomene ausschließen. Ein Modell, das Wachstum erklärt (Solow), sagt nichts über Krisen. Ein Modell, das Krisen beschreibt (Minsky), besitzt kein geschlossenes Gleichungssystem. Ein Modell, das Gleichgewicht beweist (Arrow-Debreu), setzt perfekte Information voraus und schließt damit die Informationsasymmetrien aus, die nach Akerlof (1970), Spence (1973) und Stiglitz (1981) für das Verständnis realer Märkte unverzichtbar sind.

Die Konsequenzen dieses Fragmentierungsproblems sind gravierend:

1. **Widersprüchliche Politikempfehlungen.** Ein IS-LM-Ökonom empfiehlt Fiskalstimulus in der Rezession; ein RBC-Ökonom hält die Rezession für effizient. Beide berufen sich auf formale Modelle. Die Modelle sind nicht vergleichbar, weil sie auf inkompatiblen Annahmen ruhen.

2. **Blinde Flecken.** Die Finanzkrise 2007–2009 wurde von der Mehrheit der makroökonomischen Modelle nicht vorhergesagt — nicht weil die Modelle falsch parametrisiert waren, sondern weil sie die relevanten Mechanismen (endogene Kreditdynamik, Herding auf Immobilienmärkten, Informationsasymmetrie bei strukturierten Produkten) schlicht nicht enthielten. Die Mechanismen existierten in Einzelmodellen (Minsky informell, Akerlof für Asymmetrie), aber diese waren nicht in die Standardmakroökonomik integriert.

3. **Fehlende Konsistenz.** Ein Student, der im Sommersemester das Arrow-Debreu-Gleichgewicht als Effizienzresultat lernt und im Wintersemester die Minsky-Instabilität als empirische Tatsache, hat keine Möglichkeit zu beurteilen, ob beides gleichzeitig wahr sein kann. (Es kann: Arrow-Debreu ist ein Grenzfall unter Annahmen, die in der Realität nicht erfüllt sind. Aber welche Annahmen genau, und wie hängt der Übergang zusammen? Darauf gibt die existierende Literatur keine systematische Antwort.)

4. **Keine ökonomischen Erhaltungssätze.** In der Physik garantieren Erhaltungssätze (Energie, Impuls, Ladung) die Konsistenz: Was in einer Gleichung erzeugt wird, muss in einer anderen verbraucht werden. In der Ökonomik werden Erhaltungsaussagen (Saldenmechanik, Bilanzidentitäten) oft ignoriert oder nur nachträglich geprüft. Modelle, die diese Identitäten verletzen — und viele partialanalytische Modelle tun das — produzieren logisch inkonsistente Vorhersagen.

## 1.2 Die fundamentale Frage

Die Physik hat ihr Fragmentierungsproblem gelöst — nicht vollständig, aber weitgehend. Die elektromagnetischen Phänomene, die Faraday noch als separate Entdeckungen beschrieb, sind seit Maxwell vier Gleichungen. Die Gravitationsphänomene, für die Newton eine Fernwirkung postulierte, sind seit Einstein eine geometrische Gleichung. Das Vorgehen war stets dasselbe: Axiomatisierung. Man formuliert die allgemeinsten Annahmen, die mit allen bekannten Beobachtungen verträglich sind, und leitet daraus ein geschlossenes Gleichungssystem ab.

Wir übertragen diese Methode auf die Ökonomie und stellen die analoge Frage:

> **Fundamentale Frage.** Welche Güterarten existieren, welche Agenten handeln, und welche Gleichungen bestimmen die Dynamik aller ökonomischen Observablen — Preise, Mengen, Verteilungen, Flüsse, Erwartungen — vollständig und geschlossen?

Die Antwort, die diese Monographie entwickelt, besteht aus drei Komponenten:

1. **Zehn Axiome** (Kapitel 2), die die fundamentalen Regeln der ökonomischen Dynamik festlegen: drei Erhaltungssätze (Vermögen, Güter, Geld), ein Flussprinzip (Gradienten), drei Verhaltenspostulate (Nutzenmaximierung, soziale Kopplung, adaptive Erwartungen), eine biologische Kopplung (Populationsrückkopplung), eine Gütertaxonomie (sechs Klassen) und eine Informationskostenbedingung.

2. **75 Gleichungen** (Kapitel 4–10), die aus den Axiomen folgen: Erhaltungsgleichungen, Preisdynamik, Entscheidungsgleichungen (Konsum, Arbeit, Portfolio, Produktion, Erwartungen), Informationsdynamik, Geldschöpfung, Populationsdynamik und Sprungprozesse. Jede Gleichung erscheint in ihrer allgemeinsten Form — ohne eingesetzte Funktionalformen.

3. **Ein Baukasten** austauschbarer funktionaler Formen (Anhang C), aus dem der Anwender je nach Kontext wählt: CRRA oder CARA für den Nutzen, Cobb-Douglas oder CES für die Produktion, lineares oder sigmoïdes Herding. Die Theorie legt die *Struktur* fest, der Anwender wählt die *Form*.

## 1.3 Vollständigkeitskriterium

Wann ist ein ökonomisches Gleichungssystem „vollständig"? Wir übernehmen fünf Kriterien, die gemeinsam eine präzise Definition liefern:

**Definition 1.1 (Strukturelle Vollständigkeit).** *Ein ökonomisches Gleichungssystem* $\dot{\mathbf{X}} = \mathbf{F}(\mathbf{X}) + \mathbf{G}(\mathbf{X})\boldsymbol{\xi}$ *ist strukturell vollständig, wenn es die folgenden fünf Bedingungen erfüllt:*

**(V1) Observable-Abdeckung.** Jede empirisch messbare ökonomische Größe (BIP, Inflation, Arbeitslosenquote, Gini-Koeffizient, Leistungsbilanz, Zinsspread, Handelsvolumen, etc.) ist als Funktion des Zustandsvektors $\mathbf{X}(t)$ darstellbar.

**(V2) Kausale Geschlossenheit.** Das System enthält keine unbestimmten endogenen Variablen — jede Variable, die im System auftritt und sich zeitlich ändert, wird durch eine Gleichung bestimmt. Exogene Variablen (Anfangsbedingungen, institutionelle Randbedingungen, stochastische Prozesse) sind explizit als solche benannt.

**(V3) Hadamard-Bedingungen.** Das System besitzt für gegebene Anfangsbedingungen $\mathbf{X}(0) \in \Omega$ eine Lösung (Existenz), diese ist eindeutig (zumindest fast sicher im stochastischen Fall), und sie hängt stetig von den Anfangsbedingungen ab (zumindest abseits von Kipppunkten).

**(V4) Konsistenz.** Die Erhaltungssätze (A1–A3) werden durch keine Gleichung verletzt. Identische Größen, die aus verschiedenen Gleichungen berechnet werden können, liefern dasselbe Ergebnis. Die Stock-Flow-Konsistenz gilt: jedes Guthaben ist jemandes Schuld.

**(V5) Reproduktion bekannter Modelle.** Jedes empirisch validierte Standardmodell entsteht als Grenzfall unter explizit benennbaren vereinfachenden Annahmen.

Die Bedingungen V1–V4 sind *interne* Konsistenzbedingungen. V5 ist eine *externe* Bedingung: Die Theorie muss alles erklären können, was die Einzelmodelle erklären — und darüber hinaus die Phänomene, die zwischen den Einzelmodellen liegen.

## 1.4 Was die Theorie leistet — und was nicht

Es ist wichtig, den Anspruch der Theorie präzise abzugrenzen, um Missverständnisse zu vermeiden:

**Was die Theorie leistet:**

- Sie vereinheitlicht die existierenden Modelle der Wachstumstheorie, Makroökonomik, Finanzökonomik, Handelstheorie, Informationsökonomik und Verhaltensökonomik zu einem einzigen konsistenten System.
- Sie identifiziert die *Annahmen*, unter denen jedes Einzelmodell gültig ist — und die Punkte, an denen diese Annahmen versagen.
- Sie beschreibt Phänomene, die an der Grenze zwischen Einzelmodellen liegen: Finanzkrisen als Zusammenspiel von Kreditdynamik (Geldtheorie), Herding (Verhaltensökonomik) und Informationsasymmetrie (Informationsökonomik).
- Sie erzeugt aus einem System konkret lösbare Probleme (optimale Bankenanzahl, Crashpuffer, Diffusionsgeschwindigkeiten), die kein Einzelmodell beantworten kann.

**Was die Theorie nicht leistet:**

- Sie sagt keine exogenen Schocks vorher (Naturkatastrophen, Pandemien, geopolitische Konflikte). Sie beschreibt die *Reaktion* des Systems auf solche Schocks, nicht deren Eintreten.
- Sie enthält keine universellen Parameterwerte. Die *Struktur* (welche Variablen an welche Gleichung gekoppelt sind) ist axiomatisch; die *Parameterwerte* (wie stark die Kopplungen sind) müssen empirisch kalibriert werden.
- Sie bestimmt nicht die *funktionale Form* der Nutzen-, Produktions- oder Herding-Funktionen. Sie legt deren *qualitative Eigenschaften* fest (Monotonie, Konkavität, Beschränktheit) und überlässt die Formwahl dem Anwender (Anhang C).
- Sie endogenisiert nicht die Modellwahl der Agenten (Reflexivität) — das bleibt eine offene Erweiterung (Kapitel 35).

In der Terminologie der Physik: Die Theorie liefert die *Feldgleichungen*, nicht die *Lösungen*. Die Feldgleichungen bestimmen die Struktur des Raums der möglichen ökonomischen Dynamiken. Die konkreten Lösungen — der Zeitpfad einer bestimmten Volkswirtschaft — hängen von den Anfangsbedingungen, Parameterwahlen und exogenen Einflüssen ab.

## 1.5 Abgrenzung zu bestehenden Ansätzen

### 1.5.1 DSGE-Modelle

Die Dynamic Stochastic General Equilibrium (DSGE) Modelle, die seit den 1980er Jahren den makroökonomischen Mainstream bilden, teilen mit unserer Theorie den Anspruch auf mikrofundierte Dynamik mit Unsicherheit. Die Unterschiede sind jedoch grundlegend:

| Eigenschaft | DSGE | Axiomatische Kontinuumsökonomik |
|-------------|------|-------------------------------|
| Agent | Repräsentativ (identisch) | Heterogen, verteilt in $(w, \theta, \mathcal{I})$ |
| Geld | Oft nicht modelliert; wenn, dann „Geld im Nutzen" | Endogene Kreditschöpfung (M.1) |
| Finanzmärkte | Abwesend oder stark stilisiert | Portfolio (III.2), Herding (V.3), Regime (VIII) |
| Information | Perfekt oder rationale Erwartungen | Endogenes Informationsfeld $\mathcal{I}(\mathbf{x},t)$ |
| Krisen | Exogene Schocks | Endogene Instabilität (Minsky, Fisher, Kaskaden) |
| Gleichgewicht | Stets Gleichgewicht (per Definition) | Gleichgewicht als Grenzfall; Ungleichgewicht ist der Regelfall |
| Psychologie | Rational (per Annahme) | Drei-Ebenen-Architektur: Rational + Psychologisch + Sozial |

Die zentrale Kritik an DSGE ist nicht, dass die Modelle *falsch* sind — sie sind Grenzfälle unseres Systems (repräsentativer Agent, perfekte Information, kein Herding) —, sondern dass sie die interessantesten Phänomene ausschließen: Finanzkrisen, Vermögensblasen, Informationskaskaden, endogene Ungleichheit. Unser System enthält DSGE als Spezialfall und geht darüber hinaus.

### 1.5.2 Agent-Based Models (ABM)

Agent-Based Models simulieren heterogene Agenten mit Verhaltensregeln und beobachten emergentes Systemverhalten. Sie teilen mit unserer Theorie die Betonung von Heterogenität und begrenzter Rationalität. Der Unterschied:

| Eigenschaft | ABM | Axiomatische Kontinuumsökonomik |
|-------------|-----|-------------------------------|
| Grundlage | Simulationsregeln | Axiome + Gleichungssystem |
| Analytik | Keine geschlossenen Lösungen | Steady States, Grenzfälle, Stabilitätsanalyse |
| Reproduzierbarkeit | Abhängig von Implementation | Gleichungssystem ist eindeutig |
| Spezialfälle | Nicht systematisch ableitbar | Grigorianischer Katalog aller Grenzfälle |
| Konsistenz | Nicht garantiert (ad-hoc-Regeln) | SFC-Konsistenz, Erhaltungssätze |

ABM sind numerische Laboratorien; unsere Theorie ist ein analytischer Rahmen. Beide sind komplementär: Das Gleichungssystem liefert die Struktur, ABM können die konkreten Dynamiken für spezifische Parametrisierungen simulieren.

### 1.5.3 Post-Keynesianische SFC-Modelle

Die Stock-Flow-Consistent Models von Godley und Lavoie (2007) teilen mit unserer Theorie die Insistenz auf Bilanzkonsistenz und endogener Geldschöpfung. Unser System erweitert den SFC-Rahmen um:

- Räumliche Struktur und Handelsströme (F.1, F.2)
- Endogene Information als Feld ($\mathcal{I}$)
- Drei-Ebenen-Verhaltensarchitektur (V.1–V.3, L.1–L.4)
- Schwellenwertdynamik und Regime-Switching (Schw.1, RS.1)
- Formale Vollständigkeit (Hadamard-Bedingungen)

Die SFC-Bilanzmatrix (Kapitel 12) ist ein integraler Bestandteil unseres Systems, nicht eine separate Konsistenzprüfung.

## 1.6 Aufbau der Monographie

Die Monographie folgt einer strikten Logik: von den Axiomen über die allgemeinen Gleichungen zum Systemschluss, dann zu den Spezialfällen, Märkten, Optimierungsproblemen und schließlich zur empirischen Validierung.

**Teil I — Grundlagen** (Kapitel 1–3) formuliert die zehn Axiome, die sechs Güterklassen, die fünf Agentenklassen und die Netzwerkstruktur. Hier wird festgelegt, *was wir voraussetzen*.

**Teil II — Das allgemeine Gleichungssystem** (Kapitel 4–10) leitet aus den Axiomen 75 Gleichungen ab — jede in ihrer allgemeinsten Form, ohne eingesetzte Funktionalformen. Hier wird festgelegt, *was aus den Axiomen folgt*.

**Teil III — Systemschluss** (Kapitel 11–14) beweist, dass das System vollständig, konsistent und lösbar ist: Freiheitsgrad-Zählung, Closure-Tabelle, Stock-Flow-Konsistenz, Kausalstruktur, Hadamard-Bedingungen. Hier wird festgelegt, *warum 75 Gleichungen genügen*.

**Teil IV — Klassische Modelle als Grenzfälle** (Kapitel 15–23) zeigt, dass Solow, Ramsey, Arrow-Debreu, IS-LM, CAPM, Mundell-Fleming, Minsky, Fisher, Piketty, Stigler, Akerlof, Grossman-Stiglitz, Prospect Theory und Granovetter als Spezialfälle des Systems entstehen. Jeder Grenzübergang wird explizit: Annahmen benennen, Gleichungen reduzieren, Ergebnis mit Original vergleichen. Hier wird festgelegt, *was das System enthält*.

**Teil V — Spezifische Märkte** (Kapitel 24–27) wendet das System auf konkrete Markttypen an: Arbeit, Immobilien und Rohstoffe, Kredit und Versicherung, Plattformen und digitale Ökonomie.

**Teil VI — Optimierung und konkrete Probleme** (Kapitel 28–30) stellt statische Einperioden-Optimierung der vollen dynamischen Lösung im System gegenüber und löst konkrete Fragen: optimale Bankenanzahl, Crashpuffer, Technologiediffusion.

**Teil VII — Validierung** (Kapitel 31–33) testet das System numerisch: Weltsimulation mit 30 Ländern, Krisensimulationen, empirische Proxy-Tests.

**Teil VIII — Grenzen und Ausblick** (Kapitel 34–35) benennt, was die Theorie nicht kann, und formuliert das Forschungsprogramm.

**Anhänge** A–F enthalten die vollständige Gleichungsliste, Symboltabelle, den Baukasten funktionaler Formen, Simulationscode, Datenquellen und den formalen Hadamard-Beweis.

## 1.7 Notation

Die durchgängig verwendete Notation:

### Zustandsvariablen

| Symbol | Bedeutung | Raum |
|--------|-----------|------|
| $w_i(t)$ | Vermögen von Agent $i$ | $\mathbb{R}$ |
| $c_i(t)$ | Konsum von Agent $i$ | $\mathbb{R}_{\geq 0}$ |
| $L_i(t)$ | Arbeitsangebot von Agent $i$ | $[0, L_{\max}]$ |
| $\theta_{ik}(t)$ | Bestand an Gut $k$ von Agent $i$ | $\mathbb{R}_{\geq 0}$ |
| $p_k(t)$ | Preis von Gut $k$ | $\mathbb{R}_{> 0}$ |
| $\mathcal{I}_k(\mathbf{x}, t)$ | Informationsstand über Gut $k$ | $[0, 1]$ |
| $n_k(\mathbf{x}, t)$ | Güterbestandsdichte | $\mathbb{R}_{\geq 0}$ |
| $m(\mathbf{x}, t)$ | Gelddichte | $\mathbb{R}_{\geq 0}$ |
| $N(t)$ | Bevölkerung | $\mathbb{N}$ (bzw. $\mathbb{R}_{> 0}$ im Kontinuum) |
| $K(t)$ | Aggregierter Kapitalstock | $\mathbb{R}_{\geq 0}$ |

### Flüsse

| Symbol | Bedeutung |
|--------|-----------|
| $\vec{j}_{n_k}$ | Güterstrom |
| $\vec{j}_m$ | Geldstrom |
| $\vec{j}_w$ | Vermögensstrom |
| $Y$ | Aggregiertes Einkommen (BIP) |
| $C$ | Aggregierter Konsum |

### Parameter

| Symbol | Bedeutung | Typ |
|--------|-----------|-----|
| $\gamma_i$ | Risikoaversion | axiomatisch: $> 0$ |
| $\beta_i$ | Zeitpräferenzrate | axiomatisch: $> 0$ |
| $\delta_k$ | Abschreibungsrate | güterklassenspezifisch |
| $\alpha_H$ | Herding-Intensität | endogen (VI.4) |
| $D_\mathcal{I}$ | Informationsdiffusionskonstante | physisch |
| $\omega$ | Informationszerfallsrate | physisch |

### Funktionale Objekte (axiomatische Eigenschaften, *nicht* konkrete Formen)

| Symbol | Bedeutung | Axiomatische Eigenschaft | Konkrete Wahlen → Anhang C |
|--------|-----------|-------------------------|---------------------------|
| $u(c)$ | Nutzenfunktion | $u' > 0$, $u'' < 0$ | CRRA, CARA, Log, Epstein-Zin |
| $F(K, L, \mathcal{I})$ | Produktionsfunktion | $F_K > 0$, $F_{KK} < 0$, Inada | Cobb-Douglas, CES, Leontief |
| $\phi(L)$ | Arbeitsleid | $\phi' > 0$, $\phi'' > 0$ | Isoelastisch, quadratisch |
| $\omega_{k,i}(\mathcal{I})$ | Informationsgewicht | $\sum_k \omega_k = 1$, $\partial\omega/\partial\mathcal{I} > 0$ | Softmax, Probit, Linear |
| $\mathcal{C}_k(\mathcal{I})$ | Informationskosten | $\mathcal{C}' > 0$, $\mathcal{C}'' > 0$ | Quadratisch, exponentiell |
| $\Phi(x)$ | Herding-Funktion | $\Phi(0) = 0$, $\Phi' > 0$, $|\Phi| \leq \Phi_{\max}$ | Linear, Sigmoid, asymmetrisch |
| $\Psi(c, c^*)$ | Psychologische Verzerrung | $\Psi(c^*, c^*) = 0$, Verlustasymmetrie | Linear, Prospect Theory |

### Operatoren und Konventionen

| Notation | Bedeutung |
|----------|-----------|
| $\dot{x} \equiv dx/dt$ | Zeitableitung |
| $\nabla$ | Räumlicher Gradient |
| $\nabla^2$ | Laplace-Operator |
| $\xi_i(t)$ | Weißes Rauschen (Wiener-Prozess) |
| $\widetilde{\mathcal{N}}(dt, d\ell)$ | Kompensierter Poisson-Prozess |
| $\mathcal{L}$ (kalligraphisch) | Kreditvolumen (Loans) — **nicht** Arbeit $L$ |
| $r$ (ohne Index) | Referenzzins (Leitzins-äquivalent) |
| $r_K, r_\mathcal{L}, r_D$ | Kapitalrendite, Kreditzins, Depositzins |
| $A_{ij}^{(\ell)}$ | Netzwerkgewicht (Schicht $\ell$) |
| $\sigma(\cdot)$ | Logistische Sigmoidfunktion $1/(1+e^{-x})$ |
| $\mathbb{1}[\cdot]$ | Indikatorfunktion |

### Konventionen

- Subskript $i$: Agent. Subskript $k$: Gut. Superskript $(\ell)$: Netzwerkschicht. Superskript $(\alpha)$: Güterklasse.
- Kalligraphische Buchstaben ($\mathcal{A}, \mathcal{B}, \mathcal{K}, \mathcal{L}, \mathcal{I}$) bezeichnen Mengen oder spezifische Variablen (Agentenmenge, Banken, Güterklasse, Kredit, Information).
- Fettdruck ($\mathbf{X}, \mathbf{F}$) bezeichnet Vektoren und vektorwertige Funktionen.
- Griechische Buchstaben ($\alpha, \beta, \gamma, \delta$) sind stets Parameter, nie Variablen.

---

*Ende von Kapitel 1. Im folgenden Kapitel formulieren wir die zehn Axiome, auf denen das gesamte Gleichungssystem ruht.*

---

# Kapitel 2: Die zehn Axiome

---

Dieses Kapitel enthält die vollständige axiomatische Basis der Theorie. Alles, was in den folgenden Kapiteln an Gleichungen abgeleitet wird, folgt aus diesen zehn Aussagen — und aus nichts anderem. Das Kapitel ist daher das Fundament: Wer die Axiome akzeptiert, muss die Konsequenzen akzeptieren; wer ein Axiom ablehnt, kann präzise benennen, an welcher Stelle die Theorie für ihn nicht gilt.

Die Axiome sind in vier Gruppen geordnet:

| Gruppe | Axiome | Charakter |
|--------|--------|-----------|
| **Erhaltung** | A1, A2, A3 | Buchhaltungsidentitäten — *logisch notwendig* |
| **Flüsse** | A4 | Konstitutivgesetz — *empirisch fundiert* |
| **Verhalten** | A5, A6, A7 | Verhaltenspostulate — *falsifizierbar* |
| **Struktur** | A8, A9, A10 | Biologische und informationelle Randbedingungen |

Die Erhaltungsaxiome A1–A3 sind im strengen Sinne keine *Annahmen*, sondern logische Notwendigkeiten: Wenn ein Agent Vermögen verliert, muss ein anderer es gewinnen. Sie drücken aus, dass die Ökonomie ein geschlossenes Buchführungssystem ist. Die Verhaltensaxiome A5–A7 sind dagegen substanzielle Behauptungen über menschliches Handeln. Sie sind falsifizierbar — es ist denkbar, dass Agenten *nicht* nutzenmaximierend handeln (A5), *nicht* von ihren Peers beeinflusst werden (A6) oder *nicht* adaptiv lernen (A7). Die Theorie behauptet, dass diese Axiome eine hinreichend genaue Beschreibung menschlichen Wirtschaftsverhaltens liefern.

Jedes Axiom wird in drei Schritten präsentiert:

1. **Verbale Formulierung** — ein Satz, der die Aussage in natürlicher Sprache fasst.
2. **Formale Kurzform** — die kompakteste symbolische Darstellung.
3. **Erläuterung** — Motivation, Implikationen, Grenzen.

---

## 2.1 A1 — Vermögenserhaltung

> **Axiom A1.** *Das Vermögen eines Agenten ändert sich ausschließlich durch Einkommen, Konsum, Bewertungsänderungen seiner Bestände und Zinserträge. Vermögen kann weder entstehen noch verschwinden, ohne dass eine dieser vier Ursachen vorliegt.*

**Kurzform:**

$$\frac{dw_i}{dt} = y_i - c_i + \sum_k \theta_{ik}\,\dot{p}_k + r\,b_i$$

**Erläuterung.**

A1 ist die individuelle Bilanzidentität. Sie zerlegt die Vermögensänderung in vier Komponenten:

| Term | Bedeutung | Vorzeichen |
|------|-----------|------------|
| $y_i$ | Einkommen (Arbeit + Kapitalertrag + Transfers) | $+$ |
| $c_i$ | Konsum (Ausgaben für Güter und Dienstleistungen) | $-$ |
| $\sum_k \theta_{ik}\,\dot{p}_k$ | Bewertungsgewinne/-verluste der Bestände | $\pm$ |
| $r\,b_i$ | Nettozinsertrag auf Finanzpositionen | $\pm$ |

Die Gleichung ist eine *Identität*, keine Verhaltensannahme — sie besagt lediglich, dass Vermögen buchhalterisch konsistent geführt wird. Ihre Kraft liegt darin, dass sie *alles andere ausschließt*: Es gibt keine fünfte Quelle von Vermögensänderungen. Insbesondere schließt A1 aus, dass Vermögen durch Informationsgewinne direkt entsteht (Information ändert $p_k$ und damit *indirekt* $w_i$ über den Bewertungsterm, aber sie erzeugt kein Einkommen ohne Transaktion).

**Aggregation.** Summation über alle Agenten $i \in \mathcal{A}$ liefert die aggregierte Vermögenserhaltung:

$$\frac{dW}{dt} = Y - C$$

Bewertungsgewinne und Zinsen heben sich in der Summe auf (Nullsumme zwischen Agenten), sodass das Gesamtvermögen nur durch die Differenz aus Gesamteinkommen $Y$ und Gesamtkonsum $C$ wächst — das aggregierte Sparen.

**Status.** A1 ist eine logische Notwendigkeit in jedem konsistenten Buchführungssystem. Kein ökonomisches Modell, das dieses Axiom verletzt, kann konsistente Vorhersagen über Vermögensdynamik liefern.

---

## 2.2 A2 — Gütererhaltung

> **Axiom A2.** *Für jede Güterklasse $k$ gilt eine Kontinuitätsgleichung: Die zeitliche Änderung des lokalen Bestands plus der Abfluss durch Handel gleicht der Differenz aus Produktion und Vernichtung.*

**Kurzform:**

$$\frac{\partial n_k}{\partial t} + \nabla \cdot \vec{j}_{n_k} = q_k - d_k$$

**Erläuterung.**

A2 ist das ökonomische Analogon zur physikalischen Kontinuitätsgleichung. Sie besagt: Güter verschwinden nicht einfach — wenn an einem Ort der Bestand sinkt, müssen die Güter entweder abgeflossen ($\nabla \cdot \vec{j} > 0$), konsumiert ($d_k > 0$) oder abgeschrieben worden sein. Umgekehrt können Güter nur durch Produktion ($q_k > 0$) oder Zufluss entstehen.

Die Gleichung gilt *für jede Güterklasse separat* — das ist wesentlich. Maschinen ($\mathcal{K}_1$) und Nahrung ($\mathcal{K}_3$) unterliegen verschiedenen Vernichtungsraten $d_k$: Maschinen schreiben langsam ab ($d_k = \delta_k n_k$), Nahrung wird beim Konsum sofort vernichtet ($d_k = c_k$). Die Güterklassenstruktur (A9) differenziert die Dynamik.

**Wichtiger Unterschied zur physikalischen Erhaltung:** In der Physik ist die Kontinuitätsgleichung eine *strikte* Erhaltung — Energie kann nicht erzeugt oder vernichtet werden ($q_k = d_k = 0$). In der Ökonomie haben wir echte *Quellen* (Produktion) und *Senken* (Konsum, Abschreibung). A2 ist daher eine *Bilanzgleichung*, keine Erhaltung im physikalischen Sinne. Die strikte Erhaltung gilt nur für $\mathcal{K}_2$ (Land, Gold — Bestand ändert sich nur durch Handel, nicht durch Produktion oder Zerfall).

**Status.** Logische Notwendigkeit. Jede Bestandsänderung muss einem der vier Kanäle (Produktion, Konsum, Abschreibung, Handel) zugeordnet werden können.

---

## 2.3 A3 — Gelderhaltung

> **Axiom A3.** *Die Geldmenge ändert sich ausschließlich durch Geldschöpfung (Zentralbank, Geschäftsbanken) und Geldvernichtung (Steuertilgung). Geld kann nicht physisch erzeugt oder vernichtet werden, außer durch diese institutionellen Kanäle.*

**Kurzform:**

$$\frac{\partial m}{\partial t} + \nabla \cdot \vec{j}_m = g - \tau$$

**Erläuterung.**

A3 unterscheidet sich von A2 in einem wesentlichen Punkt: Geld ($\mathcal{K}_5$) wird nicht *produziert* wie Güter, sondern *geschöpft* — durch Kreditvergabe der Geschäftsbanken und durch Offenmarktoperationen der Zentralbank. Der Term $g$ fasst alle Geldschöpfungsquellen zusammen, $\tau$ alle Vernichtungskanäle (primär: Steuertilgung, Kreditrückzahlung).

Die fundamentale Eigenschaft von $\mathcal{K}_5$ ist die *Bilanzsymmetrie*: Jede Geldschöpfung erzeugt simultan ein Guthaben und eine Forderung in gleicher Höhe. $\Delta M = \Delta \mathcal{L}$ — das neu geschöpfte Geld ist immer zugleich jemandes Schuld. Daraus folgt: Die *Nettosumme* aller monetären Positionen ist null:

$$\sum_{i \in \mathcal{A}} m_i^{\text{netto}} = 0$$

Dies ist die fundamentale SFC-Bedingung (Stock-Flow-Consistency, Godley & Lavoie 2007), die in unserem System automatisch durch A3 garantiert wird.

**Status.** Logische Notwendigkeit plus institutionelle Festlegung: Welche Akteure Geld schöpfen dürfen, ist eine institutionelle Randbedingung, keine Naturgesetzlichkeit. A3 beschreibt die Struktur der Geldschöpfung, nicht ihre konkrete Ausgestaltung.

---

## 2.4 A4 — Gradientengetriebene Flüsse

> **Axiom A4.** *Alle ökonomischen Ströme — Güter, Kapital, Geld, Information — fließen entlang des negativen Gradienten eines zugehörigen Potentials. Güter fließen dorthin, wo ihr effektiver Preis höher ist; Kapital dorthin, wo die erwartete Rendite höher ist; Information dorthin, wo sie seltener ist.*

**Kurzform:**

$$\vec{j} = -D\,\nabla\mu^{\text{eff}}$$

**Erläuterung.**

A4 ist ein Konstitutivgesetz — es beschreibt, *wie* sich Ströme zu Potentialdifferenzen verhalten. Die Analogie zur Physik ist direkt: Wärme fließt entlang des Temperaturgradienten (Fourier), Strom entlang des Spannungsgradienten (Ohm), Teilchen entlang des Konzentrationsgradienten (Fick). In der Ökonomie fließen Güter und Kapital dorthin, wo sie den höchsten Ertrag erwarten lassen.

Das entscheidende Detail ist das Wort *effektiv*: Der Gradient wird nicht auf dem *objektiven* Preis berechnet, sondern auf dem *effektiven Potential* $\mu^{\text{eff}}$, das den objektiven Preis, die Herding-Verzerrung und die Transaktionskosten zusammenfasst (Kapitel 5, Gleichung F.2). Agenten handeln nicht aufgrund der wahren Rendite, sondern aufgrund der *wahrgenommenen* Rendite. Im Grenzfall perfekter Information ($\mathcal{I} \to \infty$) und ohne Herding ($\alpha_H = 0$) reduziert sich $\mu^{\text{eff}}$ auf den objektiven Preis, und A4 wird zum neoklassischen Arbitrageprinzip.

| Flusstyp | Potential $\mu^{\text{eff}}$ | Diffusionskonstante $D$ |
|----------|------------------------------|------------------------|
| Güterstrom | Effektiver Güterpreis | $D_k$ (Handelsfriktion) |
| Kapitalstrom | Erwartete risikoadjustierte Rendite | $D_K$ (Kapitalmarktfriktion) |
| Geldstrom | Zinsdifferenz + Inflationserwartung | $D_m$ (Zahlungsinfrastruktur) |
| Informationsfluss | Informationskonzentration $\mathcal{I}$ | $D_\mathcal{I}$ (Kommunikationsinfrastruktur) |

Die Diffusionskonstanten $D$ sind *physische* Parameter: Sie hängen von der Infrastruktur ab (Straßennetz für Güter, Glasfaser für Information, Zahlungssysteme für Geld). Ihre Größenordnungen unterscheiden sich erheblich — die Information-Diffusion im Internet ist Größenordnungen schneller als die physische Güterdiffusion.

**A4 als empirische Hypothese.** Anders als A1–A3 ist A4 keine logische Notwendigkeit, sondern eine empirische Behauptung: Es ist *denkbar*, dass Ströme nicht dem Gradienten folgen (z.B. bei administrativen Handelsbarrieren, Kapitalverkehrskontrollen). Solche Blockaden modellieren wir als Modifikationen von $D$ (regionale Barrieren setzen $D \to 0$ lokal), nicht als Verletzung von A4.

---

## 2.5 A5 — Nutzenmaximierung

> **Axiom A5.** *Jeder Agent $i$ maximiert den erwarteten diskontierten Lebensnutzen über seine Entscheidungsvariablen (Konsum, Arbeitsangebot, Portfolio). Der Nutzen hängt vom Konsum, vom Arbeitsangebot und vom Informationsstand ab.*

**Kurzform:**

$$\max_{c_i,\, L_i,\, \theta_i} \;\mathbb{E}\!\left[\int_0^\infty e^{-\beta_i t}\, u_i\!\left(c_i,\, L_i,\, \theta_i,\, \mathcal{I}_i\right) dt\right]$$

unter der Budgetrestriktion A1.

**Erläuterung.**

A5 ist das zentrale Verhaltensaxiom. Es besagt, dass Agenten *zielgerichtet* handeln — sie versuchen, ihre Situation nach einem konsistenten Kriterium (dem Nutzen $u_i$) zu verbessern. Die Konsequenz ist mächtig: Aus A5 folgen über die Euler-Lagrange-Gleichungen des zugehörigen Variationsproblems die gesamte Konsumplanung, Portfolioallokation, Arbeitsangebotsentscheidung und unternehmerische Risikowahl.

Drei Aspekte verdienen besondere Betonung:

**1. Der Nutzen hängt von $\mathcal{I}_i$ ab.** Dies unterscheidet unser A5 von der neoklassischen Version. In der Standardtheorie ist $u(c)$ — der Agent weiß, was er konsumiert, und bewertet es unabhängig von seiner Information. In unserer Theorie ist $u(c, \mathcal{I})$ — der *wahrgenommene Nutzen* hängt davon ab, wie viel der Agent über die verfügbaren Güter weiß. Ein Agent, der nur drei von hundert Gütern kennt ($\mathcal{I}$ klein), optimiert über eine eingeschränkte Menge und trifft im Allgemeinen suboptimale Entscheidungen. Die Informationsabhängigkeit erzeugt *endogene begrenzte Rationalität*: Nicht weil Agenten irrational wären, sondern weil sie unvollständig informiert sind.

**2. Die Nutzenfunktion ist nicht spezifiziert.** A5 postuliert die *Existenz* einer Nutzenfunktion $u$ mit den axiomatischen Eigenschaften $u' > 0$ (mehr ist besser) und $u'' < 0$ (abnehmender Grenznutzen). Die *konkrete Form* — ob CRRA, CARA, logarithmisch, Epstein-Zin — ist eine Modellierungswahl (Anhang C). Alle qualitativen Ergebnisse der Theorie (Spezialfälle, Stabilität, kausale Struktur) hängen nur von den axiomatischen Eigenschaften ab.

**3. A5 ist das rationale Grundgerüst — aber nicht die ganze Geschichte.** Die Drei-Ebenen-Architektur (Kapitel 6) erweitert A5 um psychologische Verzerrungen (Ebene 2) und soziale Kopplung (Ebene 3). Die Optimierung aus A5 liefert den *rationalen Kern* der Entscheidung; die Ebenen 2 und 3 (aus A6 und den Axiomen über Psychologie) modifizieren das Ergebnis. A5 allein beschreibt den homo oeconomicus; das vollständige System beschreibt den homo sapiens.

**A5 als falsifizierbare Hypothese.** Es ist denkbar, dass manche Agenten *nicht* nutzenmaximierend handeln (z.B. gewohnheitsbasiertes Kaufverhalten ohne jede Optimierung). In einem solchen Fall wäre $c_i = c_i^{\text{Gewohnheit}}$ — eine feste Regel anstelle der Euler-Gleichung. Empirisch zeigt sich, dass nutzenmaximierendes Verhalten eine gute Approximation für die *meisten* Entscheidungen ist, mit systematischen Abweichungen, die durch Ebene 2 und 3 erfasst werden.

---

## 2.6 A6 — Soziale Kopplung

> **Axiom A6.** *Entscheidungen jedes Agenten werden durch die beobachtbaren Entscheidungen seiner Nachbarn im sozialen Netzwerk beeinflusst. Die Stärke der Beeinflussung hängt von der Netzwerkposition, dem Informationsstand und dem aktuellen Marktregime ab.*

**Kurzform:**

$$\dot{x}_i \ni \sum_j A_{ij}^{\text{eff}}\, \Phi(x_j - x_i)$$

für jede Entscheidungsvariable $x \in \{c, L, \theta\}$, wobei $\Phi$ die verallgemeinerte Herding-Funktion ist.

**Erläuterung.**

A6 bricht mit der neoklassischen Annahme isolierter Agenten. In der Standardtheorie hängt die Konsumentscheidung von Agent $i$ nur von seinen eigenen Präferenzen und seinem Budget ab. A6 postuliert dagegen: Der Konsum von Agent $i$ wird *auch* vom Konsum seiner Nachbarn $j$ beeinflusst, gewichtet mit der Netzwerkverbindung $A_{ij}^{\text{eff}}$.

Die Herding-Funktion $\Phi$ hat die folgenden axiomatischen Eigenschaften:

| Eigenschaft | Formal | Interpretation |
|-------------|--------|----------------|
| Monotonie | $\Phi'(x) > 0$ | Höherer Nachbarkonsum → stärkerer Nachahmungsimpuls |
| Nullpunkt | $\Phi(0) = 0$ | Identischer Konsum → kein Impuls |
| Beschränktheit | $|\Phi(x)| \leq \Phi_{\max}$ | Nachahmung hat eine Obergrenze |
| Asymmetrie möglich | $\Phi(x) \neq -\Phi(-x)$ | Aufwärts-Herding (Blasen) kann stärker sein als Abwärts |

Die konkrete Form von $\Phi$ — linear, sigmoïd, asymmetrisch — ist eine Modellierungswahl (Anhang C). Die axiomatischen Eigenschaften genügen, um das qualitative Verhalten festzulegen: Herding erzeugt *positive Rückkopplung* (steigende Preise → mehr Käufe → steigende Preise) und kann — über kritische Schwellenwerte hinaus — zu Blasen, Kaskaden und Regimewechseln führen.

**A6 erfasst mehrere empirisch dokumentierte Phänomene:**

- **Statuskonsum** (Veblen 1899): Konsum steigt, weil die Nachbarn mehr konsumieren.
- **Bankruns** (Diamond & Dybvig 1983): Einlagenabzug, weil andere abziehen.
- **Blasenbildung** (Kindleberger 1978): Investition in ein Asset, weil andere investieren.
- **Technologieadoption** (Rogers 1962): Übernahme einer Technologie, weil das Netzwerk sie übernimmt.

All diese Phänomene folgen im System aus *einem einzigen Term* — dem Herding-Term in A6. Die verschiedenen Manifestationen ergeben sich je nachdem, welche Entscheidungsvariable $x$ betroffen ist (Konsum, Portfolio, Arbeit, Adoptionsentscheidung).

**A6 als falsifizierbare Hypothese.** Wenn $A_{ij} = 0$ für alle $i, j$ (kein Netzwerk) oder $\Phi \equiv 0$ (keine Nachahmung), dann sind Agenten isoliert, und A6 ist trivial erfüllt. Der Arrow-Debreu-Grenzfall (Kapitel 16) entsteht genau unter dieser Annahme. Empirisch ist die Hypothese der sozialen Kopplung gut belegt — von Banerjee (1992) über Bikhchandani, Hirshleifer & Welch (1992) bis zu modernen Netzwerkstudien (Jackson 2008).

---

## 2.7 A7 — Adaptive Erwartungen

> **Axiom A7.** *Agenten bilden Erwartungen über zukünftige Preise als gewichtete Kombination aus vier Quellen: Beobachtung des aktuellen Preises, Fundamentalwert-Schätzung, Trendextrapolation und idiosynkratischem Rauschen.*

**Kurzform:**

$$\frac{d\hat{p}_{ik}}{dt} = \omega_a\!\left(p_k - \hat{p}_{ik}\right) + \omega_f\!\left(p_k^* - \hat{p}_{ik}\right) + \alpha_t\,\dot{p}_k + \sigma_{\hat{p}}\,\xi_i$$

**Erläuterung.**

A7 beschreibt, wie Agenten die Zukunft einschätzen. Die vier Terme:

| Term | Bezeichnung | Interpretation |
|------|-------------|----------------|
| $\omega_a(p_k - \hat{p}_{ik})$ | Adaptive Korrektur | Agent passt Erwartung an beobachteten Preis an |
| $\omega_f(p_k^* - \hat{p}_{ik})$ | Fundamentale Korrektur | Agent glaubt an einen Fundamentalwert $p_k^*$ |
| $\alpha_t\,\dot{p}_k$ | Trendextrapolation | Agent extrapoliert den aktuellen Trend |
| $\sigma_{\hat{p}}\,\xi_i$ | Idiosynkratisches Rauschen | Heterogene Einschätzungen |

A7 ist eine Verallgemeinerung, die drei Grenzfälle als Spezialfälle enthält:

| Spezialfall | Bedingung | Ergebnis |
|-------------|-----------|----------|
| Perfekte Voraussicht | $\omega_a = 1$, $\omega_f = \alpha_t = \sigma = 0$ | $\hat{p} = p$ (Agent kennt den Preis exakt) |
| Rationale Erwartungen | $\omega_f = 1$, Rest $= 0$ | $\hat{p} = p^* = \mathbb{E}[p \mid \mathcal{I}]$ (unverzerrte Prognose) |
| Chartist/Trendfolger | $\alpha_t \gg \omega_a, \omega_f$ | $\hat{p}$ folgt dem Trend (Momentumstrategie) |

Die relative Gewichtung der vier Quellen ist *selbst endogen* — sie hängt vom Marktzustand ab. In ruhigen Phasen dominiert die fundamentale Korrektur ($\omega_f$ groß); in Blasenphasen dominiert die Trendextrapolation ($\alpha_t$ steigt); in Krisenzeiten dominiert die adaptive Korrektur ($\omega_a$ groß, schnelle Anpassung an neue Realitäten). Diese Zustandsabhängigkeit der Erwartungsgewichte wird durch die endogenen Verhaltensparameter (VI.1–VI.9, Kapitel 6) modelliert.

**A7 vs. Rationale Erwartungen.** Die Hypothese rationaler Erwartungen (Muth 1961, Lucas 1972) ist der Spezialfall $\omega_f = 1$, Rest $= 0$ — Agenten kennen das Modell und bilden unverzerrte Prognosen. A7 schließt dies als Grenzfall ein, behauptet aber, dass der allgemeinere Fall (adaptive + fundamentale + Trend-Komponente) empirisch adäquater ist. Insbesondere erzeugt die Trendextrapolation ($\alpha_t > 0$) positive Rückkopplung: steigende Preise → steigende Erwartungen → steigende Nachfrage → steigende Preise. In Kombination mit Herding (A6) ist dies der Mechanismus der Blasenbildung.

---

## 2.8 A8 — Populationsrückkopplung

> **Axiom A8.** *Die Bevölkerungsdynamik folgt einer logistischen Gleichung mit endogener Tragfähigkeit: Geburts- und Sterberaten sind Funktionen des Pro-Kopf-Vermögens, und die Tragfähigkeit hängt von Technologie, Ressourcen und Umweltbelastung ab.*

**Kurzform:**

$$\dot{N} = r_N\, N\!\left(1 - \frac{N}{\kappa(t)}\right) + M_{\text{netto}}$$

mit endogener Tragfähigkeit $\kappa = \kappa(A, R, E)$.

**Erläuterung.**

A8 koppelt die Ökonomie an die Biologie. Die logistische Gleichung beschreibt das fundamentale Muster: Bevölkerung wächst exponentiell, solange Ressourcen reichlich vorhanden sind ($N \ll \kappa$), und stabilisiert sich, wenn die Tragfähigkeitsgrenze erreicht wird ($N \to \kappa$).

Die Tragfähigkeit $\kappa$ ist *nicht* konstant, sondern hängt von drei Systemvariablen ab:

| Variable | Effekt auf $\kappa$ | Mechanismus |
|----------|---------------------|-------------|
| Technologie $A(t)$ | $\kappa \uparrow$ | Höhere Produktivität erlaubt größere Population |
| Ressourcen $R(t)$ | $\kappa \uparrow$ bei $R \uparrow$ | Mehr Nahrung, Energie, Wasser |
| Emissionen $E(t)$ | $\kappa \downarrow$ bei $E \uparrow$ | Umweltverschmutzung reduziert Lebensqualität |

Zusätzlich enthält A8 einen Migrationsterm $M_{\text{netto}}$, der regionale Bevölkerungsänderungen durch Zu- und Abwanderung erfasst. Migration ist im System über die Schwellenwertdynamik (Kapitel 10) mit der Lohndifferenz und den Informationskosten gekoppelt.

**A8 und der demographische Übergang.** Die Geburtenrate $b$ ist eine fallende Funktion des Pro-Kopf-Vermögens (Fertilität sinkt mit steigendem Wohlstand — beobachtet in allen Industrieländern). Die Sterberate $d$ ist ebenfalls fallend (bessere Medizin, Ernährung). Der *Nettoeffekt* ist der demographische Übergang: Erst wächst $N$ (weil $d$ schneller sinkt als $b$), dann stabilisiert sich $N$ (weil $b$ schließlich unter $d$ fällt).

**Status.** A8 ist eine empirisch gut belegte Hypothese. Die logistische Grundstruktur ist in Ökologie (Verhulst 1838) und Demographie (Lotka-Volterra) Standard. Die Endogenisierung der Tragfähigkeit ($\kappa = \kappa(A, R, E)$) ist eine Erweiterung, die die Rückkopplung zwischen Ökonomie und physischer Umwelt erfasst.

---

## 2.9 A9 — Güterdiversität

> **Axiom A9.** *Die Menge aller Güter $\mathcal{K}$ ist in sechs disjunkte Klassen partitioniert, die sich in Rivalität, Ausschließbarkeit und Zerfallsrate unterscheiden. Jede Klasse unterliegt einer eigenen Dynamik.*

**Kurzform:**

$$\mathcal{K} = \mathcal{K}_1 \sqcup \mathcal{K}_2 \sqcup \mathcal{K}_3 \sqcup \mathcal{K}_4 \sqcup \mathcal{K}_5 \sqcup \mathcal{K}_6$$

**Erläuterung.**

A9 kodifiziert die Einsicht, dass nicht alle Güter gleich sind. Eine Maschine ($\mathcal{K}_1$) verliert mit der Zeit an Wert (Abschreibung), Gold ($\mathcal{K}_2$) nicht. Nahrung ($\mathcal{K}_3$) wird beim Konsum vernichtet, Software ($\mathcal{K}_4$) nicht. Geld ($\mathcal{K}_5$) wird durch Kreditschöpfung erzeugt; Information ($\mathcal{K}_6$) breitet sich räumlich aus und zerfällt.

Eine Theorie, die alle Güter gleich behandelt — wie es die meisten Makromodelle mit „dem einen Gut" tun — kann weder Informationsausbreitung noch Kreditdynamik noch den Unterschied zwischen Immobilien und Nahrung korrekt beschreiben.

Die sechs Klassen mit ihren formalen Signaturen werden in Kapitel 3 im Detail dargestellt. A9 postuliert hier nur die *Existenz* der Partition und die Tatsache, dass *jede Klasse eine eigene Dynamik hat*.

**Status.** A9 ist eine empirische Beobachtung, keine logische Notwendigkeit — man *könnte* eine Theorie mit einem einzigen homogenen Gut formulieren (das tut Solow). Aber eine solche Theorie kann die Phänomene der Informationsökonomie, der Finanzmarktdynamik und der digitalen Ökonomie nicht erfassen. A9 ist der Preis für Allgemeinheit.

---

## 2.10 A10 — Informationskosten

> **Axiom A10.** *Information über ein Gut $k$ zu erlangen erfordert Ressourcen. Die Kosten sind positiv, steigend und konvex: Die ersten Informationen sind billig (leicht zu bekommen), die letzten teuer (tiefes Spezialwissen).*

**Kurzform:**

$$\mathcal{C}_k(\mathcal{I}_k): \quad \mathcal{C}_k > 0, \quad \mathcal{C}_k' > 0, \quad \mathcal{C}_k'' > 0$$

**Erläuterung.**

A10 ist die Grundlage der gesamten Informationsökonomik innerhalb unseres Systems. Das Axiom postuliert drei Eigenschaften:

1. **Positivität** ($\mathcal{C} > 0$): Information ist nie kostenlos. Selbst die einfachste Recherche erfordert Zeit, die einen Opportunitätskostenwert hat. Dies ist die Grundlage von Stiglers (1961) Suchkostentheorie.

2. **Monotonie** ($\mathcal{C}' > 0$): Mehr Information zu beschaffen kostet mehr. Die erste Information über ein neues Gut (dass es existiert) ist billiger als die letzte (die exakte Zusammensetzung seiner Inhaltsstoffe).

3. **Konvexität** ($\mathcal{C}'' > 0$): Die *Grenzkosten* der Information steigen. Die einfach zugängliche Information (Preis auf dem Preisschild) ist billig; die schwer zugängliche (Qualität eines CDO-Tranches) ist teuer. Dies erzeugt ein natürliches Optimum: Rationale Agenten stoppen die Informationssuche, wenn die Grenzkosten den Grenznutzen übersteigen (I.5 in Kapitel 7).

**Konsequenz: Rationale Uninformiertheit.** Aus A10 folgt direkt, dass es *rational* sein kann, uninformiert zu bleiben. Wenn die Kosten der Information über Gut $k$ den erwarteten Nutzengewinn übersteigen, verzichtet der Agent auf die Information — und trifft eine suboptimale Entscheidung. Dies ist kein Defekt, sondern ein Gleichgewicht: Die Informationslücke selbst ist die optimale Reaktion auf die Kostenstruktur.

Dieses Phänomen hat weitreichende Konsequenzen: Es erklärt, warum Märkte für komplexe Finanzprodukte ($\mathcal{I}$ niedrig, $\mathcal{C}''$ hoch) anfälliger für Blasen und Zusammenbrüche sind als Märkte für einfache Konsumgüter ($\mathcal{I}$ hoch, $\mathcal{C}''$ niedrig). Es erklärt, warum Werbung wirkt (sie senkt $\mathcal{C}$ effektiv). Und es erklärt das Grossman-Stiglitz-Paradox (1980): Wenn alle informiert wären, gäbe es keine Anreize, kostspielige Information zu beschaffen; wenn niemand informiert ist, gibt es hohe Anreize → das Gleichgewicht liegt *zwischen* vollständiger und null Information.

**Status.** A10 ist eine empirische Hypothese mit starker Evidenz. Die Frage ist nicht, *ob* Information kostet, sondern *wie* die Kostenfunktion genau aussieht. A10 legt nur die qualitativen Eigenschaften (positiv, steigend, konvex) fest; die konkrete Form ($c_0 + c_1\mathcal{I} + c_2\mathcal{I}^2$ oder exponentiell etc.) ist Modellierungswahl (Anhang C).

---

## 2.11 Zusammenfassung: Die Axiome auf einer Seite

| Nr. | Axiom | Kurzform | Typ | Konsequenz |
|-----|-------|----------|-----|------------|
| **A1** | Vermögenserhaltung | $\dot{w}_i = y_i - c_i + \theta\dot{p} + rb$ | Identität | Individuelle Bilanz → I.1 |
| **A2** | Gütererhaltung | $\dot{n}_k + \nabla\!\cdot\!\vec{j} = q_k - d_k$ | Identität | Güterbilanzen → P.3 |
| **A3** | Gelderhaltung | $\dot{m} + \nabla\!\cdot\!\vec{j}_m = g - \tau$ | Identität | Geldschöpfung → M.1, SFC |
| **A4** | Gradientenflüsse | $\vec{j} = -D\nabla\mu^{\text{eff}}$ | Konstitutiv | Handelsströme → F.1, F.2 |
| **A5** | Nutzenmaximierung | $\max \mathbb{E}\!\int e^{-\beta t} u\,dt$ | Verhalten | Euler → V.1, Portfolio → III.2, Produktion → III.3 |
| **A6** | Soziale Kopplung | $\dot{x}_i \ni \sum A_{ij}\Phi(x_j - x_i)$ | Interaktion | Herding → V.3, Blasen → VIII, Kaskaden → Schw.1 |
| **A7** | Adaptive Erwartungen | $\dot{\hat{p}} = \omega_a(\cdot) + \omega_f(\cdot) + \alpha_t(\cdot) + \sigma\xi$ | Information | Erwartungsbildung → III.4 |
| **A8** | Populationsrückkopplung | $\dot{N} = r_N N(1 - N/\kappa) + M$ | Biologie | Demographie → V.1–V.5 |
| **A9** | Güterdiversität | $\mathcal{K} = \bigsqcup_{\alpha=1}^6 \mathcal{K}_\alpha$ | Struktur | Güterklassen → Kap. 3, K.1 |
| **A10** | Informationskosten | $\mathcal{C}' > 0,\; \mathcal{C}'' > 0$ | Information | Rationale Ignoranz → I.5, Suchkosten |

Die rechte Spalte zeigt, *welche* Gleichungen aus den Axiomen folgen — die Ableitung erfolgt in Teil II. Die Axiome A1–A3 sind logische Notwendigkeiten; A4 ist ein empirisch fundiertes Konstitutivgesetz; A5–A7 sind falsifizierbare Verhaltenspostulate; A8–A10 sind strukturelle Randbedingungen. Zusammen bilden sie die Basis, auf der das gesamte Gleichungssystem steht.

## 2.12 Axiomatisch vs. Modellierungswahl — Die fundamentale Unterscheidung

Um Missverständnissen vorzubeugen, formulieren wir die Abgrenzung zwischen Axiom und Modellierungswahl noch einmal explizit als Prinzip:

> **Prinzip der Formfreiheit.** *Die Axiome A1–A10 legen die qualitativen Eigenschaften aller Funktionen fest (Monotonie, Vorzeichen, Beschränktheit). Sie legen nicht die funktionale Form fest. Jede konkrete Funktion, die die axiomatischen Eigenschaften erfüllt, erzeugt ein konsistentes Gleichungssystem. Die qualitativen Resultate (Stabilität, Spezialfälle, kausale Struktur) sind forminvariant.*

In der Praxis bedeutet dies: Wenn wir in den folgenden Kapiteln $u$, $F$, $\Phi$, $\Psi$, $\omega$ oder $\mathcal{C}$ schreiben, meinen wir *eine beliebige Funktion mit den axiomatischen Eigenschaften* — nicht eine spezifische Formel. Der Leser, der CRRA-Nutzen verwenden möchte, setzt $u(c) = c^{1-\gamma}/(1-\gamma)$ ein. Der Leser, der CARA bevorzugt, setzt $u(c) = -e^{-\alpha c}$ ein. Die Theorie trifft in beiden Fällen dieselben qualitativen Aussagen.

---

*Ende von Kapitel 2. Im folgenden Kapitel beschreiben wir die sechs Güterklassen, die fünf Agentenklassen und die Netzwerkstruktur des Systems.*

---

# Kapitel 3: Güterklassen, Agenten, Netzwerk

---

Bevor die Gleichungen aufgestellt werden (Teil II), muss die *Ontologie* des Systems definiert sein: Was gibt es? Wer handelt? Wer ist mit wem verbunden? Dieses Kapitel legt die drei Bausteine fest:

1. **Güter** — sechs disjunkte Klassen mit verschiedenen physischen Eigenschaften (§3.1–3.2)
2. **Agenten** — fünf funktionale Klassen mit verschiedenen Entscheidungsproblemen (§3.3)
3. **Netzwerk** — fünf Verbindungsebenen, die Agenten koppeln (§3.4)

Abschließend definieren wir den Zustandsvektor (§3.5), klassifizieren alle Variablen nach ihrem Endogenitätsstatus (§3.6) und trennen scharf zwischen axiomatischen Festlegungen und austauschbaren Modellierungswahlen (§3.7).

---

## 3.1 Die sechs Güterklassen

Axiom A9 postuliert die Existenz einer Partition $\mathcal{K} = \bigsqcup_{\alpha=1}^6 \mathcal{K}_\alpha$. Dieses Kapitel definiert die Partition konkret.

Die fundamentale Einsicht ist, dass Güter sich in drei *physischen* Eigenschaften unterscheiden, die ihre Dynamik vollständig bestimmen:

> **Definition 3.1 (Gütersignatur).** *Jedes Gut $k \in \mathcal{K}$ wird durch ein Tripel $(s_k, r_k, e_k)$ charakterisiert:*
> - $s_k \in \{0, 1\}$ — **Rivalität**: $s_k = 1$ wenn der Konsum durch Agent $i$ den verfügbaren Bestand für Agent $j$ reduziert; $s_k = 0$ sonst.
> - $r_k \in \{0, 1\}$ — **Ausschließbarkeit**: $r_k = 1$ wenn der Zugang technisch oder rechtlich beschränkbar ist; $r_k = 0$ sonst.
> - $e_k \geq 0$ — **Zerfallsrate**: Die Rate, mit der der Bestand ohne menschliches Zutun abnimmt (Abschreibung, Verderb, Informationszerfall).

Aus den Kombinationen von $(s, r, e)$ ergeben sich die sechs Klassen:

| $\alpha$ | Klasse | Name | $s$ | $r$ | $e$ | Beispiele | Kerngleichung |
|---|---|---|---|---|---|---|---|
| 1 | $\mathcal{K}_1$ | **Abschreibende Güter** | 1 | 1 | $\delta_k > 0$ | Maschinen, Fahrzeuge, Gebäude | $\dot{n}_k = -\delta_k n_k + q_k - d_k$ |
| 2 | $\mathcal{K}_2$ | **Nicht-abschreibende Güter** | 1 | 1 | $0$ | Land, Gold, Diamanten, Kunst | $\dot{n}_k = q_k - d_k$ |
| 3 | $\mathcal{K}_3$ | **Konsumierbare Güter** | 1 | 1 | $\to \infty$ | Nahrung, Energie, Treibstoff | $\dot{n}_k = q_k - c_k$ |
| 4 | $\mathcal{K}_4$ | **Immaterielle Güter** | 0 | 1 | $\geq 0$ | Patente, Software, Musik, Marken | $\dot{n}_k = q_k$ (Nutzung verbraucht nicht) |
| 5 | $\mathcal{K}_5$ | **Monetäre Güter** | 1* | 1 | $0$ | Bargeld, Bankguthaben, Kryptowährungen | $\dot{m} = g - \tau$ (A3) |
| 6 | $\mathcal{K}_6$ | **Informationelle Güter** | 0 | 0 | $\omega > 0$ | Daten, Wissen, Nachrichten | $\dot{\mathcal{I}}_k = D\nabla^2\mathcal{I}_k - \omega\mathcal{I}_k + \mathcal{S}_k$ |

*\*Geld ist rival im Besitz (ein Euro kann nur einmal ausgegeben werden), aber nicht-rival in der Nutzung als Wertmaßstab.*

Jede Klasse hat eine qualitativ verschiedene Dynamik. Im Detail:

**$\mathcal{K}_1$ — Abschreibende Güter.** Der Bestand sinkt exponentiell mit Rate $\delta_k$ und wird durch Produktion $q_k$ aufgefüllt und durch Konsum/Entsorgung $d_k$ reduziert. Die Gleichung ist eine spezialisierte Version der allgemeinen Gütererhaltung (A2) mit dem Zerfall als dominantem Senkenterm. Typische Abschreibungsraten: Maschinen $\delta \approx 0{,}05$–$0{,}10$ pro Jahr; Gebäude $\delta \approx 0{,}02$; Fahrzeuge $\delta \approx 0{,}15$.

**$\mathcal{K}_2$ — Nicht-abschreibende Güter.** Kein Zerfall ($\delta = 0$). Land wird nicht weniger, Gold rostet nicht. Der Bestand ändert sich nur durch Handel (Umverteilung) und — bei natürlichen Ressourcen — durch Extraktion. Diese Klasse enthält die *reinen Vermögensspeicher*: Assets, deren Wert allein aus der Knappheit kommt ($q_k \approx 0$ für Gold, $q_k = 0$ für Land).

**$\mathcal{K}_3$ — Konsumierbare Güter.** Vernichtung bei Konsum: Nahrung wird gegessen, Benzin wird verbrannt. Formal ist $e \to \infty$ äquivalent zu $d_k = c_k$ — der gesamte Konsum wird sofort vernichtet. Der Bestand ist daher ein *Flussgleichgewicht*: Er existiert nur als Differenz zwischen laufender Produktion und laufendem Verbrauch.

**$\mathcal{K}_4$ — Immaterielle Güter.** Nicht-rival ($s = 0$): Der Konsum durch einen Agenten reduziert den Bestand *nicht*. Tausend Nutzer können dieselbe Software gleichzeitig verwenden, ohne dass sie weniger wird. Ausschließbar ($r = 1$): Patente, Urheberrecht, DRM beschränken den Zugang. Die Dynamik hat keine Senke (außer Obsoleszenz, $\delta_k \geq 0$) — der Bestand wächst monoton mit der Produktion. Die Grenzkosten der Reproduktion sind null: $MC_k^{\text{Kopie}} = 0$.

**$\mathcal{K}_5$ — Monetäre Güter.** Unterliegen A3 (Gelderhaltung). Die Besonderheit: Geld wird nicht *produziert* wie physische Güter, sondern *geschöpft* — durch Kreditvergabe (Geschäftsbanken) und Offenmarktoperationen (Zentralbank). Die Quelle $g$ und die Senke $\tau$ sind institutionell bestimmt (Kapitel 8).

**$\mathcal{K}_6$ — Informationelle Güter.** Weder rival noch ausschließbar — Wissen breitet sich aus wie ein Diffusionsfeld. Die Dynamik ist eine Reaktions-Diffusionsgleichung: Ausbreitung ($D\nabla^2\mathcal{I}$), natürlicher Zerfall ($-\omega\mathcal{I}$) durch Vergessen und Veralten, Quellen ($\mathcal{S}_k$) durch Forschung und Werbung. Diese Klasse ist das dynamische Fundament der Informationsökonomik (Kapitel 7).

### Warum sechs Klassen?

Die Partition ist nicht willkürlich — sie folgt aus der Kombinatorik der drei binären Merkmale $(s, r)$ plus der Zerfallsrate $e$:

| $(s, r)$ | $e = 0$ | $e > 0$ | $e \to \infty$ |
|---|---|---|---|
| $(1, 1)$ | $\mathcal{K}_2$ | $\mathcal{K}_1$ | $\mathcal{K}_3$ |
| $(0, 1)$ | — | $\mathcal{K}_4$ | — |
| $(1, 1)^*$ | $\mathcal{K}_5$ | — | — |
| $(0, 0)$ | — | $\mathcal{K}_6$ | — |

Die leeren Zellen sind empirisch unbedeutend oder logisch ausgeschlossen. Die sechs Klassen decken die ökonomisch relevanten Kombinationen vollständig ab.

---

## 3.2 Konversion zwischen Klassen

Güter können ihre Klasse wechseln:

- Ein Patent ($\mathcal{K}_4$) wird offengelegt → freies Wissen ($\mathcal{K}_6$)
- Wissen ($\mathcal{K}_6$) wird patentiert → immaterielles Gut ($\mathcal{K}_4$)
- Eine Maschine ($\mathcal{K}_1$) wird verschrottet → Alteisen als Konsumgut ($\mathcal{K}_3$)
- Nahrung ($\mathcal{K}_3$) wird konserviert → langlebiges Gut ($\mathcal{K}_1$, kleines $\delta$)

Die allgemeine Konversionsgleichung ist:

> **Gleichung K.1 (Güterkonversion).**
>
> $$\frac{dn_k^{(\alpha)}}{dt} = \underbrace{\text{[intrinsische Dynamik von } \mathcal{K}_\alpha\text{]}}_{\text{aus §3.1}} \;-\; \sum_{\beta \neq \alpha} \lambda_{\alpha\beta}\, n_k^{(\alpha)} \;+\; \sum_{\beta \neq \alpha} \lambda_{\beta\alpha}\, n_k^{(\beta)}$$

wobei $\lambda_{\alpha\beta} \geq 0$ die Konversionsrate von Klasse $\alpha$ nach $\beta$ ist.

**Interpretation.** Der erste Summenterm beschreibt den *Abfluss* aus $\mathcal{K}_\alpha$ (Güter verlassen die Klasse); der zweite den *Zufluss* aus allen anderen Klassen. Die Konversionsraten $\lambda_{\alpha\beta}$ sind endogene Variablen — sie hängen von Technologie ($A$), Institutionen (Patentrecht, Regulierung) und Informationsstand ($\mathcal{I}$) ab.

**Die Konversionsmatrix.** Die $6 \times 6$-Matrix $\Lambda = (\lambda_{\alpha\beta})$ ist dünn besetzt: Die meisten Übergänge sind physikalisch unmöglich oder ökonomisch irrelevant. Die empirisch wichtigsten Konversionen sind:

| Von → Nach | $\lambda$ | Trigger |
|---|---|---|
| $\mathcal{K}_4 \to \mathcal{K}_6$ | $\lambda_{46}$ | Patentablauf, Open-Source-Entscheidung |
| $\mathcal{K}_6 \to \mathcal{K}_4$ | $\lambda_{64}$ | Patentierung von Wissen |
| $\mathcal{K}_1 \to \mathcal{K}_3$ | $\lambda_{13}$ | Verschrottung, Entsorgung |
| $\mathcal{K}_3 \to \mathcal{K}_1$ | $\lambda_{31}$ | Konservierung, Verarbeitung |
| $\mathcal{K}_5 \to \mathcal{K}_2$ | $\lambda_{52}$ | Kauf von Gold mit Geld |
| $\mathcal{K}_2 \to \mathcal{K}_5$ | $\lambda_{25}$ | Verkauf von Gold gegen Geld |

Die Konversion $\mathcal{K}_5 \leftrightarrow \mathcal{K}_2$ ist der klassische Goldstandard: Geld und Gold sind ineinander konvertierbar. Die Konversion $\mathcal{K}_4 \leftrightarrow \mathcal{K}_6$ ist die zentrale Spannung der Wissensökonomie: Wann soll Wissen frei sein, wann geschützt?

K.1 erscheint hier *einmal* in allgemeiner Form. Ihre Spezialisierungen für bestimmte Märkte folgen in Teil V.

---

## 3.3 Die fünf Agentenklassen

Das System enthält fünf funktionale Klassen von Agenten — nicht als soziologische Typisierung, sondern als Unterscheidung nach *Entscheidungsproblem* und *Budgetrestriktion*:

$$\mathcal{A} = \mathcal{W} \cup \mathcal{U} \cup \mathcal{B} \cup \mathcal{G} \cup \mathcal{Z}$$

### 3.3.1 Arbeiter ($\mathcal{W}$)

| Merkmal | Spezifikation |
|---|---|
| **Einkommen** | $y_i = w_\ell \ell_i$ (nur Arbeitseinkommen) |
| **Kreditbeschränkung** | $b_i \geq 0$ (kein Schuldenzugang) |
| **Budget** | $\dot{w}_i = w_\ell \ell_i - c_i + r \cdot b_i$ (A1-Spezialisierung) |
| **Konsum** | Euler-Gleichung (V.1), modifiziert durch Ebene 2 und 3 |
| **Portfolio** | Eingeschränkt: $\theta_{ik} \in [0, \theta_{\max}^{\mathcal{W}}]$ (kein Leerverkauf, begrenzter Marktzugang) |
| **Arbeit** | Endogen: $\ell_i^* = \arg\max_\ell [u(c_i) - \phi(\ell_i)]$ unter $c_i = w_\ell \ell_i + r b_i$ |
| **Entscheidungsvariablen** | $(c_i, \ell_i, \theta_{ik}, \hat{p}_{ik})$ |

Die Klasse $\mathcal{W}$ umfasst alle Agenten, deren primäre Einkommensquelle Arbeit ist. Die Kreditbeschränkung $b_i \geq 0$ ist die schärfste Restriktion: Arbeiter können nicht gegen zukünftiges Einkommen leihen. Dies erzeugt die bekannte Asymmetrie zwischen Arbeitern und Unternehmern — Arbeiter sind stärker von kurzfristigen Einkommensschocks betroffen, weil sie Konsumschwankungen nicht durch Verschuldung glätten können.

### 3.3.2 Unternehmer ($\mathcal{U}$)

| Merkmal | Spezifikation |
|---|---|
| **Einkommen** | $y_j = p_k q_{jk} - w_\ell L_j - r K_j$ (Profit = Umsatz − Lohn − Kapitalkosten) |
| **Produktion** | $\dot{q}_k = \lambda_q \frac{p_k - MC_k(q_k)}{p_k} q_k - \delta_q q_k$ (III.3) |
| **Grenzkosten** | $MC_k(q) = w_\ell / F_L(K, L)$ (aus der Produktionsfunktion) |
| **Investition** | Kapitalakkumulation: $\dot{K}_j = I_j - \delta K_j$ |
| **Entscheidungsvariablen** | $(q_k, L_j, K_j, \theta_{ik}, \hat{p}_{ik})$ |

Unternehmer wählen simultan Produktionsmenge, Arbeitsnachfrage, Investition und Portfolio. Die Entscheidung ist erheblich komplexer als die der Arbeiter, weil die Produktionsfunktion $F(K, L, \mathcal{I})$ (und damit der Profit) von der Informationsinfrastruktur abhängt.

### 3.3.3 Banken ($\mathcal{B}$)

| Merkmal | Spezifikation |
|---|---|
| **Einkommen** | $y_b = r_L L_b - r_D D_b$ (Zinsmarge: Kreditzins − Einlagenzins) |
| **Bilanz** | Aktiva $= L_b + K_b$; Passiva $= D_b$; Eigenkapital $= E_b = L_b + K_b - D_b$ |
| **Geldschöpfung** | $g_{\mathcal{B}} = \dot{L}_b$ (Kreditvergabe erzeugt Geld, A3) |
| **Regulierung** | Basel-Beschränkung: $E_b \geq \alpha_{\text{Basel}} \cdot \text{RWA}_b$ |
| **Kreditangebot** | $L_b^* \propto E_b / \text{RWA}$ (beschränkt durch risikogewichtete Aktiva) |
| **Entscheidungsvariablen** | $(L_b, D_b, r_L, r_D)$ |

Banken sind die *einzigen* privaten Agenten, die Geld schöpfen können (über Kreditvergabe). Ihre Bilanzidentität ist die mikrofundierte Grundlage von A3. Die Basel-Beschränkung ist eine *harte Nebenbedingung* — sie begrenzt die Kreditvergabe und damit die Geldschöpfung. Wenn $E_b$ sinkt (Verluste), muss $L_b$ sinken: der Kreditkanal der Krise.

### 3.3.4 Staaten ($\mathcal{G}$)

| Merkmal | Spezifikation |
|---|---|
| **Budget** | $\dot{w}^{\mathcal{G}} = T - G - \text{Tr} - r_G B^{\mathcal{G}}$ (A1-Spezialisierung) |
| **Steuereinnahmen** | $T = \tau_{\mathcal{W}} \sum_{i \in \mathcal{W}} y_i + \tau_{\mathcal{U}} \sum_{j \in \mathcal{U}} \pi_j + \tau_{\text{MwSt}} \sum_k p_k d_k$ |
| **Ausgaben** | $G = G_{\text{Konsum}} + G_{\text{Invest}} + G_{\text{Transfers}}$ |
| **Schulden** | $\dot{B}^{\mathcal{G}} = G + r_G B^{\mathcal{G}} - T$ |
| **Geldvernichtung** | Steuern vernichten Geld: $\tau \to -\tau$ in A3 |
| **Kontrollparameter** | $(\tau_{\mathcal{W}}, \tau_{\mathcal{U}}, \tau_{\text{MwSt}}, G, \text{Tr})$ — politisch gesetzt |

Der Staat ist der *einzige* Agent, dessen Kontrollparameter semi-endogen sind: Die Steuersätze und Ausgaben folgen *Reaktionsregeln* auf den Systemzustand (z.B. antizyklische Fiskalpolitik), aber die Regeln selbst sind politisch gewählt, nicht ökonomisch determiniert.

### 3.3.5 Zentralbanken ($\mathcal{Z}$)

| Merkmal | Spezifikation |
|---|---|
| **Geldschöpfung** | $g_{\mathcal{Z}} = \dot{M}^{\text{Basis}}$ (Basisgeld-Emission) |
| **Zinssteuerung** | Taylor-Regel: $r^{\mathcal{Z}} = \rho_r r_{t-1} + (1-\rho_r)[\bar{r} + \phi_\pi(\pi_t - \pi^*) + \phi_y(\hat{y}_t - \hat{y}^*)] + \varepsilon_r$ |
| **Taylor-Prinzip** | $\phi_\pi > 1$ (Zins reagiert überproportional auf Inflation) |
| **Kontrollparameter** | $(r^{\mathcal{Z}}, M_0, \phi_\pi, \phi_y, \pi^*)$ — geldpolitischer Rahmen |

Die Zentralbank hat im System zwei Hebel: den Zinssatz $r^{\mathcal{Z}}$ und die Basisgeldmenge $M_0$. Die Taylor-Regel (VI.1) ist eine *semi-endogene* Reaktionsfunktion: Sie ist determiniert, sobald die Parameter $(\phi_\pi, \phi_y, \pi^*, \bar{r})$ gewählt sind, aber diese Wahl selbst ist institutionell.

### Zusammenfassung der Agentenklassen

| Klasse | Symbol | Einkommen | Besondere Restriktion | Rolle im System |
|---|---|---|---|---|
| Arbeiter | $\mathcal{W}$ | Arbeit | $b_i \geq 0$ (kein Kredit) | Konsum, Arbeit |
| Unternehmer | $\mathcal{U}$ | Profit | Produktionsfunktion $F$ | Produktion, Investition |
| Banken | $\mathcal{B}$ | Zinsmarge | Basel-Beschränkung | Geldschöpfung, Kredit |
| Staaten | $\mathcal{G}$ | Steuern | Politische Constraint | Umverteilung, Regulierung |
| Zentralbank | $\mathcal{Z}$ | — | Institutioneller Rahmen | Geldpolitik, Zinssetzung |

Die Klassen sind *nicht* disjunkt in dem Sinne, dass ein Agent seine Klasse nicht wechseln könnte — ein Arbeiter kann Unternehmer werden (Klassenwechsel $C_{\mathcal{W} \to \mathcal{U}}$ in V.1, Kapitel 9). Aber zu jedem Zeitpunkt $t$ gehört jeder Agent genau einer Klasse an.

---

## 3.4 Das Multiplex-Netzwerk

In der neoklassischen Theorie interagieren Agenten nur über den anonymen Markt — der Preis aggregiert alle Information, und kein Agent hat eine bevorzugte Beziehung zu einem anderen. In unserem System ist diese Anonymität die *Ausnahme*, nicht die Regel.

Die Verbindungsstruktur zwischen Agenten wird als **Multiplex-Netzwerk** modelliert — ein Graph mit mehreren Ebenen, wobei jede Ebene einen anderen Interaktionskanal repräsentiert.

### 3.4.1 Netzwerkdefinition (V.6)

> **Gleichung V.6 (Multiplex-Netzwerk).**
>
> $$\mathcal{G} = \left(A^{(1)}, A^{(2)}, A^{(3)}, A^{(4)}, A^{(5)}\right)$$
>
> *wobei $A^{(\ell)} \in [0,1]^{N \times N}$ die gewichtete Adjazenzmatrix der Ebene $\ell$ ist.*

| Ebene $\ell$ | Name | Verbindung | Beispiele |
|---|---|---|---|
| 1 | **Handel** | $\mathcal{W} \leftrightarrow \mathcal{U}$, $\mathcal{U} \leftrightarrow \mathcal{U}$ | Lieferanten-Kunden-Beziehungen |
| 2 | **Information** | Alle $\leftrightarrow$ Alle | Wissens-Spillovers, Marktinformation |
| 3 | **Kredit** | $\mathcal{B} \leftrightarrow \mathcal{W}$, $\mathcal{B} \leftrightarrow \mathcal{U}$ | Kreditbeziehungen; systemisch relevante Links |
| 4 | **Sozial** | Alle $\leftrightarrow$ Alle | Peer-Einfluss, Nachbarschaft, Communitys |
| 5 | **Politisch** | $\mathcal{U} \leftrightarrow \mathcal{G}$, Wähler $\leftrightarrow$ $\mathcal{G}$ | Lobbying, Regulierung, Wählerblöcke |

Jede Ebene ist ein gerichteter oder ungerichteter Graph auf der Agentenmenge $\mathcal{A}$. Ein Eintrag $A_{ij}^{(\ell)} \in [0, 1]$ misst die Verbindungsstärke: 0 = keine Verbindung, 1 = maximale Verbindung. Die Gesamtdimension ist $5 \times N \times N$.

Die fünf Ebenen unterscheiden sich in ihrer Reichweite und Geschwindigkeit:

| Ebene | Reichweite | Typische Geschwindigkeit | Persistenz |
|---|---|---|---|
| Handel | Regional bis global | Tage–Wochen | Mittel |
| Information | Global (Internet) | Sekunden–Stunden | Niedrig (Zerfall $\omega$) |
| Kredit | Regional bis national | Monate–Jahre | Hoch |
| Sozial | Lokal bis global | Stunden–Wochen | Hoch |
| Politisch | National | Jahre | Sehr hoch |

### 3.4.2 Effektive Adjazenz (V.7)

Ein Agent wird nicht auf jeder Ebene gleich stark beeinflusst. Für die Verhaltensdynamik (Herding A6, Erwartungsbildung A7) benötigen wir eine *gewichtete Superposition*:

> **Gleichung V.7 (Effektive Adjazenz).**
>
> $$A^{\text{eff}} = \sum_{\ell=1}^{5} \omega_\ell\, A^{(\ell)}$$
>
> *wobei $\omega_\ell \geq 0$ das Gewicht der Ebene $\ell$ ist.*

Die Gewichte $\omega_\ell$ können zustandsabhängig sein: In einer Kreditkrise dominiert die Kreditebene ($\omega_3$ steigt), in einer Blase die soziale und Informationsebene ($\omega_4, \omega_2$ steigen). Die zustandsabhängige Gewichtung erzeugt *endogene Netzwerkrelevanz* — welche Verbindungen „zählen", hängt vom Marktzustand ab.

**Graph-Laplacian.** Aus $A^{\text{eff}}$ folgt der Laplace-Operator des Netzwerks:

$$L_{ij}^{\text{eff}} = \begin{cases} \sum_k A_{ik}^{\text{eff}} & \text{falls } i = j \\ -A_{ij}^{\text{eff}} & \text{falls } i \neq j \end{cases}$$

Der Laplacian tritt direkt in der Herding-Dynamik auf: Der Term $\sum_j A_{ij}^{\text{eff}}(\theta_{jk} - \theta_{ik})$ aus A6 ist gleich $-(L^{\text{eff}} \boldsymbol{\theta}_k)_i$ — der Laplacian angewandt auf das Portfoliofeld. Die spektralen Eigenschaften des Laplacian bestimmen:

| Eigenschaft | Formalisierung | Konsequenz |
|---|---|---|
| **Algebraische Konnektivität** | $\lambda_2(L^{\text{eff}})$ | Fragmentierungsrisiko — bei $\lambda_2 \to 0$ zerfällt das Netzwerk |
| **Spektralradius** | $\lambda_N(L^{\text{eff}})$ | Maximale Ansteckungsgeschwindigkeit |
| **Zentralität** | Eigenvektor zu $\lambda_N$ | Systemisch wichtigste Agenten |

### 3.4.3 Netzwerkdynamik (V.8)

Das Netzwerk ist nicht statisch — Verbindungen entstehen und zerfallen:

> **Gleichung V.8 (Linkdynamik).**
>
> $$\dot{A}_{ij}^{(\ell)} = \alpha_\ell^+\, g(z_i, z_j)\,(1 - A_{ij}^{(\ell)}) - \alpha_\ell^-\, A_{ij}^{(\ell)}$$

| Term | Bedeutung |
|---|---|
| $\alpha_\ell^+$ | Linkbildungsrate der Ebene $\ell$ |
| $g(z_i, z_j)$ | Ähnlichkeits-/Attraktionsfunktion der Agentenzustände |
| $(1 - A_{ij}^{(\ell)})$ | Sättigungsterm — bereits bestehende Links wachsen nicht weiter |
| $\alpha_\ell^-$ | Linkzerfallsrate |

Die Funktion $g$ hat axiomatische Eigenschaften ($g \geq 0$, $g$ steigt mit Ähnlichkeit), aber keine vorgeschriebene Form. Beispiele:

- **Handelsebene**: $g \propto \exp(-\gamma \|x_i - x_j\|)$ — räumliche Nähe fördert Handel.
- **Kreditebene**: $g$ hängt von Bonität, Sicherheiten und Beziehungshistorie ab.
- **Sozialebene**: $g$ steigt mit Vermögensähnlichkeit $|w_i - w_j| < \Delta w_{\text{krit}}$ — soziale Homophilie.
- **Informationsebene**: Permanenter Link ($\alpha^-$ klein); geometrische Diffusion.
- **Politische Ebene**: $g$ steigt mit ideologischer Nähe; zerfällt bei Regimewechsel.

V.8 erzeugt endogene Netzwerkbildung: In Boomzeiten entstehen mehr Handels- und Kreditlinks ($g$ steigt, weil Bonität steigt); in Krisen zerfallen sie ($\alpha^-$ steigt, weil Vertrauen sinkt). Die Netzwerkstruktur ist damit *selbst* eine dynamische Variable des Systems.

---

## 3.5 Der Zustandsvektor

Alle Variablen des Systems werden in einem einzigen Zustandsvektor zusammengefasst:

> **Definition 3.2 (Zustandsvektor).**
>
> $$\mathbf{X}(t) = \underbrace{(w_i, c_i, L_i, \theta_{ik}, \hat{p}_{ik})_{i \in \mathcal{A}}}_{\text{Mikro: Agenten}} \cup \underbrace{(p_k, n_k^{(\alpha)}, m, \mathcal{I}_k)_{k \in \mathcal{K}, \alpha}}_{\text{Felder: Güter}} \cup \underbrace{(N_\mathcal{X}, R_k, A_{ij}^{(\ell)})}_{\text{Struktur}} \cup \underbrace{(\gamma_i, \beta_i, c_i^*, \zeta_i, \ldots)}_{\text{Parameter}} \cup \underbrace{(\mathcal{T}, H_i, E, \kappa_{\text{eco}})}_{\text{Langsam}} \cup \underbrace{(a_{ik}, E_{\text{adv},k})}_{\text{Aufmerksamkeit}} \cup \underbrace{(\vartheta_k^{(i)}, \text{Regime}(t))}_{\text{Schwellenwerte}}$$

Die sieben Blöcke im Überblick:

| Block | Variablen | Dimension | Bestimmt durch |
|---|---|---|---|
| **Mikro** | $w_i, c_i, L_i, \theta_{ik}, \hat{p}_{ik}$ | $N(2K + 3)$ | I.1, V.1–V.3, L.1–L.4, III.2, III.4 |
| **Güterfelder** | $p_k, n_k^{(\alpha)}, m, \mathcal{I}_k$ | $7K + 1$ | II.2, P.3, I.4, I.1 (Info) |
| **Struktur** | $N_\mathcal{X}, R_k, A_{ij}^{(\ell)}$ | $5 + K + 5N^2$ | V.1–V.5, V.4, V.8 |
| **Parameter** | $\gamma_i, \beta_i, c_i^*, \zeta_i, \ldots$ | $\sim 6N$ | VI.1–VI.9 |
| **Langsam** | $\mathcal{T}, H_i, E, \kappa_{\text{eco}}$ | $N + 3$ | VII.1–VII.4 |
| **Aufmerksamkeit** | $a_{ik}, E_{\text{adv},k}$ | $NK + K$ | I.3 (Aufmerksamkeit), I.2 (Werbung) |
| **Schwellenwerte** | $\vartheta_k^{(i)}, \text{Regime}(t)$ | $NK + 1$ | Schw.1–Schw.2, RS.1 |

Die Aufmerksamkeit $a_{ik} \in [0, 1]$ — der Anteil der kognitiven Ressourcen, den Agent $i$ auf Gut $k$ richtet — ist eine *begrenzte Ressource*: $\sum_k a_{ik} = 1$ (Gleichung I.3, Kapitel 7). Sie koppelt an die Informationsdynamik ($\mathcal{I}_k$) und die Nutzenarchitektur ($\omega_{ik}$): Ein Agent kann nur Güter nachfragen, denen er Aufmerksamkeit widmet. Die Werbeausgaben $E_{\text{adv},k}$ steuern die Aufmerksamkeitsallokation von außen (Unternehmer investieren in Werbung, um $a_{ik}$ zu erhöhen).

Die Schwellenwerte $\vartheta_k^{(i)}$ — die individuellen Aktivierungsschwellen für Regimewechsel (Bankrun-Auslösung, Kauf-/Verkaufsentscheidung, Migrationsbereitschaft) — bestimmen, wann ein Agent diskontinuierlich handelt. Der Regimezustand $\text{Regime}(t) \in \{1, \ldots, R\}$ beschreibt den globalen Marktzustand (Normalphase, Blase, Krise, Recovery — Kapitel 10).

Die Dimension ist:

$$\dim(\mathbf{X}) \approx \mathcal{O}(N^2 + NK)$$

wobei $N = |\mathcal{A}|$ die Agentenzahl und $K = |\mathcal{K}|$ die Güterzahl ist. Der $N^2$-Term kommt aus dem Netzwerk ($5N^2$ Einträge in $A^{(\ell)}$), der $NK$-Term aus Portfolio ($\theta_{ik}$), Aufmerksamkeit ($a_{ik}$) und Schwellenwerten ($\vartheta_k^{(i)}$).

Die Komponenten verteilen sich auf fünf *Zeitskalen*:

| Block | Variablen | Typische Zeitskala | Beispiele |
|---|---|---|---|
| **Ultraschnell** | Preise, Flüsse | Sekunden–Tage | Börsenkurse, Devisenströme |
| **Schnell** | Konsum, Produktion, Erwartungen | Wochen–Quartale | Konsumentscheidungen, Produktionsanpassung |
| **Mittel** | Population, Netzwerk | Jahre | Bevölkerungsdynamik, Kreditnetzwerk |
| **Langsam** | Technologie, Humankapital, Vertrauen | Jahrzehnte | Innovationszyklen, Bildungsinvestition |
| **Ultralangsam** | Emissionen, Ökologie | Jahrhunderte | Klimawandel, Ressourcendepletion |

Diese Skalentrennung ist methodisch bedeutsam: Sie erlaubt *Quasi-Gleichgewichtsapproximationen*, bei denen die langsamen Variablen als konstant behandelt werden, während die schnellen Variablen ihr Gleichgewicht erreichen (Kapitel 14).

---

## 3.6 Endogen, exogen, semi-endogen: Vollständige Klassifikation

Für den Systemschluss (Teil III) ist es fundamental zu wissen, welche Variablen durch die Gleichungen bestimmt werden und welche von außen vorgegeben sind.

> **Definition 3.3 (Endogenitätsklassifikation).**
> - **Endogen**: Variable wird durch die Systemgleichungen bestimmt; ihr Zeitpfad folgt aus den DGL und den Anfangsbedingungen.
> - **Semi-endogen**: Variable folgt einer *Reaktionsregel* auf endogene Variablen, aber die Regel selbst ist exogen gewählt.
> - **Exogen**: Variable wird von außen vorgegeben und ändert sich nicht als Reaktion auf das System.
> - **Anfangsbedingung**: Wert zum Startzeitpunkt $t_0$; danach endogen.

Die vollständige Zuordnung:

| Variable | Status | Bestimmt durch | Endogenisierbar? |
|---|---|---|---|
| Preise $p_k$ | endogen | II.2 (Preisdynamik) | — |
| Konsum $c_i$ | endogen | V.1–V.3 (Drei-Ebenen) | — |
| Arbeitsangebot $L_i$ | endogen | L.1–L.4 | — |
| Information $\mathcal{I}_k$ | endogen | I.1 (Informationsdynamik) | — |
| Vermögen $w_i$ | endogen | I.1 (Vermögensbilanz) | — |
| Güterbestände $n_k$ | endogen | P.3 (Gütererhaltung) | — |
| Geldmenge $M$ | endogen | M.1 (Geldschöpfung) | — |
| Flüsse $\vec{j}$ | endogen | A4 + Potentiale | — |
| Erwartungen $\hat{p}_{ik}$ | endogen | III.4 (Adaptive Erwartungen) | — |
| Nominalzins $r_{\text{nom}}$ | semi-endogen | Taylor-Regel (VI.1) | Ja (durch ZB-Lernmodell) |
| Steuersatz $\tau$ | semi-endogen | Fiskalregel (Inst.1) | Ja (durch politische Ökonomie) |
| Regulierung $r_k$ | semi-endogen | Inst.2 | Ja |
| Netzwerk $A_{ij}$ | endogen* | V.8 (Linkdynamik) | — |
| Präferenzen $(\gamma_i, \beta_i)$ | endogen** | VI.2 (Adaptive Parameter) | — |
| Technologie-Basis $A_0$ | exogen | Historisch gegeben | Teilweise (über F&E → I.1) |
| Naturressourcen $R_k(0)$ | Anfangsbedingung | Geologie | Nein |
| Katastrophen | exogen | Externe Schocks (VIII.7) | Teilweise (Klima → endogen) |

*Das Netzwerk ist in unserem System endogen (V.8), kann aber in Kalibrierungen auch exogen vorgegeben werden.

**Die Präferenzen driften über VI.1–VI.9, sind aber durch exogene Baselines $\gamma_i^{\text{base}}$ verankert.

**Beobachtung 3.1.** *Im erweiterten System (S13, 75 Gleichungen) ist fast alles endogen. Die einzigen wahrhaft exogenen Größen sind:*

1. *Anfangsbedingungen $\mathbf{X}(0)$*
2. *Externe Schocks (Naturkatastrophen, VIII.7)*
3. *Die institutionellen Reaktionsregeln (Taylor-Regel, Fiskalregel)*
4. *Die axiomatischen Funktionseigenschaften (nicht die Formen)*

Dies ist eine außergewöhnlich *schmale* exogene Basis — das System bestimmt fast alle Variablen selbst.

---

## 3.7 Axiomatisch vs. Modellierungswahl: Was ist austauschbar?

Kapitel 2 (§2.12) formulierte das Prinzip der Formfreiheit. Hier geben wir die vollständige Übersicht, welche Eigenschaften axiomatisch festliegen und welche austauschbar sind.

### Was axiomatisch festliegt (invariant):

| Funktion | Axiomatische Eigenschaft | Formale Bedingung |
|---|---|---|
| Informationskosten $\mathcal{C}(\mathcal{I})$ | Positivität, Monotonie, Konvexität | $\mathcal{C} > 0$, $\mathcal{C}' > 0$, $\mathcal{C}'' > 0$ |
| Nutzenfunktion $u(c)$ | Monotonie, Konkavität | $u' > 0$, $u'' < 0$ |
| Produktionsfunktion $F(K,L)$ | Monotonie, abnehmende Grenzerträge, Inada | $F_K > 0$, $F_{KK} < 0$, $F(0,L) = 0$ |
| Arbeitsleid $\phi(L)$ | Konvexität | $\phi' > 0$, $\phi'' > 0$ |
| Informationsgewichte $\omega(\mathcal{I})$ | Normierung, Monotonie | $\sum \omega = 1$, $\partial\omega/\partial\mathcal{I} > 0$ |
| Herding-Funktion $\Phi(x)$ | Monotonie, Nullpunkt, Beschränktheit | $\Phi' > 0$, $\Phi(0) = 0$, $|\Phi| \leq \Phi_{\max}$ |
| Psychologische Verzerrung $\Psi$ | Verlustaversion, Referenzabhängigkeit | $|\Psi'(x)| > |\Psi'(-x)|$ für $x > 0$ |
| Erwartungsgewichte $\omega_a, \omega_f, \alpha_t$ | Nicht-Negativität, Zustandsabhängigkeit | $\omega_a, \omega_f \geq 0$, Summe variabel |

### Was Modellierungswahl ist (austauschbar):

| Funktion | Standardwahl | Alternativen | Qualitativ gleichwertig? |
|---|---|---|---|
| $u(c)$ | CRRA: $\frac{c^{1-\gamma}}{1-\gamma}$ | CARA: $-e^{-\alpha c}$; Log: $\ln c$; Epstein-Zin | Ja |
| $F(K,L)$ | Cobb-Douglas: $AK^\alpha L^\beta$ | CES: $A[\alpha K^\rho + (1-\alpha)L^\rho]^{1/\rho}$; Leontief | Ja |
| $\omega(\mathcal{I})$ | Softmax: $\frac{\mathcal{I}_k^\eta}{\sum \mathcal{I}_k^\eta}$ | Probit; Linear | Ja |
| $\mathcal{C}(\mathcal{I})$ | Quadratisch: $c_0 + c_1\mathcal{I} + c_2\mathcal{I}^2$ | Exponentiell: $c_0 e^{\lambda\mathcal{I}}$ | Ja |
| Word-of-Mouth in I.1 | Logistisch: $\mathcal{I}(1-\mathcal{I})$ | Gompertz: $\mathcal{I}\ln(\mathcal{I}_{\max}/\mathcal{I})$ | Ja |
| $\Phi(x)$ | Sigmoïd: $\tanh(\alpha x)$ | Linear: $\alpha x$; Asymmetrisch | Ja |

> **Proposition 3.1 (Forminvarianz).** *Zwei Instanzen des Systems, die dieselben Axiome A1–A10 erfüllen, aber verschiedene Funktionalformen verwenden, erzeugen qualitativ identische Dynamik: dieselben Gleichgewichte (bis auf Parameterwerte), dieselben Bifurkationstypen, dieselbe kausale Struktur.*

Der Beweis folgt daraus, dass die qualitativen Eigenschaften (Vorzeichen der Ableitungen, Existenz von Fixpunkten, Stabilitätsbedingungen) nur von den axiomatischen Eigenschaften abhängen. Die Funktionalform bestimmt lediglich die *quantitativen* Werte (Fixpunktlagen, Übergangsgeschwindigkeiten, numerische Momente).

Dieses Prinzip hat eine praktische Konsequenz: **Der gesamte Haupttext der Monographie ist forminvariant.** Wer eine andere Nutzenfunktion oder Produktionsfunktion bevorzugt, ersetzt sie in Anhang C — der Rest des Buches bleibt gültig.

---

*Ende von Kapitel 3. Damit sind die Grundlagen — Axiome, Güter, Agenten, Netzwerk — vollständig. In Teil II leiten wir nun die 75 Gleichungen ab, die aus diesen Grundlagen folgen.*

---

# TEIL II — DAS ALLGEMEINE GLEICHUNGSSYSTEM

---

Teil II enthält die vollständige Ableitung aller 75 Gleichungen des Systems. Jede Gleichung wird in ihrer allgemeinsten Form präsentiert — ohne eingesetzte Funktionalformen. Wo eine konkrete Form benötigt wäre, stehen stattdessen die *axiomatischen Eigenschaften* der betreffenden Funktion und ein Verweis auf Anhang C für konkrete Wahlen.

Die Gleichungen sind in sieben Kapitel geordnet, die der kausalen Logik des Systems folgen:

| Kapitel | Gegenstand | Gleichungen | Charakter |
|---|---|---|---|
| 4 | Erhaltung | I.1–I.4, P.3 | Buchhaltungsidentitäten |
| 5 | Preise und Flüsse | II.1–II.4, F.1–F.2 | Konstitutivgesetze |
| 6 | Entscheidungen | V.1–V.3, L.1–L.5, III.2–III.4, U.1–U.3, VI.1–VI.9 | Verhaltensgleichungen |
| 7 | Information | I.1–I.3, I.5, Ent.2 | Informationsdynamik |
| 8 | Geld und Kredit | M.1, E.1, P.4, IV.1–IV.4 | Monetäre Mechanik |
| 9 | Population und Struktur | V.1–V.5, VII.1–VII.4 | Langsame Dynamik |
| 10 | Sprünge und Regime | VIII.1–VIII.7, Schw.1–Schw.2, RS.1 | Diskontinuitäten |

---

# Kapitel 4: Erhaltungsgleichungen

---

Dieses Kapitel leitet die fünf Erhaltungsgleichungen des Systems ab — die Bilanzidentitäten, die sicherstellen, dass Vermögen, Güter und Geld konsistent geführt werden. Sie folgen direkt aus den Axiomen A1–A3 (Kapitel 2) und der Güterklassenstruktur A9 (Kapitel 3).

Die Erhaltungsgleichungen sind *keine* Verhaltensannahmen — sie beschreiben nicht, was Agenten *tun*, sondern was buchhalterisch *gelten muss*, egal was Agenten tun. Ihre Verletzung wäre nicht ein falsches Modell, sondern ein logischer Widerspruch.

---

## 4.1 Individuelle Vermögensbilanz (I.1)

In Kapitel 2 (§2.1) wurde Axiom A1 als verbale Aussage und Kurzform eingeführt. Hier leiten wir die vollständige Gleichung ab, spezialisiert auf die fünf Agentenklassen.

> **Gleichung I.1 (Individuelle Vermögensbilanz).**
>
> $$\frac{dw_i}{dt} = y_i - c_i + \sum_{k \in \mathcal{K}} \theta_{ik}\,\dot{p}_k + r\,b_i$$

Die vier Terme:

| Term | Symbol | Bedeutung | Vorzeichen |
|---|---|---|---|
| Einkommen | $y_i$ | Zufluss aus Arbeit, Profit, Zinsen, Transfers | $+$ |
| Konsum | $c_i$ | Abfluss durch Güterverbrauch | $-$ |
| Bewertung | $\sum_k \theta_{ik}\,\dot{p}_k$ | Kapitalgewinne/-verluste aus Preisänderungen | $\pm$ |
| Zinsen | $r\,b_i$ | Nettozinsertrag auf Finanzpositionen | $\pm$ |

### Spezialisierung auf die Agentenklassen

I.1 ist die *allgemeine* Bilanz. Ihre konkrete Form hängt von der Agentenklasse ab, weil jede Klasse einen anderen Einkommenstyp und andere Restriktionen hat:

**Arbeiter $i \in \mathcal{W}$:**

$$\frac{dw_i}{dt} = \underbrace{w_\ell\, \ell_i}_{y_i^{\mathcal{W}}} - c_i + \sum_k \theta_{ik}\,\dot{p}_k + r\, b_i, \qquad b_i \geq 0$$

Das Einkommen ist reines Arbeitseinkommen $w_\ell \ell_i$ (Lohnsatz mal Arbeitszeit). Die Kreditbeschränkung $b_i \geq 0$ (aus §3.3.1) ist *bindend*: Arbeiter können keine Schulden aufnehmen, nur positive Finanzpositionen halten. Diese Beschränkung ist eine der folgenreichsten Annahmen des Systems — sie erzeugt die fundamentale Asymmetrie zwischen Arbeitern und Unternehmern.

**Unternehmer $j \in \mathcal{U}$:**

$$\frac{dw_j}{dt} = \underbrace{p_k\, q_{jk} - w_\ell\, L_j - r\, K_j}_{y_j^{\mathcal{U}} = \pi_j} - c_j + \sum_k \theta_{jk}\,\dot{p}_k + r\, b_j$$

Das Einkommen ist der *Profit* $\pi_j$ — die Differenz aus Umsatz ($p_k q_{jk}$), Lohnkosten ($w_\ell L_j$) und Kapitalkosten ($rK_j$). Im Gegensatz zu Arbeitern haben Unternehmer Zugang zu Kreditfinanzierung ($b_j$ kann negativ sein).

**Banken $b \in \mathcal{B}$:**

$$\frac{dw_b}{dt} = \underbrace{r_L\, L_b - r_D\, D_b}_{y_b^{\mathcal{B}}} - c_b^{\text{Betrieb}} + \sum_k \theta_{bk}\,\dot{p}_k$$

Der Bankprofit ist die *Zinsmarge* — Differenz aus Kreditzinsen ($r_L L_b$) und Einlagenzinsen ($r_D D_b$). Der „Konsum" $c_b^{\text{Betrieb}}$ ist der operative Aufwand (Personal, Infrastruktur). Banken unterliegen zusätzlich der Basel-Beschränkung:

$$E_b \geq \alpha_{\text{Basel}} \cdot \text{RWA}_b \tag{NB.2}$$

Diese harte Nebenbedingung begrenzt die Kreditmenge und damit die Geldschöpfung (§4.4).

**Staaten $g \in \mathcal{G}$:**

$$\frac{dw^{\mathcal{G}}}{dt} = \underbrace{T}_{y^{\mathcal{G}}} - G - \text{Tr} - r_G\, B^{\mathcal{G}}$$

Das Einkommen ist die Gesamtsteuer $T = \tau_{\mathcal{W}} \sum_{i \in \mathcal{W}} y_i + \tau_{\mathcal{U}} \sum_{j \in \mathcal{U}} \pi_j + \tau_{\text{MwSt}} \sum_k p_k d_k$. Die Ausgaben zerfallen in Konsum $G$, Transfers $\text{Tr}$ und Zinsen auf Staatsschulden $r_G B^{\mathcal{G}}$. Daraus folgt die Schuldendynamik:

$$\dot{B}^{\mathcal{G}} = G + \text{Tr} + r_G B^{\mathcal{G}} - T$$

Positives $\dot{B}^{\mathcal{G}}$ bedeutet Neuverschuldung; negatives bedeutet Schuldentilgung.

**Zentralbanken $z \in \mathcal{Z}$:** Die Zentralbank hat kein konventionelles Vermögen im Sinne von I.1 — sie verfügt über die Fähigkeit zur Basisgeldschöpfung ($g_{\mathcal{Z}} = \dot{M}^{\text{Basis}}$) und steuert den Zinssatz via Taylor-Regel (VI.1). Ihre „Bilanz" unterliegt anderen Regeln als die der anderen Klassen.

### Harte Nebenbedingungen

I.1 wird durch zwei Nebenbedingungen ergänzt:

> **NB.1 (Subsistenzkonsum).** $c_i \geq c_i^{\min} > 0 \quad \forall i \in \mathcal{A}, \;\forall t \geq 0$
>
> *Kein Agent kann unter das Existenzminimum konsumieren.*

> **NB.2 (Eigenkapitalanforderung).** $E_b \geq \alpha_{\text{Basel}} \cdot \text{RWA}_b \quad \forall b \in \mathcal{B}$
>
> *Banken müssen eine Mindest-Eigenkapitalquote halten.*

NB.1 ist eine *physische* Restriktion (Agenten sterben, wenn $c < c^{\min}$). NB.2 ist eine *institutionelle* Restriktion (regulatorische Vorgabe). Beide sind harte Ungleichungen, die die zulässige Menge des Optimierungsproblems (A5) einschränken.

---

## 4.2 Aggregierte Vermögenserhaltung (I.2)

Gleichung I.2 ist keine unabhängige Gleichung — sie folgt durch Summation von I.1 über alle Agenten.

> **Gleichung I.2 (Aggregierte Vermögenserhaltung).**
>
> $$\frac{dW}{dt} = Y - C$$
>
> *wobei $W = \sum_{i \in \mathcal{A}} w_i$, $Y = \sum_{i \in \mathcal{A}} y_i$, $C = \sum_{i \in \mathcal{A}} c_i$.*

**Ableitung.** Summation von I.1:

$$\frac{dW}{dt} = \sum_i \frac{dw_i}{dt} = \underbrace{\sum_i y_i}_{Y} - \underbrace{\sum_i c_i}_{C} + \underbrace{\sum_i \sum_k \theta_{ik}\,\dot{p}_k}_{= 0} + \underbrace{\sum_i r\, b_i}_{= 0}$$

Die letzten beiden Terme verschwinden:

1. **Bewertungsgewinne** ($\sum_i \sum_k \theta_{ik}\,\dot{p}_k = 0$): Für jedes Asset $k$ gilt $\sum_i \theta_{ik} = 1$ (alle Anteile summieren zu 100%). Der aggregierte Bewertungsgewinn ist $\dot{p}_k \sum_i \theta_{ik} = \dot{p}_k$. Aber der Bewertungsgewinn des einen ist der Bewertungsverlust des anderen — in der Summe null. Genauer: In einem geschlossenen System ist Vermögen aus Bewertungsänderungen ein *Nullsummenspiel* zwischen den Haltern.

2. **Zinsen** ($\sum_i r\, b_i = 0$): Die Summe aller Finanzpositionen ist null — das Guthaben des einen ist die Schuld des anderen. Dies folgt direkt aus A3 (Gelderhaltung): $\sum_i m_i^{\text{netto}} = 0$.

Was bleibt, ist die einfachste aller makroökonomischen Identitäten: Das Gesamtvermögen wächst um das aggregierte Sparen $S = Y - C$.

> **Proposition 4.1 (Nullsumme der Finanzpositionen).** *In einem geschlossenen System (keine externe Geldquelle) gilt:*
>
> $$\sum_{i \in \mathcal{A}} b_i = 0 \qquad \text{und} \qquad \sum_{i \in \mathcal{A}} \sum_k \theta_{ik}\,\dot{p}_k = 0$$
>
> *Bewertungsgewinne und Zinserträge sind zwischen Agenten umverteilt, aber aggregiert null.*

**Implikation.** I.2 besagt: Die einzige Möglichkeit, das *Gesamtvermögen* einer geschlossenen Ökonomie zu erhöhen, ist, mehr zu produzieren als zu konsumieren ($Y > C$). Weder Bewertungsgewinne (Aktienblase) noch Zinserträge (Finanzwirtschaft) können das Gesamtvermögen steigern — sie verteilen nur um. Dies ist eine tiefe Konsequenz aus A1, die in vielen populären Diskussionen übersehen wird.

**Offene Ökonomie.** Für ein *Subsystem* (Land, Sektor) gilt I.2 *nicht* in dieser Reinform — es gibt Kapitalflüsse $\vec{j}_w$ (Gleichung II.1, Kapitel 5), die Vermögen über Systemgrenzen hinweg transferieren:

$$\frac{dW^{\text{Land}}}{dt} = Y^{\text{Land}} - C^{\text{Land}} - \oint_{\partial \Omega} \vec{j}_w \cdot d\vec{A}$$

Der Flussterm ist die Leistungsbilanz (Nettokapitalexport/-import).

---

## 4.3 Gütererhaltung mit Konversion (P.3)

In Kapitel 2 (§2.2) wurde Axiom A2 als allgemeine Kontinuitätsgleichung formuliert, und in Kapitel 3 (§3.1–3.2) die Güterklassen und Konversionsoperatoren eingeführt. Hier verbinden wir beides zur vollständigen Güterbestandsgleichung.

> **Gleichung P.3 (Güterbestandsdynamik — vollständig).**
>
> $$\frac{dn_k^{(\alpha)}}{dt} = \underbrace{q_k^{(\alpha)}}_{\text{Produktion}} - \underbrace{c_k^{(\alpha)}}_{\text{Konsum}} - \underbrace{\delta_\alpha\, n_k^{(\alpha)}}_{\text{Zerfall}} - \underbrace{\nabla \cdot \vec{j}_{n_k}^{(\alpha)}}_{\text{Handelsfluss}} - \underbrace{\sum_{\beta \neq \alpha} \lambda_{\alpha\beta}\, n_k^{(\alpha)}}_{\text{Konversion hinaus}} + \underbrace{\sum_{\beta \neq \alpha} \lambda_{\beta\alpha}\, n_k^{(\beta)}}_{\text{Konversion hinein}}$$

Dies ist die *zentrale* Erhaltungsgleichung für physische Güter. Sie hat sechs Terme — drei mehr als die einfache Kontinuitätsgleichung A2, weil sie die Güterklassenstruktur (A9) und die Konversion (K.1) einbezieht.

### Term-für-Term-Analyse

**Produktion $q_k^{(\alpha)}$.** Die Quellrate — wie viel von Gut $k$ in Klasse $\alpha$ pro Zeiteinheit produziert wird. Für $\mathcal{K}_2$ (Land, Gold) gilt $q_k \approx 0$ (kein menschlich erzeugbares Angebot). Für $\mathcal{K}_4$ (Software, Patente) gilt $q_k > 0$, aber die Grenzkosten der Reproduktion sind null ($MC_k^{\text{Kopie}} = 0$). Die Produktion selbst wird in Kapitel 6 (Gleichung III.3) als Konsequenz der Gewinnmaximierung modelliert.

**Konsum $c_k^{(\alpha)}$.** Die Senkenrate — wie viel konsumiert wird. Für $\mathcal{K}_3$ (Nahrung, Energie) ist $c_k = d_k$ — der gesamte Konsum vernichtet das Gut sofort. Für $\mathcal{K}_4$ (immaterielle Güter) ist $c_k = 0$ — Nutzung vernichtet nicht. Der Konsum selbst wird in Kapitel 6 (Gleichung V.1) als optimal gewählt modelliert.

**Zerfall $\delta_\alpha n_k^{(\alpha)}$.** Exponentieller Verfall des Bestands — Maschinen verschleißen, Gebäude verfallen, Information veraltet. Die Zerfallsraten sind klassenspezifisch:

| Klasse | $\delta_\alpha$ | Typische Halbwertszeit |
|---|---|---|
| $\mathcal{K}_1$ (Maschinen) | $0{,}05$–$0{,}15$ a$^{-1}$ | 5–14 Jahre |
| $\mathcal{K}_2$ (Gold, Land) | $0$ | $\infty$ |
| $\mathcal{K}_3$ (Nahrung) | $\to \infty$ | $\to 0$ (sofortige Vernichtung) |
| $\mathcal{K}_4$ (Patente) | $\geq 0$ | 0 (kein Zerfall) bis 20 Jahre (Patentablauf) |
| $\mathcal{K}_5$ (Geld) | $0$ | $\infty$ (physische Haltbarkeit) |
| $\mathcal{K}_6$ (Information) | $\omega > 0$ | Wochen bis Jahre (Vergessen, Veralten) |

**Handelsfluss $\nabla \cdot \vec{j}_{n_k}^{(\alpha)}$.** Die räumliche Divergenz des Güterstroms — wie viel Gut $k$ nettoabfließt. Positive Divergenz (Nettoexport) reduziert den lokalen Bestand. Der Fluss $\vec{j}$ wird in Kapitel 5 (Gleichung F.1) als Konsequenz des Gradientenaxioms A4 abgeleitet.

**Konversion hinaus/hinein.** Die letzten beiden Terme sind die Klassenübergänge (K.1 aus §3.2). Beispiel: Wenn ein Patent abläuft ($\mathcal{K}_4 \to \mathcal{K}_6$), sinkt $n_k^{(4)}$ und steigt $n_k^{(6)}$ um den gleichen Betrag.

### Spezialisierung nach Güterklasse

P.3 nimmt für jede Klasse eine eigene Gestalt an. Wir schreiben sie hier explizit aus, um die Verschiedenartigkeit der Dynamik zu zeigen:

**$\mathcal{K}_1$ — Abschreibende Güter (Maschinen, Gebäude):**

$$\dot{n}_k^{(1)} = q_k - d_k - \delta_k n_k^{(1)} - \nabla \cdot \vec{j}_{n_k}^{(1)} + \lambda_{31} n_k^{(3)} - \lambda_{13} n_k^{(1)}$$

**$\mathcal{K}_2$ — Nicht-abschreibende Güter (Land, Gold):**

$$\dot{n}_k^{(2)} = \underbrace{q_k}_{\approx 0} - d_k - \nabla \cdot \vec{j}_{n_k}^{(2)} + \lambda_{52} n_k^{(5)} - \lambda_{25} n_k^{(2)}$$

Für $\mathcal{K}_2$ ist die Gleichung fast trivial: Der Bestand ändert sich nur durch Handel (Umverteilung zwischen Agenten) und Konversion (Gold kaufen / Gold verkaufen). Produktion ist vernachlässigbar ($q_k \approx 0$); Zerfall ist null ($\delta = 0$). Dies erklärt, warum Gold und Land *reine Umverteilungsgüter* sind — ihr Gesamtbestand ist (annähernd) konstant.

**$\mathcal{K}_3$ — Konsumierbare Güter (Nahrung, Energie):**

$$\dot{n}_k^{(3)} = q_k - c_k - \nabla \cdot \vec{j}_{n_k}^{(3)} + \lambda_{13} n_k^{(1)} - \lambda_{31} n_k^{(3)}$$

Kein Zerfallsterm, weil der Konsum $c_k$ den gesamten Verbrauch bereits erfasst ($\delta \to \infty$ ist äquivalent zu „sofortige Vernichtung bei Nutzung"). Der Bestand ist ein *Flussgleichgewicht*: Er existiert nur, solange laufend produziert wird.

**$\mathcal{K}_4$ — Immaterielle Güter (Patente, Software):**

$$\dot{n}_k^{(4)} = q_k - \delta_k^{\text{obs}} n_k^{(4)} - \lambda_{46} n_k^{(4)} + \lambda_{64} n_k^{(6)}$$

Kein Konsumterm (Nutzung vernichtet nicht). Die Zerfallsrate $\delta_k^{\text{obs}}$ erfasst Obsoleszenz (technologische Überholung, nicht physischen Verfall). Die Konversion $\mathcal{K}_4 \leftrightarrow \mathcal{K}_6$ ist die Spannung zwischen geschütztem und freiem Wissen.

**$\mathcal{K}_5$ — Monetäre Güter (Geld):** → eigene Gleichung I.4 (§4.4).

**$\mathcal{K}_6$ — Informationelle Güter (Wissen, Daten):**

$$\dot{\mathcal{I}}_k = D_{\mathcal{I}} \nabla^2 \mathcal{I}_k - \omega\, \mathcal{I}_k + \mathcal{S}_k + \lambda_{46} n_k^{(4)}$$

Eine Reaktions-Diffusionsgleichung: Diffusion ($D_{\mathcal{I}} \nabla^2$), Zerfall durch Vergessen ($-\omega \mathcal{I}_k$), Quellen durch Forschung und Werbung ($\mathcal{S}_k$), Zufluss aus offengelegten Patenten ($\lambda_{46} n_k^{(4)}$). Die vollständige Informationsgleichung (I.1) in Kapitel 7 erweitert dies um drei weitere Terme.

### Aggregation

Summation von P.3 über alle Klassen $\alpha$:

$$\frac{dn_k^{\text{total}}}{dt} = \sum_\alpha q_k^{(\alpha)} - \sum_\alpha c_k^{(\alpha)} - \sum_\alpha \delta_\alpha n_k^{(\alpha)} - \nabla \cdot \vec{j}_{n_k}^{\text{total}}$$

Die Konversionsterme heben sich auf ($\sum_\alpha \sum_{\beta \neq \alpha} \lambda_{\alpha\beta} n_k^{(\alpha)} = \sum_\alpha \sum_{\beta \neq \alpha} \lambda_{\beta\alpha} n_k^{(\beta)}$) — Konversion verschiebt Güter zwischen Klassen, vernichtet aber nichts. Das Aggregat reduziert sich auf die einfache Form von A2 (Kapitel 2, §2.2), angereichert um den klassenspezifischen Zerfall.

---

## 4.4 Gelderhaltung (I.4) und Geldschöpfung (M.1)

Geld ($\mathcal{K}_5$) erhält eine eigene Gleichung, weil seine Dynamik fundamental verschieden ist: Geld wird nicht *produziert*, sondern *geschöpft*.

> **Gleichung I.4 (Gelderhaltung).**
>
> $$\frac{\partial m}{\partial t} + \nabla \cdot \vec{j}_m = g - \tau$$

Dies ist die direkte Umsetzung von A3 (§2.3) als Feldgleichung. Die Quelle $g$ und die Senke $\tau$ werden in M.1 aufgeschlüsselt:

> **Gleichung M.1 (Drei Quellen der Geldschöpfung).**
>
> $$\dot{M} = \underbrace{g_{\mathcal{Z}}}_{\substack{\text{Zentralbank:}\\\text{Basisgeld}}} + \underbrace{g_{\mathcal{B}} \cdot \text{Kredit}_{\text{netto}}}_{\substack{\text{Geschäftsbanken:}\\\text{Giralgeld}}} - \underbrace{\tau_{\mathcal{G}}}_{\substack{\text{Steuertilgung:}\\\text{Geldvernichtung}}}$$

Die drei Kanäle:

**1. Zentralbank-Geldschöpfung $g_{\mathcal{Z}}$.** Die Zentralbank erzeugt Basisgeld $M_0$ durch Offenmarktoperationen (Kauf von Staatsanleihen), quantitative Lockerung (QE) und — perspektivisch — durch digitales Zentralbankgeld (CBDC). Der Term $g_{\mathcal{Z}} = \dot{M}_0$ ist eine *Kontrolvariable* der Zentralbank.

**2. Geschäftsbanken-Kreditschöpfung $g_{\mathcal{B}}$.** Jede Kreditvergabe erzeugt simultan ein Guthaben (auf dem Konto des Kreditnehmers) und eine Forderung (in der Bilanz der Bank). Netto-Kreditausweitung $\text{Kredit}_{\text{netto}} = \dot{L}_b > 0$ *schöpft* Geld; Kreditrückzahlung $\dot{L}_b < 0$ *vernichtet* Geld. Der Geldschöpfungsmultiplikator $g_{\mathcal{B}}$ hängt von der Vertrauenslage und den Basel-Anforderungen ab.

**3. Steuerliche Geldvernichtung $\tau_{\mathcal{G}}$.** Dieser Term erfordert Präzision: *Nicht jede Steuerzahlung vernichtet Geld.* Wenn ein Bürger Steuern zahlt und der Staat das Geld für Ausgaben verwendet (Löhne, Investitionen, Transfers), fließt es sofort in den privaten Kreislauf zurück — die umlaufende Geldmenge $M$ ändert sich nicht (das Geld wechselt nur den Besitzer). Geldvernichtung tritt *ausschließlich* dann ein, wenn der Staat die Steuereinnahmen zur *Schuldentilgung* verwendet — d.h. Staatsanleihen zurückkauft, die bei der Zentralbank oder im Bankensystem liegen. In diesem Fall ist die Tilgung die exakte *Umkehrung* der Geldschöpfung: So wie Kreditvergabe Geld erzeugt ($\Delta M = \Delta L > 0$), so vernichtet Kreditrückzahlung Geld ($\Delta M = \Delta L < 0$). Der Term $\tau_{\mathcal{G}}$ in M.1 misst daher nicht das Steueraufkommen, sondern den *netto-geldvernichtenden Anteil* der Fiskalpolitik: $\tau_{\mathcal{G}} = \text{Schuldentilgung}_\text{netto}$. In einer Volkswirtschaft mit konstantem Schuldenstand ($\dot{L}_{\text{Staat}} = 0$) ist $\tau_{\mathcal{G}} = 0$ — Steuern fließen vollständig als Ausgaben zurück.

### Die fundamentale Symmetrie der Kreditschöpfung

Aus M.1 folgt eine Eigenschaft, die alle anderen Quellen/Senken des Systems *nicht* haben:

> **Proposition 4.2 (Bilanzsymmetrie der Kreditschöpfung).** *Für jede Geldschöpfung durch Kreditvergabe gilt:*
>
> $$\Delta M = \Delta L$$
>
> *Das erzeugte Geld ist betragsmäßig identisch mit der erzeugten Schuld. Die Nettosumme aller monetären Positionen bleibt null:*
>
> $$\sum_{i \in \mathcal{A}} m_i^{\text{netto}} = 0$$

Dies ist die einzige Transaktion im System mit *perfekter* Bilanzsymmetrie. Alle anderen Quellen und Senken (Produktion, Konsum, Zerfall) erzeugen *echte* Nettoänderungen der realen Bestände.

### Die Bankbilanz (M.2)

Für die Konsistenz der Geldschöpfung muss die Bankbilanz jederzeit erfüllt sein:

$$\text{Aktiva: } L_b + K_b + R_b = D_b + E_b + B_b \text{ :Passiva} \tag{M.2}$$

| Aktivseite | Bedeutung | Passivseite | Bedeutung |
|---|---|---|---|
| $L_b$ | Kredite (Forderungen) | $D_b$ | Einlagen (Verbindlichkeiten) |
| $K_b$ | Realkapital (Gebäude, IT) | $E_b$ | Eigenkapital |
| $R_b$ | Reserven (bei Zentralbank) | $B_b$ | Anleihen (Refinanzierung) |

Die Basel-Beschränkung (NB.2) wirkt hier als *Transmissionsmechanismus*: Wenn $E_b$ sinkt (z.B. durch Kreditausfälle), muss $L_b$ sinken → weniger Kreditvergabe → weniger Geldschöpfung → monetäre Kontraktion. Dies ist der Kreditkanal der Krise — ein Mechanismus, der aus der Buchhaltungsidentität M.2 plus der regulatorischen Nebenbedingung NB.2 folgt, ohne jede Verhaltensannahme.

---

## 4.5 Was Erhaltung hier NICHT bedeutet

Der Begriff „Erhaltung" kann zu Missverständnissen führen, wenn man ihn physikalisch versteht (Energieerhaltung: $dE/dt = 0$). In der Ökonomie ist die Situation fundamental verschieden.

### Quellen und Senken: Die Asymmetrie der Ökonomie

Das physikalische Erhaltungsgesetz besagt: Energie kann weder erzeugt noch vernichtet werden. Die ökonomischen „Erhaltungsgleichungen" besagen lediglich: Bestandsänderungen müssen *genau einem der identifizierten Kanäle zugeordnet werden können*. Es gibt aber echte Quellen (Produktion, Geldschöpfung, Forschung) und echte Senken (Konsum, Zerfall, Steuertilgung).

Die vollständige Übersicht:

| Quelle/Senke | Variable | Gleichung | Bilanz-Symmetrie? |
|---|---|---|---|
| Güterproduktion | $n_k \uparrow$ | P.3: $+q_k$ | **Nein** — erzeugt Nettowert (Wertschöpfung) |
| Güterkonsum | $n_k \downarrow$ | P.3: $-c_k$ | **Nein** — vernichtet Wert |
| Abschreibung | $n_k \downarrow$ | P.3: $-\delta_k n_k$ | **Nein** — irreversibel |
| Kreditschöpfung | $M \uparrow$, $L \uparrow$ | M.1 | **Ja** — $\Delta M = \Delta L$ (netto null) |
| Konversion | $n_k^{(\alpha)} \downarrow$, $n_k^{(\beta)} \uparrow$ | K.1, P.4 | **Nein** — Profit $\Pi \neq 0$ möglich |
| Informationserzeugung | $\mathcal{I}_k \uparrow$ | I.1: $+\mathcal{S}_k$ | **Nein** — erzeugt nicht-rivales Gut |
| Informationszerfall | $\mathcal{I}_k \downarrow$ | I.1: $-\omega\mathcal{I}_k$ | **Nein** — irreversibel |
| Katastrophe | $n_k, K, N \downarrow$ | VIII.7 | **Nein** — exogene Vernichtung |

> **Beobachtung 4.1 (Einzigkeit der symmetrischen Transaktion).** *Die einzige Transaktion mit perfekter Bilanzsymmetrie ist die Kreditschöpfung ($\Delta M = \Delta L$). Alle anderen Quellen und Senken erzeugen echte Netto-Bestands- und Wertänderungen.*

### Wertschöpfung: Die Nicht-Erhaltung des ökonomischen Werts

Der ökonomische *Wert* — gemessen als $\sum_k p_k n_k$ — ist *nicht* erhalten. Er ändert sich durch drei Kanäle:

1. **Produktiver Mehrwert**: $\sum_k p_k q_k > \sum_k p_k d_k$ (Produktion erzeugt mehr Wert als Konsum vernichtet).
2. **Konversionsprofit**: Wenn aus billigen Inputs ($p_{\text{in}} n_{\text{in}}$) teure Outputs ($p_{\text{out}} n_{\text{out}}$) entstehen, ist die Differenz der Gewinn (P.4):

$$\Pi^{(\text{Konv})} = p_{\text{out}} \cdot \Delta n_{\text{out}} - \sum_{\text{in}} p_{\text{in}} \cdot |\Delta n_{\text{in}}| - w_L L^{(\text{Konv})} - rK^{(\text{Konv})} - \mathcal{C}(\mathcal{I})$$

3. **Bewertungsänderungen**: Preisänderungen $\dot{p}_k$ bewerten bestehende Bestände um — ohne dass sich physisch etwas ändert. Eine Aktienblase erhöht $\sum_k p_k n_k$ ohne Produktion.

Die Bruttowertschöpfung (BWS, „Gross Value Added") ist die Summe aller Konversionsprofite plus Löhne plus Kapitalerträge:

$$\text{BWS} = \sum_{\text{Konversionen}} \left(\Pi + w_L L + rK\right) = Y \tag{P.4b}$$

Dies ist die *Definition* des BIP. Sie folgt aus P.3 und P.4 — nicht als eigene Annahme, sondern als Konsequenz der Buchhaltungsidentitäten.

### Geschlossenes vs. offenes System

Für das *Gesamtsystem* (geschlossene Ökonomie, alle Agenten) gelten die Erhaltungssätze in ihrer einfachsten Form:

| Größe | Erhaltung | Bedeutung |
|---|---|---|
| Vermögen (aggregiert) | $\dot{W} = Y - C$ | Sparen $= $ Investition |
| Finanzpositionen | $\sum b_i = 0$ | Guthaben $=$ Schulden |
| Güter (innerhalb $\alpha$) | $\dot{n}^{(\alpha)}_{\text{total}} = q - c - \delta n + \text{Konversion}_{\text{netto}}$ | Produktion $-$ Verbrauch $-$ Zerfall |
| Geld (netto) | $\sum m_i^{\text{netto}} = 0$ | Forderungen $=$ Verbindlichkeiten |

Für *Teilsysteme* (ein Land, ein Sektor, ein Agent) kommen Flüsse hinzu — das Teilsystem ist offen.

---

## 4.6 Zusammenfassung und Bezüge

Die fünf Gleichungen dieses Kapitels und ihre Herkunft:

| Gleichung | Name | Axiom | Status |
|---|---|---|---|
| **I.1** | Individuelle Vermögensbilanz | A1 | Identität |
| **I.2** | Aggregierte Vermögenserhaltung | A1 (Summation) | Abgeleitete Identität |
| **P.3** | Güterbestandsdynamik (vollständig) | A2 + A9 + K.1 | Identität mit Quellen/Senken |
| **I.4** | Gelderhaltung | A3 | Identität |
| **M.1** | Geldschöpfungsgleichung | A3 (Zerlegung von $g$) | Institutionelle Aufschlüsselung |

Ergänzend: **P.4** (Konversionsprofit), **P.4b** (BIP-Identität), **M.2** (Bankbilanz), **NB.1** (Subsistenzkonsum), **NB.2** (Basel-Eigenkapital).

Diese Gleichungen stellen das *Skelett* des Systems dar — die buchhalterischen Identitäten, die unabhängig von jedem Verhalten gelten. In den folgenden Kapiteln füllen wir das Skelett mit Dynamik: Kapitel 5 beschreibt, *wie* die Flüsse $\vec{j}$ mit den Preisen $p_k$ zusammenhängen (Konstitutivgesetz A4). Kapitel 6 beschreibt, *wie* die Agenten ihre Entscheidungsvariablen $c_i$, $L_i$, $\theta_{ik}$ wählen (Verhaltensaxiome A5–A7).

Die Hierarchie ist klar:

$$\text{Axiome (Kap.\ 2)} \xrightarrow{\text{Ableitung}} \text{Erhaltung (Kap.\ 4)} \xrightarrow{\text{+ Konstitutivgesetz}} \text{Flüsse (Kap.\ 5)} \xrightarrow{\text{+ Verhalten}} \text{Entscheidungen (Kap.\ 6)}$$

Jede Schicht setzt die vorherigen voraus: Ohne Erhaltung keine konsistenten Bilanzen; ohne Flüsse keine Preisdynamik; ohne Verhalten keine Entscheidungen.

---

*Ende von Kapitel 4. Im folgenden Kapitel leiten wir ab, wie die Flüsse des Systems — Güter, Kapital, Geld, Information — mit den Preisen zusammenhängen.*

---

# Kapitel 5: Preise und Flüsse

---

Kapitel 4 hat die Bilanzen aufgestellt — *was* erhalten bleibt. Dieses Kapitel beantwortet eine andere Frage: *Wie bewegen sich die Dinge?* Genauer: Wie hängen die Ströme $\vec{j}$ (Güter, Kapital, Geld, Information) mit den treibenden Kräften (Preise, Renditen, Zinsgradienten) zusammen?

Die Antwort kommt aus Axiom A4 (§2.4): Alle ökonomischen Ströme fließen entlang des negativen Gradienten eines zugehörigen Potentials. Die zentrale Komplikation — und die zentrale Leistung dieses Kapitels — ist, dass Agenten *nicht* auf das objektive Potential reagieren, sondern auf ein *effektives* Potential, das objektiven Preis, Herding-Verzerrung und Informationskosten zusammenfasst.

Das Kapitel enthält sechs Gleichungen in vier Abschnitten:

| Gleichung | Gegenstand | Charakter |
|---|---|---|
| **II.2** | Preisdynamik | Fundamentale Preisgleichung (3 Komponenten) |
| **F.2** | Effektives Potential | Zusammensetzung aus $p + $ Herding $+$ Illiquidität |
| **F.1** | Allgemeiner Fluss | $\vec{j} = -D\nabla\mu^{\text{eff}}$ |
| **II.1** | Vermögensfluss | Diffusion + Konvektion im Vermögenspotential |
| **II.4** | Geldfluss | Zinsgradient + Kreditfeld |
| **II.3** | Informationsfluss | Reaktions-Diffusion (→ Detail in Kapitel 7) |

---

## 5.1 Preisdynamik (II.2)

Die Preisgleichung ist die vielleicht wichtigste Einzelgleichung des Systems — sie verbindet Angebot und Nachfrage, Erwartungen und Information in einer einzigen Formel.

> **Gleichung II.2 (Fundamentale Preisdynamik).**
>
> $$\dot{p}_k = \underbrace{\frac{1}{\lambda_k}(D_k - S_k)}_{\text{Walrasianische Anpassung}} + \underbrace{\eta_k\, p_k}_{\text{Inflationserwartung}} - \underbrace{\frac{\phi_k}{\mathcal{I}_k + \epsilon}}_{\text{Illiquiditätsprämie}}$$

Drei Komponenten, drei Zeitskalen, drei verschiedene Denktraditionen:

### Komponente 1: Walrasianische Anpassung

$$\dot{p}_k^{(1)} = \frac{1}{\lambda_k}(D_k - S_k)$$

Der Preis steigt, wenn die Nachfrage $D_k$ das Angebot $S_k$ übersteigt. Der Parameter $\lambda_k > 0$ ist die *Markttiefe* — er misst, wie stark der Preis auf Überschussnachfrage reagiert. Ein großes $\lambda_k$ bedeutet einen tiefen, liquiden Markt (viele Marktteilnehmer, hohe Transaktionsvolumina); ein kleines $\lambda_k$ einen dünnen Markt, in dem kleine Nachfrageänderungen große Preisausschläge verursachen.

| Markt | Typisches $\lambda_k$ | Konsequenz |
|---|---|---|
| US-Staatsanleihen | Sehr groß | Extrem stabile Preise |
| Blue-Chip-Aktien | Groß | Moderate Volatilität |
| Small-Cap-Aktien | Mittel | Hohe Volatilität |
| Immobilien | Klein | Träge Preisanpassung |
| Kryptowährungen | Sehr klein | Extreme Ausschläge |

Dieser Term ist die *Marshallianische Preisanpassung* — der Kern der neoklassischen Theorie. In unserem System ist er lediglich der erste von drei Termen.

### Komponente 2: Inflationserwartungsdrift

$$\dot{p}_k^{(2)} = \eta_k\, p_k$$

Der Preis driftet mit Rate $\eta_k$ mit der Inflationserwartung. Wenn Agenten positive Inflation erwarten ($\eta_k > 0$), steigt der Preis auch *ohne* Überschussnachfrage — eine selbsterfüllende Prophezeiung. Im Gleichgewicht gilt $\eta_k = \pi^*$ (Zielinflation der Zentralbank). In Panikphasen kann $\eta_k$ stark ansteigen (Hyperinflationserwartung) oder negativ werden (Deflationserwartung).

Der Parameter $\eta_k$ ist *endogen* — er wird durch die Erwartungsgleichung III.4 (Kapitel 6, §6.7) bestimmt. Die Kopplung $\text{II.2} \leftrightarrow \text{III.4}$ ist eine der zirkulären Abhängigkeiten, die das System simultan und nicht rekursiv machen.

### Komponente 3: Illiquiditätsprämie

$$\dot{p}_k^{(3)} = -\frac{\phi_k}{\mathcal{I}_k + \epsilon}$$

Dies ist der originellste — und folgenreichste — Term. Er besagt: Wenn die Information über ein Gut sinkt ($\mathcal{I}_k \to 0$), fällt der Preis. Die Intuition: Wenn niemand Bescheid weiß (keine Analysten, keine Nachrichten, keine Transaktionshistorie), kann niemand den Wert einschätzen — die Agenten ziehen sich zurück, die Nachfrage bricht ein, der Preis fällt.

Die mathematische Struktur ist eine *Singularität*: Für $\mathcal{I}_k \to 0$ divergiert der Abwärtsdruck:

| $\mathcal{I}_k$-Niveau | Interpretation | Illiquiditätsterm |
|---|---|---|
| $0{,}5$–$1{,}0$ | Normal | $-\phi_k$ bis $-2\phi_k$ |
| $0{,}1$–$0{,}2$ | Stress | $-5\phi_k$ bis $-10\phi_k$ |
| $0{,}01$ | Panik | $-100\phi_k$ |
| $\to \epsilon$ | Markteinfrierung | $\to -\phi_k/\epsilon$ (divergiert) |

Diese Singularität ist kein mathematisches Artefakt, sondern der *Mechanismus* für:

- **Flash-Crashs** (Mai 2010, Oktober 2014): Plötzlicher Informationskollaps → Preisverfall in Sekunden.
- **Markteinfrierer** (September 2008, März 2020): Informationsasymmetrie wird so groß, dass kein Preis den Markt räumen kann — Akerlofs (1970) Lemon-Problem in extremis.
- **Illiquiditätsspiralen** (Brunnermeier & Pedersen 2009): Fallende Preise → sinkende Sicherheitenwerte → Margin-Calls → erzwungene Verkäufe → weiter fallende Preise.

Der Regularisierungsparameter $\epsilon > 0$ verhindert die *mathematische* Divergenz ($1/0$), hat aber einen *ökonomischen* Sinn: Er repräsentiert die *Restinformation*, die selbst in völliger Panik vorhanden bleibt (z.B. die physische Existenz eines Guts ist bekannt, auch wenn sein Marktwert unbekannt ist).

### Das Zusammenspiel der drei Komponenten

In normalen Zeiten dominiert Term 1 (Walrasianische Anpassung) — der Preis konvergiert zum Angebot-Nachfrage-Gleichgewicht. In Blasenphasen dominiert Term 2 (Inflationserwartung) — Preise steigen, weil alle steigende Preise erwarten. In Krisen dominiert Term 3 (Illiquidität) — Preise stürzen ab, weil niemand mehr Bescheid weiß.

> **Proposition 5.1 (Regimeabhängige Preisdynamik).** *Das dominante Regime der Preisgleichung II.2 hängt vom Informationsniveau $\mathcal{I}_k$ ab:*
>
> | Regime | Bedingung | Dominanter Term | Verhalten |
> |---|---|---|---|
> | *Gleichgewicht* | $D \approx S$, $\mathcal{I}$ hoch | Keiner (alle klein) | $\dot{p} \approx 0$ |
> | *Normaler Handel* | $D \neq S$, $\mathcal{I}$ mittel | Walrasianisch $(\lambda^{-1}(D-S))$ | Monotone Konvergenz |
> | *Blase* | $\eta_k$ groß, $\mathcal{I}$ hoch | Erwartungsdrift $(\eta p)$ | Exponentielles Wachstum |
> | *Krise* | $\mathcal{I} \to 0$ | Illiquiditätsprämie $(-\phi/\mathcal{I})$ | Preiskollaps |

Die *Übergänge* zwischen diesen Regimen sind nicht exogen — sie werden durch die Schwellenwertdynamik (Kapitel 10) und die Rückkopplung zwischen Preis, Information und Herding endogen erzeugt.

---

## 5.2 Das effektive Potential (F.2)

Axiom A4 besagt, dass Ströme dem negativen Gradienten eines Potentials folgen. Aber *welches* Potential? In der neoklassischen Theorie ist die Antwort einfach: der Preis $p_k$. In unserem System ist die Antwort komplexer: Agenten reagieren auf das *effektive* Potential, das den objektiven Preis um zwei Verzerrungen korrigiert.

> **Gleichung F.2 (Effektives Potential).**
>
> $$\mu_k^{\text{eff}}(\mathbf{x}, t) = \underbrace{p_k(\mathbf{x}, t)}_{\text{Objektiver Preis}} + \underbrace{\alpha_H \cdot \bar{p}_k^{\text{Herding}}(\mathbf{x}, t)}_{\text{Herding-Verzerrung}} + \underbrace{\frac{\psi_k}{\mathcal{I}_k(\mathbf{x}, t) + \epsilon}}_{\text{Illiquiditätszuschlag}}$$

Drei Schichten, die das Potential zusammensetzen:

### Schicht 1: Objektiver Preis $p_k$

Der Marktpreis, bestimmt durch II.2. Dies ist das Potential, auf das ein perfekt informierter, nicht beeinflussbarer Agent reagieren würde. Im Grenzfall $\alpha_H = 0$ und $\mathcal{I} \to \infty$ gilt $\mu^{\text{eff}} = p_k$ — das effektive Potential reduziert sich auf den Preis, und F.1 wird zum neoklassischen Arbitrageprinzip.

### Schicht 2: Herding-Verzerrung $\alpha_H \bar{p}_k^{\text{Herding}}$

Der Term $\bar{p}_k^{\text{Herding}}$ ist der *lokale Peer-gewichtete Durchschnitt* der Konsum-/Portfolioentscheidungen in der Nachbarschaft des Agenten — die effektive Adjazenz V.7 gewichtet die Signals:

$$\bar{p}_k^{\text{Herding}}(\mathbf{x}, t) = \sum_{j \in \mathcal{N}(i)} A_{ij}^{\text{eff}}\, \theta_{jk}$$

Wenn die Nachbarn eines Agenten Gut $k$ kaufen ($\theta_{jk}$ hoch), erscheint $k$ attraktiver als sein Preis allein nahelegt → das effektive Potential steigt → der Fluss in Richtung $k$ steigt. Dies ist der Transmissionsmechanismus von Blasen: Steigende Käufe → steigende wahrgenommene Attraktivität → noch mehr Käufe.

Der Parameter $\alpha_H \geq 0$ ist die *Herding-Empfindlichkeit*:

| $\alpha_H$ | Verhalten | Grenzfall |
|---|---|---|
| $0$ | Kein Herding — rein rationaler Agent | Arrow-Debreu |
| Klein | Schwache Peerbeeinflussung (Normalfall) | Moderate Zyklen |
| Groß | Starkes Herding — Agentenentscheidungen konvergieren | Blasen, Crashs |
| $\to \infty$ | Vollständige Synchronisation — alle Agenten handeln gleich | Herdenlauf |

$\alpha_H$ ist *selbst endogen* — er steigt in Stressphasen (Verunsicherung → Orientierung an anderen) und sinkt in Normalphasen (Selbstvertrauen → eigene Entscheidung). Die Dynamik von $\alpha_H$ folgt aus den endogenen Parametern VI.1–VI.9 (Kapitel 6, §6.9).

### Schicht 3: Illiquiditätszuschlag $\psi_k / (\mathcal{I}_k + \epsilon)$

Wenn die Information über Gut $k$ niedrig ist ($\mathcal{I}_k$ klein), steigt der effektive Preis: Der Agent muss mehr „bezahlen" (in Form von Suchkosten, Risikozuschlag, Bewertungsunsicherheit), um Gut $k$ zu erwerben. Dies ist die *Transaktionskostenkomponente* des effektiven Potentials — sie folgt direkt aus Axiom A10 (Informationskosten sind konvex).

Die ökonomische Logik: Ein Agent, der ein CDO kaufen möchte ($\mathcal{I}$ niedrig), muss erheblichen Aufwand treiben, um den wahren Wert einzuschätzen (Due Diligence, Rating-Reports, Marktanalyse). Dieser Aufwand erhöht den *effektiven* Preis — selbst wenn der nominale Marktpreis niedrig ist. Im Ergebnis fließen weniger Güter in die Hand von uninformierten Agenten, als es der Nominalpreis allein nahelegen würde.

### Regimeanalyse des effektiven Potentials

Die Zusammensetzung von F.2 ändert sich je nach Marktzustand dramatisch:

**Normalphase** ($\mathcal{I}$ moderat, $\alpha_H$ klein):
$$\mu^{\text{eff}} \approx p_k + \text{kleine Korrekturen}$$
Flüsse sind *nahezu rational* — der Markt funktioniert im Wesentlichen effizient.

**Blasenphase** ($\mathcal{I}$ hoch, $\alpha_H$ groß):
$$\mu^{\text{eff}} \gg p_k \qquad (\text{Herding dominiert})$$
Das effektive Potential übersteigt den objektiven Preis — Kapital fließt in überbewertete Assets. Selbstverstärkende Schleife: Zufluss → Preisanstieg → noch höheres $\mu^{\text{eff}}$ → noch mehr Zufluss.

**Krisenphase** ($\mathcal{I} \to 0$, $\alpha_H$ dreht um):
$$\mu^{\text{eff}} \to +\infty \qquad (\text{Illiquiditätszuschlag explodiert})$$
Das effektive Potential wird unendlich groß → *kein* Fluss mehr in Richtung dieses Guts → Markt friert ein. Gleichzeitig dreht der Herding-Term um ($\bar{p}^{\text{Herding}}$ negativ) → Alle verkaufen → Preiskaskade nach unten.

> **Proposition 5.2 (Drei Regime des effektiven Potentials).** *Das qualitative Verhalten des effektiven Potentials F.2 wird durch zwei Parameter bestimmt:*
>
> $$\mathcal{R}_1 = \frac{\alpha_H |\bar{p}^H|}{p_k} \qquad (\text{relative Herding-Stärke})$$
> $$\mathcal{R}_2 = \frac{\psi_k}{p_k (\mathcal{I}_k + \epsilon)} \qquad (\text{relative Illiquidität})$$
>
> | $\mathcal{R}_1$ | $\mathcal{R}_2$ | Regime | Marktcharakter |
> |---|---|---|---|
> | $\ll 1$ | $\ll 1$ | Effizient | Preise spiegeln Fundamentale |
> | $\gg 1$ | $\ll 1$ | Blase | Preise über Fundamentalen |
> | beliebig | $\gg 1$ | Krise | Marktversagen (Illiquidität) |

---

## 5.3 Flüsse auf effektiven Potentialen (F.1)

Mit dem effektiven Potential (F.2) definiert, ergibt sich der allgemeine Fluss als direkte Anwendung von A4:

> **Gleichung F.1 (Allgemeiner Fluss).**
>
> $$\vec{j}_{n_k} = -D_k\, \nabla \mu_k^{\text{eff}}$$

Güter fließen in Richtung des *fallenden* effektiven Potentials — vom „teuren" zum „billigen" Standort, wobei „teuer" und „billig" durch $\mu^{\text{eff}}$ (nicht durch $p_k$ allein) definiert sind.

Die Diffusionskonstante $D_k > 0$ ist ein *physischer* Parameter — sie hängt von der Transportinfrastruktur ab:

| Flusstyp | $D_k$ hängt ab von | Typische Größenordnung |
|---|---|---|
| Physische Güter ($\mathcal{K}_1$–$\mathcal{K}_3$) | Straßenetz, Häfen, Logistik | $10^1$–$10^3$ km$^2$/Jahr |
| Kapital ($\mathcal{K}_2$) | Finanzinfrastruktur, Regulierung | $10^4$–$10^6$ km$^2$/Jahr |
| Geld ($\mathcal{K}_5$) | Zahlungssysteme, SWIFT, Blockchain | $10^6$–$10^8$ km$^2$/Jahr |
| Information ($\mathcal{K}_6$) | Internet, Medien, Telekommunikation | $10^8$–$10^{10}$ km$^2$/Jahr |

Die Diffusionskonstanten spannen *zehn Größenordnungen* — Information diffundiert millionenfach schneller als physische Güter. Diese Skalentrennung hat tiefgreifende Konsequenzen: Preise (die auf Information reagieren) passen sich in Millisekunden an; Güterströme (die auf Logistik angewiesen sind) in Monaten. Das Ergebnis ist eine *permanente Entkopplung* zwischen Finanz- und Realökonomie — eine der zentralen Pathologien moderner Volkswirtschaften.

### Der Zusammenhang zwischen A4 und F.1

F.1 ist die *generalisierte* Version von A4. Die Hierarchie:

| Ebene | Gleichung | Potential | Voraussetzung |
|---|---|---|---|
| Axiom A4 | $\vec{j} = -D\nabla p_k$ | Objektiver Preis | Perfekte Information, kein Herding |
| F.1 | $\vec{j} = -D\nabla\mu^{\text{eff}}$ | Effektives Potential | Begrenzte Rationalität |
| Grenzfall | $\text{F.1} \to \text{A4}$ | $\mu^{\text{eff}} \to p_k$ | wenn $\alpha_H = 0$, $\psi_k = 0$, $\mathcal{I} \to \infty$ |

Der Arrow-Debreu-Grenzfall (Kapitel 16) entsteht genau dann, wenn alle Verhaltensverzerrungen verschwinden: kein Herding ($\alpha_H = 0$), keine Transaktionskosten ($\psi_k = 0$), vollständige Information ($\mathcal{I} \to \infty$). Dann ist $\mu^{\text{eff}} = p_k$, und F.1 reduziert sich auf das neoklassische Arbitrageprinzip.

### Einsetzen von F.2 in F.1: Die expandierte Flussgleichung

Für die konkrete Berechnung setzt man F.2 in F.1 ein:

$$\vec{j}_{n_k} = -D_k\left[\nabla p_k + \alpha_H\, \nabla\bar{p}_k^{\text{Herding}} + \nabla\!\left(\frac{\psi_k}{\mathcal{I}_k + \epsilon}\right)\right]$$

$$= -D_k\,\nabla p_k - D_k\,\alpha_H\,\nabla\bar{p}_k^{\text{Herding}} + D_k\,\frac{\psi_k}{(\mathcal{I}_k + \epsilon)^2}\,\nabla\mathcal{I}_k$$

Der dritte Term zeigt eine bemerkenswerte Struktur: Er treibt Güter *in Richtung steigender Information* ($\nabla\mathcal{I}_k > 0$). Dies ist der *Informationssog*: Güter fließen dorthin, wo man am besten über sie Bescheid weiß — ein Mechanismus, der erklärt, warum Handelsströme an bekannten Routen hängen und warum neue Märkte nur langsam erschlossen werden.

---

## 5.4 Vermögensfluss (II.1)

Die Vermögensdynamik aus I.1 (§4.1) beschreibt, wie sich das Vermögen eines einzelnen Agenten ändert. Auf der *räumlichen* Ebene gibt es zusätzlich einen Fluss von Vermögen zwischen Standorten. Bevor wir die Flussgleichung formulieren, definieren wir die beiden Felder, die sie antreiben.

### Vermögensdichte

> **Definition 5.1 (Vermögensdichte).** *Die Vermögensdichte $\rho_w(\mathbf{x}, t)$ am Ort $\mathbf{x}$ zur Zeit $t$ ist:*
>
> $$\rho_w(\mathbf{x}, t) = \frac{1}{|\Omega(\mathbf{x})|}\sum_{i \in \Omega(\mathbf{x})} w_i(t)$$
>
> *wobei $\Omega(\mathbf{x})$ die lokale Nachbarschaft um $\mathbf{x}$ und $|\Omega(\mathbf{x})|$ deren Volumen (Fläche, Einwohnerzahl) ist.*

$\rho_w$ ist die *lokale Vermögenskonzentration* — sie misst, wie viel Vermögen pro Raumeinheit an einem Punkt gebunden ist. Sie ist das ökonomische Analogon zur Massendichte in der Fluiddynamik. Hohe Vermögensdichte: Finanzzentren (London, New York, Zürich). Niedrige Vermögensdichte: periphere Regionen.

### Vermögenspotential

Das Vermögenspotential $\Phi_w$ spielt für Kapitalströme dieselbe Rolle wie das effektive Potential $\mu_k^{\text{eff}}$ (F.2, §5.2) für Güterströme: Es bestimmt, *wohin* Kapital fließt. Seine axiomatischen Eigenschaften sind:

> **Definition 5.2 (Vermögenspotential).** *Das Vermögenspotential $\Phi_w(\mathbf{x}, t)$ ist ein skalares Feld mit folgenden Eigenschaften:*
>
> $$\Phi_w(\mathbf{x}, t) = \underbrace{h(\rho_w)}_{\text{Konzentrationsterm}} + \underbrace{\beta_w \, V_w(\mathbf{x})}_{\text{Standortattraktivität}}$$
>
> *wobei:*

| Komponente | Eigenschaft | Interpretation |
|---|---|---|
| $h(\rho_w)$ | $h' < 0$ (fallend in $\rho_w$) | Kapital fließt *von* hoher Konzentration *weg* (Diversifikation) |
| $V_w(\mathbf{x})$ | Exogenes Standortpotential | Infrastruktur, Institutionenqualität, Rechtsstaatlichkeit |
| $\beta_w > 0$ | Sensitivitätsparameter | Wie stark Kapital auf Standortqualität reagiert |

*Axiomatische Eigenschaften:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Diversifikationstrieb** | $\frac{\partial \Phi_w}{\partial \rho_w} < 0$ | Hohe Konzentration → hohes Potential → Kapital fließt ab |
| **Standortanziehung** | $\frac{\partial \Phi_w}{\partial V_w} > 0$ | Gute Institutionen → hohes Potential → Kapital fließt zu |
| **Gradientenfluss** | $\vec{j}_w \propto -\nabla\Phi_w$ | Kapital fließt entlang des negativen Gradienten (A4) |
| **Gleichgewicht** | $\nabla\Phi_w = 0 \Rightarrow \vec{j}_w^{\text{diff}} = 0$ | Kein Potentialgradient → kein diffusiver Fluss |

Der Gradient des Vermögenspotentials zerlegt sich in zwei Kräfte:

$$-\nabla\Phi_w = \underbrace{-h'(\rho_w)\nabla\rho_w}_{\text{Diffusion: weg von Konzentration}} - \underbrace{\beta_w\nabla V_w}_{\text{Drift: hin zu Attraktivität}}$$

Die beiden Kräfte wirken oft *gegeneinander*: Diversifikation treibt Kapital aus Finanzzentren, aber Standortattraktivität zieht es dorthin zurück. Im Gleichgewicht balancieren sich beide — das Ergebnis ist die beobachtete räumliche Vermögensverteilung.

### Die Flussgleichung

> **Gleichung II.1 (Vermögensfluss).**
>
> $$\vec{j}_w = -D_w\,\nabla\Phi_w + \vec{v}_w\,\rho_w$$

| Term | Bedeutung | Physikalische Analogie |
|---|---|---|
| $-D_w\nabla\Phi_w$ | Diffusiver Fluss entlang des Vermögenspotentials | Ficksches Gesetz |
| $\vec{v}_w\rho_w$ | Konvektiver Fluss: Vermögensdichte wird mit Driftgeschwindigkeit $\vec{v}_w$ transportiert | Advektion |

**Diffusiver Term.** Vermögen fließt von Regionen hohen Vermögenspotentials zu Regionen niedrigen Potentials — Kapital sucht Rendite. Der Diffusionskoeffizient $D_w > 0$ hängt von der Kapitalmarktliberalisierung ab: In einem vollständig offenen Markt ist $D_w$ groß (Kapital fließt frei); bei Kapitalverkehrskontrollen ist $D_w$ klein oder null.

**Konvektiver Term.** Zusätzlich zur Diffusion gibt es eine *gerichtete Drift* $\vec{v}_w$ — die systematische Bewegung von Kapital in eine bestimmte Richtung, getrieben durch institutionelle Kanäle (Zentralbank-Interventionen, staatliche Investitionsprogramme, Carry-Trade-Ströme).

**Das Lucas-Paradox.** II.1 erklärt das berühmte Lucas-Paradox (1990): Warum fließt Kapital nicht von reichen in arme Länder (wie es die neoklassische Theorie vorhersagt)? Antwort: Weil $\Phi_w$ nicht nur die Vermögenskonzentration enthält, sondern auch die Standortattraktivität $V_w$ — und $V_w$ korreliert mit Institutionenqualität, Informationsstand und Rechtssicherheit. Für arme Länder mit schwachen Institutionen ist $V_w$ niedrig, also $\Phi_w$ *trotz niedriger Konzentration* nicht hoch genug — das Potential zieht kein Kapital an. Im Grenzfall $V_w^{\text{arm}} \ll V_w^{\text{reich}}$ fließt Kapital *von* arm *nach* reich (Kapitalflucht), was empirisch beobachtet wird.

---

## 5.5 Geldfluss (II.4)

Geld hat eine eigene Flussgleichung, weil sein Antrieb sich von dem physischer Güter unterscheidet: Geld fließt nicht primär entlang von Preisgradienten, sondern entlang von *Zinsgradienten* und entlang des *Kreditfeldes*.

> **Gleichung II.4 (Geldfluss).**
>
> $$\vec{j}_m = -D_m\,\nabla r + \sigma_m\,\vec{E}_{\text{Kredit}}$$

| Term | Bedeutung | Treibende Kraft |
|---|---|---|
| $-D_m\nabla r$ | Geld fließt in Richtung *höherer* Zinsen | Zinsdifferenz (spread) |
| $\sigma_m\vec{E}_{\text{Kredit}}$ | Geld fließt entlang des Kreditanreizfeldes | Kreditvergabe der Banken |

**Zinsgradient-Term.** Wenn in Region A der Zins höher ist als in Region B ($\nabla r$ zeigt von B nach A), fließt Geld von B nach A ($-\nabla r$ zeigt nach A). Dies ist die Grundlage des *Carry Trade*: Geld wird in Niedrigzinswährungen aufgenommen und in Hochzinswährungen angelegt.

Der Diffusionskoeffizient $D_m$ misst die Geschwindigkeit der monetären Anpassung — er ist in modernen Volkswirtschaften mit elektronischem Zahlungsverkehr erheblich höher als in bargeldbasierten Systemen.

**Kreditfeld-Term.** Das „Kreditfeld" $\vec{E}_{\text{Kredit}}$ ist eine Analogie zum elektrischen Feld: Banken erzeugen durch Kreditvergabe ein *Anreizfeld*, das Geld in Richtung kreditwürdiger Agenten lenkt. Formal:

$$\vec{E}_{\text{Kredit}} = -\nabla\Phi_{\text{Kredit}}$$

wobei $\Phi_{\text{Kredit}}$ das Kreditpotential ist — hoch dort, wo Banken aktiv Kredite vergeben; niedrig dort, wo sie Kredit einschränken (Credit Crunch). Die Kopplungskonstante $\sigma_m$ misst, wie stark das Kreditfeld den Geldfluss beeinflusst.

**Die zwei Regime des Geldflusses:**

| Regime | Dominanter Term | Situation | Beispiel |
|---|---|---|---|
| *Zinsgetrieben* | $-D_m\nabla r$ | Normale Geldpolitik | Carry Trade, Kapitalimporte |
| *Kreditgetrieben* | $\sigma_m\vec{E}_{\text{Kredit}}$ | Quantitative Lockerung, Credit Crunch | QE (2009–2022): $r \approx 0$, aber $\vec{E}_{\text{Kredit}}$ massiv |

Wenn der Zinssatz an der Nullzinsgrenze liegt ($r \to 0$, Liquiditätsfalle), verschwindet der erste Term ($\nabla r \approx 0$). Der Geldfluss wird dann *vollständig* durch den Kreditkanal bestimmt — dies erklärt, warum quantitative Lockerung (QE) trotz Nullzins expansiv wirkt: Die Zentralbank verändert $\vec{E}_{\text{Kredit}}$, nicht $r$.

---

## 5.6 Informationsfluss (II.3) — Vorschau

Die Informationsdynamik hat eine eigene, reichere Struktur als die anderen Flüsse und wird in Kapitel 7 vollständig behandelt. Hier geben wir nur die Gleichung und ihre Position im Flusssystem:

> **Gleichung II.3 (Informationspropagation).**
>
> $$\dot{\mathcal{I}}_k = \underbrace{D_{\mathcal{I}}\,\nabla^2 \mathcal{I}_k}_{\text{Diffusion}} - \underbrace{\omega\,\mathcal{I}_k}_{\text{Zerfall}} + \underbrace{\mathcal{S}_k}_{\text{Quellen}} - \underbrace{\mu\,\mathcal{I}_k^3}_{\text{Sättigung}} + \underbrace{\beta\,|\dot{p}_k|}_{\text{Preis-Feedback}}$$

Fünf Terme, die in Kapitel 7 (§7.1) im Detail behandelt werden. Hier ist nur die *Kopplung* zu den Preisen relevant:

**Rückkopplung Preis → Information.** Der Term $\beta|\dot{p}_k|$ besagt: Starke Preisbewegungen erzeugen Information. Ein Aktienkurs, der um 10% fällt, generiert Nachrichten, Analysen, Marktkommentare — die Informationsdichte $\mathcal{I}_k$ *steigt*. Dies ist der „Events create news"-Mechanismus.

**Rückkopplung Information → Preis.** Über den Illiquiditätsterm in II.2: Sinkende $\mathcal{I}_k$ lässt den Preis fallen ($-\phi/\mathcal{I}$). Beide Rückkopplungen zusammen erzeugen zwei mögliche Spiralen:

| Spirale | Mechanismus | Ergebnis |
|---|---|---|
| **Stabilisierend** | Preis fällt → News erzeugt ($\beta|\dot{p}|$) → $\mathcal{I}$ steigt → Illiquiditätsprämie sinkt → Preis erholt sich | Selbstkorrektur |
| **Destabilisierend** | Preis fällt → Agenten fliehen → Analysten verlassen den Markt → $\mathcal{I}$ sinkt *trotz* Preisfall → Illiquidität steigt → Preis fällt weiter | Illiquiditätsspirale |

Welche Spirale dominiert, hängt vom Regime ab: In normalen Zeiten stabilisiert das Preis-Feedback; in Krisen destabilisiert der Analystenflucht-Mechanismus. Der Kipppunkt wird durch Schw.1 (Kapitel 10) bestimmt.

---

## 5.7 Das Flusssystem als Ganzes: Kausale Kopplung

Die sechs Gleichungen dieses Kapitels bilden ein gekoppeltes System — sie sind nicht sequenziell, sondern simultan:

$$\text{II.2} \underset{\dot{p} \to \beta|\dot{p}| \to \mathcal{I}}{\overset{\mathcal{I} \to -\phi/\mathcal{I}}{\rightleftarrows}} \text{II.3} \qquad \text{II.2} \underset{p \to \mu^{\text{eff}}}{\overset{\vec{j} \to D,S}{\rightleftarrows}} \text{F.1/F.2} \qquad \text{II.4} \underset{g \to M}{\overset{r \to \eta}{\rightleftarrows}} \text{II.2}$$

Die vollständige kausale Kette:

1. **Konsumentscheidung** (V.1–V.3, Kapitel 6) → Nachfrage $D_k$
2. **Produktionsentscheidung** (III.3, Kapitel 6) → Angebot $S_k$
3. **Preisanpassung** (II.2): $D_k - S_k \to \dot{p}_k$
4. **Effektives Potential** (F.2): $p_k + \text{Herding} + \text{Illiquidität} \to \mu^{\text{eff}}$
5. **Güterflüsse** (F.1): $-D\nabla\mu^{\text{eff}} \to \vec{j}_{n_k}$
6. **Lokale Vermögensänderung** (I.1 + F.1): $w_i$ ändert sich → neue Nachfrage → zurück zu 1.
7. **Kreditvermittlung** ($\mathcal{B}$): Vermögensänderung → Kreditwürdigkeit → M.1 → Geldmenge ändert sich
8. **Geldflüsse** (II.4): Zinsgradienten + Kreditfeld → $\vec{j}_m$
9. **Informationsdiffusion** (II.3): Neuigkeiten breiten sich aus, veralten, werden produziert
10. **Rückkopplung** (II.3 → F.2): Informationsstand verändert effektives Potential → neue Flüsse

Alle zehn Schritte laufen *simultan* ab — es gibt keine kausale Reihenfolge, nur eine konzeptuelle. Das System ist ein *gekoppeltes PDE-System*, das selbstreferenziell ist: Preise beeinflussen Flüsse, Flüsse beeinflussen Bestände, Bestände beeinflussen Preise.

> **Beobachtung 5.1 (Finanz-Real-Entkopplung).** *Die Diffusionskonstanten für Geld und Information ($D_m, D_{\mathcal{I}}$) sind Größenordnungen schneller als für physische Güter ($D_k$). In Kombination mit der simultanen Kopplung bedeutet dies: Die Finanzsphäre reagiert in Millisekunden (Hochfrequenzhandel), während die Realökonomie in Monaten anpasst. Die resultierende Entkopplung — Finanzpreise bewegen sich, als ob die Wirtschaft bereits reagiert hätte, aber die Wirtschaft reagiert erst Quartale später — ist eine fundamentale Pathologie, die das System endogen erzeugt.*

### Zusammenfassung

| Gleichung | Name | Ableitung aus | Bestimmt |
|---|---|---|---|
| **II.2** | Preisdynamik | A2 + A4 + A10 | Preis $p_k(t)$ |
| **F.2** | Effektives Potential | A4 + A6 + A10 | $\mu_k^{\text{eff}}(\mathbf{x}, t)$ |
| **F.1** | Allgemeiner Fluss | A4 + F.2 | $\vec{j}_{n_k}(\mathbf{x}, t)$ |
| **II.1** | Vermögensfluss | A1 + A4 | $\vec{j}_w(\mathbf{x}, t)$ |
| **II.4** | Geldfluss | A3 + A4 | $\vec{j}_m(\mathbf{x}, t)$ |
| **II.3** | Informationsfluss | A9($\mathcal{K}_6$) + A4 | $\dot{\mathcal{I}}_k(\mathbf{x}, t)$ → Detail Kap. 7 |

Die Erhaltungsgleichungen (Kapitel 4) plus die Flussgleichungen (Kapitel 5) bilden zusammen das *physikalische Gerüst* des Systems — Bilanzen und Transportgesetze. Was noch fehlt, ist der *Agent*: Wie wählen die Agenten ihre Entscheidungsvariablen $c_i$, $L_i$, $\theta_{ik}$? Das ist das Thema des nächsten Kapitels.

---

*Ende von Kapitel 5. Im folgenden Kapitel beschreiben wir die Drei-Ebenen-Architektur der Agenten-Entscheidungen: rational, psychologisch, sozial.*

---

# Kapitel 6 — Entscheidungen: Die Drei-Ebenen-Architektur

Die Kapitel 4 und 5 haben das *physikalische Gerüst* aufgestellt: Bilanzen sagen, was erhalten bleibt; Flussgleichungen sagen, wohin die Dinge strömen. Aber *warum* strömen sie? Was treibt die Agenten, ihre Entscheidungsvariablen — Konsum $c_i$, Arbeit $L_i$, Portfolio $\theta_{ik}$, Produktion $q_k$ — so und nicht anders zu wählen?

Die neoklassische Antwort lautet: rationale Nutzenmaximierung unter Nebenbedingungen. Diese Antwort ist nicht falsch — sie ist unvollständig. Empirisch reagieren Agenten auf Referenzpunkte (Kahneman & Tversky 1979), auf das Verhalten ihrer Nachbarn (Banerjee 1992), auf Burnout (Bakker & Demerouti 2007), auf Statussorgen (Frank 1985). Diese Phänomene sind keine Randerscheinungen — sie sind die Regel.

Unser Framework löst dieses Problem durch eine *additive Drei-Ebenen-Architektur*: Jede Entscheidungsgröße $x_i$ eines Agenten folgt einer Dynamik der Form

$$\dot{x}_i = \underbrace{\text{Rationale Komponente}}_{\text{Ebene 1}} + \underbrace{\text{Psychologische Modifikation}}_{\text{Ebene 2}} + \underbrace{\text{Soziale Kopplung}}_{\text{Ebene 3}}$$

Die drei Ebenen addieren sich, dominieren aber in verschiedenen Situationen (§6.10). In normalen Zeiten dominiert Ebene 1 — das System verhält sich approximativ neoklassisch. In Stressphasen übernehmen Ebenen 2 und 3 — und erzeugen Dynamiken, die rein rationale Modelle prinzipiell nicht abbilden können.

Dieses Kapitel ist mit Abstand das gleichungsreichste der Monographie. Es enthält die folgenden Gleichungen:

| Gleichung | Gegenstand | Ebene |
|---|---|---|
| **U.1** | Erweiterte Nutzenfunktion | Fundament |
| **U.2** | Informationsgewichte | Fundament |
| **U.3** | Effektiver Preis | Fundament |
| **V.1** | Rationaler Konsum | 1 |
| **V.1a** | Wahrgenommener Zins | 1 (informationsgefiltert) |
| **V.2** | Psychologische Konsumverzerrung | 2 |
| **V.3** | Soziale Konsumkopplung | 3 |
| **L.1** | Rationaler Arbeitskern | 1 |
| **L.1a** | Wahrgenommener Alternativlohn | 1 (informationsgefiltert) |
| **L.2** | Psychologische Arbeitsverzerrung | 2 |
| **L.3** | Soziale Arbeitskopplung | 3 |
| **L.4** | Integrierte Arbeitsdynamik | 1+2+3 |
| **III.3** | Produktion | 1 |
| **III.2** | Portfolio | 1+3 |
| **III.4** | Erwartungsbildung | hybrid |
| **L.5** | Unternehmerische Risikoentscheidung | 1 (informationsmoduliert) |
| **VI.1–VI.9** | Endogene Verhaltensparameter | Meta-Ebene |

---

## 6.1 Das Prinzip: Rational + Psychologisch + Sozial

Die zentrale Entwurfsentscheidung lautet: Die drei Ebenen sind *additiv* und *modular*.

> **Definition 6.1 (Drei-Ebenen-Architektur).** *Sei $x_i(t) \in \mathbb{R}$ eine Entscheidungsvariable von Agent $i$. Die allgemeine Entscheidungsdynamik lautet:*
>
> $$\dot{x}_i = \mathcal{R}_x(\mathbf{X}_i, \mathcal{I}_i) + \Psi_x(\mathbf{X}_i, \mathbf{X}_i^{\text{ref}}, \mathcal{I}_i) + \sum_{j=1}^N A_{ij}^{\text{eff}} \, \Phi_x(x_j - x_i, \mathcal{I}_j, \mathcal{I}_i)$$
>
> *wobei:*
> - *$\mathcal{R}_x$: rationale Komponente — abgeleitet aus Nutzenmaximierung (A5);*
> - *$\Psi_x$: psychologische Modifikation — verhaltensökonomische Verzerrung;*
> - *$\Phi_x$: soziale Kopplungsfunktion — Netzwerkdiffusion (A6).*

Die Additivität ist nicht willkürlich, sondern folgt einem klaren Design-Prinzip:

**Warum additiv?** (1) Im Grenzfall $\Psi = \Phi = 0$ reduziert sich das System exakt auf das neoklassische Modell — die rationale Ebene ist *eingebettet*, nicht ersetzt. (2) Jede Ebene kann unabhängig getestet, kalibriert und falsifiziert werden. (3) Die additive Struktur ermöglicht eine klare vergleichende Statik: Wie ändert sich die Dynamik, wenn man Ebene 2 oder 3 „abschaltet"?

**Warum modular?** Die funktionale Form jeder Komponente ($\mathcal{R}$, $\Psi$, $\Phi$) bleibt *unspezifiziert*. Das Hauptergebnis dieses Kapitels ist: Die axiomatischen Eigenschaften dieser Funktionen — Monotonien, Nullpunkte, Beschränktheiten — genügen vollständig, um die qualitative Dynamik (Bifurkationen, Regime, Kausalstruktur) abzuleiten. Spezifische Funktionalformen (CRRA, Kahneman-Tversky, Sigmoid) sind *Modellierungswahlen* für die numerische Implementierung (Anhang C), nicht Teil der Theorie.

---

## 6.2 Nutzenarchitektur (U.1, U.2, U.3)

Bevor wir die Entscheidungsdynamik ableiten, formulieren wir das Fundament: die erweiterte Nutzenfunktion, die den *statischen* Optimierungskern bildet.

### U.1 — Erweiterte Nutzenfunktion mit Informationsgewichten

Die neoklassische Nutzenfunktion $u(c)$ kennt ein Konsumgut. Unser System hat sechs Güterklassen (§3.1), fünf Agentenklassen (§3.2) und $|\mathcal{K}|$ heterogene Güter. Die Nutzenfunktion muss diese Struktur reflektieren.

> **Gleichung U.1 (Erweiterte Nutzenfunktion).**
>
> $$u_i\bigl(c_i, \theta_i, \ell_i, \mathcal{I}_i\bigr) = \sum_{\alpha=1}^{6} \sum_{k \in \mathcal{K}_\alpha} \omega_{k,i}(\mathcal{I}_i) \cdot v_\alpha(c_{ik}, n_{ik}) - V(\ell_i)$$

| Symbol | Bedeutung |
|---|---|
| $\omega_{k,i}(\mathcal{I}_i)$ | Informationsgewichtete Präferenz für Gut $k$ (→ U.2) |
| $v_\alpha(\cdot)$ | Klassenspezifischer Nutzenterm für Güterklasse $\alpha$ |
| $V(\ell_i)$ | Arbeitsleid (Disutility of Labor) |
| $\mathcal{I}_i$ | Informationszustand des Agenten (→ Kapitel 7) |

Die axiomatischen Eigenschaften der Komponenten sind:

> **Definition 6.2 (Axiomatische Nutzeneigenschaften).** *Die Funktionen $v_\alpha$ und $V$ erfüllen:*
>
> | Funktion | Eigenschaft | Formalisierung | Ökonomische Bedeutung |
> |---|---|---|---|
> | $v_\alpha$ | Monotonie | $v_\alpha' > 0$ | Mehr ist besser |
> | $v_\alpha$ | Konkavität | $v_\alpha'' < 0$ | Abnehmender Grenznutzen |
> | $v_1, v_3$ | Inada-Bedingungen | $v'(0) = \infty$, $v'(\infty) = 0$ | Erste Einheit unendlich wertvoll; Sättigung |
> | $v_2, v_4$ | Besitznutzen | $v(0) = 0$, $v' > 0$ beschränkt | Nicht-Verbrauchsgüter: Nutzen durch Halten |
> | $v_5$ | Liquiditätspräferenz | $v_5' > 0$, $v_5'' < 0$, $v_5(0) = 0$ | Geld hat Nutzen (Liquidität), aber abnehmend |
> | $v_6$ | Informationsnutzen | $v_6' > 0$, $v_6'' < 0$, $v_6(0) = 0$ | Information hat Wert, aber stark abnehmend |
> | $V$ | Konvexes Arbeitsleid | $V' > 0$, $V'' > 0$ | Jede Arbeitsstunde kostet mehr als die vorige |

Entscheidend ist, *was hier fehlt*: Es steht nirgends, dass $v_1$ die CRRA-Form $c^{1-\gamma}/(1-\gamma)$ hat, oder dass $v_5$ logarithmisch ist, oder dass $V$ potenzförmig ist. All das sind *zulässige Spezialisierungen* (Anhang C.1 listet sie), aber die allgemeine Theorie benötigt sie nicht. Die Monotonie- und Konkavitätseigenschaften allein genügen, um die qualitativen Ergebnisse abzuleiten.

**Axiomatische Herkunft.** U.1 folgt aus A5 (Nutzenmaximierung) erweitert um A9 (Güterheterogenität, sechs Klassen) und A10 (Informationskosten, $\omega$-Gewichte). Ohne A9 hätte $u$ nur einen Konsumterm; ohne A10 wären die Gewichte $\omega_{k,i} = \text{const}$ — und jeder Agent würde über alle Güter gleich informiert entscheiden.

### U.2 — Informationsgewichte

Die Gewichte $\omega_{k,i}(\mathcal{I}_i)$ in U.1 sind keine konstanten Präferenzparameter. Sie hängen von der Information ab, die der Agent über das jeweilige Gut besitzt.

> **Gleichung U.2 (Informationsabhängige Gewichte).**
>
> $$\omega_{k,i} = \omega_{k,i}(\mathcal{I}_i), \quad\text{wobei } \omega: \mathbb{R}_+^{|\mathcal{K}|} \to \Delta^{|\mathcal{K}|-1}$$

Die axiomatischen Eigenschaften sind:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Normierung** | $\sum_{k \in \mathcal{K}} \omega_{k,i} = 1$ | Budgetallokation ist vollständig |
| **Informationsmonotonie** | $\frac{\partial \omega_{k,i}}{\partial \mathcal{I}_{ik}} > 0$ | Mehr Information über $k$ → höheres Gewicht |
| **Informationsexklusion** | $\mathcal{I}_{ik} = 0 \Rightarrow \omega_{k,i} = 0$ | Unbekannte Güter haben keine Nachfrage |
| **Glattheit** | $\omega \in C^1$ | Keine Sprünge bei marginaler Informationsänderung |

Das Informationsexklusions-Axiom ist ökonomisch zentral: Ein Agent, der von einem Gut nichts weiß, fragt es nicht nach — egal wie nützlich es objektiv wäre. Dies ist der Mechanismus, durch den Werbung reale Nachfrage erzeugt (nicht nur Nachfrage umlenkt): Sie transformiert $\mathcal{I}_{ik} = 0$ in $\mathcal{I}_{ik} > 0$ und schaltet damit den Gewichtungsterm $\omega_{k,i}$ von Null auf einen positiven Wert.

**Kausalkette.** U.2 schließt den Informations-Nachfrage-Kanal:

$$\mathcal{I}_{ik} \xrightarrow{\text{U.2}} \omega_{k,i} \xrightarrow{\text{U.1}} u_i \xrightarrow{\text{A5}} c_{ik}^* \xrightarrow{\text{I.1}} D_k \xrightarrow{\text{II.2}} p_k \xrightarrow{\text{Profit}} E_{\text{adv},k} \xrightarrow{\text{I.1}} \mathcal{I}_{ik}$$

Dieser Kreislauf ist *selbstverstärkend*: Information erzeugt Nachfrage, Nachfrage erzeugt Profit, Profit finanziert Werbung, Werbung erzeugt Information.

### U.3 — Effektiver Preis

Die Budgetbeschränkung enthält nicht den Marktpreis $p_k$, sondern einen *effektiven* Preis, der Informationskosten internalisiert.

> **Gleichung U.3 (Effektiver Preis).**
>
> $$p_k^{\text{eff}} = p_k \cdot \left(1 + \frac{\psi_k}{\mathcal{I}_k + \epsilon}\right)$$

| Symbol | Bedeutung |
|---|---|
| $p_k$ | Marktpreis (aus II.2) |
| $\psi_k > 0$ | Suchkostenparameter (gut- und marktspezifisch) |
| $\epsilon > 0$ | Regularisierung (Restinformation) |

Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Aufschlag** | $p_k^{\text{eff}} \geq p_k$ für alle $\mathcal{I}_k \geq 0$ | Information senkt Kosten, erzeugt sie nie |
| **Vollständige Information** | $\mathcal{I}_k \to \infty \Rightarrow p_k^{\text{eff}} \to p_k$ | Bei perfekter Information: Arrow-Debreu |
| **Informationskollaps** | $\mathcal{I}_k \to 0 \Rightarrow p_k^{\text{eff}} \to \infty$ | Kein Wissen → prohibitive Transaktionskosten |
| **Monotonie** | $\frac{\partial p_k^{\text{eff}}}{\partial \mathcal{I}_k} < 0$ | Mehr Information senkt den effektiven Preis |

U.3 folgt aus A4 (Gradientenfluss): Agenten optimieren nicht gegen den Marktpreis, sondern gegen den wahrgenommenen Preis. Die Differenz $p_k^{\text{eff}} - p_k = p_k \psi_k / (\mathcal{I}_k + \epsilon)$ misst reale Transaktionskosten — Suchkosten, Verifikationskosten, Vertrauensaufbau.

**Zusammenspiel U.1 + U.2 + U.3.** Die drei Gleichungen bilden gemeinsam die *informationsverzerrte Entscheidungsgrundlage*:

- U.1 definiert den Nutzen (Zielfunktion);
- U.2 bestimmt, welche Güter überhaupt wahrgenommen werden (Aufmerksamkeitsfilter);
- U.3 bestimmt, was die Güter den Agenten subjektiv kosten (Budgetverzerrung).

Im Grenzfall $\mathcal{I}_{ik} = \infty$ für alle $k$: $\omega_{k,i} = 1/|\mathcal{K}|$ und $p_k^{\text{eff}} = p_k$ — das System reduziert sich auf das Arrow-Debreu-Modell mit homogenen, vollständig informierten Agenten.

---

## 6.3 Konsum: Die Drei Ebenen (V.1, V.1a, V.2, V.3)

Wir wenden die Drei-Ebenen-Architektur (Definition 6.1) auf die Konsumentscheidung an. Die vollständige Konsumdynamik des Agenten $i$ lautet:

$$\frac{dc_i}{dt} = \underbrace{\mathcal{R}\bigl(r_i^{\text{wahr}}, \beta_i, \gamma_i, c_i, w_i, p^{\text{eff}}\bigr)}_{\text{V.1: Rational}} + \underbrace{\Psi_c\bigl(c_i, c_i^*, \dot{c}_i^{\text{hist}}, \text{Gini}, \mathcal{I}_i\bigr)}_{\text{V.2: Psychologisch}} + \underbrace{\sum_{j=1}^N A_{ij}^{\text{eff}} \, \Phi\bigl(c_j - c_i, \mathcal{I}_j, \mathcal{I}_i\bigr)}_{\text{V.3: Sozial}}$$

Wir behandeln jede Ebene einzeln, dann ihre Komposition.

### Ebene 1: Rationale Konsumregel (V.1)

> **Gleichung V.1 (Rationale Konsumregel).**
>
> $$\frac{dc_i}{dt}\bigg|_{\text{rat}} = \mathcal{R}\bigl(r_i^{\text{wahr}}, \beta_i, \gamma_i, c_i, w_i, p^{\text{eff}}\bigr)$$
>
> *wobei $\mathcal{R}: \mathbb{R}^6 \to \mathbb{R}$ die allgemeine rationale Konsumregel mit folgenden axiomatischen Eigenschaften:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Intertemporale Substitution** | $\frac{\partial \mathcal{R}}{\partial r_i^{\text{wahr}}} > 0$ | Höherer wahrgenommener Zins → Konsum verschieben |
| **Zeitpräferenz** | $\frac{\partial \mathcal{R}}{\partial \beta_i} < 0$ | Höhere Ungeduld → mehr Gegenwartskonsum |
| **Risikoaversion** | $\frac{\partial |\mathcal{R}|}{\partial \gamma_i} < 0$ | Höhere Risikoaversion → glatterer Konsumpfad |
| **Budgetrespekt** | $c_i(t) \leq w_i(t) + y_i(t)$ für alle $t$ | Keine Ponzi-Schemata (Transversalität) |
| **Nullpunkt** | $\mathcal{R}(\beta, \beta, \gamma, c, w, p) = 0$ | Bei $r = \beta$: kein Konsumwachstum |

Die Funktion $\mathcal{R}$ löst im stationären Fall das intertemporale Optimierungsproblem $\max \int_0^\infty e^{-\beta t} u(c) dt$ unter der Vermögensbeschränkung $\dot{w} = r w + y - p^{\text{eff}} c$. Die Euler-Gleichung dieses Problems hat die generische Form $\dot{c}/c = (r - \beta)/\gamma$ — aber das ist nur *ein* Spezialfall (Ramsey-Euler). Die axiomatischen Eigenschaften oben sind allgemeiner: Sie erlauben Habit-Formation, rekursive Präferenzen (Epstein-Zin), myopische Agenten und vieles mehr (Anhang C.2 listet vier konkrete Spezialisierungen).

**Axiomatische Herkunft.** V.1 folgt aus A5 (Nutzenmaximierung): Der Agent maximiert U.1 unter seiner dynamischen Budgetbeschränkung. Das Ergebnis ist eine Regel $\mathcal{R}$, nicht eine Funktionalform.

### Wahrgenommener Zins (V.1a)

Die rationale Regel V.1 enthält den *wahrgenommenen* Zins $r_i^{\text{wahr}}$, nicht den wahren Marktzins $r$. Die Verbindung ist informationsgefiltert:

> **Gleichung V.1a (Wahrgenommener Zins).**
>
> $$r_i^{\text{wahr}} = r + \nu_r(\mathcal{I}_i)$$
>
> *wobei $\nu_r$ ein informationsabhängiges Rauschen mit:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Erwartungstreue** | $E[\nu_r] = 0$ | Kein systematischer Bias |
| **Varianzreduktion** | $\text{Var}(\nu_r) \sim 1/\mathcal{I}_i$ | Mehr Information → kleinerer Fehler |
| **Vollständige Information** | $\mathcal{I}_i \to \infty \Rightarrow \nu_r \xrightarrow{f.s.} 0$ | Perfekt informiert: kein Rauschen |
| **Keine Information** | $\mathcal{I}_i \to 0 \Rightarrow \text{Var} \to \infty$ | Erratische Konsumentscheidungen |

Der wahrgenommene Zins ist das *erste* von mehreren Beispielen eines Grundprinzips: In der Ökonoaxiomatik beobachten Agenten die Welt nicht direkt, sondern durch einen Informationsfilter. In entwickelten Volkswirtschaften mit hohem $\mathcal{I}^{\text{Geld}}$ ist die Korrektur klein — die Euler-Gleichung gilt approximativ. In Entwicklungsländern, in Pandemien, in Finanzkrisen ist $\mathcal{I}$ niedrig — und die Agenten treffen systematisch falsche Entscheidungen, weil sie den Zins falsch wahrnehmen.

> **Beobachtung 6.1 (Informationsverknüpfung).** *V.1a schließt einen kritischen Kreislauf: Information beeinflusst nun simultan die Aufmerksamkeitsgewichte (U.2), die effektiven Preise (U.3), den wahrgenommenen Zins (V.1a), die unternehmerische Risikowahrnehmung (L.5, §6.8) und das effektive Ökonomische Potential (F.2, §5.2). Es gibt keinen einzigen Entscheidungskanal, der informationsunabhängig ist.*

### Ebene 2: Psychologische Modifikation (V.2)

Die zweite Ebene korrigiert die rationale Regel durch verhaltensökonomische Verzerrungen.

> **Gleichung V.2 (Psychologische Konsumverzerrung).**
>
> $$\Psi_c\bigl(c_i, c_i^*, \dot{c}_i^{\text{hist}}, \text{Gini}, \mathcal{I}_i\bigr)$$
>
> *wobei $\Psi_c: \mathbb{R}^5 \to \mathbb{R}$ folgende axiomatische Eigenschaften erfüllt:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Referenzpunktanziehung** | $\frac{\partial \Psi_c}{\partial (c_i^* - c_i)} > 0$ | Konsum driftet zum Referenzpunkt |
| **Verlustaversion** | $|\Psi_c(c < c^*)| > |\Psi_c(c > c^*)|$ bei gleichem Abstand | Verluste wiegen schwerer als Gewinne |
| **Relative Deprivation** | $\frac{\partial \Psi_c}{\partial \text{Gini}} < 0$ wenn $c_i < \bar{c}$ | Ungleichheit drückt Konsum der Armen |
| **Nullpunkt** | $\Psi_c(c^*, c^*, 0, 0, \cdot) = 0$ | Am Referenzpunkt ohne Ungleichheit: keine Verzerrung |
| **Beschränktheit** | $|\Psi_c| \leq \Psi_{\max}$ | Psychologische Verzerrung übersteuert nicht beliebig |

Die Argumente von $\Psi_c$ verdienen eine Erklärung:

- **$c_i^*$ (Referenzpunkt):** Das Konsumniveau, das der Agent als „normal" empfindet. Er ist *endogen* — er evolviert mit der Erfahrung des Agenten (VI.1, §6.9). Wenn der Agent sich an eine Gehaltserhöhung gewöhnt, steigt $c_i^*$ — das ist *Lifestyle Creep*.

- **$\dot{c}_i^{\text{hist}}$ (Konsumgeschichte):** Die Änderungsrate des Konsums in der jüngsten Vergangenheit. Agenten, die gerade einen Konsumschock erlitten haben ($\dot{c}^{\text{hist}} < 0$), sind in einem anderen psychologischen Zustand als Agenten mit stabilem Konsum. Dies ist der Habit-Formation-Kanal.

- **Gini (Ungleichheitsmaß):** Der Gini-Koeffizient der Konsumverteilung innerhalb der sichtbaren Nachbarschaft des Agenten. Relative Deprivation — das subjektive Gefühl, im Vergleich zu anderen zurückzufallen — ist empirisch einer der stärksten Prädiktoren für psychologisches Wohlbefinden (Runciman 1966, Clark et al. 2008).

**Axiomatische Herkunft.** V.2 ist *kein* Axiom — es ist eine *Erweiterung* des Axioms A5. Die neoklassische Nutzenmaximierung bleibt als Ebene 1 erhalten; Ebene 2 addiert eine empirisch fundierte Verzerrung *auf* die rationale Lösung. Die spezifische Form von $\Psi_c$ — linear, Kahneman-Tversky, Habit-Gini-Mischform — ist eine Modellierungswahl (Anhang C.3).

### Ebene 3: Soziale Kopplung (V.3)

Die dritte Ebene koppelt den Agenten an sein Netzwerk.

> **Gleichung V.3 (Soziale Konsumkopplung).**
>
> $$\sum_{j=1}^N A_{ij}^{\text{eff}} \, \Phi\bigl(c_j - c_i, \mathcal{I}_j, \mathcal{I}_i\bigr)$$
>
> *wobei $\Phi: \mathbb{R} \times \mathbb{R}_+ \times \mathbb{R}_+ \to \mathbb{R}$ die verallgemeinerte Herding-Funktion mit folgenden axiomatischen Eigenschaften:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Monotonie** | $\frac{\partial \Phi}{\partial (c_j - c_i)} > 0$ | Nachbarn mit höherem Konsum üben Aufwärtsdruck aus |
| **Nullpunkt** | $\Phi(0, \cdot, \cdot) = 0$ | Identischer Konsum → kein Herding-Druck |
| **Informationsmodulation** | $\frac{\partial |\Phi|}{\partial \mathcal{I}_j} > 0$ | Besser informierte Nachbarn haben stärkeren Einfluss |
| **Asymmetrie möglich** | $\Phi(x) \neq -\Phi(-x)$ im Allgemeinen | Aufwärtsherding (Blasen) kann stärker sein als Abwärts |
| **Beschränktheit** | $|\Phi| \leq \Phi_{\max}$ | Keine unbeschränkte Imitation |

Die *effektive Adjazenzmatrix* $A_{ij}^{\text{eff}}$ stammt aus dem Multiplex-Netzwerk (§3.3): Sie aggregiert die Handels-, Informations- und Sozialschichten $V.6, V.7, V.8$ zu einer einzigen Einflussstärke. Der Term $\sum_j A_{ij}^{\text{eff}} \Phi(\cdot)$ ist mathematisch ein *nichtlinearer Diffusionsoperator auf dem Netzwerk* — er hat dieselbe Struktur wie der Laplacian $\Delta_G$ aus §3.3, ist aber durch die nichtlineare $\Phi$-Funktion verallgemeinert.

**Kausale Konsequenz.** V.3 erzeugt *endogenes Herding*:

1. Agent $j$ kauft mehr → $c_j$ steigt.
2. $\Phi(c_j - c_i, \cdot) > 0$ → Aufwärtsdruck auf $c_i$.
3. Agent $i$ kauft mehr → weitere Nachbarn folgen.
4. Kaskadeneffekt über das Netzwerk.
5. In Kombination mit der Preisdynamik II.2: Steigender Konsum → steigende Nachfrage → steigende Preise → steigende Inflationserwartung $\eta_k$ → weiter steigende Preise.

Dies ist der Mechanismus für Konsumblasen (Immobilien, Kryptowährungen) und für Panikrückzüge (Bank Runs, Finanzkrise 2008). Die *Asymmetrie* von $\Phi$ — Aufwärtsherding stärker als Abwärtsherding — erklärt, warum Blasen langsam aufgebaut und schnell zerstört werden.

### Kompositionsregel

Die vollständige Konsumdynamik ist die Summe der drei Ebenen:

$$\boxed{\frac{dc_i}{dt} = \mathcal{R}\bigl(r_i^{\text{wahr}}, \beta_i, \gamma_i, c_i, w_i, p^{\text{eff}}\bigr) + \Psi_c\bigl(c_i, c_i^*, \dot{c}_i^{\text{hist}}, \text{Gini}, \mathcal{I}_i\bigr) + \sum_{j=1}^N A_{ij}^{\text{eff}} \, \Phi\bigl(c_j - c_i, \mathcal{I}_j, \mathcal{I}_i\bigr)}$$

> **Proposition 6.1 (Neoklassischer Grenzfall des Konsums).** *Sei $\mathcal{I}_{ik} = \infty$ für alle $i, k$ (perfekte Information), $c_i^* = c_i$ für alle $i$ (kein psychologischer Bias) und $A_{ij}^{\text{eff}} = 0$ für alle $i \neq j$ (kein Netzwerk). Dann reduziert sich die Konsumdynamik auf:*
>
> $$\frac{dc_i}{dt} = \mathcal{R}(r, \beta_i, \gamma_i, c_i, w_i, p)$$
>
> *d.h., die intertemporale Euler-Gleichung des Ramsey-Modells. Die Ökonoaxiomatik enthält die neoklassische Gleichgewichtstheorie als exakten Spezialfall.*

---

## 6.4 Arbeitsangebot: Die Drei Ebenen (L.1, L.1a, L.2, L.3, L.4)

Die Drei-Ebenen-Architektur gilt nicht nur für den Konsum — sie gilt für *jede* Entscheidung. Der Arbeitsmarkt folgt derselben Struktur, mit parallelen, aber inhaltlich verschiedenen Mechanismen auf jeder Ebene.

### Ebene 1: Rationaler Arbeitskern (L.1)

> **Gleichung L.1 (Rationale Arbeitsangebotsentscheidung).**
>
> $$L_i^* = \arg\max_{L_i} \bigl[ u(c_i) - V(L_i) \bigr] \quad \text{u.d.N.} \quad c_i \leq w_L L_i + r_i^{\text{wahr}} K_i + \pi_i$$
>
> *wobei $u$ und $V$ die allgemeinen Nutzenfunktionen aus U.1 (Definition 6.2) sind.*

Die *Bedingung erster Ordnung* dieses Problems lautet:

$$w_L \cdot u'(c_i^*) = V'(L_i^*)$$

Sie besagt: Der Lohn mal dem Grenznutzen des Konsums gleicht dem Grenzleid der Arbeit. Die axiomatischen Eigenschaften sind:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Grenznutzen positiv, fallend** | $u' > 0, \; u'' < 0$ | Mehr Konsum ist besser, aber abnehmend |
| **Grenzleid positiv, steigend** | $V' > 0, \; V'' > 0$ | Arbeit kostet; jede Stunde mehr |
| **Innere Lösung** | $V'(0) < w_L \cdot u'(w_L \cdot 0 + rK)$ | Erste Arbeitsstunde lohnt sich |
| **Komparative Statik** | $\frac{\partial L^*}{\partial w_L} \gtrless 0$ | Substitutions- vs. Einkommenseffekt (vorzeichen\-uneindeutig) |

Das Vorzeichen von $\partial L^*/\partial w_L$ ist im Allgemeinen *uneindeutig* — es hängt von der relativen Stärke des Substitutionseffekts (höherer Lohn macht Arbeit attraktiver) und des Einkommenseffekts (höherer Lohn macht Freizeit leistbar) ab. Diese fundamentale Ambiguität ist kein Defekt, sondern ein *Ergebnis*: Die Theorie sagt voraus, dass die Arbeitsangebotselastizität ein empirisch zu bestimmender Parameter ist, nicht ein theoretisch fixierter Wert.

### Wahrgenommener Alternativlohn (L.1a)

Für die Entscheidung, *wo* man arbeitet (Jobwechsel, Migration), ist nicht der eigene Lohn relevant, sondern der *wahrgenommene Alternativlohn* anderswo.

> **Gleichung L.1a (Wahrgenommener Alternativlohn).**
>
> $$w_{L,i}^{(\text{alt})} = w_L^{(\text{Ziel})} + \nu_w(\mathcal{I}_i^{\text{Arbeitsmarkt}})$$
>
> *wobei $\nu_w$ denselben axiomatischen Eigenschaften genügt wie $\nu_r$ in V.1a:*

| Eigenschaft | Formalisierung |
|---|---|
| Erwartungstreue | $E[\nu_w] = 0$ |
| Varianzreduktion | $\text{Var}(\nu_w) \sim 1/\mathcal{I}_i^{\text{Arbeitsmarkt}}$ |
| Vollständige Information | $\mathcal{I} \to \infty \Rightarrow \nu_w \to 0$ |

Agenten mit schlechter Arbeitsmarktinformation über- oder unterschätzen den Lohn am Zielort systematisch. Dies betrifft direkt die Migrationsentscheidung: Das Schwellenwert-Formalismus (Kapitel 10, Schw.1) verwendet $w_{L,i}^{(\text{alt})}$, nicht den wahren Lohn. Fehlinformierte Agenten migrieren entweder zu früh (überschätzter Ziellohn) oder zu spät (unterschätzter Ziellohn) — beides ineffizient.

### Ebene 2: Psychologische Modifikation (L.2)

> **Gleichung L.2 (Psychologische Arbeitsverzerrung).**
>
> $$\Psi_L\bigl(L_i, L_i^*, \bar{L}, \mathcal{I}_i^{\text{job}}, H_i\bigr)$$
>
> *wobei $\Psi_L: \mathbb{R}^5 \to \mathbb{R}$ folgende axiomatische Eigenschaften erfüllt:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Rückkehr zum Optimum** | $\frac{\partial \Psi_L}{\partial (L_i^* - L_i)} > 0$ | Tendenz zur rationalen Lösung |
| **Überlastungsschaden** | $\Psi_L < 0$ für $L_i \gg \bar{L}$ | Chronische Überarbeit → Burnout → Arbeitsangebot sinkt |
| **Intrinsische Motivation** | $\frac{\partial \Psi_L}{\partial \mathcal{I}_i^{\text{job}}} > 0$ | Jobidentifikation erhöht Arbeit über das rationale Niveau |
| **Gesundheitskopplung** | $\frac{\partial \Psi_L}{\partial H_i} > 0$ | Bessere Gesundheit → höheres Arbeitsangebot |
| **Nullpunkt** | $\Psi_L(L^*, L^*, \bar{L}, 0, H_{\text{normal}}) = 0$ | Am Optimum ohne Identifikation: keine Verzerrung |

Die Parallele zu V.2 ist erkennbar — aber die Mechanismen sind verschieden:

| Konsum (V.2) | Arbeit (L.2) |
|---|---|
| Referenzpunktanziehung | Rückkehr zum Optimum |
| Verlustaversion | Burnout (Überlastungsschaden) |
| Relative Deprivation | Intrinsische Motivation |
| Lifestyle Creep ($c^*$ steigt) | Berufliche Identifikation ($\mathcal{I}^{\text{job}}$ steigt) |

### Ebene 3: Soziale Kopplung und Statusdruck (L.3)

> **Gleichung L.3 (Soziale Arbeitskopplung).**
>
> $$\sum_{j=1}^N A_{ij}^{\text{eff}} \, \Phi_L\bigl(L_j - L_i, \mathcal{I}_j, \mathcal{I}_i\bigr) + \mathcal{S}\bigl(\text{rank}_i, \text{Kultur}\bigr)$$
>
> *wobei $\Phi_L$ die axiomatischen Eigenschaften von $\Phi$ in V.3 teilt (Monotonie, Nullpunkt, Beschränktheit), und $\mathcal{S}$ der Statusdruck-Operator mit:*

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Normkonvergenz** | $\frac{\partial \Phi_L}{\partial (L_j - L_i)} > 0$ | Arbeitszeit konvergiert zur Peer-Norm |
| **Statusmonotonie** | $\frac{\partial \mathcal{S}}{\partial \text{rank}_i} > 0$ | Höherer Status → mehr Arbeitsdruck |
| **Kultursensitivität** | $\mathcal{S}$ variiert mit Kulturparameter | Japan ($\mathcal{S}$ groß) vs. Frankreich ($\mathcal{S}$ klein) |

L.3 enthält im Gegensatz zu V.3 einen *zusätzlichen* Term $\mathcal{S}$: den Statusdruck. Konsum kann man verbergen — Arbeitszeit nicht (in den meisten Kulturen). Der Status-Term erklärt: Warum arbeiten japanische Manager 2.400 Stunden/Jahr, obwohl der Grenzlohn ihrer letzten Stunden negativ ist? Der soziale Druck übersteigt den ökonomischen Anreiz.

### Integrierte Arbeitsdynamik (L.4)

> **Gleichung L.4 (Vollständige Arbeitsangebotsdynamik).**
>
> $$\boxed{\dot{L}_i = \underbrace{\alpha_L(L_i^* - L_i)}_{\text{L.1: Rational}} + \underbrace{\Psi_L(L_i, L_i^*, \bar{L}, \mathcal{I}_i^{\text{job}}, H_i)}_{\text{L.2: Psychologisch}} + \underbrace{\sum_j A_{ij}^{\text{eff}} \Phi_L(\cdot) + \mathcal{S}(\cdot)}_{\text{L.3: Sozial}}}$$

Der rationale Term hat die spezifische Form $\alpha_L(L_i^* - L_i)$ mit *Anpassungsgeschwindigkeit* $\alpha_L > 0$ — die Arbeit konvergiert zum First-Order-Optimum aus L.1, aber nicht instantan. Die Geschwindigkeit dieser Konvergenz ist selbst ein empirischer Parameter (Arbeitsmarktrigidität).

> **Proposition 6.2 (Strukturelle Symmetrie Konsum-Arbeit).** *Die Konsumdynamik (V.1 + V.2 + V.3) und die Arbeitsdynamik (L.1 + L.2 + L.3 = L.4) haben exakt dieselbe Drei-Ebenen-Struktur:*
>
> | Dimension | Konsum | Arbeit |
> |---|---|---|
> | **Ebene 1: Rational** | Euler-Gleichung mit $r_i^{\text{wahr}}$ | FOC: $w_L u'(c) = V'(L)$ |
> | **Informationsfilter** | Wahrgenommener Zins (V.1a) | Wahrgenommener Alternativlohn (L.1a) |
> | **Ebene 2: Psychologisch** | Referenzpunkt + Verlustaversion | Burnout + Intrinsische Motivation |
> | **Ebene 3: Sozial** | Herding im Konsum ($\Phi$) | Arbeitsnormen + Statusdruck ($\Phi_L + \mathcal{S}$) |
>
> *Diese Symmetrie ist nicht zufällig — sie reflektiert die Dualität zwischen Konsum/Freizeit und Produktion/Einkommen im Nutzenmaximierungsproblem (A5).*

---

## 6.5 Produktion (III.3)

Die Produktionsentscheidung folgt einem einfacheren Schema als Konsum und Arbeit, weil sie primär von der Gewinnmarge gesteuert wird.

> **Gleichung III.3 (Produktionsdynamik).**
>
> $$\frac{dq_k}{dt} = \lambda_q \frac{p_k - MC_k(q_k)}{p_k} q_k - \delta_q q_k$$

| Symbol | Bedeutung |
|---|---|
| $q_k$ | Produktionsmenge des Guts $k$ |
| $\lambda_q > 0$ | Produktionsanpassungsgeschwindigkeit |
| $p_k$ | Marktpreis (aus II.2) |
| $MC_k(q_k)$ | Grenzkosten (steigend: $MC_k' > 0$) |
| $\delta_q > 0$ | Abschreibungsrate |

Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Expansion bei positivem Gewinn** | $p_k > MC_k \Rightarrow \dot{q}_k > 0$ (netto) | Gewinn zieht Produktion an |
| **Kontraktion bei negativem Gewinn** | $p_k < MC_k \Rightarrow \dot{q}_k < 0$ | Verlust stößt ab |
| **Stationäres Gleichgewicht** | $\dot{q}_k = 0 \Leftrightarrow p_k - MC_k = \delta_q p_k / \lambda_q$ | Preis deckt Grenzkosten plus Abschreibung |
| **Abschreibung** | $\delta_q q_k$ gleichmäßig | Ohne Neuinvestition: Zerfall |

Der erste Term — $\lambda_q (p_k - MC_k)/p_k \cdot q_k$ — ist die *relative Gewinnmarge* mal Produktionsniveau mal Anpassungsgeschwindigkeit. Das ist eine *gradientengesteuerte Expansion*: Unternehmen expandieren proportional zu ihrem Gewinn. Der zweite Term — $\delta_q q_k$ — ist physische Abschreibung des Kapitalstocks.

**Kopplung.** III.3 koppelt an folgende Gleichungen:

- **II.2** liefert $p_k$ (Preisdynamik);
- **L.1** + **L.4** liefern das Arbeitsangebot, das in $MC_k$ eingeht;
- **P.3** (§4.3) verbucht die produzierte Menge in der Populationsbilanz der Güterklasse $\alpha = 1$ (Produktion als Quelle).

---

## 6.6 Portfolio (III.2)

Die Portfolioentscheidung — welchen Anteil seines Vermögens ein Agent in welches Asset investiert — kombiniert rationale Optimierung mit sozialer Imitation.

> **Gleichung III.2 (Portfoliodynamik).**
>
> $$\frac{d\theta_{ik}}{dt} = \underbrace{\lambda_\theta \frac{\partial u_i}{\partial \theta_{ik}}}_{\text{Rationale Optimierung}} + \underbrace{\alpha_H \sum_j A_{ij}^{\text{eff}} (\theta_{jk} - \theta_{ik})}_{\text{Herding}} + \underbrace{\sigma_\theta \xi_i}_{\text{Idiosynkratischer Schock}}$$

| Symbol | Bedeutung |
|---|---|
| $\theta_{ik}$ | Anteil von Agent $i$ in Asset $k$ |
| $\lambda_\theta > 0$ | Portfolioanpassungsgeschwindigkeit |
| $\partial u_i / \partial \theta_{ik}$ | Grenznutzen der Portfolioänderung (aus U.1) |
| $\alpha_H \geq 0$ | Herding-Stärke |
| $\sigma_\theta \xi_i$ | Idiosynkratisches Rauschen (private Information, Noise Trading) |

Die drei Terme haben eine klare Parallele zur Drei-Ebenen-Architektur:

| Term | Ebene | Mechanismus |
|---|---|---|
| $\lambda_\theta \partial u / \partial \theta$ | 1 (Rational) | Markowitz-artige Diversifikation |
| $\alpha_H \sum_j A_{ij}(\theta_j - \theta_i)$ | 3 (Sozial) | Portfolioimitation (Herding) |
| $\sigma_\theta \xi_i$ | Stochastisch | Private Signale, Noise |

Die psychologische Ebene 2 fehlt als *expliziter* Term — sie ist implizit in $\partial u_i / \partial \theta_{ik}$ enthalten, da die Nutzenfunktion U.1 bereits die psychologischen Verzerrungen über die endogene Risikoaversion $\gamma_i$ (VI.2, §6.9) und die Referenzpunkte (VI.1) aufnimmt.

**Finanzmarktdynamik.** III.2 erzeugt die typischen Phänomene von Finanzmärkten: (1) Diversifikation durch den rationalen Term; (2) Blasen durch Herding ($\alpha_H$ groß → alle kaufen dasselbe Asset); (3) Überraschungscrashs durch den Noise-Term ($\xi$ stark negativ → ein Agent verkauft → andere folgen durch Herding).

---

## 6.7 Erwartungen (III.4)

Die Erwartungsbildung ist selbst eine Entscheidung — Agenten wählen eine Erwartungsregel, und diese Wahl hat Rückwirkungen auf alle anderen Entscheidungen.

> **Gleichung III.4 (Hybride Erwartungsbildung).**
>
> $$\frac{d\hat{p}_{ik}}{dt} = \underbrace{\omega_a (p_k - \hat{p}_{ik})}_{\text{Adaptiv}} + \underbrace{\omega_f (p_k^* - \hat{p}_{ik})}_{\text{Fundamental}} + \underbrace{\alpha_t \dot{p}_k}_{\text{Extrapolativ}} + \underbrace{\sigma_{\hat{p}} \xi_i}_{\text{Nachrichtenschock}}$$

| Komponente | Parameter | Mechanismus |
|---|---|---|
| Adaptiv | $\omega_a > 0$ | Erwartung nähert sich dem beobachteten Preis |
| Fundamental | $\omega_f > 0$ | Erwartung nähert sich dem Modell-Gleichgewichtspreis $p_k^*$ |
| Extrapolativ | $\alpha_t \geq 0$ | Trendverfolgung: steigende Preise → Erwartung steigender Preise |
| Nachrichtenschock | $\sigma_{\hat{p}} > 0$ | Plötzliche Neubewertung durch private Information |

Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Langfristige Konsistenz** | $\hat{p} \to p^*$ wenn $\omega_f > 0$ und $p \to p^*$ | Fundamentalisten treiben zum Gleichgewicht |
| **Kurzfristige Instabilität** | $\alpha_t > \omega_a + \omega_f$ möglich | Trend dominiert → selbsterfüllende Prophezeiung |
| **Informationsabhängigkeit** | $\omega_a, \omega_f$ können von $\mathcal{I}_i$ abhängen | Besser informiert → stärkerer Fundamentalanteil |
| **Heterogenität** | $\omega_a^{(i)} \neq \omega_a^{(j)}$ | Verschiedene Agenten, verschiedene Regeln |

III.4 folgt aus A7 (Adaptive Erwartungen), verallgemeinert auf drei Kanäle. In der Sprache der Heterogeneous-Agent-Literatur (Brock & Hommes 1998) ist $\omega_a$ der *Chartist*-Anteil, $\omega_f$ der *Fundamentalist*-Anteil, und $\alpha_t$ die *Momentum*-Komponente.

Die zentrale Kopplung ist: III.4 liefert $\hat{p}_{ik}$, das über die Inflationserwartung $\eta_k$ in die Preisgleichung II.2 (§5.1) eingeht. Wenn die Extrapolation dominiert ($\alpha_t$ groß), erzeugt die Rückkopplung III.4 → II.2 → III.4 explosive Blasen. Wenn der Fundamentalanteil dominiert ($\omega_f$ groß), konvergiert das System zum Gleichgewicht.

---

## 6.8 Unternehmerisches Risiko (L.5)

Die Entscheidung, ein Unternehmen zu gründen (oder zu schließen), ist eine diskrete *Schwellenwertentscheidung* — nicht eine marginale Anpassung wie bei Konsum oder Arbeit.

> **Gleichung L.5 (Unternehmerische Risikoentscheidung).**
>
> $$\Pi_i^{\text{erw}} = \underbrace{\mathcal{I}_i^{\text{Markt}} \cdot E[R_i]}_{\text{Informierter Ertragswert}} - \underbrace{\frac{\gamma_i}{2}\, \sigma_i^2(\mathcal{I}_i)}_{\text{Risikokosten}} - \underbrace{c_{\text{entry}}}_{\text{Markteintrittskosten}}$$
>
> *Gründe, wenn $\Pi_i^{\text{erw}} > 0$.*

| Symbol | Bedeutung |
|---|---|
| $E[R_i]$ | Erwartete Rendite des Startups |
| $\mathcal{I}_i^{\text{Markt}}$ | Marktinformationsniveau des Agenten |
| $\gamma_i$ | Risikoaversion (aus VI.2, endogen) |
| $\sigma_i^2(\mathcal{I}_i)$ | Wahrgenommene Varianz (informationsabhängig) |
| $c_{\text{entry}}$ | Fixe Eintrittskosten |

Die zentrale axiomatische Eigenschaft ist die *Informationsmodulation der wahrgenommenen Varianz*:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Varianzreduktion** | $\frac{\partial \sigma_i^2}{\partial \mathcal{I}_i} < 0$ | Mehr Information → weniger wahrgenommenes Risiko |
| **Grenzfall: perfekte Information** | $\mathcal{I}_i \to \infty \Rightarrow \sigma_i^2 \to \sigma_{\text{obj}}^2$ | Nur objektives Risiko bleibt |
| **Grenzfall: keine Information** | $\mathcal{I}_i \to 0 \Rightarrow \sigma_i^2 \to \infty$ | Knightsche Unsicherheit: kein Gründer |
| **Risikoaversion endogen** | $\gamma_i = \gamma_i(t)$ via VI.2 | Kumulative Verluste erhöhen $\gamma_i$ |

Die Drei-Ebenen-Architektur gilt auch für L.5, allerdings implizit:

| Ebene | Effekt auf die Gründungsentscheidung |
|---|---|
| **1 (Rational)** | Gründe wenn $\Pi_i^{\text{erw}} > 0$ (positiver Kapitalwert) |
| **2 (Psychologisch)** | Überconfidence → überschätze $E[R]$; Verlustaversion → überschätze Verlustrisiko |
| **3 (Sozial)** | Gründerkultur (Silicon Valley: $c_{\text{eff}} < c_{\text{entry}}$) vs. Risikoscheu (bürokratische Kultur: $c_{\text{eff}} > c_{\text{entry}}$) |

**Kausalkette.** L.5 schließt einen Kreislauf mit der Informationsdynamik (Kapitel 7): Mehr Marktinformation → weniger wahrgenommenes Risiko → mehr Gründungen → mehr Gütervarietät → Wirtschaftswachstum → mehr Information. Gleichzeitig schafft die Rückkopplung über VI.2 (endogene Risikoaversion) einen *gegenläufigen* Mechanismus: Gescheiterte Gründungen → kumulative Verluste → höheres $\gamma_i$ → weniger Gründungen.

---

## 6.9 Endogene Verhaltensparameter (VI.1–VI.9)

Die Ebenen 1–3 verwenden Parameter — Referenzpunkte $c_i^*$, Risikoaversion $\gamma_i$, Zeitpräferenz $\beta_i$, Herding-Stärke $\alpha_H$, und andere. In der Standardtheorie sind diese Parameter *exogen* (Kalibrierungskonstanten). In der Ökonoaxiomatik sind sie *endogen*: Sie evolvieren als Funktionen des Systemzustands.

Dies ist die *Meta-Ebene* — die Parameter der Entscheidungsarchitektur driften selbst.

> **Definition 6.3 (Endogene Parameterdynamik).** *Die neun Gleichungen VI.1–VI.9 definieren die Evolution der Verhaltensparameter. Jede hat die generische Form:*
>
> $$\dot{\theta}_i = f_\theta(\text{Erfahrung}_i, \text{Zustand}_i) - \mu_\theta(\theta_i - \theta_i^{\text{base}})$$
>
> *bestehend aus einem erfahrungsgetriebenen Drift $f_\theta$ und einer Mean-Reversion zum Basiswert $\theta_i^{\text{base}}$ mit Rate $\mu_\theta > 0$.*

### VI.1 — Referenzpunktdynamik

> **Gleichung VI.1.**
>
> $$\dot{c}_i^* = \lambda_c\bigl(\mathcal{I}_i - \mathcal{I}_i^{\text{ref}}\bigr) + \epsilon_{c,i}$$

Der Referenzpunkt steigt, wenn der Agent mehr Information über höherwertige Güter erhält — „wer sieht, was andere haben, will mehr." Dies ist der endogene Mechanismus für Lifestyle Creep.

### VI.2 — Risikoaversion

> **Gleichung VI.2.**
>
> $$\dot{\gamma}_i = \alpha_\gamma \int_\mathcal{T} \bigl[\rho_i(t') - \bar{\rho}\bigr] dt' - \mu_\gamma(\gamma_i - \gamma_i^{\text{base}})$$

Kumulative Verluste ($\rho_i < \bar{\rho}$) erhöhen die Risikoaversion; Mean-Reversion zieht zum Basiswert zurück. Nach einer Finanzkrise ist die gesamte Population risikoscheuer — bis die Erinnerung verblasst.

### VI.3 — Zeitpräferenz

> **Gleichung VI.3.**
>
> $$\dot{\beta}_i = f_\beta(\tau_i^{\text{payoff}}, \mathcal{I}_i) - \mu_\beta(\beta_i - \beta_i^{\text{base}})$$

Schnelle Auszahlungen ($\tau^{\text{payoff}}$ klein) reduzieren die Zeitpräferenz — der Agent wird ungeduldiger. Soziale Medien mit instantaner Gratifikation treiben $\tau^{\text{payoff}}$ nach unten und $\beta_i$ nach oben (mehr Ungeduld).

### VI.4 — Herding-Stärke

> **Gleichung VI.4.**
>
> $$\dot{\alpha}_H = \phi_H(\pi_i^{\text{pol}}) + \sigma_H \xi_H$$

Die Herding-Stärke wird durch politische Polarisation $\pi^{\text{pol}}$ getrieben — in polarisierten Gesellschaften folgen Agenten stärker ihrer In-Group.

### VI.5 — Anti-Herding (Contrarianismus)

> **Gleichung VI.5.**
>
> $$\dot{\alpha}_{\text{anti}} = \phi_A(-\pi_i^{\text{pol}}) + \sigma_A \xi_A$$

Gespiegelt zu VI.4: Weniger Polarisation → mehr Raum für Contrarianismus. In offenen, pluralistischen Gesellschaften ist $\alpha_{\text{anti}}$ höher — Arbitrage funktioniert besser, weil Contrarians gegen den Herdenstrom handeln.

### VI.6 — Technologie und Wissenswachstum

> **Gleichung VI.6.**
>
> $$\dot{A} = \theta_A A - \delta_A A + s_A Y$$

Wissen wächst auf den Schultern von Riesen ($\theta_A A$), zerfällt ($\delta_A A$), und wird durch F\&E-Investitionen ($s_A Y$) akkumuliert. Die Struktur folgt der endogenen Wachstumstheorie (Romer 1990), eingebettet in unser Gleichungssystem.

### VI.7 — Knightsche Unsicherheit

> **Gleichung VI.7.**
>
> $$\dot{\zeta}_i^K = \phi_K(\text{Surprise}_i) - \mu_K \zeta_i^K$$

Die Knightsche Unsicherheit — Unsicherheit, die sich nicht als Wahrscheinlichkeit quantifizieren lässt — springt bei unerwarteten Ereignissen hoch und klingt exponentiell ab. Nach einem Schwarzen Schwan ($\text{Surprise}$ groß): kurzfristiger Spike in $\zeta^K$, der alle Entscheidungen verzerrt.

### VI.8 — Modellunsicherheit

> **Gleichung VI.8.**
>
> $$\dot{\sigma}_i^K = \beta_K \zeta_i^K + \nu_{\text{news},i}$$

Die Modellunsicherheit wird durch die Knightsche Unsicherheit (VI.7) getrieben — ein *Kaskadeneffekt*: Surprise → Knightsche Unsicherheit → Modellunsicherheit. Agenten, die ihr eigenes Modell der Welt anzweifeln, treffen qualitativ andere Entscheidungen als Agenten mit festem Weltbild.

### VI.9 — Non-Ergodicity Correction

> **Gleichung VI.9.**
>
> $$\alpha_{\text{erg}}(t) = \alpha_0 \bigl(1 - e^{-t/\tau_{\text{erg}}}\bigr)$$

Für kurze Zeiträume ($t \ll \tau_{\text{erg}}$) ist das System nicht-ergodisch — Ensemble-Mittelwerte weichen von Zeitmittelwerten ab. Für lange Zeiträume ($t \gg \tau_{\text{erg}}$) nähert sich $\alpha_{\text{erg}} \to \alpha_0$ und das System wird approximativ ergodisch. Diese Korrektur nach Peters (2019) ist besonders relevant für die Vermögensverteilung: In nicht-ergodischen Systemen kann das *mittlere* Vermögen wachsen, während das *typische* Vermögen fällt.

### Gesamtstruktur der endogenen Parameter

> **Beobachtung 6.2 (Quasistationäre Trennung).** *Die neun Gleichungen VI.1–VI.9 operieren auf einer langsameren Zeitskala als die Entscheidungsvariablen $c_i, L_i, \theta_{ik}$. Man kann daher approximativ trennen: Auf kurzen Zeitskalen (Tage bis Wochen) sind die VI-Parameter quasistationär — die Drei-Ebenen-Architektur operiert mit festen Parametern. Auf langen Zeitskalen (Monate bis Dekaden) driften die Parameter — und die qualitative Natur des Systems ändert sich.*

| Zeitskala | Was sich ändert | Beispiel |
|---|---|---|
| **Sekunden–Tage** | $c_i, L_i, \theta_{ik}, p_k$ | Tageshandel, Konsum |
| **Wochen–Monate** | $c_i^*, \gamma_i, \beta_i$ | Lifestyle-Anpassung nach Gehaltserhöhung |
| **Jahre–Dekaden** | $\alpha_H, A, \zeta^K$ | Kulturelle Verschiebung, Technologiewandel |
| **Generationen** | $\tau_{\text{erg}}, \alpha_0$ | Ergodizitätscharakter der Wirtschaft |

---

## 6.10 Dominanzanalyse: Wann regiert welche Ebene?

Das zentrale qualitative Ergebnis dieses Kapitels ist: Die Drei-Ebenen-Architektur ist nicht symmetrisch — verschiedene Situationen aktivieren verschiedene Ebenen.

> **Proposition 6.3 (Situationsabhängige Dominanz).** *Für die Entscheidungsdynamik $\dot{x}_i = \mathcal{R} + \Psi + \sum A_{ij}\Phi$ gelten folgende Dominanzmuster:*
>
> | Situation | Dominante Ebene | Mechanismus | Beispiel |
> |---|---|---|---|
> | **Langfristiges Sparen** | 1 (Rational) | $|\mathcal{R}| \gg |\Psi|, |\Phi|$ | Altersvorsorge |
> | **Nach Gehaltserhöhung** | 2 (Psychologisch) | $c_i^*$ verschiebt sich (VI.1) | Lifestyle Creep |
> | **Immobilienblase** | 3 (Sozial) | $\alpha_H$ groß, $\Phi > 0$ kaskadiert | „Alle kaufen → ich auch" |
> | **Finanzkrise** | 2 + 3 | $\Psi < 0$ (Verlustpanik) + $\Phi < 0$ (Herding-Crash) | Panikverstärkung |
> | **Normalzustand** | 1 (approximativ) | $\Psi \approx 0$, $\Phi \approx 0$ | DSGE-Bereich |
> | **Jobmarkt (Japan)** | 3 (Sozial) | $\mathcal{S}$ groß | Überstundenkultur |
> | **Start-up-Ökosystem** | 1 + 3 | $\Pi^{\text{erw}} > 0$ + Gründerkultur | Silicon Valley |
> | **Post-Pandemie** | 2 | $\gamma_i$ erhöht (VI.2), $\zeta^K$ erhöht (VI.7) | Vorsichtsmotiv |

Die letzte Zeile der Tabelle verdient Betonung: Die *Dominanz* entsteht nicht durch das Abschalten einer Ebene, sondern durch die *relative Größe* der Terme. In einer Panik sind $|\Psi|$ und $|\Phi|$ groß — nicht weil die rationale Ebene verschwindet, sondern weil die psychologischen und sozialen Kräfte sie überlagern.

> **Proposition 6.4 (Neoklassische Einbettung, allgemein).** *Seien $\Psi_x \equiv 0$ und $\Phi_x \equiv 0$ für alle Entscheidungsvariablen $x \in \{c, L, \theta, q, \hat{p}\}$. Dann reduziert sich das vollständige Entscheidungssystem auf:*
>
> | Gleichung | Reduzierte Form | Standardmodell |
> |---|---|---|
> | $\dot{c}_i$ | $\mathcal{R}(r, \beta, \gamma, c, w, p)$ | Ramsey-Euler |
> | $L_i^*$ | $w_L u'(c) = V'(L)$ | Neoklassisches Arbeitsangebot |
> | $\dot{\theta}_{ik}$ | $\lambda_\theta \partial u/\partial \theta_{ik} + \sigma_\theta \xi$ | Markowitz + Noise |
> | $\dot{q}_k$ | $\lambda_q(p - MC)/p \cdot q - \delta_q q$ | Competitive Output Adjustment |
> | $d\hat{p}_{ik}/dt$ | $\omega_a(p - \hat{p}) + \omega_f(p^* - \hat{p})$ | Adaptive-Fundamental (Brock-Hommes) |
>
> *Die Ökonoaxiomatik ist nicht eine Alternative zur neoklassischen Theorie. Sie ist deren minimale Erweiterung, die Verhaltenseffekte und Netzwerkkopplung als additive Terme einbettet.*

---

*Ende von Kapitel 6. Im folgenden Kapitel analysieren wir die Informationsdynamik — den fünften Zustandsblock, der alle Entscheidungen durchdringt und die Brücke zwischen Werbung, Aufmerksamkeit und Marktergebnis schlägt.*

---

# Kapitel 7 — Information

In Kapitel 6 haben wir gesehen, wie Information in *jede* Entscheidung eingreift: über die Nachfragegewichte (U.2), über den effektiven Preis (U.3), über den wahrgenommenen Zins (V.1a), über die unternehmerische Risikowahrnehmung (L.5), über das effektive Potential (F.2). Jedes Mal haben wir $\mathcal{I}_{ik}$ als gegebenes Feld behandelt und seine Wirkung auf die Entscheidung beschrieben. Dieses Kapitel beantwortet die komplementäre Frage: *Woher kommt Information? Wie wird sie produziert, wie breitet sie sich aus, wie vergeht sie?*

Die Antwort kommt aus den Axiomen A9 (Güterdiversität — Information als sechste Güterklasse $\mathcal{K}_6$), A10 (Informationskosten — konvex, strikt positiv) und A4 (Gradientenfluss — Information als räumliches Feld). Information ist in der Ökonoaxiomatik kein Parameter und kein exogenes Signal — sie ist ein *dynamisches Feld* mit eigener Produktions-, Diffusions- und Zerfallsdynamik, das rückgekoppelt an alle anderen Felder des Systems ist.

Das Kapitel enthält fünf Gleichungen:

| Gleichung | Gegenstand | Axiom |
|---|---|---|
| **I.1** | Informationsproduktion und -ausbreitung | A4 + A9 + A10 |
| **I.2** | Optimale Werbung (Dorfman-Steiner) | A5 |
| **I.3** | Aufmerksamkeitsbeschränkung | A5 (beschränkt) |
| **I.5** | Netto-Informationsnutzen | A5 + A10 |
| **Ent.2** | Gütervernichtung und Informationsentropie | A2 (Senken) |

---

## 7.1 Informationsproduktion und -ausbreitung (I.1)

Dies ist die zentrale Gleichung des Kapitels — sie beschreibt die vollständige Dynamik der Information $\mathcal{I}_k(\mathbf{x}, t)$ als Reaktions-Diffusions-Gleichung mit fünf Termen.

> **Gleichung I.1 (Informationsdynamik).**
>
> $$\dot{\mathcal{I}}_k = \underbrace{D_\mathcal{I}\,\nabla^2\mathcal{I}_k}_{\text{Räumliche Diffusion}} + \underbrace{\sigma_{\text{adv}} \cdot E_{\text{adv},k}}_{\text{Werbung}} + \underbrace{\mathcal{W}(\mathcal{I}_k)}_{\text{Word-of-Mouth}} + \underbrace{\sigma_{\text{use}} \cdot c_k / n_k}_{\text{Nutzungserfahrung}} - \underbrace{\omega\,\mathcal{I}_k}_{\text{Vergessen}}$$

Fünf Terme, fünf verschiedene Mechanismen, die zusammen die vollständige Informationsökologie beschreiben.

### Term 1: Räumliche Diffusion

$$D_\mathcal{I}\,\nabla^2\mathcal{I}_k$$

Information breitet sich räumlich aus — von Orten hoher Informationsdichte zu Orten niedriger Dichte. Der Laplace-Operator $\nabla^2$ ist derselbe wie in der Wärmeleitungsgleichung; die Diffusionskonstante $D_\mathcal{I}$ misst die Geschwindigkeit der Ausbreitung.

| Medium | Typisches $D_\mathcal{I}$ | Konsequenz |
|---|---|---|
| Mundpropaganda (vorindustriell) | Klein | Information bleibt lokal |
| Printmedien (19. Jh.) | Mittel | Nationale Ausbreitung in Wochen |
| Radio/TV (20. Jh.) | Groß | Nationale Ausbreitung in Stunden |
| Internet/Social Media (21. Jh.) | Sehr groß | Globale Ausbreitung in Minuten |

Die *historische Zunahme* von $D_\mathcal{I}$ ist einer der tiefgreifendsten Strukturwandel der Wirtschaftsgeschichte. In einer Welt mit $D_\mathcal{I} \approx 0$ (lokale Informationsblasen) können Preisdiskrepanzen über Jahrzehnte bestehen bleiben — Arbitrage scheitert an Unwissenheit, nicht an Kapitalknappheit. In einer Welt mit $D_\mathcal{I} \gg 1$ (globale Informationshomogenität) tendieren Preise zur Konvergenz — aber die *Volatilität* steigt, weil lokale Schocks instantan global propagiert werden.

Dieser Term folgt aus Axiom A4: Information als Feld der Güterklasse $\mathcal{K}_6$ fließt entlang ihres negativen Gradienten.

### Term 2: Werbung

$$\sigma_{\text{adv}} \cdot E_{\text{adv},k}$$

Die direkteste Quelle von Information: Unternehmen investieren $E_{\text{adv},k}$ Geldeinheiten in Werbung, die mit Effizienz $\sigma_{\text{adv}} > 0$ in Information konvertiert wird. Dieser Term ist die *kontrollierte Quelle* — im Gegensatz zu den anderen drei Quellen, die endogen aus dem Systemzustand entstehen, ist die Werbung eine Entscheidungsvariable des Unternehmens (→ I.2, §7.2).

Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Positivität** | $\sigma_{\text{adv}} > 0$ | Werbung erzeugt Information (per Definition) |
| **Linearität in $E_{\text{adv}}$** | Ist eine Modellierungswahl | Abnehmende Werbeeffizienz (Sättigung) möglich als $\sigma_{\text{adv}}(E) \downarrow$ |
| **Kopplung an Firmenentscheidung** | $E_{\text{adv},k}$ ist Lösung von I.2 | Endogene Werbung, nicht exogen |

### Term 3: Word-of-Mouth

$$\mathcal{W}(\mathcal{I}_k)$$

Die axiomatischen Eigenschaften der Word-of-Mouth-Funktion $\mathcal{W}$ sind:

> **Definition 7.1 (Axiomatische Eigenschaften der Mundpropaganda).** *Die Funktion $\mathcal{W}: [0, \mathcal{I}_{\max}] \to \mathbb{R}_+$ erfüllt:*
>
> | Eigenschaft | Formalisierung | Interpretation |
> |---|---|---|
> | **Nullpunkt unten** | $\mathcal{W}(0) = 0$ | Ohne jede Kenntnis: keine Mundpropaganda |
> | **Nullpunkt oben** | $\mathcal{W}(\mathcal{I}_{\max}) = 0$ | Bei Sättigung: niemand berichtet Bekanntes |
> | **Unimodales Maximum** | $\exists\, \mathcal{I}^* \in (0, \mathcal{I}_{\max})$: $\mathcal{W}'(\mathcal{I}^*) = 0$, $\mathcal{W}(\mathcal{I}^*) > 0$ | Maximale Mundpropaganda bei intermediärer Bekanntheit |
> | **S-Kurve** | $\mathcal{W}$ erzeugt sigmoide Adoptionskurve | Langsamer Start → Beschleunigung → Sättigung |

Diese Eigenschaften sind *allgemeiner* als die spezifische logistische Form $\mathcal{W} = \sigma_{\text{WoM}} \cdot \mathcal{I}(1 - \mathcal{I}/\mathcal{I}_{\max})$. Auch Gompertz-Formen ($\mathcal{W} = \sigma \mathcal{I}\ln(\mathcal{I}_{\max}/\mathcal{I})$), Bass-Modelle oder asymmetrische S-Kurven erfüllen die axiomatischen Eigenschaften — die Wahl ist eine Modellierungswahl (Anhang C.5), nicht Teil der Theorie.

Das unimodale Maximum hat eine klare ökonomische Interpretation: wenn *zu wenige* Menschen ein Gut kennen ($\mathcal{I} \approx 0$), gibt es fast niemanden, der darüber berichten kann; wenn *alle* es kennen ($\mathcal{I} \approx \mathcal{I}_{\max}$), gibt es niemanden, dem man etwas Neues erzählen könnte. Mundpropaganda ist maximal, wenn etwa die Hälfte der Population informiert ist — *der Moment, in dem das Produkt „viral geht"*.

### Term 4: Nutzungserfahrung

$$\sigma_{\text{use}} \cdot c_k / n_k$$

Wer ein Gut konsumiert, lernt darüber — proportional zur *Konsumintensität* $c_k/n_k$ (Konsum pro verfügbarem Bestand). Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Informationsproduktion durch Nutzung** | $\sigma_{\text{use}} > 0$ | Erfahrung ist nie informationslos |
| **Proportionalität zum Konsum** | $\propto c_k$ | Mehr Konsum → mehr Erfahrung |
| **Inverse Proportionalität zum Bestand** | $\propto 1/n_k$ | Bei seltenem Gut: jede Einheit lehrt mehr |

Dieser Term verbindet die Informationsdynamik direkt mit der Realsphäre: Er koppelt I.1 an die Konsumentscheidung (V.1–V.3, Kapitel 6). Ein Gut, das niemand konsumiert ($c_k = 0$), erzeugt keine Erfahrungsinformation — es bleibt auf Werbung und Mundpropaganda angewiesen.

### Term 5: Vergessen

$$-\omega\,\mathcal{I}_k$$

Information zerfällt mit Rate $\omega > 0$ — sie ist *vergänglich*. Dieses Axiom unterscheidet Information fundamental von physischem Kapital: Wissen veraltet, Aufmerksamkeit verblasst, Markenbekanntheit erodiert.

| $\omega$-Bereich | Interpretation | Beispiel |
|---|---|---|
| $\omega$ sehr klein | Langlebige Information | Grundlagenforschung, Alphabetisierung |
| $\omega$ mittel | Information mit Halbwertszeit | Markenbekanntheit ($\sim$ 1–5 Jahre) |
| $\omega$ groß | Kurzlebige Information | Nachrichten ($\sim$ Tage), Social-Media-Trends ($\sim$ Stunden) |

Im Steady State $\dot{\mathcal{I}}_k = 0$ muss die Summe aller Quellen den Zerfall exakt kompensieren:

$$\mathcal{I}_k^* = \frac{\sigma_{\text{adv}} E_{\text{adv},k} + \mathcal{W}(\mathcal{I}_k^*) + \sigma_{\text{use}} c_k/n_k}{\omega}$$

Dies ist eine *implizite* Gleichung (weil $\mathcal{W}$ von $\mathcal{I}_k^*$ abhängt), die im Allgemeinen *multiple Gleichgewichte* zulässt — ein niedriges (wenig bekannt, wenig Mundpropaganda) und ein hohes (allgemein bekannt, sich selbst tragend). Der Übergang zwischen beiden wird durch die Schwellenwertdynamik (Kapitel 10) bestimmt.

### Das Zusammenspiel: Informationsökologie

Die fünf Terme bilden ein komplettes ökologisches System:

| Phase | Dominante Terme | Dynamik |
|---|---|---|
| **Markteinführung** | Werbung | $\sigma_{\text{adv}} E_{\text{adv}} \gg$ Rest; ohne Werbung: $\mathcal{I} \to 0$ |
| **Wachstum** | WoM + Nutzung | $\mathcal{W}$ dominiert, S-Kurve, virales Wachstum |
| **Reife** | Zerfall $\approx$ Quellen | Steady State: $\mathcal{I}^* = \text{Quellen}/\omega$ |
| **Verfall** | Zerfall dominiert | Werbung stoppt, WoM erlischt, $\mathcal{I} \to 0$ |

Diese vier Phasen korrespondieren exakt zum *Produktlebenszyklus* — ein klassisches Konzept der Marketingliteratur (Vernon 1966), das hier erstmals als *emergentes Ergebnis* einer dynamischen Gleichung erscheint, statt als deskriptive Kategorie.

> **Proposition 7.1 (Informationslebenszyklus).** *Die Gleichung I.1 erzeugt unter den axiomatischen Eigenschaften von $\mathcal{W}$ (Definition 7.1) und bei endlicher Werbeperiode ($E_{\text{adv}} > 0$ für $t \in [0, T]$, dann $E_{\text{adv}} = 0$) automatisch den klassischen Produktlebenszyklus:*
>
> | Phase | Zeitraum | $\mathcal{I}_k(t)$ | Treiber |
> |---|---|---|---|
> | *Einführung* | $t \in [0, t_1]$ | $\mathcal{I} \ll 1$, wachsend | Werbung |
> | *Wachstum* | $t \in [t_1, t_2]$ | $\mathcal{I}$ wächst schnell | Word-of-Mouth (virales Maximum) |
> | *Reife* | $t \in [t_2, T]$ | $\mathcal{I} \approx \mathcal{I}^*$ (Steady State) | Quellen $\approx$ Zerfall |
> | *Rückgang* | $t > T$ | $\mathcal{I} \to 0$ exponentiell | Zerfall dominiert |

### Kopplung an die Preisgleichung: Die zwei Informations-Spiralen

Die Gleichung II.3 (§5.6) enthielt bereits die Kopplung zum Preis: Der Term $\beta|\dot{p}_k|$ in der aggregierten Informationsdynamik besagt, dass starke Preisbewegungen Information erzeugen (der „Events create news"-Mechanismus). In Kombination mit dem Illiquiditätsterm $-\phi/(\mathcal{I} + \epsilon)$ in II.2 (§5.1) entstehen zwei Spiralen:

**Stabilisierende Spirale.** Preis fällt → Nachrichtenwert ($\beta|\dot{p}|$) erzeugt Information → $\mathcal{I}$ steigt → Illiquiditätsprämie sinkt → Preisverfall bremst sich → Selbstkorrektur.

**Destabilisierende Spirale.** Preis fällt → Analysten verlassen den Markt → Informationsproduktion bricht ein → $\mathcal{I}$ sinkt *trotz* Preisfall → Illiquiditätsprämie steigt → Preisverfall beschleunigt → Illiquiditätsspirale.

Welche Spirale dominiert, hängt von einem einzigen Verhältnis ab:

$$\frac{\beta|\dot{p}_k|}{\omega\,\mathcal{I}_k} \gtrless 1$$

Wenn der Nachrichteneffekt den Zerfall überwiegt ($> 1$): Stabilisierung. Wenn der Zerfall überwiegt ($< 1$): Destabilisierung. Der Kipppunkt ist endogen — er verschiebt sich mit der Markttiefe $\lambda_k$ (§5.1), dem Herding $\alpha_H$ (V.3, §6.3) und der Regime-Dynamik (RS.1, Kapitel 10).

---

## 7.2 Optimale Werbung (I.2)

Der Werbungsterm in I.1 enthält $E_{\text{adv},k}$ — die Werbeausgaben des Unternehmens, das Gut $k$ produziert. Wie bestimmt ein Unternehmen $E_{\text{adv},k}$ optimal?

### Das Firmenproblem

Das Unternehmen $j \in \mathcal{U}$ (Unternehmer-Klasse, §3.3) maximiert seinen Gewinn:

$$\max_{E_{\text{adv},k}} \left[ p_k \cdot q_k(\mathcal{I}_k) - c(q_k) - E_{\text{adv},k} \right]$$

Hierbei ist $q_k(\mathcal{I}_k)$ die Nachfragemenge, die über die Kette I.1 → U.2 → V.1 von der Information abhängt: Mehr Werbung → mehr Information → höhere Nachfragegewichte → höhere Nachfrage → höherer Umsatz. Die Kosten bestehen aus Produktionskosten $c(q_k)$ und Werbeausgaben $E_{\text{adv},k}$.

### Die Dorfman-Steiner-Bedingung

Die Bedingung erster Ordnung dieses Problems liefert:

> **Gleichung I.2 (Optimale Werberegel — erweiterte Dorfman-Steiner-Bedingung).**
>
> $$\frac{E_{\text{adv},k}}{p_k\, q_k} = \frac{\epsilon_{\mathcal{I},q}}{\epsilon_{p,q}}$$

| Symbol | Bedeutung |
|---|---|
| $E_{\text{adv},k} / (p_k q_k)$ | Werbeintensität (Werbeausgaben als Anteil am Umsatz) |
| $\epsilon_{\mathcal{I},q} = \frac{\partial q}{\partial \mathcal{I}} \cdot \frac{\mathcal{I}}{q}$ | Informationselastizität der Nachfrage |
| $\epsilon_{p,q} = -\frac{\partial q}{\partial p} \cdot \frac{p}{q}$ | Preiselastizität der Nachfrage |

Die Interpretation ist elegant: Ein Unternehmen soll genau dann mehr in Werbung investieren (statt den Preis zu senken), wenn die Nachfrage stärker auf Information als auf Preissenkungen reagiert. Das Verhältnis $\epsilon_{\mathcal{I},q}/\epsilon_{p,q}$ ist die *relative Effektivität* von Werbung gegenüber Preispolitik.

Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Positivität** | $E_{\text{adv}}/pq \geq 0$ | Werbung nie negativ |
| **Werbung lohnt ↔ Info wirkt** | $\epsilon_{\mathcal{I},q} > 0 \Leftrightarrow E_{\text{adv}} > 0$ | Werbung nur wenn Info die Nachfrage steigert |
| **Keine Werbung bei perfekter Info** | $\mathcal{I} \to \infty \Rightarrow \epsilon_{\mathcal{I},q} \to 0$ | Wenn alle alles wissen: Werbung wirkungslos |
| **Keine Werbung bei preisunelastischer Nachfrage** | $\epsilon_{p,q} \to \infty$ | Preispolitik dominiert |

Die Dorfman-Steiner-Bedingung (1954) ist ein klassisches Ergebnis der Industrieökonomik. In der Ökonoaxiomatik erhält sie eine neue Dimension: Die Informationselastizität $\epsilon_{\mathcal{I},q}$ hängt über U.2 von der *bestehenden* Informationsstruktur ab. In Märkten, in denen Konsumenten schlecht informiert sind ($\mathcal{I}_k$ niedrig), ist $\epsilon_{\mathcal{I},q}$ *hoch* — Werbung wirkt stark. In gesättigten Informationsmärkten ($\mathcal{I}_k$ hoch) ist $\epsilon_{\mathcal{I},q}$ niedrig — Werbung hat abnehmende Grenzerträge.

### Werbung nach Güterklasse

Die sechs Güterklassen (§3.1) unterscheiden sich fundamental in ihrer Informationselastizität:

| Güterklasse | $\epsilon_{\mathcal{I},q}$ typisch | Werbeintensität | Beispiel |
|---|---|---|---|
| $\mathcal{K}_1$ (depreciating, rivalrous) | Mittel | Mittel | Lebensmittel: Markenwerbung |
| $\mathcal{K}_2$ (appreciating, rivalrous) | Hoch | Hoch | Immobilien: „Hot market"-Kampagnen |
| $\mathcal{K}_3$ (nicht-depreciating, rivalrous) | Mittel | Mittel | Möbel, Autos |
| $\mathcal{K}_4$ (IP: nicht-rivalrous) | Sehr hoch | Sehr hoch | Software, Medien: Netzwerkeffekte |
| $\mathcal{K}_5$ (Geld) | Niedrig | Niedrig | Bankprodukte: reguliert |
| $\mathcal{K}_6$ (Information) | Sehr hoch | Ambivalent | Nachrichten, Bildung |

Besonders bemerkenswert ist $\mathcal{K}_4$ (Intellectual Property): Da IP nicht-rivalrös ist ($r = 0$), kostet zusätzliche Produktion *fast nichts* — der gesamte Wettbewerb findet über Information statt. Die Werbe-zu-Umsatz-Ratio ist hier am höchsten: Tech-Unternehmen geben typisch 20–40% ihres Umsatzes für Marketing aus, verglichen mit 2–5% bei physischen Gütern. I.2 erklärt dies endogen.

---

## 7.3 Aufmerksamkeitsbeschränkung (I.3)

Die Gleichungen I.1 und I.2 behandeln die *angebotsseitige* Informationsdynamik — wieviel Information produziert, verbreitet und vergessen wird. Die *nachfrageseitige* Begrenzung ist die Aufmerksamkeit: Agenten können nicht unbegrenzt Information verarbeiten.

> **Gleichung I.3 (Aufmerksamkeitsbeschränkung).**
>
> $$\sum_{k \in \mathcal{K}} a_{ik} \leq A_{\max}$$

| Symbol | Bedeutung |
|---|---|
| $a_{ik} \geq 0$ | Aufmerksamkeit, die Agent $i$ dem Gut $k$ widmet |
| $A_{\max}$ | Kognitive Aufmerksamkeitskapazität (biologisch begrenzt) |

### Bedeutung der Beschränkung

I.3 ist keine Gleichung im üblichen Sinn — es ist eine *Ungleichungsbeschränkung*. Ihre Konsequenzen sind tiefgreifend:

> **Proposition 7.2 (Aufmerksamkeitsverdünnung).** *Bei $|\mathcal{K}|$ heterogenen Gütern und gleichverteilter Aufmerksamkeit gilt:*
>
> $$a_{ik} = \frac{A_{\max}}{|\mathcal{K}|} \xrightarrow{|\mathcal{K}| \to \infty} 0$$
>
> *Je mehr Güter existieren, desto weniger Aufmerksamkeit erhält jedes einzelne. Die pro-Gut-Informationsaufnahme $\dot{\mathcal{I}}_{ik}^{\text{wahrgen.}} = a_{ik} \cdot \mathcal{I}_k$ sinkt mit der Güterzahl — obwohl die Gesamtinformation $\mathcal{I}_k$ steigt.*

Dies ist der Mechanismus der *Informationsüberflutung*: In einer Wirtschaft mit tausenden Gütern kann ein Agent nur den Bruchteil $A_{\max}/|\mathcal{K}|$ seiner Aufmerksamkeit jedem Gut widmen. Die Konsequenz: selbst bei hoher Informationsdichte $\mathcal{I}_k$ ist die *wahrgenommene* Information $a_{ik} \cdot \mathcal{I}_k$ für die meisten Güter nahe Null — und über U.2 (Informationsexklusion: $\mathcal{I}_{ik} = 0 \Rightarrow \omega_{k,i} = 0$) werden diese Güter *nicht nachgefragt*.

### Die Aufmerksamkeitsallokation als Optimierungsproblem

Die Aufmerksamkeitsallokation $a_{ik}^*$ ist selbst eine Entscheidung: Der Agent wählt, worüber er sich informiert. Das Optimierungsproblem lautet:

$$\max_{\{a_{ik}\}} \sum_k \omega_{k,i}(\mathcal{I}_{ik}^{\text{wahrgen.}}) \cdot v_\alpha(c_{ik}) \quad \text{u.d.N.} \quad \sum_k a_{ik} \leq A_{\max}, \quad a_{ik} \geq 0$$

Die Kuhn-Tucker-Bedingungen dieses Problems erzeugen eine *sparsame* Allokation: Die meisten $a_{ik} = 0$ (der Agent ignoriert das Gut), und nur wenige Güter erhalten positive Aufmerksamkeit. Dies ist der *formale Mechanismus* dafür, dass Konsumenten in einer Volkswirtschaft mit $|\mathcal{K}| = 10.000$ Gütern von den meisten nichts wissen und sie nicht nachfragen — nicht weil die Güter nicht existieren, sondern weil kognitive Aufmerksamkeit eine *knappe Ressource* ist.

### Aufmerksamkeit als Engpass der digitalen Ökonomie

In der digitalen Ökonomie ($\mathcal{K}_4, \mathcal{K}_6$) wird I.3 zum bestimmenden Engpass. Die Kosten der Informationsproduktion ($E_{\text{adv}}$ in I.1) sind nahe Null (Social Media, Blogs, Videos kosten fast nichts). Aber die *Verarbeitung* ist konstant beschränkt durch $A_{\max}$. Das Ergebnis:

| Epoche | Engpass | Konsequenz |
|---|---|---|
| **Vorindustriell** | Informationsproduktion ($E_{\text{adv}} \approx 0$) | Lokale Märkte, wenig Wettbewerb |
| **Industriell** | Distribution ($D_\mathcal{I}$ begrenzt) | Nationale Märkte, Massenmedien |
| **Digital** | Aufmerksamkeit ($A_{\max}$ konstant!) | Winner-takes-all, Plattformen |

Die digitale Ökonomie ist aus der Perspektive von I.3 eine Welt, in der $D_\mathcal{I} \to \infty$ und $\sigma_{\text{adv}} \to \infty$, aber $A_{\max}$ *unverändert*. Die Konsequenz ist eine extreme Konzentration: Wenige Güter/Plattformen absorbieren den Großteil der Aufmerksamkeit, und die Informationsgewichte $\omega_{k,i}$ (U.2) werden extrem ungleich verteilt — exakt das, was wir empirisch als „Winner-takes-all"-Ökonomie beobachten (Kapitel 27).

> **Beobachtung 7.1 (Informations-Unschärfe).** *Aus I.3 folgt ein Analogon der Heisenbergschen Unschärferelation: Ein Agent kann nicht gleichzeitig über alle Güter vollständig informiert sein. Die Produkt-Information-Unschärfe*
>
> $$\Delta\mathcal{I}_k \cdot \Delta\theta_k \gtrsim \hbar_{\text{ök}} = \frac{A_{\max}}{|\mathcal{K}|}$$
>
> *besagt: Je genauer der Agent über ein Gut informiert ist ($\Delta\mathcal{I}_k$ klein), desto weniger Aufmerksamkeit bleibt für die Allokationsentscheidung über andere Güter ($\Delta\theta_k$ groß). Vollständige Information über alle Güter ist physisch unmöglich, wenn $|\mathcal{K}| > A_{\max}/\epsilon$ für jedes $\epsilon > 0$.*

---

## 7.4 Netto-Informationsnutzen (I.5)

Warum sucht ein Agent überhaupt nach Information? Die Antwort folgt aus A5 (Nutzenmaximierung) und A10 (Informationskosten): Information hat Nutzen (U.1, Klasse $v_6$), aber kostet etwas. Der Agent sucht, solange der Grenznutzen die Grenzkosten übersteigt.

> **Gleichung I.5 (Netto-Informationsnutzen).**
>
> $$\Pi_{ik}^{\text{info}} = \underbrace{v_6(\mathcal{I}_{ik}^{\text{neu}}) - v_6(\mathcal{I}_{ik}^{\text{alt}})}_{\text{Nutzengewinn durch Information}} - \underbrace{\mathcal{C}(\mathcal{I}_{ik})}_{\text{Suchkosten (A10)}}$$
>
> *Agent $i$ sucht Information über Gut $k$, solange $\Pi_{ik}^{\text{info}} > 0$.*

### Axiomatische Eigenschaften der Komponenten

Das Informationsnutzen-Kosten-Kalkül hängt von zwei Funktionen ab, deren axiomatische Eigenschaften aus den Axiomen folgen:

**Informationsnutzen $v_6$ (aus U.1, Klasse 6):**

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Monotonie** | $v_6' > 0$ | Mehr Information ist immer besser |
| **Konkavität** | $v_6'' < 0$ | Abnehmender Grenznutzen der Information |
| **Nullpunkt** | $v_6(0) = 0$ | Keine Information → kein Informationsnutzen |

**Suchkosten $\mathcal{C}(\mathcal{I})$ (aus A10):**

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Positivität** | $\mathcal{C}(\mathcal{I}) > 0$ für $\mathcal{I} > 0$ | Informationssuche kostet immer etwas |
| **Monotonie** | $\mathcal{C}' > 0$ | Mehr Information → höhere Kosten |
| **Konvexität** | $\mathcal{C}'' > 0$ | Steigende Grenzkosten: letzte Information am teuersten |

### Optimale Informationssuche

Die Bedingung erster Ordnung $\partial\Pi_{ik}^{\text{info}}/\partial\mathcal{I}_{ik} = 0$ liefert:

$$v_6'(\mathcal{I}_{ik}^*) = \mathcal{C}'(\mathcal{I}_{ik}^*)$$

Der Agent sucht bis der *Grenznutzen* der Information gleich den *Grenzkosten* der Suche ist. Da $v_6$ konkav ($v_6'' < 0$) und $\mathcal{C}$ konvex ($\mathcal{C}'' > 0$) ist, existiert genau ein Schnittpunkt — der optimale Informationsstand $\mathcal{I}_{ik}^*$ ist *eindeutig bestimmt*.

> **Proposition 7.3 (Informationsdefizit und Marktversagen).** *Der optimale individuelle Informationsstand $\mathcal{I}_{ik}^*$ ist im Allgemeinen **suboptimal** im Sinne der gesamtwirtschaftlichen Wohlfahrt:*
>
> $$\mathcal{I}_{ik}^* < \mathcal{I}_{ik}^{\text{sozial optimal}}$$
>
> *Grund: Information hat positive Externalitäten — wenn Agent $i$ über Gut $k$ informiert ist, steigt die Marktliquidität für alle Handelspartner (über den Illiquiditätsterm in II.2). Diese Externalität wird im privaten Kalkül I.5 nicht internalisiert. Das Ergebnis ist systematische Unterinvestition in Information — ein Marktversagen, das durch den Vergleich $\mathcal{I}^* < \mathcal{I}^{\text{soz.opt.}}$ messbar wird.*

### Grenzfälle

| Grenzfall | Bedingung | Ergebnis |
|---|---|---|
| **Kostenlose Information** | $\mathcal{C} \equiv 0$ | $\mathcal{I}_{ik}^* \to \infty$: Agent wird perfekt informiert (Arrow-Debreu) |
| **Prohibitiv teure Information** | $\mathcal{C}'(0) > v_6'(0)$ | $\mathcal{I}_{ik}^* = 0$: Agent bleibt uninformiert (Marktversagen) |
| **Internet-Zeitalter** | $\mathcal{C}$ sinkt global | $\mathcal{I}^*$ steigt, aber Aufmerksamkeit (I.3) bleibt Engpass |

---

## 7.5 Gütervernichtung und Informationsentropie (Ent.2)

Die Informationsdynamik hat eine thermodynamische Seite: Information wird nicht nur produziert und vergessen — sie *vernichtet* auch Güter. Genauer: Information über neue Produkte macht alte Produkte obsolet.

> **Gleichung Ent.2 (Totale Gütervernichtungsrate).**
>
> $$d_k^{\text{total}} = \underbrace{c_k}_{\text{Konsum}} + \underbrace{\delta_k\, n_k}_{\text{Physische Abschreibung}} + \underbrace{\lambda_{\text{obs},k}\, n_k}_{\text{Obsoleszenz}} + \underbrace{J_{\text{Kat},k}}_{\text{Katastrophenschock}}$$

| Term | Mechanismus | Güterklasse |
|---|---|---|
| $c_k$ | Konsumgüter werden durch Konsum vernichtet | $\mathcal{K}_1, \mathcal{K}_3$ (depreciating/consumable) |
| $\delta_k n_k$ | Physischer Zerfall, proportional zum Bestand | Alle physischen Klassen |
| $\lambda_{\text{obs},k} n_k$ | Informationsgetriebene Obsoleszenz | Vor allem $\mathcal{K}_4$ (IP), teilweise $\mathcal{K}_3$ |
| $J_{\text{Kat},k}$ | Diskrete Vernichtung (Krieg, Naturkatastrophe) | Alle Klassen (→ VIII.7, Kapitel 10) |

### Informationsgetriebene Obsoleszenz

Der für dieses Kapitel zentrale Term ist $\lambda_{\text{obs},k} n_k$. Die Obsoleszenzrate $\lambda_{\text{obs},k}$ hängt von der Informationsdynamik ab:

$$\lambda_{\text{obs},k} = \lambda_{\text{obs},k}(\dot{\mathcal{I}}_k, \mathcal{I}_k^{\text{neu}} - \mathcal{I}_k^{\text{alt}})$$

Axiomatische Eigenschaften:

| Eigenschaft | Formalisierung | Interpretation |
|---|---|---|
| **Informationsmonotonie** | $\frac{\partial \lambda_{\text{obs}}}{\partial \dot{\mathcal{I}}} > 0$ | Schnellere Informationsdynamik → schnellere Obsoleszenz |
| **Nullpunkt** | $\dot{\mathcal{I}} = 0 \Rightarrow \lambda_{\text{obs}} = \lambda_{\text{obs}}^{\text{phys}}$ | Ohne neue Information: nur physische Abschreibung |
| **Klassenabhängigkeit** | $\lambda_{\text{obs}}^{(\mathcal{K}_4)} \gg \lambda_{\text{obs}}^{(\mathcal{K}_1)}$ | IP veraltet schneller als physische Güter |

Die ökonomische Bedeutung: In der digitalen Ökonomie ($\mathcal{K}_4, \mathcal{K}_6$) ist die Obsoleszenzrate hoch — Software wird in 2–5 Jahren wertlos, Patente in 10–15 Jahren. Die Informationsdynamik I.1 treibt $\dot{\mathcal{I}}$ nach oben (mehr Werbung, schnellere Diffusion), was $\lambda_{\text{obs}}$ erhöht und den *effektiven Bestand* $n_k$ senkt. Dies erzeugt eine permanente Nachfrage nach Innovation — der endogene Mechanismus der „kreativen Zerstörung" (Schumpeter 1942), hier als Konsequenz der Informationsgleichung.

### Ent.2 in der Güterbestandsgleichung

Ent.2 spezialisiert die Senke in der Güterbestandsgleichung P.3 (§4.3): Dort steht $d_k$ als allgemeiner Vernichtungsterm — hier zerlegen wir ihn in seine vier Komponenten. Die vollständige Güterbilanz lautet damit:

$$\dot{n}_k + \nabla \cdot \vec{j}_{n_k} = q_k - d_k^{\text{total}} + \nu_{k \leftarrow j} - \nu_{j \leftarrow k}$$

wobei $q_k$ die Produktion (III.3, §6.5), $\nabla \cdot \vec{j}_{n_k}$ die Flussdivergenz (F.1, §5.3), und $\nu$ die Konversion (K.1, §3.2) ist.

### Entropie und Irreversibilität

> **Beobachtung 7.2 (Ökonomischer Entropiesatz).** *Die totale Gütervernichtungsrate $d_k^{\text{total}} \geq 0$ impliziert eine Richtung der ökonomischen Zeit: Ohne Produktion ($q_k = 0$) sinkt der Güterbestand $n_k$ monoton — Güter werden verbraucht, abgeschrieben, obsolet. Die „ökonomische Entropie"*
>
> $$\dot{S}_{\text{ök}} \geq 0$$
>
> *steigt global. Lokale Entropie kann sinken (ein Agent wird reicher, ein Gut wird bekannter), aber nur auf Kosten globaler Entropieproduktion — analogon zum zweiten Hauptsatz der Thermodynamik. In der Ökonomik ist die „Entropiequelle" der Verbrauch knapper Ressourcen (V.4, §9.3) und der Informationszerfall ($-\omega\mathcal{I}$ in I.1).*

---

## 7.6 Die Kausalkette: Information → Gewichte → Nachfrage → Preis → Werbung → Information

Die fünf Gleichungen dieses Kapitels bilden gemeinsam mit den Entscheidungsgleichungen aus Kapitel 6 und den Preisgleichungen aus Kapitel 5 einen geschlossenen Kreislauf — den *Informations-Werbung-Kreislauf* (Kausalkette 4 des Systems).

### Die vollständige Kette

$$\boxed{E_{\text{adv}} \xrightarrow{\text{I.1}} \mathcal{I}_k \xrightarrow{\text{U.2}} \omega_{k,i} \xrightarrow{\text{V.1–V.3}} D_k \xrightarrow{\text{II.2}} p_k \xrightarrow{\text{Profit}} \pi_k \xrightarrow{\text{I.2}} E_{\text{adv}}}$$

Schritt für Schritt:

1. **Werbeentscheidung (I.2):** Unternehmen wählt $E_{\text{adv},k}$ aus der Dorfman-Steiner-Bedingung.

2. **Informationsproduktion (I.1):** $E_{\text{adv},k}$ speist den Werbungsterm → $\mathcal{I}_k$ steigt; gleichzeitig Word-of-Mouth und Nutzungserfahrung.

3. **Nachfragegewichte (U.2, §6.2):** Steigende $\mathcal{I}_k$ erhöht $\omega_{k,i}$ — das Gut wird *sichtbarer* im Präferenzraum des Agenten.

4. **Konsumentscheidung (V.1–V.3, §6.3):** Höheres $\omega_{k,i}$ → höhere Nachfrage $D_k$. Gleichzeitig sinkt der effektive Preis $p_k^{\text{eff}}$ (U.3), was die Nachfrage zusätzlich stimuliert.

5. **Preisanpassung (II.2, §5.1):** Erhöhte Nachfrage $D_k > S_k$ → Preis $p_k$ steigt.

6. **Gewinn (III.3 + Bilanz):** Höherer Preis → höherer Gewinn $\pi_k = (p_k - MC_k) q_k$.

7. **Zurück zu I.2:** Höherer Gewinn → höherer Umsatz $p_k q_k$ → höheres Werbebudget (I.2: $E_{\text{adv}} = (\epsilon_{\mathcal{I},q}/\epsilon_{p,q}) \cdot p_k q_k$).

### Stabilitätsanalyse

Dieser Kreislauf ist *selbstverstärkend* — ein positiver Feedback-Loop. Ohne Gegenkräfte würde er divergieren: Ein Gut mit einem kleinen Informationsvorsprung würde exponentiell Marktanteil gewinnen, bis es die gesamte Nachfrage absorbiert (Winner-takes-all).

Die *stabilisierenden* Gegenkräfte sind:

| Gegenkraft | Gleichung | Mechanismus |
|---|---|---|
| **Informationszerfall** | I.1 ($-\omega\mathcal{I}$) | Ohne ständige Werbung: Vergessen |
| **Aufmerksamkeitsbeschränkung** | I.3 | Feste Aufmerksamkeit begrenzt Informationsaufnahme |
| **Preiskonkurrenz** | II.2 ($\lambda_k^{-1}(D-S)$) | Steigende Preise dämpfen Nachfrage |
| **Kostensättigung** | I.5 ($\mathcal{C}'' > 0$) | Steigende Grenzkosten der Informationssuche |
| **Word-of-Mouth-Sättigung** | I.1 ($\mathcal{W} \to 0$ für $\mathcal{I} \to \mathcal{I}_{\max}$) | Mundpropaganda erlischt bei Sättigung |

> **Proposition 7.4 (Informationsmonopol als Attraktor).** *Unter den Bedingungen $(i)$ $\epsilon_{\mathcal{I},q} > \epsilon_{p,q}$ (Information wirkt stärker als Preis), $(ii)$ $|\mathcal{K}| \gg A_{\max}$ (viel mehr Güter als Aufmerksamkeitsslots) und $(iii)$ $D_\mathcal{I}$ klein (geringe Diffusion), besitzt die Kausalkette einen stabilen Fixpunkt mit extremer Informationskonzentration:*
>
> $$\mathcal{I}_A^* \gg \mathcal{I}_B^* \quad \text{für ein dominantes Gut } A \text{ gegenüber allen } B$$
>
> *Dies ist das „Informationsmonopol" — ein Zustand, in dem ein Gut (oder eine Plattform) den Großteil der Aufmerksamkeit absorbiert. Es ist kein Preismonopol (das Gut muss nicht teuer sein) und kein Produktionsmonopol (andere Güter existieren) — es ist ein reines Informationsmonopol: Die Nachfrage fließt zum dominanten Gut, weil die Konsumenten nur von ihm wissen.*

### Wo Information überall eingreift: Gesamtübersicht

Zum Abschluss dieses Kapitels fassen wir zusammen, in welche Gleichungen die Information $\mathcal{I}$ als Input eingeht. Dies zeigt die *Universalität* der Information als Systemvariable:

| Gleichung | Kapitel | Wie $\mathcal{I}$ eingeht | Wirkung |
|---|---|---|---|
| **U.2** | §6.2 | $\omega_{k,i}(\mathcal{I}_i)$ | Aufmerksamkeitsfilter der Nachfrage |
| **U.3** | §6.2 | $p^{\text{eff}} = p(1 + \psi/(\mathcal{I}+\epsilon))$ | Transaktionskosten |
| **V.1a** | §6.3 | $r_i^{\text{wahr}} = r + \nu(\mathcal{I}_i)$ | Rauschfilter auf den Zins |
| **V.2** | §6.3 | $\Psi_c(\ldots, \mathcal{I}_i)$ | Informationsabhängige Psychologie |
| **L.1a** | §6.4 | $w_{L,i}^{(\text{alt})}(\mathcal{I}_i^{\text{AM}})$ | Rauschfilter auf den Alternativlohn |
| **L.5** | §6.8 | $\sigma_i^2(\mathcal{I}_i)$ | Wahrgenommene Varianz der Gründung |
| **II.2** | §5.1 | $-\phi/(\mathcal{I}+\epsilon)$ | Illiquiditätsprämie |
| **F.2** | §5.2 | $\psi/(\mathcal{I}+\epsilon)$ im Potential | Effektives Potential |
| **I.2** | §7.2 | $\epsilon_{\mathcal{I},q}$ | Werbungsintensität |
| **Ent.2** | §7.5 | $\lambda_{\text{obs}}(\dot{\mathcal{I}})$ | Informationsgetriebene Obsoleszenz |
| **VI.1** | §6.9 | $\dot{c}_i^* \propto \mathcal{I}_i - \mathcal{I}_i^{\text{ref}}$ | Referenzpunktverschiebung |
| **Φ_w** | §5.4 | Über $V_w(\mathcal{I})$ im Standortpotential | Kapitalströme |

Zwölf Gleichungen in sechs Kapiteln — es gibt *keinen* Subsystem des Gleichungssystems, das informationsunabhängig ist. Dies ist der formale Ausdruck der Aussage: *Information ist in der Ökonoaxiomatik nicht eine Nebenbedingung, sondern das fünfte fundamentale Feld — gleichberechtigt neben Vermögen, Gütern, Geld und Bevölkerung.*

> **Beobachtung 7.3 (Informationsdurchdringung).** *In den 75 Gleichungen des vollständigen Systems (S13) erscheint $\mathcal{I}$ direkt in mindestens 35 Gleichungen und indirekt (über die Kausalkette) in allen übrigen. Die Elimination von $\mathcal{I}$ (d.h. $\mathcal{I} = \infty$ für alle $k$) reduziert das System auf 50 Gleichungen — die klassische Ökonomik. Die verbleibenden 25 Gleichungen sind informationsgetrieben und haben kein Analogon in der neoklassischen Theorie.*

---

*Ende von Kapitel 7. Im folgenden Kapitel behandeln wir Geld, Kredit und die Aggregation individueller Dynamiken zu makroökonomischen Verteilungsgleichungen.*

---

# Kapitel 8 — Geld, Kredit und Aggregation

In Kapitel 4 (§4.4) haben wir die Gelderhaltung (I.4) und die Drei-Quellen-Geldschöpfung (M.1) als *Bilanzgleichungen* eingeführt: Sie beschreiben, wohin Geld fließt und woher es kommt. In Kapitel 5 haben wir gezeigt, wie Preise und Flüsse die realen Güter- und Monetärströme koppeln. In Kapitel 6 und 7 haben wir die Entscheidungsarchitektur und die Informationsdynamik der individuellen Agenten aufgebaut. Jetzt stehen wir vor zwei Aufgaben.

**Erstens**: Die Geldschöpfung *dynamisch* zu machen. M.1 beschreibt die Quellen, aber nicht die *Rückkopplung*: Wie hängt die Kreditvergabe von der Bankbilanz ab? Wie wirkt Vertrauen auf den Geldschöpfungsmultiplikator? Wann bricht die Kreditkette? Dafür brauchen wir die Leverage-Dynamik (M.3) und den Trust-Money-Nexus (M.4).

**Zweitens**: Den Übergang vom Mikro zum Makro vollziehen. Bisher beschreiben alle Gleichungen *individuelle* Agenten — Vermögen $w_i$, Portfolio $\theta_{ik}$, Information $\mathcal{I}_{ik}$. Die makroökonomischen Aggregate — BIP, Ungleichheit, Vermögensverteilung — folgen nicht durch einfaches Aufsummieren. Der Übergang erfordert die Boltzmann-Transportgleichung (IV.1), die alle Mikrodynamiken in eine einzige PDE für die Verteilung $f(w, \theta, \mathcal{I}, t)$ verpackt.

Das Kapitel enthält zwölf Gleichungen, davon acht neu:

| Gleichung | Gegenstand | Axiome | Status |
|---|---|---|---|
| **M.1** | Drei-Quellen-Geldschöpfung | A3 | Recap aus §4.4 |
| **M.2** | Bankbilanz | A3 | Recap aus §4.4 |
| **M.3** | Leverage-Dynamik | A3 + A5 | **Neu** |
| **M.4** | Trust-Money-Nexus | A3 + A5 | **Neu** |
| **E.1** | Arbitragebedingung | A5 + A4 | **Neu** |
| **P.4** | Konversionsprofit | A1 + A2 + A9 + A10 | Vollbehandlung (Erweiterung aus §4.5) |
| **P.4b** | BWS-Identität | A1 | Recap |
| **V.9** | BIP-Identität | A1 + A2 | **Neu** |
| **IV.1** | Boltzmann-Transportgleichung | A1 + A5 + A6 + A9 | **Neu** |
| **IV.2** | Aggregiertes Vermögen | (aus IV.1) | **Neu** |
| **IV.3** | Mean-Field-Limit | (aus IV.1) | **Neu** |
| **IV.4** | Ungleichheitsdynamik | (aus IV.1) | **Neu** |

---

## 8.1 Geldschöpfung: Von der Bilanz zur Dynamik (M.3, M.4)

### Rückgriff auf §4.4

In §4.4 haben wir folgende Resultate etabliert:

- **I.4** (Gelderhaltung): $\partial_t m + \nabla \cdot \vec{j}_m = g - \tau$ — die Feldgleichung für die Gelddichte.
- **M.1** (Drei-Quellen-Geldschöpfung): $\dot{M} = g_{\mathcal{Z}} + g_{\mathcal{B}} \cdot \text{Kredit}_{\text{netto}} - \tau_{\mathcal{G}}$ — Zentralbank, Geschäftsbanken, Steuertilgung.
- **M.2** (Bankbilanz): $L_b + K_b + R_b = D_b + E_b + B_b$ — die Bilanzidentität.
- **Proposition 4.2** (Bilanzsymmetrie): $\Delta M = \Delta L$ — Geldschöpfung erzeugt betragsmäßig identische Schuld.

Was fehlt: Die *Dynamik* des Geldschöpfungsmultiplikators. M.1 beschreibt die Quellen, aber der Term $g_{\mathcal{B}}$ war bisher undurchsichtig. Wie viel Kredit vergeben die Banken? Die Antwort liegt in ihrer Bilanz: Je höher der Leverage (Kredite relativ zum Eigenkapital), desto mehr Geld wird geschöpft — bis regulatorische oder marktliche Grenzen binden.

### Leverage-Dynamik (M.3)

> **Gleichung M.3 (Leverage-Dynamik).**
>
> $$\text{Lev} = \frac{L_b}{E_b}; \qquad \dot{\text{Lev}} = \phi_{\text{lev}}(r_{\text{lend}} - r_{\text{dep}}) \cdot \text{Lev} - \mu_{\text{lev}}(\text{Lev} - \text{Lev}^*)$$

Die Gleichung hat zwei Terme — einen Expansions- und einen Korrekturterm.

**Term 1: Profitgetriebene Expansion.**

$$\phi_{\text{lev}}(r_{\text{lend}} - r_{\text{dep}}) \cdot \text{Lev}$$

Die Zinsmarge $r_{\text{lend}} - r_{\text{dep}}$ — die Differenz zwischen Kreditzins und Einlagenzins — ist der Gewinnanreiz der Bank. Solange die Marge positiv ist, expandiert der Leverage: Jeder zusätzliche Kredit erzeugt Gewinn. Die Expansion ist *proportional* zum bestehenden Leverage — ein multiplikativer Prozess.

| Term | Bedeutung |
|---|---|
| $\text{Lev} = L_b / E_b$ | Leverage: Kredite relativ zum Eigenkapital |
| $r_{\text{lend}}$ | Kreditzins (was die Bank vom Kreditnehmer verlangt) |
| $r_{\text{dep}}$ | Einlagenzins (was die Bank den Sparern zahlt) |
| $r_{\text{lend}} - r_{\text{dep}}$ | Zinsmarge — der Gewinnanreiz |
| $\phi_{\text{lev}}$ | Sensitivität der Leverage-Expansion gegenüber der Marge |

Die axiomatische Herkunft: Von A5 (Nutzenmaximierung) — Banken maximieren ihren Gewinn, und der Gewinn ist proportional zur Zinsmarge mal Kreditvolumen: $\Pi_b \propto (r_{\text{lend}} - r_{\text{dep}}) \cdot L_b$.

**Term 2: Regulatorische Korrektur.**

$$-\mu_{\text{lev}}(\text{Lev} - \text{Lev}^*)$$

Der Leverage relaxiert *mean-reverting* zu einem Zielwert $\text{Lev}^*$, der durch Regulierung (Basel III: $\text{Lev}^* \leq 1/\alpha_{\text{Basel}}$) und interne Risikosteuerung bestimmt wird. Die Relaxationsgeschwindigkeit $\mu_{\text{lev}}$ misst, wie schnell die Korrektur wirkt.

### Axiometrische Eigenschaften von M.3

Die Gleichung wird *nicht* durch eine spezifische Funktionalform festgelegt — die axiometrischen Eigenschaften sind:

1. **Dimensionslosigkeit**: $\text{Lev}$ ist eine reine Verhältniszahl.
2. **Nicht-Negativität**: $\text{Lev} \geq 0$ (ökonomische Bedingung).
3. **Obere Schranke**: Basel verlangt $\text{Lev} \leq 1/\alpha_{\text{Basel}}$ (regulatorische Nebenbedingung).
4. **Expansion bei positiver Marge**: $\dot{\text{Lev}} > 0$ wenn $r_{\text{lend}} > r_{\text{dep}}$ und der Leverage unterhalb des Ziels liegt.
5. **Mean-Reversion**: Ohne Gewinnanreiz ($r_{\text{lend}} = r_{\text{dep}}$) relaxiert der Leverage exponentiell zum Ziel.

### Grenzfälle und Dynamik

**Fall 1: Keine Marge ($r_{\text{lend}} = r_{\text{dep}}$).** Der Expansionsterm verschwindet. Es bleibt reine Relaxation:

$$\dot{\text{Lev}} = -\mu_{\text{lev}}(\text{Lev} - \text{Lev}^*)$$

Die Bank konvergiert exponentiell zu ihrem Ziellevel — keine endogene Dynamik. Dies ist die Situation unter starker Regulierung oder in einem Niedrigzinsumfeld, in dem die Margen komprimiert sind (Japan seit 1990).

**Fall 2: Keine Regulierung ($\mu_{\text{lev}} \to 0$).** Der Korrekturterm verschwindet:

$$\dot{\text{Lev}} = \phi_{\text{lev}}(r_{\text{lend}} - r_{\text{dep}}) \cdot \text{Lev}$$

Dies ist eine *exponentielle Differentialgleichung* — der Leverage wächst exponentiell, solange die Marge positiv ist. Dies ist der Minsky-Mechanismus: In Zeiten stabilen Wachstums expandieren Banken ihren Leverage immer weiter, bis ein Schock das Eigenkapital trifft und die Pyramide kollabiert.

**Fall 3: Krise ($E_b$ fällt durch Kreditausfälle).** Wenn Kreditnehmer ausfallen, sinkt das Eigenkapital $E_b$ — der Leverage $\text{Lev} = L_b/E_b$ springt *nach oben*. Die regulatorische Schranke bindet → erzwungener Leverage-Abbau (*Deleveraging*) → Kreditkontraktion → monetäre Schrumpfung. Dies ist der *endogene* Transmissionsmechanismus der Finanzkrise: ein Buchungsereignis (Kreditausfall) erzeugt eine reale Kontraktion (weniger Investition, weniger Produktion, weniger BIP).

> **Proposition 8.1 (Minsky-Instabilität).** *Im Regime $\mu_{\text{lev}} \to 0$ (schwache Regulierung) wächst der Leverage exponentiell: $\text{Lev}(t) = \text{Lev}(0) \cdot \exp[\phi_{\text{lev}}(r_{\text{lend}} - r_{\text{dep}})t]$. Das System ist strukturell instabil: Jeder noch so kleine Schock auf $E_b$ erzeugt erzwungenes Deleveraging, das sich über die Kreditkette (M.1 → Investition → Produktion → Kreditausfälle → $E_b \downarrow$) selbst verstärkt.*

### Kopplung an andere Gleichungen

M.3 koppelt an:

| Gleichung | Kopplungskanal |
|---|---|
| **M.1** | Leverage bestimmt Kreditkapazität: $g_{\mathcal{B}} \propto \text{Lev} \cdot E_b$ |
| **E.1** (§8.2) | $r_{\text{lend}}$ erscheint in der Arbitragebedingung |
| **VIII.6** (Kap. 10) | Bankrott: $E_b < 0$ → Bankausfall → diskontinuierter Leverage-Reset |
| **VII.1** (Kap. 9) | Vertrauen $\mathcal{T}$: Bankenstress senkt $\mathcal{T}$ → wirkt auf M.4 |

### Trust-Money-Nexus (M.4)

Der Geldschöpfungsmultiplikator — das Verhältnis von Giralgeldmenge $M$ zu Basisgeld $M_0$ — ist in der Lehrbuchökonomik eine Konstante: $m = M/M_0 = 1/\alpha_{\text{Reserve}}$. In der Realität ist der Multiplikator *endogen*, weil Banken nur dann Kredit vergeben, wenn sie den Kreditnehmern vertrauen, und Kreditnehmer nur dann Kredit nachfragen, wenn die Zinsen tragbar sind.

> **Gleichung M.4 (Trust-Money-Nexus).**
>
> $$m_{\text{mult}} = m_0 \cdot \mathcal{T} \cdot (1 - \alpha_r \cdot r)$$

| Term | Bedeutung |
|---|---|
| $m_{\text{mult}} = M / M_0$ | Geldschöpfungsmultiplikator (Giralgeld / Basisgeld) |
| $m_0$ | Struktureller Basismultiplikator |
| $\mathcal{T}$ | Vertrauensniveau (aus VII.1, langsame Variable) |
| $r$ | Nominalzins (gesetzt durch Taylor-Regel Z.1) |
| $\alpha_r$ | Zinssensitivität der Kreditnachfrage |

Die axiomatische Herkunft: A3 (Gelderhaltung) und A5 (Nutzenmaximierung). Banken vergeben Kredit (und schöpfen Geld) nur, wenn zwei Bedingungen erfüllt sind: (1) Sie vertrauen den Kreditnehmern ($\mathcal{T} > 0$), und (2) die Kreditnehmer fragen Kredit nach (Nachfrage fällt mit dem Zins).

### Grenzfälle von M.4

**Fall 1: Volles Vertrauen ($\mathcal{T} = 1$).** Der Multiplikator ist:

$$m_{\text{mult}} = m_0 \cdot (1 - \alpha_r \cdot r)$$

Dies ist der *Standard-Lehrbuch-Multiplikator* — nur zinsabhängig. Bei $r = 0$ (Nullzinspolitik) erreicht er sein Maximum: $m_{\text{mult}} = m_0$, bestimmt allein durch die strukturellen Parameter des Bankensystems.

**Fall 2: Panik ($\mathcal{T} \to 0$).** Der Multiplikator kollabiert:

$$m_{\text{mult}} \to 0$$

Das gesamte von der Zentralbank geschöpfte Basisgeld $M_0$ bleibt als *Überschussreserven* bei den Geschäftsbanken liegen — es findet keine Kreditvergabe statt. Dies ist die *Kreditklemme* (Credit Crunch). Die Zentralbank kann den Multiplikator nicht erzwingen — sie kann Basisgeld drucken, aber nicht Vertrauen. Dies erklärt, warum die massiven QE-Programme nach 2008 die Geldmenge $M_0$ vervielfachten, ohne dass die Giralgeldmenge $M$ proportional stieg: $\mathcal{T}$ war kollabiert.

**Fall 3: Hohe Zinsen ($r \to 1/\alpha_r$).** Auch bei vollem Vertrauen kollabiert der Multiplikator:

$$m_{\text{mult}} \to 0$$

Zinsen so hoch, dass keine Kreditnachfrage mehr besteht — die *Liquiditätsfalle von oben*. Dies ist das symmetrische Gegenstück zur Liquiditätsfalle von unten ($r \to 0$, aber keine Nachfrage wegen Deflationserwartungen).

**Fall 4: Nullzinspolitik bei partiellem Vertrauen ($r = 0$, $\mathcal{T} < 1$).** Der Multiplikator ist:

$$m_{\text{mult}} = m_0 \cdot \mathcal{T}$$

Der Multiplikator hängt *ausschließlich* vom Vertrauen ab. Dies ist die Situation der Eurozone 2012–2019: Nullzinsen, aber gebrochenes Vertrauen → subnormaler Multiplikator → anämisches Geldmengenwachstum trotz massiver Basisgeldexpansion.

> **Beobachtung 8.1 (Asymmetrie der Geldpolitik).** *M.4 formalisiert eine fundamentale Asymmetrie der Geldpolitik: Die Zentralbank kann den Multiplikator durch Zinssenkung nach unten entsperren (Nachfragekanal), aber sie kann ihn durch Liquiditätsinjektionen nicht erzwingen, wenn $\mathcal{T} \approx 0$ (Vertrauenskanal). Geldpolitik ist effektiver in Boom-Phasen (wo $\mathcal{T}$ hoch ist) als in Krisen (wo $\mathcal{T}$ kollabiert). Dies ist das „pushing on a string"-Problem von Keynes.*

### Die Kopplung M.1 – M.3 – M.4

Die drei Geldgleichungen bilden eine geschlossene Kette:

$$\text{M.1} \quad \dot{M} = g_{\mathcal{Z}} + \underbrace{m_{\text{mult}}}_{\text{M.4}} \cdot \underbrace{\text{Lev} \cdot E_b}_{\text{M.3}} \cdot \dot{r}_{\text{lend}} - \tau_{\mathcal{G}}$$

| Schritt | Gleichung | Prozess |
|---|---|---|
| 1. Zentralbank senkt $r$ | Z.1 (Taylor) | $r \downarrow$ |
| 2. Zinsmarge steigt | | $r_{\text{lend}} - r_{\text{dep}} \uparrow$ |
| 3. Leverage expandiert | M.3 | $\text{Lev} \uparrow$ |
| 4. Multiplikator steigt | M.4 | $m_{\text{mult}} \uparrow$ (über niedrigeres $r$) |
| 5. Geldschöpfung steigt | M.1 | $\dot{M} \uparrow$ |
| 6. Kredit fließt in Investition | E.1 (§8.2) | Portfolioreallokation |
| 7. Produktion und BIP steigen | V.9 (§8.4) | Output $\uparrow$ |
| 8. Inflation steigt | II.2 | $\pi \uparrow$ |
| 9. Zentralbank hebt $r$ an | Z.1 | Rückkopplung → stabilisierend |

Dies ist die **Kette 5** aus S13 §11.4 — der vollständige Geldschöpfungskreislauf, der von der Zentralbankentscheidung über die Kreditvergabe und die Investition zum BIP und zurück führt. Die Instabilität entsteht, wenn der *Vertrauenskanal* den *Zinskanal* dominiert: In der Krise bricht M.4 zusammen ($\mathcal{T} \to 0$), und kein noch so niedriges $r$ kann die Kreditkette reparieren.

---

## 8.2 Arbitragebedingung (E.1)

In Kapitel 6 (§6.5) haben wir die Portfolioentscheidung (III.2) eingeführt: Agenten reallokieren ihr Vermögen zwischen verschiedenen Anlageklassen, getrieben durch den Gradienten der risikoadjustierten Renditen. Die Arbitragebedingung E.1 ist die *Gleichgewichtsbedingung* dieser Portfoliodynamik — der Zustand, in dem $\dot{\theta}_{ik} = 0$ für alle Agenten und Anlageklassen.

> **Gleichung E.1 (Sechs-Klassen-Arbitragebedingung).**
>
> $$r_K - \gamma\sigma_K^2 = r - \pi = r_R \cdot (1 - \tau_R) = r_L \cdot (1 - p_{\text{Ausfall}}) = r_I \cdot \mathcal{I}_k$$

Eine einzige Gleichung, die alle sechs Güterklassen $\mathcal{K}_1$–$\mathcal{K}_6$ verbindet.

### Term-für-Term-Aufschlüsselung

**Term 1: Risikoadjustierte Kapitalrendite ($\mathcal{K}_1$).**

$$r_K - \gamma\sigma_K^2$$

| Größe | Bedeutung |
|---|---|
| $r_K = \alpha_K \cdot Y/K - \delta_K$ | Kapitalrendite: Grenzprodukt minus Abschreibung |
| $\gamma$ | Risikoaversion (endogen, aus VI.2) |
| $\sigma_K^2$ | Varianz der Kapitalrendite |
| $r_K - \gamma\sigma_K^2$ | Certainty-equivalent return: was der Agent *sicher* erhalten würde, um indifferent zu sein |

Die axiomatische Herkunft: A5 (Nutzenmaximierung) impliziert, dass risikoaverse Agenten ($\gamma > 0$) Renditen durch ihre Varianz diskontieren. Dies ist die *Mean-Variance*-Struktur der Portfoliotheorie — aber hier als *axiometrische Eigenschaft*, nicht als spezifische Nutzenfunktion.

**Term 2: Realzins ($\mathcal{K}_5$).**

$$r - \pi$$

Die Rendite des Geldes: Nominalzins $r$ (gesetzt durch Z.1) minus Inflation $\pi$. Geld ist das *risikofreie* Asset — es hat $\sigma^2 = 0$ (nominell), aber sein Realwert erodiert mit $\pi$.

**Term 3: Netto-Mietrendite ($\mathcal{K}_2$).**

$$r_R \cdot (1 - \tau_R)$$

| Größe | Bedeutung |
|---|---|
| $r_R = p_{\text{Nutzung}} / p_{\text{Bestand}}$ | Bruttomietrendite: Nutzungspreis / Bestandspreis |
| $\tau_R$ | Steuersatz auf Mieteinkünfte |
| $r_R(1 - \tau_R)$ | Nettomietrendite nach Steuern |

Die Steuer $\tau_R$ verzerrt die Arbitrage: Höhere Steuern auf Mieteinnahmen senken die Nettorendite → weniger Kapital fließt in Immobilien → Preise sinken, bis $r_R(1 - \tau_R)$ wieder dem risikofreien Zins entspricht.

**Term 4: Ausfallbereinigte Patentrendite ($\mathcal{K}_4$).**

$$r_L \cdot (1 - p_{\text{Ausfall}})$$

| Größe | Bedeutung |
|---|---|
| $r_L = p_{\text{Lizenz}} \cdot D_k / p_{\text{Patent}}$ | Bruttolizenzrendite: Lizenzgebühr × Nachfrage / Patentpreis |
| $p_{\text{Ausfall}}$ | Ausfallwahrscheinlichkeit des Patents (Konkurrent umgeht, Gericht kippt) |
| $r_L(1 - p_{\text{Ausfall}})$ | Erwartete Nettorendite |

**Term 5: Informationsgewichtete Rendite ($\mathcal{K}_6$).**

$$r_I \cdot \mathcal{I}_k$$

| Größe | Bedeutung |
|---|---|
| $r_I = \partial Y / \partial \mathcal{I}_k$ | Grenzproduktivität der Information |
| $\mathcal{I}_k$ | Informationsniveau für Gut $k$ |
| $r_I \cdot \mathcal{I}_k$ | Effektive Informationsrendite |

Hier zeigt sich die *Informationskopplung*: Die Rendite der Information ist mit dem Informationsniveau skaliert — perfekt informierte Agenten ($\mathcal{I} \to \infty$) erhalten die volle Informationsrendite; uninformierte Agenten ($\mathcal{I} \to 0$) nehmen sie nicht wahr. Dies ist keine Marktunvollkommenheit — es ist ein *Bewertungsproblem*: Wer nicht weiß, dass eine Information wertvoll ist, kann ihren Wert nicht abschätzen.

### Axiometrische Eigenschaften von E.1

> **Definition 8.1 (Arbitrage-Gleichgewicht).** *Das System befindet sich im Arbitrage-Gleichgewicht, wenn alle paarweisen risikoadjustierten Renditen übereinstimmen:*
>
> $$r_\alpha^{\text{adj}} = r_\beta^{\text{adj}} \quad \forall \alpha, \beta \in \{\mathcal{K}_1, \ldots, \mathcal{K}_6\}$$
>
> *Abweichungen von E.1 sind die Triebkräfte der Portfolioreallokation (III.2).*

Die axiometrischen Eigenschaften:

1. **Keine Funktionalform**: E.1 legt die *Struktur* der Arbitrage fest (welche Terme müssen gleich sein), nicht die spezifischen Formeln für $r_K$, $r_R$, etc.
2. **Informationsabhängigkeit**: Über den Term $r_I \cdot \mathcal{I}_k$ ist die Arbitrage *nicht* davon unabhängig, was Agenten wissen. Im Limit $\mathcal{I} \to \infty$ verschwindet diese Abhängigkeit.
3. **Risikoaversionsabhängigkeit**: Über $\gamma\sigma_K^2$ ist die Arbitrage *subjektiv* — verschiedene Agenten mit verschiedenem $\gamma_i$ (aus VI.2) sehen verschiedene risikoadjustierte Renditen.
4. **Steuerverzerrung**: Der Staat verzerrt die Arbitrage durch asymmetrische Besteuerung ($\tau_R$, aber nicht $\tau_K$ im gleichen Maße).

### Grenzfälle von E.1

**Fall 1: Perfekte Information ($\mathcal{I} \to \infty$).** E.1 reduziert sich auf die neoklassische No-Arbitrage-Bedingung:

$$r_K - \gamma\sigma_K^2 = r - \pi$$

Dies ist die *CAPM First-Order-Condition* — die Grundlage der modernen Finanztheorie. Die anderen Terme (Mieten, Patente, Information) sind ebenfalls präsent, aber der Informationsterm entfällt.

**Fall 2: Risikoneutralität ($\gamma = 0$).** Die Varianzkorrektur verschwindet:

$$r_K = r - \pi = r_R(1 - \tau_R) = r_L(1 - p_{\text{Ausfall}}) = r_I \cdot \mathcal{I}_k$$

Deterministische Arbitrage — keine Risikoprämie. Alle Returns werden am Erwartungswert gemessen.

**Fall 3: Nur ein Asset aktiv.** Jede Paargleichheit reduziert sich auf eine Zwei-Term-Bedingung:
- Nur Kapital und Geld: $r_K - \gamma\sigma_K^2 = r - \pi$ → **Fisher-Gleichung** mit Risikoprämie.
- Nur Miete und Zins: $r_R(1 - \tau_R) = r - \pi$ → **Campbell-Shiller**-Bedingung für Immobilien.

**Fall 4: EMH.** Wenn E.1 zu jedem Zeitpunkt $t$ hält, ist das System in einem permanenten Arbitrage-Gleichgewicht. Dies ist die formale Entsprechung der **Effizienzmarkthypothese** (EMH) — die in der Ökonoaxiomatik kein Axiom ist, sondern ein *Grenzfall einer Dynamik*.

> **Proposition 8.2 (EMH als Grenzfall).** *Die Effizienzmarkthypothese ist äquivalent zu $\dot{\theta}_{ik} = 0$ für alle $i, k$ — d.h. keine Portfolioreallokation findet statt. Im vollständigen System (mit endogenem $\gamma_i$, beschränkter $\mathcal{I}_{ik}$ und Herdenverhalten aus VI.4) ist dieser Zustand generisch instabil: Exogene Schocks erzeugen persistente Abweichungen von E.1, die sich durch Herdenverhalten verstärken, bevor die Arbitrage-Kräfte (III.2) sie korrigieren.*

### Kopplung von E.1 an das Gesamtsystem

| Gleichung | Kopplungskanal |
|---|---|
| **III.2** (Portfolio) | Abweichungen von E.1 treiben Portfolioreallokation |
| **II.2** (Preise) | Portfolio-Shifts ändern Nachfrage → Preise → Renditen → E.1 passt sich an |
| **M.3** (Leverage) | $r_{\text{lend}}$ erscheint auf der Bankseite → Leverage beeinflusst Kapitalangebot |
| **Z.1** (Taylor-Regel) | Zentralbank setzt $r$ → verschiebt alle Arbitrage-Relationen |
| **VI.2** (Risikoaversion) | Endogenes $\gamma_i$ → verschiedene Agenten sehen E.1 unterschiedlich |
| **I.1** (Information) | $\mathcal{I}_k$ in Term 5 → Informationsstand bestimmt wahrgenommene Renditen |

---

## 8.3 Konversionsprofit und Wertschöpfung (P.4)

In §4.5 haben wir die Nicht-Erhaltung des ökonomischen Werts diskutiert und den Konversionsprofit als eine der drei Quellen der Wertänderung eingeführt. Hier geben wir die vollständige Gleichung mit allen Termen.

### Die vollständige Konversionsprofitgleichung

> **Gleichung P.4 (Konversionsprofit).**
>
> $$\Pi^{(\text{Konv})} = \sum_\alpha p_\alpha \dot{n}_\alpha^{(\text{Konv})} - w_L \cdot L^{(\text{Konv})} - r \cdot K^{(\text{Konv})} - c_{\mathcal{I}}(\mathcal{I})$$

Die Gleichung liest sich als Bilanzidentität: Der *Profit* einer Konversion ist die *Nettowertänderung* der Güterbestände minus alle Faktorkosten.

| Term | Bedeutung | Vorzeichen |
|---|---|---|
| $\sum_\alpha p_\alpha \dot{n}_\alpha^{(\text{Konv})}$ | Nettowertänderung der Güter (Output $-$ Input, bewertet zu Marktpreisen) | $+/-$ |
| $w_L \cdot L^{(\text{Konv})}$ | Arbeitskosten der Konversion | $-$ |
| $r \cdot K^{(\text{Konv})}$ | Kapitalkosten (Maschinen, Gebäude) | $-$ |
| $c_{\mathcal{I}}(\mathcal{I})$ | Informationskosten (Know-how für die Konversion) | $-$ |
| $\Pi^{(\text{Konv})}$ | Profit (oder Verlust) der konvertierenden Einheit | $+/-$ |

### Axiomatische Herleitung

- **A2** (Gütererhaltung via K.1): Die physischen Güter müssen bilanziert werden — die Konversion ändert den Bestand $n_\alpha$.
- **A9** (Güterdiversität): Verschiedene Güterklassen haben verschiedene Konversionskosten. Die Umwandlung von Rohstoffen ($\mathcal{K}_3$) in Fertigprodukte ($\mathcal{K}_1$) kostet Arbeit und Kapital.
- **A10** (Informationskosten): $c_{\mathcal{I}}(\mathcal{I})$ ist konvex (§2.10) — die einfache Information ist billig, die spezialisierte teuer. Ein Bäcker braucht wenig Know-how, ein Halbleiterfertiger viel.
- **A1** (Vermögenserhaltung): Der Profit $\Pi$ ändert das Vermögen des Agenten via I.1.

### Die fundamentale Einsicht: Wert wird geschöpft, nicht umverteilt

$$p_{\text{out}} \cdot \Delta n_{\text{out}} \neq \sum_{\text{in}} p_{\text{in}} \cdot |\Delta n_{\text{in}}|$$

Dies ist der Kern der Wertschöpfung: Die *Bewertung* des Outputs übersteigt (oder unterschreitet) die Bewertung der Inputs — nicht weil sich die Physik geändert hat (die Gütererhaltung gilt per A2), sondern weil verschiedene Güter verschiedene *Preise* haben, und Preise werden vom Markt (II.2) gesetzt, nicht von der Physik.

Drei Regime:

| Regime | Bedingung | Beispiel |
|---|---|---|
| **Mehrwert** | $\Pi > 0$ | Rohstoff → Fertigprodukt (Automobilproduktion) |
| **Wertverlust** | $\Pi < 0$ | Fehlproduktion, Obsoleszenz, gescheiterte F&E |
| **Reine Umklassifizierung** | $\Pi = 0$, $L = K = c_{\mathcal{I}} = 0$ | Regulatorische Umklassifizierung (Gut wird verboten/freigegeben) |

### Informationskosten als Wettbewerbsbarriere

Der Term $c_{\mathcal{I}}(\mathcal{I})$ verdient besondere Aufmerksamkeit. Die Konvexität von $c_{\mathcal{I}}$ (aus A10) erzeugt eine natürliche *Barriere*:

- Für einfache Konversionen (Bäckerei): $c_{\mathcal{I}}$ ist klein → viele Anbieter → Wettbewerb → $\Pi \to 0$.
- Für komplexe Konversionen (Halbleiter): $c_{\mathcal{I}}$ ist groß → wenige Anbieter → oligopolistischer Profit → $\Pi > 0$ persistent.

> **Beobachtung 8.2 (Informationsrente).** *In Sektoren mit hohen Informationskosten $c_{\mathcal{I}}$ entsteht eine persistente Informationsrente: $\Pi > 0$ auch im langfristigen Gleichgewicht, weil nur wenige Agenten die Informationskosten tragen können. Dies erklärt die dauerhaft hohen Margen in wissensintensiven Sektoren (Pharma, Software, Halbleiter) ohne Rückgriff auf Monopolmacht oder Marktversagen.*

### Kopplung an das Gesamtsystem

P.4 koppelt an drei zentrale Gleichungen:

| Gleichung | Kopplungskanal |
|---|---|
| **V.9** (§8.4) | Summe aller $\Pi + w_LL + rK$ = BIP |
| **I.1** (§4.3, §7.1) | $\Pi$ geht in $\dot{w}_i$ ein → Vermögensdynamik |
| **K.1** (§3.1) | Konversionsraten $\kappa_{\alpha\beta}$ bestimmen, welche Güter umgewandelt werden |
| **II.2** (§5.1) | Outputpreise werden vom Markt gesetzt, nicht vom Produzenten |

---

## 8.4 BIP-Identität (V.9)

Das Bruttoinlandsprodukt ist keine *Gleichung* — es ist eine *Buchhaltungsidentität*, die die mikro-ökonomischen Konversionsprofite (P.4) zu einem makro-ökonomischen Aggregat zusammenfasst. V.9 hat zwei äquivalente Darstellungen, die den zwei klassischen Berechnungsmethoden entsprechen.

### Produktionsansatz

> **Gleichung V.9 (BIP-Identität, Produktionsansatz).**
>
> $$\text{BIP}(t) = \sum_j \bigl(p_k q_{jk} - VL_j\bigr) = \mathcal{V}^{\text{BWS}}$$

| Term | Bedeutung |
|---|---|
| $p_k q_{jk}$ | Umsatz von Firma $j$ für Gut $k$ (Preis × produzierte Menge) |
| $VL_j$ | Vorleistungen (intermediäre Inputs) von Firma $j$ |
| $p_k q_{jk} - VL_j$ | Bruttowertschöpfung (BWS) von Firma $j$ |
| $\mathcal{V}^{\text{BWS}}$ | Gesamtwirtschaftliche Bruttowertschöpfung |

### Einkommensansatz (P.4b)

> **Gleichung P.4b (BIP-Identität, Einkommensansatz).**
>
> $$\text{BWS} = \sum_{\text{Konversionen}} \bigl(\Pi + w_L L + r K\bigr) = Y$$

Jede Konversion erzeugt Profit ($\Pi$), Löhne ($w_L L$) und Kapitalerträge ($rK$). Die Summe über alle Konversionen in der Volkswirtschaft ist das BIP.

### Die Äquivalenz

V.9 und P.4b sind *nicht* zwei unabhängige Gleichungen — sie sind dieselbe Identität in zwei Lesrichtungen:

| Ansatz | Summiert über | Misst |
|---|---|---|
| **V.9 (Produktion)** | Firmen $j$: Output minus Vorleistungen | Wertschöpfung = Wo wird Wert erzeugt? |
| **P.4b (Einkommen)** | Konversionen: Profit + Löhne + Kapital | Einkommensverteilung = An wen fließt der Wert? |

Die Äquivalenz ist eine *Konsequenz* von P.4: Da der Profit $\Pi$ als Residuum definiert ist (Umsatz minus alle Kosten), ist die Summe $\Pi + w_LL + rK$ identisch mit dem Umsatz minus Vorleistungen.

### Axiomatische Einordnung

V.9 folgt aus zwei Axiomen:

- **A1** (Vermögenserhaltung): Alle Zuflüsse und Abflüsse werden bilanziert → keine Wertschöpfung verschwindet.
- **A2** (Gütererhaltung): Die physische Produktion $q_{jk}$ wird durch P.3 bestimmt → die Summe ist wohldefiniert.

V.9 ist kein Verhaltensgesetz — es ist eine Identität. Kein Modell kann sie verletzen. Ihre Rolle im System ist die *Konsistenzprüfung*: Das BIP „von oben" (V.9) und das BIP „von unten" (Summe der individuellen Konversionsprofite P.4) müssen übereinstimmen.

### Kopplung an das Gesamtsystem

| Gleichung | Kopplungskanal |
|---|---|
| **I.2** (§4.3) | $Y$ in $\dot{W} = Y - C$ kommt aus V.9 |
| **III.3** (§6.6) | Die Produktion $q_{jk}$ wird durch die Produktionsentscheidung bestimmt |
| **II.2** (§5.1) | Die Preise $p_k$ werden durch die Preisdynamik bestimmt |
| **IV.3** (§8.5) | Mean-Field: $d\bar{w}/dt = Y/N - C/N + \bar{\theta}\cdot\dot{p}$ — reproduziert V.9 pro Kopf |
| **Z.1** (Taylor) | $\pi$ in der Taylor-Regel wird aus der Veränderung von V.9 abgeleitet |

> **Proposition 8.3 (Mikro-Makro-Konsistenz über V.9).** *Die BIP-Identität V.9 verbindet die mikro-ökonomische Produktionsentscheidung (III.3) über die Konversionsprofite (P.4) mit dem makro-ökonomischen Aggregat $Y$. In jeder konsistenten Lösung des Gleichungssystems muss gelten:*
>
> $$Y = \sum_j (p_k q_{jk} - VL_j) = \sum_j (\Pi_j + w_{Lj}L_j + r_jK_j)$$
>
> *Diese Identität ist die notwendige Bedingung für die Stock-Flow-Konsistenz des Gesamtsystems (Kapitel 12).*

---

## 8.5 Aggregation: Die Boltzmann-Transportgleichung (IV.1–IV.4)

Dieses Teilkapitel vollzieht den konzeptionell tiefsten Schritt der gesamten Theorie: den Übergang vom individuellen Agenten zur makro-ökonomischen Verteilung. Bisher — in Kapiteln 4 bis 7 — haben wir die Gleichungen *eines einzelnen Agenten $i$* geschrieben: sein Vermögen ($w_i$), sein Portfolio ($\theta_{ik}$), seine Information ($\mathcal{I}_{ik}$). Das Gesamtsystem enthält $N$ solcher Agenten, und die Frage ist: *Was können wir über die Verteilung aller $N$ Zustände sagen, ohne jedes einzelne $i$ zu tracken?*

Die Antwort liefert die Boltzmann-Transportgleichung — ein Werkzeug aus der statistischen Physik, das die Mikrodynamiken in eine einzige partielle Differentialgleichung für die *Verteilungsfunktion* $f(w, \theta, \mathcal{I}, t)$ überführt.

### Motivation: Warum Aufsummieren nicht reicht

Der naive Ansatz wäre: Summiere die $N$ individuellen Gleichungen I.1 auf und erhalte eine Gleichung für das Aggregat $W = \sum_i w_i$. Das ist die Gleichung I.2 ($\dot{W} = Y - C$) — und sie funktioniert für den *Mittelwert*. Aber sie verliert alle Information über die *Verteilung*: Zwei Volkswirtschaften mit demselben BIP ($Y$) und demselben Konsum ($C$) können radikal verschiedene Vermögensverteilungen haben — eine egalitär, eine extrem ungleich. Die aggregierte Gleichung sieht keinen Unterschied.

Das Problem ist *nicht nur*, dass wir die Verteilung nicht kennen — das Problem ist, dass die *Aggregate selbst falsch werden*, wenn wir die Verteilung ignorieren. Der Grund liegt in der **Nichtlinearität** der Mikro-Gleichungen. Die Konsumfunktion $c_i(w_i)$ ist konkav (Engel-Kurve: Arme konsumieren einen größeren Anteil ihres Vermögens als Reiche). Die Risikoaversion $\gamma_i(w_i)$ hängt vom Vermögen ab. Die Produktionsentscheidung $q_j(w_j, \mathcal{I}_j)$ ist nichtlinear in beiden Argumenten. Für *jede* nichtlineare Funktion $g$ gilt die **Jensen-Ungleichung**:

$$\langle g(w) \rangle \neq g(\langle w \rangle)$$

Konkret: Der *aggregierte Konsum* einer Volkswirtschaft mit Vermögensungleichheit ist *nicht gleich* dem Konsum, den ein repräsentativer Agent mit dem Durchschnittsvermögen $\bar{w}$ wählen würde. Bei konkaver Konsumfunktion gilt $\langle c(w) \rangle > c(\langle w \rangle)$ — eine ungleiche Gesellschaft konsumiert *mehr* als eine gleiche mit demselben Durchschnittsvermögen (weil die Armen anteilig mehr konsumieren und die Reichen anteilig weniger sparen, als der Durchschnitt suggeriert). Analoges gilt für Portfolioentscheidungen, Gründungsneigung, Informationsnachfrage und jede andere nichtlineare Funktion im System.

Die Konsequenz ist fundamental: **Ein Modell, das nur mit Mittelwerten arbeitet (repräsentativer Agent), begeht bei jeder nichtlinearen Gleichung einen systematischen Aggregationsfehler.** Dieser Fehler ist nicht klein — er kann das Vorzeichen von Politikeffekten umkehren, Krisen unsichtbar machen und Ungleichheitsdynamiken vollständig eliminieren.

| Ansatz | Beschreibt | Verliert | Aggregationsfehler |
|---|---|---|---|
| Individuelle Gleichung I.1 | $w_i(t)$ für Agent $i$ | Nichts — volle Information | Keiner |
| Summe $\sum_i$ I.1 = I.2 | $W(t) = \sum_i w_i$ | Gesamte Verteilung | Jensen-Fehler bei jeder nichtlinearen Gleichung |
| **IV.1: Boltzmann** | $f(w, \theta, \mathcal{I}, t)$ | Individuelle Identitäten (aber nicht die Statistik) | **Keiner** — volle Verteilungsinformation |

Die Boltzmann-Gleichung ist daher nicht nur ein *bequemer Kompromiss* — sie ist die *notwendige* mathematische Struktur für korrekte Aggregation in einem System mit heterogenen Agenten und nichtlinearen Gleichungen. Sie verfolgt nicht mehr jeden einzelnen Agenten (das wäre für $N \sim 10^6$ numerisch untragbar), aber sie bewahrt die volle *statistische* Information — Mittelwert, Varianz, Schiefe, Wölbung und jedes höhere Moment — und damit die korrekte Berechnung *aller* Aggregate.

### Die Gleichung

> **Gleichung IV.1 (Boltzmann-Transportgleichung).**
>
> $$\frac{\partial f}{\partial t} + \frac{\partial}{\partial w}[\dot{w}f] + \frac{\partial}{\partial\theta}[\dot{\theta}f] + \frac{\partial}{\partial\mathcal{I}}[\dot{\mathcal{I}}f] = \mathcal{C}[f]$$

Die Verteilungsfunktion $f(w, \theta, \mathcal{I}, t)$ beschreibt die Dichte der Agenten im *Zustandsraum*: $f \, dw \, d\theta \, d\mathcal{I}$ ist die Zahl der Agenten im Zustandsvolumen $[w, w+dw] \times [\theta, \theta+d\theta] \times [\mathcal{I}, \mathcal{I}+d\mathcal{I}]$ zur Zeit $t$.

### Linke Seite: Fluss im Zustandsraum

Die linke Seite hat vier Terme — sie beschreiben, wie sich die Verteilung *deterministisch* verschiebt, weil die Agenten sich im Zustandsraum bewegen.

**Term 1: Zeitliche Änderung.**

$$\frac{\partial f}{\partial t}$$

Wie sich die Verteilung mit der Zeit ändert — das ist, was wir berechnen wollen.

**Term 2: Vermögensfluss.**

$$\frac{\partial}{\partial w}[\dot{w}f]$$

Die Agenten bewegen sich entlang der $w$-Achse mit Geschwindigkeit $\dot{w}$, die durch I.1 bestimmt wird:

$$\dot{w}_i = y_i - c_i + \theta_{ik}\dot{p}_k - c_{\mathcal{I}}(\mathcal{I}_i)$$

Agenten mit positivem $\dot{w}$ wandern nach rechts (werden reicher), Agenten mit negativem $\dot{w}$ nach links (werden ärmer). Der Term $\partial_w[\dot{w}f]$ beschreibt den resultierenden Strom.

**Term 3: Portfoliofluss.**

$$\frac{\partial}{\partial\theta}[\dot{\theta}f]$$

Agenten reallokieren ihre Portfolios gemäß III.2. Wenn die risikoadjustierten Renditen (E.1) ungleich sind, fließen Portfolios in die rentablere Richtung.

**Term 4: Informationsfluss.**

$$\frac{\partial}{\partial\mathcal{I}}[\dot{\mathcal{I}}f]$$

Agenten lernen (I.1 info: Werbung, Word-of-Mouth, Erfahrung) und vergessen ($-\omega\mathcal{I}$). Der Informationsfluss verschiebt die Verteilung entlang der $\mathcal{I}$-Achse.

### Rechte Seite: Kollisionsterm

$$\mathcal{C}[f]$$

Der Kollisionsterm beschreibt *diskrete Interaktionen* zwischen Agenten — Prozesse, die die Verteilung *sprunghaft* ändern, nicht durch glatten Fluss:

| Interaktion | Wirkung auf $f$ |
|---|---|
| Handel | Agent $i$ verliert $\Delta w$, Agent $j$ gewinnt $\Delta w$ → lokale Umverteilung in $w$ |
| Kreditvergabe | Bank verliert Reserven, Kreditnehmer gewinnt Guthaben → koppelt an M.1 |
| Bankrott (VIII.6) | Agent springt auf $w = 0$ → Konzentration der Verteilung am Nullpunkt |
| Erbschaft | Vermögen wird von $i$ (Tod) auf $j$ (Erbe) übertragen → verschiebt $f$ |
| Herdenverhalten (VI.4) | Agenten kopieren Portfolios → Korrelation in $\theta$ → schmalere $\theta$-Verteilung |

Der Kollisionsterm hat die Eigenschaft: $\int \mathcal{C}[f] \, dw = 0$ (Handel vernichtet keine Agenten, er verteilt nur um). Aber: $\int w \, \mathcal{C}[f] \, dw$ muss *nicht* null sein — eine Kreditvergabe erzeugt *Netto*-Vermögen (Geld wird geschöpft, vgl. M.1/Prop. 4.2).

### Axiometrische Eigenschaften von IV.1

> **Definition 8.2 (Zustandsraumverteilung).** *Die Funktion $f(w, \theta, \mathcal{I}, t) \geq 0$ heißt Zustandsraumverteilung der Agenten, wenn:*
> - *Normierung: $\int f \, dw \, d\theta \, d\mathcal{I} = N(t)$ (Gesamtpopulation),*
> - *Nicht-Negativität: $f \geq 0$ überall,*
> - *Divergenzform: Die linke Seite von IV.1 ist eine Divergenz → garantiert Erhaltung von $N$ wenn $\mathcal{C}$ agentenerhaltend ist.*

Die Dimension des Zustandsraums ist $(w, \theta, \mathcal{I}) \in \mathbb{R}^{1 + K + 1} = \mathbb{R}^{K+2}$, wobei $K$ die Zahl der Güterklassen ist. Für $K = 6$ (unsere sechs Klassen) ist der Zustandsraum achtdimensional — und IV.1 ist eine PDE in 8+1 Dimensionen (plus Zeit). Dies macht die *direkte* numerische Lösung für realistische $K$ impraktikabel und motiviert die Momentenmethode (IV.2–IV.4).

### Physikalische Analogie

Die Boltzmann-Gleichung hat ihren Ursprung in der kinetischen Gastheorie (Ludwig Boltzmann, 1872). In der Physik beschreibt $f(\mathbf{x}, \mathbf{v}, t)$ die Verteilung von Gasteilchen im Phasenraum (Ort, Geschwindigkeit). Die Analogie:

| Physik | Ökonoaxiomatik |
|---|---|
| Teilchen | Agent |
| Ort $\mathbf{x}$ | — (wir aggregieren über den Raum) |
| Geschwindigkeit $\mathbf{v}$ | Zustand $(w, \theta, \mathcal{I})$ |
| Kraft $\mathbf{F}$ | Mikro-Gleichungen (I.1, III.2, I.1-info) |
| Teilchen-Teilchen-Stoß | Handel, Kredit, Erbschaft ($\mathcal{C}[f]$) |
| Maxwellsche Geschwindigkeitsverteilung | Stationäre Vermögensverteilung (Pareto) |

Die Analogie ist *nicht* nur oberflächlich — die mathematische Struktur ist identisch. Das erweitert das Arsenal verfügbarer analytischer Werkzeuge: Alles, was in der kinetischen Theorie für die Boltzmann-Gleichung bewiesen wurde (H-Theorem, Chapman-Enskog-Entwicklung, Momentenmethode), kann auf die ökonomische IV.1 übertragen werden.

### Grenzfälle und Spezialformen

**Fall 1: Keine Interaktionen ($\mathcal{C}[f] = 0$).** Die Boltzmann-Gleichung wird zur *Vlasov-Gleichung*:

$$\frac{\partial f}{\partial t} + \frac{\partial}{\partial w}[\dot{w}f] + \frac{\partial}{\partial\theta}[\dot{\theta}f] + \frac{\partial}{\partial\mathcal{I}}[\dot{\mathcal{I}}f] = 0$$

Agenten entwickeln sich *unabhängig* entlang ihrer individuellen Trajektorien — kein Handel, kein Kredit, keine Erbschaft. Die Verteilung wird allein durch den Phasenraumfluss transportiert. Dies ist die *isolierte Agenten*-Approximation — nützlich für kurzfristige Dynamik, wenn die Interaktionsfrequenz niedrig ist.

**Fall 2: Stationarität + multiplikativer Prozess.** Wenn $\partial_t f = 0$ und die Vermögensdynamik multiplikativ ist ($\dot{w}/w \sim$ i.i.d.), dann konvergiert die Verteilung gegen eine **Pareto-Verteilung**:

$$f(w) \propto w^{-1-\alpha}$$

mit einem Pareto-Exponenten $\alpha > 0$, der von den Momenten des Wachstumsprozesses abhängt. Dies erklärt, warum die Vermögensverteilungen in fast allen Ländern *Potenzgesetze* im oberen Bereich aufweisen — es ist eine generische Konsequenz multiplikativer Dynamik im Gleichgewicht von IV.1.

**Fall 3: Repräsentativer Agent ($N \to \infty$, $\text{Var} \to 0$).** Wenn die Varianz der Verteilung gegen null geht, kollabiert $f$ auf eine Deltafunktion:

$$f(w, \theta, \mathcal{I}, t) \to N \cdot \delta(w - \bar{w}) \cdot \delta(\theta - \bar\theta) \cdot \delta(\mathcal{I} - \bar{\mathcal{I}})$$

Die Boltzmann-Gleichung reduziert sich auf den **Mean-Field-Limit** (IV.3) — eine ODE für den Mittelwert allein. Dies ist der *repräsentative Agent* der neoklassischen Makroökonomik: ein einziger Agent, dessen Zustand für alle steht.

> **Beobachtung 8.3 (Informationsverlust des repräsentativen Agenten).** *Der Übergang $f \to \delta(\cdot - \bar{w})$ (repräsentativer Agent) eliminiert die gesamte Information über Ungleichheit, Vermögensmobilität, Kreditrisiko-Heterogenität und Herdenverhalten. Die Standard-DSGE-Modelle operieren in diesem Grenzfall. Die Boltzmann-Gleichung IV.1 zeigt, welche Phänomene dabei verloren gehen — und unter welchen Bedingungen der repräsentative Agent eine gute Approximation ist: genau dann, wenn Var$(w)/\bar{w}^2 \ll 1$, die Verteilung unimodal ist und keine korrelierten Verhaltensweisen (Herden) vorliegen.*

### Die Momente: Vom PDE zum ODE-System

Die direkte Lösung von IV.1 in $\mathbb{R}^{K+2}$ ist für realistische Parameterzahlen numerisch nicht handhabbar. Die Alternative: Berechne die *Momente* der Verteilung — Mittelwert, Varianz, Schiefe, Wölbung — und leite Gleichungen für deren Dynamik ab.

#### Nulltes/Erstes Moment: Aggregiertes Vermögen (IV.2)

> **Gleichung IV.2 (Aggregiertes Vermögen).**
>
> $$W(t) = \int w \, f(w, \theta, \mathcal{I}, t) \, dw \, d\theta \, d\mathcal{I}$$

Das *erste Moment in $w$* der Verteilung — die Integration über den gesamten Zustandsraum gewichtet mit $w$ ergibt das aggregierte Vermögen $W(t)$.

**Konsistenzprüfung**: IV.2 *muss* die Gleichung I.2 ($\dot{W} = Y - C$) reproduzieren. Zeitableitung:

$$\dot{W} = \int w \, \frac{\partial f}{\partial t} \, dw \, d\theta \, d\mathcal{I} = \int w \left[-\frac{\partial}{\partial w}[\dot{w}f] + \mathcal{C}[f]\right] dw \, d\theta \, d\mathcal{I}$$

Partielle Integration des ersten Terms ergibt $\int \dot{w} f \, dw = \sum_i \dot{w}_i = Y - C$ (Summe aller Einkommen minus Konsum). Dies ist genau I.2 — die Konsistenz ist erbracht.

#### Erstes Moment: Mean-Field-Limit (IV.3)

> **Gleichung IV.3 (Mean-Field-Limit).**
>
> $$\frac{d\bar{w}}{dt} = \frac{Y}{N} - \frac{C}{N} + \bar{\theta}\cdot\dot{p}$$

| Term | Bedeutung |
|---|---|
| $\bar{w} = W/N$ | Mittleres Vermögen pro Kopf |
| $Y/N$ | Pro-Kopf-Einkommen |
| $C/N$ | Pro-Kopf-Konsum |
| $\bar{\theta}\cdot\dot{p}$ | Mittlere Kapitalgewinne (Durchschnittsportfolio × Preisänderung) |

IV.3 entsteht durch Division von I.2 durch $N$ plus dem mittleren Kapitalgewinne-Term. Es ist die Gleichung des *repräsentativen Agenten* — der Agent, dessen Zustand $\bar{w}$ das Makro-Aggregat repräsentiert.

**Gültigkeitsbedingungen:**
- $N \gg 1$ (viele Agenten).
- $\text{Var}(w)/\bar{w}^2 \ll 1$ (geringe relative Heterogenität).
- Keine korrelierten Verhaltensweisen (kein Herdenverhalten).

**Beziehung zu Standardmodellen:**
- **Solow-Modell**: $d\bar{w}/dt = sY/N - \delta\bar{w}$ — mit $C = (1-s)Y$ und ohne Kapitalgewinne.
- **DSGE-Modelle**: Sind präzise IV.3 plus eine Euler-Gleichung für $C/N$ — d.h. sie operieren im Mean-Field-Limit von IV.1.

#### Zweites Moment: Ungleichheitsdynamik (IV.4)

> **Gleichung IV.4 (Ungleichheitsdynamik).**
>
> $$\frac{d\text{Var}(w)}{dt} = 2\,\text{Cov}(w, \dot{w}) + \text{Var}(\dot{w})$$

Diese Gleichung ist das Herzstück der Verteilungsdynamik — sie beschreibt, wie sich die *Breite* der Vermögensverteilung (gemessen durch die Varianz) mit der Zeit ändert.

| Term | Bedeutung | Vorzeichen |
|---|---|---|
| $\text{Cov}(w, \dot{w})$ | Kovarianz von Vermögen und Vermögensänderung | $+$: Reiche werden reicher; $-$: Umverteilung |
| $\text{Var}(\dot{w})$ | Varianz der Einkommensänderungsraten | Immer $\geq 0$: heterogene Einkommen erhöhen Ungleichheit |

### Der Piketty-Mechanismus

Wenn $\text{Cov}(w, \dot{w}) > 0$ *systematisch* — d.h. wenn reichere Agenten höhere Renditen erzielen — wächst die Varianz exponentiell:

- **Reiche Agenten**: $\dot{w}_i \approx r \cdot w_i$ (Kapitalerträge dominieren, $r$ = Rendite auf Vermögen).
- **Arme Agenten**: $\dot{w}_i \approx y_i - c_i$ (Arbeitseinkommen minus Subsistenz).
- **Daraus folgt**: $\text{Cov}(w, \dot{w}) \approx r \cdot \text{Var}(w) > 0$.

Einsetzen in IV.4:

$$\frac{d\text{Var}(w)}{dt} \approx 2r \cdot \text{Var}(w) + \text{Var}(\dot{w})$$

Dies ist eine *exponentielle Wachstumsgleichung* für die Ungleichheit. Die Verdopplungszeit der Varianz ist $\ln 2 / (2r)$ — bei einer Kapitalrendite von $r = 5\%$ verdoppelt sich die Ungleichheit alle $\approx 7$ Jahre (in Abwesenheit von Gegenmaßnahmen).

> **Proposition 8.4 (Piketty-Bedingung in axiometrischer Form).** *Die Vermögensungleichheit (gemessen durch $\text{Var}(w)$) wächst genau dann exponentiell, wenn $\text{Cov}(w, \dot{w}) > 0$ — d.h. wenn die Rendite auf Vermögen positiv mit dem Vermögen korreliert. Die hinreichende Bedingung ist:*
>
> $$r > g \quad \Leftrightarrow \quad \text{Kapitalrendite} > \text{Wachstumsrate}$$
>
> *wobei $r = \langle\dot{w}/w\rangle_{\text{Kapital}}$ die durchschnittliche Rendite der reichsten Quintile und $g = \dot{Y}/Y$ die Wachstumsrate des BIP bezeichnet. Dies ist die formale Entsprechung von Pikettys Ungleichung $r > g$.*

### Die drei Regime der Ungleichheitsdynamik

Aus IV.4 ergeben sich drei qualitativ verschiedene Regime:

| Regime | Bedingung | Dynamik | Beispiel |
|---|---|---|---|
| **Divergenz** | $\text{Cov}(w, \dot{w}) > 0$ | $\text{Var}(w)$ wächst exponentiell | Unregulierter Kapitalismus ($r > g$) |
| **Stationarität** | $\text{Cov}(w, \dot{w}) = -\text{Var}(\dot{w})/2$ | $\text{Var}(w) = \text{const}$ | Gleichgewicht: Umverteilung genau kompensiert Divergenz |
| **Konvergenz** | $\text{Cov}(w, \dot{w}) < 0$ | $\text{Var}(w)$ sinkt | Progressive Besteuerung: $\tau(w)$ steigend → $\dot{w}$ fällt in $w$ |

**Stationarität:** Die Bedingung $d\text{Var}/dt = 0$ erfordert $\text{Cov}(w, \dot{w}) = -\text{Var}(\dot{w})/2$. Dies ist die *implizite* Gleichgewichtsbedingung: An die *Höhe* der Varianz werden keine Anforderungen gestellt — jedes Niveau von Ungleichheit kann stationär sein, solange die redistributiven Kräfte (progressive Steuer, Erbschaftssteuer, öffentliche Bildung) die divergierenden Kräfte ($r > g$) genau kompensieren.

### Kopplung von IV.4 an die Steuerpolitik

Der *politische* Hebel zur Beeinflussung der Ungleichheit liegt in der Steuerstruktur:

| Steuerpolitik | Wirkung auf $\text{Cov}(w, \dot{w})$ | Wirkung auf $\text{Var}(w)$ |
|---|---|---|
| Flat Tax ($\tau = \text{const}$) | Keine Änderung: $\text{Cov}$ bleibt positiv | Divergenz fortgesetzt |
| Progressive Steuer ($\partial\tau/\partial w > 0$) | $\dot{w}_{\text{reich}} \downarrow$ → $\text{Cov} \downarrow$ | Verlangsamung oder Stationarität |
| Erbschaftssteuer | Bruch der dynastischen Akkumulation | Stärkste Wirkung auf langfristige Varianz |
| Kapitalertragsteuer | $r^{\text{netto}} \downarrow$ für Reiche → $\text{Cov} \downarrow$ | Direkte Wirkung auf Piketty-Kanal |

> **Beobachtung 8.4 (Ungleichheit als endogene Variable).** *In der Ökonoaxiomatik ist die Vermögensungleichheit keine exogene Randbedingung und kein Politikparameter — sie ist eine endogene Variable mit eigener Dynamik (IV.4). Die Ungleichheit hat Rückkopplungen auf den Konsum (über U.1), die politische Stabilität (über VII.2) und die Kreditausfallwahrscheinlichkeit (über VIII.6). Ein Modell, das Ungleichheit ignoriert (d.h. den repräsentativen Agenten IV.3 anstelle der vollen Boltzmann-Gleichung IV.1 verwendet), verliert diese Rückkopplungen und kann Krisen, die aus Vermögens-Polarisierung entstehen, nicht abbilden.*

### Das Closure-Problem

Die Momentenentwicklung von IV.1 erzeugt eine Hierarchie: Die Gleichung für das $n$-te Moment enthält das $(n+1)$-te Moment. Konkret:

- IV.3 (erstes Moment $\bar{w}$) enthält $\bar{\theta}\cdot\dot{p}$ — dies hängt von der *Korrelation* zwischen $\theta$ und $p$ ab, also vom *zweiten* Moment.
- IV.4 (zweites Moment $\text{Var}(w)$) enthält $\text{Cov}(w, \dot{w})$ — dies hängt von der *Verteilung von $\dot{w}$ bedingt auf $w$* ab, also vom *dritten* Moment (Schiefe).

Die Hierarchie schließt *nicht* von selbst — dies ist das **Closure-Problem**, das offene Problem O1 der Theorie (S07 §9.1). Die Strategie: Abbruch der Hierarchie beim $n$-ten Moment und Approximation der höheren Momente unter einer Verteilungsannahme (z.B. Gauß-Closure: alle Momente $> 2$ werden als Funktionen von Mittelwert und Varianz ausgedrückt). Die Qualität der Approximation hängt davon ab, wie weit die tatsächliche Verteilung von der Gaußschen abweicht — bei fat-tailed Verteilungen (Pareto) ist der Fehler substantiell, bei annähernd normalverteilten Größen gering.

### Zusammenfassung: Die Momentenhierarchie

| Moment | Gleichung | Ökonomische Bedeutung | Standardmodell-Äquivalent |
|---|---|---|---|
| $W = \int wf$ | **IV.2** | Aggregiertes Vermögen | I.2 ($\dot{W} = Y - C$) |
| $\bar{w} = W/N$ | **IV.3** | Pro-Kopf-Vermögen (Mean-Field) | Solow, DSGE |
| $\text{Var}(w)$ | **IV.4** | Ungleichheit | Piketty ($r > g$) |
| Schiefe | (nicht geschlossen) | Asymmetrie: Oligarchen vs. Mittelschicht | Kein Standardmodell |
| Kurtosis | (nicht geschlossen) | Fat Tails: Extreme Vermögen | Risikomanagement (VaR) |

Die Standardmakroökonomik operiert im **ersten Moment** (Solow, DSGE = IV.3). Piketty hat das **zweite Moment** in den Fokus gerückt (IV.4). Die Ökonoaxiomatik gibt die *vollständige* Hierarchie — mit dem expliziten Hinweis, dass sie ab dem dritten Moment ein Closure-Schema erfordert.

---

### Wo Information abermals eingreift

Auch in diesem Kapitel durchzieht die Information $\mathcal{I}$ alle Gleichungen — hier in Form von drei spezifischen Kanälen:

| Gleichung | Informationskanal |
|---|---|
| **M.4** | $\mathcal{T}(\mathcal{I})$: Vertrauen hängt vom Informationsstand der Marktteilnehmer ab |
| **E.1** | $r_I \cdot \mathcal{I}_k$: Informationsrendite skaliert mit Informationsniveau |
| **P.4** | $c_{\mathcal{I}}(\mathcal{I})$: Informationskosten der Konversion |
| **IV.1** | $\partial_\mathcal{I}[\dot{\mathcal{I}}f]$: Die dritte Dimension des Zustandsraums |

Die Boltzmann-Gleichung IV.1 macht den Informationskanal besonders sichtbar: $\mathcal{I}$ ist eine *eigenständige Zustandsraumdimension*. Die Verteilung der Agenten über ihr Informationsniveau — wer weiß viel, wer wenig — bestimmt die Effizienz der Arbitrage (E.1), die Stabilität des Geldschöpfungsmultiplikators (M.4) und die Verteilung der Konversionsprofite (P.4).

---

### Kausale Gesamtstruktur von Kapitel 8

Zum Abschluss zeigen wir, wie alle Gleichungen dieses Kapitels in einer kausalen Kette zusammenhängen — der **Geldschöpfungs-Investitions-Verteilungs-Kreislauf**:

```
Zentralbank (Z.1): r ↓
│
├── M.3: Leverage Lev ↑ (höhere Zinsmarge)
├── M.4: m_mult ↑ (niedrigerer Zins, stabiles Vertrauen)
│
└── M.1: Geldschöpfung dM > 0
    │
    └── E.1: Niedrigerer r → Kapitalrendite relativ attraktiver → Portfolioreallokation
        │
        └── Investition ↑  →  Produktion  →  P.4: Konversionsprofit Π
                                                │
                                                └── V.9: BIP = Σ(Π + wL + rK)
                                                    │
                                                    ├── IV.3: d(w̄)/dt = Y/N - C/N (Mean-Field)
                                                    │
                                                    ├── IV.4: dVar(w)/dt — wer profitiert?
                                                    │
                                                    └── Inflation π ↑  →  Z.1: r ↑  (Rückkopplung)
```

Die Kette beginnt mit einer geldpolitischen Entscheidung (Z.1) und endet mit der Verteilungsdynamik (IV.4) — die *Frage, wer von der Geldpolitik profitiert*, wird nicht durch den Mittelwert (IV.3), sondern durch die Varianz (IV.4) beantwortet. Expansive Geldpolitik ($r \downarrow$) steigert das BIP (V.9 via Kette 5) — aber sie steigert die Ungleichheit, wenn $\text{Cov}(w, \dot{w}) > 0$, weil die Kapitalbesitzer überproportional profitieren (höhere Assetpreise → $\bar\theta\cdot\dot{p} > 0$ für die Vermögenden).

> **Proposition 8.5 (Geldpolitik und Ungleichheit).** *Expansive Geldpolitik ($r \downarrow$) erhöht das BIP (V.9) und die Vermögensungleichheit (IV.4) — unter der Bedingung, dass die Kapitalrendite positiv mit dem Vermögen korreliert ($\text{Cov}(w, \dot{w}) > 0$). Der redistributive Nettoeffekt hängt vom Verhältnis zwischen dem Einkommenskanal ($Y/N \uparrow$, wirkt auf alle) und dem Kapitalgewinnkanal ($\bar\theta\cdot\dot{p} \uparrow$, wirkt nur auf Vermögensbesitzer) ab. Im Grenzfall einer vollkommen gleichen Vermögensverteilung ($\text{Var}(w) = 0$) gibt es keinen Verteilungseffekt — die Geldpolitik wirkt neutral.*

---

*Ende von Kapitel 8. Im folgenden Kapitel behandeln wir Population, Ressourcen und die langsamen Variablen des Systems: Vertrauen, Humankapital, Emissionen und Ökologie.*

---

# Kapitel 9 — Population, Ressourcen und Strukturwandel

Die bisherigen Kapitel beschreiben ein ökonomisches System, dessen Populationsgröße, Ressourcenbasis und institutionelle Infrastruktur *gegeben* sind. Kapitel 4 bilanziert Vermögen und Güter; Kapitel 5 setzt Preise und Flüsse; Kapitel 6 und 7 modellieren Entscheidungen und Information; Kapitel 8 schließt Geld, Kredit und Verteilung. Aber all diese Gleichungen operieren auf einer Zeitskala von Quartalen bis Jahren — der Konjunkturskala. Es gibt eine langsamere Dynamik, die sich auf Zeitskalen von Dekaden bis Jahrhunderten abspielt: das Wachstum und die Schrumpfung von Bevölkerungen, die Erschöpfung und Regeneration von Ressourcen, der Aufbau und Verfall von Vertrauen, Humankapital und ökologischer Tragfähigkeit.

Dieses Kapitel führt die *ultra-langsamen Variablen* des Systems ein — neun Gleichungen, die die Bühne definieren, auf der alle schnelleren Dynamiken ablaufen.

### Nomenklatur-Anmerkung

In S07 (dem vereinigten Gleichungssystem) tragen die Populationsgleichungen die Labels V.1–V.5. In der Monographie sind V.1–V.3 bereits durch die Konsum-Gleichungen (§6.3: rationale Konsumregel, psychologische Verzerrung, soziale Kopplung) belegt. Um Verwechslungen zu vermeiden, verwenden wir für die Populationsgleichungen das Präfix **N** (*Numerus*):

| S07-Label | Monographie-Label | Gleichung |
|---|---|---|
| V.1 (Population) | **N.1** | Klassen-Populationsdynamik |
| V.2 (Population) | **N.2** | Gesamtpopulation |
| V.3 (Population) | **N.3** | Endogene Tragfähigkeit |
| V.4 (Population) | **N.4** | Ressourcendynamik |
| V.5 (Population) | **N.5** | Fertilitätsfunktion |

Die Konsum-Gleichungen V.1–V.3 aus §6.3 und die Netzwerk-Gleichungen V.6–V.8 aus §3.4 behalten ihre Labels. Die langsamen Strukturvariablen VII.1–VII.4 sind nicht von der Umbenennung betroffen.

Übersicht der neun Gleichungen dieses Kapitels:

| Gleichung | Gegenstand | Axiom | Zeitskala |
|---|---|---|---|
| **N.1** | Klassen-Populationsdynamik | A8 | Dekaden |
| **N.2** | Gesamtpopulation (Aggregat von N.1) | A8 | Dekaden |
| **N.3** | Endogene Tragfähigkeit | A8 | Dekaden–Jahrhunderte |
| **N.4** | Ressourcendynamik | A8 + A2 | Dekaden–Jahrhunderte |
| **N.5** | Fertilitätsfunktion (demogr. Übergang) | A8 + A5 | Dekaden |
| **VII.1** | Sozialkapital / Vertrauen | (Ergänzung) | Dekaden |
| **VII.2** | Humankapitalakkumulation | (Ergänzung) | Dekaden |
| **VII.3** | Emissionstrajektorie | A2-analog | Dekaden–Jahrhunderte |
| **VII.4** | Ökologische Tragfähigkeit | (Ergänzung) | Jahrhunderte |

---

## 9.1 Populationsdynamik (N.1, N.2, N.5)

### Klassen-Populationsdynamik (N.1)

In §3.3 haben wir fünf Agentenklassen eingeführt: Arbeiter $\mathcal{W}$, Unternehmer $\mathcal{U}$, Banken $\mathcal{B}$, Staat $\mathcal{G}$, Zentralbank $\mathcal{Z}$. Die Populationsdynamik jeder Klasse folgt einer logistischen Gleichung mit drei Komponenten: natürliches Wachstum, Migration und Klassenwechsel.

> **Gleichung N.1 (Klassen-Populationsdynamik).**
>
> $$\dot{N}_X = (b_X - d_X) \cdot N_X \cdot \left(1 - \frac{N}{\kappa}\right) + M_X + C_X$$

| Term | Bedeutung |
|---|---|
| $N_X$ | Population der Klasse $X \in \{\mathcal{W}, \mathcal{U}, \mathcal{B}, \mathcal{G}, \mathcal{Z}\}$ |
| $b_X$ | Geburtenrate der Klasse $X$ (endogen über N.5: $b_X = b(\bar{w}_X)$) |
| $d_X$ | Sterberate der Klasse $X$ |
| $b_X - d_X$ | Netto-Wachstumsrate |
| $N = \sum_X N_X$ | Gesamtpopulation |
| $\kappa(t)$ | Endogene Tragfähigkeit (N.3, §9.2) |
| $1 - N/\kappa$ | Logistischer Bremsfaktor: geht gegen null, wenn $N \to \kappa$ |
| $M_X$ | Netto-Migration in Klasse $X$ (von außen) |
| $C_X$ | Netto-Klassenwechsel in Klasse $X$ (z.B. $\mathcal{W} \to \mathcal{U}$: Arbeiter wird Unternehmer) |

### Axiomatische Herleitung

N.1 folgt aus **A8** (Populationsrückkopplung): „Geburts- und Sterberaten sind Funktionen des Pro-Kopf-Vermögens; Ressourcen sind endlich." Die logistische Struktur — die Wachstumsrate geht gegen null, wenn die Population die Tragfähigkeit erreicht — ist die einfachste Realisierung endlicher Ressourcen. Sie ist keine spezifische Funktionalform im engeren Sinne, sondern die *minimale* Struktur, die A8 erfüllt:

- $\dot{N}_X > 0$ für $N \ll \kappa$ (bei reichlich Ressourcen wächst die Population).
- $\dot{N}_X \to 0$ für $N \to \kappa$ (bei Erschöpfung der Ressourcen stagniert sie).
- $\dot{N}_X < 0$ für $N > \kappa$ (bei Überschreitung der Tragfähigkeit schrumpft sie).

### Die Konsistenzbedingungen

Der Klassenwechselterm $C_X$ beschreibt, wie Agenten zwischen Klassen wechseln: Ein Arbeiter $\mathcal{W}$, der ein Unternehmen gründet (über L.5, §6.8), wechselt in die Klasse $\mathcal{U}$. Ein Unternehmer, der bankrott geht (VIII.6, Kapitel 10), fällt in die Klasse $\mathcal{W}$ zurück. Der Klassenwechsel muss zwei Konsistenzbedingungen erfüllen:

> **N.1c (Konsistenzbedingungen).**
>
> $$\sum_X C_X = 0 \qquad \text{(Klassenwechsel erzeugt/vernichtet keine Agenten)}$$
>
> $$\sum_X M_X = M_{\text{netto}} \qquad \text{(Gesamtmigration konsistent)}$$

Die erste Bedingung ist eine *Buchhaltungsidentität*: Jeder Agent, der Klasse $X$ verlässt, muss in eine andere Klasse $Y$ eintreten. Die Übergänge bilden eine Matrix:

| Von $\backslash$ Nach | $\mathcal{W}$ | $\mathcal{U}$ | $\mathcal{B}$ | $\mathcal{G}$ | $\mathcal{Z}$ |
|---|---|---|---|---|---|
| $\mathcal{W}$ | — | Gründung (L.5) | Karriere | Beamtung | — |
| $\mathcal{U}$ | Bankrott (VIII.6) | — | Fusion | — | — |
| $\mathcal{B}$ | Bankausfall (VIII.6) | — | — | Verstaatlichung | — |
| $\mathcal{G}$ | Entlassung | Privatisierung | — | — | — |
| $\mathcal{Z}$ | — | — | — | — | — |

Die meisten Übergänge sind selten (Zeitskala: Jahre bis Dekaden). Der häufigste ist $\mathcal{W} \to \mathcal{U}$ (Gründung) und $\mathcal{U} \to \mathcal{W}$ (Bankrott) — ein Kreislauf, der von L.5 (Gründungsneigung, §6.8) und VIII.6 (Bankrott, Kapitel 10) angetrieben wird.

### Axiometrische Eigenschaften

1. **Populationserhaltung**: Summation von N.1 über alle $X$ ergibt N.2 (Gesamtpopulation) — die Klassenwechsel-Terme heben sich auf ($\sum_X C_X = 0$).
2. **Nicht-Negativität**: $N_X \geq 0$ für alle $X$ und $t$ (ökonomische Bedingung).
3. **Logistische Begrenzung**: Für $N \to \kappa$ verschwindet der natürliche Wachstumsterm.
4. **Positivität der Klassenwechsel-Matrix**: Alle Übergangsraten $\geq 0$; die Diagonale ist null (kein Wechsel in dieselbe Klasse).

### Gesamtpopulation (N.2)

N.2 ist kein unabhängiges Gesetz — sie folgt durch Summation von N.1 über alle Klassen:

> **Gleichung N.2 (Gesamtpopulation).**
>
> $$\dot{N} = r_N \cdot N \cdot \left(1 - \frac{N}{\kappa}\right) + M_{\text{netto}}$$

| Term | Bedeutung |
|---|---|
| $N = \sum_X N_X$ | Gesamtpopulation |
| $r_N = \sum_X (b_X - d_X) N_X / N$ | Gewichtete Netto-Wachstumsrate |
| $\kappa(t)$ | Endogene Tragfähigkeit (N.3) |
| $M_{\text{netto}} = \sum_X M_X$ | Netto-Migration |

N.2 ist die direkte Umsetzung von Axiom A8 in der Monographie (§2.8): $\dot{N} = r_N N(1 - N/\kappa) + M$. Die Klassen-Auflösung N.1 liefert die *Mikrostruktur* hinter der aggregierten Gleichung — welche Klasse wächst, welche schrumpft.

### Grenzfälle von N.2

**Fall 1: Geschlossene Volkswirtschaft ($M_{\text{netto}} = 0$).** Reine logistische Dynamik:

$$\dot{N} = r_N \cdot N \cdot (1 - N/\kappa)$$

Der stationäre Zustand ist $N^* = \kappa$ — die Population füllt die Tragfähigkeit vollständig aus. Die Konvergenz ist sigmoidal: exponentielles Wachstum für $N \ll \kappa$, Sättigung für $N \to \kappa$.

**Fall 2: Konstante Tragfähigkeit ($\kappa = \kappa_0 = \text{const}$).** Die klassische Malthus-Verhulst-Gleichung. Die Dynamik ist vollständig bestimmt: $N(t) = \kappa_0 / (1 + (\kappa_0/N_0 - 1)e^{-r_N t})$. Dies war eine akzeptable Approximation für vorindustrielle Gesellschaften mit konstantem Technologieniveau.

**Fall 3: Plötzlicher Tragfähigkeits-Einbruch ($\kappa$ fällt unter $N$).** Wenn durch Ressourcenerschöpfung (N.4), Klimakatastrophe (VII.3) oder Technologieverlust die Tragfähigkeit $\kappa$ *unter* die aktuelle Population $N$ fällt, wird $1 - N/\kappa < 0$ — das natürliche Wachstum kehrt sich um. Die Population schrumpft, bis $N = \kappa$ wieder erreicht ist. Dies ist der Mechanismus des *ökologischen Kollapses* (Easter Island, Mayazivilisation, Dust Bowl).

> **Proposition 9.1 (Populationskollaps).** *Wenn die Tragfähigkeit $\kappa(t)$ unter die aktuelle Population $N(t)$ fällt ($\kappa < N$), dann ist $\dot{N} < 0$ (bei $M_{\text{netto}} = 0$). Die Relaxationszeit zum neuen Gleichgewicht $N^* = \kappa$ ist $\tau_{\text{relax}} \approx 1/r_N$ — eine demografische Zeitskala (typisch 20–50 Jahre). Während dieser Transitionsphase übersteigt die Sterberate die Geburtenrate: $d > b$.*

### Fertilitätsfunktion und der demografische Übergang (N.5)

In N.1 und N.2 erscheint die Geburtenrate $b_X$ — aber woher kommt sie? In der neoklassischen Ökonomik ist $b$ exogen (gegeben). In der Ökonoaxiomatik ist sie *endogen*: Die Geburtenrate hängt vom Pro-Kopf-Vermögen ab — reiche Gesellschaften haben weniger Kinder. Dies ist der *demografische Übergang*, eines der am besten dokumentierten empirischen Gesetze der Ökonomik.

> **Gleichung N.5 (Fertilitätsfunktion).**
>
> $$b(\bar{w}) = b_{\max} \cdot \frac{w_{\text{sub}}^2}{\bar{w}^2 + w_{\text{sub}}^2}$$

| Term | Bedeutung |
|---|---|
| $b(\bar{w})$ | Geburtenrate als Funktion des Durchschnittsvermögens |
| $b_{\max}$ | Maximale Geburtenrate (typisch $\approx 0{,}05$ yr$^{-1}$) |
| $\bar{w}$ | Durchschnittliches Pro-Kopf-Vermögen (aus IV.3: $\bar{w} = W/N$) |
| $w_{\text{sub}}$ | Subsistenz-Vermögensschwelle (länderspezifisch) |

### Axiometrische Eigenschaften von N.5

Die spezifische Funktionalform (Lorentz-Kurve $w_{\text{sub}}^2/(\bar{w}^2 + w_{\text{sub}}^2)$) ist eine *Modellierungswahl*. Die axiometrischen Eigenschaften, die *jede* Realisierung von N.5 erfüllen muss:

1. **Monoton fallend**: $\partial b / \partial \bar{w} < 0$ — reichere Gesellschaften haben weniger Kinder. Dies ist der demografische Übergang.
2. **Obere Schranke**: $b \leq b_{\max}$ — die Geburtenrate ist biologisch begrenzt.
3. **Subsistenzmaximum**: $b(\bar{w} \to 0) \to b_{\max}$ — bei extremer Armut maximale Fertilität (Überlebensstrategie).
4. **Sättigung**: $b(\bar{w} \to \infty) \to 0$ — reiche Gesellschaften konvergieren gegen Nullwachstum.
5. **Halbwertspunkt**: $b(w_{\text{sub}}) = b_{\max}/2$ — der Parameter $w_{\text{sub}}$ definiert, bei welchem Vermögensniveau die Geburtenrate halbiert ist.

### Der demografische Übergang als endogenes Phänomen

N.5 koppelt die Demografie an die Ökonomie über den Vermögenskanal:

$$\text{I.1} \to \bar{w} \to \text{N.5: } b(\bar{w}) \to \text{N.1: } \dot{N}_X \to N \to \text{IV.1: } f(w, \ldots)$$

Wirtschaftswachstum (steigendes $\bar{w}$) senkt die Geburtenrate → Bevölkerungswachstum verlangsamt sich → Pro-Kopf-Vermögen steigt weiter → Geburtenrate sinkt weiter. Dies ist ein *positiver Rückkopplungskreis*, der sich selbst stabilisiert: Im Gleichgewicht wächst die Bevölkerung nicht mehr, das Pro-Kopf-Vermögen ist stationär und die Geburtenrate deckt gerade die Sterberate.

> **Beobachtung 9.1 (Endogener demografischer Übergang).** *N.5 erklärt den demografischen Übergang — den historischen Rückgang der Geburtenraten bei steigendem Wohlstand — als endogenes Phänomen, nicht als exogenen Parameter. Die vier Phasen des demografischen Übergangs ergeben sich als transiente Dynamik:*
>
> | Phase | $\bar{w}$ relativ zu $w_{\text{sub}}$ | $b$ | $d$ | $\dot{N}$ |
> |---|---|---|---|---|
> | I (Prä-Transition) | $\bar{w} \ll w_{\text{sub}}$ | Hoch ($\approx b_{\max}$) | Hoch | $\approx 0$ |
> | II (Frühe Transition) | $\bar{w}$ steigt, aber $< w_{\text{sub}}$ | Hoch | Fällt (Medizin) | $> 0$ (Explosion) |
> | III (Späte Transition) | $\bar{w} \approx w_{\text{sub}}$ | Fällt | Niedrig | Verlangsamt sich |
> | IV (Post-Transition) | $\bar{w} \gg w_{\text{sub}}$ | Niedrig ($\approx 0$) | Niedrig | $\approx 0$ oder $< 0$ |

### Kopplung der Populationsgleichungen an das Gesamtsystem

| Gleichung | Kopplungskanal |
|---|---|
| **N.3** (§9.2) | $\kappa(t)$: Die Tragfähigkeit begrenzt das Wachstum |
| **N.5** → **N.1** | $b_X = b(\bar{w}_X)$: Geburtenrate hängt vom Klassenvermögen ab |
| **IV.1** (§8.5) | $\int f \, dw \, d\theta \, d\mathcal{I} = N$: Normierung der Verteilung |
| **IV.3** (§8.5) | $\bar{w} = W/N$: Pro-Kopf-Vermögen hängt von $N$ ab |
| **L.5** (§6.8) | Gründungsneigung treibt $C_{\mathcal{W} \to \mathcal{U}}$ |
| **VIII.6** (Kap. 10) | Bankrott treibt $C_{\mathcal{U} \to \mathcal{W}}$ |
| **V.9** (§8.4) | BIP pro Kopf $Y/N$ sinkt bei wachsender Population (ceteris paribus) |

---

## 9.2 Tragfähigkeit und Ressourcen (N.3, N.4)

### Endogene Tragfähigkeit (N.3)

Die Tragfähigkeit $\kappa$ — die maximale Population, die eine Volkswirtschaft ernähren kann — ist in der Malthus-Gleichung eine Konstante. In der Ökonoaxiomatik ist sie *endogen*: Sie steigt mit dem Technologieniveau, fällt mit der Ressourcenerschöpfung und wird durch Emissionen degradiert.

> **Gleichung N.3 (Endogene Tragfähigkeit).**
>
> $$\kappa(t) = \kappa_0 \cdot \frac{A(t)}{A_0} \cdot \frac{R(t)}{R_0} \cdot \frac{1}{1 + \alpha_E \cdot E(t)/E_0}$$

| Term | Bedeutung |
|---|---|
| $\kappa(t)$ | Endogene Tragfähigkeit zur Zeit $t$ |
| $\kappa_0$ | Basis-Tragfähigkeit (typisch $\sim 10^{10}$ Personen global) |
| $A(t)$ | Technologieniveau (wächst gemäß VI.6, §6.9) |
| $A_0$ | Referenz-Technologieniveau |
| $R(t)$ | Aggregierter Ressourcenbestand (N.4) |
| $R_0$ | Anfangs-Ressourcenbestand |
| $\alpha_E$ | Emissionssensitivität |
| $E(t)$ | Kumulierte Emissionen (VII.3) |
| $E_0$ | Referenz-Emissionsniveau |

### Axiomatische Herleitung

N.3 folgt aus **A8** („Ressourcen endlich"): Die Population kann nicht unbeschränkt wachsen — die Tragfähigkeit setzt die Obergrenze. Die spezifische multiplikative Form ist eine *Modellierungswahl*, aber die axiometrischen Eigenschaften sind fest:

1. **Monoton steigend in $A$**: $\partial\kappa/\partial A > 0$ — bessere Technologie ermöglicht mehr Menschen (Grüne Revolution, Düngemittel, Intensivlandwirtschaft).
2. **Monoton steigend in $R$**: $\partial\kappa/\partial R > 0$ — mehr Ressourcen (Ackerland, Wasser, Energie) erhöhen die Tragfähigkeit.
3. **Monoton fallend in $E$**: $\partial\kappa/\partial E < 0$ — kumulierte Emissionen degradieren die Tragfähigkeit (Klimawandel, Bodenerosion, Wasserverschmutzung).
4. **Positivität**: $\kappa > 0$ solange $A > 0$ und $R > 0$.
5. **Grenzfälle**:
   - $R \to 0$: $\kappa \to 0$ — Zivilisationskollaps durch Ressourcenerschöpfung.
   - $E \to \infty$: $\kappa \to 0$ — Umweltzerstörung macht den Planeten unbewohnbar.
   - $A \to \infty$ bei $R > 0$, $E < \infty$: $\kappa \to \infty$ — rein technologische Utopie (nur theoretisch).

### Die drei Faktoren und ihre Zeitskalen

| Faktor | Variable | Zeitskala | Treiber |
|---|---|---|---|
| Technologie | $A(t)/A_0$ | Dekaden | VI.6: $\dot{A} = \theta_A A - \delta_A A + s_A Y$ |
| Ressourcen | $R(t)/R_0$ | Dekaden–Jahrhunderte | N.4: Extraktion, Regeneration, Degradation |
| Emissionen | $1/(1 + \alpha_E E/E_0)$ | Jahrhunderte | VII.3: $\dot{E} = e_E Y_{\text{fossil}} - a_E N - \delta_E E$ |

Die multiplikative Struktur impliziert, dass ein *einziger* Faktor, der gegen null geht, die gesamte Tragfähigkeit zerstört — auch wenn die anderen Faktoren hoch sind. Eine Gesellschaft mit exzellentem Technologieniveau ($A/A_0 \gg 1$) aber erschöpften Ressourcen ($R \to 0$) kollabiert ebenso wie eine ressourcenreiche Gesellschaft ($R/R_0 \approx 1$) mit zerstörtem Klima ($E \gg E_0$).

> **Proposition 9.2 (Tragfähigkeitsfalle).** *Die multiplikative Struktur von N.3 impliziert, dass die Tragfähigkeit durch den schwächsten Faktor bestimmt wird (Liebigs Minimumgesetz). Eine Volkswirtschaft, die Technologie maximiert ($A \to \infty$) aber Ressourcen und Emissionen ignoriert, kann den Tragfähigkeitsverlust durch $R \to 0$ oder $E \to \infty$ nicht kompensieren. Nachhaltige Entwicklung erfordert, dass alle drei Faktoren gleichzeitig über kritischen Schwellen bleiben.*

### Ressourcendynamik (N.4)

Die Ressourcen $R(t)$ in N.3 sind nicht statisch — sie werden verbraucht und (bei erneuerbaren Ressourcen) regeneriert.

> **Gleichung N.4 (Ressourcendynamik).**
>
> $$\dot{R}_k = r_R \cdot R_k - e_R \cdot N - \delta_R \cdot R_k$$

| Term | Bedeutung |
|---|---|
| $R_k$ | Bestand der Ressource $k$ |
| $r_R$ | Regenerationsrate ($r_R > 0$ für erneuerbare; $r_R = 0$ für fossile Ressourcen) |
| $e_R$ | Pro-Kopf-Extraktionsrate |
| $N$ | Gesamtpopulation (aus N.2) |
| $\delta_R$ | Natürliche Degradationsrate |

### Axiomatische Herleitung

N.4 folgt aus der *Erhaltungslogik* (analog zu A2): Bestandsänderung = Quellen minus Senken. Die drei Terme:

1. **Regeneration** ($r_R R_k$): Die Ressource wächst proportional zum bestehenden Bestand — z.B. Fischpopulationen, Wälder, Grundwasser. Für *fossile* Ressourcen (Öl, Kohle, Gas) ist $r_R = 0$: keine Regeneration auf ökonomisch relevanten Zeitskalen.
2. **Extraktion** ($-e_R N$): Der Pro-Kopf-Verbrauch mal der Gesamtpopulation — die *anthropogene Senke*. Je größer die Population (N.2) und je höher der Pro-Kopf-Verbrauch, desto schneller schwindet die Ressource.
3. **Degradation** ($-\delta_R R_k$): Natürlicher Verfall — Erosion von Ackerland, Versalzung von Küstengrundwasser, radioaktiver Zerfall von Uran. Wirkt auch ohne menschliche Extraktion.

### Die zwei Regime: Erneuerbar vs. Fossil

**Erneuerbare Ressourcen ($r_R > 0$).** Im stationären Zustand ($\dot{R}_k = 0$):

$$R_k^* = \frac{e_R \cdot N}{r_R - \delta_R} \qquad \text{(existiert nur für } r_R > \delta_R\text{)}$$

Die Ressource stabilisiert sich auf einem Niveau, das von der Population abhängt. Steigt $N$ (über N.2), sinkt $R_k^*$ — bis bei hinreichend großem $N$ die Regenerationsrate nicht mehr ausreicht und die Ressource kollabiert. Dies ist die *Tragödie der Allmende* (Tragedy of the Commons): Individuelle Rationalität ($e_R > 0$) führt zu kollektivem Zusammenbruch ($R \to 0$).

**Fossile Ressourcen ($r_R = 0$).** Monotoner Abbau:

$$\dot{R}_k = -(e_R N + \delta_R R_k) < 0 \quad \text{für } R_k > 0$$

Fossile Ressourcen gehen *unvermeidlich* gegen null — die einzige Frage ist, wie schnell. Die Erschöpfungszeit hängt von $N$ und $e_R$ ab. Bei konstantem $N$ und $e_R$:

$$R_k(t) = R_k(0) \cdot e^{-\delta_R t} - \frac{e_R N}{\delta_R}(1 - e^{-\delta_R t})$$

> **Beobachtung 9.2 (Fossile Endlichkeit).** *Für fossile Ressourcen ($r_R = 0$) gibt es keinen stationären Zustand mit $R > 0$. Die einzige Langfrist-Lösung ist $R = 0$ — vollständige Erschöpfung. Die N.3-Tragfähigkeit fällt dann auf den Wert, der allein durch erneuerbare Ressourcen gestützt wird. N.4 formalisiert das „Peak Oil"-Argument: Nicht die Frage ob, sondern wann.*

### Physische Constraints

Aus der physikalischen Realität folgt eine harte Nebenbedingung:

$$R_k(t) \geq 0 \quad \forall \, k, t \tag{G.1}$$

Negative Ressourcen existieren nicht. Wenn $R_k$ die Null erreicht, schaltet die Extraktion ab ($e_R \to 0$ für dieses $k$) — ein diskontinuierlicher Übergang, der die Kopplung an die Regimewechsel-Gleichungen (VIII.4, Kapitel 10) herstellt.

### Kopplung von N.3 und N.4

| Gleichung | Kopplungskanal |
|---|---|
| **N.2** | $N$: Population bestimmt Extraktionsdruck in N.4 und wird durch $\kappa$ in N.2 begrenzt |
| **VII.3** (§9.4) | $E(t)$: Emissionen drücken die Tragfähigkeit in N.3 |
| **VI.6** (§6.9) | $A(t)$: Technologieniveau treibt die Tragfähigkeit in N.3 nach oben |
| **III.3** (§6.6) | Ressourcen als Produktionsinputs: $R$ limitiert Produktion |
| **VIII.4** (Kap. 10) | Bei $R \to 0$ oder $E > E_{\text{krit}}$: Regimewechsel |
| **V.9** (§8.4) | BIP hängt von verfügbaren Ressourcen ab (über III.3) |

---

## 9.3 Langsame Variablen I: Vertrauen und Humankapital (VII.1, VII.2)

Die Populationsgleichungen N.1–N.5 und die Tragfähigkeit N.3 bilden die *biologische* Hülle des Systems. Innerhalb dieser Hülle gibt es vier *institutionelle* Variablen, die sich auf noch langsameren Zeitskalen bewegen: Vertrauen ($\mathcal{T}$), Humankapital ($H$), Emissionen ($E$) und ökologische Tragfähigkeit ($\kappa_{\text{eco}}$). Die Gruppe VII ist die langsamste Dynamik des gesamten Systems — sie dreht sich auf der Zeitskala von Dekaden bis Jahrhunderten.

### Sozialkapital und Vertrauen (VII.1)

In Kapitel 8 (§8.1) haben wir das Vertrauen $\mathcal{T}$ in der Gleichung M.4 als *gegebene Variable* verwendet: Der Geldschöpfungsmultiplikator $m_{\text{mult}} = m_0 \cdot \mathcal{T} \cdot (1 - \alpha_r r)$ kollabiert, wenn $\mathcal{T} \to 0$. Aber woher kommt $\mathcal{T}$? Wie baut es sich auf, wie zerfällt es?

> **Gleichung VII.1 (Sozialkapitaldynamik).**
>
> $$\dot{\mathcal{T}} = \gamma_{\mathcal{T}} \cdot N \cdot \left(1 - \frac{\mathcal{T}}{\mathcal{T}_{\max}}\right) - \delta_{\mathcal{T}} \cdot \mathcal{T}$$

| Term | Bedeutung |
|---|---|
| $\mathcal{T}$ | Aggregiertes Vertrauensniveau / Sozialkapital |
| $\gamma_{\mathcal{T}}$ | Vertrauensaufbaurate (Intensität sozialer Interaktion) |
| $N$ | Gesamtpopulation |
| $\mathcal{T}_{\max}$ | Maximales Vertrauensniveau (Sättigungsgrenze) |
| $\delta_{\mathcal{T}}$ | Sozialkapitalzerfall (typisch $\sim 0{,}01$ yr$^{-1}$) |

### Axiomatische Einordnung

VII.1 ist *nicht* direkt aus den zehn Axiomen A1–A10 ableitbar — sie ist eine *Ergänzung* des Gleichungssystems, motiviert durch die empirische Bedeutung des Sozialkapitals (Putnam 1993, Knack & Keefer 1997, Zak & Knack 2001). Die logistische Struktur folgt aus einer *Analogie* zu A8: Vertrauen wächst durch soziale Interaktion (analog zur biologischen Reproduktion), hat eine Sättigungsgrenze (analog zur Tragfähigkeit) und zerfällt ohne Pflege (analog zur Sterberate).

### Axiometrische Eigenschaften

1. **Logistische Begrenzung**: $\mathcal{T} \leq \mathcal{T}_{\max}$ — Vertrauen kann nicht unbeschränkt wachsen.
2. **Aufbau proportional zu $N$**: Größere Populationen können *potentiell* mehr Vertrauen aufbauen (mehr Interaktionsmöglichkeiten).
3. **Natürlicher Zerfall**: Ohne soziale Interaktion zerfällt Vertrauen exponentiell mit Rate $\delta_{\mathcal{T}}$ — Vertrauen ist keine Bestandsgröße, die sich selbst erhält.
4. **Stationärer Zustand**:

$$\mathcal{T}^* = \mathcal{T}_{\max} \cdot \left(1 - \frac{\delta_{\mathcal{T}}}{\gamma_{\mathcal{T}} \cdot N}\right) \qquad \text{(für } \gamma_{\mathcal{T}} N > \delta_{\mathcal{T}}\text{)}$$

5. **Kritische Population**: Wenn $N < \delta_{\mathcal{T}} / \gamma_{\mathcal{T}}$, ist der Aufbauterm zu schwach, um den Zerfall zu kompensieren — Vertrauen geht gegen null. Dies impliziert eine *Mindestgröße* für Gesellschaften, die stabiles Sozialkapital aufbauen können.

### Grenzfälle

**Fall 1: Stabiles Gleichgewicht ($\gamma_{\mathcal{T}} N \gg \delta_{\mathcal{T}}$).** Das Vertrauen stabilisiert sich nahe $\mathcal{T}_{\max}$:

$$\mathcal{T}^* \approx \mathcal{T}_{\max} \left(1 - \frac{\delta_{\mathcal{T}}}{\gamma_{\mathcal{T}} N}\right) \approx \mathcal{T}_{\max}$$

In großen, sozial interagierenden Bevölkerungen konvergiert das Vertrauen gegen sein Maximum. Dies ist der Idealzustand — aber er ist *fragil*.

**Fall 2: Vertrauensschock (exogener Einbruch).** Nach einer Finanzkrise, einem politischen Skandal oder einem Krieg fällt $\mathcal{T}$ sprunghaft (modelliert durch VIII.1, Kapitel 10). Die *Wiederaufbauzeit* folgt aus der Relaxationsdynamik:

$$\tau_{\text{Recovery}} \approx \frac{1}{\gamma_{\mathcal{T}} N + \delta_{\mathcal{T}}}$$

Bei $\delta_{\mathcal{T}} \sim 0{,}01$ yr$^{-1}$ und moderatem $\gamma_{\mathcal{T}} N$ dauert die Erholung Dekaden — weit langsamer als die Konjunkturerholung. Dies erklärt, warum Finanzkrisen langfristige Wachstumseinbußen erzeugen, die über den Konjunkturzyklus hinausgehen: Das BIP erholt sich (über V.9), aber das Vertrauen nicht.

**Fall 3: Gesellschaftlicher Zerfall ($\gamma_{\mathcal{T}} N < \delta_{\mathcal{T}}$).** Zu wenige soziale Interaktionen — z.B. in geschrumpften, fragmentierten oder stark polarisierten Gesellschaften. Vertrauen erodiert: $\mathcal{T} \to 0$. Über M.4 kollabiert der Geldschöpfungsmultiplikator → Kreditklemme → ökonomische Kontraktion → weitere Fragmentierung. Ein Teufelskreis.

> **Proposition 9.3 (Vertrauen als gesellschaftliches Minimum).** *Das Vertrauensniveau $\mathcal{T}$ stellt eine notwendige Bedingung für das Funktionieren des Geldsystems dar: $\mathcal{T} > 0$ ist erforderlich für $m_{\text{mult}} > 0$ (M.4). Eine Gesellschaft, die unter die kritische Populationsschwelle $N < \delta_{\mathcal{T}}/\gamma_{\mathcal{T}}$ fällt, verliert die Fähigkeit zur Kreditschöpfung — unabhängig von der Geldpolitik der Zentralbank.*

### Kopplung von VII.1 an das Gesamtsystem

| Gleichung | Kopplungskanal |
|---|---|
| **M.4** (§8.1) | $m_{\text{mult}} = m_0 \cdot \mathcal{T} \cdot (1 - \alpha_r r)$: Geldschöpfungsmultiplikator |
| **M.3** (§8.1) | Bankenstress senkt $\mathcal{T}$ (exogener Schock auf VII.1) |
| **II.4** (§5.5) | Transaktionskosten sinken mit $\mathcal{T}$: $\sigma_m \propto \mathcal{T}$ |
| **VII.4** (§9.4) | $\mathcal{T}$ geht in die ökologische Tragfähigkeit ein |
| **VIII.4** (Kap. 10) | Vertrauensverlust kann Regimewechsel auslösen |
| **N.2** | $N$ treibt den Aufbauterm in VII.1 |

### Humankapitalakkumulation (VII.2)

Das Humankapital $H_i$ — die Summe aus Bildung, Berufserfahrung, Gesundheit und kognitiven Fähigkeiten eines Agenten — ist die zweite langsame Variable. Es akkumuliert langsam (Bildung: 15–25 Jahre; Berufserfahrung: Dekaden) und erodiert ohne Investition (Wissensobsoleszenz, Qualifikationsverfall).

> **Gleichung VII.2 (Humankapitalakkumulation).**
>
> $$\dot{H}_i = e_H \cdot y_i - \delta_H \cdot H_i$$

| Term | Bedeutung |
|---|---|
| $H_i$ | Humankapital des Agenten $i$ |
| $e_H$ | Bildungsinvestitionsanteil (dimensionslos, typisch 0,05–0,15) |
| $y_i$ | Einkommen des Agenten $i$ |
| $\delta_H$ | Humankapital-Depreziation (Wissenszerfall, Obsoleszenz) |

### Axiomatische Einordnung

VII.2 ist — wie VII.1 — eine *Ergänzung* des Axiomensystems, inspiriert durch die Humankapitaltheorie (Mincer 1958, Becker 1964, Lucas 1988). Die Struktur ist die eines *Investitions-Abschreibungs-Prozesses*: Investition ($e_H y_i$) proportional zum Einkommen, Abschreibung ($\delta_H H_i$) proportional zum Bestand. Dies ist dieselbe Struktur wie die Sachkapitalakkumulation ($\dot{K} = sY - \delta K$ in III.3) — aber auf der personalen Ebene, nicht der Firmenebene.

### Axiometrische Eigenschaften

1. **Investition proportional zum Einkommen**: $\partial\dot{H}/\partial y_i > 0$ — reichere Agenten können mehr in Bildung investieren.
2. **Natürlicher Zerfall**: Ohne Einkommen ($y_i = 0$) erodiert das Humankapital exponentiell: $H_i(t) = H_i(0) \cdot e^{-\delta_H t}$.
3. **Stationärer Zustand**: $H_i^* = e_H \cdot y_i / \delta_H$ — das Humankapital stabilisiert sich proportional zum Einkommen.
4. **Ungleichheits-Reproduktion**: Da $H_i^* \propto y_i$ und $y_i$ positiv mit $w_i$ korreliert, reproduziert VII.2 die Vermögensungleichheit *auf der Humankapitalebene*: Reiche Agenten haben höheres $H$, das höheres $y$ erzeugt (über III.3), das höheres $H$ finanziert.

### Der Humankapital-Ungleichheits-Kreislauf

VII.2 erzeugt einen selbstverstärkenden Kreislauf, der die Piketty-Dynamik (IV.4) auf das Humankapital überträgt:

$$\text{Hohes } y_i \xrightarrow{\text{VII.2}} \text{Hohes } H_i \xrightarrow{\text{III.3}} \text{Hohe Produktivität} \xrightarrow{\text{P.4}} \text{Hohes } y_i$$

Im Aggregat:

$$H^* = e_H \cdot Y / (N \cdot \delta_H)$$

Das durchschnittliche Humankapital steigt mit dem Pro-Kopf-BIP und fällt mit der Depreziation. Eine Gesellschaft, deren BIP stagniert (Rezession, Stagnation), verliert Humankapital — nicht sofort (die Zeitskala ist $1/\delta_H$, typisch 10–30 Jahre), aber stetig. Dies ist der Mechanismus der *Brain-Drain-Spirale*: Ökonomische Stagnation → Humankapitalerosion → Produktivitätsverlust → weitere Stagnation.

> **Beobachtung 9.3 (Humankapitalfalle).** *VII.2 impliziert eine Bifurkation: Gesellschaften mit $e_H y / \delta_H > H^{\text{krit}}$ (einem kritischen Schwellenwert für funktionsfähige Arbeitskräfte) akkumulieren Humankapital und wachsen; Gesellschaften mit $e_H y / \delta_H < H^{\text{krit}}$ erodieren und stagnieren. Der Übergang zwischen beiden Regimen ist die „Middle-Income Trap" — die Beobachtung, dass viele Schwellenländer an einer Wohlstandsschwelle stagnieren, über die sie nicht hinauskommen.*

---

## 9.4 Langsame Variablen II: Emissionen und Ökologie (VII.3, VII.4)

### Emissionstrajektorie (VII.3)

Emissionen sind der *physikalische* Kanal, durch den ökonomische Aktivität die natürliche Umwelt verändert. In der Ökonoaxiomatik sind sie eine kumulierte Zustandsvariable — nicht der jährliche Ausstoß (Flussgröße), sondern der *in der Atmosphäre akkumulierte Bestand* (Bestandsgröße).

> **Gleichung VII.3 (Emissionstrajektorie).**
>
> $$\dot{E} = e_E \cdot Y_{\text{fossil}} - a_E \cdot N - \delta_E \cdot E$$

| Term | Bedeutung |
|---|---|
| $E$ | Kumulierte Emissionen (z.B. CO$_2$-Äquivalent in der Atmosphäre) |
| $e_E$ | Emissionsintensität der fossilen Produktion |
| $Y_{\text{fossil}}$ | Fossile Produktionsleistung (Anteil der Gesamtproduktion, der auf fossiler Energie basiert) |
| $a_E$ | Pro-Kopf-Absorptionskapazität der natürlichen Senken (Ozeane, Wälder, Böden) |
| $N$ | Gesamtpopulation |
| $\delta_E$ | Natürlicher Emissionszerfall (sehr langsam für CO$_2$: $\delta_E \approx 0{,}003$ yr$^{-1}$) |

### Axiomatische Herleitung

VII.3 folgt der *Erhaltungslogik* analog zu A2 (Gütererhaltung): Bestandsänderung = Quelle minus Senken. Die Quelle ist die fossile Produktion; die Senken sind die natürliche Absorption ($a_E N$ — proportional zur Population als Proxy für die bewirtschaftete natürliche Senkenfläche) und der natürliche Zerfall ($\delta_E E$).

### Axiometrische Eigenschaften

1. **Quelle = fossile Produktion**: $\partial\dot{E}/\partial Y_{\text{fossil}} > 0$ — mehr fossile Wirtschaftsaktivität erzeugt mehr Emissionen.
2. **Senken sind begrenzt**: $a_E N + \delta_E E$ wächst langsamer als $e_E Y_{\text{fossil}}$ bei hohem BIP → Emissionen akkumulieren.
3. **Netto-Null**: Der Zustand $\dot{E} = 0$ erfordert $e_E Y_{\text{fossil}} = a_E N + \delta_E E$ — die fossile Produktion muss auf ein Niveau sinken, das die natürlichen Senken decken.
4. **Irreversibilität** (auf ökonomischen Zeitskalen): $\delta_E$ ist für CO$_2$ so klein ($\sim 0{,}003$ yr$^{-1}$, Halbwertszeit $\sim 230$ Jahre), dass einmal emittiertes CO$_2$ *Jahrhunderte* in der Atmosphäre verbleibt.

### Drei Regime

| Regime | Bedingung | Konsequenz |
|---|---|---|
| **Akkumulation** | $e_E Y_{\text{fossil}} > a_E N + \delta_E E$ | Emissionen steigen → $\kappa$ sinkt (N.3) |
| **Netto-Null** | $e_E Y_{\text{fossil}} = a_E N + \delta_E E$ | Stationärer Zustand $E^*$ |
| **Regeneration** | $e_E Y_{\text{fossil}} < a_E N + \delta_E E$ | Emissionen sinken → $\kappa$ erholt sich |

**Die aktuelle Situation der Weltwirtschaft**: Wir befinden uns tief im Akkumulations-Regime. $Y_{\text{fossil}}$ ist trotz erneuerbarer Energien weiterhin dominant. Die natürlichen Senken ($a_E N + \delta_E E$) sind gesättigt. Das Ergebnis: $E$ steigt monoton, und über N.3 sinkt die Tragfähigkeit $\kappa$.

### Der Kippunkt

Aus S13 §11.2 folgt ein *physischer Constraint*:

$$E(t) \leq E_{\text{krit}} \tag{G.3}$$

Wenn die kumulierten Emissionen $E$ eine kritische Schwelle $E_{\text{krit}}$ überschreiten, werden *nichtlineare Rückkopplungen* aktiviert (Permafrost-Auftauen, Methanfreisetzung, Eisschild-Kollaps), die die Absorptionskapazität $a_E$ sprunghaft senken und den Emissionszerfall $\delta_E$ reduzieren. Dies ist ein *Regimewechsel* (VIII.4, Kapitel 10): Die Gleichung VII.3 selbst ändert ihre Parameter. Jenseits von $E_{\text{krit}}$ ist die Dynamik *selbstverstärkend* — mehr Emissionen → weniger Senken → noch mehr Emissionen → Klimakatastrophe.

> **Proposition 9.4 (Klimatischer Kippunkt).** *Die Emissionstrajektorie VII.3 besitzt eine kritische Schwelle $E_{\text{krit}}$, jenseits derer die Dynamik von einem stabilen Regime (Senken kompensieren Quellen) in ein instabiles Regime (positive Rückkopplung: Emissionen verstärken sich selbst) übergeht. Die Überschreitung von $E_{\text{krit}}$ ist ein irreversibler Regimewechsel (→ VIII.4), der die Tragfähigkeit $\kappa$ über N.3 nachhaltig reduziert. Die Vermeidung dieses Kippunkts erfordert, dass $Y_{\text{fossil}}$ schneller sinkt als $E$ die Schwelle $E_{\text{krit}}$ erreicht.*

### Ökologische Tragfähigkeit (VII.4)

Die ökologische Tragfähigkeit $\kappa_{\text{eco}}$ ist eine *zusammenfassende Variable*, die den Gesamtzustand des ökologischen Systems in eine einzige Zahl komprimiert. Sie misst, wie viel die natürliche Umwelt *an ökonomischer Aktivität aushält* — eine breitere Zustandsgröße als $\kappa$ (N.3), die nur die Population begrenzt.

> **Gleichung VII.4 (Ökologische Tragfähigkeit).**
>
> $$\dot{\kappa}_{\text{eco}} = f_{\text{eco}}(H, \mathcal{T}, A/K) - e_E \cdot E - \delta_{\text{eco}} \cdot \kappa_{\text{eco}}$$

| Term | Bedeutung |
|---|---|
| $\kappa_{\text{eco}}$ | Ökologische Tragfähigkeit (Indikator für den Zustand der natürlichen Umwelt) |
| $f_{\text{eco}}(H, \mathcal{T}, A/K)$ | Aufbaufunktion: abhängig von Humankapital, Vertrauen und Technologieintensität |
| $H$ | Aggregiertes Humankapital (VII.2) |
| $\mathcal{T}$ | Sozialkapital / Vertrauen (VII.1) |
| $A/K$ | Technologieintensität: Technologie pro Kapitaleinheit |
| $e_E \cdot E$ | Emissionsbelastung (VII.3) |
| $\delta_{\text{eco}}$ | Natürliche Degradation des Ökosystems |

### Axiometrische Eigenschaften

Die Funktion $f_{\text{eco}}$ ist nicht spezifiziert — ihre axiometrischen Eigenschaften sind:

1. **Steigend in $H$**: $\partial f_{\text{eco}}/\partial H > 0$ — besser gebildete Gesellschaften schützen ihre Umwelt effektiver (Umweltbewusstsein, technische Kapazität zur Restauration).
2. **Steigend in $\mathcal{T}$**: $\partial f_{\text{eco}}/\partial \mathcal{T} > 0$ — kooperationsfähige Gesellschaften können kollektive Umweltgüter besser schützen (Vermeidung der Tragödie der Allmende).
3. **Steigend in $A/K$**: $\partial f_{\text{eco}}/\partial(A/K) > 0$ — technologieintensivere Wirtschaft (mehr Output pro Kapitaleinheit) schont Ressourcen.
4. **Fallend in $E$**: Emissionen degradieren das Ökosystem.
5. **Natürlicher Zerfall**: Ohne aktive Pflege degradieren Ökosysteme ($-\delta_{\text{eco}} \kappa_{\text{eco}}$).

### Die zwei Triebkräfte: Aufbau vs. Zerstörung

VII.4 hat eine klare Struktur: *Gesellschaftliche Kapazitäten bauen ökologische Tragfähigkeit auf* ($f_{\text{eco}} > 0$); *Emissionen und Zerfall zerstören sie* ($e_E E + \delta_{\text{eco}} \kappa_{\text{eco}} > 0$). Das Gleichgewicht $\dot{\kappa}_{\text{eco}} = 0$ erfordert:

$$f_{\text{eco}}(H, \mathcal{T}, A/K) = e_E E + \delta_{\text{eco}} \kappa_{\text{eco}}$$

Diese Gleichgewichtsbedingung hat eine tiefe Implikation: *Nachhaltige Entwicklung* ist der Zustand, in dem die gesellschaftlichen Aufbaukräfte die ökologische Zerstörung kompensieren. Dies erfordert *gleichzeitig* hohes Humankapital ($H$), hohes Vertrauen ($\mathcal{T}$), hohe Technologieintensität ($A/K$) und niedrige Emissionen ($E$) — vier Bedingungen, die in der Praxis selten gleichzeitig erfüllt sind.

> **Beobachtung 9.4 (Nachhaltigkeitsbedingung).** *VII.4 definiert eine formale Nachhaltigkeitsbedingung:*
>
> $$f_{\text{eco}}(H, \mathcal{T}, A/K) > e_E E + \delta_{\text{eco}} \kappa_{\text{eco}} \quad \Leftrightarrow \quad \dot{\kappa}_{\text{eco}} > 0$$
>
> *Nachhaltige Entwicklung ist der Zustand, in dem die ökologische Tragfähigkeit wächst — nicht als moralische Forderung, sondern als Ungleichungsbedingung über endogene Variablen des Systems. Eine Gesellschaft mit niedrigem $H$, niedrigem $\mathcal{T}$ und hohem $E$ verletzt diese Bedingung und befindet sich auf einem ökologischen Abbaupfad.*

### Kopplung von VII.3 und VII.4

| Gleichung | Kopplungskanal |
|---|---|
| **N.3** (§9.2) | $E$ senkt $\kappa$: Emissionen reduzieren die populationsbezogene Tragfähigkeit |
| **N.4** (§9.2) | Fossile Ressourcennutzung erzeugt Emissionen: $Y_{\text{fossil}}$ koppelt N.4 an VII.3 |
| **VII.1** (§9.3) | $\mathcal{T}$ treibt $f_{\text{eco}}$: Kooperationsfähigkeit für Umweltschutz |
| **VII.2** (§9.3) | $H$ treibt $f_{\text{eco}}$: Bildung für Umweltbewusstsein und -kompetenz |
| **III.3** (§6.6) | $Y_{\text{fossil}}$ als Teil der Produktion → Emissionsquelle |
| **VIII.4** (Kap. 10) | $E > E_{\text{krit}}$ → Regimewechsel |
| **VI.6** (§6.9) | $A/K$ bestimmt die Technologieintensität → Aufbauterm |

---

## 9.5 Kausale Gesamtstruktur: Die ultra-langsame Rückkopplung

Die neun Gleichungen dieses Kapitels bilden ein *geschlossenes Subsystem* langsamer Variablen, das auf die schnelleren Subsysteme (Kapitel 4–8) rückwirkt. Die kausale Struktur lässt sich in drei verschachtelte Kreisläufe zerlegen.

### Kreislauf 1: Demografie-Vermögen-Rückkopplung

```
N.5: b(w̄) — Geburtenrate sinkt mit Wohlstand
│
└── N.1/N.2: Ṅ = r_N N(1 − N/κ) — Population wächst/schrumpft
    │
    └── IV.3: w̄ = W/N — Wohlstand pro Kopf hängt von N ab
        │
        └── I.1/I.2: Ẇ = Y − C — Vermögen wächst mit BIP
            │
            └── N.5: b(w̄) — Rückkopplung (stabilisierend)
```

Dieser Kreislauf ist *negativ* (stabilisierend): Mehr Wohlstand → weniger Kinder → weniger Menschen → mehr Wohlstand pro Kopf. Er erklärt den demografischen Übergang als endogenes Phänomen.

### Kreislauf 2: Ressourcen-Tragfähigkeit-Rückkopplung

```
N.4: Ṙ = r_R R − e_R N − δ_R R — Ressourcen sinken mit N
│
└── N.3: κ ∝ R — Tragfähigkeit sinkt mit R
    │
    └── N.2: Ṅ < 0 (wenn N > κ) — Population fällt
        │
        └── N.4: e_R N sinkt → R stabilisiert sich (stabilisierend)
```

Dieser Kreislauf ist ebenfalls *negativ* (stabilisierend) — aber mit einem gefährlichen Transient: Wenn die Population die Tragfähigkeit *lange genug* überschreitet, kann $R$ unter einen kritischen Wert fallen, von dem aus keine Erholung mehr möglich ist (insbesondere bei fossilen Ressourcen, $r_R = 0$).

### Kreislauf 3: Emissionen-Ökologie-Kapazitäts-Rückkopplung

```
VII.3: Ė = e_E Y_fossil − ... — Emissionen steigen mit fossilem BIP
│
├── N.3: κ sinkt ← E steigt
│
└── VII.4: κ̇_eco < 0 ← E steigt
    │
    └── VII.1/VII.2: 𝒯, H bestimmen f_eco — gesellschaftliche Gegenkräfte
        │
        └── VII.4: f_eco(H, 𝒯, A/K) vs. e_E E — Wettlauf Aufbau gegen Zerstörung
```

Dieser Kreislauf ist *ambivalent*: Er kann stabilisierend sein (wenn gesellschaftliche Kapazitäten die Zerstörung kompensieren) oder *selbstverstärkend negativ* (wenn der Kippunkt $E_{\text{krit}}$ überschritten wird). Im letzten Fall entsteht der Klimakollaps.

### Zeitskalen-Trennung

Die Gleichungen dieses Kapitels operieren auf drei verschiedenen Zeitskalen:

| Zeitskala | Gleichungen | Typische Periode |
|---|---|---|
| **Dekaden** | N.1 (Klassenwechsel), N.5 (Demogr. Übergang), VII.1 ($\mathcal{T}$), VII.2 ($H$) | 10–30 Jahre |
| **Dekaden–Jahrhunderte** | N.2 (Population), N.3 ($\kappa$), N.4 ($R$), VII.3 ($E$) | 30–300 Jahre |
| **Jahrhunderte** | VII.4 ($\kappa_{\text{eco}}$) | 100–1000 Jahre |

Die *Separierung der Zeitskalen* ist für die Systemdynamik entscheidend: Die schnellen Subsysteme (Kapitel 4–8: Preise, Flüsse, Entscheidungen, Kredit) sehen die langsamen Variablen als *quasi-stationäre Parameter*. Die langsamen Variablen (Kapitel 9) sehen die schnellen als *bereits äquilibrierte Felder*. Diese Trennung bricht zusammen, wenn ein *exogener Schock* (Kapitel 10) eine langsame Variable sprunghaft ändert — z.B. ein Vertrauensschock, der $\mathcal{T}$ instantan senkt und damit den Geldschöpfungsmultiplikator M.4 *innerhalb* des schnellen Subsystems verändert.

> **Proposition 9.5 (Zeitskalen-Hierarchie).** *Das Gleichungssystem der Ökonoaxiomatik besitzt eine Hierarchie dreier Zeitskalen:*
>
> | Ebene | Zeitskala | Variablen | Gleichungen |
> |---|---|---|---|
> | **Schnell** (Konjunktur) | Quartale–Jahre | $p, q, c, \theta, \mathcal{I}$ | I.1, II.2, III.2, III.3, V.1–V.3, M.1 |
> | **Mittel** (Struktur) | Jahre–Dekaden | $w, N_X, \mathcal{T}, H$ | I.2, IV.1–IV.4, N.1, VII.1, VII.2 |
> | **Langsam** (Zivilisation) | Dekaden–Jahrhunderte | $N, \kappa, R, E, \kappa_{\text{eco}}$ | N.2–N.4, VII.3, VII.4 |
>
> *Die Standardmakroökonomik operiert ausschließlich auf der schnellen Ebene (Konjunkturmodelle: IS-LM, DSGE) oder auf der mittleren (Wachstumsmodelle: Solow, Ramsey). Die langsame Ebene (Klima, Ressourcen, Ökologie) wird typischerweise ausgelagert in separate Modelle (IAM: Integrated Assessment Models, z.B. DICE/RICE). Die Ökonoaxiomatik integriert alle drei Ebenen in einem einzigen Gleichungssystem.*

---

### Die Langfristvision: Wo befinden wir uns?

Zum Abschluss dieses Kapitels ordnen wir die neun Gleichungen in den Gesamtkontext des Gleichungssystems ein:

| Subsystem | Kapitel | Gleichungen | Variablen |
|---|---|---|---|
| Bilateral (Vermögen, Güter, Geld) | 4 | I.1–I.4, M.1–M.2, P.3, K.1 | $w, n, m$ |
| Preise und Flüsse | 5 | II.1–II.4, F.1–F.2 | $p, j, \Phi_w$ |
| Entscheidungen | 6 | V.1–V.3, L.1–L.5, III.2–III.4, U.1–U.3, VI.1–VI.9 | $c, \ell, \theta, q$ |
| Information | 7 | I.1–I.3, I.5, Ent.2 | $\mathcal{I}, a$ |
| Geld und Aggregation | 8 | M.3–M.4, E.1, P.4, V.9, IV.1–IV.4 | Lev, $m_{\text{mult}}, f, \text{Var}(w)$ |
| **Population und Struktur** | **9** | **N.1–N.5, VII.1–VII.4** | $N_X, \kappa, R, \mathcal{T}, H, E, \kappa_{\text{eco}}$ |
| Sprünge und Regime | 10 | VIII.1–VIII.7, Schw.1–2, RS.1 | (→ Kapitel 10) |

Mit Kapitel 9 sind Teile I und II der Monographie vollständig: Alle 75 Gleichungen des Systems sind eingeführt — aufgeteilt in die Mikro-Dynamik (Kap. 4–7), die Aggregation (Kap. 8), die Langfrist-Dynamik (Kap. 9) und die Regimewechsel (Kap. 10). Im nächsten Kapitel behandeln wir die *Sprünge, Schwellenwerte und Regimewechsel* — die Prozesse, die das System aus einem Regime in ein anderes stoßen.

---

*Ende von Kapitel 9. Im folgenden Kapitel behandeln wir Sprünge, Schwellenwerte und Regimewechsel — die diskontinuierlichen Prozesse, die das System zwischen verschiedenen dynamischen Regimen verschieben.*

---

# Kapitel 10: Sprünge, Schwellenwerte und Regime

Die bisherigen Kapitel beschreiben ein System, das sich *kontinuierlich* entwickelt: Preise gleiten auf Potentialflächen, Vermögen akkumulieren sich stetig, Populationen wachsen oder schrumpfen mit differenzierbaren Raten. Doch reale Ökonomien springen. Börsencrashs vernichten in Stunden, was in Jahren aufgebaut wurde. Bankruns entstehen über Nacht. Technologische Durchbrüche transformieren ganze Industrien schlagartig. Politische Regime kippen innerhalb von Wochen.

In der Sprache der dynamischen Systeme: Die Gleichungen I–VII bilden ein *glattes* System. Kapitel 10 erweitert es um *Diskontinuitäten* — Sprünge, absorbierende Barrieren, Schwellenwertentscheidungen und Regimewechsel. Diese Erweiterungen stehen in **Gruppe VIII** (Sprünge und Regime), **Schw.** (Schwellenwerte) und **RS.** (Regime-Switching). Zusammen fügen sie dem System drei qualitativ neue Phänomene hinzu:

| Phänomen | Gleichungen | Wirkung |
|---|---|---|
| **Preissprünge** | VIII.1–VIII.3 | Diskontinuierliche Preisbewegungen mit Fat Tails |
| **Regime-Switching** | VIII.4–VIII.5 | Parameterumschaltung zwischen qualitativen Zuständen |
| **Absorbierende Barrieren** | VIII.6 | Irreversibles Ausscheiden (Bankrott) |
| **Innovation/Katastrophe** | VIII.7 | Diskrete Kapitalsprünge |
| **Individuelle Schwellenwerte** | Schw.1–Schw.2 | Agenten-Entscheidungen als Kipppunkt-Prozesse |
| **Endogene Regimeübergänge** | RS.1 | Zustandsabhängige Übergangsraten (Mikro → Makro) |

Die logische Architektur: VIII.1–VIII.3 beschreiben *was während eines Sprungs passiert* (Amplitude, Rate, Verteilung). VIII.4–VIII.5 etablieren die *Makro-Infrastruktur* der Regimewechsel (Markov-Kette, regime-abhängige Parametersätze). VIII.6–VIII.7 behandeln *spezifische diskrete Ereignisse* (Bankrott, Innovation). Schw.1–Schw.2 liefern die *Mikrofundierung*: Individuelle Schwellenwertentscheidungen aggregieren sich über Granovetter-Kaskaden zu kollektiven Regimewechseln. RS.1 schließt den Kreis: Die aggregierte Schwellenwertdynamik *endogenisiert* die Markov-Übergangsraten von VIII.4.

---

## §10.1 Sprungprozesse (VIII.1–VIII.3)

Die kontinuierliche Preisdynamik II.2 (Kapitel 5) beschreibt die Reaktion des Preises auf aggregierten Excess Demand. In normalen Zeiten genügt diese glatte Dynamik. Doch Finanzmärkte zeigen Phänomene, die keine stetige Funktion erzeugen kann: Am 6. Mai 2010 verlor der Dow Jones innerhalb von Minuten fast 1000 Punkte (Flash Crash). Am 19. Oktober 1987 fiel er an einem einzigen Tag um 22,6%. Mandelbrot (1963) dokumentierte, dass Preisänderungen schwere Tails aufweisen — extreme Ereignisse treten *Größenordnungen häufiger* auf als eine Normalverteilung vorhersagt.

Die Konsequenz: Das Preismodell muss um *Sprünge* erweitert werden. Die drei Gleichungen VIII.1–VIII.3 bilden eine geschlossene Beschreibung: VIII.1 definiert die Sprungdynamik (die SDE), VIII.2 bestimmt *wann* gesprungen wird (die Rate), und VIII.3 bestimmt *wie groß* der Sprung ist (die Verteilung).

### Jump-Diffusion (VIII.1)

> **Gleichung VIII.1 (Jump-Diffusion).**
>
> $$dp = \mu_p \cdot p \cdot dt + \sigma_p \cdot p \cdot dW + \int j(p, \ell)\, \tilde{N}(dt, d\ell)$$

| Symbol | Bedeutung |
|---|---|
| $\mu_p$ | Drift-Rate (deterministische Tendenz) |
| $\sigma_p$ | Volatilität (Diffusion, Brown'sche Bewegung) |
| $dW$ | Wiener-Prozess-Inkrement |
| $j(p, \ell)$ | Sprunggrößen-Funktion (abhängig von Preislevel $p$ und Amplitude $\ell$) |
| $\tilde{N}(dt, d\ell)$ | Kompensiertes Poisson-Zufallsmaß (Lévy-Maß) |

Die Gleichung ist eine stochastische Differentialgleichung (SDE) mit drei Komponenten:

1. **Drift**: $\mu_p \cdot p \cdot dt$ — die deterministische Preistendenz, die aus II.2 folgt. $\mu_p$ enthält den aggregierten Excess Demand als Drift.
2. **Diffusion**: $\sigma_p \cdot p \cdot dW$ — die kontinuierliche stochastische Komponente. Kleine, stetige Preisschwankungen.
3. **Sprünge**: $\int j(p, \ell)\, \tilde{N}(dt, d\ell)$ — diskontinuierliche Preisänderungen, getrieben durch ein Poisson-Maß mit Sprungamplituden $\ell$.

Die Kompensation ($\tilde{N}$ statt $N$) stellt sicher, dass der Sprungterm ein Martingal ist — eine technische Voraussetzung für konsistente Preisbildung.

> **Proposition 10.1 (Preisnicht-Negativität).** *Sofern die Sprunggrößen-Funktion $j(p, \ell) > -p$ für alle $\ell$ erfüllt, bleibt der Preis $p > 0$ für alle Zeiten. Die Bedingung besagt: Kein einzelner Sprung kann den Preis *unter Null* drücken.*

### Kopplung an das Gesamtsystem

VIII.1 überlagert II.2, nicht ersetzt sie:

- $\mu_p$ enthält die Walras-Drift aus II.2 (Excess Demand → Preisgradient)
- Die Volatilität $\sigma_p$ kann regimeabhängig sein (→ VIII.5): In einer Krise steigt $\sigma_p^{(\text{Krise})} \gg \sigma_p^{(\text{Boom})}$
- Die Sprungrate ist *nicht konstant*, sondern durch VIII.2 endogenisiert
- Preissprünge wirken auf die Vermögensbilanz I.1: Ein Portfoliohalter mit Position $\theta_{ik}$ in Gut $k$ erfährt bei Preissprung $dp_k$ eine diskrete Vermögensänderung $\theta_{ik} \cdot dp_k$

### Axiometrische Eigenschaften

| Eigenschaft | Formal | Ökonomisch |
|---|---|---|
| Semi-Martingal | $dp$ ist Semimartingal | Konsistente Preisbildung, kein Arbitrage |
| Rechtsseitig stetig | $p$ ist càdlàg (rechts stetig, linke Limiten existieren) | Preis springt *zu* einem neuen Wert, fällt nie ins Nichts |
| Endliche Variation lokal | Sprünge haben beschränkte lokale Variation | Kein Zeno-Paradox (unendlich viele Sprünge in endlicher Zeit nur bei endlicher Gesamtamplitude) |

### Spezialfälle

| Bedingung | Resultat | Historisches Modell |
|---|---|---|
| $\int j \cdot \tilde{N} = 0$ | Standard-GBM $dp = \mu p\, dt + \sigma p\, dW$ | Black-Scholes (1973) |
| $\sigma_p = 0$, nur Sprünge | Reiner Poisson-Prozess | Compound-Poisson-Modell |
| $\mu_p = 0$, $\sigma_p = 0$ | Reiner Sprungprozess ohne Drift | Katastrophenmodell |

---

### Informationsabhängige Sprungrate (VIII.2)

Die zentrale Innovation gegenüber dem Standard-Merton-Modell (1976): Die Sprungrate $\lambda_J$ ist *nicht konstant*, sondern hängt vom Systemzustand ab — insbesondere von der Information $I$ (Kapitel 7) und dem Herding-Maß $H_{\text{herd}}$ (Kapitel 6).

> **Gleichung VIII.2 (Informationsabhängige Sprungrate).**
>
> $$\lambda_J(t) = \lambda_0 + \lambda_I \cdot \mathcal{I}(t)^{-1} + \lambda_H \cdot H_{\text{herd}}(t)$$

| Symbol | Bedeutung | Vorzeichen |
|---|---|---|
| $\lambda_J(t)$ | Sprungintensität (Sprünge pro Zeiteinheit) | $> 0$ stets |
| $\lambda_0$ | Basis-Sprungrate (strukturelle Instabilität) | $> 0$ |
| $\lambda_I$ | Informations-Sensitivität | $> 0$ |
| $\mathcal{I}(t)$ | Informationsfeld (aus I.1, Kapitel 7) | $> 0$ |
| $\lambda_H$ | Herding-Sensitivität | $\geq 0$ |
| $H_{\text{herd}}(t)$ | Aggregiertes Herding-Maß (mittlere Portfoliokorrelation) | $\in [0,1]$ |

### Drei Quellen der Sprungwahrscheinlichkeit

| Term | Mechanismus | Referenz |
|---|---|---|
| $\lambda_0$ | Strukturelle Basisinstabilität (exogene Schocks: Erdbeben, politische Attentate, Schwarze Schwäne) | — |
| $\lambda_I \cdot \mathcal{I}^{-1}$ | Informationskanal: Niedrige Information → Markt ist fragil → Sprünge häufiger | Grossman-Stiglitz (1980) |
| $\lambda_H \cdot H_{\text{herd}}$ | Herding-Kanal: Gleichgerichtete Portfolios → synchroner Verkaufsdruck → Flash Crash | Cont-Bouchaud (2000) |

> **Observation 10.1 (Singularität bei Informationskollaps).** *Für $\mathcal{I} \to 0$ divergiert $\lambda_J \to \infty$: Ein vollständiger Informationskollaps erzeugt mit Sicherheit einen Sprung. Dies ist die formale Version der Intuition, dass *Märkte ohne Information jederzeit crashen*.*

### Axiometrische Eigenschaften

1. **Positivität**: $\lambda_J > 0$ stets ($\lambda_0 > 0$ garantiert).
2. **Monotonie in Information**: $\partial\lambda_J / \partial\mathcal{I} < 0$ — mehr Information stabilisiert.
3. **Monotonie in Herding**: $\partial\lambda_J / \partial H_{\text{herd}} > 0$ — mehr Herding destabilisiert.
4. **Einheit**: $[\lambda_J] = \text{yr}^{-1}$ (Sprünge pro Zeiteinheit).

> **Proposition 10.2 (Endogene Fragilität).** *Die Kopplung VIII.2 ↔ I.1 ↔ III.2 erzeugt einen positiven Rückkopplungskreis: Ein erster Sprung (VIII.1) reduziert die Information $\mathcal{I}$ (I.1, Informationszerstörung bei Schocks) und erhöht das Herding $H_{\text{herd}}$ (III.2, Herding steigt bei Unsicherheit). Beides erhöht $\lambda_J$ (VIII.2), was den nächsten Sprung wahrscheinlicher macht. Das System kann in eine Spirale eintreten: Sprung → weniger Information → mehr Herding → höhere Sprungrate → nächster Sprung.*

---

### Lévy-Sprungverteilung (VIII.3)

VIII.2 bestimmt, *wann* gesprungen wird. VIII.3 bestimmt, *wie groß* der Sprung ist.

> **Gleichung VIII.3 (Lévy-Sprungverteilung).**
>
> $$\ell(t) \sim \text{Lévy}(\alpha_L, \sigma_L), \qquad \alpha_L \in [1, 2]$$

| Symbol | Bedeutung |
|---|---|
| $\ell(t)$ | Sprungamplitude (zufällig, zum Zeitpunkt des Sprungs gezogen) |
| $\alpha_L$ | Lévy-Stabilitätsindex (Fat-Tail-Parameter) |
| $\sigma_L$ | Skalenparameter der Verteilung |

### Der Fat-Tail-Parameter $\alpha_L$

Der Stabilitätsindex $\alpha_L$ bestimmt die *Wildheit* der Sprungverteilung:

| $\alpha_L$ | Tail-Verhalten | Momente | Ökonomisch |
|---|---|---|---|
| $= 2$ | Gauß (exponentieller Abfall) | Alle endlich | Milde Schwankungen — Black-Scholes-Welt |
| $\in (1,2)$ | Potenzgesetz: $P(|\ell| > x) \sim x^{-\alpha_L}$ | Varianz $= \infty$ | Extreme Sprünge — Mandelbrot-Welt |
| $= 1$ | Cauchy (extremes Fat Tail) | Mittelwert $= \infty$ | Total wilde Märkte — kein endlicher Erwartungswert |

Die empirische Evidenz für Finanzmärkte liegt bei $\alpha_L \approx 1{,}5$–$1{,}7$ (Mandelbrot 1963, Cont 2001, Gabaix et al. 2003): Die Tail-Exponent ist strikt kleiner als 2, die Varianz der Preisänderungen ist formal unendlich. Dies hat drastische Konsequenzen:

> **Observation 10.2 (Versagen der Normalverteilung).** *Für $\alpha_L < 2$ hat die Sprungverteilung keine endliche Varianz. Risikomaße, die auf der Normalverteilung basieren (VaR unter Gauß-Annahme, Standardabweichung als Risikomaß, Sharpe Ratio), *unterschätzen das tatsächliche Risiko systematisch*. Dies ist der formale Grund, warum Finanzregulierung, die auf Normalverteilungsannahmen beruht, regelmäßig versagt.*

### Zusammenspiel VIII.1–VIII.3

Die drei Gleichungen bilden ein geschlossenes Sprungmodul:

```
VIII.2: λ_J(t) = λ_0 + λ_I/I + λ_H · H_herd   →  WANN wird gesprungen?
VIII.3: ℓ ~ Lévy(α_L, σ_L)                       →  WIE GROSS ist der Sprung?
VIII.1: dp = μ·p·dt + σ·p·dW + ∫j(p,ℓ)·Ñ(dt,dℓ) →  WAS PASSIERT mit dem Preis?
```

Die Intensität des Poisson-Maßes $\tilde{N}$ in VIII.1 wird durch VIII.2 bestimmt; die Amplitude $\ell$ durch VIII.3. VIII.1 kombiniert beides mit der glatten Drift-Diffusion aus II.2 zu einer vollständigen Preisdynamik.

---

## §10.2 Regime-Switching (VIII.4–VIII.5)

Die Sprungprozesse VIII.1–VIII.3 beschreiben diskontinuierliche Preisbewegungen *innerhalb* eines Regimes. Regime-Switching beschreibt etwas Grundlegenderes: Die *Spielregeln selbst* ändern sich. In einem Boom gelten andere Risikoaversionen, andere Kreditbedingungen, anderes Herding als in einer Krise. Die Preissensitivität auf Nachrichten ist eine andere; die geldpolitische Reaktionsfunktion ist eine andere; die Erwartungsbildung ist eine andere. Das System bewegt sich nicht nur auf einer Potentialfläche — es *wechselt die Potentialfläche*.

### Regime-Switching als Markov-Kette (VIII.4)

> **Gleichung VIII.4 (Regime-Switching).**
>
> $$Z(t) \in \{1, \dots, S\}, \qquad P(Z_{t+dt} = j \mid Z_t = i) = q_{ij} \cdot dt \quad (i \neq j)$$

| Symbol | Bedeutung |
|---|---|
| $Z(t)$ | Aktueller Regime-Zustand (diskret, endlich) |
| $S$ | Anzahl der Regime |
| $q_{ij}$ | Übergangsrate von Regime $i$ nach Regime $j$ ($q_{ij} \geq 0$, $i \neq j$) |

> **Definition 10.1 (Generator-Matrix).** *Die Rate-Matrix $Q = (q_{ij})_{i,j=1}^S$ mit $q_{ii} = -\sum_{j \neq i} q_{ij}$ ist der infinitesimale Generator der Markov-Kette $Z(t)$. Sie bestimmt die Übergangswahrscheinlichkeiten über $P(t) = e^{Qt}$.*

### Axiometrische Eigenschaften

1. **Konsistenz**: Die Zeilen der Generator-Matrix summieren zu Null: $\sum_j q_{ij} = 0$. Übergangswahrscheinlichkeiten sind erhalten.
2. **Verweildauer**: Die Verweildauer in Regime $i$ ist exponentialverteilt mit Rate $|q_{ii}|$. Erwartete Verweildauer: $1/|q_{ii}|$.
3. **Ergodizität**: Wenn die Kette irreduzibel ist (jedes Regime erreichbar), existiert eine stationäre Verteilung $\pi$ mit $\pi Q = 0$.
4. **Markov-Eigenschaft**: Die Zukunft von $Z$ hängt nur vom aktuellen Zustand ab, nicht von der Historie — eine Vereinfachung, die in §10.5 über RS.1 differenziert wird.

### Ökonomische Interpretation

| Regime-Anzahl $S$ | Typische Konfiguration | Referenz |
|---|---|---|
| $S = 2$ | Expansion / Rezession | Hamilton (1989) |
| $S = 3$ | Boom / Normal / Krise | Guidolin-Timmermann (2008) |
| $S = 4$ | Wachstum / Stagnation / Krise / Erholung | Ang-Bekaert (2002) |

Die Wahl von $S$ ist eine *Modellierungsentscheidung*, keine axiomatische Notwendigkeit. Wesentlich ist nur, dass $S > 1$: Es gibt qualitativ verschiedene Zustände des ökonomischen Systems, und Übergänge zwischen ihnen sind stochastisch.

### Spezialfälle

| Bedingung | Resultat |
|---|---|
| $S = 1$ | Kein Regime-Switching → Standardsystem (I–VII) |
| $q_{ij} = 0\ \forall\, i \neq j$ | Permanentes Regime, kein Wechsel möglich |
| $q_{ij} \to \infty$ | Sofortiger Wechsel → adiabatischer Grenzfall (ergodisches Mittel über alle Regime) |

---

### Regime-abhängiges Gesamtsystem (VIII.5)

VIII.4 definiert die Regime-Kette $Z(t)$. VIII.5 beschreibt die Konsequenz: *Alle Systemparameter können vom Regime abhängen.*

> **Gleichung VIII.5 (Regime-abhängiges Gesamtsystem).**
>
> $$\frac{dX}{dt} = F^{(Z(t))}(X) + \Sigma^{(Z(t))} \cdot \xi$$

| Symbol | Bedeutung |
|---|---|
| $X$ | Vollständiger Zustandsvektor (alle Variablen aus I–VII) |
| $F^{(Z)}$ | Regime-spezifische Drift (deterministische Dynamik im Regime $Z$) |
| $\Sigma^{(Z)}$ | Regime-spezifische Diffusionsmatrix (stochastische Dynamik) |
| $\xi$ | Weißes Rauschen (Vektor) |

### Was bedeutet „regimeabhängig"?

Jeder Parameter des Gesamtsystems kann einen Regime-Index tragen:

| Parameter | Boom (Z=1) | Normal (Z=2) | Krise (Z=3) |
|---|---|---|---|
| Risikoaversion $\gamma_i$ | Niedrig | Mittel | Hoch |
| Herding-Parameter $\alpha_H$ | Moderat | Niedrig | Hoch |
| Kreditvergabe-Neigung | Expansiv | Neutral | Restriktiv |
| Volatilität $\sigma_p$ | Niedrig | Mittel | Hoch |
| Vertrauensaufbau $\alpha_{\mathcal{T}}$ | Positiv | Neutral | Negativ |

> **Proposition 10.3 (Regime-Konsistenz).** *Innerhalb jedes Regimes $Z = z$ ist das System ein glattes SDE-System $dX/dt = F^{(z)}(X) + \Sigma^{(z)} \xi$, für das die Hadamard-Bedingungen (Existenz, Eindeutigkeit, stetige Abhängigkeit von Anfangsbedingungen) separat gelten. An den Regime-Übergängen sind die Parameter diskontinuierlich — das Gesamtsystem ist stückweise glatt.*

### Axiometrische Eigenschaften

1. **Stückweise Glattheit**: Innerhalb jedes Regimes ist $F^{(Z)}$ glatt; an Übergängen springt der Parametersatz.
2. **Hierarchie**: VIII.5 ändert *Parameter*, nicht *Gleichungen*. Die strukturelle Form der Gleichungen I–VII bleibt in jedem Regime gleich.
3. **Symmetrie-Bruch**: Verschiedene Regime können verschiedene Gleichgewichte haben. Ein Boom-Gleichgewicht existiert möglicherweise in der Krisenparametrisierung nicht.
4. **Bifurkation**: Regime-Wechsel können das System über die Bifurkationsschwelle eines Parameters schieben → qualitativ neue Dynamik.

---

## §10.3 Bankrott und Innovation (VIII.6–VIII.7)

Die bisherigen Gleichungen VIII.1–VIII.5 behandeln *Systemsprünge*: Preise springen, Parameter wechseln. VIII.6 und VIII.7 behandeln *individuelle diskrete Ereignisse*: Ein Agent geht bankrott; eine Innovation transformiert den Kapitalstock.

### Absorbierende Barriere: Bankrott (VIII.6)

> **Gleichung VIII.6 (Bankrott-Barriere).**
>
> $$T_{\text{bankrott}} = \inf\{t : w_i(t) \leq 0\}$$

| Symbol | Bedeutung |
|---|---|
| $T_{\text{bankrott}}$ | Stopzeit (erster Zeitpunkt der Insolvenz) |
| $w_i(t)$ | Vermögen des Agenten $i$ (aus I.1) |
| $\inf\{\cdot\}$ | Infimum: erster Zeitpunkt, zu dem die Bedingung zutrifft |

Die Gleichung definiert eine *absorbierende Barriere*: Sobald das Vermögen eines Agenten null (oder negativ) wird, scheidet er aus dem aktiven System aus. Dies ist ein *First-Passage-Time-Problem*: Gesucht ist die Verteilung der Zeitpunkte, zu denen die Vermögenstrajektorie $w_i(t)$ erstmals die Nulllinie kreuzt.

### Axiometrische Eigenschaften

1. **Irreversibilität** (im Basismodell): Bankrott ist ein absorbierender Zustand. Agent $i$ wird aus den Bilanzgleichungen I.1 entfernt.
2. **Populationskopplung**: Bei Bankrott gilt $N_X \to N_X - 1$ (N.1 — Populationsänderung innerhalb einer Klasse).
3. **Bilanz-Konsequenz**: Das Restvermögen (negativ, da Schulden $>$ Aktiva) muss auf Gläubiger verteilt werden → Kaskadenpotential.
4. **Verteilung**: Die First-Passage-Time $T_{\text{bankrott}}$ hängt von der Drift $\mu_w$ und der Volatilität $\sigma_w$ der Vermögensdynamik ab. Für einen geometrischen Random Walk mit negativer Drift ist $T < \infty$ fast sicher.

### Kopplungen

| Gleichung | Wirkungskanal |
|---|---|
| I.1 | Die Dynamik von $w_i$ bestimmt die First-Passage-Time |
| IV.1 | Bankrott erzeugt Konzentration der Vermögensverteilung bei $w = 0$ |
| N.1 | Populationsänderung: Scheidender Agent reduziert $N_X$ |
| M.3 | Bankausfall (Banken): $E_b < 0 \to$ Leverage-Reset → Kreditkontraktion |
| L.5 | Unternehmerkreislauf: Gründung (L.5) $\leftrightarrow$ Bankrott (VIII.6) |
| VIII.4/RS.1 | Massenkonkurs → Regimewechsel (Krise) |

> **Observation 10.3 (Kaskadeneffekt bei Bankrott).** *Der Bankrott eines Agenten ist kein isoliertes Ereignis. Über I.1 überträgt sich der Ausfall auf Gläubiger (Forderungsverlust), über M.3 auf das Kreditvolumen (Leverage-Kontraktion), über III.2 auf Erwartungen (Herding steigt). Ein Bankrott kann weitere Bankrotte auslösen — eine Kaskade, die über RS.1 zum Regimewechsel führen kann.*

### Spezialfälle

| Bedingung | Resultat |
|---|---|
| $\sigma_w = 0$ (deterministisch) | $T_{\text{bankrott}} = \infty$ wenn $\dot{w} > 0$ stets; endlich wenn $\dot{w} < 0$ persistiert |
| Beschränkte Haftung: $w_i \geq -w_{\max}$ | Bankrott bei $w_i \leq -w_{\max}$ |
| Recovery-Erweiterung | Bankrott ist nicht absorbierend; Agent kann über Entschuldungsprozess zurückkehren |

---

### Diskrete Innovation und Katastrophe (VIII.7)

> **Gleichung VIII.7 (Diskreter Kapitalsprung).**
>
> $$K(t^+) = K(t^-) + \Delta K_{\text{innov}}$$

| Symbol | Bedeutung |
|---|---|
| $K(t^+)$ | Kapitalstock unmittelbar *nach* dem Sprung |
| $K(t^-)$ | Kapitalstock unmittelbar *vor* dem Sprung |
| $\Delta K_{\text{innov}}$ | Diskrete Kapitaländerung (positiv: Innovation, negativ: Katastrophe) |

### Zwei Vorzeichen, zwei Phänomene

| Fall | $\Delta K_{\text{innov}}$ | Mechanismus | Historische Beispiele |
|---|---|---|---|
| **Innovation** | $> 0$ | Technologischer Durchbruch erhöht den *effektiven* Kapitalstock schlagartig | Dampfmaschine, Elektrizität, Internet |
| **Katastrophe** | $< 0$ | Physische Vernichtung von Kapital | Krieg, Erdbeben, Pandemie |

Die Gleichung ist bewusst minimal: Sie beschreibt den Sprung selbst, nicht seine Ursache. Die Ursache wird durch andere Gleichungen bestimmt:

- Innovation: Der Technologieindex $A$ (VI.6) überschreitet eine kritische Schwelle → diskreter Produktivitätssprung
- Katastrophe: Exogener Schock (Krieg) oder endogener Zusammenbruch (Systemkrise) → physischer Kapitalverlust
- *Schöpferische Zerstörung* (Schumpeter): $\Delta K_{\text{alt}} < 0$ und $\Delta K_{\text{neu}} > 0$ simultan — die alte Technologie wird vernichtet, die neue entsteht

### Kopplung

| Gleichung | Wirkungskanal |
|---|---|
| VI.6 | Technologiedynamik $\dot{A}$ — Innovation als Sprung in $A$ |
| I.1–I.2 | Vermögensbilanz reagiert sofort auf Kapitalsprung |
| III.3 | Produktionsfunktion ändert sich bei Kapitalsprung |
| N.3 | Tragfähigkeit $\kappa$ springt bei Technologiedurchbruch ($\kappa \uparrow$) |
| Ent.2 | Katastrophe als $\Delta K < 0$ |

> **Proposition 10.4 (Asymmetrie von Innovation und Katastrophe).** *Positive Innovationssprünge sind typischerweise selten und groß (Schumpeters „Gale of Creative Destruction": wenige, transformative Durchbrüche). Negative Katastrophensprünge sind noch seltener und noch größer (Kriege, Pandemien). Beide folgen einer rechtsschiefen Verteilung — der Erwartungswert wird von den seltenen extremen Ereignissen dominiert.*

---

## §10.4 Schwellenwertdynamik (Schw.1–Schw.2)

Die Gleichungen VIII.1–VIII.7 beschreiben Sprünge und Regimewechsel auf *Systemebene*. Doch was *treibt* diese Wechsel? Warum kippt ein Markt plötzlich von Euphorie in Panik? Warum bricht ein politisches Regime zusammen, das jahrelang stabil schien?

Die Antwort liegt auf der *Mikro-Ebene*: Individuelle Agenten treffen discontinuierliche Entscheidungen — sie wechseln von „halten" zu „verkaufen", von „bleiben" zu „fliehen", von „kooperieren" zu „revoltieren". Jede dieser Entscheidungen hat einen *Schwellenwert*: einen kritischen Punkt, ab dem der Agent umschaltet. Die Aggregation vieler solcher Schwellenwertentscheidungen erzeugt die kollektiven Sprünge, die VIII.1–VIII.5 auf Makroebene beschreiben. Dies ist die *Mikrofundierung des Regime-Switchings*.

### Schwellenwert-Aktivierung (Schw.1)

> **Gleichung Schw.1 (Schwellenwert-Aktivierung).**
>
> $$S_i^{(k)}(t) = \sigma\!\left(\frac{\mu_k^{(i)}(t) - \theta_k^{(i)}}{\tau_k}\right), \qquad \sigma(x) = \frac{1}{1 + e^{-x}}$$

| Symbol | Bedeutung |
|---|---|
| $S_i^{(k)}(t)$ | Aktivierungswahrscheinlichkeit für Entscheidung $k$ des Agenten $i$ |
| $\mu_k^{(i)}(t)$ | Entscheidungspotential (aggregiert alle Anreize) |
| $\theta_k^{(i)}$ | Individueller Schwellenwert (Trägheit, Gewohnheit, Transaktionskosten) |
| $\tau_k > 0$ | Temperaturparameter (Schärfe der Entscheidung) |
| $\sigma(x)$ | Logistische Sigmoid-Funktion |

### Entscheidungspotentiale: Fünf Anwendungen

Die Gleichung Schw.1 ist eine *universelle Formel*: Sie beschreibt jede diskrete Entscheidung als Sigmoid-Aktivierung. Was sich ändert, ist das Entscheidungspotential $\mu_k^{(i)}$ und der Schwellenwert $\theta_k^{(i)}$:

| Entscheidung $k$ | Entscheidungspotential $\mu_k^{(i)}$ | Schwellenwert $\theta_k^{(i)}$ |
|---|---|---|
| **Unternehmensgründung** (L.5) | $\Pi_i^{\text{erw}}$ — erwarteter Gewinn | $c_{\text{entry}}$ — Gründungskosten |
| **Migration** | $w_L^{(\text{Ziel})} - w_L^{(\text{Quelle})} - c_{\text{Mig}}$ — Lohndifferenz | Soziale Bindung |
| **Bankrun** | $\alpha_H \cdot \bar{S}_{\text{Peers}} + (1 - \mathcal{I}_i^{\text{Bank}})$ — Herding + Informationsmangel | $\theta_{\text{trust}}$ — Vertrauen |
| **Technologieadoption** | $\Delta Y_k / Y_k - c_{\text{adopt}}$ — Produktivitätsgewinn | Lernkosten |
| **Regime-Wechsel** | $|\mu^{\text{eff}} - p|$ — Preisüberbewertung (Irrationalitätsgap) | Regime-Trägheit |

### Axiometrische Eigenschaften

1. **Wertebereich**: $S_i^{(k)} \in (0, 1)$ — stets eine Wahrscheinlichkeit.
2. **Monotonie**: $\partial S / \partial \mu > 0$ — höherer Anreiz → höhere Aktivierungswahrscheinlichkeit.
3. **Symmetrie am Kipppunkt**: $S(\mu = \theta) = 1/2$ — am Schwellenwert besteht perfekte Unsicherheit.
4. **Temperatur-Grenzfälle**:
   - $\tau_k \to 0$: $S \to \Theta(\mu - \theta)$ (Heaviside-Funktion) — deterministische Entscheidung: ja/nein.
   - $\tau_k \to \infty$: $S \to 1/2$ — völlige Indifferenz, Entscheidung ist Zufall.

> **Definition 10.2 (Temperaturparameter $\tau_k$).** *Der Temperaturparameter steuert die **Schärfe** der Entscheidung. Ein kleines $\tau_k$ bedeutet: Der Agent entscheidet fast deterministisch, sobald $\mu_k > \theta_k$. Ein großes $\tau_k$ bedeutet: Selbst bei hohem Anreiz entscheidet der Agent nur mit mäßiger Wahrscheinlichkeit. In der Physik entspricht $\tau_k$ der thermischen Energie; in der Ökonomik misst $\tau_k$ die Qualität der Informationsverarbeitung und die Rationalität des Agenten.*

### Mean-Field-Aggregation

Aus den $N$ individuellen Aktivierungen entsteht ein aggregiertes Maß:

$$\bar{S}^{(k)}(t) = \frac{1}{N} \sum_i S_i^{(k)} \approx \int \sigma\!\left(\frac{\mu_k - \theta}{\tau_k}\right) f(\theta)\, d\theta$$

wobei $f(\theta)$ die Verteilung der Schwellenwerte in der Population ist. Diese Integral-Aggregation verbindet die Mikro-Entscheidung (einzelner Agent) mit dem Makro-Ergebnis (Anteil der Aktivierten).

### Die Granovetter-Schwelle

Die entscheidende Frage: Wann erzeugt eine kleine Änderung im Entscheidungspotential $\mu_k$ eine *lawinenartige* Kaskade von Aktivierungen?

> **Proposition 10.5 (Granovetter-Kaskadenbedingung).** *Die Kaskadenbedingung lautet:*
>
> $$\frac{\partial \bar{S}^{(k)}}{\partial \mu_k} > 1 \qquad \Longleftrightarrow \qquad \frac{1}{\tau_k} \cdot f(\bar{\theta}_k) > 1$$
>
> *In Worten: Eine Kaskade tritt auf, wenn die **Dichte der Schwellenwertverteilung** am aktuellen Kipppunkt $\bar{\theta}_k$ **hoch genug** ist und die **Temperatur** $\tau_k$ **niedrig genug**. Eine enge Schwellenwertverteilung (viele Agenten nahe am gleichen Schwellenwert) bei niedriger Temperatur (deterministische Entscheidungen) garantiert: Wenn ein Agent kippt, kippen viele.*

Die Bedingung ist die formale Version von Granovetters (1978) *Threshold Model of Collective Behavior*: Heterogene Schwellenwerte in einer Population bestimmen, ob ein kleiner Anstoß eine Kaskade auslöst.

---

### Endogene Schwellenwertdynamik (Schw.2)

In Schw.1 sind die Schwellenwerte $\theta_k^{(i)}$ Parameter. Doch Schwellenwerte *ändern sich*: Ein Agent, der eine Blase überlebt hat, wird vorsichtiger (höherer Schwellenwert). Ein Agent, dessen Nachbarn alle verkaufen, wird ängstlicher (niedrigerer Schwellenwert). Schw.2 endogenisiert diese Dynamik.

> **Gleichung Schw.2 (Endogene Schwellenwertdynamik).**
>
> $$\dot{\theta}_k^{(i)} = -\alpha_\theta \cdot (\theta_k^{(i)} - \bar{\theta}_k) + \beta_\theta \cdot \mathbb{1}[\text{letzte Entscheidung fehlgeschlagen}] - \gamma_\theta \cdot \sum_j A_{ij} \cdot \mathbb{1}[S_j^{(k)} > 0{,}5]$$

| Term | Kraft | Ökonomisch |
|---|---|---|
| $-\alpha_\theta (\theta_k^{(i)} - \bar{\theta}_k)$ | **Mean Reversion** | Schwellenwert kehrt zum Populationsmittel zurück (Normalisierung, Vergessen) |
| $+\beta_\theta \cdot \mathbb{1}[\text{Fehlschlag}]$ | **Lernen aus Misserfolg** | Fehlgeschlagene Entscheidung $\to$ Schwelle steigt $\to$ Agent wird vorsichtiger |
| $-\gamma_\theta \cdot \sum_j A_{ij} \cdot \mathbb{1}[S_j > 0{,}5]$ | **Soziale Erosion** | Aktivierte Nachbarn senken die eigene Schwelle $\to$ Kaskadeneffekt |

### Drei Kräfte, ein Gleichgewicht

Die drei Terme wirken gegeneinander:

1. **Mean Reversion** ($\alpha_\theta$): Zieht alle Schwellenwerte zum Populationsmittel $\bar{\theta}_k$. Ohne die anderen Terme würde die Population homogen. Diese Kraft stabilisiert.
2. **Fehlschlag-Lernen** ($\beta_\theta$): Erhöht die Schwelle nach negativen Erfahrungen. Ein gebranntes Kind scheut das Feuer. Diese Kraft *erhöht* die Trägheit und *verhindert* Kaskaden.
3. **Soziale Erosion** ($\gamma_\theta$): Senkt die Schwelle, wenn Nachbarn bereits aktiviert sind. Dies ist der *Granovetter-Mechanismus*: Je mehr Nachbarn die Schwelle überschritten haben, desto leichter kippt der eigene Agent. Diese Kraft *treibt* Kaskaden.

> **Observation 10.4 (Der wandernde Kipppunkt).** *Schw.2 bewirkt, dass der Kipppunkt aus Proposition 10.5 nicht stationär ist. In normalen Zeiten dominiert die Mean Reversion ($\alpha_\theta$): Schwellenwerte sind breit verteilt, die Kaskadenbedingung $f(\bar{\theta})/\tau_k > 1$ ist nicht erfüllt, das System ist stabil. Aber die soziale Erosion ($\gamma_\theta$) kann die Schwellenwertverteilung zusammendrücken — die Verteilung wird enger, $f(\bar{\theta})$ steigt — bis plötzlich die Kaskadenbedingung erfüllt ist. Der Kipppunkt wandert zum System hin.*

### Axiometrische Eigenschaften

1. **Mean Reversion dominiert langfristig**: Für $\alpha_\theta$ groß genug konvergiert $\theta_k^{(i)} \to \bar{\theta}_k$.
2. **Hysterese**: Nach einer Krise ($\beta_\theta$-Schocks) sind Schwellenwerte erhöht → System ist vorübergehend *stabiler* (Krise reinigt).
3. **Netzwerkabhängig**: Stark vernetzte Agenten (hohe $\sum_j A_{ij}$) haben niedrigere effektive Schwellenwerte → sie kippen zuerst.
4. **Endogene Heterogenität**: Auch wenn alle Agenten mit dem gleichen $\theta$ starten, erzeugt Schw.2 durch unterschiedliche Nachbarschaften und Fehlschlagserfahrungen eine *heterogene Schwellenwertverteilung*.

---

## §10.5 Endogene Regimeübergänge (RS.1)

Bis hier sind die Übergangsraten $q_{ij}$ in VIII.4 exogene Konstanten — Regime wechseln mit fester Wahrscheinlichkeit, unabhängig vom Systemzustand. Dies ist unbefriedigend: Finanzkrisen passieren nicht zufällig. Sie werden durch Leverage-Aufbau, Herding, Informationsverlust und Vertrauenserosion *vorbereitet*. RS.1 schließt diese Lücke: Die Übergangsraten werden zustandsabhängig.

> **Gleichung RS.1 (Endogene Regime-Übergangsraten).**
>
> $$q_{ij}(X(t)) = q_{ij}^{(0)} \cdot \exp\!\left(\sum_m \beta_m^{(ij)} \cdot X_m(t)\right)$$

| Symbol | Bedeutung |
|---|---|
| $q_{ij}(X(t))$ | Endogene Übergangsrate von Regime $i$ nach $j$ |
| $q_{ij}^{(0)}$ | Basis-Übergangsrate (kann sehr klein sein: „Krisen sind selten") |
| $\beta_m^{(ij)}$ | Sensitivität des Übergangs $i \to j$ auf Zustandsvariable $X_m$ |
| $X_m(t)$ | Zustandsvariable $m$ aus dem Zustandsvektor |

### Warum die Exponentialform?

Die Exponentialform garantiert $q_{ij} > 0$ für alle Zustände $X$ — eine physikalische Konsistenzbedingung (Übergangsraten müssen nicht-negativ sein). Zudem hat sie eine natürliche Interpretation: Kleine Zustandsänderungen können *exponentielle* Änderungen der Übergangsrate bewirken. Das System ist *sensitiv auf Kipppunkte*.

> **Definition 10.3 (Endogenisierung).** *RS.1 ersetzt die konstanten $q_{ij}$ in VIII.4 durch eine zustandsabhängige Funktion $q_{ij}(X)$. Damit wird die Markov-Kette $Z(t)$ zum* zustandsmodulierten Markov-Prozess *— die Übergangswahrscheinlichkeiten hängen vom kontinuierlichen Zustand $X$ ab. Die Trennung von „Regime-Ebene" (diskret) und „Zustandsebene" (kontinuierlich) bleibt erhalten, aber die Ebenen kommunizieren: $X$ beeinflusst $Z$ (über RS.1), und $Z$ beeinflusst $X$ (über VIII.5).*

### Konkrete Regime-Übergänge

| Übergang | Schlüssel-Zustandsvariablen | Mechanismus |
|---|---|---|
| Boom $\to$ Crash | $\beta_{\text{Lev}} \cdot \text{Lev} + \beta_H \cdot \alpha_H - \beta_I \cdot \mathcal{I}$ | Hoher Leverage + Herding + wenig Information → Crash |
| Wachstum $\to$ Stagnation | $\beta_R \cdot (R_{\text{krit}} - R) + \beta_T \cdot \mathcal{T}^{-1}$ | Ressourcen knapp + Vertrauen gering → Stagnation |
| Frieden $\to$ Krise | $\beta_{\text{Gini}} \cdot \text{Gini} + \beta_w \cdot \bar{S}^{(\text{Protest})}$ | Hohe Ungleichheit + Protest-Schwelle überschritten → Krise |
| Deflation $\to$ Inflation | $\beta_M \cdot \dot{M}/M + \beta_\pi \cdot E[\pi]$ | Geldmengenwachstum + Inflationserwartungen → Regimewechsel |

### Axiometrische Eigenschaften

1. **Positivität**: $q_{ij}(X) > 0$ stets (Exponentialfunktion).
2. **Exponentielle Sensitivität**: Kleine Zustandsänderungen können große Ratenänderungen bewirken — das System ist auf Kipppunkte sensibilisiert.
3. **Kopplung an Schw.1**: Alternative Form $q_{ij}(X) = q_{ij}^{(0)} + \alpha_q \cdot \bar{S}^{(\text{Regime-}j)}(t)$, wobei die Übergangsrate direkt steigt, wenn mehr Agenten individuell die Schwelle für Regime $j$ überschritten haben.

### Spezialfälle

| Bedingung | Resultat |
|---|---|
| $\beta_m = 0\ \forall\, m$ | $q_{ij} = q_{ij}^{(0)} = \text{const}$ → VIII.4 (exogene Raten) |
| $\beta_m \to \infty$ für ein $X_m$ | Übergang wird deterministisch bei $X_m >$ Schwelle |
| $q_{ij}^{(0)} \to 0$ | Übergang im Normalzustand extrem selten; nur endogene Dynamik kann ihn auslösen |

> **Proposition 10.6 (Bottom-Up-Regime-Switching).** *RS.1 verbindet die Mikro-Ebene (individuelle Schwellenwerte, Schw.1–Schw.2) mit der Makro-Ebene (Regimewechsel, VIII.4–VIII.5). Der Transmissionskanal ist: Individuelle Schwellenwertüberschreitungen → aggregiertes $\bar{S}^{(k)}$ steigt → $q_{ij}(X)$ steigt → Regime wechselt → Parameter ändern sich (VIII.5) → alle Agenten operieren in neuem Regime. Dies ist der* Granovetter → Hamilton*-Mechanismus: individuelle Kaskaden treiben aggregierte Phasenübergänge.*

---

## §10.6 Mikro → Makro: Granovetter-Kaskaden

Die sechs Abschnitte dieses Kapitels bilden zusammen eine geschlossene Kaskaden-Architektur. In diesem letzten Abschnitt beschreiben wir den vollständigen Mechanismus — von der individuellen Entscheidung bis zum Makro-Regimewechsel — als zusammenhängenden Prozess.

### Der Mechanismus in sechs Schritten

1. **Heterogene Schwellenwerte**: Die individuellen Schwellenwerte $\theta_k^{(i)}$ sind heterogen verteilt mit Verteilung $f(\theta)$. Diese Verteilung wird durch Schw.2 endogen erzeugt — sie ist nicht exogen vorgegeben.

2. **Anstieg des Entscheidungspotentials**: Das Entscheidungspotential $\mu_k$ steigt (z.B. durch Blasenaufbau am Aktienmarkt, steigende Ungleichheit, Ressourcenknappheit).

3. **Erste Aktivierung**: Die Agenten mit den *niedrigsten* Schwellenwerten aktivieren zuerst (Schw.1: $S_i \to 1$). Diese „Pioniere" sind die am stärksten betroffenen, am wenigsten trägen, am besten informierten.

4. **Soziale Erosion**: Die Aktivierung der Pioniere senkt über Schw.2 (γ$_\theta$-Term) die Schwellenwerte der *Nachbarn*. Der Kipppunkt wandert.

5. **Kaskade oder Stabilisierung**: Wenn die Schwellenwertdichte am kritischen Punkt hoch genug ist (Proposition 10.5: $f(\bar{\theta})/\tau_k > 1$), kommt es zur *Kaskade*: Immer mehr Agenten kippen, die soziale Erosion beschleunigt sich, die Schwellenwertverteilung kollabiert. Wenn die Dichte zu niedrig ist, stoppt die Ausbreitung — lokales Ereignis, keine Kaskade.

6. **Regimewechsel**: Die aggregierte Kaskade erhöht $\bar{S}^{(k)}$ → RS.1: Die Übergangsrate $q_{ij}(X)$ steigt → VIII.4: Das System wechselt das Regime → VIII.5: Alle Parameter ändern sich. Der Mikro-Prozess (individuelle Schwellenwertüberschreitungen) hat einen *Makro-Regimewechsel* erzeugt.

### Formale Darstellung

$$\underbrace{\theta_k^{(i)} \text{ heterogen}}_{\text{Schw.2}} \xrightarrow{\mu_k \uparrow} \underbrace{S_i^{(k)} \to 1}_{\text{Schw.1, erste Agenten}} \xrightarrow{\gamma_\theta} \underbrace{\theta_k^{(j)} \downarrow}_{\text{Schw.2, Erosion}} \xrightarrow{f(\bar{\theta})/\tau > 1} \underbrace{\text{Kaskade}}_{\bar{S}^{(k)} \uparrow} \xrightarrow{q_{ij} \uparrow} \underbrace{Z \text{ wechselt}}_{\text{VIII.4 + RS.1}}$$

### Drei paradigmatische Kaskaden

| Kaskade | $\mu_k$ | $\theta_k$ | Soziale Erosion | Historisches Beispiel |
|---|---|---|---|---|
| **Bankrun** | Herding + fehlende Bankinformation | Vertrauen in die Bank | „Mein Nachbar hebt ab → ich auch" | Northern Rock (2007) |
| **Blasen-Crash** | Irrationalitätsgap $|\mu^{\text{eff}} - p|$ | Regime-Trägheit | „Alle verkaufen → ich auch" | Dotcom (2000), Subprime (2008) |
| **Revolution** | Ungleichheit + Protestaggregation | Repressionsangst | „Viele protestieren → Einzelrisiko sinkt" | Arabischer Frühling (2011) |

> **Proposition 10.7 (Notwendigkeit der Mikrofundierung).** *Ohne die Mikro-Ebene (Schw.1, Schw.2) ist Regime-Switching (VIII.4) ein reiner Ad-hoc-Mechanismus: Regime wechseln mit exogener Wahrscheinlichkeit, ohne dass das Modell erklärt, **warum**. Die Kopplung Schw.1 → Schw.2 → RS.1 → VIII.4 liefert diese Erklärung: Regimewechsel entstehen aus individuellen Schwellenwertentscheidungen, die sich über soziale Netzwerke kaskadenartig ausbreiten. Die Markov-Eigenschaft von VIII.4 ist damit nicht Axiom, sondern **Approximation**: Die tatsächliche Regime-Dynamik entsteht Bottom-Up aus Schw.1–RS.1 und ist nur im Mean-Field-Limit Markov.*

### Die Verbindung zu historischen Modellen

| Modell | Kaskaden-Element | Rolle in der Ökonoaxiomatik |
|---|---|---|
| Granovetter (1978) | Threshold Models of Collective Behavior | Schw.1 (Schwellenwert-Aktivierung) |
| Schelling (1971) | Segregationsmodell (binäre Entscheidung + Netzwerk) | Schw.1 + $A_{ij}$ (Netzwerk) |
| Watts (2002) | Small-World-Kaskaden | Netzwerktopologie bestimmt Kaskadendynamik |
| Minsky (1986) | Finanzkrise als endogene Kaskade | RS.1 (Leverage → Crash) |
| Hamilton (1989) | Regime-Switching in Konjunkturzyklen | VIII.4 (Markov-Kette) |

---

## §10.7 Abschluss: Vollständigkeit der Sprung- und Regime-Gleichungen

### Zusammenfassung der eingeführten Gleichungen

| Nr. | Name | Gleichung | Wirkung |
|---|---|---|---|
| **VIII.1** | Jump-Diffusion | $dp = \mu_p p\, dt + \sigma_p p\, dW + \int j(p,\ell)\, \tilde{N}(dt, d\ell)$ | Preissprünge über Diffusion hinaus |
| **VIII.2** | Sprungrate | $\lambda_J = \lambda_0 + \lambda_I \mathcal{I}^{-1} + \lambda_H H_{\text{herd}}$ | Wann wird gesprungen? |
| **VIII.3** | Sprungverteilung | $\ell \sim \text{Lévy}(\alpha_L, \sigma_L)$ | Wie groß ist der Sprung? |
| **VIII.4** | Regime-Switching | $Z(t) \in \{1,\dots,S\}$, $P(Z \to j) = q_{ij} \cdot dt$ | Diskrete Regime-Zustände |
| **VIII.5** | Regimeabhängiges System | $dX/dt = F^{(Z)}(X) + \Sigma^{(Z)} \xi$ | Alle Parameter regimeabhängig |
| **VIII.6** | Bankrott-Barriere | $T_{\text{bankrott}} = \inf\{t: w_i \leq 0\}$ | Irreversibles Ausscheiden |
| **VIII.7** | Kapitalsprung | $K(t^+) = K(t^-) + \Delta K_{\text{innov}}$ | Innovation und Katastrophe |
| **Schw.1** | Schwellenwert-Aktivierung | $S_i^{(k)} = \sigma((\mu_k^{(i)} - \theta_k^{(i)})/\tau_k)$ | Individuelle Kipppunkte |
| **Schw.2** | Schwellenwert-Dynamik | $\dot{\theta} = -\alpha_\theta(\theta - \bar{\theta}) + \beta_\theta \cdot \mathbb{1}[\text{fail}] - \gamma_\theta \sum A_{ij} \mathbb{1}[S_j > 0{,}5]$ | Wandernde Schwellen |
| **RS.1** | Endogene Raten | $q_{ij}(X) = q_{ij}^{(0)} \exp(\sum \beta_m X_m)$ | Zustandsabhängige Übergänge |

### Wo stehen wir?

Mit Kapitel 10 sind **alle 75 Gleichungen** des Systems eingeführt. Teil II ist vollständig.

| Subsystem | Kapitel | Gleichungen |
|---|---|---|
| Bilateral (Vermögen, Güter, Geld) | 4 | I.1–I.4, M.1–M.2, P.3, K.1 |
| Preise und Flüsse | 5 | II.1–II.4, F.1–F.2 |
| Entscheidungen | 6 | V.1–V.3, L.1–L.5, III.2–III.4, U.1–U.3, VI.1–VI.9 |
| Information | 7 | I.1–I.3, I.5, Ent.2 |
| Geld und Aggregation | 8 | M.3–M.4, E.1, P.4, V.9, IV.1–IV.4 |
| Population und Struktur | 9 | N.1–N.5, VII.1–VII.4 |
| **Sprünge und Regime** | **10** | **VIII.1–VIII.7, Schw.1–Schw.2, RS.1** |

Die Aufgabe von Teil III ist nun: zu zeigen, dass dieses Gleichungssystem *geschlossen* ist — dass es genau so viele Gleichungen wie Unbekannte besitzt, dass es stock-flow-konsistent ist, und dass es unter geeigneten Bedingungen Lösungen hat.

---

*Ende von Kapitel 10. Im folgenden Teil III (Systemschluss) zeigen wir, dass das in Teilen I und II aufgebaute Gleichungssystem vollständig, konsistent und — unter geeigneten Regularitätsbedingungen — wohlgestellt ist.*

---
---

# TEIL III — SYSTEMSCHLUSS

Die Teile I und II haben 75 Gleichungen entwickelt — von den zehn Axiomen über die bilateralen Bilanzgleichungen, die Preisdynamik, die Drei-Ebenen-Entscheidungsarchitektur, die Informationsdynamik, das Geld- und Kreditsystem, die Population und Strukturwandel bis zu den Sprung- und Regimeprozessen. Jede Gleichung wurde einzeln motiviert, axiomatisch hergeleitet und in ihren Kopplungen dargestellt.

Doch ein Gleichungssystem ist mehr als die Summe seiner Teile. Die entscheidenden Fragen sind:

1. **Ist das System geschlossen?** Gibt es genau so viele unabhängige Gleichungen wie Unbekannte — oder bleiben Variablen unbestimmt? (Kapitel 11)
2. **Ist es konsistent?** Werden die fundamentalen Erhaltungsgleichungen (Vermögen, Güter, Geld) unter allen Umständen eingehalten — auch bei Kreditschöpfung, Bankrott und Regimewechseln? (Kapitel 12)
3. **Wie ist es kausal strukturiert?** Welche Rückkopplungsschleifen treiben die Dynamik, und wo greift die Irrationalität ein? (Kapitel 13)
4. **Existieren Lösungen?** Gibt es Gleichgewichte, und sind sie stabil — oder führt das System in Chaos und Singularitäten? (Kapitel 14)

Teil III beantwortet diese vier Fragen und zeigt: Das System ist im Sinne von Hadamard *wohlgestellt* — lokal existieren Lösungen, sie sind eindeutig, und sie hängen stetig von den Anfangsbedingungen ab. Global kann das System allerdings sensitive Abhängigkeit zeigen, multiple Gleichgewichte besitzen und Regimewechsel durchlaufen. Dies ist kein Defekt der Theorie — es bildet die reale Ökonomie ab.

---

# Kapitel 11: Freiheitsgrade und Closure

Das zentrale Problem jeder umfassenden Theorie: Ist das System *geschlossen*? Ein Gleichungssystem mit $D$ Unbekannten und weniger als $D$ unabhängigen Gleichungen ist *unterbestimmt* — es gibt unendlich viele Lösungen, die Theorie sagt nichts Definitives voraus. Ein System mit mehr als $D$ unabhängigen Gleichungen ist *überbestimmt* — es gibt generisch keine Lösung, die Theorie widerspricht sich selbst. Nur ein System mit genau $D$ unabhängigen Gleichungen ist *wohl-geschlossen*.

---

## §11.1 Der Zustandsvektor: Wie viele Variablen?

Das System operiert auf einem Zustandsvektor $X(t)$, der *alle* dynamischen Variablen enthält. Wir listen ihn vollständig auf:

| Block | Variablen | Dimension | Bestimmt durch |
|---|---|---|---|
| **Mikro-Zustand** | $w_i, c_i, L_i, \theta_{ik}, \hat{p}_{ik}$ | $N(4K + 6)$ | I.1, V.1–V.3, L.1–L.4, III.2, III.4 |
| **Güterfelder** | $p_k, n_k^{(\alpha)}, m, \mathcal{I}_k$ | $6K + 2$ | II.2, P.3, M.1, I.1 (Info) |
| **Struktur** | $N_X, R_k, A_{ij}^{(\ell)}$ | $J + 5N^2$ | N.1–N.5, VII.1 |
| **Verhaltensparameter** | $\gamma_i, \beta_i, c_i^*, \zeta_i^K, \sigma_i^K, \alpha_H$ | $5N + 1$ | VI.1–VI.9 |
| **Langsame Variablen** | $\mathcal{T}, H_i, E, \kappa_{\text{eco}}$ | $N + 3$ | VII.1–VII.4 |
| **Aufmerksamkeit/Werbung** | $a_{ik}, E_{\text{adv},k}$ | $NK + K$ | I.3, I.2 |
| **Schwellenwerte/Regime** | $\theta_k^{(i)}, Z(t)$ | $NK + 1$ | Schw.2, VIII.4 |

Die Gesamtdimension ist:

$$\dim(X) = N(4K + 6) + 6K + 2 + J + 5N^2 + 5N + 1 + N + 3 + NK + K + NK + 1 \approx \mathcal{O}(N^2 + NK)$$

Für eine typische Simulation mit $N = 1000$ Agenten und $K = 6$ Güterklassen ist $\dim(X) \approx 5 \cdot 10^6$ — ein hochdimensionales System, aber numerisch handhabbar (Kapitel 24).

> **Observation 11.1 (Quadratische Skalierung).** *Die Dimension des Zustandsvektors skaliert wie $\mathcal{O}(N^2)$, nicht wie $\mathcal{O}(N)$. Der Grund: Die Netzwerkmatrix $A_{ij}$ hat $N^2$ Einträge (auf jeder der 5 Schichten). Dies ist der Preis der axiomatisch geforderten heterogenen Interaktionsstruktur — und der Grund, warum Mean-Field-Approximationen (Kapitel 8) für die numerische Praxis unverzichtbar sind.*

---

## §11.2 Die 75 Gleichungen: Unabhängigkeit und Summationsidentitäten

Das System umfasst 75 Gleichungen. Doch nicht alle sind unabhängig — die Erhaltungsgleichungen sind durch *Summationsidentitäten* verknüpft:

| Identität | Gleichungen | Relation |
|---|---|---|
| Aggregierte Vermögenserhaltung | I.1 $\to$ I.2 | $\sum_i \dot{w}_i = \dot{W}$ — I.2 folgt aus Summation über I.1 |
| Güteraggregation | P.3 individuell $\to$ aggregiert | $\sum_\alpha \dot{n}_k^{(\alpha)} = \dot{N}_k$ |
| Geldaggregation | M.1 individuell $\to$ aggregiert | $\sum_i \dot{m}_i = \dot{M}$ |
| BIP-Identität | V.9 | $Y \equiv C + I + G + NX$ — definitorisch, keine dynamische Gleichung |

Vier der 75 Gleichungen sind somit *nicht unabhängig* — sie folgen aus Summation über die individuellen Bilanzgleichungen. Die Zahl der unabhängigen dynamischen Gleichungen ist:

$$\text{Unabhängige Gleichungen} = 75 - 4 - 1 = 70$$

(die $-1$ kommt von V.9, die eine reine Definitionsgleichung ist, keine dynamische).

> **Proposition 11.1 (Freiheitsgrad-Zählung).** *Das System besitzt $\dim(X) \approx \mathcal{O}(N^2 + NK)$ dynamische Variablen und 70 unabhängige dynamische Gleichungen. Die Gleichungen bestimmen die **Dynamik** (Zeitableitungen $\dot{X}$) aller Variablen. Was nicht bestimmt ist: die **Anfangsbedingungen** $X(0)$ und die **Parameter** ($\gamma_0, \alpha_\theta, \lambda_0, \dots$). Das System ist dynamisch geschlossen — gegeben Anfangsbedingungen und Parameter, ist die Trajektorie $X(t)$ für $t > 0$ vollständig bestimmt.*

---

## §11.3 Die Closure-Tabelle

Die Closure-Tabelle zeigt auf einen Blick, welches Subsystem welche Variable schließt:

| Subsystem | Bestimmende Gleichungen | Geschlossene Variable(n) | Benötigte Inputs |
|---|---|---|---|
| **Konsum** | V.1–V.3, Schw.1 | $c_i(t)$ | $p_k, \mathcal{I}_i, w_i, A_{ij}$ |
| **Arbeit** | L.1–L.4, Schw.1 | $L_i(t)$ | $w_L, \mathcal{I}_i^{\text{job}}, A_{ij}$ |
| **Produktion** | III.3, P.3 | $Y_k(t), q_k(t)$ | $K_k, L_k, R_k, \mathcal{I}_k$ |
| **Preise** | II.2 | $p_k(t)$ | $D_k(c_i), S_k(q_k)$ |
| **Kapital** | III.4, K.1 | $K(t), \lambda_{\alpha\beta}^*$ | $r_K, p_\alpha, p_\beta$ |
| **Geld** | M.1, VI.1 | $M(t), r(t)$ | $\pi, Y$, Taylor-Regel |
| **Information** | I.1–I.3 | $\mathcal{I}_k(t), a_{ik}$ | $E_{\text{adv}}, A_{\max}$ |
| **Vermögen** | I.1 | $w_i(t)$ | $r, L_i, c_i, T_i$ |
| **Population** | N.1–N.2, Schw.1 | $N_X(t)$ | $w_L^{(\text{lokal})}, \theta_{\text{Mig}}$ |
| **Regime** | VIII.4, RS.1 | $Z(t)$ | $X(t), \bar{S}^{(k)}$ |

> **Observation 11.2 (Zirkuläre Closure).** *Die Closure ist **zirkulär**, nicht hierarchisch: Konsum braucht Preise, Preise brauchen Konsum (über Excess Demand). Vermögen braucht Konsum, Konsum braucht Vermögen. Information braucht Werbung, Werbung braucht Profit, Profit braucht Preise, Preise brauchen Information (über Gewichte). Jede Variable wird durch Gleichungen bestimmt, die wiederum andere Variablen als Input benötigen. Das System ist **simultan** — es kann nicht rekursiv gelöst werden, Subsystem für Subsystem.*

### Visualisierung der zirkulären Closure

```
Konsum (V.1-V.3) ←── Preise (II.2)
       │                    ↑
       ↓                    │
Gütersenke (P.3) ──→ Excess Demand
       │                    ↑
       ↓                    │
Vermögen (I.1) ────→ Arbeit/Produktion (L.1, III.3)
       │                    ↑
       ↓                    │
Geld (M.1) ────────→ Investition (III.4)
       │                    ↑
       ↓                    │
Info (I.1) ────────→ Erwartungen (III.4)
```

---

## §11.4 Was bleibt offen: Anfangsbedingungen und Parameterwahl

Das Gleichungssystem bestimmt die *Dynamik* — die Zeitableitungen aller Variablen. Es bestimmt **nicht**:

### 1. Anfangsbedingungen $X(0)$

Die Lösung des Systems erfordert einen vollständig spezifizierten Anfangszustand: Vermögen aller Agenten, Güterbestände, Preise, Informationsfeld, Schwellenwerte, Netzwerkstruktur. In einer empirischen Anwendung wird $X(0)$ durch historische Daten gegeben.

### 2. Parameterwerte

Alle Gleichungen enthalten Parameter ($\gamma_0, \alpha_\theta, \lambda_0, \sigma_L, \dots$), deren numerische Werte kalibriert oder geschätzt werden müssen. Die *qualitativen* Vorhersagen der Theorie (Existenz von Blasen, Kaskaden, Ungleichheitsdrift) hängen nicht von den Parameterwerten ab — sie folgen aus der Struktur der Gleichungen. Die *quantitativen* Vorhersagen (Wann genau kippt der Markt? Wie hoch steigt die Ungleichheit?) sind parameterabhängig.

### 3. Funktionale Formen

Die Gleichungen enthalten Funktionen ($u(c), F(K,L), C(\mathcal{I}), \dots$), die nicht spezifiziert, sondern nur durch *axiomatische Eigenschaften* eingeschränkt sind. Die Wahl der funktionalen Form ist eine **Modellierungsentscheidung**, keine axiomatische Notwendigkeit.

---

## §11.5 Axiomatisch vs. Modellierungswahl: Die Baukastenlogik

Die Trennung zwischen dem, was die Theorie *vorschreibt*, und dem, was der Anwender *wählt*, ist das Grundprinzip der axiomatischen Methode. Wir formalisieren sie hier:

### Was ist axiomatisch (unveränderlich)?

| Zusammenhang | Axiomatische Eigenschaft | Formale Bedingung |
|---|---|---|
| Informationskosten $C(\mathcal{I})$ | Existenz, Positivität, Monotonie, Konvexität | $C > 0,\ C' > 0,\ C'' > 0$ |
| Nutzenfunktion $u(c)$ | Existenz, Monotonie, Konkavität | $u' > 0,\ u'' < 0$ |
| Produktionsfunktion $F(K,L)$ | Monotonie, abnehmende Grenzerträge, Inada | $F_K > 0,\ F_{KK} < 0,\ F(0,L) = 0$ |
| Arbeitsleid $\varphi(L)$ | Konvexität (Grenzleid wächst) | $\varphi' > 0,\ \varphi'' > 0$ |
| Informationsgewichte $\omega(\mathcal{I})$ | Summe 1, monoton in $\mathcal{I}$ | $\sum \omega = 1,\ \partial\omega/\partial\mathcal{I} > 0$ |

### Was ist Modellierungswahl (austauschbar)?

| Gleichung | Gewählte Form | Alternativen |
|---|---|---|
| Infokosten (A10) | $c_0 + c_1 \mathcal{I} + c_2 \mathcal{I}^2$ | $c_0 \exp(\lambda \mathcal{I})$, $c_0/(1 - \mathcal{I}/\mathcal{I}_{\max})$ |
| Nutzen (U.1) | CRRA: $c^{1-\gamma}/(1-\gamma)$ | CARA: $-\exp(-\alpha c)$, Log: $\ln c$ |
| Produktion (III.3) | Cobb-Douglas: $AK^\alpha L^\beta$ | CES: $A[\alpha K^\rho + (1-\alpha) L^\rho]^{1/\rho}$ |
| Word-of-Mouth (I.1) | Logistisch: $\mathcal{I}(1 - \mathcal{I})$ | Gompertz: $\mathcal{I} \ln(\mathcal{I}_{\max}/\mathcal{I})$ |

> **Proposition 11.2 (Struktur-Form-Separation).** *Die **strukturellen** Vorhersagen der Theorie (Existenz von Blasen, Kaskadeneffekte, Ungleichheitsdrift, Fisher-Spirale, Minsky-Zyklen) hängen **nur von den axiomatischen Eigenschaften** der Funktionen ab — nicht von ihrer konkreten Form. Man benötigt keine Cobb-Douglas-Funktion, um Solow-Konvergenz zu zeigen; jede $F$ mit $F''>0$, $F''<0$, Inada genügt. Die **quantitativen** Vorhersagen (Konvergenzgeschwindigkeit, Krisentiefe, Ungleichheitsniveau) hängen von der gewählten Form und den kalibrierten Parametern ab.*

### Die Baukasten-Architektur

```
              AXIOMATISCHE STRUKTUR (Teil I+II, unveränderlich)
                         ↓
          75 Gleichungen mit axiomatischen Eigenschaften
                         ↓
         ┌───────────────┼───────────────┐
         ↓               ↓               ↓
   Funktionale Form  Parameter    Anfangsbedingungen
   (aus Anhang C)    (Kalibrierung)  (Daten)
         ↓               ↓               ↓
         └───────────────┼───────────────┘
                         ↓
              KONKRETES MODELL (quantitativ, falsifizierbar)
```

Der Anwender wählt aus dem *Baukasten* (Anhang C) die funktionalen Formen, kalibriert die Parameter an Daten, spezifiziert die Anfangsbedingungen — und erhält ein konkretes, simulierbares, falsifizierbares Modell. Die Theorie gibt die Struktur; der Anwender füllt die Formen.

---

## §11.6 Vollständigkeitstest

Woher wissen wir, dass das System *vollständig* ist — dass keine wesentlichen Gleichungen fehlen?

> **Definition 11.1 (Fundamentale Vollständigkeit).** *Ein Gleichungssystem ist **fundamental vollständig**, wenn es die folgenden fünf Kriterien erfüllt:*

| Nr. | Kriterium | Prüfung | Ergebnis |
|---|---|---|---|
| 1 | **Observable-Abdeckung** | Jede messbare ökonomische Größe (BIP, Inflation, Gini, Arbeitslosigkeit, ...) ist Funktion von $X(t)$ | ✓ |
| 2 | **Kausale Geschlossenheit** | Keine dynamische Variable bleibt unbestimmt (keine „freien" Gleichungen) | ✓ (Closure-Tabelle) |
| 3 | **Hadamard-Bedingungen** | Existenz, Eindeutigkeit, stetige Abhängigkeit (lokal) | ✓ (Kapitel 14) |
| 4 | **Erhaltungskonsistenz** | Alle Erhaltungsgleichungen A1–A3 sind konsistent | ✓ (Kapitel 12) |
| 5 | **Spezialfall-Abdeckung** | Alle bekannten validierten Modelle sind Grenzfälle | ✓ (Teil IV) |

Die Vollständigkeit ist dabei im Hadamard'schen Sinne gemeint — *strukturelle* Vollständigkeit. Das System kann keine exogenen Schocks „vorhersagen" (Wetter, Pandemie, Krieg), und die genauen Parameterwerte müssen empirisch kalibriert werden. Was es kann: Gegeben Anfangsbedingungen und Parameter, die gesamte endogene Dynamik *abbilden*.

---

*Ende von Kapitel 11. Im folgenden Kapitel prüfen wir die Stock-Flow-Konsistenz: Ob die Bilanz- und Flussrelationen unter allen Umständen erfüllt sind.*

---

# Kapitel 12: Stock-Flow-Konsistenz

Die Erhaltungsgleichungen A1–A3 (Vermögenserhaltung, Gütererhaltung, Gelderhaltung) sind das Fundament des Systems. Werden sie verletzt, bricht die gesamte Theorie zusammen: Es entstünde Vermögen aus dem Nichts, Güter verschwänden, Geld materialisiere sich ohne Kreditvorgang. Die Frage der *Stock-Flow-Konsistenz* (SFC) geht über die einzelnen Erhaltungsgleichungen hinaus: Sie prüft, ob das Gesamtsystem — über alle Sektoren, alle Transaktionen, alle Zeitpunkte — die Bilanzrelationen einhält.

Die SFC-Analyse folgt der Tradition von Godley-Lavoie (2007) und Tobin (1982): Jede Transaktion wird in einer Bilanzmatrix (Bestände) und einer Flussmatrix (Transaktionen) erfasst. Die zentrale Prüfung: *Jede Zeile summiert sich korrekt. Jede Spalte summiert sich korrekt.*

---

## §12.1 Die Bilanzmatrix (Bestandsmatrix)

Die Bilanzmatrix erfasst alle Bestände der fünf Sektorklassen ($\mathcal{W}$: Haushalte, $\mathcal{U}$: Firmen, $\mathcal{B}$: Banken, $\mathcal{G}$: Staat, $\mathcal{Z}$: Ausland):

| Aktiva/Passiva | Haushalte $\mathcal{W}$ | Firmen $\mathcal{U}$ | Banken $\mathcal{B}$ | Staat $\mathcal{G}$ | Ausland $\mathcal{Z}$ | $\Sigma$ |
|---|---|---|---|---|---|---|
| $\mathbb{K}_1$: Sachkapital | $+K_{\mathcal{W}}$ | $+K_{\mathcal{U}}$ | — | $+K_{\mathcal{G}}$ | — | $K$ |
| $\mathbb{K}_2$: Land, Gold | $+n_2^{\mathcal{W}}$ | $+n_2^{\mathcal{U}}$ | — | $+n_2^{\mathcal{G}}$ | — | $N_2$ |
| $\mathbb{K}_3$: Konsumgüter | — | $+n_3^{\mathcal{U}}$ (Lager) | — | — | — | $N_3$ |
| $\mathbb{K}_4$: Patente, IP | $+n_4^{\mathcal{W}}$ | $+n_4^{\mathcal{U}}$ | — | — | — | $N_4$ |
| $\mathbb{K}_5$: Geld/Deposits | $+M_{\mathcal{W}}$ | $+M_{\mathcal{U}}$ | $-D$ (Verbindl.) | $-B_{\mathcal{G}}$ (Schuld) | $\pm \text{NFA}$ | $0^*$ |
| $\mathbb{K}_6$: Information | $+\mathcal{I}_{\mathcal{W}}$ | $+\mathcal{I}_{\mathcal{U}}$ | — | $+\mathcal{I}_{\mathcal{G}}$ | — | $\mathcal{I}$ |
| Kredite | $-L_{\mathcal{W}}$ | $-L_{\mathcal{U}}$ | $+L$ (Forderung) | — | — | $0$ |
| Eigenkapital | $+\text{EK}$ | $-\text{EK}$ | — | — | — | $0$ |
| **Nettovermögen** | $w_{\mathcal{W}}$ | $w_{\mathcal{U}}$ | $w_{\mathcal{B}}$ | $w_{\mathcal{G}}$ | $w_{\mathcal{Z}}$ | $W$ |

> **Observation 12.1 (Monetäre Nettonull).** *Die Zeile $\mathbb{K}_5$ (Geld/Deposits) summiert sich zu Null ($^*$): Jedes Guthaben ist die Verbindlichkeit eines anderen Sektors. Geld entsteht durch Kreditschöpfung (M.1): $\dot{M} = g_Z + g_B \cdot \text{Kredit} - \tau_{\mathcal{G}}$. Die Nettosumme aller monetären Forderungen und Verbindlichkeiten ist identisch Null — dies ist die fundamentale SFC-Konsistenz des Geldsystems.*

> **Observation 12.2 (Reale Netto-Positivität).** *Die physischen Bestände ($\mathbb{K}_1$–$\mathbb{K}_4$, $\mathbb{K}_6$) summieren sich **nicht** zu Null: Sachkapital, Güter, Informationen existieren als realer Reichtum. Die Gesamtwirtschaft kann `netto` reicher werden — durch Produktion. Sie wird netto ärmer durch Konsum, Abschreibung und Katastrophen. Die monetäre Sphäre (Null-Summe) und die reale Sphäre (positiver Nettowert) folgen verschiedenen Logiken.*

---

## §12.2 Die Flussmatrix (Transaktionsflüsse)

Die Flussmatrix erfasst alle Transaktionen pro Zeiteinheit:

| Transaktion | $\mathcal{W}$ | $\mathcal{U}$ | $\mathcal{B}$ | $\mathcal{G}$ | $\mathcal{Z}$ | $\Sigma$ |
|---|---|---|---|---|---|---|
| Konsum $C$ | $-C$ | $+C$ | — | — | — | $0$ |
| Investition $I$ | — | $-I$ | — | — | — | $-I$ |
| Staatsausgaben $G$ | — | $+G$ | — | $-G$ | — | $0$ |
| Exporte $X$ | — | $+X$ | — | — | $-X$ | $0$ |
| Importe $\text{IM}$ | — | $-\text{IM}$ | — | — | $+\text{IM}$ | $0$ |
| Löhne $w_L$ | $+w_L$ | $-w_L$ | — | — | — | $0$ |
| Profite $\Pi$ | $+\Pi$ | $-\Pi$ | — | — | — | $0$ |
| Steuern $T$ | $-T_{\mathcal{W}}$ | $-T_{\mathcal{U}}$ | — | $+T$ | — | $0$ |
| Zinsen auf Kredite | $-r_L L_{\mathcal{W}}$ | $-r_L L_{\mathcal{U}}$ | $+r_L L$ | — | — | $0$ |
| Zinsen auf Deposits | $+r_D D_{\mathcal{W}}$ | $+r_D D_{\mathcal{U}}$ | $-r_D D$ | — | — | $0$ |
| Kreditschöpfung (M.1) | — | $+\Delta L$ | $-\Delta L + \Delta D$ | — | — | $\Delta M$ |
| Info-Investition (I.2) | — | $-E_{\text{adv}}$ | — | — | — | $-E_{\text{adv}}$ |
| **Saldo (Sparen)** | $S_{\mathcal{W}}$ | $S_{\mathcal{U}}$ | $S_{\mathcal{B}}$ | $S_{\mathcal{G}}$ | $S_{\mathcal{Z}}$ | $\equiv I$ |

### Konsistenz-Checks

1. **Zeilensummen**: Alle reinen Transfers summieren sich zu Null (Geld wechselt den Sektor, verschwindet aber nicht). Nur Investition ($-I$), Kreditschöpfung ($\Delta M$) und Info-Investition ($-E_{\text{adv}}$) verändern den aggregierten Bestand.
2. **Spaltensummen**: Das Sparen jedes Sektors $S_X$ ist die Differenz zwischen Einkommen und Ausgaben — identisch mit der Bestandsänderung $\dot{w}_X$.
3. **VGR-Identität**: Die letzte Zeile ergibt $\sum S_X \equiv I$ — gesamtwirtschaftliches Sparen gleich Investition (die Fundamentalidentität der VGR).

> **Proposition 12.1 (SFC-Konsistenz).** *Jede Transaktion in der Flussmatrix entspricht einem Term in den Gleichungen I.1–I.4 und M.1. Die Zeilensummen-Bedingung (jeder Transfer ist null-summig) folgt direkt aus der bilateralen Struktur von I.1: $\dot{w}_i = \sum_j [\text{Zuflüsse} - \text{Abflüsse}]$. Die Spaltensummen-Bedingung (Sparen = Bestandsänderung) folgt aus der Definition des Sparens als Residuum. Das Gleichungssystem ist **konstruktionsbedingt** stock-flow-konsistent.*

---

## §12.3 Quellen und Senken

Nicht alle Transaktionen sind null-summig. Das System hat *echte* Quellen (Wertschöpfung) und Senken (Vernichtung):

| Quelle/Senke | Variable | Gleichung | Null-summig? |
|---|---|---|---|
| Güterproduktion (Quelle) | $n_k \uparrow$ | P.3: $+q_k$ | Nein — erzeugt Netto-Wert (BWS) |
| Güterkonsum (Senke) | $n_k \downarrow$ | P.3: $-c_k$ | Nein — vernichtet Wert |
| Abschreibung (Senke) | $n_k \downarrow$ | P.3: $-\delta_k n_k$ | Nein — irreversibel |
| Kreditschöpfung (Q+S) | $M \uparrow, L \uparrow$ | M.1 | **Ja** — $\Delta M = \Delta L$ (netto null) |
| Konversion (Q+S) | $n_k^\alpha \downarrow, n_k^\beta \uparrow$ | K.1, P.4 | Nein — $\Pi \neq 0$ (Mehrwert möglich) |
| Info-Produktion (Quelle) | $\mathcal{I}_k \uparrow$ | I.1: $+\sigma_{\text{adv}} E_{\text{adv}}$ | Nein — nicht-rivales Gut |
| Info-Zerfall (Senke) | $\mathcal{I}_k \downarrow$ | I.1: $-\omega \mathcal{I}_k$ | Nein — irreversibel |
| Katastrophe (Senke) | $n_k, K, N \downarrow$ | VIII.7, Ent.2 | Nein — exogene Vernichtung |

> **Observation 12.3 (Einzige null-summige Quelle).** *Die **einzige** Transaktion mit perfekter Bilanz-Symmetrie ist die Kreditschöpfung: Jedes Guthaben erzeugt eine gleich große Schuld ($\Delta M = \Delta L$). Alle anderen Quellen und Senken erzeugen netto positive oder negative Wertänderungen. Dies ist der fundamentale Unterschied zwischen der **realen** Sphäre (Produktion schafft Wert, Konsum vernichtet ihn) und der **monetären** Sphäre (Geld entsteht und verschwindet paarweise).*

---

## §12.4 Prüfung: Werden A1–A3 je verletzt?

Die Erhaltungsgleichungen gelten *exakt* — sie sind Axiome, keine Approximationen. Aber: In bestimmten Situationen *scheinen* sie verletzt zu werden. Die SFC-Matrix zeigt, dass die scheinbare Verletzung stets durch eine kompensatorische Transaktion aufgefangen wird:

| Scheinbare Verletzung | SFC-Zeile | Gleichgewichtsmechanismus | Instabilitätsmechanismus |
|---|---|---|---|
| Handelsdefizit ($NX < 0$) | Export–Import | Wechselkursanpassung | Kapitalzufluss → Schuldenaufbau |
| Schuldenspirale ($\dot{b}/b > r$) | Kreditzeile | Haushaltsdisziplin ($T \uparrow$) | Fisher: $p \downarrow \to b/W \uparrow$ |
| Vermögensblase ($p_K \gg p_K^*$) | Eigenkapitalzeile | Mean-Reversion (II.2) | Herding: $\alpha_H > \alpha_H^{\text{krit}}$ |
| Geldmengenexplosion ($\dot{M}/M > g$) | Kreditschöpfung | Taylor-Regel (VI.1: $r \uparrow$) | Liquiditätsfalle ($r \to 0$) |
| Infomonopol ($\mathcal{I}_A \gg \mathcal{I}_B$) | Info-Zeile | Diffusion ($D\nabla^2 \mathcal{I}$) | Exklusion ($r_k = 1$: Ausschließbarkeit) |

> **Proposition 12.2 (Erhaltung unter Symmetriebrechung).** *Die Erhaltungsgleichungen A1–A3 gelten im Gleichungssystem **exakt und zu jeder Zeit**. Sie können „scheinen", verletzt zu werden, wenn man nur einen Sektor betrachtet (ein Sektor kann netto sparen oder verschulden). Aber die Summe über alle Sektoren ist stets null-summig (A1: $\sum \dot{w}_i = \dot{Y} - \dot{C}$). Die einzigen Situationen, in denen Erhaltung im erweiterten Sinne „bricht", sind Quantitative Easing ($g_Z$ nicht sterilisiert, A3 gilt aber weiterhin: die Zentralbankbilanz erweitert sich auf beiden Seiten) und Fiskaltransfers (Redistribution ändert die Verteilung, nicht die Summe).*

---

*Ende von Kapitel 12. Im folgenden Kapitel analysieren wir die kausale Struktur des Systems — die Rückkopplungsschleifen, die die Dynamik treiben.*

---

# Kapitel 13: Kausalstruktur

Die Closure-Tabelle (Kapitel 11) zeigt, welche Gleichung welche Variable bestimmt. Doch Closure ist nicht Kausalität. Die zentrale Frage ist: *Wie treiben die Variablen einander an?* Welche Rückkopplungsschleifen erzeugen stabile Gleichgewichte, und welche erzeugen explosive Dynamik?

Das Gleichungssystem enthält fünf fundamentale Kausalketten. Jede Kette ist ein geschlossener Kreislauf — die letzte Variable beeinflusst die erste. Drei der fünf Ketten sind *potenziell instabil*: Unter bestimmten Parameterbedingungen erzeugen sie selbstverstärkende Dynamik (Blasen, Spiralen, Kaskaden). Zwei sind *strukturell stabil* — sie besitzen eingebaute Dämpfungsmechanismen.

---

## §13.1 Die fünf fundamentalen Rückkopplungsschleifen

### Schleife 1: Der Konsum-Handels-Kreislauf

$$\text{V.1–V.3}\ (c_i) \longrightarrow \text{P.3}\ (\dot{n}_k < 0) \longrightarrow \text{II.2}\ (p_k \uparrow) \longrightarrow \nabla\mu_{\text{eff}} \longrightarrow \text{F.1}\ (j_{nk} \to \text{Import}) \longrightarrow \text{Handelsdefizit} \longrightarrow \text{Wechselkurs} \longrightarrow c_i$$

Konsum reduziert den lokalen Güterbestand → Preis steigt → Import-Gradient entsteht → Güter fließen ein (Handelsdefizit) → Wechselkurs passt sich an → Importgüter werden teurer → Konsum wird gedämpft.

**Stabilität**: Strukturell stabil. Der Wechselkurs-Mechanismus wirkt als *negativer Feedback*: Übermäßiger Konsum erzeugt Handelsdefizite, die über den Wechselkurs den Konsum drosseln.

### Schleife 2: Der Arbeits-Produktions-Kreislauf

$$\text{L.1–L.4}\ (L_i) \longrightarrow \text{III.3}\ (q_k \uparrow) \longrightarrow \text{P.3}\ (\dot{n}_k > 0) \longrightarrow \text{II.2}\ (p_k \downarrow) \longrightarrow w_L \longrightarrow \text{L.1} \longrightarrow L_i$$

Arbeit produziert Güter → Güterbestand steigt → Preis fällt → Lohn passt sich an → Arbeitsangebot wird angepasst.

**Stabilität**: Strukturell stabil. Die Euler-Bedingung L.1 ($w_L u'(c) = \varphi'(L)$) wirkt als Dämpfung — steigende Arbeit erzeugt steigendes Grenzleid, das das Arbeitsangebot begrenzt.

### Schleife 3: Der Investitions-Kapital-Kreislauf

$$\text{L.5}\ (\Pi_i^{\text{erw}} > 0) \longrightarrow K \uparrow \longrightarrow r_K\ (\text{E.1}) \longrightarrow \text{Kapitalfluss}\ (\text{F.1}) \longrightarrow \text{III.3}\ (Y \uparrow) \longrightarrow \Pi \longrightarrow \text{L.5}$$

Erwarteter Gewinn → Investition → Kapitalstock steigt → Produktion steigt → Profit → mehr Investition.

**Stabilität**: Stabil unter Solow-Bedingungen ($F'' < 0$: abnehmende Grenzerträge). Instabil bei *Overconfidence* ($E[R]$ überschätzt) oder bei konstantem Grenzertrag ($\alpha = 1$: AK-Modell).

### Schleife 4: Der Information-Werbung-Kreislauf

$$\text{I.2}\ (E_{\text{adv}}) \longrightarrow \text{I.1}\ (\mathcal{I}_k \uparrow) \longrightarrow \text{U.2}\ (\omega_k \uparrow) \longrightarrow \text{Nachfrage} \uparrow \longrightarrow \text{II.2}\ (p_k \uparrow) \longrightarrow \Pi \uparrow \longrightarrow \text{I.2}\ (E_{\text{adv}} \uparrow)$$

Werbung erhöht Information → Nachfragegewichte steigen → Preis steigt → Profit steigt → mehr Werbung.

**Stabilität**: *Potenziell instabil*. Die Schleife ist selbstverstärkend — jeder Werbekreisel kann sich aufschaukeln. Begrenzt durch: (a) Informationskosten $C(\mathcal{I})$ sind konvex (A10), (b) Aufmerksamkeitsbeschränkung I.3 ($\sum a_{ik} \leq A_{\max}$), (c) Information zerfällt ($-\omega \mathcal{I}$).

### Schleife 5: Der Geldschöpfungs-Kreislauf

$$\text{VI.1}\ (r \downarrow) \longrightarrow \text{M.1}\ (M \uparrow) \longrightarrow \text{E.1}\ (\text{niedrigerer } r) \longrightarrow I \uparrow \longrightarrow Y \uparrow \longrightarrow \pi \uparrow \longrightarrow \text{VI.1}\ (r \uparrow)$$

Zinssenkung → Kreditschöpfung → Geldmenge steigt → Investition steigt → BIP steigt → Inflation steigt → Taylor-Regel erhöht Zins.

**Stabilität**: Stabil unter Taylor-Prinzip ($\partial r / \partial \pi > 1$). Instabil bei Liquiditätsfalle ($r \to 0$, kein Spielraum nach unten) oder bei passiver Geldpolitik.

---

## §13.2 Zusammenfassung: Stabilität und Instabilität

| Schleife | Gleichungskette | Feedback-Typ | Stabilitätsbedingung |
|---|---|---|---|
| 1. Konsum-Handel | V.1 → P.3 → II.2 → F.1 → $c_i$ | Negativ | Stets stabil (Wechselkurs als Dämpfer) |
| 2. Arbeit-Produktion | L.1 → III.3 → P.3 → II.2 → L.1 | Negativ | Stets stabil (Euler-Dämpfung) |
| 3. Investition-Kapital | L.5 → III.3 → I.2 → L.5 | Positiv/Negativ | Stabil für $F'' < 0$; instabil bei Overconfidence |
| 4. Information-Werbung | I.2 → I.1 → U.2 → II.2 → I.2 | Positiv | Kann instabil werden; begrenzt durch I.3, A10 |
| 5. Geld-Kredit | VI.1 → M.1 → E.1 → Y → VI.1 | Negativ | Stabil unter Taylor-Prinzip |

> **Proposition 13.1 (Drei Instabilitätsquellen).** *Das System hat drei potenzielle Instabilitätsquellen, die alle zur Drei-Ebenen-Architektur (Kapitel 6) gehören:*
>
> *(a) **Herding** ($\alpha_H > \alpha_H^{\text{krit}}$): Die Preis-Herding-Schleife (II.2 ↔ III.2 ↔ III.4) erzeugt selbstverstärkende Blasen. Der kritische Herding-Parameter ist $\alpha_H^{\text{krit}} = \lambda(\gamma\sigma^2 - \eta)$.*
>
> *(b) **Informationskollaps** ($\mathcal{I} \to 0$): Der Term $-\varphi_k/(\mathcal{I} + \varepsilon)$ in II.2 erzeugt eine Pol-Singularität. Bei $\mathcal{I} \to 0$ divergieren die Transaktionskosten → Liquiditätskollaps.*
>
> *(c) **Schulden-Deflation** ($b/W$ groß, $\dot{p} < 0$): Die Fisher-Spirale — Deflation erhöht den realen Schuldenstand, was weitere Deflation erzeugt. Begrenzt nur durch VIII.6 (Bankrott als absorbierende Barriere).*

---

## §13.3 Wo Irrationalität eingreift

In jeder der fünf Kausalketten gibt es mindestens einen Punkt, an dem die *Irrationalität* (Ebene 2: psychologische Verzerrungen, Ebene 3: soziale Kopplung) in die ansonsten rationale Dynamik (Ebene 1) eingreift:

| Kette | Rationaler Pfad | Irrationalitäts-Eingriff |
|---|---|---|
| 1 (Konsum) | $c_i$ aus Euler-Gleichung V.1 | Herding (V.3): $c_i$ folgt Peers, nicht Euler |
| 2 (Arbeit) | $L_i$ aus Grenzleid $=$ Grenznutzen (L.1) | Burnout, Statusdruck (L.2, L.3) |
| 3 (Investition) | $\Pi_i > 0$ entscheidet rational (L.5) | Overconfidence: $E[R]$ systematisch überschätzt |
| 4 (Information) | Rationale Werbung (I.2 Dorfman-Steiner) | Info-Herding: alle werben für dasselbe Gut |
| 5 (Geld) | Taylor-Regel (VI.1) | Reflexivität: Markt antizipiert Regel → Regel wird ineffektiv |

> **Observation 13.1 (Konsistente Irrationalität).** *Die Irrationalität propagiert durch den gesamten Kreislauf. Herding im Konsum (V.3) verzerrt die Nachfrage → verzerrte Preise (II.2) → verzerrte Investitionssignale (III.4) → verzerrte Kapitalallokation → verzerrte Löhne → verzerrter Konsum. Das System ist **konsistent irrational** — nicht nur punktuell verzerrt, sondern durchgängig. Die Drei-Ebenen-Architektur (Kapitel 6) stellt sicher, dass die Irrationalität **additiv** eingekoppelt wird: Ebene 2 und 3 modifizieren Ebene 1, ersetzen sie aber nicht.*

---

## §13.4 Warum das System simultan ist

Ein *rekursives* System kann sequentiell gelöst werden: Zuerst Variable 1, dann Variable 2 (die von 1 abhängt), dann Variable 3 (die von 1 und 2 abhängt), und so weiter. Ein *simultanes* System kann nicht sequentiell gelöst werden — alle Variablen müssen gleichzeitig bestimmt werden.

Das ökonoaxiomatische System ist *simultan*. Der Beweis ist einfach: Die Closure-Tabelle (§11.3) zeigt, dass jedes Subsystem Inputs von anderen Subsystemen benötigt, die wiederum Inputs vom ersten Subsystem benötigen. Es gibt keine Hierarchie — kein Subsystem ist „zuerst" bestimmt.

> **Proposition 13.2 (Simultanität).** *Das System I–VIII + Schw + RS besitzt keine kausale Ordnung (topologische Sortierung), in der jede Variable nur von bereits bestimmten Variablen abhängt. Der Kreislauf Konsum → Preise → Vermögen → Konsum allein reicht, um Rekursivität auszuschließen. Die Lösung erfordert die simultane Integration des gesamten ODE/SDE-Systems — numerisch realisiert durch Euler-Maruyama, Milstein oder Runge-Kutta-Verfahren mit implizitem Gleichungslöser (→ Kapitel 24).*

### Das effektive Potential als Propagationskanal

Die Simultanität hat eine elegante Darstellung über das *effektive Potential* (F.2, Kapitel 5):

$$\mu_k^{\text{eff}}(x,t) = \underbrace{p_k(x,t)}_{\text{Marktpreis}} + \underbrace{\alpha_H \cdot \bar{p}_k^{\text{Herding}}}_{\text{Herding-Verzerrung}} + \underbrace{\frac{\psi_k}{\mathcal{I}_k(x,t) + \varepsilon}}_{\text{Transaktionskosten}}$$

Güter, Kapital und Geld fließen nicht dorthin, wo der *objektive* Preis am höchsten ist, sondern dorthin, wo das *wahrgenommene* Potential am höchsten ist. Ein überbewerteter Markt mit starkem Herding zieht *trotzdem* Kapital an — weil $\mu^{\text{eff}} > p$ durch den Herding-Term. Dies ist der formale Mechanismus, durch den Irrationalität die Preise, die Flüsse und die Allokation *simultan* verzerrt.

---

*Ende von Kapitel 13. Im folgenden Kapitel untersuchen wir die mathematischen Eigenschaften des Systems: Existenz, Eindeutigkeit und Stabilität der Lösungen.*

---

# Kapitel 14: Existenz, Eindeutigkeit und Stabilität

Die bisherigen Kapitel von Teil III haben die *Struktur* des Systems analysiert: Freiheitsgrade, Konsistenz, Kausalität. Kapitel 14 befasst sich mit der *mathematischen Wohlgestelltheit*: Existieren Lösungen? Sind sie eindeutig? Sind sie stabil?

Die Standardreferenz ist Hadamard (1902): Ein Problem ist *wohlgestellt* (well-posed), wenn es (1) eine Lösung besitzt, (2) die Lösung eindeutig ist, und (3) die Lösung stetig von den Anfangsbedingungen abhängt. Wir prüfen jede der drei Bedingungen.

---

## §14.1 Das System als gekoppelte SDE

Das Gesamtsystem lässt sich kompakt schreiben als:

$$dX = F^{(Z(t))}(X)\, dt + \Sigma^{(Z(t))}(X)\, dW + J(X)\, d\tilde{N}$$

wobei:
- $X$ der Zustandsvektor ist ($\dim(X) \approx \mathcal{O}(N^2)$)
- $F^{(Z)}$ die regimeabhängige Drift (deterministische Dynamik)
- $\Sigma^{(Z)}$ die regimeabhängige Diffusion (stochastische Fluktuationen)
- $J$ die Sprungkomponente (VIII.1, VIII.7)
- $Z(t)$ der diskrete Regime-Zustand (VIII.4)
- $dW$ der Wiener-Prozess
- $d\tilde{N}$ das kompensierte Poisson-Maß

---

## §14.2 Existenz

> **Proposition 14.1 (Lokale Existenz).** *Wenn die Drift $F^{(Z)}$ lokal Lipschitz-stetig ist und die Diffusion $\Sigma^{(Z)}$ beschränkt, dann existiert für jeden Anfangswert $X(0) \in \mathbb{R}^D$ eine **lokale** Lösung $X(t)$ für $t \in [0, T_{\max})$ (Picard-Lindelöf/Itô-Existenzsatz).*

Die Lipschitz-Bedingung ist für die meisten Terme des Systems erfüllt: Die Produktionsfunktion III.3, die Konsumgleichungen V.1–V.3, die Populationsdynamik N.1–N.5 sind glatte Funktionen. Zwei Stellen erfordern besondere Aufmerksamkeit:

| Kritischer Term | Gleichung | Problem | Regularisierung |
|---|---|---|---|
| $\varphi_k / (\mathcal{I}_k + \varepsilon)$ | II.2 | Pol bei $\mathcal{I} \to 0$ | $\varepsilon > 0$ (bereits eingebaut) |
| Endogene Parameter VI.1–VI.9 | VI | Lipschitz-Bedingung muss geprüft werden | Beschränkte Parameteränderungsraten |

> **Proposition 14.2 (Globale Existenz).** *Die Lösung existiert **global** ($T_{\max} = \infty$), wenn der Zustandsvektor beschränkt bleibt. Beschränkende Terme im System:*
> - $n_k \geq 0$ *(Positivität der Güterbestände — Nichtnegativitätsbedingung)*
> - $c_i \geq c_i^{\min} > 0$ *(Existenzminimum — NB.1)*
> - $N \leq \kappa$ *(Tragfähigkeitsgrenze — N.3)*
> - *Information ist logistisch gesättigt (obere Schranke $\mathcal{I}_{\max}$)*
> - *Vermögen wird durch Bankrott (VIII.6) bei $w_i = 0$ absorbiert, nicht bei $w_i = -\infty$*
>
> *Diese Terme definieren eine **invariante Region** $\mathcal{D} \subset \mathbb{R}^D$, die der Zustandsvektor nicht verlässt.*

---

## §14.3 Eindeutigkeit

> **Proposition 14.3 (Lokale Eindeutigkeit).** *Unter der Lipschitz-Bedingung ist die Lösung **lokal eindeutig** — verschiedene Anfangsbedingungen führen zu verschiedenen Trajektorien, und keine Trajektorie gabelt sich.*

Für das Gesamtsystem mit Regime-Switching (VIII.4) gilt: Innerhalb jedes Regimes $Z = z$ ist das System ein glattes SDE, für das die Eindeutigkeit durch Lipschitz gesichert ist. An den Regimeübergängen gabelt sich die Trajektorie *scheinbar* — aber die stochastischen Terme ($dW$, $d\tilde{N}$) machen die Lösung als *starke* SDE-Lösung fast sicher eindeutig.

> **Observation 14.1 (Multiple Regime-Pfade).** *Zwei identische Anfangsbedingungen können zu verschiedenen Regime-Sequenzen führen — das System ist **pfadabhängig**. Dies ist nicht Verletzung der Eindeutigkeit, sondern Konsequenz der Stochastik: Die Lösung ist eindeutig für jede Realisation des Zufalls $(\omega)$, aber verschiedene Realisationen führen zu verschiedenen Regime-Historien.*

---

## §14.4 Stetige Abhängigkeit und Sensitivität

> **Proposition 14.4 (Stetige Abhängigkeit in glatten Regimen).** *Innerhalb eines Regimes $Z = z$ (ohne Sprünge) hängt die Lösung stetig von den Anfangsbedingungen ab: Kleine Änderungen in $X(0)$ erzeugen kleine Änderungen in $X(t)$ für endliche $t$. Dies folgt aus der Grönwall-Ungleichung.*

An Regimeübergängen und Kipppunkten bricht die stetige Abhängigkeit *kontrolliert*:

> **Observation 14.2 (Sensitive Abhängigkeit nahe Kipppunkten).** *In der Nähe eines Kipppunkts (Granovetter-Schwelle: $f(\bar{\theta})/\tau > 1$, Proposition 10.5) kann eine infinitesimale Änderung in $X(0)$ darüber entscheiden, ob eine Kaskade ausgelöst wird oder nicht. Das System zeigt **sensitive Abhängigkeit** — die Hallmark von Chaos. Dies ist kein Defekt der Theorie: Es bildet die empirische Realität ab, in der kleine Auslöser (ein einziger Bankrott, ein Tweet, ein Gerücht) Finanzkrisen auslösen können.*

---

## §14.5 Steady-State-Analyse

### Definition

$$\text{Steady State}: \quad \dot{X}^* = 0 \quad (\text{deterministischer Teil, } \xi = 0)$$

### Existenz für geschlossene Volkswirtschaft

Für eine geschlossene Volkswirtschaft ($\nabla \cdot j = 0$) existieren Steady-State-Bedingungen:

| Nr. | Bedingung | Gleichung | Interpretation |
|---|---|---|---|
| SS.1 | $K^* = \left(\frac{sA}{n + \delta}\right)^{1/(1-\alpha)} L$ | III.3, I.2 | Solow-Steady-State des Kapitalstocks |
| SS.2 | $\mathcal{I}^* = S/\omega$ | I.1 | Informationsfeld-Gleichgewicht |
| SS.3 | $p^* = MC(q^*)$ | II.2 | Walrasianisches Preisgleichgewicht |
| SS.4 | $r^* = \beta + \gamma g$ | E.1 | Natürlicher Zins (Ramsey-Regel) |

> **Proposition 14.5 (Solow-Attraktor).** *Der Solow-Steady-State SS.1 ist **stabil**: Der dominante Eigenwert der Jacobi-Matrix ist $\lambda_1 = (\alpha - 1)(n + \delta) < 0$ (da $\alpha < 1$). Kleine Abweichungen vom Steady State werden exponentiell gedämpft. Die Konvergenzrate ist $|\lambda_1| = (1 - \alpha)(n + \delta)$, typischerweise $\sim 2$–$5\%$ pro Jahr (konsistent mit der empirischen Konvergenzliteratur: Barro-Sala-i-Martin 1992).*

### Stabilität: Jacobi-Analyse

Die lokale Stabilität des Steady State $X^*$ wird durch die Eigenwerte der Jacobi-Matrix $J = \partial F / \partial X \big|_{X^*}$ bestimmt:

| Eigenwert-Konfiguration | Stabilitätstyp | Ökonomisches Beispiel |
|---|---|---|
| $\text{Re}(\lambda_i) < 0\ \forall\, i$ | Stabiler Knoten/Fokus | Walras-GG, Solow-GG |
| $\exists\, i: \text{Re}(\lambda_i) > 0$ | Instabil (Sattelpunkt) | Minsky vor Crash |
| $\text{Re}(\lambda_i) = 0$ | Bifurkation (Phasenübergang) | $\alpha_H = \alpha_H^{\text{krit}}$ |

### Offene Volkswirtschaft

Für die offene Volkswirtschaft existiert generisch *kein globaler Steady State* — die räumliche Heterogenität (verschiedene Länder, verschiedene Ressourcen, verschiedene Institutionen) verhindert einen einheitlichen Ruhezustand. Stattdessen existiert ein *statistisches Gleichgewicht*: eine stationäre Verteilung $f_\infty(X)$, die die Fokker-Planck-Gleichung

$$\frac{\partial f}{\partial t} = -\nabla \cdot (F \cdot f) + \frac{1}{2} \nabla^2 (\Sigma^2 \cdot f) = 0$$

löst. Hinreichende Bedingung: Hypoelliptizität des Diffusionsoperators + Existenz einer Lyapunov-Funktion.

---

## §14.6 Bifurkationen und Chaos

### Herding-Bifurkation

Die zentrale Bifurkation des Systems liegt im Herding-Parameter $\alpha_H$:

$$\alpha_H^{\text{krit}} = \lambda(\gamma\sigma^2 - \eta)$$

| $\alpha_H$ | Dynamik | Ökonomisch |
|---|---|---|
| $< \alpha_H^{\text{krit}}$ | Gedämpfte Zyklen, stabile Konvergenz | Effiziente Märkte (näherungsweise) |
| $= \alpha_H^{\text{krit}}$ | Hopf-Bifurkation: Grenzzykel entsteht | Endogener Konjunkturzyklus (Minsky) |
| $> \alpha_H^{\text{krit}}$ | Explosive Spirale → Crash (begrenzt durch VIII.6) | Blasen-Crash-Dynamik |

### Informations-Singularität

Der Term $\varphi_k / (\mathcal{I}_k + \varepsilon)$ in II.2 erzeugt eine deterministische Singularität bei $\mathcal{I} \to 0$:

$$\ddot{p} \propto -\varphi / \mathcal{I}^2 \to -\infty$$

Dies ist der *Informationskollaps*: Wenn die Information eines Marktes auf Null fällt, divergieren die Transaktionskosten → der Markt wird illiquide → Preise sind undefiniert. Die Regularisierung $\varepsilon > 0$ verhindert die mathematische Singularität, modelliert aber die ökonomische Realität: Selbst im schlimmsten Fall bleibt ein Minimum an Information (der letzte Transaktionspreis).

### Kramers-Escape-Rate

In der stochastischen Version des Systems ist die Frage nicht *ob*, sondern *wann* ein Crash kommt. Die Kramers-Escape-Rate gibt die mittlere Wartezeit bis zum Verlassen eines metastabilen Zustands:

$$\tau_{\text{escape}} \sim \exp\!\left(\frac{2\Delta V}{\sigma^2}\right)$$

wobei $\Delta V$ die Potentialbarriere und $\sigma^2$ die Noise-Amplitude ist. Die Crash-Wartezeit ist *exponentiell lang* für kleine Noise — aber endlich. Jeder metastabile Zustand (Blase, Schuldenspirale, politische Stabilität) wird irgendwann verlassen.

---

## §14.7 Offene mathematische Probleme

Trotz der nachgewiesenen lokalen Wohlgestelltheit bleiben fundamentale mathematische Fragen offen:

| Nr. | Problem | Status | Was fehlt |
|---|---|---|---|
| O6 | Globale Existenz und Eindeutigkeit | Offen | Regularisierung der $\varphi/\mathcal{I}$-Singularität + Lipschitz für VI |
| O7 | Vollständige Bifurkationsklassifikation | Teilgelöst | Minsky $=$ Hopf (bewiesen); Codim-2-Analyse fehlt |
| O8 | Stochastische Ergodentheorie | Offen | Wann existiert $f_\infty$? Hinreichend: Hypoelliptizität + Lyapunov |

> **Observation 14.3 (Ehrlichkeit über Grenzen).** *Die offenen Probleme O6–O8 sind nicht spezifisch für die Ökonoaxiomatik — sie betreffen jedes hochdimensionale nichtlineare stochastische System. Die Navier-Stokes-Gleichungen (Millennium-Problem) haben dieselben offenen Fragen. Der Unterschied: Für die Navier-Stokes-Gleichungen sind die Gleichungen seit 180 Jahren bekannt. Für die Ökonomik formuliert diese Monographie erstmals ein System, das überhaupt die Frage nach globaler Existenz stellt.*

---

## §14.8 Abschluss: Wo stehen wir?

Teil III hat vier Fragen beantwortet:

| Frage | Kapitel | Antwort |
|---|---|---|
| Ist das System geschlossen? | 11 | Ja — 70 unabhängige Gleichungen für $\mathcal{O}(N^2)$ Variablen; Closure ist simultan, nicht rekursiv |
| Ist es konsistent? | 12 | Ja — SFC ist konstruktionsbedingt erfüllt; A1–A3 gelten exakt zu jeder Zeit |
| Wie ist es kausal strukturiert? | 13 | 5 fundamentale Schleifen; 3 potenziell instabil (Herding, Info-Kollaps, Fisher); Irrationalität ist systemisch |
| Existieren Lösungen? | 14 | Lokal ja (Picard-Lindelöf); global offen; stabil nahe Solow-GG; chaotisch nahe Kipppunkten |

Das System ist im Sinne von Hadamard *lokal wohlgestellt*. Global zeigt es die volle Komplexität nichtlinearer dissipativer Systeme: multiple Gleichgewichte, Regime-Switching, sensitive Abhängigkeit, langfristige Pfadabhängigkeit. Dies ist keine Schwäche — es ist der Grund, warum die Ökonomik keine einfache Physik ist.

Im folgenden Teil IV zeigen wir, dass die bekannten ökonomischen Modelle — von Solow über Arrow-Debreu bis Minsky — als *Spezialfälle* des allgemeinen Systems entstehen.

---

*Ende von Kapitel 14 und Teil III. Im folgenden Teil IV (Katalog der Spezialfälle) leiten wir systematisch ab, welche bekannten Modelle als Grenzfälle des allgemeinen Systems entstehen.*

---
---

# TEIL IV — KATALOG DER SPEZIALFÄLLE

## Methodisches Prinzip

Teil IV hat eine einzige Aufgabe: zu zeigen, dass die bekannten ökonomischen Modelle — Solow, Ramsey, Arrow-Debreu, IS-LM, CAPM, Minsky, Piketty und viele andere — als *Grenzfälle* des allgemeinen Systems emergieren. Dies ist der ultimative Konsistenztest: Wenn das allgemeine System korrekt ist, *muss* jedes validierte Modell als Spezialfall enthalten sein.

Die Methode ist in jedem Fall identisch und folgt strikt der Richtung **allgemein → speziell**:

> **Protokoll für jeden Grenzübergang:**
>
> 1. **Ausgangspunkt**: Das volle 75-Gleichungssystem in allgemeiner Form (Teil II)
> 2. **Vereinfachungsannahmen**: Explizite Parametersetzungen ($\alpha_H = 0$, $N = 1$, $\mathcal{I} \to \infty$, ...)
> 3. **Elimination**: Welche Gleichungen verschwinden, welche Terme fallen weg?
> 4. **Reduktion**: Das verbleibende System Schritt für Schritt vereinfachen
> 5. **Identifikation**: Die resultierende Gleichung mit dem historischen Modell vergleichen
> 6. **Was geht verloren?**: Welche Phänomene kann das reduzierte Modell *nicht* beschreiben?

Wir beginnen *niemals* vom bekannten Modell und zeigen rückwärts, dass es „irgendwie" drinsteckt. Wir beginnen *immer* vom allgemeinen System und lassen es Schritt für Schritt kollabieren — bis das bekannte Modell als mathematische Konsequenz vor uns liegt.

---

# Kapitel 15: Wachstumstheorie

Die Wachstumstheorie fragt: Wie entwickelt sich eine Volkswirtschaft langfristig? Seit Solow (1956) ist die Antwort an eine einzige Gleichung geknüpft — die Fundamentalgleichung der Kapitalakkumulation. Wir zeigen, dass diese Gleichung aus dem allgemeinen System emergiert, wenn man genügend Komplexität entfernt.

---

## §15.1 Solow (1956): Exogene Sparquote, ein Gut, ein Agent

### Schritt 1: Das volle System

Wir starten mit dem vollständigen Zustandsvektor $X(t)$ und allen 75 Gleichungen. Für die Wachstumstheorie sind die relevanten Gleichungen:

- **I.1** (individuelle Vermögensbilanz): $\dot{w}_i = y_i - c_i + \sum_k \theta_{ik} \dot{p}_k + r_i^b b_i - T_i$
- **I.2** (aggregierte Vermögenserhaltung): $\dot{W} = Y - C$
- **III.3** (Produktionsfunktion): $q_k = F_k(K_k, L_k, R_k, \mathcal{I}_k)$ mit $F_K > 0, F_{KK} < 0$
- **V.1–V.3** (Konsum, drei Ebenen): $\dot{c}_i = R_i c_i + \Psi_c(\cdot) + \Phi_c(\cdot)$
- **N.1–N.2** (Population): $\dot{N}_X = g_X N_X + M_X + C_X$
- **VI.6** (Technologiedynamik): $\dot{A} = \theta_A A - \delta_A A + s_A Y$
- **IV.1–IV.4** (Aggregation): Boltzmann-Transport für $f(w, \theta, \mathcal{I}, t)$

### Schritt 2: Vereinfachungsannahmen

Wir setzen systematisch:

| Annahme | Formal | Konsequenz |
|---|---|---|
| **Ein repräsentativer Agent** | $N = 1$ (Mean-Field-Limit IV.3: $\text{Var} \to 0$) | IV.1–IV.4 entfallen; alle Agenten identisch |
| **Ein Gut** | $K = 1$ (eine Güterklasse $\mathbb{K}_1$) | Alle Summationen $\sum_k$ verschwinden |
| **Kein Herding** | $\alpha_H = 0$ | V.3 (Herding) $\to 0$; III.2 wird rein nutzenbasiert |
| **Keine Psychologie** | V.2 $\equiv 0$ ($\Psi_c = 0$) | Ebene 2 entfällt: kein Referenzpunkt, keine Verlustasymmetrie |
| **Keine Information** | $\mathcal{I} \to \infty$ überall | I.1–I.3, I.5, Ent.2 entfallen; U.3: $p^{\text{eff}} \to p$; U.2: $\omega \to 1/K = 1$ |
| **Homogene Präferenzen** | $\gamma_i = \gamma,\ \beta_i = \beta$ | VI.1–VI.9 entfallen (Parameter konstant) |
| **Exogene Sparquote** | $c = (1-s)Y$, $s = \text{const}$ | V.1 wird zur Identität, nicht zur Euler-Gleichung |
| **Kein Geld** | $m \equiv 0$ | M.1–M.4 entfallen; rein reale Ökonomie |
| **Keine Sprünge** | VIII.1–VIII.7, Schw.1, Schw.2, RS.1 $\equiv 0$ | Gesamte Gruppe VIII + Schwellenwerte entfallen |
| **Keine Netzwerke** | $A_{ij} = 0$ | V.6–V.8 entfallen |
| **Exogene Bevölkerung** | $\dot{N} = nN$, $n = \text{const}$ | N.1–N.5 reduzieren sich auf eine Konstante |
| **Exogene Technologie** | $\dot{A} = gA$, $g = \text{const}$ | VI.6 wird zur Identität |

### Schritt 3: Elimination

Von den 75 Gleichungen *überleben* nach diesen Annahmen genau drei:

| Überlebende Gleichung | Allgemeine Form | Reduzierte Form |
|---|---|---|
| **I.2** (Bilanz) | $\dot{W} = Y - C$ | $\dot{K} = Y - C = sY$ (da $W \equiv K$, $C = (1-s)Y$) |
| **III.3** (Produktion) | $q = F(K, L, R, \mathcal{I})$ | $Y = AK^\alpha L^\beta$ (Modellierungswahl: Cobb-Douglas) |
| **N.2** (Population) | $\dot{N} = nN$ | $L = L_0 e^{nt}$ |

Alle anderen 72 Gleichungen sind entweder identisch erfüllt (z.B. I.1 = I.2 bei $N=1$), trivial ($0 = 0$), oder durch die Annahmen ausgeschaltet.

### Schritt 4: Reduktion

Wir setzen III.3 in I.2 ein:

$$\dot{K} = sY - \delta K = s \cdot A K^\alpha L^\beta - \delta K$$

Division durch $L$ und Definition des Pro-Kopf-Kapitalstocks $k = K/L$:

$$\dot{k} = \frac{\dot{K}}{L} - nk = sAk^\alpha - (n + \delta)k$$

### Schritt 5: Identifikation

$$\boxed{\dot{k} = sAk^\alpha - (n + \delta)k}$$

Dies ist *exakt* die Fundamentalgleichung von Solow (1956, QJE, Gl. 7). Der Steady State folgt aus $\dot{k} = 0$:

$$k^* = \left(\frac{sA}{n + \delta}\right)^{1/(1-\alpha)}$$

Die Konvergenzrate (aus Linearisierung um $k^*$) ist $\lambda_1 = (1 - \alpha)(n + \delta)$, typischerweise $\sim 2\text{–}5\%$ pro Jahr (Barro-Sala-i-Martin 1992).

### Schritt 6: Was geht verloren?

| Verloren | Gleichung | Ökonomisches Phänomen |
|---|---|---|
| Heterogenität | IV.1–IV.4 | Ungleichheit, Vermögensverteilung |
| Informationsasymmetrie | I.1–I.3, U.2–U.3 | Fehlallokation, Lemons |
| Herding | V.3, III.2 ($\alpha_H$) | Blasen, Crash |
| Geld | M.1–M.4 | Inflation, Liquiditätsfalle |
| Regimewechsel | VIII.1–VIII.7 | Krisen, Sprünge |
| Entscheidungspsychologie | V.2 | Loss Aversion, Habit |

> **Proposition 15.1 (Solow-Emergenz).** *Das Solow-Modell emergiert aus dem allgemeinen System unter 12 simultanen Vereinfachungen. 72 der 75 Gleichungen werden trivial. Die Fundamentalgleichung $\dot{k} = sAk^\alpha - (n+\delta)k$ ist eine mathematische Konsequenz der aggregierten Bilanzgleichung I.2 bei exogener Sparquote, einem Gut, einem repräsentativen Agenten und abnehmenden Grenzerträgen ($\alpha < 1$). Keine der 12 Annahmen ist axiomatisch — alle sind Vereinfachungen, die jederzeit aufgehoben werden können.*

---

## §15.2 Ramsey-Cass-Koopmans (1928/1965): Optimaler Konsum

Der Ramsey-Grenzfall unterscheidet sich vom Solow-Grenzfall in *genau einer* Annahme: Die Sparquote ist nicht exogen, sondern folgt aus *intertemporaler Nutzenmaximierung*.

### Schritt 1–2: Gleiche Ausgangsbasis, eine Annahme weniger

Wir übernehmen *alle* Solow-Annahmen *außer* der exogenen Sparquote. Stattdessen bleibt die Konsumgleichung V.1 in ihrer allgemeinen Form aktiv:

$$\dot{c}_i = R_i \cdot c_i$$

wobei $R_i$ die allgemeine rationale Konsumregel aus V.1 ist (Kapitel 6). Im allgemeinen System ist:

$$R_i = \frac{r_i^{\text{wahr}} - \beta_i}{\gamma_i} + \text{Vorsichtssparen} + \text{Liquiditätsprämie} + \dots$$

### Schritt 3: Elimination unter Ramsey-Annahmen

Unter den Solow-Annahmen ($N=1$, $K=1$, $\alpha_H = 0$, $\mathcal{I} \to \infty$, keine Psychologie) vereinfacht sich $R_i$ drastisch:

- Kein Herding ($\alpha_H = 0$) → kein sozialer Term
- Keine Informationskosten ($\mathcal{I} \to \infty$) → kein Vorsichtssparen aus Unwissen
- Keine Psychologie ($\Psi_c = 0$) → kein Referenzpunkt-Effekt
- Homogene Präferenzen ($\gamma_i = \gamma$, $\beta_i = \beta$) → einheitliche Parameter
- Der wahrgenommene Zins $r_i^{\text{wahr}}$ wird zum realen Zins $r$ (keine Verzerrung)

Es bleibt:

$$R = \frac{r - \beta}{\gamma}$$

### Schritt 4: Reduktion

V.1 wird zu:

$$\frac{\dot{c}}{c} = \frac{r - \beta}{\gamma}$$

wobei $r = F'(k) - \delta$ (Grenzprodukt des Kapitals, aus III.3 und E.1). Zusammen mit I.2:

$$\dot{k} = f(k) - c - (n + \delta)k$$

### Schritt 5: Identifikation

$$\boxed{\frac{\dot{c}}{c} = \frac{r - \rho}{\gamma}, \qquad \dot{k} = f(k) - c - (n + \delta)k}$$

Dies ist *exakt* das Ramsey-Cass-Koopmans-System (Ramsey 1928, EJ; Cass 1965, RES; Koopmans 1965), wobei $\rho \equiv \beta$ die Zeitpräferenzrate ist und $\gamma$ die relative Risikoaversion (= inverse Substitutionselastizität).

### Schritt 6: Was geht verloren (relativ zu Solow)?

Nichts — im Gegenteil, Ramsey ist *strikt allgemeiner* als Solow: Die Sparquote ist endogen. Was relativ zum *allgemeinen System* verloren geht, ist identisch mit der Solow-Liste ($§15.1$, Schritt 6).

> **Proposition 15.2 (Ramsey-Emergenz).** *Die Euler-Gleichung $\dot{c}/c = (r - \rho)/\gamma$ emergiert aus V.1 (allgemeine rationale Konsumregel) unter den Annahmen: ein Agent, ein Gut, keine Information, keine Psychologie, kein Herding. Sie ist der einfachste nicht-triviale Spezialfall der Drei-Ebenen-Konsumarchitektur — Ebene 1 allein, ohne Ebene 2 und 3.*

---

## §15.3 AK-Modell: Endogenes Wachstum ohne abnehmende Grenzerträge

### Ausgangspunkt: Solow-Reduktion

Wir starten beim bereits reduzierten Solow-System ($\dot{k} = sAk^\alpha - (n+\delta)k$) und ändern *eine einzige Annahme*:

$$\alpha = 1 \qquad (\text{konstante Grenzerträge des Kapitals})$$

### Reduktion

$$\dot{K} = sAK - \delta K = (sA - \delta)K$$

Division durch $K$:

$$\frac{\dot{K}}{K} = sA - \delta = g = \text{const}$$

### Identifikation

$$\boxed{\frac{\dot{K}}{K} = sA - \delta}$$

Konstante Wachstumsrate, kein Steady-State-*Niveau* (der Steady State aus §15.1 divergiert: $k^* = (sA/(n+\delta))^{1/(1-\alpha)} \to \infty$ für $\alpha \to 1$).

### Was geht verloren?

Die Solow-Konvergenz ($\lambda_1 = (1-\alpha)(n+\delta) \to 0$ für $\alpha \to 1$): Arme Länder holen reiche *nicht* ein. Das AK-Modell erklärt persistente Wachstumsratenunterschiede, kann aber keine Konvergenz abbilden.

---

## §15.4 Romer (1990): Endogene Technologie

### Ausgangspunkt: Das Solow-System *plus* die Technologiegleichung

Im Solow-Modell ist $A$ exogen ($\dot{A} = gA$). Romer endogenisiert $A$ durch eine *Wissensproduktionsfunktion*. Im allgemeinen System ist die Technologiegleichung VI.6:

$$\dot{A} = \theta_A A - \delta_A A + s_A Y$$

### Vereinfachungsannahmen (zusätzlich zu Solow)

- Keine Romer-spezifischen Vereinfachungen nötig — VI.6 ist bereits *in der allgemeinen Form* das Romer-Modell
- $\theta_A A$: "Standing on Shoulders" (Wissensexternalität — neues Wissen baut auf altem auf)
- $s_A Y$: F&E-Investitionsanteil des BIP
- $\delta_A A$: Wissenszerfall (Veraltung)

### Reduktion

Das Solow-System wird erweitert durch:

$$\dot{k} = s_K A k^\alpha - (n + \delta)k, \qquad \dot{A} = (\theta_A - \delta_A) A + s_A A k^\alpha$$

wobei $s_K = s - s_A$ der physische Sparanteil und $s_A$ der F&E-Anteil ist.

### Identifikation

Die langfristige Wachstumsrate ist endogen:

$$g = \theta_A - \delta_A + s_A \frac{Y}{A}$$

Dies ist strukturell äquivalent zu Romer (1990, JPE): Wachstum wird durch F&E-Investition ($s_A$) und Wissensexternalitäten ($\theta_A$) getrieben, nicht durch exogenen technischen Fortschritt.

> **Proposition 15.3 (Endogenes Wachstum als Aktivierung von VI.6).** *Der Übergang von Solow zu Romer erfordert keine neue Gleichung — nur die **Aktivierung** einer bereits vorhandenen (VI.6). Im Solow-Modell ist VI.6 zur Identität $\dot{A} = gA$ degeneriert; im Romer-Modell ist sie eine vollwertige dynamische Gleichung. Die Ökonoaxiomatik enthält endogenes Wachstum als **optionalen Freiheitsgrad**, nicht als Erweiterung.*

---

### Zusammenfassung: Wachstumstheorie als Schichtmodell

```
ALLGEMEINES SYSTEM (75 Gleichungen)
    │
    │ setze: N=1, K=1, α_H=0, I→∞, keine Psychologie,
    │        kein Geld, keine Sprünge, keine Netzwerke
    ↓
RAMSEY (3 Gl.: I.2, V.1, III.3)  ─── endogenes c(t)
    │
    │ setze: c = (1−s)Y (exogene Sparquote)
    ↓
SOLOW (2 Gl.: I.2, III.3)  ─── K̇ = sY − δK
    │                    │
    │ setze: α = 1       │ aktiviere VI.6
    ↓                    ↓
AK-MODELL               ROMER
K̇/K = sA − δ           Ȧ = θA + s_A Y
```

---

# Kapitel 16: Allgemeines Gleichgewicht

Die Gleichgewichtstheorie sucht einen Zustand, in dem alle Märkte simultan geräumt sind — Angebot gleich Nachfrage für jedes Gut. Arrow und Debreu (1954) bewiesen die Existenz eines solchen Gleichgewichts unter bestimmten Bedingungen. Wir zeigen: Dieses Gleichgewicht ist ein *Fixpunkt* des allgemeinen Systems — der Punkt, an dem alle Zeitableitungen verschwinden.

---

## §16.1 Arrow-Debreu (1954): Allgemeines Gleichgewicht

### Schritt 1: Das volle System

Das System besteht aus 75 gekoppelten Differentialgleichungen. Ein Gleichgewicht ist definiert als:

$$X^* \text{ mit } \dot{X}\big|_{X = X^*} = 0$$

### Schritt 2: Vereinfachungsannahmen

| Annahme | Formal | Konsequenz |
|---|---|---|
| **Perfekte Information** | $\mathcal{I}(x,t) \to \infty$ überall | U.3: $p^{\text{eff}} \to p$ (keine Transaktionskosten); U.2: $\omega \to 1/K$ (Gleichgewichtung); I.1–I.3, I.5, Ent.2 entfallen |
| **Kein Herding** | $\alpha_H = 0$ | V.3 $\to 0$; III.2: $\dot{\theta}_{ik} = \lambda_\theta \partial u / \partial\theta_{ik}$ (rein nutzenbasiert) |
| **Kein Noise** | $\sigma = 0$ (alle stochastischen Terme) | Deterministisches System |
| **Stationarität** | $\dot{p} = 0,\ \dot{c} = 0,\ \dot{\theta} = 0$ | Alle Zeitableitungen Null |
| **Keine Sprünge, Regime** | VIII $\equiv 0$, Schw $\equiv 0$, RS $\equiv 0$ | Kein Regime-Switching |

### Schritt 3: Elimination — Was passiert mit jeder Gleichungsgruppe?

Wir gehen systematisch durch das gesamte System:

**Gruppe I (Erhaltung)**:
- I.1 stationär ($\dot{w}_i = 0$): $y_i = c_i + T_i$ — jeder Agent konsumiert sein Einkommen nach Steuern
- I.2 stationär ($\dot{W} = 0$): $Y = C$ — aggregierter Output gleich aggregierter Konsum

**Gruppe II (Preise/Flüsse)**:
- II.2 stationär ($\dot{p}_k = 0$): Die Preisdynamik $\dot{p}_k = \lambda_k^{-1}(D_k - S_k) + \eta_k p_k - \varphi_k/(\mathcal{I} + \varepsilon)$ wird zu:
  - $\eta_k p_k = 0$ (keine Inflationserwartung im GG) und $\varphi_k/(\mathcal{I}+\varepsilon) \to 0$ (perfekte Info)
  - Es bleibt: $0 = \lambda_k^{-1}(D_k - S_k)$, also:

$$D_k(p^*) = S_k(p^*) \qquad \forall\, k = 1, \dots, K$$

- F.2 stationär: $\mu^{\text{eff}} = p$ (effektives Potential = Marktpreis, da Herding = 0 und $\mathcal{I} \to \infty$)
- F.1: Keine Nettoflüsse im GG ($j = 0$)

**Gruppe III (Verhalten)**:
- III.2 stationär ($\dot{\theta}_{ik} = 0$): $\lambda_\theta \partial u / \partial\theta_{ik} = 0$ → Portfolio-Optimalität (FOC)
- III.3 stationär: $q_k^* = F_k(K_k^*, L_k^*, R_k^*, \mathcal{I}_k)$ — Produktion bei optimalen Inputs
- III.4: Erwartungen sind korrekt (im GG fallen Erwartungen und Realisation zusammen)

**Gruppe IV (Aggregation)**: Bei identischen Agenten ($\text{Var} \to 0$) trivial.

**Gruppen V–VIII**: Entfallen komplett.

### Schritt 4: Das verbleibende System

Es bleiben:

| Bedingung | Gleichung | Interpretation |
|---|---|---|
| Markträumung | $D_k(p^*) = S_k(p^*) \ \forall\, k$ | Walras-Gleichgewicht |
| Nutzenmaximierung | $\partial u / \partial\theta_{ik} = 0$ | Portfolio-FOC |
| Budgetbeschränkung | $p \cdot x_i \leq p \cdot \omega_i$ | Walras-Budget |
| Profitmaximierung | $p = MC(q^*)$ | Null-Profit-Bedingung |

### Schritt 5: Identifikation

$$\boxed{\exists\, p^* \in \mathbb{R}_{++}^K : D_k(p^*) = S_k(p^*) \quad \forall\, k}$$

Dies ist *exakt* die Definition des Arrow-Debreu-Gleichgewichts (Arrow-Debreu 1954). Die Existenz folgt aus dem Brouwer'schen Fixpunktsatz, angewandt auf die überschüssige Nachfragefunktion $z(p) = D(p) - S(p)$.

### Schritt 6: Was geht verloren?

| Verloren | Durch welche Annahme | Konsequenz |
|---|---|---|
| Preisdynamik | $\dot{p} = 0$ | Keine Anpassungsprozesse, kein Tâtonnement |
| Informationsasymmetrie | $\mathcal{I} \to \infty$ | Kein Akerlof, kein Grossman-Stiglitz |
| Herding, Blasen | $\alpha_H = 0$ | Keine Fehlbewertung |
| Heterogenität | $\text{Var} \to 0$ | Keine Verteilungseffekte |
| Geld | entfällt | Reale Ökonomie, kein nominaler Effekt |

> **Proposition 16.1 (Arrow-Debreu als Fixpunkt).** *Das Arrow-Debreu-Gleichgewicht ist der **Fixpunkt** $\{X^* : \dot{X}|_{X^*} = 0\}$ des allgemeinen Systems unter den Annahmen perfekter Information, keines Herdings, keiner Stochastik und Stationarität. Jede Abweichung von diesen Annahmen — endliche Information, positives Herding, Stochastik, Nicht-Stationarität — erzeugt Dynamik, die über das Arrow-Debreu-Modell hinausgeht. Arrow-Debreu ist nicht die allgemeine Theorie — es ist der spezielle Ruhezustand.*

---

## §16.2 Walras-Tâtonnement: Dynamik zum Gleichgewicht

Das Tâtonnement ist die *Dynamik*, die zum Arrow-Debreu-Fixpunkt führt. Im allgemeinen System ist es ein Spezialfall der Preisgleichung II.2.

### Ausgangspunkt: II.2 in allgemeiner Form

$$\dot{p}_k = \lambda_k^{-1}(D_k - S_k) + \eta_k p_k - \frac{\varphi_k}{\mathcal{I}_k + \varepsilon}$$

### Vereinfachungen

- $\eta_k = 0$: Keine Inflationserwartung
- $\varphi_k = 0$: Keine Illiquiditätsprämie (perfekte Information)
- $\alpha_H = 0$: Kein Herding (Nachfrage $D_k$ ist nicht durch Peers verzerrt)

### Reduktion

$$\dot{p}_k = \lambda_k^{-1}(D_k(p) - S_k(p))$$

### Identifikation

Dies ist *exakt* der Walrasianische Tâtonnement-Prozess (Walras 1874): Preise steigen bei Überschussnachfrage ($D > S$), fallen bei Überschussangebot ($D < S$), und konvergieren zum Gleichgewicht $D = S$.

> **Observation 15.1 (II.2 enthält Tâtonnement und mehr).** *Die allgemeine Preisgleichung II.2 ist eine dreiteilige Superposition: Walras-Tâtonnement ($\lambda^{-1}(D-S)$) + Inflationserwartung ($\eta p$) + Illiquiditätsprämie ($-\varphi/(\mathcal{I}+\varepsilon)$). Das Tâtonnement ist der erste Term allein. Die Instabilitäten, die Walras nicht erfassen kann — Blasen ($\eta > 0$ durch Herding), Informationskollaps ($\mathcal{I} \to 0$) — liegen in den anderen beiden Termen.*

---

# Kapitel 17: Makroökonomik

---

## §17.1 IS-LM (Hicks 1937)

### Schritt 1: Das volle System

Für die makroökonomische Kurzfristanalyse sind relevant:
- **I.2**: $\dot{W} = Y - C$
- **V.1**: Konsumgleichung (Drei-Ebenen)
- **III.3**: Produktionsfunktion
- **M.1**: Geldschöpfung
- **I.4**: Gelderhaltung
- **VI.1**: Zinspolitik (Taylor-Regel)

### Schritt 2: Vereinfachungsannahmen

| Annahme | Formal | Konsequenz |
|---|---|---|
| **Kurzfristig** | $K = \text{const}$, $\dot{p} = 0$, $P = \text{const}$ | Keine Kapitalakkumulation, feste Preise |
| **Geschlossene VW** | $NX = 0$ | Export-Import entfällt |
| **Stationarität** | $\dot{c} = 0,\ \dot{m} = 0$ | Gleichgewicht auf beiden Märkten |
| **Kein Herding, keine Info** | $\alpha_H = 0$, $\mathcal{I} \to \infty$ | Rationale Entscheidungen |
| **Repräsentativer Agent** | $N = 1$ | Keine Heterogenität |

### Schritt 3: Elimination

**I.2** stationär: $0 = Y - C - I - G$ (da geschlossen: $Y = C + I + G$)

**V.1** stationär unter obigen Annahmen: Die allgemeine Konsumgleichung $\dot{c} = R \cdot c + \Psi_c + \Phi_c$ wird zu $\dot{c} = 0$, was im stationären Zustand $R = 0$ erfordert: $r = \beta$. Alternativ, für die IS-LM-Analyse setzen wir die Konsumfunktion $C = C(Y - T, r)$ als *implizite Lösung* der stationären V.1. Investition: $I = I(r)$ aus III.4 stationär.

**I.4** stationär ($\dot{m} = 0$): Die Gelderhaltung $\dot{M} = g_Z + g_B \cdot \text{Kredit} - \tau_{\mathcal{G}}$ wird im Gleichgewicht zu: $M/P = L(Y, r)$ — die reale Geldnachfrage ist eine Funktion von Output und Zins.

### Schritt 4: Reduktion

Es bleiben zwei Gleichgewichtsbedingungen in zwei Unbekannten ($Y, r$):

$$\text{IS}: \quad Y = C(Y - T, r) + I(r) + G$$
$$\text{LM}: \quad M/P = L(Y, r)$$

### Schritt 5: Identifikation

$$\boxed{\text{IS}: Y = C(Y-T) + I(r) + G, \qquad \text{LM}: M/P = L(Y, r)}$$

Dies ist *exakt* das IS-LM-Modell (Hicks 1937, Econometrica). Die IS-Kurve folgt aus der stationären aggregierten Bilanz I.2 plus der Konsumfunktion (aus V.1 stationär). Die LM-Kurve folgt aus der stationären Gelderhaltung I.4.

### Schritt 6: Was geht verloren?

| Verloren | Gleichung | Phänomen |
|---|---|---|
| Dynamik | Alle $\dot{X}$ | Anpassungsprozesse, Overshooting |
| Preisflexibilität | $\dot{p} \neq 0$ | Inflation, Deflation |
| Heterogenität | IV.1–IV.4 | Verteilungseffekte des Zinses |
| Herding, Blasen | V.3, III.2 | Finanzinstabilität |
| Information | I.1 | Fehlallokation durch Informationsmangel |

---

## §17.2 Keynesianischer Multiplikator

### Ausgangspunkt: IS-Gleichung (aus §17.1)

$$Y = C(Y - T) + I + G$$

### Zusätzliche Vereinfachung

Lineare Konsumfunktion: $C = c_0 + c'(Y - T)$ mit marginaler Konsumquote $c' \in (0, 1)$.

### Reduktion

$$Y = c_0 + c'(Y - T) + I + G$$
$$Y - c'Y = c_0 - c'T + I + G$$
$$Y(1 - c') = c_0 - c'T + I + G$$

$$\boxed{Y = \frac{1}{1 - c'}(c_0 - c'T + I + G), \qquad \frac{dY}{dG} = \frac{1}{1 - c'}}$$

Der Multiplikator $1/(1-c')$ emergiert aus der *Kreislaufstruktur*: Mehr Staatsausgaben → mehr Einkommen → mehr Konsum → mehr Einkommen → ... Die geometrische Reihe konvergiert, weil $c' < 1$ (aus der axiomatischen Eigenschaft $u'' < 0$: abnehmender Grenznutzen impliziert eine Sparquote $> 0$).

---

## §17.3 Phillips-Kurve

### Ausgangspunkt: III.3 + II.2 in allgemeiner Form

Die Produktionsentscheidung III.3 bestimmt den Output: $q = F(K, L)$. Die Preisdynamik II.2 reagiert auf Excess Demand.

### Log-Linearisierung um den Steady State

Wir linearisieren III.3 und II.2 um $X^*$ (die Steady-State-Werte aus §14.5):

- III.3 linearisiert: $\hat{q}_t = \alpha \hat{k}_t + (1-\alpha)\hat{l}_t$ → Grenzkosten: $\widehat{mc}_t = w_t - (f(k) - k f'(k)) \approx \kappa \hat{x}_t$ wobei $\hat{x}_t$ der Output-Gap ist
- II.2 mit rationalen Erwartungen (III.4) und intertemporaler Preissetzung (Calvo 1983 als Modellierungswahl):

### Reduktion

$$\boxed{\pi_t = \kappa \hat{x}_t + \beta_\pi E_t[\pi_{t+1}]}$$

wobei $\kappa$ die Steigung der Phillips-Kurve ist (abhängig von der Substitutionselastizität und der Preisflexibilität) und $\beta_\pi$ der Diskontfaktor.

> **Observation 17.1 (Phillips als linearisierte II.2 + III.3).** *Die New-Keynesian Phillips-Kurve ist eine **Log-Linearisierung** der allgemeinen Gleichungen II.2 und III.3 um den Steady State. Sie gilt approximativ in der Nähe des Gleichgewichts. Weit entfernt vom Gleichgewicht (Hyperinflation, Deflation) versagt die Linearisierung — dann muss man die vollen nichtlinearen Gleichungen lösen.*

---

## §17.4 Liquiditätsfalle

### Ausgangspunkt: IS-LM (§17.1) + Taylor-Regel VI.1

Die Taylor-Regel (VI.1) setzt den Nominalzins: $r = r^* + \phi_\pi(\pi - \pi^*) + \phi_y(\hat{y} - 0)$.

### Grenzübergang

$$r \to 0 \qquad (\text{Nominalzins an der Nullzinsgrenze})$$

### Konsequenzen im System

1. **LM-Kurve wird horizontal** bei $r = 0$: Geld und Bonds sind perfekte Substitute → Geldnachfrage ist unendlich elastisch bzgl. $r$
2. **Geldmultiplikator** (M.3): $m_{\text{mult}} = 1/(1 - (1-r_k) \cdot (1-c_B))$ → bei $r \to 0$: $m_{\text{mult}} \to 0$ (Banken verleihen nicht, weil Marge verschwunden)
3. **Geldpolitik wirkungslos**: $\Delta M$ vergrößert nur die Geldbasis, ohne Kreditschöpfung auszulösen
4. **Nur Fiskalpolitik wirkt**: $\Delta G \to \frac{1}{1-c'} \Delta Y$ (Multiplikator bleibt intakt)

### Identifikation

Dies ist *exakt* die Keynesianische Liquiditätsfalle (Keynes 1936, General Theory, Kap. 15): Bei $r = 0$ ist Geldpolitik wirkungslos, nur Fiskalpolitik stimuliert.

> **Proposition 17.1 (Liquiditätsfalle als Singularität).** *Die Liquiditätsfalle ist eine **Singularität** des monetären Subsystems: Bei $r \to 0$ degeneriert die Taylor-Regel VI.1, der Geldmultiplikator M.3 kollabiert, und die Zinselastizität der Kreditschöpfung M.1 wird null. Das System hat an diesem Punkt einen **Rang-Defekt** — ein Steuerungsinstrument (Geldpolitik) fällt aus.*

---

# Kapitel 18: Finanzmärkte

---

## §18.1 CAPM (Sharpe 1964): Capital Asset Pricing Model

### Schritt 1: Die allgemeine Portfoliogleichung III.2

$$\dot{\theta}_{ik} = \lambda_\theta \frac{\partial u}{\partial \theta_{ik}} + \alpha_H \sum_j A_{ij}^{\text{eff}}(\theta_{jk} - \theta_{ik}) + \sigma_\theta \xi_i$$

Drei Kräfte: Nutzenmaximierung + Herding + Noise.

### Schritt 2: Vereinfachungsannahmen

| Annahme | Formal | Konsequenz |
|---|---|---|
| **Stationarität** | $\dot{\theta}_{ik} = 0$ | Portfolio-Gleichgewicht |
| **Kein Herding** | $\alpha_H = 0$ | Herding-Term verschwindet |
| **Kein Noise** | $\sigma_\theta = 0$ | Deterministisches Optimum |
| **Perfekte Info** | $\mathcal{I} \to \infty$ | Alle Agenten kennen alle Verteilungen |
| **Eine Periode** | Statisch | Keine intertemporale Optimierung |
| **Mean-Variance-Nutzen** | $u(\theta) = E[r_P] - \frac{\gamma}{2}\text{Var}(r_P)$ | Quadratischer Nutzen (Modellierungswahl) |

### Schritt 3: Elimination

III.2 wird zu:

$$0 = \lambda_\theta \frac{\partial u}{\partial \theta_{ik}}$$

Die First-Order-Condition (FOC) des Mean-Variance-Problems:

$$\frac{\partial}{\partial \theta_{ik}} \left[E[r_P] - \frac{\gamma}{2}\text{Var}(r_P)\right] = 0$$

$$E[r_k] - r_f = \gamma \sum_j \theta_j \text{Cov}(r_k, r_j)$$

### Schritt 4: Aggregation

Im Marktgleichgewicht halten alle Agenten das Marktportfolio ($\theta_k^* = w_k^M$). Dann wird:

$$\sum_j \theta_j \text{Cov}(r_k, r_j) = \text{Cov}(r_k, r_M)$$

und aus $E[r_M] - r_f = \gamma \text{Var}(r_M)$ folgt $\gamma = (E[r_M] - r_f)/\text{Var}(r_M)$.

### Schritt 5: Identifikation

$$\boxed{E[r_k] - r_f = \beta_k \cdot (E[r_M] - r_f), \qquad \beta_k = \frac{\text{Cov}(r_k, r_M)}{\text{Var}(r_M)}}$$

Dies ist *exakt* die Security Market Line des CAPM (Sharpe 1964, JoF).

### Schritt 6: Was geht verloren?

Die drei weggenommenen Terme in III.2 erzeugen *genau* die Phänomene, die das CAPM nicht erfassen kann:

| Weggenommener Term | Erzeugt im allgemeinen System |
|---|---|
| $\alpha_H \sum A_{ij}(\theta_j - \theta_i)$ | Herding → Blasen, Momentum-Anomalie, Überbewertung |
| $\sigma_\theta \xi_i$ | Idiosynkratisches Rauschen → Excess Volatility, Noise Trading |
| Dynamik ($\dot{\theta} \neq 0$) | Portfolioanpassung → Volatility Clustering, Autokorrelation |

> **Proposition 18.1 (CAPM als stationärer Grenzfall von III.2).** *Das CAPM emergiert aus III.2 unter Stationarität, keinem Herding, keinem Noise und Mean-Variance-Nutzen. Die gesamte "Anomalie-Literatur" der empirischen Finanzwissenschaft (Momentum, Value, Size, Low-Vol) bildet Phänomene ab, die durch die **weggelassenen Terme** $\alpha_H > 0$ und $\sigma_\theta > 0$ im allgemeinen System erzeugt werden.*

---

## §18.2 Efficient Market Hypothesis (EMH)

### Ausgangspunkt: II.2 in allgemeiner Form

$$\dot{p}_k = \lambda_k^{-1}(D_k - S_k) + \eta_k p_k - \frac{\varphi_k}{\mathcal{I}_k + \varepsilon}$$

### Vereinfachungen für die starke EMH

| Annahme | Formal | Konsequenz |
|---|---|---|
| $\mathcal{I} \to \infty$ | Perfekte Information | $\varphi/(\mathcal{I}+\varepsilon) \to 0$: keine Illiquiditätsprämie |
| $\alpha_H = 0$ | Kein Herding | $\eta_k \to 0$ (kein selbstverstärkender Preisanstieg) |
| Marktgleichgewicht | $D_k = S_k$ | $\lambda^{-1}(D-S) = 0$ |

### Reduktion

$$\dot{p}_k = \sigma_k p_k\, dW_t$$

Die einzige verbleibende Dynamik ist *weißes Rauschen* — der Preis folgt einer geometrischen Brown'schen Bewegung (GBM). Dies ist die EMH: Preise reflektieren *alle* verfügbare Information, und Preisänderungen sind unvorhersagbar.

### Identifikation

$$\boxed{dp = \mu p\, dt + \sigma p\, dW} \qquad (\text{GBM, Black-Scholes 1973})$$

### Was die EMH-Annahmen verbergen

Die drei Terme, die zu Null gesetzt werden, sind *genau* die drei Feinde der EMH:

| EMH-Verletzung | Term in II.2 | Beobachtetes Phänomen |
|---|---|---|
| Info-Asymmetrie | $-\varphi/(\mathcal{I}+\varepsilon)$ | Insider-Vorteile, Akerlof-Lemons |
| Herding | $\eta_k p_k$ (mit $\eta \propto \alpha_H$) | Blasen, Momentum, Crashes |
| Illiquidität | $-\varphi/(\mathcal{I}+\varepsilon)$ | Liquiditätsprämie, Bid-Ask-Spread |

---

# Kapitel 19: Offene Ökonomie

---

## §19.1 Mundell-Fleming: IS-LM-BP

### Ausgangspunkt: IS-LM (§17.1) + offene Ökonomie

Wir erweitern das IS-LM-System um den Handelskanal. Im allgemeinen System (S08): $R = 2$ Regionen, Handelsgleichung III.5°, Wechselkursdynamik.

### Vereinfachungsannahmen (zusätzlich zu IS-LM)

- $R = 2$ (zwei Länder)
- Statische Erwartungen: $\dot{e} = 0$ (keine Wechselkursspekulation)
- Kleine offene Wirtschaft (Land $\alpha$ ist klein relativ zum Ausland $\beta$)

### Reduktion

Drei Gleichgewichtsbedingungen:

$$\text{IS}: Y = C(Y-T) + I(r) + G + NX(e, Y, Y^*)$$
$$\text{LM}: M/P = L(Y, r)$$
$$\text{BP}: r = r^* + \dot{e}^e \quad (\text{Zinsparität, aus E.1 offen})$$

### Identifikation und das Trilemma

$$\boxed{\text{IS-LM-BP-System}}$$

Aus den Gleichungen folgt das *Unmöglichkeitsdreieck* (Mundell 1963): Von den drei Zielen — (1) fester Wechselkurs, (2) freier Kapitalverkehr, (3) autonome Geldpolitik — sind maximal zwei gleichzeitig erreichbar.

---

## §19.2 Gravitationsmodell und komparativer Vorteil

### Ausgangspunkt: Handelsflüsse F.1 + Potentiale F.2

Der Güterfluss F.1 ist: $j_{n,k} = -D_k \nabla\mu_k^{\text{eff}}$. Im inter-regionalen Fall wird der Gradient über Regionen zu einer diskreten Differenz:

$$\text{Trade}_{\alpha\beta,k} \propto \chi^{\text{Güter}} \cdot S_k^\alpha \cdot \sigma\!\left(\frac{e_{\alpha\beta} p_k^\beta - p_k^\alpha}{p_k^\alpha}\right)$$

### Vereinfachung: Aggregation über Güter

Summation über $k$ und Approximation $S_k^\alpha \propto Y_\alpha$ (Angebot proportional zum BIP):

$$\text{Trade}_{\alpha\beta} \propto Y_\alpha \cdot Y_\beta \cdot \chi_{\alpha\beta}$$

wobei $\chi_{\alpha\beta} < 1$ die bilaterale Handelsoffenheit parametrisiert (Proxy für inverse Distanz).

### Identifikation

$$\boxed{\text{Trade}_{\alpha\beta} \propto \frac{Y_\alpha \cdot Y_\beta}{d_{\alpha\beta}}}$$

Dies ist das Gravitationsmodell (Tinbergen 1962, Anderson 1979). Es emergiert aus der Flussgleichung F.1, wenn man Handelsfriktionen ($\chi < 1$) als distanzproportional modelliert.

---

## §19.3 Lucas-Paradox

### Das Paradox

Neoklassisch (Solow): Kapital sollte von reichen zu armen Ländern fließen (höhere Grenzrendite bei niedrigerem $k$). Empirisch: Das Gegenteil passiert. Lucas (1990) stellte die Frage: Warum?

### Auflösung durch das allgemeine System

Der Kapitalfluss folgt nicht dem *objektiven* Potentialgradient, sondern dem *effektiven*:

$$\mu^{\text{eff}} = p + \alpha_H \bar{p}^{\text{Herding}} + \frac{\psi}{\mathcal{I} + \varepsilon}$$

Für arme Länder gilt: $\mathcal{I}_{\text{arm}} \ll \mathcal{I}_{\text{reich}}$ (weniger Information über arme Märkte). Dann:

$$\frac{\psi}{\mathcal{I}_{\text{arm}} + \varepsilon} \gg \frac{\psi}{\mathcal{I}_{\text{reich}} + \varepsilon}$$

Die Transaktionskosten für Investitionen in arme Länder sind *prohibitiv hoch*. Der effektive Potentialgradient zeigt *von arm nach reich* — obwohl der objektive Preisunterschied in die andere Richtung weist.

> **Proposition 19.1 (Lucas-Paradox als Informationssingularität).** *Das Lucas-Paradox löst sich auf, sobald man die Informationsgleichung I.1 und das effektive Potential F.2 berücksichtigt. Im allgemeinen System fließt Kapital nicht zum höchsten Grenzprodukt, sondern zum niedrigsten **wahrgenommenen** Risiko — und das liegt in informationsreichen Märkten. Die fehlende Variable in Lucas' Analyse ist $\mathcal{I}$.*

---

# Kapitel 20: Finanzinstabilität

---

## §20.1 Minsky-Instabilität: Hopf-Bifurkation bei $\alpha_H = \alpha_H^{\text{krit}}$

### Schritt 1: Die relevanten Gleichungen

Die Minsky-Dynamik liegt in der Kopplung dreier Gleichungen:

$$\text{II.2}: \quad \dot{p} = \lambda^{-1}(D - S) + \eta p - \frac{\varphi}{\mathcal{I} + \varepsilon}$$
$$\text{III.2}: \quad \dot{\theta}_{ik} = \lambda_\theta \frac{\partial u}{\partial \theta_{ik}} + \alpha_H \sum_j A_{ij}(\theta_j - \theta_i) + \sigma_\theta \xi_i$$
$$\text{III.4}: \quad \dot{\hat{p}}_k = \alpha_t(\dot{p}_k - \dot{\hat{p}}_k) + \text{Ankerkorrektur}$$

### Schritt 2: Die Rückkopplungsschleife

$$p \uparrow \xrightarrow{\text{III.4}} \hat{p} \uparrow \xrightarrow{\text{III.2, } \alpha_H > 0} \theta \uparrow\ (\text{Nachkauf}) \xrightarrow{\text{II.2}} D \uparrow \xrightarrow{} p \uparrow$$

Dies ist ein *positiver Feedback*: Preissteigerung → optimistische Erwartungen → Herding-Nachkauf → Nachfrage steigt → Preis steigt weiter.

### Schritt 3: Linearisierung und Bifurkationsanalyse

Linearisierung der Kopplung II.2 ↔ III.2 ↔ III.4 um den Gleichgewichtspreis $p^*$. Die Jacobi-Matrix hat Eigenwerte, die von $\alpha_H$ abhängen:

$$\text{Re}(\lambda(\alpha_H)) \begin{cases} < 0 & \text{für } \alpha_H < \alpha_H^{\text{krit}} \quad (\text{stabil: gedämpfte Zyklen}) \\ = 0 & \text{für } \alpha_H = \alpha_H^{\text{krit}} \quad (\text{Hopf-Bifurkation}) \\ > 0 & \text{für } \alpha_H > \alpha_H^{\text{krit}} \quad (\text{instabil: Blase/Spirale}) \end{cases}$$

wobei:

$$\boxed{\alpha_H^{\text{krit}} = \lambda(\gamma\sigma^2 - \eta)}$$

### Schritt 4: Die vier Minsky-Phasen als Regime-Sequenz

| Phase | Ökonomisch | Im System |
|---|---|---|
| 1. **Hedge** | Stabile Finanzierung | $\alpha_H < \alpha_H^{\text{krit}}$, Lev niedrig |
| 2. **Speculative** | Steigende Verschuldung | $\alpha_H \to \alpha_H^{\text{krit}}$, Lev steigt (M.3) |
| 3. **Ponzi** | Nur Preissteigerung bedient Schulden | $\alpha_H > \alpha_H^{\text{krit}}$, Spirale aktiv |
| 4. **Crash** | Schuldenpyramide kollabiert | VIII.4: Regimewechsel / VIII.6: Bankrott |

> **Proposition 20.1 (Minsky als Hopf-Bifurkation).** *Der Minsky-Zyklus emergiert aus dem allgemeinen System als **Hopf-Bifurkation** der Kopplung II.2 ↔ III.2 ↔ III.4 beim kritischen Herding-Parameter $\alpha_H^{\text{krit}}$. Kein Minsky-spezifisches Modell muss postuliert werden — die Instabilität entsteht aus der allgemeinen Preisdynamik (II.2) plus Portfolioentscheidung mit Herding (III.2) plus adaptiver Erwartungsbildung (III.4).*

---

## §20.2 Fisher-Deflationsspirale

### Ausgangspunkt: I.1 + II.2 bei $\dot{p} < 0$ und hoher Verschuldung

Die Fisher-Spirale ist eine *positive Rückkopplung* zwischen Deflation und Verschuldung:

$$p \downarrow \xrightarrow{\text{I.1}} \text{realer Schuldenwert } (b/p) \uparrow \xrightarrow{} w \downarrow \xrightarrow{\text{V.1}} c \downarrow \xrightarrow{\text{II.2}} D \downarrow \xrightarrow{} p \downarrow$$

### Formale Darstellung

Aus I.1: $\dot{w}_i = y_i - c_i + \theta_i \dot{p} + r b_i - T_i$. Bei $\dot{p} < 0$ und positivem Portfolio $\theta_i > 0$: Der Term $\theta_i \dot{p} < 0$ ist ein *Kapitalverlust durch Deflation*.

Aus der Fisher-Gleichung (E.1): $r_{\text{real}} = r_{\text{nom}} - \pi$. Bei Deflation ($\pi < 0$): $r_{\text{real}} > r_{\text{nom}}$ — der *reale* Zinssatz steigt, obwohl der nominale konstant bleibt.

### Instabilitätsbedingung

Die Spirale ist instabil, wenn die Deflation schneller den Schuldenwert erhöht als die Einkommen die Schulden bedienen können:

$$\frac{\dot{b}}{b} > r \quad \Longleftrightarrow \quad |\dot{p}/p| > r - g$$

### Identifikation

Dies ist *exakt* Fishers Debt-Deflation-Theorie (Fisher 1933, Econometrica): Deflation bei hoher Verschuldung erzeugt eine selbstverstärkende Abwärtsspirale. Im allgemeinen System ist die Fisher-Spirale *ein Spezialfall der Schleife 5* (Kapitel 13: Schulden-Deflation I.1 ↔ II.2).

---

# Kapitel 21: Verteilung

---

## §21.1 Piketty: $r > g$ und steigende Ungleichheit

### Ausgangspunkt: IV.4 (Varianz der Vermögensverteilung)

$$\frac{d\,\text{Var}(w)}{dt} = 2\,\text{Cov}(w, \dot{w}) + \text{Var}(\dot{w})$$

Diese Gleichung ist *allgemein* — sie folgt aus der Definition der Varianz und der Vermögensdynamik I.1, ohne jede Vereinfachung.

### Schritt 2: Piketty-Annahme

$$r > g \quad \text{persistent (Kapitalrendite systematisch größer als Wachstumsrate)}$$

### Schritt 3: Konsequenz für $\text{Cov}(w, \dot{w})$

Aus I.1: $\dot{w}_i = y_i - c_i + r_i w_i + \dots$ (vereinfacht, wobei $r_i w_i$ die Kapitalrendite ist). Wenn $r_i$ positiv mit $w_i$ korreliert ist (reichere Agenten erzielen höhere Renditen — Zugang zu besseren Investitionen, Skaleneffekte), dann:

$$\text{Cov}(w, \dot{w}) = \text{Cov}(w, r \cdot w) = r \cdot \text{Var}(w) + \text{Cov}(w, r) \cdot E[w] > 0$$

Die Vermögensvarianz wächst monoton — Ungleichheit steigt.

### Schritt 4: Langfristige Dynamik

Bei $r > g$ und positivem $\text{Cov}(w, \dot{w})$: $\text{Var}(w)$ wächst exponentiell → $\text{Gini} \to 1$.

### Identifikation

$$\boxed{r > g \implies \frac{d\,\text{Gini}}{dt} > 0 \implies \text{Gini} \to 1}$$

Dies ist die formale Version von Pikettys zentraler These (Piketty 2014). Sie emergiert aus IV.4 (Varianz-Dynamik der Vermögensverteilung) unter der einzigen Annahme $r > g$.

> **Proposition 21.1 (Piketty als Konsequenz von IV.4).** *Die Piketty-Dynamik erfordert kein eigenes Modell — sie folgt aus der allgemeinen Varianz-Gleichung IV.4, die selbst eine mathematische Konsequenz der Boltzmann-Aggregation IV.1 und der Vermögensgleichung I.1 ist. Die Bedingung $r > g$ ist die **einzige** Zusatzannahme. Gegenmaßnahmen (progressive Besteuerung, Erbschaftssteuer) erscheinen formal als Terme in I.1, die $\text{Cov}(w, \dot{w})$ reduzieren.*

---

## §21.2 Kuznets-Kurve: Invertiertes U

### Ausgangspunkt: IV.1 (Boltzmann-Transport) + N.1 (Klassenwechsel)

Die Kuznets-Kurve beschreibt ein invertiertes U der Ungleichheit über den Entwicklungsprozess: Erst steigt die Ungleichheit, dann fällt sie.

### Mechanismus im allgemeinen System

1. **Anfangs**: Wenige Agenten wechseln vom niedrigproduktiven Sektor (Landwirtschaft, Klasse $\mathcal{W}_1$) in den hochproduktiven (Industrie, $\mathcal{W}_2$). Dies erzeugt über N.1 (Klassenwechsel $C_X$) eine bimodale Verteilung in IV.1: viele Arme + wenige Reiche → Gini steigt.

2. **Mitte**: Die Mehrheit befindet sich im Übergang. Beide Sektoren koexistieren. Maximale Spreizung der Verteilung → Gini maximal.

3. **Spät**: Die Mehrheit ist im hochproduktiven Sektor angekommen. Die Verteilung wird unimodal → Gini sinkt.

### Identifikation

Die Kuznets-Kurve ist kein Spezialfall einer *einzelnen* Gleichung, sondern ein *emergentes Phänomen* der Interaktion IV.1 (Verteilung) + N.1 (Klassenwechsel) + III.3 (heterogene Produktivität). Keine Vereinfachungsannahme erzeugt sie — sie entsteht aus der Struktur.

---

# Kapitel 22: Informationsökonomik

---

## §22.1 Stigler (1961): Suchkosten

### Ausgangspunkt: Axiom A10 (Informationskosten)

$$C(\mathcal{I}) \text{ mit } C > 0,\ C' > 0,\ C'' > 0$$

### Identifikation

Stiglers Suchkostentheorie (1961, JPE) postuliert: Information ist *nicht* kostenlos — Agenten müssen Ressourcen aufwenden, um Preise, Qualitäten und Alternativen zu erfahren. Im allgemeinen System ist dies *Axiom A10*: Information ist ein knappes, kostspieliges Gut.

Die gesamte Suchkostentheorie ist damit nicht ein Spezialfall — sie ist ein *Axiom* des allgemeinen Systems. Jedes Modell, das kostenlose Information annimmt ($C(\mathcal{I}) = 0$), verletzt A10.

---

## §22.2 Grossman-Stiglitz (1980): Das Informationsparadox

### Das Paradox

Wenn Preise alle Information enthalten (EMH: $\mathcal{I} \to \infty$ in Preisen), hat niemand Anreiz, Information zu beschaffen (da $C(\mathcal{I}) > 0$ für jede Informationsmenge). Aber wenn niemand Information beschafft, können Preise sie nicht enthalten.

### Auflösung im allgemeinen System

Im allgemeinen System existiert das Paradox *nicht*, weil $\mathcal{I} \to \infty$ keine Lösung ist:

1. **A10**: $C(\mathcal{I}) > 0$ — Information kostet immer etwas
2. **I.5** (Informationsnutzen): $\Pi^{\text{info}} = \Delta v_6 - C(\mathcal{I})$ — Informationsgewinnung lohnt sich, solange der Grenznutzen die Grenzkosten übersteigt
3. **Gleichgewicht**: $C'(\mathcal{I}^*) = \partial v_6 / \partial \mathcal{I}$ — interiores Gleichgewicht bei endlichem $0 < \mathcal{I}^* < \infty$

Die Auflösung: Im allgemeinen System ist Information *nie* perfekt und *nie* null. Es gibt ein *interiores* Gleichgewicht, in dem informierte Agenten profitieren und uninformierte nicht.

> **Proposition 22.1 (Grossman-Stiglitz-Auflösung).** *Das Informationsparadox ist ein Artefakt der Extremannahme $\mathcal{I} \to \infty$. Im allgemeinen System mit endlichen Informationskosten (A10) und endogener Informationsdynamik (I.1) konvergiert das System auf ein interiores Gleichgewicht $\mathcal{I}^* \in (0, \infty)$, in dem Information teilweise — aber nie vollständig — in Preisen enthalten ist.*

---

## §22.3 Akerlof (1970): Market for Lemons

### Ausgangspunkt: U.3 (effektiver Preis) bei asymmetrischer Information

$$p_k^{\text{eff}} = p_k \cdot \left(1 + \frac{\psi_k}{\mathcal{I}_k + \varepsilon}\right)$$

### Asymmetrie

- Verkäufer: $\mathcal{I}_{\text{Verkäufer}}$ hoch (kennt Qualität)
- Käufer: $\mathcal{I}_{\text{Käufer}}$ niedrig (kennt Qualität nicht)

### Konsequenz

Bei niedrigem $\mathcal{I}_{\text{Käufer}}$: $p^{\text{eff}} \gg p$ für den Käufer → er bietet weniger → gute Qualität zieht sich zurück (da $p < p_{\text{fair}}$) → nur schlechte Qualität bleibt (Lemons).

Im Grenzfall $\mathcal{I}_{\text{Käufer}} \to 0$: $p^{\text{eff}} \to \infty$ → Markt bricht vollständig zusammen.

> **Proposition 22.2 (Akerlof als Informationssingularität).** *Adverse Selektion emergiert aus U.3 bei asymmetrischer Information: Wenn $\mathcal{I}_{\text{Käufer}} \ll \mathcal{I}_{\text{Verkäufer}}$, übersteigt der effektive Preis den Marktpreis, gute Qualität wird vom Markt verdrängt, und nur Lemons bleiben. Der vollständige Marktkolaps ($\mathcal{I} \to 0$) ist die Pol-Singularität von II.2: $-\varphi/(\mathcal{I}+\varepsilon) \to -\infty$.*

---

# Kapitel 23: Verhaltensökonomik

---

## §23.1 Prospect Theory (Kahneman-Tversky 1979)

### Ausgangspunkt: V.2 (psychologische Konsumverzerrung) in allgemeiner Form

$$\dot{c}_i = R_i c_i + \Psi_c(c_i, c_i^*, \text{Gini}, \mathcal{I}_i) + \Phi_c(\cdot)$$

Die Funktion $\Psi_c$ (Ebene 2 der Drei-Ebenen-Architektur) hat axiomatische Eigenschaften:

| Eigenschaft | Formal | Ökonomisch |
|---|---|---|
| Referenzpunkt-Anziehung | $\partial\Psi_c / \partial(c^* - c) > 0$ | Konsum driftet zum Referenzpunkt |
| Verlust-Asymmetrie | $|\Psi_c(c < c^*)| > |\Psi_c(c > c^*)|$ | Verluste wiegen schwerer als Gewinne |
| Relative Deprivation | $\partial\Psi_c / \partial\text{Gini} < 0$ für $c < \bar{c}$ | Ungleichheit drückt Arme |

### Spezifizierung: Prospect-Theory-Form (Modellierungswahl)

Wenn man als *Modellierungswahl* die funktionale Form der Prospect Theory einsetzt:

$$\Psi_c = \alpha^+ (c_i - c_i^*)^\mu \cdot \mathbb{1}[c > c^*] - \lambda \alpha^- (c_i^* - c_i)^\mu \cdot \mathbb{1}[c < c^*]$$

mit $\lambda > 1$ (Verlustaversion) und $\mu < 1$ (abnehmende Sensitivität), dann reproduziert V.2 *exakt* die Kahneman-Tversky Wertfunktion.

### Identifikation

$$\boxed{v(x) = \begin{cases} x^\mu & x \geq 0 \\ -\lambda(-x)^\mu & x < 0 \end{cases}, \qquad \lambda > 1}$$

### Was das allgemeine System hinzufügt

V.2 ist *allgemeiner* als Prospect Theory:
- Der Referenzpunkt $c^*$ ist *endogen* (VI.1: $\dot{c}^* = \lambda_c(\mathcal{I} - \mathcal{I}^{\text{ref}})$), nicht exogen
- Die Verlustasymmetrie kann *regimeabhängig* sein (VIII.5: $\lambda^{(\text{Krise})} > \lambda^{(\text{Boom})}$)
- Die Funktion $\Psi_c$ kann von Ungleichheit (Gini) abhängen — ein Kanal, den Prospect Theory nicht hat

> **Proposition 23.1 (Prospect Theory als Modellierungswahl in V.2).** *Prospect Theory (Kahneman-Tversky 1979) ist eine **spezifische funktionale Form** für die allgemeine psychologische Konsumverzerrung $\Psi_c$ in V.2. Die axiomatischen Eigenschaften von $\Psi_c$ (Referenzpunkt-Anziehung, Verlust-Asymmetrie) sind stärker als Prospect Theory verlangt — sie erlauben weitere Spezialisierungen (Habit Formation, relative Deprivation), die über Kahneman-Tversky hinausgehen.*

---

## §23.2 Herding und Blasen

### Ausgangspunkt: V.3 (soziale Konsumkopplung) in allgemeiner Form

$$\Phi_c(c_j - c_i, \mathcal{I}_j, \mathcal{I}_i, Z) \text{ mit } \partial\Phi/\partial(c_j - c_i) > 0, \quad \Phi(0) = 0$$

### Spezialisierung 1: Lineares Herding

$$\Phi_c = \alpha_H(c_j - c_i) \qquad \Rightarrow \qquad \text{Standard-Herding (de Groot-Friedkin)}$$

### Spezialisierung 2: Informationsgewichtetes Herding

$$\Phi_c = \alpha_H \cdot \frac{\mathcal{I}_j}{\mathcal{I}_i + \varepsilon} \cdot (c_j - c_i) \qquad \Rightarrow \qquad \text{informed Herding (informiertere Nachbarn haben mehr Einfluss)}$$

### Spezialisierung 3: Asymmetrisches Herding

$$\Phi_c = \alpha_H^+ \max(c_j - c_i, 0) + \alpha_H^- \min(c_j - c_i, 0), \quad \alpha_H^+ > |\alpha_H^-|$$

**Aufwärts-Herding stärker als Abwärts-Herding**: Agenten imitieren Mehrkonsum schneller als Minderkonsum. Dies erzeugt die *Blasen-Asymmetrie*: Blasen bauen sich langsam auf, platzen aber schnell.

### Blasendynamik in III.2

Die Portfolio-Version (III.2: $\alpha_H \sum A_{ij}(\theta_j - \theta_i)$) erzeugt bei $\alpha_H > \alpha_H^{\text{krit}}$ die Hopf-Bifurkation (§20.1). Die Konsum-Version (V.3) erzeugt *reale* Blasen: Überkonsum, der durch soziale Nachahmung getrieben wird.

---

## §23.3 Granovetter-Kaskaden

### Ausgangspunkt: Schw.1 + Schw.2 (Kapitel 10)

Die Schwellenwert-Architektur (§10.4–10.6) ist *bereits* die formale Granovetter-Theorie. Kein weiterer Grenzübergang nötig — Granovetter (1978) ist ein *Baustein* des allgemeinen Systems, nicht ein Spezialfall davon.

### Was Granovetter impliziert vs. was das System liefert

| Granovetter (1978) | Ökonoaxiomatik |
|---|---|
| Exogene Schwellenwertverteilung $f(\theta)$ | Endogene Verteilung via Schw.2 |
| Statische Analyse (einmaliger Kipppunkt) | Dynamische Analyse (wandernder Kipppunkt, Observation 10.4) |
| Kein Netzwerk (Mean-Field) | Explizites Netzwerk $A_{ij}$ (V.6–V.8) |
| Keine Rückkopplung auf Makro | RS.1 koppelt Kaskade an Regimewechsel |

> **Proposition 23.2 (Granovetter als Spezialfall von Schw.1).** *Granovetters Threshold Model (1978) ist der **statische Mean-Field-Grenzfall** von Schw.1: feste Schwellenwerte ($\dot{\theta} = 0$, Schw.2 deaktiviert), deterministisch ($\tau \to 0$), ohne Netzwerk ($A_{ij} = 1/N$ für alle). Die Kaskadenbedingung $f(\bar{\theta})/\tau > 1$ ist eine Verallgemeinerung von Granovetters Schwellenbedingung.*

---

## §23.4 Zusammenfassung: Was die Verhaltensökonomik zur allgemeinen Theorie beiträgt

Die Verhaltensökonomik (Kahneman, Tversky, Thaler, Shiller) hat *Phänomene* dokumentiert: Verlustaversion, Herding, Kaskaden, Anomalien. Im allgemeinen System sind diese Phänomene *nicht ad hoc* eingefügt — sie sind *axiomatische Konsequenzen* der Drei-Ebenen-Architektur:

| Phänomen | Ebene | Gleichung | Axiom |
|---|---|---|---|
| Loss Aversion | 2 (Psychologie) | V.2: $\Psi_c$ | A5 (Nutzen mit Referenzpunkt) |
| Herding | 3 (Sozial) | V.3: $\Phi_c$ | A6 (Soziale Kopplung) |
| Kaskaden | 3 (Netzwerk) | Schw.1–Schw.2 | A6 + A7 |
| Overconfidence | 2 (Psychologie) | L.5: $E[R]$ überschätzt | A7 (Adaptive Erwartungen) |
| Statuskonsum | 3 (Sozial) | V.3: $\Phi_c$ mit Gini | A6 |

---

# Abschluss von Teil IV: Die Landkarte der Spezialfälle

## Zusammenfassende Tabelle

| Modell | Kapitel | Grenzübergang | Überlebende Gleichungen | Übereinstimmung |
|---|---|---|---|---|
| Solow (1956) | 15.1 | $N=1, K=1, \alpha_H=0, \mathcal{I}\to\infty$, exogenes $s$ | I.2, III.3 | ✓ exakt |
| Ramsey (1928) | 15.2 | Wie Solow, aber endogenes $c(t)$ | I.2, V.1, III.3 | ✓ exakt |
| AK | 15.3 | Solow + $\alpha = 1$ | I.2, III.3 | ✓ exakt |
| Romer (1990) | 15.4 | Solow + VI.6 aktiviert | I.2, III.3, VI.6 | ✓ exakt |
| Arrow-Debreu (1954) | 16.1 | $\mathcal{I}\to\infty, \alpha_H=0, \sigma=0, \dot{X}=0$ | $D_k = S_k$ | ✓ exakt |
| Walras-Tâtonnement | 16.2 | II.2 ohne Herding/Info | $\dot{p} = \lambda^{-1}(D-S)$ | ✓ exakt |
| IS-LM (1937) | 17.1 | Stationarität, geschlossen, $K=\text{const}$ | I.2, I.4 stationär | ✓ exakt |
| Multiplikator | 17.2 | IS + lineares $C$ | $Y = \frac{1}{1-c'}(I+G)$ | ✓ exakt |
| Phillips-Kurve | 17.3 | Log-Lin. von II.2 + III.3 | $\pi = \kappa\hat{x} + \beta E[\pi]$ | ✓ exakt |
| Liquiditätsfalle | 17.4 | IS-LM + $r \to 0$ | LM horizontal, $m_{\text{mult}} \to 0$ | ✓ exakt |
| CAPM (1964) | 18.1 | III.2 stationär, $\alpha_H=0, \sigma_\theta=0$ | $\mu_k - r = \beta_k(\mu_M - r)$ | ✓ exakt |
| EMH | 18.2 | II.2 mit $\mathcal{I}\to\infty, \alpha_H=0$ | $dp = \mu p\,dt + \sigma p\,dW$ | ✓ exakt |
| Mundell-Fleming | 19.1 | IS-LM + 2 Länder + BP | IS-LM-BP | ✓ exakt |
| Gravitation | 19.2 | F.1 aggregiert | $\text{Trade} \propto Y_\alpha Y_\beta/d$ | ✓ qualitativ |
| Lucas-Paradox | 19.3 | F.2 mit $\mathcal{I}_{\text{arm}} \ll \mathcal{I}_{\text{reich}}$ | Kapital: reich → reich | ✓ qualitativ |
| Minsky (1986) | 20.1 | Hopf bei $\alpha_H = \alpha_H^{\text{krit}}$ | II.2 ↔ III.2 ↔ III.4 | ✓ exakt |
| Fisher (1933) | 20.2 | I.1 + II.2 bei $\dot{p}<0$, $b/W$ groß | Schulden-Deflations-Spirale | ✓ exakt |
| Piketty (2014) | 21.1 | IV.4 mit $r > g$ | $d\text{Var}(w)/dt > 0$ | ✓ exakt |
| Kuznets (1955) | 21.2 | IV.1 + N.1 (Klassenwechsel) | Invertiertes U der Gini | ✓ qualitativ |
| Stigler (1961) | 22.1 | = Axiom A10 | $C(\mathcal{I}) > 0$ | ✓ = Axiom |
| Grossman-Stiglitz | 22.2 | I.5 + A10: $0 < \mathcal{I}^* < \infty$ | Interiores GG | ✓ Auflösung |
| Akerlof (1970) | 22.3 | U.3 bei $\mathcal{I}_{\text{Käufer}} \ll \mathcal{I}_{\text{Verkäufer}}$ | Lemon-Selektion | ✓ qualitativ |
| Prospect Theory | 23.1 | V.2 mit Kahneman-Tversky-Form | $v(x) = x^\mu / -\lambda(-x)^\mu$ | ✓ exakt |
| Herding/Blasen | 23.2 | V.3, III.2 mit $\alpha_H > \alpha_H^{\text{krit}}$ | Hopf + Asymmetrie | ✓ qualitativ |
| Granovetter (1978) | 23.3 | Schw.1 statisch, Mean-Field | $f(\bar{\theta})/\tau > 1$ | ✓ exakt |

> **Beobachtung (Vollständigkeit der Spezialfälle).** *Von 24 untersuchten Modellen sind 17 **exakt** reproduzierbar als mathematische Grenzfälle, 6 **qualitativ** reproduzierbar (die Struktur stimmt, nicht die exakte Gleichung), und 1 ist identisch mit einem Axiom (Stigler = A10). Kein einziges Modell **widerspricht** dem allgemeinen System — es ist mit jedem davon kompatibel. Dies ist der Spezialfall-Test aus Definition 11.1 (Kriterium 5).*

---

*Ende von Teil IV. Im folgenden Teil V (Validierung) zeigen wir, dass das System nicht nur theoretisch konsistent, sondern auch empirisch überprüfbar ist.*
