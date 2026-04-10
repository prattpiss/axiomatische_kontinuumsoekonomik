# axiomatische_kontinuumsoekonomik
Axiomatische Kontinuumsoekonomik or Ökonoaxiomatik idk how to call it — Axiomatic Economics Framework. 10 axioms, 6 goods classes, 63 coupled differential equations traying to unify production, trade, money, finance &amp; information dynamics. Includes world simulation (30 countries), agent-based models, parameter sweeps, and completeness proof.

# Ökonoaxiomatik

**Ein axiomatisches Framework für die Ökonomie** — aufgebaut aus 10 Axiomen, 6 Güterklassen und 63 Gleichungen, die Produktion, Konsum, Handel, Information, Geldpolitik und Finanzmarktdynamik in einem konsistenten Differentialgleichungssystem vereinen.

## Struktur

| Ordner | Inhalt |
|---|---|
| `Effekte/` | Theoretische Papers (S01–S16): Spezialeffekte, Vollständigkeitsbeweis, Informationsunschärfe, Handelsmodelle |
| `Simulation/` | Einzelsimulation des Kernmodells |
| `Einzeldynamik/` | Isolierte Dynamiken einzelner Gleichungsgruppen |
| `Weltsimulation/` | Weltsimulation mit 30 Ländern, BIP-Kalibrierung (Jahr 2000), Handelsströme, GIF-Animation |
| `Notebooks/` | NB01–NB08: Simulationen, Parametersweeps, Informationsausbreitung, Makro mit Bankensektor, Emerging-Market-Szenarien |
| `Verkettungen/` | Verkettete Mehrstufenmodelle |
| `Markdowns/` | Begleitende Dokumentation |

## Theoretischer Kern

- **10 Axiome** (A1–A10): Von Güterklassen über Preisdynamik bis Informationsthermodynamik
- **8 Gleichungsgruppen** (I–VIII): Bestände, Preise, Produktion/Konsum, Ströme, VGR, Geld/Zins, Außenhandel, Information
- **6 Güterklassen**: K1 (abschreibend), K2 (nicht-abschreibend), K3 (Verbrauchsgüter), K4 (immateriell), K5 (monetär), K6 (informationell)

## Papers (Auswahl)

| Paper | Thema |
|---|---|
| S07 | Kanonisches Gleichungssystem (50 Gleichungen) |
| S13 | Fundamentale Theorie & Vollständigkeit (63 Gleichungen) |
| S14 | Ökonomische Informations-Unschärferelation |
| S15 | Lotka-Volterra-Informationskonkurrenz |
| S16 | 5-Komponenten-Handelsmodell (Gravitation + Ricardo + HO + Info + FX) |

## Simulationen

- **Weltsimulation**: 30 Länder, 14 gekoppelte DGL-Gruppen, Handelsströme, animierte Weltkarte
- **NB08**: Emerging-Market Tech-Boost, Informationskonkurrenz-Bifurkation, Unschärfe-Validierung
- **Parametersweeps**: Sensitivitätsanalysen über alle Modellparameter

## Technologie

Python 3.13 · NumPy · SciPy · Matplotlib · Cartopy

