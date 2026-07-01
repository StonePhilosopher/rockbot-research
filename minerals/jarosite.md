# Research: Jarosite — Vugg Simulator

**Date:** 2026-05-27
**Species:** Jarosite
**Researcher:** 🪨✍️ (cron expansion)
**Status:** Complete
**Paragenetic context:** Iron oxidation zone / acid sulfate environment. Forms alongside goethite, hematite, alunite, and other iron oxyhydroxides in the weathered "iron hat" (gossan) capping sulfide ore deposits. Part of the broader iron oxide-sulfate supergene sequence.

---

## Species: Jarosite

### Identity
- **Formula:** KFe³⁺₃(SO₄)₂(OH)₆
- **Crystal system:** Trigonal (rhombohedral, space group R3m)
- **Mineral group:** Sulfate — alunite supergroup (jarosite subgroup, B-site = Fe³⁺)
- **Hardness (Mohs):** 2.5–3.5
- **Specific gravity:** 2.9–3.3 (typically ~3.15–3.26)
- **Cleavage:** Distinct on {0001} (basal)
- **Fracture:** Uneven to conchoidal
- **Luster:** Subadamantine to vitreous; resinous on fractures

### Color & Appearance
- **Typical color:** Amber yellow to dark yellowish-brown; sometimes reddish-brown or ochre
- **Color causes:** O²⁻ → Fe³⁺ charge transfer transitions. The Fe³⁺ in octahedral coordination absorbs in the blue-violet, transmitting yellow-brown. Higher Fe³⁺ concentration or finer grain size deepens the color toward brown.
- **Transparency:** Transparent to translucent in thin fragments; opaque in massive aggregates
- **Streak:** Light yellow — diagnostic and much paler than the surface color
- **Notable visual features:** Often confused with limonite or goethite in the field because it shares the same environments. Pseudocubic crystals are the hallmark — they look like tiny cubes but are actually trigonal. Strongly pyroelectric (generates charge when heated). Barely detectable radioactivity from trace K-40.

### Crystal Habits
- **Primary habit:** Pseudocubic — crystals appear cubic but belong to the trigonal system. The {1011} rhombohedron dominates, giving a cube-like appearance.
- **Common forms/faces:** {1011} rhombohedron (dominant, creates pseudocubic look), {0001} basal pinacoid, {1120} prism. Rare true cubes — the pseudocubic habit is a crystallographic illusion.
- **Twin laws:** None commonly reported
- **Varieties:**
  - **Natrojarosite** — Na > K substitution. Common in nature; Na/K ratios to 1:2.4 documented. Oscillatory zoning between jarosite and natrojarosite observed at Apex Mine, Arizona and Gold Hill, Utah.
  - **Hydronium jarosite** — H₃O⁺ substitutes for K⁺. Forms from alkali-deficient solutions. Decreased c lattice parameter.
  - **Argentojarosite** — Ag⁺ in the A site. Rare, from silver-rich oxidation zones.
  - **Plumbojarosite** — Pb²⁺ in the A site (with charge balance via A-site vacancies).
  - **Beaverite** — Pb²⁺ + Cu²⁺ substitution in A and B sites.
- **Special morphologies:** Granular crusts, nodules, fibrous masses, concretionary aggregates, reniform (kidney-shaped) masses, minute crystals in acid sulfate soils

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** Ambient to ~150°C. Optimal below 100°C. End-member jarosite and natrojarosite favored at T < 100°C.
- **Optimal growth temperature:** 25–80°C (supergene/weathering zone). Higher T up to ~150°C possible in low-grade hydrothermal or fumarolic settings.
- **Decomposition temperature:** ~400–500°C (dehydrates and decomposes; structural OH and SO₄ break down)
- **Temperature-dependent habits:**
  - Low T (<50°C): Fine-grained, earthy, massive, or as minute crystals in soils
  - Moderate T (50–100°C): Better-formed pseudocubic crystals, crusts on vug walls
  - Higher T (>100°C, rare): Larger, more distinct crystals; hydrothermal occurrences

#### Chemistry Required
- **Required elements in broth:** Fe³⁺ (minimum ~20 ppm), K⁺ (or Na⁺/H₃O⁺ for natrojarosite/hydroniumjarosite), SO₄²⁻ (from pyrite oxidation or other sulfide weathering)
- **Optional/enhancing elements:** Na (→ natrojarosite), Ag (→ argentojarosite), Pb (→ plumbojarosite), Cu (→ beaverite), Al (→ alunite solid solution — intermediate members rare but documented)
- **Inhibiting elements:**
  - High Ca → gypsum or anhydrite precipitates instead, competing for sulfate
  - Very high silica → ferrihydrite or amorphous silica-iron gels
  - Low sulfate → goethite or hematite form instead (no jarosite without SO₄)
  - Neutral to alkaline pH → goethite/hematite stable; jarosite requires acid
- **Required pH range:** 1.5–3.5 (strongly acidic). Optimal pH ~2–3. Above pH 3.5, goethite becomes thermodynamically favored. Below pH 1.5, jarosite dissolves.
- **Required Eh range:** Strongly oxidizing (Eh > +0.6 V at pH 2–3). Fe must be fully oxidized to Fe³⁺.
- **Required O₂ range:** High. Jarosite is an oxidation product. Needs oxygen to oxidize Fe²⁺ → Fe³⁺ and to maintain the sulfate.

#### Secondary Chemistry Release
- **Does it release chemicals when forming?** Jarosite precipitation CONSUMES acid (H⁺) from the fluid: 3Fe³⁺ + 2SO₄²⁻ + K⁺ + 6H₂O → KFe₃(SO₄)₂(OH)₆ + 6H⁺. Wait — this generates acid! Actually, the net reaction from pyrite oxidation is: 2FeS₂ + 7.5O₂ + H₂O → Fe₂(SO₄)₃ + H₂SO₄, then Fe₂(SO₄)₃ + K⁺ + 6H₂O → 2KFe₃(SO₄)₂(OH)₆ + ... The full chain is acid-generating. Jarosite formation temporarily buffers pH by consuming Fe³⁺ and some SO₄, but the overall oxidation of sulfide ores is acid-producing.
- **Byproducts of nucleation:** Removes Fe³⁺ and SO₄²⁻ from fluid. Can buffer pH in acid mine drainage systems by precipitating as a solid phase, temporarily reducing dissolved metal loads.
- **Byproducts of dissolution:** Dissolves in acid, releasing K⁺, Fe³⁺, SO₄²⁻, and OH⁻. In the simulator, dissolution should acidify the fluid further (jarosite dissolution in AMD is self-sustaining once started).
- **Byproducts of decomposition:** Thermal decomposition releases SO₃/SO₂, H₂O, and leaves iron oxide residue (hematite or maghemite).

#### Growth Characteristics
- **Relative growth rate:** Moderate to fast in acid mine drainage conditions. Rapid nucleation when pH drops below 3 and Fe³⁺/SO₄ are available. Slower in natural weathering profiles.
- **Maximum crystal size:** Exceptional crystals to ~2 cm (rare); typically <1 mm. Mammoth Mine, Tintic, Utah produced notable specimens.
- **Typical crystal size in vugs:** 0.1–2 mm pseudocubic crystals; often as crusts or coatings rather than free-standing crystals.
- **Does growth rate change with temperature?** Yes — higher T accelerates nucleation but narrows the stability field (goethite wins above ~100°C at moderate pH). Low T favors persistence but slow growth.
- **Competes with:**
  - **Goethite** — the main competitor. At pH > 3 or lower sulfate, goethite wins. At pH < 3 with abundant sulfate, jarosite wins. The jarosite-goethite boundary is one of the most important mineralogical transitions in acid mine drainage.
  - **Hematite** — at higher T or dehydration
  - **Schwertmannite** — Fe₈O₈(OH)₆(SO₄)·nH₂O, a metastable precursor that often transforms to goethite or jarosite
  - **Ferrihydrite** — amorphous Fe(OH)₃ precursor, transforms to goethite or jarosite depending on pH and sulfate
  - **Alunite** — if Al is abundant and Fe is scarce
  - **Gypsum/anhydrite** — for sulfate at higher pH or Ca-rich conditions

#### Stability
- **Breaks down in heat?** Yes — decomposes at 400–500°C. Releases structural water and sulfate, leaving iron oxide.
- **Breaks down in light?** No — photostable.
- **Dissolves in water?** Very slightly soluble in pure water. Solubility increases dramatically with acidity.
- **Dissolves in acid?** Yes — soluble in HCl and other strong acids. This is the classic test: jarosite dissolves in warm HCl, distinguishing it from goethite (which is more resistant).
- **Oxidizes?** No — already fully oxidized (Fe³⁺ only). It IS an oxidation product.
- **Dehydrates?** Not directly to a simple anhydrous form, but thermal decomposition at >400°C produces hematite + volatiles.
- **Radiation sensitivity:** Barely detectable radioactivity from K-40. No significant radiation damage effects documented.

### Paragenesis
- **Forms AFTER:** Pyrite, marcasite, chalcopyrite, or any iron sulfide exposed to oxidizing, acidic conditions. The classic sequence:
  ```
  Pyrite (FeS₂) → [oxidation] → dissolved Fe²⁺ + SO₄²⁻ + H⁺ (acid)
    ↓ further oxidation
  Fe³⁺(aq) + SO₄²⁻ + K⁺/Na⁺
    ↓ pH < 3, abundant sulfate
  Jarosite (KFe₃(SO₄)₂(OH)₆)
  ```
  Intermediate steps often include ferrihydrite or schwertmannite as amorphous precursors.
- **Forms BEFORE:** Goethite (at higher pH or over longer time scales), hematite (at higher T or from dehydration). In acid sulfate soils, jarosite persists until pH rises (e.g., by liming or natural buffering).
- **Commonly associated minerals:**
  - Goethite, limonite ( intimately intergrown in gossans)
  - Hematite (in oxidized caps)
  - Gypsum, anglesite, cerussite (sulfate minerals from the same oxidation)
  - Malachite, azurite, chalcanthite (copper oxidation zone companions)
  - Native sulfur (in strongly oxidizing, low-pH environments)
  - Alunite (in alkali-rich, aluminum-bearing systems)
  - Ferrihydrite, schwertmannite (precursor phases)
- **Zone:** Supergene oxidation zone, acid mine drainage (AMD), acid sulfate soils, gossan (iron cap), fumarolic deposits
- **Geological environment:**
  - **Gossans:** The rust-stained oxidized cap over sulfide ore deposits (classic with goethite + hematite)
  - **Acid mine drainage:** Active and abandoned mine sites where pyrite oxidation generates acid (pH < 3) and jarosite precipitates in stream beds, ponds, and tailings
  - **Acid sulfate soils:** Coastal and inland soils with buried sulfide layers; jarosite forms when these are drained and exposed to oxygen
  - **Hydrothermal veins:** Rare, low-T (<150°C) occurrences in vugs and fractures
  - **Fumaroles:** Volcanic fumarole deposits (e.g., Vulcano, Italy)
  - **Mars:** Detected by Spirit, Opportunity, and Curiosity rovers — evidence of past acidic, oxidizing aqueous environments

### Famous Localities
- **Classic locality 1:** Barranco del Jaroso, Sierra Almagrera, Almería, Spain — type locality (1852). Named after the yellow-flowered *Cistus* shrub (*jara* in Spanish) that grows there. The mineral and the flower share the same color.
- **Classic locality 2:** Apex Mine, Arizona and Gold Hill, Utah — oscillatory zoning of jarosite/natrojarosite documented. Important for understanding the jarosite-natrojarosite miscibility gap.
- **Classic locality 3:** Mammoth Mine, Tintic District, Juab County, Utah — notable larger crystals.
- **Notable specimens:**
  - Sierra Peña Blanca, Aldama, Chihuahua, Mexico — well-formed pseudocubic crystals
  - Bisbee and Tombstone, Cochise County, Arizona — associated with famous copper minerals
  - Iron Arrow Mine, Chaffee County, Colorado
  - Rio Tinto, Huelva, Spain — massive jarosite in one of the world's most famous acid mine drainage sites (the river runs red from iron oxides and jarosite)
  - Barranco del Jaroso, Spain — type locality
  - Antarctica — discovered in deep ice cores (2021), speculated to be from atmospheric dust. Also relevant to Mars: if jarosite can form in Antarctic ice, it could form in Martian ice/dust deposits.

### Fluorescence
- **Fluorescent under UV?** No
- **SW (255nm) color:** None
- **MW (310nm) color:** None
- **LW (365nm) color:** None
- **Phosphorescent?** No
- **Activator:** N/A
- **Quenched by:** Fe³⁺ itself quenches fluorescence. Jarosite, like goethite and hematite, is a fluorescence killer.
- **Note:** Jarosite coatings on fluorescent minerals (fluorite, calcite) will suppress their fluorescence. In the simulator, jarosite presence could reduce or eliminate fluorescence of underlying crystals.

### Flavor Text

> Jarosite is the mineral that thrives where nothing else wants to live. It crystallizes in acid strong enough to etch steel, in the runoff from dying pyrite, in the blood-red rivers of Rio Tinto where pH drops below 2 and fish vanished centuries ago. Its crystals are a trick — they look like tiny cubes, cubic as salt, but tilt them in polarized light and the truth comes out: trigonal, rhombohedral, a hexagonal soul wearing cubic clothes. It needs three things that don't usually coexist: iron, sulfate, and a pH so low that goethite gives up and goes home. Where pyrite weathers and oxygen wins, jarosite is the scab that forms over the wound — yellow, brittle, and strangely beautiful. It was first found in Spain, named for a yellow wildflower, and later discovered on Mars. That span — from an Andalusian riverbed to the dust of another planet — tells you everything about how universal acid and iron really are.

### Simulator Implementation Notes
- **New parameters needed:** trace_K (already in some scenarios). pH tracking already exists. SO₄ may need explicit tracking (currently S is tracked as total sulfur; oxidation state matters for jarosite).
- **New events needed:**
  - `acid_mine_drainage_cascade` — when pyrite oxidizes in water, generate H⁺ (lower pH) and dissolved Fe²⁺/SO₄, then oxidize Fe²⁺ → Fe³⁺, then precipitate jarosite if pH < 3 and K/Na available
  - `jarosite-goethite_transition` — when pH rises above 3.5, existing jarosite should dissolve and reprecipitate as goethite
  - `natrojarosite_zoning` — if Na > K, natrojarosite forms instead; oscillatory zoning possible with fluctuating Na/K
- **Nucleation rule pseudocode:**
```
IF temperature < 150°C
   AND Fe_ppm > 30
   AND SO4_ppm > 50
   AND (K_ppm > 10 OR Na_ppm > 10 OR H3O_present)
   AND pH < 3.5
   AND pH > 1.5
   AND O2_present (oxidizing)
   THEN nucleate jarosite
   
   IF K > Na → jarosite
   IF Na > K → natrojarosite
   IF both low → hydroniumjarosite (rare, low pH)
```
- **Growth rule pseudocode:**
```
IF temperature < 150°C
   AND Fe_ppm > 20
   AND SO4_ppm > 30
   AND pH < 3.5
   THEN grow at rate 0.5 × calcite_baseline
   
IF pH rises above 3.5:
   dissolve jarosite → release Fe³⁺ + SO₄²⁻ + K⁺
   nucleate goethite instead
```
- **Habit selection logic:**
  - Default → pseudocubic (the trigonal rhombohedron that looks cubic)
  - High σ, rapid growth → granular crusts or nodules
  - Low σ, slow growth → better-formed pseudocubic crystals
  - In soils/AMD → fine-grained, earthy, massive
- **Decomposition products:**
  - At 400–500°C: jarosite → hematite (or maghemite) + SO₃/SO₂ + H₂O
  - In neutral/alkaline conditions: dissolves → Fe³⁺(aq) + SO₄²⁻ + K⁺ + OH⁻

### Variants for Game
- **Variant 1: Pseudocubic Jarosite** — Well-formed crystals appearing cubic. Moderate σ, T 25–80°C, pH 2–3. The "trophy" form — rare and distinctive.
- **Variant 2: Natrojarosite** — Na-dominant variety. Forms when Na > K in the broth. Same pseudocubic habit but with oscillatory zoning possible (banded Na/K layers). Gold Hill, Utah style.
- **Variant 3: Acid Mine Drainage Crust** — Granular, earthy, massive. High σ, rapid nucleation, pH < 2. Covers vug walls in thick yellow-brown crusts. The most common natural form but least collectible.
- **Variant 4: Rio Tinto Sulfur Companion** — Forms alongside native sulfur in strongly oxidizing, very low pH conditions. Rare in nature but visually striking: bright yellow jarosite + bright yellow sulfur. Vulcano, Italy style fumarolic occurrence.

---

## Linked Sequence: Iron Oxide-Sulfate Paragenesis

Jarosite belongs to the broader **iron oxidation zone sequence**:
1. **Pyrite/marcasite** (FeS₂) — primary sulfide, reduced, forms first
2. **Ferrihydrite/schwertmannite** — amorphous/metastable precursors (Fe(OH)₃ or Fe₈O₈(OH)₆(SO₄))
3. **Jarosite** (KFe₃(SO₄)₂(OH)₆) — stable at pH < 3, high sulfate, oxidizing
4. **Goethite** (α-FeOOH) — stable at pH > 3, lower sulfate, or over long time scales
5. **Hematite** (α-Fe₂O₃) — dehydration product at higher T, or final oxidation endpoint

The jarosite-goethite boundary is pH-dependent and is one of the most important transitions in acid mine drainage geochemistry. In the simulator, crossing pH 3 should trigger a dissolution/reprecipitation event.

See also:
- `memory/research-hematite.md`
- `memory/research-magnetite.md`
- `memory/research-goethite.md`
- `memory/research-lepidocrocite.md`
- `memory/research-pyrite.md`

---

*"Jarosite is the mineral proof that acidity is a place, not just a condition. It builds crystals in pH 2, names itself after a flower, and waits patiently on Mars for someone to notice."*
