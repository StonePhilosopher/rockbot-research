# Zinc Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-06-03
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering sphalerite, wurtzite, smithsonite, aurichalcite, and rosasite as a single pH-Eh-Cu-ratio-controlled mineral system.
**Related files:**
- `memory/research-sphalerite.md` — (Zn,Fe)S, cubic primary sulfide
- `memory/research-wurtzite.md` — (Zn,Fe)S, hexagonal polymorph
- `memory/research-smithsonite.md` — ZnCO₃, secondary carbonate
- `memory/research-aurichalcite.md` — (Zn,Cu)₅(CO₃)₂(OH)₆, Cu-Zn carbonate
- `memory/research-rosasite.md` — (Cu,Zn)₂(CO₃)(OH)₂, Cu-Zn carbonate
- `memory/research-broth-ratio-sphalerite-wurtzite.md` — Polymorph competition model

---

## The Story This Sequence Tells

The zinc oxidation zone is the story of what happens when a zinc sulfide body meets oxygen, water, and sometimes copper. It's simpler than the copper oxidation zone — zinc only has one oxidation state (Zn²⁺) — but the chemistry is subtle and beautiful.

Where copper dances between Cu⁰, Cu⁺, and Cu²⁺, zinc is monogamous: always Zn²⁺. The drama isn't in redox. It's in **what anion Zn²⁺ pairs with** as conditions change, and **what happens when copper shows up** to share the dance floor.

This sequence teaches two lessons the copper zone can't:
1. **Polymorph competition** — same composition, different structure, temperature-and-pH-dependent
2. **Solid-solution branching** — two metals (Cu + Zn) competing for the same carbonate ligand, with ratio determining the winner

---

## The Full Sequence (Deep to Surface)

```
DEPTH                                          SURFACE
  │                                              │
  ▼                                              ▼

Primary zone (hypogene):
  Sphalerite (Zn,Fe)S ──► Wurtzite (Zn,Fe)S
         │                    (hexagonal polymorph)
         │                    low pH, kinetic trapping
         │
         │ uplift + exposure to O₂ + H₂O + CO₂
         ▼
Oxidation zone (supergene):

  Reducing ───────────────────────────────────── Oxidizing
         │                                              │
         ▼                                              ▼

  If Cu is ABSENT or LOW:
         │
         └──► Smithsonite (ZnCO₃)
                  │
                  ├──► Pure ZnCO₃: white, grey, yellow
                  ├──► Cuprian: blue (Cu substitutes for Zn)
                  ├──► Cobaltoan: pink (Co substitutes for Zn)
                  └──► "Turkey fat": yellow (CdS inclusions)

  If Cu is PRESENT (mixed Cu-Zn oxidation zone):
         │
         ├──► HIGH Zn : Cu ratio (~5:4 or more)
         │      └──► Aurichalcite (Zn,Cu)₅(CO₃)₂(OH)₆
         │            Pale green, tufted sprays
         │            The Zn-dominant partner
         │
         └──► HIGH Cu : Zn ratio (~3:2 or more)
                └──► Rosasite (Cu,Zn)₂(CO₃)(OH)₂
                      Blue-green, botryoidal crusts
                      The Cu-dominant partner
```

---

## Phase Diagram: pH vs Cu:Zn Ratio at Fixed Eh (+0.4V, 25°C)

```
     pH
      ▲
   9  │  Smithsonite    │    Rosasite
      │  (pure Zn)      │    (Cu-rich)
   8  │─────────────────┼─────────────────
      │  Aurichalcite   │
   7  │  (mixed Zn/Cu)  │
      │                 │
   6  │  Wurtzite       │  Sphalerite
      │  (low pH)       │  (neutral pH)
      └─────────────────┼─────────────────► Cu:Zn ratio
      low               │              high
      0:1              1:1             3:1
```

**Key insight:** At low Cu:Zn ratios, smithsonite or aurichalcite forms depending on pH. At high Cu:Zn ratios, rosasite dominates regardless of pH (above 6). The sphalerite/wurtzite boundary is controlled by pH and temperature, not Cu content.

---

## The Polymorph Story: Sphalerite vs Wurtzite

Same formula: (Zn,Fe)S. Same elements. Different crystal structure.

| Feature | Sphalerite | Wurtzite |
|---|---|---|
| Structure | Cubic (ABCABC stacking) | Hexagonal (ABABAB stacking) |
| Stability | Thermodynamically stable at ALL crustal T | Metastable — kinetically trapped |
| Typical T | 50–500°C | 100–300°C (especially <150°C) |
| pH preference | Neutral to mildly acidic (5–7) | Strongly acidic (<4) |
| Fe content | Up to 40 mol% (marmatite) | Up to 8 mol% |
| Habit | Tetrahedra, dodecahedra | Hexagonal prisms, radial clusters |
| Diagnostic | Resinous luster, 6-direction cleavage | Submetallic luster, basal cleavage |

**The schalenblende phenomenon:** In the Aachen district (Germany) and Tri-State district (USA), sphalerite and wurtzite grow in alternating layers — colloform banding that records oscillating pH or temperature. This is not exsolution. This is two minerals with identical composition taking turns precipitating because conditions flickered across the polymorph boundary.

**Simulator implication:** The polymorph competition should use a **kinetic trapping model**, not equilibrium. At low pH (<4) and rapid precipitation (high σ), wurtzite nucleates even though sphalerite is the stable phase. Over time (or if pH rises), wurtzite converts to sphalerite — but the conversion is sluggish at room temperature.

---

## The Carbonate Branch: Smithsonite, Aurichalcite, Rosasite

When Zn²⁺ meets CO₃²⁻ in the oxidation zone, three carbonates are possible depending on who else is in the broth:

### Smithsonite (ZnCO₃) — The Solitary Path
- **When:** Cu is absent or very low, pH 7–8.5
- **Appearance:** Botryoidal, reniform, drusy crusts. Rarely well-crystallized.
- **Famous colors:** Blue (cuprian), pink (cobaltoan), yellow ("turkey fat" with CdS inclusions)
- **Secret:** Extreme birefringence (δ = 0.225) — transparent crystals show spectacular doubling

### Aurichalcite vs Rosasite — The Cu/Zn Ratio Duel

These two minerals are the **same story told with different emphasis**. Both are Cu-Zn hydroxycarbonates. The difference is the Cu:Zn ratio:

| Feature | Aurichalcite | Rosasite |
|---|---|---|
| Formula | (Zn,Cu)₅(CO₃)₂(OH)₆ | (Cu,Zn)₂(CO₃)(OH)₂ |
| Cu:Zn ratio | Zn-dominant (~5:4) | Cu-dominant (~3:2) |
| Zn per formula unit | 5 | 1 |
| Cu per formula unit | 4 | 2 |
| CO₃ per formula unit | 2 | 1 |
| Color | Pale green, blue-green | Blue, bluish green |
| Habit | Tufted sprays, radiating needles | Botryoidal, fibrous crusts |
| Hardness | 2 (very soft) | 4 |
| Crystal system | Monoclinic | Monoclinic |

**The broth-ratio rule:**
- High Zn²⁺, moderate Cu²⁺, abundant CO₃²⁻ → Aurichalcite
- High Cu²⁺, moderate Zn²⁺, moderate CO₃²⁻ → Rosasite
- Low Cu²⁺, abundant Zn²⁺, abundant CO₃²⁻ → Smithsonite

**Famous co-occurrence:** The Kelly Mine, New Mexico, USA — aurichalcite and rosasite occur together on the same specimens, sometimes intergrown, recording fluid chemistry that oscillated across the Cu:Zn ratio threshold.

---

## Formation Mechanisms

### Sphalerite (Primary)
- **How it forms:** Zn²⁺ + S²⁻ in reducing hydrothermal fluids, 150–350°C
- **What it needs:** High Zn (>50 ppm), high S (as S²⁻), reducing conditions, neutral to mildly acidic pH
- **Iron content:** Increases with temperature — the marmatite variety (black, >20% Fe) is a high-T indicator
- **What happens next:** When exposed to oxygenated groundwater, sulfide sulfur oxidizes to sulfate, releasing Zn²⁺ into solution

### Wurtzite (Metastable Polymorph)
- **How it forms:** Same chemistry as sphalerite, but under acidic conditions (pH < 4) with rapid precipitation
- **What it needs:** Low pH (<4), high Zn activity, kinetic trapping (rapid σ buildup)
- **Where:** Volcanic-hosted massive sulfide deposits, acid mine drainage precipitates, low-T sedimentary concretions
- **Secret:** Often forms radial clusters that look like dark flowers — each "petal" is a hexagonal prism radiating from a center
- **What happens next:** Over geological time, converts to sphalerite (structure rearrangement, no chemistry change). At room temperature, the conversion is essentially frozen — wurtzite persists.

### Smithsonite (Secondary Carbonate)
- **How it forms:** Zn²⁺ (from oxidized sphalerite) + CO₃²⁻ (from dissolved CO₂ or carbonate host rock)
- **What it needs:** Oxidizing conditions (Eh > +0.2V), neutral to mildly alkaline pH (7–8.5), carbonate availability
- **Where:** The "dry zone" above the water table — where oxygen is present but water is intermittent
- **Notable:** Often forms pseudomorphs after sphalerite — the crystal shape of the original sulfide is preserved in carbonate
- **What happens next:** If Cu is introduced (from adjacent copper oxidation), smithsonite can be overgrown or replaced by aurichalcite or rosasite

### Aurichalcite (Mixed Cu-Zn, Zn-dominant)
- **How it forms:** Where Zn-rich fluids encounter Cu-bearing oxidized rock, or where a Cu-Zn sulfide body (like chalcopyrite-sphalerite ore) undergoes weathering
- **What it needs:** Both Cu²⁺ and Zn²⁺ in solution, Zn > Cu in concentration, pH 7–9, abundant CO₃²⁻
- **Where:** Oxidized zones of Cu-Zn deposits — Tsumeb (Namibia), Kelly Mine (New Mexico), Lavrion (Greece)
- **Secret:** The softest mineral in this sequence (H = 2) — softer than a fingernail. Handle with care.
- **What happens next:** If Cu continues to dominate the fluid, aurichalcite may be overgrown by rosasite. If Zn dominates, aurichalcite may persist or convert to smithsonite.

### Rosasite (Mixed Cu-Zn, Cu-dominant)
- **How it forms:** Where Cu²⁺ is abundant relative to Zn²⁺ in the oxidation zone — typically closer to the primary Cu source
- **What it needs:** Cu²⁺ > Zn²⁺ in fluid, moderate CO₃²⁻, pH 6.5–8.5
- **Where:** Same deposits as aurichalcite, but in zones with higher Cu/Zn ratio — often intergrown with malachite, azurite, or chrysocolla
- **Secret:** The velvety botryoidal surfaces look like miniature green-blue moons. Under magnification, radiating fibers are visible — each one a crystal that grew outward from a nucleation point.
- **What happens next:** If Cu becomes even more dominant and pH shifts, rosasite may be replaced by malachite or azurite (the pure copper carbonates).

---

## Simulator Implementation — Unified Zinc Zone Model

### New Parameter: `Cu_Zn_ratio`
The zinc oxidation zone needs a way to track the relative abundance of copper and zinc in the fluid. This is the key branching parameter for aurichalcite vs rosasite vs smithsonite.

**Implementation:**
```javascript
Cu_Zn_ratio = dissolved_Cu_ppm / dissolved_Zn_ppm
// If Zn = 0, ratio = Infinity (defaults to smithsonite path)
// If both = 0, no carbonate forms
```

### Supersaturation Functions — Unified

```javascript
// SPHALERITE (primary sulfide)
σ_sphalerite = f(Zn, S, T, pH)
  Zn > 50 ppm
  S as S²⁻ (reducing, Eh < 0)
  T = 50–500°C
  pH = 5–7 (neutral to mildly acidic)
  // Iron content increases with T: Fe_ppm / Zn_ppm → color (yellow→brown→black)

// WURTZITE (metastable polymorph)
σ_wurtzite = f(Zn, S, T, pH, σ_rate)
  Same Zn + S as sphalerite
  T = 100–300°C (can form at lower T kinetically)
  pH < 4 (critical — acidic conditions)
  σ_rate > threshold (rapid precipitation — kinetic trapping)
  // If pH > 5: nucleation suppressed (sphalerite wins)
  // Over time: metastable conversion to sphalerite if T > 150°C

// SMITHSONITE (pure Zn carbonate)
σ_smithsonite = f(Zn, CO3, T, pH, Eh, Cu_Zn_ratio)
  Zn > 30 ppm
  CO3 > threshold
  T = 10–50°C (ambient supergene)
  pH = 7.0–8.5
  Eh > +0.2V (oxidizing)
  Cu_Zn_ratio < 0.2 (Cu is minor — pure Zn path)

// AURICHALCITE (Zn-dominant Cu-Zn carbonate)
σ_aurichalcite = f(Zn, Cu, CO3, T, pH, Eh, Cu_Zn_ratio)
  Zn > 40 ppm, Cu > 20 ppm
  CO3 > high threshold (2 CO3 per formula unit)
  T = 10–40°C
  pH = 7–9
  Eh = +0.2 to +0.6V
  Cu_Zn_ratio = 0.2–1.0 (Cu present but Zn dominates)

// ROSASITE (Cu-dominant Cu-Zn carbonate)
σ_rosasite = f(Cu, Zn, CO3, T, pH, Eh, Cu_Zn_ratio)
  Cu > 30 ppm, Zn > 15 ppm
  CO3 > moderate threshold
  T = 10–40°C
  pH = 6.5–8.5
  Eh = +0.2 to +0.6V
  Cu_Zn_ratio > 0.5 (Cu dominates or is comparable)
```

### Special Simulator Events

#### `event_zinc_sulfide_oxidation`
**Trigger:** Sphalerite or wurtzite present in zone with Eh > +0.2V and O₂ > threshold.
**Effect:**
- Sphalerite/wurtzite enters dissolution phase
- S²⁻ oxidizes to SO₄²⁻ (releases acid: H₂SO₄)
- Zn²⁺ released to fluid (+50–200 ppm depending on dissolution rate)
- If Cu-bearing sulfides also present (chalcopyrite, bornite), Cu²⁺ also released
- pH drops locally (acid generation)
- **Key:** This event creates the Zn²⁺ (and possibly Cu²⁺) needed for secondary carbonates

#### `event_polymorph_conversion`
**Trigger:** Wurtzite present with T > 150°C and pH > 5 for >10 steps.
**Effect:**
- Gradual conversion: wurtzite → sphalerite
- Rate: slow at 150°C, moderate at 250°C
- Crystal shape preserved (structural rearrangement, no dissolution)
- In simulator: change mineral ID, keep position/size, update color/luster
- At T < 100°C: conversion essentially halted (metastable persistence)

#### `event_carbonate_ratio_shift`
**Trigger:** Fluid Cu_Zn_ratio changes by >0.3 in a single step.
**Effect:**
- If ratio rises (more Cu): aurichalcite may convert to rosasite, or rosasite overgrows aurichalcite
- If ratio falls (more Zn): rosasite may convert to aurichalcite, or smithsonite overgrows both
- Kinetics: slow — overgrowth more likely than replacement at low T
- In simulator: favor nucleation of the new ratio-appropriate mineral on existing crystals

#### `event_pseudomorph_smithsonite_after_sphalerite`
**Trigger:** Sphalerite dissolves while σ_smithsonite > threshold in same zone.
**Effect:**
- Smithsonite nucleates in place of dissolving sphalerite
- Retains original crystal shape (tetrahedral/dodecahedral pseudomorph)
- Color: typically grey-white (unless Cu/Co impurities present)
- Diagnostic: "false cleavage" — smithsonite doesn't have sphalerite's dodecahedral cleavage, so pseudomorphs show conchoidal fracture where cleavage is expected

### Color Coding for Zone Visualization

| Mineral | Representative Color | Hex |
|---|---|---|
| Sphalerite | Honey yellow | #D4A843 |
| Wurtzite | Dark brown | #5C4033 |
| Smithsonite (pure) | White-grey | #E8E8E8 |
| Smithsonite (cuprian) | Sky blue | #87CEEB |
| Smithsonite (cobaltoan) | Pink | #FFB6C1 |
| Aurichalcite | Pale green | #C8E6C9 |
| Rosasite | Blue-green | #5F9EA0 |

---

## Individual Flavor Text

### Sphalerite
> The miner's compass. Sphalerite doesn't just contain zinc — it contains information. The iron content is a geothermometer: yellow means cool, brown means warm, black means hot. The resinous luster and perfect dodecahedral cleavage are unmistakable once learned. And if you're very lucky, you'll find cleiophane — the almost pure variety, colorless to pale green, with a dispersion that outshines diamond. Sphalerite is the most important zinc ore on Earth, but in a vug, it's the beginning of a story that ends in blue-green carbonates.

### Wurtzite
> The phantom twin. Same chemistry as sphalerite, different soul. Where sphalerite is cubic and confident, wurtzite is hexagonal and elusive — it only appears when conditions are acidic and precipitation is rapid, a kinetic ghost trapped in a structure it shouldn't have. The radial clusters from Aachen look like dark flowers made of hexagonal prisms. Given enough time and warmth, wurtzite surrenders to sphalerite — the stable phase always wins eventually. But in a cool vug, wurtzite can persist forever, a metastable memory of an acidic moment.

### Smithsonite
> The chameleon carbonate. Botryoidal, drusy, reniform — smithsonite is a shape-shifter that rarely shows its true crystalline face. But the colors! Cuprian smithsonite is the blue of a winter sky. Cobaltoan smithsonite is the pink of dawn. "Turkey fat" smithsonite is yellow from cadmium sulfide inclusions, a mineral wearing another mineral's color. And if you find a transparent crystal, look for the extreme doubling — smithsonite's birefringence is among the highest of any common mineral. It forms when zinc sulfide meets oxygen and carbon dioxide, the simplest possible transformation: one anion replaces another, and the world gets a new color.

### Aurichalcite
> The softest spray. Aurichalcite is what happens when zinc and copper decide to share a carbonate. The result is delicate beyond belief — hardness 2, softer than a fingernail, forming tufted sprays that look like frozen sea anemones or the first frost on autumn grass. The pale green color is copper diluted by zinc: enough Cu to tint, enough Zn to soften. In the Kelly Mine of New Mexico, aurichalcite grows alongside rosasite on the same specimens, recording fluid chemistry that oscillated across the Cu:Zn threshold. Handle it once and you'll never forget how soft a mineral can be.

### Rosasite
> The blue-green moon. Rosasite is aurichalcite's copper-rich cousin, and it wears its copper proudly — deeper blue, harder (H=4), more botryoidal. The velvety surfaces look like miniature moons under magnification, each one a radiating fiber forest growing outward from a nucleation point. It's the mineral that taught geologists about Cu:Zn ratio control: same temperature, same pH, same oxidation state, but different metal ratios produce different minerals. Rosasite is what you find closer to the copper source; aurichalcite is what you find further out. Together, they map the fluid chemistry of an ancient oxidation zone in blue and green.

---

## Cross-Zone Interactions

### With the Copper Oxidation Zone
When Cu-Zn sulfide deposits (chalcopyrite + sphalerite) weather, the two oxidation zones overlap:
- **Near Cu source:** Native copper → cuprite → malachite/azurite → rosasite (if Zn present)
- **Near Zn source:** Sphalerite → smithsonite → aurichalcite → (rosasite if Cu penetrates)
- **Interface zone:** The most complex mineralogy — all Cu and Zn carbonates possible, plus mixed Cu-Zn minerals

### With the Lead Oxidation Zone
In polymetallic deposits (e.g., Mississippi Valley Type), Zn and Pb sulfides (sphalerite + galena) weather together:
- Galena → anglesite/cerussite (lead oxidation zone)
- Sphalerite → smithsonite (zinc oxidation zone)
- If both Cu and Pb present: rosasite/aurichalcite + pyromorphite/mimetite/vanadinite — a mineralogist's paradise

### With the Iron Oxidation Zone
Sphalerite often contains iron (marmatite variety). When this iron oxidizes:
- Fe²⁺ → Fe³⁺ → goethite/hematite (iron oxidation zone minerals)
- This iron oxidation can generate acid, lowering pH and promoting wurtzite over sphalerite in late-stage precipitation
- Jarosite may form if K⁺ and SO₄²⁻ are abundant

---

## Famous Localities

### Sphalerite
- **Elmwood Mine, Tennessee, USA:** Giant red crystals to 25 cm, world-class fluorite association
- **Tri-State District (Oklahoma/Kansas/Missouri, USA):** Classic MVT deposits, yellow to black sphalerite
- **Santander, Spain:** Transparent gemmy yellow sphalerite with diamond-like dispersion

### Wurtzite
- **Aachen, Germany:** Type locality, famous "schalenblende" banded sphalerite-wurtzite ore
- **Tri-State District, USA:** Low-T wurtzite in colloform crusts
- **Cuba:** Hot spring precipitates at 25–60°C, modern wurtzite formation

### Smithsonite
- **Kelly Mine, New Mexico, USA:** Blue cuprian smithsonite, classic American mineral
- **Tsumeb, Namibia:** Pink cobaltoan, yellow cadmian, blue cuprian — all colors
- **Sardinia, Italy:** Massive white and yellow smithsonite, historical zinc ore

### Aurichalcite
- **Kelly Mine, New Mexico, USA:** Type locality, delicate green sprays with rosasite
- **Lavrion, Greece:** Ancient slag reworking, aurichalcite on oxidized ore
- **Tsumeb, Namibia:** Exceptional sprays to 5 cm, associated with rosasite and smithsonite

### Rosasite
- **Rosas Mine, Sardinia, Italy:** Type locality (hence the name)
- **Kelly Mine, New Mexico, USA:** Deep blue-green botryoidal crusts with aurichalcite
- **Tsumeb, Namibia:** Velvety globules to 3 cm, associated with malachite and azurite

---

## Simulator Wiring Notes

### New Parameters Needed
- `Cu_Zn_ratio` — dissolved Cu / dissolved Zn in fluid (dimensionless)
- `pH_acid_threshold` — for wurtzite kinetic trapping (pH < 4)
- `polymorph_conversion_timer` — track how long wurtzite has been at T > 150°C, pH > 5

### New Events Needed
- `event_zinc_sulfide_oxidation` — sphalerite/wurtzite → Zn²⁺ + SO₄²⁻
- `event_polymorph_conversion` — wurtzite → sphalerite over time
- `event_carbonate_ratio_shift` — aurichalcite ↔ rosasite based on Cu_Zn_ratio
- `event_pseudomorph_smithsonite_after_sphalerite` — shape-preserving replacement

### Pseudomorph Mechanics
The zinc zone has two pseudomorph opportunities:
1. **Smithsonite after sphalerite:** Shape-preserving, common in nature
2. **Wurtzite → sphalerite conversion:** Structural rearrangement, shape preserved, chemistry identical

Both should use the simulator's pseudomorph system (if built) or be implemented as "same position, new mineral ID, retained size/shape."

### Growth Priority in Mixed Zones
When Cu and Zn carbonates compete:
1. If Cu_Zn_ratio < 0.2: smithsonite
2. If Cu_Zn_ratio = 0.2–0.5: aurichalcite (if Zn > 40 ppm, Cu > 20 ppm)
3. If Cu_Zn_ratio = 0.5–2.0: rosasite (if Cu > 30 ppm, Zn > 15 ppm)
4. If Cu_Zn_ratio > 2.0: malachite/azurite (copper oxidation zone takes over)

---

## Related Files
- `memory/research-copper-oxidation-zone.md` — Adjacent Cu system with native Cu → cuprite → malachite/azurite
- `memory/research-lead-oxidation-zone.md` — Adjacent Pb system with galena → anglesite/cerussite → pyromorphite
- `memory/research-iron-oxidation-zone.md` — Acid generation from Fe sulfide oxidation drives pH changes
- `memory/research-broth-ratio-sphalerite-wurtzite.md` — Polymorph competition model
- `memory/research-broth-ratio-malachite-azurite.md` — pCO₂ branching (analogous to Cu_Zn_ratio branching)
- `memory/research-broth-ratio-descloizite-mottramite.md` — Pb-Zn-V ratio branching (same mathematical structure)

---

*Zinc doesn't change its oxidation state. It doesn't have copper's redox drama. But zinc tells a different story — the story of what happens when one stable element meets changing conditions. Sphalerite becomes smithsonite. Smithsonite becomes aurichalcite or rosasite depending on who else shows up. Wurtzite is a kinetic ghost, a structure that shouldn't exist but does because conditions were too fast for equilibrium. The zinc oxidation zone is quieter than copper's, but the chemistry is just as precise — and the colors, when they come, are worth waiting for.*
