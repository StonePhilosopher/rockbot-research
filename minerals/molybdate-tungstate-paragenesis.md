# Molybdate–Tungstate Paragenetic Sequence — Vugg Simulator

**Research Date:** 2026-06-14
**Scope:** Unified paragenetic master covering the full Mo–W oxidation zone sequence, from primary sulfide/oxide precursors through secondary molybdates and tungstates.
**Linked Individual Files:** `research-molybdenite.md`, `research-wulfenite.md`, `research-powellite.md`, `research-scheelite.md`, `research-stolzite.md`, `research-raspite.md`, `research-ferrimolybdite.md`, `research-wolframite.md`

---

## Conceptual Overview

The molybdate–tungstate paragenetic sequence is a **two-branched oxidation cascade** that starts with primary minerals deep in hydrothermal systems and converges in the supergene zone. Unlike the lead oxidation zone (where one element — Pb — branches across multiple anions) or the copper oxidation zone (where one element — Cu — changes oxidation state), the Mo–W sequence is defined by **two rare heavy metals** that share crystal-chemical behavior:

- Both Mo and W are Group 6 elements with stable +6 oxidation states
- Both form tetrahedral oxyanions (MoO₄²⁻ and WO₄²⁻) that are structurally interchangeable
- Both precipitate as dense, brightly colored secondary minerals when they meet appropriate cations (Pb²⁺, Ca²⁺, Fe³⁺)
- Both have primary sulfide/oxide precursors that must oxidize before secondary minerals can form

The sequence splits early (primary stage) and converges late (supergene stage):

```
PRIMARY (hypogene, reducing, high-T)
├── Molybdenite (MoS₂) ──┐
│   H=1, hexagonal, greasy │
│   porphyry/skarn/vein    │
│                          │
└── Wolframite ((Fe,Mn)WO₄) ──┐
    H=5.5, monoclinic          │
    vein/greisen/skarn         │
                               │
OXIDATION (supergene, oxidizing, low-T)
│                              │
├─ Mo branch ──────────────────┤
│  MoS₂ + O₂ + H₂O → MoO₄²⁻ + H⁺
│  ├─ IF Pb²⁺ present → Wulfenite (PbMoO₄), tetragonal, orange
│  ├─ IF Ca²⁺ present → Powellite (CaMoO₄), tetragonal, yellow
│  └─ IF Fe³⁺ present, Pb absent → Ferrimolybdite (Fe₂(MoO₄)₃·8H₂O), orthorhombic, canary yellow
│
├─ W branch ───────────────────┤
│  (Fe,Mn)WO₄ + O₂ → WO₄²⁻ + Fe/Mn oxides
│  ├─ IF Ca²⁺ present → Scheelite (CaWO₄), tetragonal, white/yellow
│  └─ IF Pb²⁺ present → Stolzite (PbWO₄), tetragonal, brown/yellow
│      └─ OR Raspite (PbWO₄), monoclinic, yellow/brown (dimorph competition)
│
└─ Crossover ──────────────────┘
   Wulfenite–Stolzite–Raspite solid solution (Mo ↔ W)
   Scheelite–Powellite solid solution (W ↔ Mo)
```

The key insight for the simulator: **you cannot have secondary molybdates or tungstates without first having primary precursors that oxidize.** This is not an "elements arrive in fluid" scenario — it's a "primary minerals must be destroyed to feed the oxidation zone" scenario. The sequence is fundamentally **destructive-constructive**: old crystals die, release their metals into solution, and new crystals form from the remains.

---

## Primary Precursors: Deep Formation

### Molybdenite (MoS₂)
- **Depth:** Primary/hypogene — 350–600°C, reducing conditions
- **Habitat:** Porphyry Mo deposits (Climax-type), porphyry Cu-Mo skarns, high-T veins
- **Role:** The sole natural source of Mo for the oxidation zone. Without molybdenite (or its oxidation), no wulfenite, no powellite, no ferrimolybdite.
- **Oxidation reaction:** MoS₂ + 7.5O₂ + 3H₂O → MoO₄²⁻ + 2SO₄²⁻ + 6H⁺
  - Acidifies fluid (produces H⁺)
  - Releases molybdate ion (MoO₄²⁻), the mobile transport species
- **Simulator event:** `event_molybdenite_oxidation` — triggered when Eh rises and O₂ penetrates. Releases trace_Mo from crystal into fluid as MoO₄²⁻. Can be partial (rim oxidation) or complete (full dissolution).

### Wolframite ((Fe,Mn)WO₄)
- **Depth:** Primary/hypogene — 300–500°C, moderate Eh
- **Habitat:** Quartz veins, greisens, skarns
- **Role:** Primary source of W for the oxidation zone. Along with scheelite (which can be primary OR secondary), wolframite feeds the tungstate cascade.
- **Oxidation reaction:** (Fe,Mn)WO₄ + O₂ + H₂O → WO₄²⁻ + Fe(OH)₃/MnO₂
  - Less acidic than molybdenite oxidation (no sulfuric acid)
  - Releases tungstate ion (WO₄²⁻)
- **Simulator event:** `event_wolframite_oxidation` — releases trace_W into fluid. Fe and Mn precipitate as oxides/hydroxides locally.

### Scheelite (CaWO₄) — Dual Role
- **Depth:** Can be primary (200–500°C, skarns) OR secondary (weathering product of wolframite)
- **Role:** In the Mo–W sequence, scheelite is ambiguous. It forms primary in skarns but can also reprecipitate from wolframite oxidation. In the simulator, treat it as **primary when temp > 200°C, secondary when temp < 100°C**.
- **Key crossover:** Scheelite and powellite form a complete solid solution. A crystal can start as scheelite (W-rich) and become powellite-like (Mo-rich) if MoO₄²⁻ arrives later.

---

## The Oxidation Zone: Three Cation Gateways

Once MoO₄²⁻ and/or WO₄²⁻ are in solution, three cations compete to precipitate them:

### 1. Lead Gateway — Wulfenite / Stolzite / Raspite
**Pb²⁺ + MoO₄²⁻ → Wulfenite (PbMoO₄)**
**Pb²⁺ + WO₄²⁻ → Stolzite (PbWO₄)** or **Raspite (PbWO₄)**

- **Pb source:** Galena (PbS) oxidation — same Pb pool that feeds anglesite, cerussite, pyromorphite
- **Competition:** Wulfenite competes with pyromorphite/mimetite/vanadinite for Pb AND with powellite/scheelite for the oxyanion
- **Dimorph competition (W only):** Stolzite (tetragonal) vs Raspite (monoclinic)
  - Raspite is the true low-T stable form (<395°C)
  - Stolzite nucleates more readily even below 395°C (metastable persistence of high-T form)
  - In practice, both form at ambient T; stolzite is more common because kinetic barriers favor tetragonal nucleation
  - **Simulator rule:** If both Pb²⁺ and WO₄²⁻ are present, nucleate stolzite with 70% probability, raspite with 30%. If reheated above 395°C, raspite converts to stolzite.
- **Solid solution:** Wulfenite (Mo) ↔ Stolzite/Raspite (W) — complete series. Intermediate compositions should be named as "wulfenite-stolzite" or "wulfenite-raspite" with color gradation.

### 2. Calcium Gateway — Powellite / Scheelite
**Ca²⁺ + MoO₄²⁻ → Powellite (CaMoO₄)**
**Ca²⁺ + WO₄²⁻ → Scheelite (CaWO₄)**

- **Ca source:** Host rock (limestone, basalt), alteration of plagioclase, or primary scheelite dissolution
- **Competition:** Fluorite and apatite compete for Ca²⁺; if F or PO₄³⁻ are high, scheelite/powellite may be suppressed
- **Fluorescence distinction:** Scheelite = blue SW UV. Powellite = yellow SW UV. Same lattice, different metal, different glow. This is the single most useful field discriminator.
- **Solid solution:** Scheelite (W) ↔ Powellite (Mo) — complete series. Intermediate "scheelite-powellite" is common in nature.
- **Simulator rule:** If both Ca²⁺ and MoO₄²⁻/WO₄²⁻ are present, check Ca budget after fluorite/apatite nucleation. Remaining Ca nucleates scheelite/powellite. Color and fluorescence shift with Mo:W ratio.

### 3. Iron Gateway — Ferrimolybdite
**2Fe³⁺ + 3MoO₄²⁻ + 8H₂O → Fe₂(MoO₄)₃·8H₂O**

- **Fe source:** Pyrite/marcasite oxidation — ubiquitous in most ore deposits
- **Key condition:** Pb must be ABSENT or nearly absent. If Pb is available, wulfenite wins (higher stability, lower solubility product)
- **pH sensitivity:** Ferrimolybdite prefers acidic conditions (pH 2–6). At higher pH, Fe³⁺ precipitates as goethite/limonite instead.
- **Simulator rule:** IF MoO₄²⁻ present AND Fe³⁺ present AND Pb < threshold AND pH < 6 → nucleate ferrimolybdite. Forms as crusts/tufts on oxidizing molybdenite surfaces.

---

## Fluid Chemistry Controls: The Mo–W–Pb–Ca–Fe System

### Temperature Control
| Stage | Temperature | Minerals |
|-------|-------------|----------|
| Primary | 300–600°C | Molybdenite, wolframite, primary scheelite |
| Transitional | 100–300°C | Rare — retrograde scheelite replacing wolframite |
| Supergene | 15–80°C | Wulfenite, powellite, stolzite, raspite, ferrimolybdite |

### pH Control
| pH Range | Dominant Mo/W Species | Favored Minerals |
|----------|----------------------|------------------|
| <4 (acidic) | H₂MoO₄, H₂WO₄ | Ferrimolybdite (if Fe³⁺ available) |
| 4–7 (mildly acidic) | MoO₄²⁻, WO₄²⁻ | Wulfenite, stolzite, raspite, scheelite |
| 7–9 (neutral-alkaline) | MoO₄²⁻, WO₄²⁻ | Scheelite, powellite, wulfenite |
| >9 (strongly alkaline) | MoO₄²⁻, WO₄²⁻ | Powellite (Ca more available at high pH) |

### Eh Control
- **Reducing (Eh < 0):** Molybdenite stable, wolframite stable. No secondary molybdates/tungstates.
- **Moderately oxidizing (Eh 0–0.3):** MoS₂ oxidizes to MoO₄²⁻. Wulfenite, powellite, ferrimolybdite can nucleate.
- **Strongly oxidizing (Eh > 0.3):** All sulfides oxidized. Maximum secondary mineral diversity.

### Cation Competition Matrix
Given MoO₄²⁻ and/or WO₄²⁻ in solution, which mineral forms?

| Cation Priority | Condition | Result |
|-----------------|-----------|--------|
| 1st: Pb²⁺ | Pb > threshold, any pH | Wulfenite (if Mo) or Stolzite/Raspite (if W) |
| 2nd: Ca²⁺ | Ca > threshold, Pb < threshold | Powellite (if Mo) or Scheelite (if W) |
| 3rd: Fe³⁺ | Fe³⁺ > threshold, Pb+Ca < threshold, pH < 6 | Ferrimolybdite (Mo only) |

Note: This is an **approximate priority**. Real systems are simultaneous competitions, not sequential. The simulator should use supersaturation products (σ) for each mineral and let them compete stochastically.

---

## Cross-Zone Interactions

### Mo–W Interactions
The molybdate–tungstate sequence interacts with several other oxidation zones:

1. **Lead oxidation zone:** Wulfenite/stolzite/raspite share the Pb²⁺ pool with anglesite, cerussite, pyromorphite, mimetite, vanadinite. When PO₄³⁻ or AsO₄³⁻ or VO₄³⁻ are present, those minerals win the Pb competition. Wulfenite needs a Pb-rich, P/As/V-poor fluid.

2. **Iron oxidation zone:** Ferrimolybdite shares Fe³⁺ with goethite, jarosite, and scorodite. In strongly acidic oxidation zones, ferrimolybdite may form instead of goethite on molybdenite surfaces. As pH rises, goethite wins and ferrimolybdite dehydrates.

3. **Copper oxidation zone:** In porphyry Cu-Mo systems (Bingham Canyon, Butte), the copper and molybdenum oxidation zones overlap. Chalcopyrite oxidizes to chrysocolla/brochantite/antlerite while molybdenite oxidizes to wulfenite/ferrimolybdite. The fluids may interact: acidic Cu oxidation fluids (H₂SO₄ from chalcopyrite weathering) can accelerate molybdenite oxidation.

4. **Calcium silicate zone:** In skarns, scheelite forms alongside garnet, diopside, and wollastonite. If the skarn is later weathered, scheelite may partially dissolve and reprecipitate as powellite if Mo-bearing fluids arrive.

### Simulator Event: `event_molybdenum_tungsten_overlap`
Triggered when both Mo and W oxidation products are present in the same fluid. Effects:
- Mixed-crystal nucleation: "wulfenite-stolzite" (Pb + Mo + W), "scheelite-powellite" (Ca + Mo + W)
- Color blending: orange (W-rich wulfenite) → brown (W-rich stolzite) → yellow (Mo-rich powellite)
- Fluorescence shift: blue (scheelite) → white → yellow (powellite)

---

## Simulator Implementation Notes

### New Parameters
- `trace_WO4` — tungstate concentration in fluid (derived from wolframite/scheelite oxidation)
- `trace_MoO4` — molybdate concentration in fluid (derived from molybdenite oxidation)
- `mo_fraction` — in mixed crystals, 0.0 = pure W, 1.0 = pure Mo

### New Events
1. **`event_molybdenite_oxidation`** — Primary molybdenite begins oxidizing. Converts crystal-bound MoS₂ → fluid MoO₄²⁻. Produces H⁺ (acidifies fluid). Can be partial (rim) or complete.
2. **`event_wolframite_oxidation`** — Primary wolframite begins oxidizing. Releases WO₄²⁻ and precipitates Fe/Mn oxides locally.
3. **`event_dimorph_competition`** — When Pb + WO₄²⁻ are present, stolzite vs raspite nucleation probability check. Stolzite wins kinetically; raspite is thermodynamically favored but rarer.
4. **`event_molybdate_tungstate_overlap`** — Both Mo and W oxyanions present in same fluid. Enables solid-solution nucleation.
5. **`event_scheelite_powellite_conversion`** — If MoO₄²⁻ arrives at existing scheelite, crystal may develop Mo-rich zones (fluorescence shifts blue→yellow).

### Pseudocode: Nucleation Rules
```
# Primary precursors (deep, reducing)
IF temp > 350 AND Mo_available AND S_available AND Eh < 0 → nucleate molybdenite
IF temp > 300 AND W_available AND Eh < 0.2 → nucleate wolframite
IF temp > 200 AND Ca_available AND W_available → nucleate scheelite

# Secondary molybdates (oxidation zone)
IF temp < 80 AND Eh > 0.2:
    IF MoO4_available:
        IF Pb > threshold → nucleate wulfenite (competes with pyromorphite/mimetite for Pb)
        ELSE IF Ca > threshold AND Ca_not_consumed_by_fluorite → nucleate powellite
        ELSE IF Fe3 > threshold AND pH < 6 → nucleate ferrimolybdite
    
    IF WO4_available:
        IF Pb > threshold → nucleate stolzite (70%) OR raspite (30%)
        ELSE IF Ca > threshold → nucleate scheelite (secondary)
```

### Pseudocode: Growth Rules
```
# Wulfenite
IF temp < 80 AND Pb_available AND MoO4_available → grow at rate 2
Compete with pyromorphite/mimetite/vanadinite for Pb

# Stolzite
IF temp < 100 AND Pb_available AND WO4_available → grow at rate 2
Compete with wulfenite (if Mo present) and anglesite/cerussite for Pb

# Raspite (same formula as stolzite, different structure)
IF temp < 100 AND Pb_available AND WO4_available → grow at rate 1.5 (slower than stolzite)
IF temp > 395 → convert to stolzite (reconstructive phase transition)

# Powellite
IF temp < 200 AND Ca_available AND MoO4_available → grow at rate 3
Compete with fluorite/apatite for Ca
Fluorescence: yellow under SW UV

# Scheelite (secondary)
IF temp < 200 AND Ca_available AND WO4_available → grow at rate 3
Compete with powellite (if Mo present) and fluorite/apatite for Ca
Fluorescence: blue under SW UV

# Ferrimolybdite
IF temp < 60 AND Fe3_available AND MoO4_available AND Pb < threshold AND pH < 6 → grow at rate 4 (fast crust)
Forms radiating acicular aggregates
```

### Decomposition and Pseudomorph Mechanics
- **Molybdenite oxidation** → can leave "ghost" hexagonal outlines in limonite/goethite (pseudomorph after molybdenite)
- **Wolframite oxidation** → often preserves crystal shape in Fe/Mn oxide crusts
- **Wulfenite** → stable in oxidation zone; may partially dissolve if pH drops very low
- **Ferrimolybdite dehydration** → at >100°C loses water, becomes amorphous yellow-brown crust
- **Raspite → Stolzite conversion** → at >395°C, monoclinic raspite reconstructs to tetragonal stolzite. Preserves crystal shape but changes optical properties.

---

## Individual Flavor Texts

### Molybdenite
> Molybdenite is the mineral that confuses everyone who first meets it — soft as a fingernail, greasy as graphite, and six-sided like it was drawn by a crystallographer. But it's the gateway mineral for an entire paragenetic sequence. When oxygen finally reaches it, molybdenite doesn't just weather — it dissolves its identity into the groundwater, carrying molybdate ions upward to paint the oxidation zone in wulfenite's impossible orange. Every blade-thin hexagonal plate is a future sunset waiting to happen.

### Wolframite
> Wolframite carries tungsten out of the deep earth in silence. Dark, heavy, unremarkable to the untrained eye — it looks like a lump of dark ore. But within its monoclinic lattice is the metal that makes lightbulb filaments glow and rocket nozzles survive re-entry. When weathering finally cracks it open, the tungsten doesn't vanish; it recombines as scheelite's blue-glowing dipyramids or stolzite's dense brown crystals. Wolframite is the seed crystal of patience: it waits millions of years underground, then releases its treasure only when the surface finally reaches down.

### Wulfenite
> Wulfenite is what happens when two primary sulfides — galena and molybdenite — meet their end in the same oxidizing groundwater. The lead from one and the molybdenum from the other combine into paper-thin amber windows with a luster that rivals diamond. Red Cloud Mine crystals are collector holy grails: orange squares so vivid they look like someone pressed stained glass into rock. It's a mineral that demands two parents and won't compromise on aesthetics.

### Stolzite
> Stolzite is what happens when two heavy elements find each other in the wreckage of a broken vein — lead from oxidized galena, tungsten from weathered wolframite, both stripped of their primary partners and thrown together in the cold oxidizing zone. The result is a crystal of extraordinary density and brilliance, with refractive indices that rival diamond. Same formula as raspite, same elements in the same ratio, but stolzite chose tetragonal symmetry — the high-temperature form that, paradoxically, crystallizes in the cool supergene zone. It's the wulfenite of tungsten deposits: a thin, bright signal that the primary ore body below has been eating itself from the top down.

### Raspite
> Raspite is stolzite's less famous twin — identical chemistry, different structure, same story of lead and tungsten finding each other in oxidized rock. Where stolzite grows tetragonal and bold, raspite grows monoclinic and subtle, its tabular crystals flattened on perfect cleavage planes. At 395°C the two forms dance: raspite converts to stolzite, stolzite never converts back. In nature they often occur together at Broken Hill, raspite the rarer visitor, stolzite the persistent host. Both are messages from deep time, written in lead and tungsten, delivered by groundwater.

### Powellite
> Powellite is what molybdenite becomes when it meets the sky. Deep underground, molybdenite sits in its primary veins — soft, lead-gray, smelling of sulfur. But when erosion lifts those veins into the oxygen zone, the chemistry flips. MoS₂ becomes MoO₄²⁻, calcium steps in, and powellite crystallizes as thin yellow plates with adamantine fire. Under UV it answers scheelite's blue with its own bright yellow — same crystal structure, same lattice mechanism, different song. The two minerals are twins separated at birth: scheelite stays deep, powellite climbs toward the light.

### Scheelite
> Scheelite is the mineral that glows its own name. Under shortwave UV it ignites into impossible sky-blue — not from impurities, but from its own crystal lattice ringing like a struck bell. Those dipyramidal pseudo-octahedra, heavy as sin in the hand, form in the skarn zone where granite meets limestone and the earth's chemistry rewires itself. Every tungsten atom in your phone's vibration motor once passed through scheelite on its way out of the ground. The old prospectors knew: find the blue glow, find the tungsten. Sometimes find the gold too.

### Ferrimolybdite
> Ferrimolybdite is molybdenite's yellow warning sign — the canary-colored crust that tells you oxygen has arrived and the primary sulfides are dying. Where wulfenite is the glamorous result of Pb and Mo meeting in the oxidation zone, ferrimolybdite is what happens when there's no lead around: iron steps in instead, and you get fuzzy yellow needles instead of amber windows. It's the commoner's molybdate — less collected, less photographed, but geologically more common. Every yellow fuzz on a weathered molybdenite surface is a miniature ecosystem of element exchange.

---

## Game Variants by Species

### Wulfenite
- **Red Cloud:** Deep red-orange, ultra-thin tabular, Arizona — the collector's grail
- **Los Lamentos:** Thick tabular orange, large crystals, Mexico — robust and showy
- **Stolzite-Rimmed:** Wulfenite crystal overgrown by stolzite (or vice versa) where Mo-rich fluid was later replaced by W-rich fluid

### Stolzite
- **Broken Hill Classic:** Brown dipyramids with raspite inclusions, Australia — type locality
- **Pseudomorph After Raspite:** Originally raspite (monoclinic) converted to stolzite (tetragonal) by natural heating (>395°C event)
- **Wulfenite-Zoned:** Stolzite crystal with Mo-rich core (wulfenite component) and W-rich rim

### Raspite
- **Broken Hill Rarity:** Small tabular yellow crystals with stolzite, Australia — the rare dimorph
- **Heated Pseudomorph:** Stolzite that inverted back to raspite (not thermodynamically favored — rare)
- **Mo-Substituted:** Raspite with partial Mo substitution ("wulfenite-raspite")

### Scheelite
- **Classic Skarn:** White dipyramids in garnet-diopside matrix — the textbook form
- **Xuebaoding Gold:** Golden-yellow gem crystals on cassiterite, China — world-class aesthetic
- **Powellite-Zoned:** Blue core (W-rich) with yellow rim (Mo-rich) — the solid-solution gradient

### Powellite
- **Indian Zeolite Association:** Bright yellow plates on apophyllite/stilbite, Deccan Traps — the unexpected context
- **Porphyry Crust:** Yellow powdery coatings on oxidized molybdenite, Climax-type deposits
- **Scheelite-Core:** Yellow rim on blue scheelite core — reversed zonation from late Mo arrival

### Ferrimolybdite
- **Climax Crust:** Canary-yellow fuzzy needles on molybdenite, Colorado — classic porphyry
- **Mine Tailings:** Powdery yellow coatings on waste rock — the modern, human-accelerated form
- **Dehydrated:** Brown, dull, amorphous — the ghost of ferrimolybdite after losing its water

---

## Famous Localities for the Sequence

### Red Cloud Mine, Arizona, USA
- Wulfenite type locality for deep orange, thin-tabular crystals
- Arizona state mineral (2017)
- Associated with vanadinite, cerussite, descloizite
- The single most famous wulfenite locality on Earth

### Climax Mine, Colorado, USA
- World's largest molybdenum producer
- Primary molybdenite + secondary ferrimolybdite, powellite
- Porphyry Mo deposit — textbook example of the full sequence
- Also produces wulfenite where Pb-bearing fluids overlap

### Broken Hill, New South Wales, Australia
- Type locality for both stolzite AND raspite
- Both dimorphs occur together — unique worldwide
- Associated with galena, cerussite, anglesite, pyromorphite
- The dimorph competition made visible

### Peacock Mine, Idaho, USA
- Type locality for powellite (CaMoO₄)
- Secondary molybdate in oxidized porphyry system
- Associated with molybdenite, ferrimolybdite

### Xuebaoding, Sichuan, China
- Gem-quality scheelite on cassiterite
- Golden dipyramids to 5 cm — among the world's best
- Associated with beryl, muscovite, fluorite

### Mount Peca, Slovenia
- Stolzite crystals on postage stamp (1997)
- Well-developed dipyramids
- Historic European tungsten deposit

---

## Simulator Cross-References

- **Lead oxidation zone sequence:** `memory/research-lead-oxidation-zone.md` — shares Pb²⁺ pool, anglesite/cerussite/pyromorphite competition
- **Iron oxidation zone sequence:** `memory/research-iron-oxidation-zone.md` — shares Fe³⁺ pool, goethite/jarosite competition
- **Copper oxidation zone sequence:** `memory/research-copper-oxidation-zone.md` — overlaps in porphyry Cu-Mo systems
- **Calcium silicate sequence:** `memory/research-pectolite.md`, `memory/research-wollastonite.md`, `memory/research-prehnite.md` — shares Ca²⁺ in skarn environments
- **Individual species files:** See linked files at top of document

---

## Summary

The molybdate–tungstate paragenetic sequence is a story of **rare metals finding each other twice** — first deep in the earth as sulfides and oxides, then again near the surface as oxyanions in oxidizing groundwater. Molybdenite and wolframite are the parents; wulfenite, stolzite, raspite, scheelite, powellite, and ferrimolybdite are the children. Each child inherits the heavy metal from one parent and a partner cation (Pb, Ca, or Fe) from the local chemistry. The sequence demands oxidation — without oxygen penetrating the primary vein, nothing happens. But when it does, the results are among the most visually striking secondary minerals in existence: orange wulfenite windows, blue-glowing scheelite dipyramids, dense brown stolzite crystals, and fuzzy yellow ferrimolybdite crusts. Every one of them is a message from deep time, written in elements that weigh more than lead and glow under invisible light.
