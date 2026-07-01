# Copper Silicate Paragenesis — Unified Master File

**Date:** 2026-06-18
**Researcher:** 🪨✍️ (cron expansion)
**Status:** Complete
**Scope:** Unified paragenetic master file for the four copper silicate minerals: chrysocolla, shattuckite, plancheite, and dioptase. Links individual species research files into one coherent simulator-ready sequence.

---

## The Family

Four minerals. One chemistry: oxidized copper (Cu²⁺) plus mobilized silica (SiO₂) in alkaline groundwater. Four different architectures:

| Mineral | Formula | Structure | Color | pH | Cu:Si |
|---------|---------|-----------|-------|-----|-------|
| **Chrysocolla** | Cu₂₋ₓAlₓ(H₂₋ₓSi₂O₅)(OH)₄·nH₂O | Amorphous / phyllosilicate | Blue-green | 6.5–9.5 | Variable ~1:1 |
| **Shattuckite** | Cu₅(SiO₃)₄(OH)₂ | Inosilicate (pyroxene single chains) | Azure blue | 7.5–9.5 | 5:4 (1.25:1) |
| **Plancheite** | Cu₈(Si₄O₁₁)₂(OH)₄·H₂O | Inosilicate (amphibole double chains) | Turquoise | 7.5–9.5 | 1:1 |
| **Dioptase** | Cu₆Si₆O₁₈·6H₂O | Cyclosilicate (6-membered rings) | Emerald green | 8.5–10.5 | 1:1 |

The structural progression — amorphous → single chain → double chain → ring — is not coincidental. It tracks increasing silica availability and increasing structural order as the fluid evolves. The same progression appears in the major rock-forming silicates (olivine → pyroxene → amphibole → mica → feldspar → quartz), but here it plays out in a vug at ambient temperature over geological months instead of magmatic millennia.

---

## Shared Formation Requirements

All four minerals require the same foundational conditions. Without these, no copper silicate forms:

### 1. Oxidized Copper
- Primary Cu sulfides (chalcopyrite, chalcocite, bornite) must oxidize to release Cu²⁺
- Eh > +0.3 V (oxidizing conditions)
- Minimum Cu concentration: ~20 ppm (chrysocolla) to ~50 ppm (dioptase)

### 2. Mobilized Silica
- Silica solubility is pH-dependent: minimal below pH 7, rises dramatically above pH 8.5
- Requires alkaline groundwater, typically from carbonate buffering of sulfide oxidation acid
- Minimum SiO₂: ~10 ppm (chrysocolla) to ~30 ppm (dioptase)

### 3. Alkaline pH
- The critical gate. Silica mobilization requires pH > 8.5 for significant solubility
- Carbonate host rocks (limestone, dolomite) or calcareous gangue provide the buffer
- Without carbonate, sulfide oxidation produces acid that suppresses silica mobility

### 4. Arid to Semi-Arid Climate
- Wet climates leach away concentrated solutions
- Evaporation concentrates Cu and Si in the oxidation zone
- All famous localities are in arid/semi-arid regions (Kazakhstan, Namibia, Arizona, Congo)

---

## pH-Gated Paragenetic Sequence

The four minerals partition the oxidation zone by pH and silica concentration. In a typical fluid evolution:

```
Primary sulfide oxidation (acidic, pH < 4)
        │
        ▼
Carbonate buffering kicks in ───────────────┐
        │                                  │
        ▼                                  │
pH 6.5–7.5 (mildly acidic to neutral)      │
        │                                  │
        ▼                                  │
  ┌──────────────────────────────────────┐  │
  │  Chrysocolla nucleates               │  │
  │  (amorphous, least demanding)        │  │
  │  Low Si threshold, broad pH        │  │
  └──────────────────────────────────────┘  │
        │                                  │
        ▼                                  │
pH 7.5–8.5 (mildly alkaline)               │
        │                                  │
        ▼                                  │
  ┌──────────────────────────────────────┐  │
  │  Shattuckite nucleates               │  │
  │  (pyroxene chains, 1.25:1 Cu:Si)   │  │
  │  Earlier than dioptase               │  │
  └──────────────────────────────────────┘  │
        │                                  │
pH 8.0–9.5 (moderately alkaline)           │
        │                                  │
        ▼                                  │
  ┌──────────────────────────────────────┐  │
  │  Plancheite nucleates                │  │
  │  (amphibole double chains, 1:1)    │  │
  │  Moderate silica requirement         │  │
  └──────────────────────────────────────┘  │
        │                                  │
pH 8.5–10.5 (strongly alkaline) ───────────┘
        │
        ▼
  ┌──────────────────────────────────────┐
  │  Dioptase nucleates                │
  │  (cyclosilicate rings, 1:1 Cu:Si) │
  │  Highest silica demand             │
  │  Strictest pH gate                 │
  └──────────────────────────────────────┘
        │
        ▼
Late-stage silica flooding or pH drop
        │
        ▼
  Chrysocolla (fills remaining porosity)
  OR pseudomorph replacement of earlier minerals
```

**Key insight:** This sequence is NOT strictly temporal. All four can coexist if the vug maintains a pH gradient — higher pH near carbonate walls, lower pH in the center. A single vug can host chrysocolla on the outer rim, shattuckite and plancheite in the middle, and dioptase in the most alkaline pocket.

---

## Silica Competition Model

Silica is the limiting nutrient. All four minerals compete for the same dissolved SiO₂, but with different appetites:

| Mineral | SiO₂ Threshold | Cu:Si Ratio | Structural Order | Relative Appetite |
|---------|---------------|-------------|-----------------|-------------------|
| Chrysocolla | >10 ppm | Variable ~1:1 | Lowest (amorphous) | Omnivore — takes whatever's left |
| Shattuckite | >25 ppm | 5:4 = 1.25:1 | Low (single chains) | Early consumer, Cu-rich |
| Plancheite | >25 ppm | 1:1 | Medium (double chains) | Balanced consumer |
| Dioptase | >30 ppm | 1:1 | Highest (rings) | Gourmet — needs the best conditions |

**Simulator competition rule:** At any given pH and SiO₂ concentration, calculate σ (supersaturation) for all four. Nucleate in order of highest σ. Once silica is depleted below a mineral's threshold, that mineral can no longer nucleate. Existing crystals continue to grow until their local SiO₂ is exhausted.

---

## Cross-Mineral Interactions

### Replacement/Pseudomorph Series
In nature, late-stage chrysocolla commonly replaces earlier minerals:
- **Chrysocolla after azurite after malachite** — Lupoto Mine, Congo; Whim Creek, Australia
- **Chrysocolla after malachite** — widespread
- **Dioptase coatings on shattuckite** — Tsumeb
- **Plancheite intergrown with chrysocolla** — Milpillas

**Simulator mechanic:** If chrysocolla nucleates within proximity of an earlier copper mineral (azurite, malachite, or even dioptase/shattuckite), probability of pseudomorph replacement increases with time and Cu concentration.

### Silicification Pathway
Late-stage silica flooding can transform soft chrysocolla into hard "gem silica" (chalcedony-impregnated):
- Hardness rises from 2.5–3.5 to 6–7
- Translucency develops
- Color concentrates
- Value increases dramatically

**Simulator event:** `event_silicification` — triggers if SiO₂ > 200 ppm after chrysocolla exists for >50 steps. Transforms chrysocolla habit to "gem silica" variant.

---

## Famous Localities by Mineral

| Locality | Primary Mineral | Associated Cu-Silicates | Geological Notes |
|----------|---------------|------------------------|----------------|
| **Altyn-Tyube, Kazakhstan** | Dioptase | Chrysocolla | Type locality; arid, carbonate-buffered |
| **Tsumeb, Namibia** | Dioptase | Plancheite, chrysocolla | World's finest crystals; dolomite host |
| **Shattuck Mine, Bisbee, AZ** | Shattuckite | Chrysocolla, malachite | Type locality; pseudomorphs after malachite |
| **Kaokoveld, Namibia** | Shattuckite | Chrysocolla | Premier blue specimens |
| **Mindouli, Congo** | Plancheite | Chrysocolla, dioptase | Type locality; chatoyant crusts |
| **Milpillas, Sonora, MX** | Plancheite | Chrysocolla, malachite | Unusual primary association |
| **Morenci/Ray, AZ** | Chrysocolla | — | Classic US blue-green botryoidal |
| **Lupoto Mine, Congo** | Chrysocolla | — | Double pseudomorphs (after malachite after azurite) |
| **Timna Valley, Israel** | Chrysocolla | Turquoise, malachite | Eilat stone; King Solomon's mines |

**Pattern recognition:** Every world-class copper silicate locality is in an arid climate with carbonate host rocks. The simulator should weight these conditions heavily.

---

## Simulator Events

### `event_carbonate_buffer`
**Trigger:** Sulfide oxidation produces acid (H⁺, SO₄²⁻) AND carbonate minerals (calcite, dolomite) are present in the vug wall or matrix.
**Effect:** pH rise to 7.5–9.5 instead of dropping to <4. Enables silica mobilization. Required pre-condition for all copper silicates.

### `event_silica_mobilization`
**Trigger:** pH > 8.0 AND SiO₂ > 15 ppm from host rock dissolution or hydrothermal fluid.
**Effect:** Silica becomes bioavailable. σ_dioptase, σ_shattuckite, σ_plancheite, σ_chrysocolla begin rising.

### `event_copper_silicate_nucleation_wave`
**Trigger:** pH > 7.5, SiO₂ > 20 ppm, Cu > 40 ppm, Eh > +0.4V.
**Effect:** All four copper silicates calculate σ simultaneously. Nucleation order determined by pH and SiO₂:
- pH 6.5–7.5 → chrysocolla only
- pH 7.5–8.5 → chrysocolla + shattuckite
- pH 8.0–9.5 → chrysocolla + shattuckite + plancheite
- pH 8.5–10.5 → all four (chrysocolla + shattuckite + plancheite + dioptase)

### `event_silicification`
**Trigger:** Chrysocolla exists for >50 steps AND SiO₂ > 200 ppm (late silica flood).
**Effect:** Transform chrysocolla variant to "Gem Silica" (harder, translucent, more valuable).

### `event_pseudomorph_replacement`
**Trigger:** Chrysocolla nucleates within 1 cell of azurite, malachite, or dioptase.
**Effect:** Probability (increasing with time, Cu concentration, and temperature) that chrysocolla replaces the target mineral while preserving its crystal habit.

---

## Individual Flavor Texts

### Chrysocolla
> The Greeks called it *gold-glue* — the flux that bound the precious metal. But chrysocolla is its own treasure: a blue-green gel frozen in time, the amorphous edge of the copper oxidation zone where chemistry ran out of patience before it ran out of copper. It forms botryoidal masses that look like frozen drips, or replaces azurite blade-for-blade in pseudomorphs so perfect they keep the ghost-shape of a mineral that no longer lives there. Heavily silicified, it becomes gem silica — hard enough to cut, translucent enough to glow.

*(Full research: `memory/research-chrysocolla.md`)*

### Shattuckite
> Deep in the oxidation zone, where copper weathers out of its sulfide cage and meets silica in alkaline groundwater, a blue stranger appears. Shattuckite: named for an Arizona mine where it stole malachite's shape atom by atom, leaving the ghost of green in a body of blue. It grows in sprays and spheres — a copper sky frozen in stone.

*(Full research: `memory/research-shattuckite.md`)*

### Plancheite
> In the oxidation zone, where copper weathers free of its sulfide bonds and meets silica in alkaline water, four copper silicates compete for the same atoms. Dioptase claims the emerald green. Shattuckite takes the azure blue. Chrysocolla accepts whatever is left, amorphous and forgiving. And plancheite — pale turquoise, almost forgettable beside its vivid cousins — holds a secret in its chains. Where shattuckite built pyroxene-like single chains and dioptase closed hers into rings, plancheite grew amphibole-like double chains: the same architecture that carries tremolite through mountain ranges.

*(Full research: `memory/research-plancheite.md`)*

### Dioptase
> In the sun-baked oxidation zone of a copper deposit, where sulfide-burning acids meet carbonate-buffered alkalinity, silica finally dissolves — and meets copper in a marriage of emerald green. The miners of Altyn-Tyube thought they had found emerald; what they found was rarer. Dioptase: the mineral that fools the eye and breaks the heart (handle gently — it's fragile).

*(Full research: `memory/research-dioptase.md`)*

---

## Implementation Priority for Builder

### Phase 1: Gates
1. Add `pH_silica_mobilization` parameter (silica solubility threshold at pH > 8.5)
2. Add `carbonate_buffer` check — if carbonate host present, sulfide oxidation acid is buffered
3. Ensure Cu is tracked as Cu²⁺ in oxidizing conditions

### Phase 2: Supersaturation Functions
Implement four σ functions following the existing pattern in `js/41-supersat-*.ts`:
- `supersaturation_chrysocolla(broth)` — lowest threshold, broadest pH
- `supersaturation_shattuckite(broth)` — moderate threshold, pH 7.5+
- `supersaturation_plancheite(broth)` — moderate threshold, pH 7.5+, balanced Cu:Si
- `supersaturation_dioptase(broth)` — highest threshold, strict pH 8.5+

### Phase 3: Nucleation Habits
Implement habit selection logic per individual research files:
- Chrysocolla: botryoidal, stalactitic, crust, pseudomorph, gem silica
- Shattuckite: botryoidal, fibrous spray, pseudomorph after malachite
- Plancheite: radial spray, fibrous crust, spherulitic
- Dioptase: rhombohedral prism, microcrystalline crust

### Phase 4: Simulator Events
Wire the five events listed above into the event system.

### Phase 5: Cross-References
Link to existing master files:
- `memory/research-copper-oxidation-zone.md` (Cu sulfide → Cu oxide/carbonate/sulfate/silicate)
- `memory/research-iron-oxidation-zone.md` (if Fe competes for Si in the same vug)

---

## Cross-Reference Index

| Mineral | Individual File | Notes |
|---------|----------------|-------|
| Chrysocolla | `memory/research-chrysocolla.md` | Broadest pH, amorphous, pseudomorph champion |
| Shattuckite | `memory/research-shattuckite.md` | Pyroxene chains, pH 7.5–9.5, azure blue |
| Plancheite | `memory/research-plancheite.md` | Amphibole double chains, hardest Cu-silicate |
| Dioptase | `memory/research-dioptase.md` | Cyclosilicate rings, strictest pH, gemmy |
| Copper Oxidation Zone | `memory/research-copper-oxidation-zone.md` | Master file for Cu sulfide → oxide/carbonate/sulfate |
| Malachite | `memory/research-malachite.md` | Carbonate Cu mineral, co-occurs in oxidation zone |
| Azurite | `memory/research-azurite.md` | Carbonate Cu mineral, precursor to pseudomorphs |
| Broth Ratio (malachite/azurite) | `memory/research-broth-ratio-malachite-azurite.md` | pH-CO₃²⁻ controls on Cu carbonate formation |

---

*Completed: 2026-06-18. All four individual species files were previously complete (2026-06-06 through 2026-06-07). This master file unifies them into one simulator-ready paragenetic sequence.*
