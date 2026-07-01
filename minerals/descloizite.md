# Research: Descloizite

**Date:** 2026-05-11
**Status:** Complete — ready for Vugg Simulator implementation
**Paragenetic partner:** Mottramite (see `memory/research-mottramite.md`)

---

## Species: Descloizite

### Identity
- **Formula:** PbZn(VO₄)(OH) — ideal end-member; natural material is (Pb,Zn)₂(OH)VO₄ with Zn > Cu
- **Crystal system:** Orthorhombic
- **Space group:** Pnma (no. 62)
- **Crystal class:** Dipyramidal (mmm)
- **Mineral group:** Adelite-Descloizite group / Vanadates
- **Hardness (Mohs):** 3 – 3.5
- **Specific gravity:** 6.1 – 6.2 (exceptionally heavy due to lead content)
- **Cleavage:** None
- **Fracture:** Irregular, sub-conchoidal
- **Tenacity:** Brittle
- **Luster:** Greasy, slightly resinous

### Color & Appearance
- **Typical color:** Deep cherry-red, brownish red, red-orange, reddish to blackish brown, nearly black
- **Color causes:** Intervalence charge transfer between V⁵⁺ and structural distortions in the Pb-dominant lattice; Zn²⁺ does not contribute chromophore behavior
- **Transparency:** Transparent to opaque
- **Streak:** Orange-yellow to brownish red
- **Notable visual features:** Often forms zoned crystals with color banding from center to rim; encrustations show mammillary (breast-like) surface texture; plumose aggregates resemble tiny feathers

### Crystal Habits
- **Primary habit:** Zoned tabular crystals, short prismatic, pyramidal
- **Common forms/faces:** Tabular on {010}, prismatic along [001], dipyramids
- **Twin laws:** None commonly reported
- **Varieties:**
  - **Cuprodescloizite:** dull green variety with Cu substituting for Zn (now recognized as intermediate toward mottramite)
  - **Arsendescloizite:** arsenate analogue with AsO₄ replacing VO₄
- **Special morphologies:** Drusy crusts, stalactitic aggregates, fibrous encrustations with mammillary surfaces, plumose (feathery) sprays

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 15–80°C (supergene/oxidation zone, low temperature)
- **Optimal growth temperature:** 20–40°C (ambient to slightly warm groundwater)
- **Decomposition temperature:** ~650°C (dehydrates and decomposes to lead vanadate oxides)
- **Temperature-dependent habits:** Lower temperatures favor fibrous/mammillary forms; slightly warmer conditions allow better crystal development

#### Chemistry Required
- **Required elements in broth:** Pb (≥200 ppm), Zn (≥100 ppm), V (≥50 ppm)
- **Optional/enhancing elements:** Cu (up to ~30% substitution toward mottramite), Ga, Ge (trace incorporation documented)
- **Inhibiting elements:** High Fe²⁺ (competes for oxidation zone precipitation), high CO₃²⁻ (favors cerussite over vanadates), high PO₄³⁻ (favors pyromorphite), high AsO₄³⁻ (forms arsendescloizite instead)
- **Required pH range:** 5.5–8.5 (weakly acidic to mildly alkaline)
- **Required Eh range:** Oxidizing (>+0.2V) — requires oxygenated groundwater
- **Required O₂ range:** >2 ppm dissolved O₂

#### Secondary Chemistry Release
- **Does it release chemicals when forming?** Consumes OH⁻ from solution; local pH may shift slightly acidic during rapid growth
- **Byproducts of nucleation:** None significant
- **Byproducts of dissolution/decomposition:** Releases Pb²⁺, Zn²⁺, V⁵⁺ into solution; dehydration yields H₂O vapor

#### Growth Characteristics
- **Relative growth rate:** Moderate to fast (compared to quartz baseline = 1, descloizite ≈ 3–5)
- **Maximum crystal size in nature:** Up to 2 cm individual crystals; crusts to 10+ cm
- **Typical crystal size in vugs:** 0.5–3 mm crystals in drusy crusts
- **Does growth rate change with temperature?** Yes — faster at 30–50°C, slower below 15°C
- **Competes with:** Vanadinite (if Cl available), wulfenite (if Mo available and pH drops), cerussite (if CO₃ dominates), mottramite (if Cu > Zn in fluid)

#### Stability
- **Breaks down in heat?** Yes — dehydrates above ~300°C, full decomposition by 650°C
- **Breaks down in light?** No — photostable
- **Dissolves in water?** Very low solubility; dissolves slowly in acidic groundwater (pH < 5)
- **Dissolves in acid?** Readily soluble in HCl and HNO₃ with effervescence from carbonate impurities
- **Oxidizes?** Already fully oxidized (V⁵⁺, Pb²⁺, Zn²⁺); no further oxidation possible under natural conditions
- **Dehydrates?** Yes — loses water above 300°C, becoming metadescloizite (unstable, rehydrates in humid air)
- **Radiation sensitivity:** U/Th inclusions may cause mild radiation darkening over geological time

### Paragenesis
- **Forms AFTER:** Galena (PbS) must oxidize first to release Pb²⁺; sphalerite (ZnS) must oxidize to release Zn²⁺; primary vanadium minerals (e.g., roscoelite in host rock) must weather to release V
- **Forms BEFORE:** Mottramite may replace descloizite if Cu/Zn ratio increases in late fluids; secondary carbonates may encrust it
- **Commonly associated minerals:** Vanadinite, wulfenite, pyromorphite, mimetite, cerussite, mottramite, anglesite, smithsonite, hemimorphite
- **Zone:** Supergene/oxidation zone
- **Geological environment:** Oxidized portions of lead-zinc vein deposits; gossans; calcrete profiles in arid climates

### Famous Localities
- **Berg Aukas, Namibia:** The world's finest descloizite — deep cherry-red spear-point bladed crystals to 3+ cm, zoned, transparent. Type locality for exceptional quality.
- **Tsumeb Mine, Namibia:** Superb crystals in oxidation zones, often intergrown with mottramite and smithsonite. Associated with the world's greatest mineral diversity.
- **Sierra de Córdoba, Argentina:** Original discovery locality (1854), named for Alfred Des Cloizeaux.
- **Otavi Mountain Land, Namibia:** Extensive descloizite-mottramite solid solution series documented by Millman (1960).
- **Minas do Lueca, Angola:** Classic African locality for the series.
- **Ojuela Mine, Mapimí, Mexico:** Fine drusy crusts with wulfenite.
- **Arizona and New Mexico, USA:** Encrustations in oxidized Pb-Zn deposits.

### Fluorescence
- **Fluorescent under UV?** No — non-fluorescent
- **Activator:** None
- **Quenched by:** Fe²⁺ (if present) would quench any potential fluorescence, but vanadates are generally non-fluorescent

### Flavor Text

> Descloizite is the blood of the oxidation zone — cherry-red crystals that form where lead and zinc sulfides surrender to rain and oxygen. Named for Alfred Des Cloizeaux, the French crystallographer who could read a mineral's soul in its optical angles, this mineral carries the weight of lead (specific gravity over 6) in forms so delicate they seem impossible. At Berg Aukas in Namibia, spear-point crystals grow in zoned tabular splendor, transparent as stained glass, banded from deep crimson core to amber rim. It is the zinc end of a continuous bridge to mottramite, and nature seldom chooses pure end-members — most descloizite carries a ghost of copper in its lattice, a whisper of what it might have been had the groundwater chemistry shifted. It forms drusy crusts, stalactites, and mammillary masses that coat cavity walls like the viscera of some mineral beast. In the vug, it arrives late: after galena has given up its sulfur, after vanadium has leached from clay minerals, when the fluid is cool and oxidizing and just acidic enough to keep lead mobile until the moment of precipitation. It does not fluoresce. It does not need to. Its color is its own light.

---

## Shared Paragenetic Sequence: Descloizite-Mottramite Series

These two minerals form a complete solid solution series:
- **Descloizite** = Zn-dominant end member: PbZn(VO₄)(OH)
- **Mottramite** = Cu-dominant end member: PbCu(VO₄)(OH)

Natural specimens are almost always intermediate. The Cu:Zn ratio in the crystal reflects the Cu:Zn ratio in the precipitating fluid. Where fluids are Zn-rich (sphalerite-dominated oxidation zones), descloizite forms. Where fluids are Cu-rich (chalcopyrite-dominated zones), mottramite forms. Where both metals are present in comparable amounts, a single crystal may grade from descloizite core to mottramite rim, or vice versa, recording the evolving chemistry of the oxidation zone like a dendrochronology of groundwater.

Both minerals share:
- Same orthorhombic crystal system (Pnma)
- Same crystal habit range (tabular, prismatic, botryoidal, encrusting)
- Same formation environment (oxidation zone of base metal deposits)
- Same temperature range (15–80°C supergene)
- Same pH range (5.5–8.5)
- Same geological associations (vanadinite, wulfenite, cerussite, smithsonite)
- Same luster (greasy)
- Same hardness (~3–3.5)
- Same exceptional specific gravity (~5.9–6.2 from lead content)

The series was first studied systematically by Millman (1960) on material from Minas do Lueca, Angola, and later from the Otavi Mountain Land, Namibia.

---

### Simulator Implementation Notes

- **New parameters needed:** None — uses existing Pb, Zn, Cu, V, pH, Eh, O₂ tracking
- **New events needed:** `event_zinc_pulse` (for descloizite-dominant scenarios) — analogous to existing Cu/Mo pulses
- **Nucleation rule pseudocode:**
```
IF Pb ≥ 200 ppm AND Zn ≥ 100 ppm AND V ≥ 50 ppm
   AND pH 5.5–8.5 AND Eh > +0.2V AND T 15–80°C
   AND Cu:Zn_ratio < 1.0
   → nucleate descloizite (priority over mottramite if Zn dominates)
```
- **Growth rule pseudocode:**
```
IF σ_descloizite > 1.0 AND vug_fill < 0.85
   → grow at rate 4× quartz_baseline
   → habit: tabular if T > 30°C, mammillary if T < 25°C
```
- **Habit selection logic:**
  - T > 35°C + slow growth → tabular crystals, zoned
  - T 20–35°C + moderate growth → prismatic clusters
  - T < 25°C + fast growth → drusy crusts, mammillary masses
  - Very low T + high σ → plumose/feathery aggregates
- **Decomposition products:** Above 650°C → lead vanadate oxide (amorphous) + ZnO + H₂O vapor
- **Solid solution mechanic:** If Cu > Zn in fluid during growth, crystal composition shifts toward mottramite; display as zoned color change (red-brown core → green-black rim)

### Variants for Game

- **Variant 1: Berg Aukas Blades** — Large (2–3 cm), transparent, zoned tabular crystals with cherry-red to amber color gradient. Requires slow growth (low σ, long time) at 30–40°C.
- **Variant 2: Mammillary Crust** — Drusy crust with breast-like rounded surfaces, opaque to translucent, deep brown-red. Fast growth at low temperature (<25°C).
- **Variant 3: Cuprodescloizite** — Green-tinged variety with partial Cu substitution. Forms when Cu:Zn ~0.3–0.8. Color dull olive-green to brown-green. Bridge toward mottramite.
- **Variant 4: Stalactitic** — Elongated concretionary forms hanging from vug ceiling. Rare, requires dripping conditions and long growth time.

---

*Research compiled from Wikipedia, Mindat, Handbook of Mineralogy, and Millman (1960) American Mineralogist 45:763.*
