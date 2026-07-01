# Iron Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-05-30
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering the full iron supergene oxidation chain: pyrite/marcasite → goethite/lepidocrocite → hematite → jarosite. This is the most geologically significant oxidation system on Earth — it drives acid mine drainage, creates the colors of the Grand Canyon, and governs the weathering of nearly every sulfide deposit.
**Related files:**
- `memory/research-pyrite.md` — FeS₂, cubic (primary sulfide)
- `memory/research-marcasite.md` — FeS₂, orthorhombic (acidic polymorph)
- `memory/research-pyrite-marcasite.md` — Paragenetic pair master (pH-controlled polymorph selection)
- `memory/research-goethite.md` — FeO(OH), orthorhombic (primary weathering product)
- `memory/research-lepidocrocite.md` — FeO(OH), orthorhombic (alternate weathering product)
- `memory/research-hematite.md` — Fe₂O₃, trigonal (mature oxidation product)
- `memory/research-jarosite.md` — KFe₃(SO₄)₂(OH)₆, trigonal (acidic sulfate product)

---

## The Story This Sequence Tells

Iron doesn't oxidize quietly. When pyrite — the most abundant sulfide on Earth's surface — meets oxygen and water, it doesn't just rust. It burns. The reaction releases ferrous iron, sulfate, and protons in staggering quantities: one mole of pyrite can generate two moles of sulfuric acid. This is the chemistry behind acid mine drainage, the ochre staining of streambeds, and the blood-red cliffs of the Grand Canyon's Supai Group.

The iron oxidation zone is a four-act play. Act I: pyrite or marcasite forms in the dark, in anoxic groundwater, often in vast sedimentary basins or hydrothermal veins. Act II: oxygen breaches the system — through uplift, erosion, or mining — and the sulfides begin their exothermic decay. Act III: goethite and lepidocrocite precipitate as the first solid oxidation products, often preserving the original crystal shapes as pseudomorphs. Act IV: in the most acidic, sulfate-rich environments, jarosite crystallizes as a late-stage efflorescence — a mineral that marks the extreme end of oxidative weathering.

Hematite appears at two points in this story: as a direct high-temperature oxidation product of goethite dehydration, and as a low-temperature recrystallization of amorphous iron oxyhydroxides. It's the end-state mineral — the most stable iron oxide under most Earth-surface conditions.

---

## The Full Sequence

### Stage 0: Precursor Sulfides (Hypogene)
**Pyrite (FeS₂, cubic)** or **marcasite (FeS₂, orthorhombic)** form the starting material.
- Pyrite: pH > 5.5, broader temperature range, more stable
- Marcasite: pH < 6, lower temperature, metastable (converts to pyrite at >325°C)

**Key simulator parameter:** `pH_sulfide` determines which polymorph nucleates. Both oxidize identically.

---

### Stage 1: Initial Oxidation — Ferrous Iron Release
**Chemical equation:**
```
2FeS₂ + 7O₂ + 2H₂O → 2Fe²⁺ + 4SO₄²⁻ + 4H⁺
```

**What happens:** Oxygen contacts sulfide. The reaction is autocatalytic — Fe²⁺ oxidizes to Fe³⁺ in solution, and Fe³⁺ attacks more pyrite faster than O₂ does. The pH plummets. A single pyrite crystal can create a microenvironment of pH < 2 in its own weathering rind.

**Simulator mechanics:**
- `oxidation_event`: when O₂ rises or water intrudes, pyrite/marcasite enters dissolution mode
- Release: Fe²⁺ (+50–500 ppm to broth), SO₄²⁻ (+100–1000 ppm), H⁺ (pH drop 2–4 units)
- Temperature: slightly exothermic — local T may rise 5–20°C

**Secondary effect:** If Cu, Pb, Zn are present in the same rock, the acid liberates them too. This is why iron oxidation zones often overlap with copper, lead, and zinc supergene enrichment zones. The acid doesn't just destroy pyrite — it unlocks the whole deposit.

---

### Stage 2: Primary Oxyhydroxide Precipitation — Goethite vs. Lepidocrocite
**Goethite (FeO(OH), orthorhombic)**
**Lepidocrocite (FeO(OH), orthorhombic)** — polymorph

**Chemical equation:**
```
Fe²⁺ + ¼O₂ + 1½H₂O → FeO(OH) + 2H⁺
```

**The goethite/lepidocrocite competition:**
Both have formula FeO(OH) but different crystal structures:
- **Goethite:** α-FeO(OH), orthorhombic, space group Pbnm. Double chains of edge-sharing FeO₆ octahedra. More stable, denser (SG 4.3), harder (5–5.5).
- **Lepidocrocite:** γ-FeO(OH), orthorhombic, space group Cmcm. Layer structure with tunnels. Less stable, softer (5), lighter (SG 4.0), converts to maghemite or hematite on heating.

**Formation conditions:**
| Parameter | Goethite | Lepidocrocite |
|-----------|----------|---------------|
| pH | > 6 (neutral-alkaline) | < 6 (acidic) |
| Fe²⁺ oxidation rate | Slow (O₂ or bacteria) | Fast (rapid oxidation) |
| Anions present | CO₃²⁻, PO₄³⁻, silicate | Cl⁻, SO₄²⁻ (halide/sulfate favored) |
| Temperature | 0–100°C, broad | 0–80°C, narrower |
| Stability | Very stable | Converts to goethite or hematite over time |

**Simulator rule:**
```
IF Fe_total > 50ppm AND pH > 5.5:
  nucleate GOETHITE
ELIF Fe_total > 50ppm AND pH < 6.0 AND SO₄²⁻ < 500ppm AND Cl⁻ > 50ppm:
  nucleate LEPIDOCROCITE
ELIF Fe_total > 50ppm AND pH < 6.0:
  // acidic but no lepidocrocite preference → goethite (default)
  nucleate GOETHITE
```

**Pseudomorphs:** Goethite pseudomorphs after pyrite cubes are among the most common pseudomorphs on Earth. The original crystal shape is preserved while the mineral completely replaces. In the simulator: when pyrite dissolves in oxidizing conditions, if goethite σ is high, it can "remember" the pyrite crystal's shape for 1–3 growth steps before randomizing.

**Color note:** Both minerals are typically yellow-brown to reddish-brown. Goethite tends toward brown-black; lepidocrocite is more orange-red. The "limonite" of old field guides is mostly goethite with amorphous iron hydroxides.

---

### Stage 3: Mature Oxide — Hematite
**Hematite (Fe₂O₃, trigonal)**

**Formation pathways:**
1. **Dehydration of goethite:** 2FeO(OH) → Fe₂O₃ + H₂O. Begins at ~80°C, rapid above 200°C. In nature: burial, contact metamorphism, or wildfire.
2. **Direct precipitation from Fe³⁺ solution:** Fe³⁺ + 3OH⁻ → Fe(OH)₃ (amorphous) → aging → hematite. Very slow at low T.
3. **Oxidation of magnetite:** 2Fe₃O₄ + ½O₂ → 3Fe₂O₃ (maghemite intermediate). Relevant in banded iron formations.

**Simulator conditions:**
- From goethite: IF T > 150°C AND goethite present → gradual conversion (dehydration)
- Direct: IF Fe³⁺ > 100ppm AND pH 6–9 AND T > 60°C → nucleate hematite
- From magnetite: IF magnetite present AND oxidation_event AND T > 200°C → surface hematite rind

**Hematite as end-state:** Once hematite forms, it's stable across almost all Earth-surface conditions. It doesn't oxidize further (iron is already Fe³⁺). It doesn't hydrate significantly under normal conditions. It's the geological "done" button for iron.

**Special note — Martian connection:** Hematite "blueberries" on Mars (discovered by Opportunity rover) are concretions formed by groundwater precipitation of hematite in sulfate-rich sediment. Same chemistry, different planet. The jarosite discovered by Opportunity confirms acidic conditions — Mars had acid mine drainage without the mines.

---

### Stage 4: Extreme Acid — Jarosite
**Jarosite (KFe₃(SO₄)₂(OH)₆, trigonal)**

**Chemical equation:**
```
K⁺ + 3Fe³⁺ + 2SO₄²⁻ + 6H₂O → KFe₃(SO₄)₂(OH)₆ + 6H⁺
```

**Where it fits:** Jarosite is the late-stage, extreme-acid mineral. It only forms when:
- pH < 3 (ideally 1.5–2.5)
- Fe³⁺ is abundant (from pyrite oxidation)
- SO₄²⁻ is abundant (from same source)
- K⁺ is available (feldspar alteration, groundwater)

**Jarosite marks the end of the oxidation cascade.** It's the mineral that says "the acid won." When you see jarosite in the field, you know the pH is low enough to dissolve aluminum silicates and mobilize heavy metals. It's the signature mineral of acid mine drainage, acid sulfate soils, and the most aggressive weathering environments.

**Simulator conditions:**
```
IF pH < 3.0 AND Fe³⁺ > 200ppm AND SO₄²⁻ > 500ppm AND K⁺ > 20ppm AND T < 120°C:
  nucleate JAROSITE
```

**Jarosite polymorphs/variants:**
- **Natrojarosite:** Na replaces K (NaFe₃(SO₄)₂(OH)₆)
- **Hydronium jarosite:** H₃O⁺ replaces K
- **Ammoniojarosite:** NH₄⁺ replaces K
- **Argentojarosite:** Ag⁺ replaces K (rare, silver-rich environments)

In the simulator: if K is limiting but Na is abundant, natrojarosite forms instead. Same crystal structure, different chemistry.

---

## The Complete Paragenetic Sequence (Visual)

```
STAGE 0: Primary Sulfides (anoxic, deep)
├── Pyrite (cubic, pH > 5.5) ─────┐
└── Marcasite (orthorhombic, pH < 6) │
       ↓ O₂ + H₂O intrusion         │
STAGE 1: Dissolution & Acid Generation
├── Release: Fe²⁺, SO₄²⁻, H⁺       │
└── pH drops: 7 → 2–4               │
       ↓ oxidation + hydrolysis      │
STAGE 2: Oxyhydroxides (moderate oxidation)
├── Goethite (pH > 5.5, neutral-alkaline) ──┤
└── Lepidocrocite (pH < 6, acidic, Cl⁻ rich)│
       ↓ dehydration / aging / direct precip │
STAGE 3: Hematite (mature, stable)
├── From goethite: T > 150°C         │
├── Direct: Fe³⁺ + OH⁻ (slow)       │
└── End-state oxide                  │
       ↓ extreme acid + K⁺ + SO₄²⁻  │
STAGE 4: Jarosite (extreme weathering)
├── pH < 3, K + Fe³⁺ + SO₄²⁻       │
└── The "acid won" mineral           │
```

---

## Simulator Events for the Iron Oxidation Zone

### `event_surface_oxidation`
**Trigger:** O₂ rises above 1 ppm in a zone containing pyrite/marcasite.
**Effect:**
- Pyrite/marcasite switches from growth to dissolution mode
- Rate of dissolution proportional to O₂ concentration
- Release: Fe²⁺, SO₄²⁻, H⁺ (stoichiometric per formula)
- Local pH drops
- If T > 325°C: any marcasite converts to pyrite first, then dissolves

### `event_acid_drainage`
**Trigger:** pH drops below 4 in a zone with Fe²⁺ and SO₄²⁻.
**Effect:**
- Goethite nucleation suppressed
- Lepidocrocite favored (if Cl⁻ present)
- Jarosite possible (if K⁺ and pH < 3)
- Any carbonates (calcite, siderite, etc.) in same zone enter rapid dissolution
- Cu, Pb, Zn mobilized if present

### `event_goethite_dehydration`
**Trigger:** T > 150°C in zone with goethite.
**Effect:**
- Gradual conversion: goethite → hematite + H₂O
- Rate: slow at 150°C, moderate at 250°C, rapid above 400°C
- Crystal habit: if goethite was pseudomorphing pyrite, hematite may retain the cubic shape

### `event_pseudomorph_replacement`
**Trigger:** Pyrite/marcasite dissolves while goethite σ > threshold in same microzone.
**Effect:**
- Goethite nucleates with "memory" of dissolved pyrite's habit
- For 1–3 growth cycles, crystal shape favors cube/pyritohedron
- After: normal goethite habit (acicular, botryoidal, massive)
- Special flavor text for pseudomorph specimens

---

## Cross-Zone Interactions

### Copper Oxidation Zone Overlap
When pyrite oxidizes in a deposit that also contains chalcopyrite (CuFeS₂), the acid liberates Cu²⁺. This creates the classic **supergene copper enrichment** profile:
- Deep: primary sulfides (chalcopyrite, bornite)
- Middle: secondary sulfides (chalcocite, covellite — Cu enriched)
- Upper: oxide zone (malachite, azurite, cuprite, native copper)
- The acid driving this enrichment comes from pyrite oxidation.

**Simulator implication:** Iron oxidation zone events can trigger copper oxidation zone events downstream if Cu is present in the same rock mass.

### Lead Oxidation Zone Overlap
Galena (PbS) oxidation is also acid-generating, though less so than pyrite:
```
PbS + 2O₂ → PbSO₄ (anglesite)
PbS + 2O₂ + CO₂ + H₂O → PbCO₃ + H₂SO₄ (cerussite + acid)
```

The anglesite → cerussite → pyromorphite sequence (see future lead oxidation zone master file) is enhanced by acid from neighboring pyrite oxidation.

### Aluminum Mobilization
At pH < 4 (jarosite-forming conditions), aluminosilicates (feldspars, micas) begin to dissolve. This releases:
- Al³⁺ → can form alunite (KAl₃(SO₄)₂(OH)₆), jarosite's aluminum twin
- SiO₂ → can reprecipitate as chalcedony or opal
- Kaolinite → the ultimate clay residue of advanced acid weathering

**Simulator implication:** Extreme iron oxidation can create secondary silica and clay mineral events.

---

## Famous Localities Showing the Full Sequence

### Rio Tinto, Spain
The type locality for acid mine drainage and a Mars analog site. Pyrite-rich Iberian pyritic belt weathered for thousands of years. Sequence visible in outcrop:
- Unoxidized pyrite cores
- Goethite/limonite rinds
- Surface jarosite efflorescence
- Blood-red acidic rivers (pH < 2) colored by suspended hematite/goethite

### Iron Quadrangle, Minas Gerais, Brazil
Canga — the iron-rich duricrust capping BIF-hosted iron ore. Hematite-dominated, but preserves goethite layers and jarosite in fractures. The world's largest iron ore deposits.

### Bingham Canyon, Utah
Porphyry copper deposit with massive pyrite shell. The oxidation zone shows complete iron sequence from pyrite → goethite → hematite, with jarosite in the most leached cap. Secondary copper enrichment (chalcocite blanket) beneath the iron oxidation zone — the acid from pyrite oxidation drove the Cu enrichment.

### Meridiani Planum, Mars
Opportunity rover found hematite "blueberries," jarosite in sulfate-rich sediment, and goethite signatures. Confirmed acidic groundwater on Mars ~3.5 billion years ago. Same chemistry, no oxygen atmosphere — the oxidant was likely hydrogen peroxide or photochemical processes.

---

## Individual Species Flavor Text

### Goethite
> Goethite is the patient recycler of iron. It forms when pyrite finally surrenders to oxygen — not with a burst, but with a slow molecular rearrangement that preserves the original crystal's ghost. Goethite pseudomorphs after pyrite are everywhere, and each one is a fossil of a sulfide's final breath. The mineral is named for Goethe, who knew something about transformation. In the right light, goethite doesn't look like a rust stain; it looks like a memory of something that used to be brighter.

### Lepidocrocite
> Lepidocrocite is goethite's flightier sibling — same chemistry, less commitment. It forms in the acidic flash-flood of a pyrite oxidation event: orange scales, scaly coatings, blade-like crystals that feel almost organic. But lepidocrocite doesn't last. Given time or heat, it collapses into goethite or hematite, erasing its own flaky beauty for something more stable. Collectors prize it for the color — a vivid orange-red that no other iron mineral quite matches. It's the mineral equivalent of a sunset: brilliant, brief, and already fading.

### Hematite
> Hematite is the end of iron's journey. Whatever form iron took to get here — sulfide, carbonate, silicate, oxyhydroxide — hematite is where the chemistry settles. Fe³⁺ in octahedral coordination, stacked in the corundum structure, so stable it survives on the surface of Mars. The red of the Grand Canyon is hematite. The red of rust is hematite. The red of Martian soil is hematite. It's the mineral that colors planets, and it does so because it's the last thing iron can become before there's nowhere left to oxidize.

### Jarosite
> Jarosite is the mineral of acid victory. It only forms when the pH has fallen so low that nothing else can survive — when the sulfuric acid from pyrite oxidation has won the field and the only thing left to crystallize is a potassium iron sulfate that looks like yellow-brown sugar. Jarosite's presence in a rock means the environment is hostile to life, to carbonate, to clay, to anything that can't tolerate extreme acidity. NASA's Mars rovers found jarosite and celebrated: proof of past water, and past chemistry extreme enough to be interesting. On Earth, jarosite is a warning sign. On Mars, it was a discovery. Both are telling the same story: iron, acid, and time.

---

## Simulator Implementation Notes

### New Parameters Needed
- `Fe_oxidation_state`: Track Fe²⁺ vs Fe³⁺ separately (currently just `Fe_total`). Critical for jarosite/goethite/hematite competition.
- `acid_generation_rate`: Rate of H⁺ production from sulfide oxidation. Scales with pyrite surface area × O₂ concentration.
- `pseudomorph_memory`: Temporary state variable (1–3 growth cycles) preserving dissolved crystal habit.

### Pseudocode: Iron Oxidation Zone Master Logic

```
// Stage 0: Sulfide formation (existing pyrite/marcasite logic)
IF anoxic AND Fe > 50ppm AND S > 100ppm:
  IF pH > 5.5: nucleate PYRITE
  IF pH < 6.0: nucleate MARCASITE

// Stage 1: Oxidation trigger
IF O₂ > 1ppm AND (pyrite OR marcasite) present:
  trigger event_surface_oxidation
  pyrite.dissolution_rate = k × O₂_concentration × surface_area
  release Fe²⁺, SO₄²⁻, H⁺
  local_pH -= acid_generation_rate × timestep

// Stage 2: Oxyhydroxide precipitation
IF Fe_total > 50ppm AND oxidation_state > 0.5:
  IF pH > 5.5:
    nucleate GOETHITE
    IF pyrite_recently_dissolved AND pseudomorph_memory > 0:
      goethite.habit = PYRITIC (cube/pyritohedron for 1-3 cycles)
  ELIF pH < 6.0 AND Cl⁻ > 50ppm AND SO₄²⁻ < 500ppm:
    nucleate LEPIDOCROCITE
  ELSE:
    nucleate GOETHITE (default)

// Stage 3: Hematite formation
IF goethite present AND T > 150°C:
  goethite.conversion_rate = f(T) // exponential with temperature
  IF conversion_complete: replace with HEMATITE
  
IF Fe³⁺ > 100ppm AND pH 6-9 AND T > 60°C:
  nucleate HEMATITE (direct precipitation, slow)

// Stage 4: Jarosite (extreme acid)
IF pH < 3.0 AND Fe³⁺ > 200ppm AND SO₄²⁻ > 500ppm AND K⁺ > 20ppm:
  IF K⁺ > Na⁺: nucleate JAROSITE
  ELIF Na⁺ > K⁺: nucleate NATROJAROSITE
```

### Color Coding for Zone Visualization
| Mineral | Representative Color | Hex |
|---------|---------------------|-----|
| Pyrite | Brass yellow | #D4AF37 |
| Marcasite | Pale bronze | #B5A642 |
| Goethite | Yellow-brown | #8B7355 |
| Lepidocrocite | Orange-red | #D4542A |
| Hematite | Blood red / steel grey | #A52A2A / #708090 |
| Jarosite | Mustard yellow | #D4A017 |

---

## Cross-References
- **Copper oxidation zone:** `memory/research-copper-oxidation-zone.md` — shares acid generation from pyrite oxidation
- **Lead oxidation zone:** Future unified file (galena → anglesite → cerussite → pyromorphite group)
- **Pyrite-marcasite polymorph pair:** `memory/research-pyrite-marcasite.md`
- **Uranium arsenate oxidation zone:** `memory/research-uranium-arsenate-oxidation-zone.md` — similar supergene weathering logic
- **Overgrowth paragenesis:** `memory/research-overgrowth-paragenesis.md` — sequential nucleation mechanics

---

*Iron tells the story of oxidation on Earth more clearly than any other element. From the brass cubes of pyrite to the blood-red dust of hematite to the acid-yellow crystals of jarosite, the iron oxidation zone is a complete geochemical novel — and it's playing out in every sulfide deposit, every mine drainage, every red-rock canyon on the planet.*
