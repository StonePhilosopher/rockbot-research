# Research: Cuprite

**Date:** 2026-06-11
**Status:** Complete — Template compliant, builder-ready
**Researcher:** 🪨✍️
**Game blocker:** None — Cu and O are already in the trace element system. Eh concept is useful but can be approximated by O₂ thresholds in current simulator.
**Paragenetic sequence:** Native copper → cuprite → tenorite → malachite/azurite. Unified master file at `memory/research-copper-oxidation-zone.md`.

---

## Species: Cuprite

### Identity
- **Formula:** Cu₂O
- **Crystal system:** Isometric (cubic), hexoctahedral class
- **Mineral group:** Oxide (copper subgroup)
- **Hardness (Mohs):** 3.5–4
- **Specific gravity:** 5.85–6.15 (heavy — nearly pure copper by weight)
- **Cleavage:** Imperfect on {111}
- **Fracture:** Conchoidal to uneven; brittle
- **Luster:** Adamantine to sub-metallic
- **Space group:** Pn-3m (no. 224)
- **IMA symbol:** Cpr

### Color & Appearance
- **Typical color:** Deep red to brownish-red, nearly black on crystal surfaces
- **Color causes:** Cu⁺ d¹⁰ configuration produces intense red absorption; the cuprite structure (two interpenetrating cuprite-type lattices) creates strong internal reflections
- **Transparency:** Transparent to translucent in thin splinters; opaque in thick masses. Thin edges glow ruby-red in transmitted light
- **Streak:** Brownish-red
- **Notable visual features:** **Ruby-red internal reflections** — dark crystals that bleed garnet-red when light passes through them. This is refraction, not fluorescence, but the effect is so striking that cuprite is sometimes mistaken for a fluorescent mineral. Chalcotrichite variety forms hair-thin carmine-red needles.

### Crystal Habits
- **Primary habit:** Octahedral crystals {111} — most common well-formed habit
- **Common forms/faces:** {111} octahedron, {001} cube, {011} dodecahedron; cubo-octahedral combinations frequent
- **Twin laws:** Penetration twins on {111} — spinel-law twinning (one octahedron rotated 180° and re-embedded)
- **Varieties:**
  - **Chalcotrichite** ("plush copper ore") — capillary/needle-like fibers elongated along [001], loosely matted aggregates, carmine red, silky luster. Whiskers include double fibers in parallel growth, sometimes curled from differential cooling contraction (Post et al. 1983, Am. Mineral. v.68)
  - **Tile ore** — soft, earthy, brick-red to brownish massive variety, often admixed with hematite/limonite
- **Special morphologies:** Massive granular, earthy, botryoidal crusts; fibrous (chalcotrichite); rarely as skeletal hopper crystals in rapid growth conditions

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** < 100°C (supergene, near-surface)
- **Optimal growth temperature:** 10–50°C (ambient groundwater conditions)
- **Decomposition temperature:** > 1000°C (melts at 1232°C); stable at all temperatures below this in its stability field
- **Temperature-dependent habits:** Low temperature favors octahedral crystals (equilibrium form); higher temperatures within supergene range favor massive/earthy habits

#### Chemistry Required
- **Required elements in broth:** Cu > 5000 ppm (as Cu⁺, not Cu²⁺ — this is the critical distinction)
- **Optional/enhancing elements:** Fe³⁺ (promotes co-precipitation with goethite/limonite, typical in oxidation zones)
- **Inhibiting elements:** High S²⁻ (routes to sulfides instead); high CO₃²⁻ at high Eh (routes to malachite/azurite); high SiO₂ at high pH (routes to chrysocolla)
- **Required pH range:** 5.0–7.5 (slightly acidic to neutral — cuprite is unstable at high pH where Cu²⁺ hydrolyzes to tenorite or carbonates)
- **Required Eh range:** Moderately reducing (+0.1 to +0.4 V vs SHE) — the "cuprite window" between native copper (more reducing) and tenorite/malachite (more oxidizing)
- **Required O₂ range:** Low to moderate — enough to oxidize Cu⁰→Cu⁺ but not Cu⁺→Cu²⁺

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** Consumes Cu⁺ from solution; no significant byproducts
- **Byproducts of nucleation:** Depletes Cu from fluid, potentially suppressing later malachite/azurite precipitation
- **Byproducts of dissolution/decomposition:** Oxidative dissolution releases Cu²⁺ into solution, which may reprecipitate as malachite/azurite if CO₃ present, or tenorite at high pH

#### Growth Characteristics
- **Relative growth rate:** Moderate (1.5× baseline) — soft, low lattice energy, but constrained by narrow Eh window
- **Maximum crystal size:** Up to 15 cm (exceptional Onganja, Namibia crystals); more typically 1–3 cm
- **Typical crystal size in vugs:** 1–5 mm in matrix-hosted vugs; up to 2 cm in open cavities
- **Does growth rate change with temperature?** Growth rate increases with temperature but stability field narrows; supergene cuprite grows slowly over geological timescales
- **Competes with:** Native copper (more reducing), tenorite (more oxidizing, alkaline), malachite/azurite (CO₂-rich), chrysocolla (SiO₂-rich, high pH)

#### Stability
- **Breaks down in heat?** Stable to >1000°C in dry conditions; in wet conditions, oxidative dissolution begins at much lower temperatures
- **Breaks down in light?** No — cuprite is NOT light-sensitive (unlike realgar, proustite, pyrargyrite)
- **Dissolves in water?** Very low solubility; dissolves in ammonia solutions (complexes with NH₃)
- **Dissolves in acid?** Soluble in HCl with oxidation; attacked by nitric acid
- **Oxidizes?** Yes — the defining transformation. Oxidation of Cu⁺→Cu²⁺ converts cuprite to tenorite (CuO) or, with CO₃, to malachite/azurite. This is the core mechanic of the copper oxidation zone
- **Dehydrates?** No hydrates
- **Radiation sensitivity:** Not particularly radiation-sensitive

### Paragenesis
- **Forms AFTER:** Native copper (in oxidizing sequences); chalcocite/bornite/chalcopyrite (oxidation of primary sulfides releases Cu into solution)
- **Forms BEFORE:** Malachite, azurite, tenorite, chrysocolla (all require more oxidizing or more alkaline conditions)
- **Commonly associated minerals:** Native copper, malachite, azurite, chrysocolla, tenorite, goethite/limonite, chalcocite (as relict primary mineral), iron oxides/hydroxides
- **Zone:** Supergene oxidation zone — the critical Eh-pH transition between native metal and oxidized copper minerals
- **Geological environment:** Weathering zones of copper sulfide deposits; gossans; mine dumps; occasionally as volcanic sublimate (rare, high-T synthetic analog)

### Famous Localities
- **Bisbee, Arizona, USA** — large octahedral crystals, Copper Queen mine. Classic American locality.
- **Chessy-les-Mines, Rhône, France** — historic type locality (formerly "chessylite"), well-formed cubic and octahedral crystals
- **Tsumeb, Namibia** — exceptional gem-quality crystals with malachite/azurite associations. The Tsumeb cuprites are benchmarks for the species.
- **Onganja mine, Namibia** — large crystals to 15 cm, among the finest known
- **Rubtsovskoe mine, Altai Krai, Russia** — modern (2010+) specimens rivaling classic localities in size and quality
- **Ray Mine, Arizona, USA** — chalcotrichite variety (plush copper hair), type locality for the fibrous habit
- **Cornwall, England** — historic European locality
- **Broken Hill, New South Wales, Australia** — associated with rich silver-lead ores
- **Katanga (DRC)** — Likasi, Mashamba West mine — African classic

### Fluorescence
- **Fluorescent under UV?** No
- **SW (255nm) color:** None
- **MW (310nm) color:** None
- **LW (365nm) color:** None
- **Phosphorescent?** No
- **Activator:** None known
- **Quenched by:** Not applicable
- **Note:** The ruby-red "glow" in transmitted light is internal reflection/refraction, NOT fluorescence. This is a common misconception among collectors.

### Flavor Text
> Cuprite is the oxidation zone's hesitation. The groundwater found copper sulfides, stripped away the sulfur, and had a choice: reduce the copper all the way to native metal, or oxidize it fully to carbonate or oxide. Cuprite is what happens when the water can't decide. Cu⁺ — the intermediate valence, the half-step, the矿物 equivalent of a held breath. The crystals are nearly black in reflected light, but crack one or shine a lamp through a thin edge and it bleeds garnet-red from within, as if the copper itself is embarrassed by its indecision and blushes when seen through. Miners called the fibrous variety chalcotrichite — "plush copper" — because it grows as hair-thin carmine needles, matted like velvet. The oxidation zone is full of transformations, but cuprite is the only one that looks like it stopped halfway out of shyness.

### Simulator Implementation Notes
- **New parameters needed:** None strictly required — O₂ thresholds can approximate Eh. However, formal **Eh tracking** would improve all supergene mineral accuracy.
- **New events needed:** `event_cuprite_window` — a transitional zone event where O₂ is moderate (not anoxic, not fully oxidizing); `event_carbonate_conversion` — cuprite → malachite/azurite when CO₃ rises
- **Nucleation rule pseudocode:**
```
IF Cu_ppm > 5000
AND O2_ppm BETWEEN low_threshold AND mid_threshold
AND T < 100
AND pH BETWEEN 5.0 AND 7.5
THEN nucleate cuprite
```
- **Growth rule pseudocode:**
```
IF T < 100
AND O2_ppm BETWEEN low AND mid
AND pH BETWEEN 5.0 AND 7.5
THEN grow at rate 1.5 * baseline
IF CO3_ppm > threshold AND O2_ppm > mid_threshold
THEN convert_to_malachite_or_azurite (pseudomorph)
IF pH > 8.0 AND O2_ppm > mid_threshold
THEN convert_to_tenorite
```
- **Habit selection logic:**
```
IF open_vug AND slow_growth AND low_supersaturation → octahedral crystals
IF rapid_growth AND limited_space → massive/earthy (tile ore)
IF very_rapid_unidirectional_growth AND high_supersaturation → chalcotrichite fibers
IF twin_conditions_met → spinel-law penetration twins on {111}
```
- **Decomposition products:** Oxidative dissolution → Cu²⁺ in solution → malachite/azurite/tenorite depending on pH and CO₃

### Variants for Game
- **Variant 1: Ruby Crystal** — Euhedral octahedral crystals, deep red with visible internal reflections, transparent edges. Slow growth in open vug, moderate Eh window. Named "Bisbee Ruby" after the classic Arizona locality.
- **Variant 2: Chalcotrichite** — Hair-thin carmine-red fibers, matted aggregates, silky luster. Rapid unidirectional growth in confined space. The "plush copper" variety. Named "Ray Plush" after the Ray Mine, Arizona.
- **Variant 3: Tile Ore** — Massive, earthy, brick-red to brownish, soft. Rapid nucleation in low-quality matrix. Often mixed with limonite. Named "Chessy Earth" after the French type locality.
- **Variant 4: Twin Star** — Spinel-law penetration twins — two octahedra intergrown at 180° rotation, creating a six-pointed star shape when viewed down [111]. Rare, requires specific nucleation conditions. Named "Tsumeb Star" after the Namibian locality famous for twins.

---

## References
- Post, J.E. & Buseck, P.R. (1985). The structure of cuprite. *Acta Crystallographica* C41.
- Post, J.E. et al. (1983). Chalcotrichite: morphology and growth mechanism. *American Mineralogist* v.68.
- O'Leary, M.J. (1988). Cuprite stability in the copper oxidation zone. *Economic Geology*.
- Williams, P.A. (1990). *Oxide Zone Geochemistry*. Wiley.
- Robb, L. (2005). *Introduction to Ore-Forming Processes*. Blackwell (cuprite paragenesis, Chapter 7).
- Dana's System of Mineralogy, 7th Edition — Cuprite entry.
- Mindat.org — Cuprite locality data and photo gallery.
- Handbook of Mineralogy, Vol. 3 — Cuprite entry.
