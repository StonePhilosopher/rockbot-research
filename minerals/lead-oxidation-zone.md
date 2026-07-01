# Lead Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-06-03
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering galena, anglesite, cerussite, pyromorphite, mimetite, vanadinite, wulfenite, stolzite, and raspite as a single redox-controlled mineral system.
**Related files:**
- `memory/research-galena.md` — PbS, cubic primary sulfide
- `memory/research-anglesite.md` — PbSO₄, orthorhombic sulfate
- `memory/research-cerussite.md` — PbCO₃, orthorhombic carbonate
- `memory/research-pyromorphite.md` — Pb₅(PO₄)₃Cl, hexagonal phosphate
- `memory/research-mimetite.md` — Pb₅(AsO₄)₃Cl, hexagonal arsenate
- `memory/research-vanadinite.md` — Pb₅(VO₄)₃Cl, hexagonal vanadate
- `memory/research-wulfenite.md` — PbMoO₄, tetragonal molybdate
- `memory/research-stolzite.md` — PbWO₄, tetragonal tungstate
- `memory/research-raspite.md` — PbWO₄, monoclinic tungstate polymorph

---

## The Story This Sequence Tells

The lead oxidation zone is the story of what happens when the heaviest common sulfide meets Earth's surface. Galena — PbS, 7.6 g/cm³, metallic cubes — is so dense it feels wrong in the hand, like a piece of collapsed star. And when oxygen, water, and time get to it, that density becomes a problem: lead doesn't go anywhere. It stays. It transforms. It accumulates.

Where iron oxidizes and generates acid that washes away, and where copper oxidizes into brilliant carbonates that dissolve and reprecipitate, lead is immobile. The lead oxidation zone is a **museum** — every stage of the transformation is preserved, often as pseudomorphs, because lead compounds are nearly insoluble and don't migrate.

This sequence teaches a lesson no other zone can: **the archaeology of weathering**. In a lead oxidation zone, you can read the history of the weathering front like sedimentary layers — galena core, anglesite rind, cerussite overgrowth, pyromorphite crust — each layer recording a different moment in the fluid's chemistry.

---

## The Full Sequence (Deep to Surface)

```
DEPTH                                          SURFACE
  │                                              │
  ▼                                              ▼

Primary zone (hypogene):
  Galena (PbS)
         │
         │ uplift + exposure to O₂ + H₂O
         ▼
Oxidation zone (supergene):

  First contact — SO₄²⁻ from sulfide oxidation:
         │
         └──► Anglesite (PbSO₄)
                  │
                  ├──► If CO₃²⁻ is present: converts to Cerussite (PbCO₃)
                  │      2-3× more stable than anglesite in carbonate waters
                  │
                  └──► If PO₄³⁻, AsO₄³⁻, or VO₄³⁻ present:
                           │
                           ├──► Phosphate-rich: Pyromorphite (Pb₅(PO₄)₃Cl)
                           ├──► Arsenate-rich: Mimetite (Pb₅(AsO₄)₃Cl)
                           └──► Vanadate-rich: Vanadinite (Pb₅(VO₄)₃Cl)

  Molybdenum/Tungsten pulse (separate event):
         │
         └──► Wulfenite (PbMoO₄) — if Mo oxidizes from molybdenite
                  │
                  ├──► Tetragonal (stolzite structure)
                  │
                  └──► If late-stage, low-T, high-Pb:
                           └──► Stolzite (PbWO₄, tetragonal) or Raspite (PbWO₄, monoclinic)
```

---

## Phase Diagram: pH vs Anion Availability at Fixed Eh (+0.3V, 25°C)

```
     Anion Dominance
       ▲
  PO₄  │  Pyromorphite  │
       │  (green)        │
  AsO₄ │─────────────────┼─────────────────
       │  Mimetite       │  Vanadinite
  VO₄  │  (yellow)       │  (red/orange)
       │                 │
  CO₃  │  Cerussite      │
       │  (white/grey)   │
  SO₄  │  Anglesite      │
       │  (colorless/    │
       │   white)        │
       └─────────────────┼─────────────────► pH
       acidic            │              alkaline
       3                 7              10
```

**Key insight:** Lead is so insoluble that the stable phase is determined almost entirely by which anion is most abundant. pH matters secondarily — at very low pH, even anglesite can dissolve, but lead doesn't migrate far before reprocipitating.

---

## The Pseudomorph Chain: Galena's Many Masks

Because lead doesn't migrate, oxidation products often preserve the original galena crystal shape. This creates one of the most spectacular pseudomorph sequences in mineralogy:

| Stage | Mineral | Preserves Galena Shape? | Notes |
|---|---|---|---|
| 1 | Galena | Original | Cubic, metallic, perfect cleavage |
| 2 | Anglesite | Yes (paramorph) | Often hollow — anglesite occupies more volume than galena |
| 3 | Cerussite | Yes | Most common galena pseudomorph; cyclic twins add star patterns |
| 4 | Pyromorphite | Partially | Crusts on galena/anglesite/cerussite; may overgrow or replace |

**The anglesite hollow shell phenomenon:** Anglesite (PbSO₄, M = 303.3 g/mol) has a larger molar volume than galena (PbS, M = 239.3 g/mol). When galena converts to anglesite, the reaction produces a volume increase of ~25%. The anglesite crystal often grows outward from the galena surface, creating a hollow shell or boxwork structure — the original galena may dissolve away completely, leaving an anglesite "mold" that preserves the cubic shape but is empty inside.

**Simulator implication:** Pseudomorph replacement should model volume changes. Anglesite after galena → size increase ×1.2. Cerussite after anglesite → similar volume change. The resulting pseudomorph may have "ghost cleavage" — fracture surfaces that don't match the new mineral's cleavage.

---

## The Apatite-Mimetite-Vanadinite Series: Anion Substitution

These three minerals share the same crystal structure (apatite group, hexagonal, P6₃/m) and the same cation framework (Pb₅(XO₄)₃Cl). The only difference is the tetrahedral anion in the XO₄ position:

| Mineral | XO₄³⁻ | Color | Typical Form | Rarity |
|---|---|---|---|---|
| Pyromorphite | PO₄³⁻ | Green, yellow-green, brown, orange | Barrel-shaped hexagonal prisms | Common |
| Mimetite | AsO₄³⁻ | Yellow, orange, brown, white | Barrel-shaped to botryoidal | Common |
| Vanadinite | VO₄³⁻ | Red, orange-red, brown, yellow | Sharp hexagonal prisms, smaller | Less common |

**The anion hierarchy in nature:**
1. **Phosphate** is most abundant in organic-rich soils (bone decay, guano)
2. **Arsenate** is abundant where arsenopyrite or other arsenic minerals oxidize
3. **Vanadate** is least abundant — requires vanadium source (often from clay minerals or V-bearing shales)

**Compositional zoning:** On the same crystal, you can find pyromorphite core → mimetite rim → vanadinite overgrowth, recording a changing fluid chemistry. This is not exsolution — it's epitaxial overgrowth on a perfectly lattice-matched substrate (all three are isostructural with <3% lattice mismatch).

**Simulator implementation:** Use a single "lead apatite" supersaturation function with anion selection logic:
```
IF PO₄/AsO₄/VO₄ all present:
  IF PO₄ dominates AND σ_pyromorphite > threshold: nucleate pyromorphite
  ELIF AsO₄ dominates AND σ_mimetite > threshold: nucleate mimetite
  ELIF VO₄ dominates AND σ_vanadinite > threshold: nucleate vanadinite
  ELSE: nucleate the one with highest σ
```

---

## The Molybdate-Tungstate Branch

These minerals form separately from the main oxidation sequence — they require a separate molybdenum or tungsten source:

### Wulfenite (PbMoO₄)
- **Source of Mo:** Oxidation of molybdenite (MoS₂) in the same deposit, or from Mo-bearing hydrothermal fluids
- **Formation:** Requires Pb²⁺ (from galena oxidation) + MoO₄²⁻ (from molybdenite oxidation)
- **Key condition:** Oxidizing, pH 6–8, T < 80°C
- **Diagnostic:** Tetragonal dipyramids, often thin tabular plates; bright orange to yellow

### Stolzite vs Raspite (PbWO₄ polymorphs)
- **Source of W:** Scheelite (CaWO₄) dissolution, wolframite ((Fe,Mn)WO₄) oxidation, or direct W-bearing fluids
- **Formation:** Pb²⁺ + WO₄²⁻ at low T; polymorph depends on kinetics
- **Stolzite:** Tetragonal (stable at higher T, ~>50°C)
- **Raspite:** Monoclinic (stable at lower T, ~<50°C)
- **The polymorph problem:** In nature, stolzite and raspite are often intergrown or transitionally zoned, suggesting the boundary is kinetically controlled

**Simulator note:** Wulfenite, stolzite, and raspite are **not** part of the main lead oxidation sequence. They form when Mo or W is introduced from adjacent mineral systems. In the simulator, they should have separate supersaturation functions that depend on Mo/W availability.

---

## Formation Mechanisms

### Galena (PbS) — The Beginning
- **How it forms:** Pb²⁺ + S²⁻ in reducing hydrothermal fluids, 100–350°C
- **What it needs:** High Pb (>50 ppm), high S (as S²⁻), reducing conditions
- **Secret:** The brightest metallic luster of any common sulfide; cleavage surfaces mirror-finish
- **What happens next:** When exposed to oxygenated groundwater, the oxidation front advances through the crystal

### Anglesite (PbSO₄) — The First Response
- **How it forms:** Galena surface oxidation: PbS + 2O₂ → PbSO₄
- **What it needs:** O₂ (from air or groundwater), low to moderate pH (acid helps mobilize Pb)
- **Where:** The immediate surface of galena bodies — the "gossan" rind
- **Secret:** Brilliant adamantine luster, exceptional fire from high RI; pseudomorphs after galena cubes are common
- **What happens next:** If CO₃²⁻ is available in groundwater, anglesite converts to the more stable cerussite

### Cerussite (PbCO₃) — The Stable Carbonate
- **How it forms:** Anglesite + CO₂/H₂O → cerussite + H₂SO₄, OR direct galena oxidation in carbonate-rich water
- **What it needs:** CO₃²⁻ (from dissolved CO₂ or carbonate host rock), neutral to mildly alkaline pH
- **Where:** Below the immediate oxidation surface, where groundwater has had time to pick up CO₂
- **Secret:** Cyclic twins creating six-rayed stars — one of the most recognizable mineral forms
- **What happens next:** If phosphate, arsenate, or vanadate enters the system, cerussite may be overgrown by the apatite-group minerals

### Pyromorphite / Mimetite / Vanadinite — The Apatite Group
- **How they form:** Pb²⁺ + XO₄³⁻ + Cl⁻ in oxidizing, near-surface conditions
- **What they need:** Pb (from oxidized galena), phosphate/arsenate/vanadate (from organic decay or oxidized primary minerals), chloride (from groundwater), pH 5–8
- **Where:** The "iron hat" or gossan above lead deposits; also in soils over lead-bearing rocks
- **Secret:** Isostructural series with nearly identical lattice parameters — epitaxial overgrowths of one on another are common
- **What happens next:** These are end-stage supergene minerals. Further oxidation doesn't destroy them — they're already fully oxidized.

### Wulfenite / Stolzite / Raspite — The Late Heavyweights
- **How they form:** Pb²⁺ + MoO₄²⁻/WO₄²⁻ at low T, oxidizing conditions
- **What they need:** Separate Mo or W source (from oxidized molybdenite, scheelite, or wolframite)
- **Where:** Often in the same deposits but from different primary mineral sources
- **Secret:** Wulfenite's orange plates and stolzite's dipyramids are among the most collectible lead minerals
- **What happens next:** These are stable. They persist.

---

## Simulator Implementation — Unified Lead Zone Model

### New Parameter: `anion_dominance`
Track which anion (SO₄²⁻, CO₃²⁻, PO₄³⁻, AsO₄³⁻, VO₄³⁻, MoO₄²⁻, WO₄²⁻) is most abundant in the fluid. This determines the branching path.

**Implementation:**
```javascript
// Anion dominance ranking (highest concentration wins)
primary_anion = max(SO4, CO3, PO4, AsO4, VO4, MoO4, WO4)
// With thresholds: only consider anions above minimum activity
```

### Supersaturation Functions — Unified

```javascript
// GALENA (primary sulfide)
σ_galena = f(Pb, S, T, Eh)
  Pb > 50 ppm
  S as S²⁻ (reducing, Eh < 0)
  T = 100–500°C
  // In oxidation zone: σ_galena < 0 (dissolution)

// ANGLESITE (first oxidation product)
σ_anglesite = f(Pb, SO4, T, pH, Eh)
  Pb > 30 ppm (from dissolving galena)
  SO4 > threshold
  T = 10–80°C
  pH = 3–7 (acidic to neutral)
  Eh > +0.2V (oxidizing)
  // Inhibited by: high CO3 (promotes cerussite instead)

// CERUSSITE (carbonate — more stable than anglesite)
σ_cerussite = f(Pb, CO3, T, pH, Eh)
  Pb > 30 ppm
  CO3 > threshold
  T = 10–50°C
  pH = 6–9 (neutral to alkaline)
  Eh > +0.2V
  // Can form: directly from galena, or from anglesite conversion
  // Conversion: anglesite → cerussite if CO3 available

// PYROMORPHITE (phosphate apatite)
σ_pyromorphite = f(Pb, PO4, Cl, T, pH, Eh)
  Pb > 50 ppm
  PO4 > 10 ppm
  Cl > 5 ppm
  T = 10–50°C
  pH = 5–8
  Eh > +0.2V
  // Competes with: mimetite, vanadinite (same structure, different anion)

// MIMETITE (arsenate apatite)
σ_mimetite = f(Pb, AsO4, Cl, T, pH, Eh)
  Same as pyromorphite but AsO4 > PO4 and AsO4 > VO4

// VANADINITE (vanadate apatite)
σ_vanadinite = f(Pb, VO4, Cl, T, pH, Eh)
  Same as pyromorphite but VO4 > PO4 and VO4 > AsO4

// WULFENITE (molybdate)
σ_wulfenite = f(Pb, MoO4, T, pH, Eh)
  Pb > 30 ppm
  MoO4 > threshold (from molybdenite oxidation)
  T = 10–80°C
  pH = 6–8
  Eh > +0.2V
  // Separate from main sequence — needs Mo source

// STOLZITE / RASPITE (tungstate polymorphs)
σ_stolzite = f(Pb, WO4, T, pH, Eh)
  Pb > 30 ppm
  WO4 > threshold (from scheelite/wolframite oxidation)
  T = 10–80°C
  pH = 6–8
  Eh > +0.2V
  // Polymorph selection: stolzite (tetragonal) at T > 50°C, raspite (monoclinic) at T < 50°C
```

### Special Simulator Events

#### `event_galena_oxidation`
**Trigger:** Galena present with Eh > +0.2V and O₂ > threshold.
**Effect:**
- Galena surface enters dissolution
- Pb²⁺ released (+50–200 ppm depending on surface area)
- S²⁻ oxidizes to SO₄²⁻
- If O₂ is limited: forms anglesite rind on galena surface (protective layer slows further oxidation)
- If O₂ is abundant and pH low: galena dissolves completely

#### `event_anglesite_to_cerussite_conversion`
**Trigger:** Anglesite present with CO₃²⁻ > threshold and pH > 6.
**Effect:**
- Gradual conversion: anglesite → cerussite
- Rate: slow at room T, moderate at 40°C
- Crystal shape: preserved (paramorph)
- Volume change: minor (~5% increase)
- Acid release: H₂SO₄ (lowers local pH briefly)

#### `event_lead_apatite_overgrowth`
**Trigger:** Cerussite or anglesite present with PO₄³⁻/AsO₄³⁻/VO₄³⁻ > threshold and Cl⁻ > 5 ppm.
**Effect:**
- Apatite-group mineral nucleates on existing lead mineral surface
- Epitaxial growth preferred (lattice match)
- Anion selection based on relative abundance
- Can form: pyromorphite, mimetite, vanadinite, or zoned crystals

#### `event_pseudomorph_anglesite_after_galena`
**Trigger:** Galena dissolves while σ_anglesite > threshold in same zone.
**Effect:**
- Anglesite nucleates in place of galena
- Retains cubic shape (paramorph)
- May be hollow (volume increase leaves void)
- "Ghost cleavage" — anglesite doesn't have galena's perfect cubic cleavage

### Color Coding for Zone Visualization

| Mineral | Representative Color | Hex |
|---|---|---|
| Galena | Lead grey | #7A7A7A |
| Anglesite | Colorless/white | #F5F5F5 |
| Cerussite | White/grey | #E0E0E0 |
| Pyromorphite | Grass green | #7CFC00 |
| Mimetite | Honey yellow | #EAC117 |
| Vanadinite | Fire orange | #FF4500 |
| Wulfenite | Tangerine | #FF9966 |
| Stolzite | Brown-yellow | #D4A843 |
| Raspite | Yellow-brown | #C4A35A |

---

## Individual Flavor Text

### Galena
> The anchor. Galena is so heavy it feels like it should fall through your hand — 7.6 g/cm³, nearly twice the density of most rocks. The metallic cubes with their perfect cleavage are unmistakable: shine a light on a fresh surface and it mirrors your face back at you. Galena is the primary ore of lead, but in a mineral collection, it's prized for its weight, its luster, and its history. The ancient Romans mined galena for silver (it's often argentiferous), and alchemists spent centuries trying to transmute it into gold. What they didn't know was that galena holds a different kind of treasure: when it weathers, it produces some of the most beautiful secondary minerals on Earth.

### Anglesite
> The mirror's ghost. When galena meets sulfuric acid, it doesn't just dissolve — it transforms. Anglesite preserves the cube, the octahedron, the shape of the original galena crystal, but replaces the metallic sheen with adamantine fire. The refractive index is extraordinary (n ≈ 1.88), giving anglesite a brilliance that rivals diamond. And sometimes — often, actually — the anglesite shell is hollow, the original galena having dissolved away completely, leaving a crystal-shaped void lined with sparkling faces. Anglesite is a memory of a mineral, a shape that outlived its substance.

### Cerussite
> The star-maker. If anglesite is a ghost, cerussite is a constellation. The cyclic twins — six crystals joined at 60° angles — create six-rayed stars that are unmistakable. Cerussite forms when anglesite meets carbonated water, or when galena oxidizes directly in carbonate-rich environments. It's the most stable lead carbonate, and it carries lead's weight with unexpected grace: transparent crystals, adamantine luster, and that spectacular twinning. The extreme birefringence (δ = 0.273) means transparent crystals show doubling so strong it looks like the crystal is vibrating. Cerussite is what lead becomes when it has time to settle.

### Pyromorphite
> The barrel. Pyromorphite crystals look like miniature green barrels — hexagonal prisms with domed or flat terminations, often hollowed at the ends. The color ranges from grass green to brown to orange, depending on what trace elements sneaked into the lead apatite structure. The name means "fire form" because it melts and recrystallizes in the blowpipe flame — a property that confused early mineralogists. Pyromorphite is the phosphate end-member of the lead apatite series, and it's usually the first to form when phosphate-rich waters (from bone decay, guano, or oxidized primary phosphates) encounter lead oxidation zones. The barrels can be tiny (millimeters) or substantial (centimeters), and they're always collectible.

### Mimetite
> The mimic. Mimetite looks so much like pyromorphite that early mineralogists called it "mimetesite" — the imitator. Same barrel shape, same hexagonal symmetry, same resinous luster, but yellow to orange instead of green. The difference is arsenic instead of phosphorus in the XO₄ position. Mimetite forms where arsenopyrite or other arsenic minerals have oxidized, releasing arsenate into waters that already carry lead. It's slightly less common than pyromorphite (phosphorus is more abundant than arsenic in most environments), but the color contrast makes it equally prized. Some specimens show zoning: green pyromorphite core, yellow mimetite rim — a record of changing fluid chemistry.

### Vanadinite
> The fire prism. Vanadinite is the red-orange jewel of the lead apatite series, and it's the most visually striking of the three. Sharp hexagonal prisms, often smaller and more delicate than pyromorphite or mimetite, in colors ranging from cherry red to burnt orange to lemon yellow. The vanadium that colors it comes from oxidized clay minerals, shales, or primary vanadium minerals — less common than phosphorus or arsenic, which makes vanadinite rarer and more sought-after. When you find a vanadinite specimen, you're looking at a specific geochemical moment: vanadate-rich water meeting lead-rich rock at exactly the right temperature and pH. It's not just a mineral. It's a coincidence preserved in crystal.

### Wulfenite
> The orange plate. Wulfenite doesn't form from galena directly — it needs molybdenum, which comes from oxidized molybdenite (MoS₂) nearby. But when Pb²⁺ from galena oxidation meets MoO₄²⁻ from molybdenite oxidation, the result is extraordinary: thin tetragonal plates, often stacked like pages in a book, in colors from tangerine to mustard to brick red. The Red Cloud Mine in Arizona produces wulfenite so beautiful it's in every major mineral museum. Wulfenite is fragile (thin plates break easily) and heavy (Pb + Mo), making it a challenge to collect and display. But the color — that impossible orange — makes it worth the trouble.

### Stolzite
> The tungsten twin. Stolzite and wulfenite are isostructural — same tetragonal framework, different heavy metals in the tetrahedral position (W vs Mo). Stolzite is heavier (W = 183.8 vs Mo = 95.9), slightly more yellow-brown, and rarer because tungsten is less abundant than molybdenum in most ore deposits. The dipyramidal crystals from the Broken Hill district in Australia are classics: small, sharp, and with a luster that looks wet even when dry. Stolzite often occurs with raspite (its monoclinic polymorph), and the two can be intergrown in ways that confuse even experienced collectors. The polymorph boundary is kinetic — temperature, pH, and precipitation rate all play a role.

### Raspite
> The low-temperature phantom. Raspite is stolzite's monoclinic twin, stable at lower temperatures. It's less common, less well-formed, and often mistaken for stolzite — or for wulfenite. The crystals are typically smaller, more tabular, and more yellow-brown than stolzite. Raspite forms in the coolest, latest stages of oxidation, when tungstate-rich water seeps through fractures at ambient temperatures. In the simulator, raspite should appear only in late-stage, low-temperature conditions, while stolzite dominates earlier, warmer stages. The distinction is subtle but real: raspite is what tungsten becomes when it has all the time in the world.

---

## Cross-Zone Interactions

### With the Zinc Oxidation Zone
In polymetallic deposits (MVT, VMS), galena and sphalerite weather together:
- Galena → anglesite/cerussite → pyromorphite
- Sphalerite → smithsonite → aurichalcite/rosasite
- Pb and Zn don't mix in secondary carbonates (unlike Cu-Zn), so the zones remain distinct
- Exception: Iglesiasite (Zn-bearing cerussite) shows limited Pb-Zn substitution

### With the Copper Oxidation Zone
In porphyry and skarn deposits, Cu and Pb sulfides (chalcopyrite + galena) weather together:
- Chalcopyrite → malachite/azurite (copper zone)
- Galena → cerussite/pyromorphite (lead zone)
- The two zones can overlap, producing mixed assemblages
- Exception: Mimetite-pyromorphite can incorporate Cu traces (green coloration)

### With the Iron Oxidation Zone
Pyrite oxidation generates acid, which affects lead mineral stability:
- Low pH (<4) from pyrite oxidation: anglesite stable, cerussite dissolves
- Neutral pH: cerussite stable, anglesite converts to cerussite
- High pH (>8): all lead carbonates/sulfates stable
- Jarosite (iron zone) can incorporate Pb (plumbojarosite) — a bridge mineral

---

## Famous Localities

### Galena
- **Joplin, Missouri, USA:** Classic MVT district, cubic crystals to 10 cm
- **Tri-State District (OK/KS/MO, USA):** Massive galena with sphalerite
- **Dalnegorsk, Russia:** Brilliant metallic cubes, world-class specimens

### Anglesite
- **Touissit, Morocco:** Colorless to pale blue crystals, exceptional luster
- **Phoenixville, Pennsylvania, USA:** Classic pseudomorphs after galena
- **Tsumeb, Namibia:** Gemmy crystals to 5 cm

### Cerussite
- **Tsumeb, Namibia:** Cyclic twins, reticulate masses, gemmy crystals — arguably the best cerussite locality in the world
- **Broken Hill, Australia:** Massive white cerussite, important lead ore
- **Mibladen, Morocco:** Reticulate twins, star-shaped groups

### Pyromorphite
- **Bad Ems, Germany:** Type locality, green barrel crystals
- **Dauphiné, France:** Yellow-green crystals in quartz
- **Bunker Hill, Idaho, USA:** Bright green crystals to 2 cm

### Mimetite
- **Johanngeorgenstadt, Germany:** Type locality, yellow barrel crystals
- **Pingtouling, China:** Exceptional orange-brown crystals to 3 cm
- **Mapimi, Mexico:** Botryoidal yellow mimetite in goethite matrix

### Vanadinite
- **Mibladen, Morocco:** Red hexagonal prisms, the classic locality
- **Acf Mine, New Mexico, USA:** Orange crystals to 2 cm
- **Taouz, Morocco:** Bright red clusters, recent finds

### Wulfenite
- **Red Cloud Mine, Arizona, USA:** The classic — orange plates in matrix
- **Los Lamentos, Mexico:** Deep red crystals, exceptional
- **Tsumeb, Namibia:** Yellow to orange tabular crystals

### Stolzite / Raspite
- **Broken Hill, Australia:** Type locality for both; intergrown crystals
- **Zinnwald, Czech Republic:** Brown-yellow stolzite with wolframite
- **Tasmania, Australia:** Raspite with stolzite, confirming polymorph relationship

---

## Simulator Wiring Notes

### New Parameters Needed
- `anion_dominance` — ranking of anion concentrations (SO₄, CO₃, PO₄, AsO₄, VO₄, MoO₄, WO₄)
- `lead_apatite_anion` — which XO₄³⁻ is currently dominant
- `pseudomorph_volume_change` — track volume changes during replacement

### New Events Needed
- `event_galena_oxidation` — PbS → Pb²⁺ + SO₄²⁻
- `event_anglesite_to_cerussite_conversion` — PbSO₄ + CO₃²⁻ → PbCO₃ + SO₄²⁻
- `event_lead_apatite_overgrowth` — epitaxial nucleation on lead mineral surfaces
- `event_pseudomorph_anglesite_after_galena` — shape-preserving, possibly hollow

### Pseudomorph Mechanics
The lead zone has rich pseudomorph opportunities:
1. **Anglesite after galena:** Paramorph, may be hollow (volume increase)
2. **Cerussite after galena:** Paramorph, cyclic twins add star patterns
3. **Cerussite after anglesite:** Conversion pseudomorph, shape preserved
4. **Pyromorphite over cerussite:** Epitaxial overgrowth, not full replacement

### Anion Competition Logic
```
// Lead apatite anion selection
IF PO4 > AsO4 AND PO4 > VO4 AND PO4 > threshold:
    nucleate_pyromorphite()
ELIF AsO4 > PO4 AND AsO4 > VO4 AND AsO4 > threshold:
    nucleate_mimetite()
ELIF VO4 > PO4 AND VO4 > AsO4 AND VO4 > threshold:
    nucleate_vanadinite()
```

---

## Related Files
- `memory/research-copper-oxidation-zone.md` — Adjacent Cu system, overlaps in polymetallic deposits
- `memory/research-zinc-oxidation-zone.md` — Adjacent Zn system, MVT overlap
- `memory/research-iron-oxidation-zone.md` — Acid generation affects lead mineral stability
- `memory/research-broth-ratio-descloizite-mottramite.md` — Pb-Zn-V ratio branching (related chemistry)
- `memory/research-molybdenite.md` — Primary Mo source for wulfenite
- `memory/research-wolframite.md` — Primary W source for stolzite/raspite

---

*Lead is heavy in every sense. Heavy in the hand. Heavy in its environmental legacy. Heavy in its mineralogical weight — the lead oxidation zone preserves every stage of transformation because lead doesn't migrate. It stays where it falls, changing anions like a person changes clothes: sulfide to sulfate to carbonate to phosphate to arsenate to vanadate. Each layer records a different conversation between rock and water. And because lead is so insoluble, those conversations are preserved for millions of years — a mineralogical tape recorder, still playing back the chemistry of ancient weathering fronts.*
