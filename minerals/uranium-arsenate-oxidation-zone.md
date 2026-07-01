# Uranium Arsenate Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-05-30
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering torbernite, zeunerite, uranospinite, and their meta- (dehydrated) equivalents as a single groundwater-chemistry-controlled mineral system.
**Related files:**
- `memory/research-torbernite.md` — Cu(UO₂)₂(PO₄)₂·12H₂O (Cu, phosphate)
- `memory/research-zeunerite.md` — Cu(UO₂)₂(AsO₄)₂·(10-16)H₂O (Cu, arsenate)
- `memory/research-uranospinite.md` — Ca(UO₂)₂(AsO₄)₂·10H₂O (Ca, arsenate)
- `memory/research-autunite.md` — Ca(UO₂)₂(PO₄)₂·10-12H₂O (Ca, phosphate) — already in game
- `memory/research-tyuyamunite.md` — Ca(UO₂)₂(VO₄)₂·5H₂O (Ca, vanadate) — already in game
- `memory/research-carnotite.md` — K₂(UO₂)₂(VO₄)₂·3H₂O (K, vanadate) — already in game
- `memory/research-meta-minerals-pararealgar.md` — meta-mineral dehydration mechanic template

---

## The Story This Sequence Tells

The autunite group is geology's own fluorescent ink. These minerals form in the uppermost oxidized parts of uranium deposits — the near-surface weathering zone where uraninite (UO₂) meets oxygenated groundwater. What makes them extraordinary isn't just the radioactivity; it's the layered, micaceous crystal structure that lets them cleave into paper-thin sheets, and the uranium atom itself acting as the fluorescence activator.

Within this group, chemistry partitions four ways:
- **Cation:** Ca²⁺ (autunite, uranospinite) vs Cu²⁺ (torbernite, zeunerite)
- **Anion:** PO₄³⁻ (autunite, torbernite) vs AsO₄³⁻ (zeunerite, uranospinite)

Same structure. Same UO₂²⁺ uranyl sheets. Different guests at the interlayer table.

---

## The Full Sequence (Deep to Surface)

```
DEPTH                                          SURFACE
  │                                              │
  ▼                                              ▼

Primary zone (hypogene):
  Uraninite (UO₂) ────────────────────────────────
         │
         │ groundwater + O₂ oxidizes U⁴⁺ → U⁶⁺
         │ P/As/V leached from host rock
         ▼
Supergene oxidation zone:

  Primary uranyl minerals (highly hydrated):

    Phosphate anion available:
      ├── Autunite      Ca(UO₂)₂(PO₄)₂·10-12H₂O   [yellow-green, orthorhombic]
      └── Torbernite    Cu(UO₂)₂(PO₄)₂·12H₂O       [emerald-green, tetragonal]

    Arsenate anion available:
      ├── Uranospinite  Ca(UO₂)₂(AsO₄)₂·10H₂O       [yellow-green, orthorhombic]
      └── Zeunerite     Cu(UO₂)₂(AsO₄)₂·(10-16)H₂O [emerald-green, tetragonal]

    Vanadate anion available (already in game):
      ├── Tyuyamunite   Ca(UO₂)₂(VO₄)₂·5H₂O         [yellow, orthorhombic]
      └── Carnotite     K₂(UO₂)₂(VO₄)₂·3H₂O         [bright yellow, monoclinic]

  Dehydration products (meta- minerals):
    ├── Meta-autunite     Ca(UO₂)₂(PO₄)₂·6-8H₂O
    ├── Metatorbernite    Cu(UO₂)₂(PO₄)₂·8H₂O
    ├── Metauranospinite  Ca(UO₂)₂(AsO₄)₂·?H₂O
    └── Metazeunerite     Cu(UO₂)₂(AsO₄)₂·8H₂O
```

---

## Phase Diagram: Groundwater Chemistry Control

At fixed Eh (oxidizing, U⁶⁺ stable), the controlling variables are:

```
     PO₄³⁻ vs AsO₄³⁻ availability
          ▲
   High   │  Torbernite      │  Zeunerite
   PO₄    │  (green sheets)  │  (green sheets)
  ────────┼──────────────────┼───────────────
   High   │  Autunite        │  Uranospinite
   AsO₄   │  (yellow-green)  │  (yellow-green)
          └──────────────────┴───────────────►
                    Ca²⁺        Cu²⁺
                    (calcic)    (cupric)
```

**Key insight:** The autunite group is a cation-anion exchange system. Same uranyl sheet backbone, different interlayer cations and tetrahedral anions. In the simulator, this means if you have U + oxidizing conditions, the mineral that forms depends on which cation (Ca vs Cu) and which anion (P vs As) are available in the groundwater.

---

## Formation Mechanisms

### All Autunite-Group Minerals Share:
1. **Primary precursor:** Uraninite (UO₂) or pitchblende oxidized by oxygenated groundwater
2. **U⁴⁺ → U⁶⁺ oxidation:** Uranium becomes mobile as uranyl ion (UO₂²⁺)
3. **Anion availability:** PO₄³⁻ from apatite dissolution, AsO₄³⁻ from arsenopyrite/scorodite oxidation
4. **Cation availability:** Ca²⁺ from calcite/dolomite, Cu²⁺ from chalcopyrite/chalcocite oxidation
5. **Low-T, near-surface:** All form below ~50°C in the weathering zone
6. **Layered structure:** Micaceous sheets with perfect {001} cleavage

### The Dehydration Story
All autunite-group minerals are **hydrated** when fresh. They contain 10-16 water molecules per formula unit, sitting in the interlayer spaces between uranyl sheets. In dry air or heated conditions, they lose water and transform into their **meta-** counterparts:

```
Autunite (12H₂O)  ──dry air──►  Meta-autunite (6-8H₂O)
Torbernite (12H₂O) ──heat───►   Metatorbernite (8H₂O)
Zeunerite (12H₂O) ──dry────►   Metazeunerite (8H₂O)
Uranospinite (10H₂O) ──dry──►   Metauranospinite (variable)
```

**In the simulator:** This should be modeled as a **reversible dehydration** event. When relative humidity drops below a threshold, hydrated autunite-group crystals have a chance per step to convert to their meta- form. The meta- form is structurally the same (same XRD pattern, same sheets) but less hydrated, more brittle, and often more translucent or opaque.

---

## Individual Species — The Four Players

### Torbernite — Cu(UO₂)₂(PO₄)₂·12H₂O
- **Color:** Emerald to apple green — the classic "uranium mica" color
- **Crystal system:** Tetragonal (pseudo-tetragonal, actually orthorhombic distortion is minor)
- **Habit:** Thin square or octagonal tabular crystals, micaceous, to 2.5 cm
- **Famous for:** Bright green sheets that look like emerald mica
- **Type locality:** Cornwall, England (mine named after Torbey)
- **Collector appeal:** The most common and visually striking autunite-group mineral

### Zeunerite — Cu(UO₂)₂(AsO₄)₂·(10-16)H₂O
- **Color:** Yellow-green to emerald green — very similar to torbernite
- **Crystal system:** Tetragonal
- **Habit:** Flat tabular on {001}, subparallel micaceous growths, to 4 cm
- **Famous for:** Being the arsenate twin of torbernite — same color, different anion
- **Type locality:** Weißer Hirsch Mine, Schneeberg, Erzgebirge, Germany
- **Collector appeal:** Rarer than torbernite, distinguished by association with arsenic minerals (scorodite, olivenite)

### Autunite — Ca(UO₂)₂(PO₄)₂·10-12H₂O
- **Color:** Yellow-green to lemon yellow — the yellowest of the group
- **Crystal system:** Orthorhombic (pseudo-tetragonal)
- **Habit:** Tabular square crystals, small crusts, fan-shaped aggregates
- **Famous for:** Strong fluorescence under UV — the classic "glowing uranium mineral"
- **Type locality:** Autun, Saône-et-Loire, France (type locality for the group)
- **Collector appeal:** Fluorescent display piece — glows bright yellow-green under LW UV

### Uranospinite — Ca(UO₂)₂(AsO₄)₂·10H₂O
- **Color:** Yellow-green, lemon yellow, siskin green — lighter than zeunerite
- **Crystal system:** Orthorhombic
- **Habit:** Thin tabular crystals flattened on {001}, to 1 mm; more commonly aggregates and crusts
- **Famous for:** The calcium-arsenate end member — lighter in color, more powdery/waxy in habit
- **Type locality:** Ellweiler, Rhineland-Palatinate, Germany
- **Collector appeal:** Delicate micro-crystals, often as fine coatings; epitaxial overgrowths on zeunerite reported

---

## Fluorescence — The Uranium Signature

All autunite-group minerals fluoresce due to the **uranyl ion (UO₂²⁺)** itself acting as the activator. This is intrinsic fluorescence — no Mn²⁺, no REE, no organic activator needed. The uranium atom IS the light source.

| Mineral | LW (365nm) | SW (255nm) | Notes |
|---------|-----------|-----------|-------|
| Autunite | Bright yellow-green | Yellow-green | Strongest fluorescence in the group |
| Torbernite | Weak green | Weak green | Cu²⁺ partially quenches; still visible |
| Zeunerite | Weak green | Weak green | Similar to torbernite |
| Uranospinite | Yellow-green | Yellow-green | Intermediate between autunite and Cu-members |

**Quenching:** Cu²⁺ is a known fluorescence quencher. The Cu-dominant members (torbernite, zeunerite) fluoresce more weakly than the Ca-dominant members (autunite, uranospinite). In the simulator, this could be a subtle visual cue: Ca-autunites glow brighter under UV mode.

---

## Famous Localities for the Full Sequence

### Autun, France (type locality)
The namesake. Uranium-bearing granite pegmatite. Produced the first described autunite in 1852.

### Margnac, Haute Vienne, France
Classic autunite locality. Fluorescent tabular crystals on matrix, up to 1 cm. The go-to specimen for display.

### Musonoi Mine, Shaba, Zaire (now DRC)
The world's best torbernite. Bright emerald-green platy crystals, sometimes to 2.5 cm, often in thick books. The reference specimen for the species.

### Schneeberg District, Erzgebirge, Germany
Type locality for zeunerite (Weißer Hirsch Mine) and the broader Saxony-Bohemia uranium belt. Also produced uraninite, pitchblende, and the full autunite suite.

### Rabejac Deposit, Lodève, Hérault, France
Extraordinary supergene uranyl mineralization. Type locality for three uranyl species (fontanite, seelite, rabejacite). Uranospinite reported as fine-grained waxy coatings.

### Montoso Quarries, Piedmont, Italy
Beautiful epitaxial crystals of uranospinite on zeunerite. A rare locality for crystallized (not crusty) uranospinite.

### Grandview Mine, Arizona, USA
Notable zeunerite locality. Secondary uranium mineralization in brecciated sandstone.

---

## Cross-Reference to Other Simulator Systems

### Thermal Decomposition
All autunite-group minerals dehydrate rather than decompose chemically:
- **Dehydration onset:** ~60-80°C (lose interlayer water)
- **Full dehydration:** ~100-150°C → meta- form
- **Structural breakdown:** >300°C (uranyl sheet decomposes)
- **No CO₂ release** (unlike carbonates) — these are phosphates/arsenates

In the simulator: Model as a two-stage dehydration event, not a single decomposition. Fresh crystals → meta- crystals at moderate heat, then structural collapse at high heat.

### Radioactivity
All four are radioactive (U content ~50-60 wt%). In the simulator, this could be:
- A passive radiation count in specimen info
- Visual "radiation halo" in dark mode (inspired by real radiation damage to surrounding minerals)
- Color darkening of adjacent clear minerals over time (simulated radiation damage)

### Associated Minerals (Real Paragenesis)
- **Primary:** Uraninite, pitchblende
- **Secondary Cu:** Chalcopyrite, chalcocite, malachite, azurite, cuprite, olivenite
- **Secondary Fe/As:** Scorodite, goethite, limonite
- **Secondary Ca:** Calcite, gypsum
- **Gangue:** Quartz, fluorite, barite

---

## Simulator Implementation — Unified Autunite Group Model

### New Chemistry Parameters
1. **UO₂²⁺ concentration:** Track uranium oxidation state. U⁴⁺ = primary (uraninite). U⁶⁺ = mobile, available for autunite-group formation.
2. **pH:** All autunite-group minerals form in mildly acidic to neutral conditions (pH 5-7). Strong acid dissolves the sheets; strong alkali precipitates uranophane (Ca-silicate) instead.
3. **Relative humidity / dehydration state:** A new environmental variable. Low RH triggers meta- conversion.

### Supersaturation Functions — Unified

```javascript
// AUTUNITE (Ca-phosphate)
σ_autunite = f(U6, Ca, PO4, pH, T)
  U6 > threshold (oxidized uranium present)
  Ca > 20 ppm
  PO4 > 10 ppm
  pH 5.5–7.5
  T < 50°C
  RH > 60% (hydrated form)

// TORBERNITE (Cu-phosphate)
σ_torbernite = f(U6, Cu, PO4, pH, T)
  U6 > threshold
  Cu > 30 ppm
  PO4 > 10 ppm
  pH 5.0–7.0
  T < 50°C
  RH > 60%
  // Cu-phosphate outcompetes Ca-phosphate when Cu >> Ca

// URANOSPINITE (Ca-arsenate)
σ_uranospinite = f(U6, Ca, AsO4, pH, T)
  U6 > threshold
  Ca > 20 ppm
  AsO4 > 10 ppm (from arsenopyrite/scorodite oxidation)
  pH 5.5–7.5
  T < 50°C
  RH > 60%

// ZEUNERITE (Cu-arsenate)
σ_zeunerite = f(U6, Cu, AsO4, pH, T)
  U6 > threshold
  Cu > 30 ppm
  AsO4 > 10 ppm
  pH 5.0–7.0
  T < 50°C
  RH > 60%
  // Cu-arsenate outcompetes Ca-arsenate when Cu >> Ca
```

### Priority Rules (Cation Competition)
When both Ca and Cu are available:
- If Cu/Ca ratio > 2: Cu-member forms (torbernite or zeunerite)
- If Cu/Ca ratio < 0.5: Ca-member forms (autunite or uranospinite)
- Intermediate ratios: both can nucleate (mixed paragenesis)

When both PO₄ and AsO₄ are available:
- PO₄/AsO₄ ratio > 2: phosphate member forms
- PO₄/AsO₄ ratio < 0.5: arsenate member forms
- Intermediate: mixed or solid solution (simplified: pick dominant)

### Dehydration Rules
```javascript
// Hydrated → Meta- conversion
IF autunite_group_crystal exists AND RH < 40%:
  prob = (40 - RH) / 40 * time_factor
  IF random() < prob:
    convert to meta_ equivalent
    // Color shifts slightly: more opaque, less vitreous
    // Fluorescence weakens (uranyl ion more constrained)
```

### Nucleation Habit
All autunite-group minerals share the same nucleation pattern:
- **Tabular on {001}:** Flat sheets, micaceous
- **Square/octagonal outline:** Tetragonal/orthorhombic symmetry expressed
- **Subparallel growth:** Stacks of overlapping sheets, like mica books
- **Crusts and aggregates:** When growth space is limited, forms waxy coatings

---

## Builder Notes

### Priority for Implementation
1. **Torbernite** — highest visual impact, classic green, most famous
2. **Autunite** — fluorescence mechanic is unique and compelling
3. **Zeunerite** — completes the Cu/As corner of the matrix
4. **Uranospinite** — completes the Ca/As corner; lower priority (rarer, less spectacular)

### New Fluid Chemistry Needed
- **U oxidation state tracking:** U⁴⁺ (primary, immobile) vs U⁶⁺ (oxidized, mobile)
- **Relative humidity:** For dehydration mechanics
- **pH buffering:** Mildly acidic conditions for stability

### Visual Design
- All four should share a "sheet-like" crystal render: flat polygons with thickness
- Color palette:
  - Torbernite: #2E8B57 to #228B22 (sea green to forest green)
  - Zeunerite: #9ACD32 to #6B8E23 (yellow-green to olive)
  - Autunite: #ADFF2F to #7CFC00 (yellow-green, brighter)
  - Uranospinite: #F0E68C to #E6E6FA (pale yellow-green to light lavender)
- Fluorescence effect: Under UV mode, autunite-family crystals glow with a bloom shader

---

## Flavor Text — Sequence Epilogue

> The autunite group is geology writing itself in fluorescent ink. Four minerals, one structure, four ways to answer the same question: what was in the groundwater when the uranium oxidized? If the water carried phosphate and calcium, you get autunite — the yellow-green sheets that glow under UV like someone bottled starlight. If the water was richer in copper, you get torbernite — emerald mica so thin it bends. Arsenate instead of phosphate? Zeunerite and uranospinite, the arsenic twins, rarer and more dangerous in equal measure. All of them are hydrated — water trapped between the uranyl sheets like pages in a book — and all of them dry out if you leave them on a shelf too long, turning from vivid to dusty, from hydrated to meta-, from alive to merely preserved. Handle them gently. They're not just radioactive. They're thirsty.

---

*File created 2026-05-30 by 🪨✍️ during Vugg Simulator mineral expansion cron. Next step: Builder implements unified autunite-group model with U-oxidation-state tracking, cation-anion competition matrix, and reversible dehydration mechanic.*
