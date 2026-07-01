# Silver Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-06-08
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering argentite → acanthite → native silver as a single temperature-redox controlled mineral system, with chlorargyrite as the halide branch.
**Related files:**
- `memory/research-argentite.md` — Ag₂S, high-T cubic polymorph
- `memory/research-acanthite.md` — Ag₂S, low-T monoclinic polymorph
- `memory/research-native-silver.md` — Ag⁰
- `memory/research-copper-oxidation-zone.md` — Parallel copper system for cross-reference

---

## The Story This Sequence Tells

Silver has three identities in the Earth's crust, and they are controlled by a single variable: **temperature**. Above 173°C, silver sulfide is cubic argentite — a high-symmetry metal-like conductor. Cool it through 173°C and the lattice collapses into monoclinic acanthite, a semiconductor. The cubic crystal shape doesn't change (it's a paramorph), but everything inside does.

Then there's native silver — the metal itself. Silver shouldn't exist as a native element. It's too reactive, too eager to bond with sulfur or chlorine. But in the deepest reducing zones, where sulfur has been exhausted by earlier precipitation, silver has nothing left to react with and simply precipitates as itself.

The silver oxidation zone is shorter than the copper system — fewer minerals, fewer branches — but no less profound. It's the story of a metal that keeps trying to become something else (sulfide, halide) and occasionally, in the right conditions, gets to just be itself.

---

## The Full Sequence (Temperature-Redox Controlled)

```
HIGH TEMPERATURE ──────────────────────── LOW TEMPERATURE
        │                                        │
        ▼                                        ▼

Hypogene zone (epithermal, 200–300°C):
  Argentite (Ag₂S) ──► Acanthite (Ag₂S)
    │                    │
    │  Cubic (Im-3m)     │  Monoclinic (P2₁/c)
    │  Metallic conductor│  Semiconductor
    │  87% Ag            │  87% Ag
    │                    │
    │  COOLING           │  Paramorph —
    │  through 173°C     │  keeps cubic
    │                    │  external shape
    ▼                    ▼
    
    Primary/supergene zone (<173°C):
    Acanthite (Ag₂S) remains stable
    │
    │  IF S²⁻ depleted and Eh drops:
    │  
    └──► Native Silver (Ag⁰)
            │
            │  100% Ag
            │  Strongly reducing
            │  Sulfide stability field
            │  exhausted
            │
            ▼
    IF Cl⁻ available and oxidizing:
    
    Chlorargyrite (AgCl) — horn silver
            │
            │  Oxidation zone mineral
            │  Arid climate, saline brines
            │  Soluble in water (rare)
            ▼
```

---

## The Argentite-Acanthite Polymorphic Transition

This is one of the most famous mineralogical phase transitions. Both minerals have the same formula (Ag₂S) but entirely different crystal structures:

| Property | Argentite (β-Ag₂S) | Acanthite (α-Ag₂S) |
|----------|-------------------|-------------------|
| **Temperature** | >173°C | <173°C |
| **Crystal system** | Cubic (isometric) | Monoclinic |
| **Space group** | Im-3m | P2₁/c |
| **Symmetry** | High — body-centered cubic | Low — no symmetry center |
| **Conductivity** | Metallic | Semiconductor |
| **Electron transport** | Free electrons (delocalized) | Hopping conduction |
| **Color** | Black | Lead-gray to iron-black |
| **Hardness** | ~2 | 2–2.5 |

**Critical behavior:** When argentite cools through 173°C, the internal structure switches to monoclinic acanthite, but the external cubic crystal shape is preserved. This is a **paramorph** — a mineral that keeps its parent's crystal form despite having a different internal structure. All natural Ag₂S at room temperature is acanthite, but many specimens still look cubic because they inherited argentite's form.

In the Vugg Simulator, this means:
- **Above 173°C**: nucleate argentite (cubic habit)
- **Cooling through 173°C**: automatic phase transition to acanthite
- **Visual result**: crystal keeps cubic outline but internal symmetry changes
- **Collector value**: paramorphic acanthite (pseudo-cubic) is more prized than naturally monoclinic acanthite

---

## Key Reactions

### Reaction 1: Argentite → Acanthite (cooling)
```
β-Ag₂S (argentite, cubic) ──► α-Ag₂S (acanthite, monoclinic)
                    at 173°C
```
No composition change. Purely structural. The cubic crystal becomes a monoclinic crystal wearing a cubic shell.

### Reaction 2: Acanthite → Native Silver (reduction, sulfide depletion)
```
Ag₂S + 2e⁻ → 2Ag⁰ + S²⁻
```
Requires strongly reducing conditions where sulfide is depleted (already precipitated as pyrite, galena, etc.). The electrons reduce Ag⁺ to Ag⁰.

### Reaction 3: Acanthite Oxidation → Silver Ions (supergene leaching)
```
Ag₂S + 2O₂ → 2Ag⁺ + SO₄²⁻
```
In the oxidation zone, acanthite dissolves, releasing Ag⁺ into descending groundwater. This is the transport step for supergene enrichment.

### Reaction 4: Silver Ions → Acanthite (supergene enrichment)
```
2Ag⁺ + H₂S → Ag₂S + 2H⁺
```
Descending Ag⁺ from oxidized acanthite above meets H₂S in the enrichment zone, reprecipitating as secondary acanthite. The ore upgrades itself.

### Reaction 5: Silver Ions + Chloride → Chlorargyrite (oxidation zone)
```
Ag⁺ + Cl⁻ → AgCl (chlorargyrite)
```
In arid climates with saline groundwater, silver precipitates as the halide rather than returning to sulfide. Chlorargyrite ("horn silver") was named for its horn-like masses and was one of the first silver ores recognized by ancient miners.

### Reaction 6: Native Silver Formation from Galena (supergene)
```
PbS (galena with Ag) + 2Ag⁺ → 2Ag⁰ + Pb²⁺ + S
```
Argentiferous galena is a common primary silver source. During supergene weathering, the Ag in galena is liberated and can reduce to native silver at the iron redox front.

---

## The Silver-Halide Branch

Silver is unique among base metals in forming **insoluble halides** that are stable across nearly all pH and Eh conditions:

| Halide | Formula | Solubility | Color | Zone |
|--------|---------|-----------|-------|------|
| Chlorargyrite | AgCl | Very low | Colorless to gray | Oxidation (arid) |
| Embolite | Ag(Cl,Br) | Very low | Pale yellow-green | Oxidation (arid) |
| Bromargyrite | AgBr | Very low | Pale yellow | Oxidation (coastal) |
| Iodargyrite | AgI | Very low | Yellow | Oxidation (iodine-rich) |

The extreme insolubility of silver halides means that **silver is relatively immobile in the supergene zone** compared to copper. Once silver hits chloride-rich groundwater, it precipitates as chlorargyrite and stays put. This is why silver enrichment blankets are thinner and less extensive than copper enrichment blankets — the silver gets trapped by chloride before it can travel far.

In the Vugg Simulator, if `trace_Cl` is tracked:
- High Cl⁻ + oxidizing → chlorargyrite instead of acanthite
- Low Cl⁻ + reducing → native silver or acanthite
- This is a branching mechanic: the halide diverts the silver from returning to sulfide

---

## Temperature-Eh Landscape

```
                    Eh (V vs SHE)
       reducing ──────────────────────── oxidizing
         -0.3       -0.1       +0.1      +0.3
          │          │          │         │
    300°C │          │          │         │
          │ Argentite│          │         │
          │ (cubic)  │          │         │
    173°C │──────────┤          │         │
          │ Acanthite│          │         │
          │(monoclinic)         │         │
    100°C │          │          │         │
     50°C │Native Ag │          │Acanthite│Chlorargyrite
          │          │          │(stable) │(if Cl⁻)
          └──────────┴──────────┴─────────┘
```

Key insight: **native silver requires the most reducing conditions AND depleted sulfur**. It's not just about Eh — it's about the absence of competitors for silver's bonding.

---

## Paragenetic Position in Multi-Metal Deposits

### Silver in Porphyry Copper Deposits
Most porphyry copper deposits contain minor silver (1–50 g/t) as a byproduct. The silver paragenesis follows the copper sulfide sequence:
1. **Primary**: Silver in solid solution in chalcopyrite, bornite, and tetrahedrite
2. **Supergene enrichment**: Released during chalcopyrite → chalcocite replacement, reprecipitates as acanthite or native silver
3. **Oxidation zone**: Chlorargyrite in arid climates; acanthite coating in humid climates

### Silver in Epithermal Veins
Epithermal deposits are the primary source of high-grade silver ore:
1. **High-sulfidation**: Argentite/acanthite + enargite + pyrite (acidic, oxidizing)
2. **Low-sulfidation**: Acanthite + pyrargyrite + proustite + native silver (neutral pH, reducing)
3. **Supergene**: Secondary acanthite + native silver wire growth in vugs

### Silver in Cobalt-Nickel-Arsenide Veins (Cobalt, Ontario type)
Unique paragenesis where silver is the main economic mineral:
1. **Primary**: Native silver + skutterudite + niccolite + cobaltite
2. **Supergene**: Secondary native silver + erythrite (cobalt bloom) + annabergite (nickel bloom)

---

## Famous Localities for the Full Sequence

### Kongsberg, Norway
The world's finest native silver locality. Calcite veins in Precambrian gneiss host wire silver to 30+ cm, acanthite coatings, and rare cubic silver crystals. The wires are electrum (Ag-Au alloy) in some cases. Famous specimens in Oslo Natural History Museum.

### Guanajuato, Mexico
Classic acanthite locality — paramorphic pseudo-cubic crystals from the Rayas Mine. Also pyrargyrite, proustite, and native silver. The transition from argentite to acanthite is visible in the crystal forms.

### Keweenaw Peninsula, Michigan, USA
Native silver in amygdaloidal basalt flows, associated with native copper. The silver and copper coexist in the same vugs — a rare paragenesis. Historic native American mining district.

### Cobalt, Ontario, Canada
Silver-arsenide vein district. Massive and dendritic native silver with cobaltite, skutterudite, and niccolite. The supergene zone produces spectacular secondary native silver.

### Butte, Montana, USA
In the copper sulfide supergene blanket, minor silver is released during chalcopyrite → chalcocite replacement. Silver appears as acanthite coatings on chalcocite and rare native silver inclusions.

### Imiter, Morocco
Giant silver mine with supergene enrichment. Primary acanthite + argentiferous galena → secondary acanthite + native silver in the oxidation zone. The upper levels contain native silver crystals to 300 kg/t.

---

## Individual Flavor Text for Each Mineral

### Argentite
> Argentite is silver sulfide trying to be a metal. Above 173°C, its crystal structure is cubic — body-centered, symmetric, conducting electricity like a true metal. It's the high-temperature form of what becomes acanthite, and like all high-temperature minerals, it can't survive cooling. Every cubic "argentite" specimen you've ever seen was actually acanthite in disguise: the internal lattice shifted to monoclinic, but the crystal's cubic outline remained, frozen in place like a ghost of its hotter self. True argentite exists only in furnaces and deep hydrothermal veins hot enough to keep it alive.

### Acanthite
> Acanthite is the cold-storage form of silver sulfide — what argentite becomes when the hydrothermal furnace cools below 173°C. The cubic crystal shapes it inherited from its hotter self don't change, even as the atomic lattice underneath quietly shifts from isometric to monoclinic. It's a mineral wearing its old clothes to a new job. At 87% silver by weight, it's the most important silver ore on Earth, yet most collectors know it as the dark tarnish on a native silver specimen. The thorn in its name is real: rare acanthite crystals sprout in spiky aggregates that look like mineral frost. Most of the world's historic silver — from Kongsberg's cathedral wires to Potosí's mountain of ore — passed through acanthite's lattice on its way to the smelter.

### Native Silver
> Native silver is a mineral that defies its own chemistry. Silver shouldn't exist as a native metal — it's too reactive, too eager to bond with sulfur or chlorine. But in the deep reducing zones of hydrothermal veins, where every sulfur atom has already been claimed, silver has nothing left to react with and simply precipitates as itself. The result is breathtaking: wire silver, crystallizing as delicate metallic threads that curl through open vugs like frozen lightning. Kongsberg, Norway produced wires over 30 cm long — cathedral spires of pure metal growing in calcite veins a kilometer underground. The Keweenaw Peninsula's basalt flows hosted silver alongside native copper, two impossible metals coexisting in volcanic rock. Tarnish is inevitable; every native silver specimen eventually develops a dark acanthite rind from atmospheric sulfur. But freshly broken surfaces still flash with the brightest metallic luster known to mineralogy. It's the only native element that can make you rich just by looking at it wrong.

---

## Simulator Implementation — Unified Zone Model

### New Parameters Needed
- `trace_Cl` (if not already tracked) — for chlorargyrite branch
- `argentite_stable` (boolean) — true when T > 173°C

### Phase Transition Event
```
EVENT: argentite_acanthite_transition
TRIGGER: temperature drops below 173°C AND argentite crystals present
EFFECT:
  - All argentite crystals convert to acanthite
  - Visual: keep cubic/paramorphic outline (flag as paramorph)
  - Chemistry: no change (same formula)
  - Crystal record updated: species = "acanthite", habit = "pseudo-cubic (paramorph)"
```

### Silver Nucleation Logic
```
IF T > 173°C AND trace_Ag > threshold AND trace_S > threshold
   AND Eh = reducing
   → nucleate ARGENTITE (cubic habit)

IF T < 173°C AND trace_Ag > threshold AND trace_S > threshold
   AND Eh = reducing
   → nucleate ACANTHITE (monoclinic habit, or paramorphic cubic if parent argentite)

IF trace_Ag > high_threshold AND trace_S ≈ 0 (depleted)
   AND Eh = strongly reducing
   → nucleate NATIVE SILVER (wire/dendritic habit)

IF trace_Ag > threshold AND trace_Cl > threshold
   AND Eh = oxidizing
   → nucleate CHLORARGYRITE (massive/horny habit)
```

### Supergene Enrichment Event
```
EVENT: silver_supergene_enrichment
TRIGGER: oxidation_zone above vug releases Ag⁺ into descending fluid
         AND vug is below water table (reducing)
         AND trace_S > threshold
EFFECT:
  - IF no Cl⁻: acanthite nucleates (secondary enrichment)
  - IF Cl⁻ present: chlorargyrite nucleates in oxidation zone above
  - Native silver may form at the redox front if S is locally depleted
```

### Cross-Zone Interactions
```
Copper sulfide zone → Silver release:
  When chalcopyrite → chalcocite replacement occurs,
  trace_Ag in solid solution is liberated.
  → Can nucleate acanthite or native silver in same vug

Iron oxidation zone → Silver immobilization:
  Fe²⁺ at the redox front reduces Ag⁺ → Ag⁰
  → Native silver forms at iron redox boundary
```

---

## Variants for Game — Paragenetic Sequence View

When the simulator shows a silver run in "Record Groove" mode or epilogue view, it should narrate the sequence:

1. **Epithermal Hot**: argentite cubes forming at 200°C (if scenario reaches high T)
2. **Cooling Transition**: argentite → acanthite paramorph at 173°C (visual only)
3. **Sulfide Stability**: acanthite as the stable silver carrier (most common)
4. **Sulfide Depletion**: native silver wires in the most reducing, S-depleted pockets
5. **Oxidation Branch**: chlorargyrite (if Cl⁻ and oxidizing) OR secondary acanthite (if reducing)

---

## Blockers

**None for the sulfide sequence.** Ag and S are already in the trace system. The polymorphic transition mechanic is a visual/structural feature (same formula, different crystal system) that the builder can implement with habit flags.

**Chlorargyrite branch** requires `trace_Cl` to be added to the trace element system. Cl is not currently tracked in the 30-element list. If the builder wants the halide branch, Cl addition is the blocker.

---

## Cross-References

- `memory/research-copper-sulfide-paragenesis.md` — Parallel copper system; silver commonly follows copper in porphyry deposits
- `memory/research-copper-oxidation-zone.md` — Silver released during copper sulfide enrichment feeds this sequence
- `memory/research-nickel-oxidation-zone.md` — Cobalt-nickel-silver veins (Cobalt, Ontario type)
- `memory/research-iron-oxidation-zone.md` — Fe²⁺ at the redox front reduces Ag⁺ to native silver
- `memory/research-tetrahedrite.md` — Silver-bearing sulfosalt; common primary silver host
- `memory/research-pyrargyrite.md` — Silver antimony sulfide; associated in epithermal veins
- `memory/research-proustite.md` — Silver arsenic sulfide; associated in epithermal veins

---

*"Silver keeps trying to become something else — sulfide, halide — and occasionally, in the right conditions, gets to just be itself."*
