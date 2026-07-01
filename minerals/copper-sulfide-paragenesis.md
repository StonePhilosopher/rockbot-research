# Copper Sulfide Paragenesis — Unified Master File

**Date:** 2026-06-08
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering chalcopyrite → bornite → chalcocite → covellite as a single hypogene-to-supergene sulfide enrichment system.
**Related files:**
- `memory/research-chalcopyrite.md` — CuFeS₂ (primary hypogene sulfide)
- `memory/research-bornite.md` — Cu₅FeS₄ (primary + transitional)
- `memory/research-chalcocite.md` — Cu₂S (supergene enrichment)
- `memory/research-covellite.md` — CuS (supergene transition)
- `memory/research-copper-oxidation-zone.md` — Native copper → cuprite → malachite/azurite (oxidation zone continuation)
- `memory/research-enargite.md` — Cu₃AsS₄ (high-sulfidation porphyry endpoint)

---

## The Story This Sequence Tells

The copper sulfide paragenesis is the story of a porphyry copper deposit aging — from molten intrusion through cooling, uplift, exposure, and weathering. The same copper atoms, captured first in iron-bearing chalcopyrite, are progressively stripped of their iron and enriched through a cascade of replacement reactions that make each successive mineral more copper-rich than the last.

This is metallurgical alchemy performed by water and time. The ore literally gets better as the deposit weathers.

At the deepest level: chalcopyrite (34.6% Cu). After supergene enrichment: chalcocite (79.8% Cu). A 2.3× concentration upgrade, performed by groundwater over hundreds of thousands of years.

---

## The Full Sequence (Hypogene → Supergene)

```
HOT, DEEP, REDUCING                    COOL, SHALLOW, OXIDIZING
        │                                        │
        ▼                                        ▼

Primary zone (hypogene, 300–600°C):
  Chalcopyrite (CuFeS₂) ──► Bornite (Cu₅FeS₄)
    │                          │
    │    Cu:Fe = 1:1           │    Cu:Fe = 5:1
    │    34.6% Cu              │    63.3% Cu
    │                          │
    │    Exsolution:           │    Exsolution:
    │    chalcopyrite          │    chalcopyrite
    │    lamellae in bornite   │    lamellae in bornite
    │    (cooling product)     │    (cooling product)
    │                          │
    ▼                          ▼
    Uplift + groundwater table establishes
    ▼
Supergene enrichment zone (<150°C, below water table):
  
  Bornite + descending Cu²⁺ ──► Chalcocite (Cu₂S)
         │                         │
         │    Fe leached away      │    79.8% Cu
         │    Cu added             │    No Fe remaining
         │                         │
         │    Pseudomorphs:        │    Pseudomorphs:
         │    bornite → chalcocite │    chalcopyrite → chalcocite
         │                         │
         ▼
    Chalcocite + sulfur ──► Covellite (CuS)
         │                    │
         │    S added         │    66.5% Cu
         │    (sulfur-rich    │    Highest S content
         │     fluids)        │
         │                    │
         │    Can coat or     │    Can pseudomorph
         │    replace         │    after chalcocite
         │    chalcocite      │
         ▼
    Partial oxidation begins:
    Covellite ──► Cuprite (Cu₂O) ──► Malachite / Azurite
         │              │                  │
         │    Eh rises  │    More O₂       │    CO₂ present
         │    Cu⁺→Cu²⁺  │    Cu⁺→Cu²⁺      │    Carbonate
         │              │                  │
         ▼              ▼                  ▼
    [Continues in memory/research-copper-oxidation-zone.md]
```

---

## Key Replacement Reactions

### Reaction 1: Chalcopyrite → Bornite (hypogene)
```
5 CuFeS₂ + 2 Cu⁺ + 2 e⁻ → Cu₅FeS₄ + 4 Fe²⁺ + 6 S²⁻
```
Simplified: chalcopyrite loses Fe, gains Cu. Requires Cu-rich fluid at 250–400°C.

### Reaction 2: Bornite → Chalcocite (supergene enrichment)
```
Cu₅FeS₄ + 3 Cu²⁺ (descending) → 4 Cu₂S + Fe²⁺ + 2 S
```
The signature supergene enrichment reaction. Descending Cu²⁺ (leached from oxidizing ore above) reacts with primary bornite, displacing Fe and concentrating Cu.

### Reaction 3: Chalcopyrite → Chalcocite (direct supergene)
```
2 CuFeS₂ + 3 Cu²⁺ + 6 e⁻ → 2 Cu₂S + 2 Fe²⁺ + 4 S²⁻
```
Direct replacement when bornite is absent or already consumed.

### Reaction 4: Chalcocite → Covellite (sulfur addition)
```
Cu₂S + S⁰ → 2 CuS
```
Where sulfur-rich fluids encounter chalcocite, sulfur is added rather than Cu. Results in covellite — lower Cu grade but striking indigo-blue color.

### Reaction 5: Covellite decomposition (temperature)
```
2 CuS ──► Cu₂S + S (at >507°C)
```
Covellite is thermally unstable. In the Vugg Simulator, this means a late-stage thermal event can convert covellite back to chalcocite, releasing sulfur vapor into the fluid.

---

## The Cu:S Ratio Ladder

| Mineral | Formula | Cu:S | % Cu | Zone |
|---------|---------|------|------|------|
| Chalcopyrite | CuFeS₂ | 1:2 | 34.6% | Primary (hypogene) |
| Bornite | Cu₅FeS₄ | 5:4 | 63.3% | Primary / Transitional |
| Chalcocite | Cu₂S | 2:1 | 79.8% | Supergene enrichment |
| Covellite | CuS | 1:1 | 66.5% | Supergene transition |
| Cuprite | Cu₂O | — | 88.8% | Oxidation |
| Native copper | Cu | — | 100% | Most reducing |

The progression from chalcopyrite to chalcocite is a **Cu enrichment** trend — the deposit literally concentrates its own copper through weathering. This is why supergene enrichment blankets are among the most valuable copper ores on Earth.

---

## Temperature-Eh Landscape

```
                    Eh (V vs SHE)
       reducing ──────────────────────── oxidizing
         -0.2        0.0       +0.2       +0.4
          │           │          │          │
    500°C │           │          │          │
          │  Chalcopyrite        │          │
          │  Bornite             │          │
    300°C │           │          │          │
          │           │          │          │
    150°C │           │ Chalcocite│          │
          │           │ (supergene)         │
     50°C │           │ Covellite │ Cuprite  │
          │           │           │ Malachite│
     25°C │Native Cu  │           │ Azurite  │
          │           │           │          │
          └───────────┴───────────┴──────────┘
```

Key insight: **temperature and Eh trade off**. At high temperature, reducing conditions can still be oxidizing relative to room-temperature standards. The sulfide stability field expands upward with temperature.

---

## The Supergene "Blanket" Concept

In real porphyry copper deposits, the supergene enrichment zone forms a laterally extensive layer — the "chalcocite blanket" — ranging from 10 to 2,500 feet thick. It sits at the paleo-water table, where descending oxygenated water meets primary sulfides.

In the Vugg Simulator, this translates to a **zone mechanic**:

1. **Primary zone** (deep, hot, reducing): chalcopyrite + bornite nucleate and grow
2. **Cooling event**: temperature drops, fluid becomes less reducing
3. **Supergene zone** (cool, mildly reducing): descending Cu²⁺ triggers chalcocite nucleation via replacement
4. **Transition zone** (cool, boundary): covellite forms where sulfur is abundant
5. **Oxidation zone** (cool, oxidizing): cuprite, malachite, azurite, brochantite, antlerite

The blanket has **internal structure**:
- **Upper blanket**: chalcocite dominant, replacing bornite
- **Lower blanket**: covellite dominant, where sulfur-rich fluids linger
- **Base**: relict chalcopyrite (not fully replaced)

---

## Pseudomorph Mechanics

A pseudomorph is a mineral that preserves the crystal shape of another mineral it replaced. In copper sulfide paragenesis, pseudomorphs are common and diagnostic:

| Pseudomorph | Parent Shape | Product | How |
|-------------|-----------|---------|-----|
| Chalcocite after chalcopyrite | Tetrahedron | Cu₂S | Cu²⁺ replaces CuFeS₂ atom by atom |
| Chalcocite after bornite | Cuboctahedron | Cu₂S | Same reaction on bornite |
| Chalcocite after pyrite | Cube | Cu₂S | Pyrite becomes chalcocite ghost |
| Covellite after chalcopyrite | Tetrahedron | CuS | Sulfur addition to CuFeS₂ |
| Covellite after enargite | Prismatic | CuS | High-sulfidation replacement |

In the Vugg Simulator, pseudomorphs should be modeled as:
- **Shape inheritance**: the new mineral uses the parent crystal's shape (not its own default habit)
- **Texture flag**: marked as "pseudomorph" in the crystal record
- **Chemical continuity**: the parent mineral's trace elements may be partially inherited

---

## Inter-Zone Interactions

### Copper sulfide zone ↔ Iron oxidation zone
The iron liberated from chalcopyrite/bornite during supergene enrichment (Fe²⁺) feeds goethite and hematite formation in the iron oxidation zone. The copper sulfide and iron oxidation zones are chemically coupled through shared Fe.

### Copper sulfide zone ↔ Enargite zone
In high-sulfidation systems, enargite (Cu₃AsS₄) may precede or replace chalcopyrite. Enargite → covellite is a documented replacement in some deposits (Butte, Montana). The arsenic released during this reaction can feed arsenate minerals (olivenite, clinoclase) in the oxidation zone.

### Copper sulfide zone ↔ Zinc oxidation zone
Sphalerite (ZnS) commonly coexists with chalcopyrite. During supergene weathering, Zn²⁺ descends separately from Cu²⁺ because zinc has different Eh-pH stability. This separation explains why smithsonite and chalcocite can form in the same deposit but in different zones.

---

## Famous Localities for the Full Sequence

### Butte, Montana, USA
The type locality for supergene enrichment theory. Enormous chalcocite blanket (hundreds of meters thick) over primary chalcopyrite-bornite ore. Famous for: chalcocite sixlings, covellite coatings on bornite, enargite → covellite pseudomorphs.

### Chuquicamata, Chile
World's largest supergene enrichment blanket (up to 2,500 ft thick). Massive chalcocite replacing primary chalcopyrite. The deposit that proved supergene theory at industrial scale.

### Cornwall, England
Historic source of stellate chalcocite crystals ("redruthite"). Also famous for bornite ("peacock ore") and chalcopyrite. Classic example of primary + limited supergene sequence in a compact district.

### Morenci, Arizona, USA
Well-studied porphyry system with clear zonation: leached cap → oxidized zone → supergene chalcocite blanket → primary chalcopyrite-bornite. Used as the textbook example in economic geology courses.

### Mount Isa, Queensland, Australia
Sedimentary-hosted copper sulfide sequence: chalcopyrite → bornite → chalcocite in stratiform beds. Shows the same paragenetic sequence can occur in non-porphyry settings.

---

## Individual Flavor Text for Each Mineral

### Chalcopyrite
> The common copper ore — the mineral that launched Bronze Age civilizations. Its brass-yellow tetrahedra are so distinctive that prospectors call it "fool's gold," but there's nothing foolish about a mineral that contains both copper and iron in perfect stoichiometric marriage. In the dark, hot heart of a porphyry deposit, chalcopyrite is the beginning of a story that ends with bright green malachite on the surface. It holds the copper. Everything after is just rearrangement.

### Bornite
> Bornite is the mineral that shows off. Fresh from the rock it's a humble bronze — but give it air and it transforms, cycling through every color in a peacock's tail as oxide layers of different thicknesses stack on its surface. Thin-film interference, the same physics behind soap bubbles, turns a copper ore into a rainbow. Those colors aren't bornite anymore — they're its ghost, the mineral performing its own oxidation in real time.

### Chalcocite
> Chalcocite is a thief that wears its victim's face. In the supergene enrichment zone — that shadowy band between the oxygen-rich world above and the sulfide-dark depths below — copper leached from oxidizing ore descends and reacts with primary chalcopyrite, stealing its iron and sulfur to make something richer. Nearly 80% copper by weight, it's one of the richest ores that exists. And sometimes it performs a mineralogical heist: replacing another crystal atom by atom while keeping the original shape perfectly intact. A chalcopyrite-shaped ghost, now made of purer copper than the original ever was.

### Covellite
> Covellite is the blue heart of the copper deposit — the only common mineral that's naturally indigo. Where chalcocite hoards copper and covellite shares it with sulfur in equal measure, the result is a mineral so soft you can peel it into flexible sheets like dark blue mica. It forms at the knife-edge boundary where descending copper-rich waters meet sulfur-rich primary ore — not quite oxidized, not quite reduced. A transitional species, born in the tension between two chemical worlds, wearing a color that belongs to neither.

---

## Simulator Implementation — Unified Zone Model

### New Parameters Needed
- `supergene_zone` (boolean): true when the vug is below the water table but above the primary zone
- `descending_Cu` (ppm): Cu²⁺ concentration in descending meteoric water
- `paleo_water_table` (depth marker): the boundary between oxidation and enrichment

### Zone Detection Logic
```
IF depth > water_table AND temperature < 150°C AND Eh < +0.1V
   → supergene_zone = true
   → chalcocite/covellite can nucleate via replacement
```

### Enrichment Reaction Event
```
EVENT: supergene_enrichment
TRIGGER: supergene_zone == true AND descending_Cu > 100 ppm
         AND (chalcopyrite OR bornite present in vug)
EFFECT:
  - IF bornite present:
      bornite dissolves at rate 3
      chalcocite nucleates, inherits bornite's shape (pseudomorph)
      Fe²⁺ released to broth
  - IF chalcopyrite present AND no bornite:
      chalcopyrite dissolves at rate 2
      chalcocite nucleates, inherits chalcopyrite's shape
      Fe²⁺ released to broth
  - IF trace_S > 200 AND chalcocite present:
      chalcocite may partially convert to covellite (S addition)
```

### Cu:S Ratio Branching
```
IF supergene_zone == true:
   IF trace_Cu / trace_S > 2.0:
      → favor chalcocite (Cu-rich)
   IF trace_Cu / trace_S in [0.8, 2.0]:
      → favor covellite (S-rich)
   IF trace_Cu / trace_S < 0.8:
      → no Cu sulfide nucleates (insufficient Cu)
```

### Thermal Decomposition Chain
```
IF temperature > 507°C AND covellite present:
   covellite → chalcocite + S_vapor
   S_vapor added to broth (+trace_S)

IF temperature > 103°C AND chalcocite present:
   chalcocite polymorph transition (monoclinic → hexagonal)
   (visual only — no composition change)

IF temperature > 228°C AND bornite present:
   bornite order-disorder transition (orthorhombic → isometric)
   (visual only — crystal shape changes from massive to pseudo-cubic)
```

---

## Variants for Game — Paragenetic Sequence View

When the simulator shows a copper sulfide run in "Record Groove" mode or epilogue view, it should narrate the sequence:

1. **Porphyry Primary**: chalcopyrite tetrahedra + bornite disseminations (hot, deep, reducing)
2. **Transitional Bornite**: bornite with chalcopyrite exsolution lamellae (cooling below 228°C)
3. **Enrichment Blanket**: chalcocite replacing bornite pseudomorphically (cool, mildly reducing)
4. **Transition Zone**: covellite coating chalcocite, or replacing it (boundary conditions)
5. **Oxidized Cap**: cuprite, malachite, azurite — the story's colorful end → `memory/research-copper-oxidation-zone.md`

---

## Blockers

None. All elements (Cu, Fe, S) are already in the trace system. The supersaturation functions for chalcopyrite, bornite, chalcocite, and covellite already exist in the simulator.

The unified zone model (supergene enrichment event, descending Cu²⁺, pseudomorph mechanics) is **design documentation** for future builder implementation. No new trace elements or chemistry conditions are needed.

---

## Cross-References

- `memory/research-copper-oxidation-zone.md` — Continuation of this sequence into the oxidation zone (native copper, cuprite, malachite, azurite)
- `memory/research-iron-oxidation-zone.md` — Iron released from chalcopyrite/bornite during supergene enrichment feeds goethite/hematite
- `memory/research-zinc-oxidation-zone.md` — Sphalerite commonly coexists with chalcopyrite; Zn and Cu separate during weathering
- `memory/research-enargite.md` — High-sulfidation Cu-As sulfide that may precede or replace chalcopyrite in some deposits
- `memory/research-broth-ratio-malachite-azurite.md` — Carbonate zone branching after cuprite

---

*"The deposit concentrates its own copper through weathering. A chalcopyrite-shaped ghost, now made of purer copper than the original ever was."*
