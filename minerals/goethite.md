# Research: Goethite — Vugg Simulator

**Date:** 2026-05-20
**Researcher:** 🪨✍️ (cron expansion)
**Status:** Complete
**Paragenetic context:** Dimorph of lepidocrocite (γ-FeOOH). Forms from oxidation of pyrite, siderite, magnetite, and other Fe²⁺-bearing minerals. The thermodynamically stable iron oxyhydroxide at Earth surface conditions.

---

## Species: Goethite

### Identity
- **Formula:** α-FeO(OH) — iron(III) oxide-hydroxide, the alpha polymorph of FeOOH
- **Crystal system:** Orthorhombic, space group Pbnm (same structure as diaspore, AlO(OH))
- **Mineral group:** Oxide (hydroxide subgroup, diaspore group)
- **Hardness (Mohs):** 5.0–5.5
- **Specific gravity:** 3.3–4.3 (typically 4.0–4.3 for crystalline material, lower for earthy masses)
- **Cleavage:** Perfect on {010}
- **Fracture:** Uneven to splintery
- **Luster:** Adamantine to dull, metallic to earthy depending on habit and crystal size

### Color & Appearance
- **Typical color:** Yellowish-brown to dark brown, reddish-brown, nearly black. Sometimes with iridescent tarnish (rainbow colors from thin-film interference on oxidized surfaces).
- **Color causes:** O²⁻ → Fe³⁺ charge transfer transitions. The exact shade depends on particle size, degree of crystallinity, and minor element substitutions. Nanoscale goethite appears more yellow; coarser crystals appear darker brown to black.
- **Transparency:** Opaque to sub-translucent (thin fragments may transmit yellow-brown light)
- **Streak:** Brownish-yellow to orange-yellow — diagnostic and lighter than the mineral's surface color
- **Notable visual features:** Often forms pseudomorphs after other minerals (especially pyrite — the "iron cross" goethite pseudomorphs are classic). Velvety botryoidal surfaces with rainbow iridescence. Acicular sprays of fine needles with silky luster. Fossil replacements preserve organic textures in stunning detail.

### Crystal Habits
- **Primary habit:** Prismatic/acicular — needle-like to blade-like crystals elongated along [001]
- **Common forms/faces:** {010} prominent (perfect cleavage), {100}, {001}, often in radiating sprays or sheaves
- **Twin laws:** None commonly reported
- **Varieties:**
  - **Needle ironstone / needle iron ore:** Acicular crystals in radiating sprays
  - **Brown ochre:** Earthy, massive, used as pigment since Lascaux (~17,000 years ago)
  - **Bog iron:** Concretionary masses from swampy groundwater
- **Special morphologies:**
  - **Botryoidal:** Kidney-shaped, grape-like globular masses (famous from Colorado, Utah, Arizona)
  - **Stalactitic:** Hanging dripstone forms in caves and mine workings
  - **Pseudomorphs:** After pyrite (cubes with striations preserved), siderite (rhombohedra), marcasite, gypsum (stalactites). The crystal shape of the parent mineral is retained even as the chemistry completely changes.
  - **Oolitic:** Small round grains cemented together (important iron ore in the Great Lakes region)
  - **Reniform:** Kidney-shaped masses
  - **Gossan:** The weathered, oxidized "iron hat" capping sulfide ore deposits — often goethite + hematite + quartz + jarosite

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 0–300°C (enormous span — from ambient weathering to low-grade hydrothermal)
- **Optimal growth temperature:** 25–150°C (supergene/weathering zone optimal; hydrothermal goethite forms up to ~300°C)
- **Decomposition temperature:** ~250–400°C (dehydrates to hematite α-Fe₂O₃; the transformation is topotactic — crystal shape is preserved while internal structure rearranges)
- **Temperature-dependent habits:**
  - Low T (<100°C): Fine-grained, earthy, massive, or botryoidal
  - Moderate T (100–200°C): Acicular to prismatic crystals, often larger and more lustrous
  - High T (>200°C, hydrothermal): Coarse bladed crystals, sometimes pseudomorphing primary sulfides

#### Chemistry Required
- **Required elements in broth:** Fe³⁺ (the direct building block). In the simulator, goethite should nucleate when Fe²⁺ is oxidized to Fe³⁺ in the presence of water and OH⁻. Effectively: Fe > 20 ppm, O₂ present.
- **Optional/enhancing elements:**
  - Mn³⁺/Mn⁴⁺ → substitution darkens color toward black ("waddy" or manganese-rich goethite)
  - Al³⁺ → can substitute up to ~30% Al for Fe (aluminous goethite, common in bauxite and laterite)
  - Ni, Co, Cr → trace substitutions in lateritic goethite
- **Inhibiting elements:**
  - High silica (Si > 100 ppm) → can stabilize lepidocrocite or ferrihydrite instead, or form amorphous iron-silicate gels
  - Very high sulfate → favors jarosite or schwertmannite over goethite
  - Organic matter → complexes Fe, delays nucleation
  - Very high carbonate → may precipitate siderite instead if Eh is low
- **Required pH range:** 3–8 (broad). Optimal at mildly acidic to neutral (pH 5–7). Below pH 3, goethite dissolves; above pH 8, lepidocrocite or ferrihydrite may form preferentially.
- **Required Eh range:** Oxidizing (Eh > +0.2 V at pH 7). Goethite requires Fe³⁺, which forms when Fe²⁺ is oxidized.
- **Required O₂ range:** Presence of oxygen required — this is the hallmark of goethite formation. Even trace O₂ in groundwater is enough.

#### Secondary Chemistry Release
- **Does it release chemicals when forming?** Goethite formation consumes Fe²⁺ and oxidizes it, but the net effect depends on the precursor:
  - From pyrite oxidation: releases SO₄²⁻ + H⁺ (acid mine drainage chemistry)
  - From siderite oxidation: releases CO₂
  - From Fe²⁺(aq) oxidation: consumes H⁺ if oxidized by O₂ (4Fe²⁺ + O₂ + 6H₂O → 4FeO(OH) + 8H⁺... actually this is acid-generating in sulfide systems but can be pH-neutral in carbonate-buffered systems)
- **Byproducts of nucleation:** Removes dissolved Fe from fluid. Can acidify the broth if sulfide oxidation is the Fe source.
- **Byproducts of dissolution:** Releases Fe³⁺ (which hydrolyzes to Fe(OH)₃ colloid in neutral water) or dissolves as Fe³⁺(aq) in acid. Dissolution is congruent in strong acid: FeO(OH) + 3H⁺ → Fe³⁺ + 2H₂O
- **Byproducts of decomposition:** Dehydration to hematite releases H₂O (structural water) but returns no chemistry to the fluid.

#### Growth Characteristics
- **Relative growth rate:** Moderate — slower than malachite in oxidation zones, faster than hematite in weathering profiles. In the simulator, set to ~0.4× calcite baseline (matching current game implementation).
- **Maximum crystal size:** To 20+ cm (exceptional acicular crystals from Colorado). Pseudomorphs after pyrite can reach 10+ cm cubes.
- **Typical crystal size in vugs:** 0.1–3 cm for crystals; botryoidal masses can fill entire vug cavities
- **Does growth rate change with temperature?** Yes — higher T accelerates growth, but above ~250°C it dehydrates to hematite instead. Low-T goethite is typically fine-grained and earthy.
- **Competes with:**
  - **Lepidocrocite** (γ-FeOOH) — kinetically favored at rapid oxidation, neutral pH; goethite wins at slow oxidation, lower pH, or over time via dissolution-reprecipitation
  - **Hematite** (α-Fe₂O₃) — thermodynamically more stable at higher T; goethite dehydrates to hematite above ~250°C
  - **Jarosite** (KFe₃(SO₄)₂(OH)₆) — competes in low-pH, high-sulfate environments
  - **Siderite** (FeCO₃) — if Eh drops and CO₃²⁻ is available, siderite can form instead of or replace goethite

#### Stability
- **Breaks down in heat?** Yes — dehydrates to hematite (α-Fe₂O₃) starting at ~250°C, complete by ~400°C. The transformation is topotactic: external crystal shape is preserved.
- **Breaks down in light?** No — goethite is photostable (unlike realgar/pararealgar).
- **Dissolves in water?** Essentially insoluble in pure water. Solubility increases dramatically with acidity.
- **Dissolves in acid?** Yes — soluble in HCl and other strong acids. The classic field test: warm HCl dissolves goethite, leaving behind any quartz or silicates. This is how miners separated "iron hat" gossan material.
- **Oxidizes?** No — goethite is already fully oxidized (Fe³⁺). It is the *product* of iron oxidation.
- **Dehydrates?** Yes — to hematite at 250–400°C.
- **Radiation sensitivity:** Not notably radiation-sensitive, though radioactive inclusions (e.g., uraninite) can create pleochroic halos in surrounding goethite.

### Paragenesis
- **Forms AFTER:** Pyrite, marcasite, siderite, magnetite, chalcopyrite, or any Fe²⁺-bearing mineral exposed to oxidizing conditions. The classic sequence:
  ```
  Pyrite (FeS₂) → [oxidation] → dissolved Fe²⁺ + SO₄²⁻ + H⁺ → [further oxidation] → goethite
  Siderite (FeCO₃) → [oxidation] → Fe²⁺ + CO₂ → [oxidation + hydrolysis] → goethite
  Magnetite (Fe₃O₄) → [oxidation] → Fe³⁺ → [hydrolysis] → goethite
  ```
- **Forms BEFORE:** Hematite (at higher T or longer time scales). Goethite is the metastable-to-stable precursor that eventually dehydrates to hematite in hot, dry environments.
- **Commonly associated minerals:**
  - Pyrite, marcasite (as precursors for pseudomorphs)
  - Hematite (often intimately intergrown — "iron hat" gossan material)
  - Quartz (gangue in hydrothermal veins; goethite stains it yellow-brown)
  - Jarosite, alunite (acid-generating oxidation of sulfides)
  - Malachite, azurite (copper oxidation zone — goethite is the iron companion)
  - Smithsonite, hemimorphite (zinc oxidation zone)
  - Limonite (field term for mixtures of goethite + lepidocrocite + ferrihydrite)
- **Zone:** Supergene/oxidation zone. Weathering zone. Gossan. Also primary low-T hydrothermal.
- **Geological environment:**
  - **Gossans:** The oxidized cap over sulfide ore deposits (famous at Rio Tinto, Spain; Bingham Canyon, Utah)
  - **Bog iron:** Concretionary masses in swampy, reducing-oxidizing transition zones
  - **Laterites:** Tropical weathering profiles (highly aluminous goethite in bauxite)
  - **Cave deposits:** Stalactitic goethite from iron-rich groundwater
  - **Hydrothermal veins:** Low-temperature (<300°C) vein fillings, often as late-stage oxidation product
  - **Sedimentary iron formations:** The world's largest iron deposits (Lake Superior-type banded iron formations contain goethite as a weathering product of primary siderite, magnetite, or chert-hosted iron)

### Famous Localities
- **Crystal Peak / Lake George area, Park & Teller Cos., Colorado, USA:** Exceptionally sharp, lustrous acicular crystals — among the world's finest for the species. Needles to several cm with adamantine luster.
- **Pelican Point, Utah Co., Utah, USA:** Perfect goethite pseudomorphs after pyrite cubes — textbook examples where the pyrite crystal shape is preserved in goethite.
- **Copper Queen Mine, Bisbee, Cochise Co., Arizona, USA:** Attractive botryoidal goethite associated with famous copper minerals. Part of the same supergene oxidation zone that produced Bisbee's azurite and malachite.
- **Graves Mountain, Lincoln Co., Georgia, USA:** Highly iridescent goethite — rainbow surface films.
- **Santa Eulalia, Chihuahua, Mexico:** Fascinating elongated pseudomorphs after gypsum stalactites (hollow centers where gypsum dissolved).
- **Rio Tinto, Huelva, Spain:** The type locality of acid mine drainage — blood-red rivers from goethite/hematite/jarosite oxidation of massive pyrite deposits. The name "Rio Tinto" means "colored river."
- **Lascaux Caves, Dordogne, France:** Goethite was used as brown ochre pigment in cave paintings ~17,000 years ago. Evidence of humanity's relationship with this mineral predates agriculture.
- **Hollertszug Mine, Herdorf, Germany:** Type locality (first described 1806). Named after Johann Wolfgang von Goethe (1749–1832), the German polymath who was also a mineral enthusiast.

### Fluorescence
- **Fluorescent under UV?** No — goethite does not fluoresce under standard UV wavelengths. The Fe³⁺ ion quenches fluorescence.
- **SW (255nm):** None
- **MW (310nm):** None
- **LW (365nm):** None
- **Phosphorescent?** No
- **Activator:** N/A
- **Quenched by:** N/A (the Fe³⁺ itself is the quencher — iron oxyhydroxides are classic fluorescence killers)
- **Note:** While goethite itself does not fluoresce, it can **coat** fluorescent minerals and suppress their fluorescence. A goethite-coated fluorite will not glow. In the simulator, goethite presence could reduce fluorescence of nearby crystals.

### Flavor Text
*A short paragraph for the game's epilogue. Scientific but vivid. One hook that makes you remember the mineral. Match the voice of existing entries.*

> Goethite is rust with ambition. It starts as the oxidation of something else — pyrite, siderite, magnetite — and ends up preserving their shapes like a mineral taxidermist. Give it a pyrite cube and centuries of trickling oxygen, and it will hand you back the same crystal, striations and all, now made of yellow-brown iron instead of golden sulfur. The cave painters of Lascaux knew it as brown ochre. Modern miners know it as the "iron hat" — the rust-stained gossan capping every sulfide deposit, announcing treasure below. It is the most patient mineral in the oxidation zone: every other iron phase eventually becomes goethite, and goethite eventually becomes hematite, but goethite spends the longest time in between — stable, stubborn, and beautiful in its own earthy way.

### Simulator Implementation Notes
- **New parameters needed:** None — goethite uses Fe (already tracked) and O₂ (already tracked as oxidation state).
- **New events needed:**
  - `pyrite_weathering` — when pyrite is exposed to O₂, it should generate acid (lower pH) and dissolved Fe²⁺, which then oxidizes to goethite
  - `siderite_decomp_oxidation` — siderite thermal decomposition in oxidizing conditions produces goethite instead of magnetite/wüstite
  - `pseudomorph_growth` — special habit for goethite replacing pyrite/siderite
- **Nucleation rule pseudocode:**
```
IF temperature < 300°C
   AND Fe_ppm > 20
   AND O2_present (oxidizing conditions)
   AND pH > 3
   AND NOT (sulfate > 200 AND pH < 4)  // jarosite wins here
   AND NOT (silica > 150 AND rapid_oxidation)  // lepidocrocite wins here
   THEN nucleate goethite
```
- **Growth rule pseudocode:**
```
IF temperature < 250°C
   AND Fe_ppm > 20
   AND O2_present
   AND pH > 3
   THEN grow at rate 0.4 × calcite_baseline
   
IF temperature > 250°C
   THEN transform to hematite (dehydration)
```
- **Habit selection logic:**
  - If replacing pyrite/marcasite/siderite (pseudomorph_after flag set) → inherit parent habit
  - If σ > 2.0 and T < 100°C → botryoidal (globular masses)
  - If σ moderate and T 100–200°C → acicular (needles)
  - If σ low and T moderate → massive/earthy
  - If in cave/vug environment with dripping water → stalactitic
- **Decomposition products:**
  - At 250–400°C: goethite → hematite (α-Fe₂O₃) + H₂O
  - The hematite retains the goethite crystal shape (topotactic transformation)

### Variants for Game
- **Variant 1: Needle Ironstone** — Acicular crystals in radiating sprays, moderate σ, T 100–200°C. High luster. Classic Colorado style.
- **Variant 2: Botryoidal Gossan** — Grape-like globular masses, high σ, low T (<100°C). Often with rainbow iridescence. Forms from rapid oxidation of pyrite in humid conditions.
- **Variant 3: Pyrite Pseudomorph** — Cube-shaped with preserved striations, but composed entirely of goethite. Only nucleates when pyrite is actively dissolving/oxidizing. The ultimate trophy — a pyrite that became goethite but kept its pride.

---

## Completed Species (link to research files)
- Lepidocrocite → `memory/research-lepidocrocite.md` (dimorph — same formula, different structure)
- Pyrite → `memory/research-pyrite.md` (primary precursor for pseudomorphs)
- Marcasite → `memory/research-pyrite-marcasite.md` (polymorph of pyrite, also oxidizes to goethite)
- Siderite → `memory/research-siderite.md` (carbonate precursor, decomposes to goethite)
- Hematite → `memory/research-hematite.md` (dehydration product at high T)
- Magnetite → `memory/research-magnetite.md` (precursor via oxidation)

---

*"Goethite is the answer to the question: what happens when you leave iron out in the rain for ten thousand years?"*
