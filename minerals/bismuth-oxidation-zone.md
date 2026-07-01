# Research: Bismuth Oxidation Zone Paragenetic Sequence — Vugg Simulator

**Date:** 2026-06-12
**Scope:** Unified paragenetic master file covering the full bismuth sequence from primary sulfide through native metal to oxidation-zone products. Individual species files exist for bismuthinite, native bismuth, and clinobisvanite. This file adds bismite and bismutite, and models the full Eh-S-pH-CO₂ control system.

**Linked Files:**
- `memory/research-bismuthinite.md` — primary sulfide
- `memory/research-native-bismuth.md` — native element
- `memory/research-clinobisvanite.md` — oxidation zone vanadate
- `memory/research-bismite.md` — oxidation zone oxide (this file)
- `memory/research-bismutite.md` — oxidation zone carbonate (this file)

---

## Species: Bismite

### Identity
- **Formula:** Bi₂O₃
- **Crystal system:** Monoclinic (pseudo-orthorhombic in massive forms)
- **Mineral group:** Oxide
- **Hardness (Mohs):** 4–5
- **Specific gravity:** 8.5–9.5 (extremely dense for a nonmetallic mineral)
- **Cleavage:** None in massive forms; perfect {001} in rare crystals
- **Fracture:** Uneven to subconchoidal
- **Luster:** Adamantine to earthy (dull in massive/altered material)

### Color & Appearance
- **Typical color:** Yellow to greenish-yellow, grey-green, or green-grey; massive forms often clay-like and dull
- **Color causes:** Bi³⁺ in octahedral coordination; charge transfer between Bi and O gives the yellow-green hue
- **Transparency:** Translucent in thin grains; opaque in massive aggregates
- **Streak:** Grey to black (unusual for a yellow mineral — diagnostic)
- **Notable visual features:** Massive and clay-like with no visible crystals; resembles earthy limonite but far heavier

### Crystal Habits
- **Primary habit:** Massive, clay-like, earthy aggregates; no macroscopic crystals in natural specimens
- **Common forms/faces:** None — massive only
- **Twin laws:** None observed
- **Varieties:** Massive/earthy (default); rare crystalline forms are laboratory products
- **Special morphologies:** Crusts and powdery coatings on oxidized bismuthinite; replacement pseudomorphs after native bismuth

### Formation Conditions

#### Temperature
- **Nucleation temperature range:** <80°C (supergene/oxidation zone)
- **Optimal growth temperature:** 20–50°C (ambient surface conditions)
- **Decomposition temperature:** Melts at ~817°C; stable up to that point
- **Temperature-dependent habits:** None — always massive in nature

#### Chemistry Required
- **Required elements:** Bi³⁺ (from oxidation of bismuthinite or native bismuth), O₂
- **Optional/enhancing elements:** None significant
- **Inhibiting elements:** High CO₂ (favors bismutite instead), high V⁵⁺ (favors clinobisvanite), reducing agents
- **Required pH range:** Neutral to slightly acidic (5–7)
- **Required Eh range:** Strongly oxidizing (>+0.4V)
- **Required O₂ range:** High — requires atmospheric oxygen access

#### Secondary Chemistry Release
- **Byproducts of nucleation:** Consumes Bi³⁺ from solution; releases no significant byproducts
- **Byproducts of dissolution:** Releases Bi³⁺ back to fluid; can reprecipitate as bismutite if CO₂ is present

#### Growth Characteristics
- **Relative growth rate:** Very slow (supergene alteration product, not primary crystallization)
- **Maximum crystal size:** No natural crystals; massive aggregates to several cm as coatings
- **Typical crystal size in vugs:** 0.1–5 mm as powdery crusts
- **Does growth rate change with temperature?** Not applicable — forms at ambient conditions
- **Competes with:** Bismutite (if CO₂ available), clinobisvanite (if V available), bismoclite (if Cl available)

#### Stability
- **Breaks down in heat?** Melts at ~817°C
- **Breaks down in light?** No
- **Dissolves in water?** Very low solubility
- **Dissolves in acid?** Soluble in strong acids (HCl, HNO₃) and hot concentrated alkali
- **Oxidizes?** Already fully oxidized (Bi³⁺)
- **Radiation sensitivity:** None known

### Paragenesis
- **Forms AFTER:** Bismuthinite (Bi₂S₃ → oxidation → Bi³⁺), native bismuth (Bi⁰ → oxidation → Bi³⁺)
- **Forms BEFORE:** Bismutite (if CO₂ later infiltrates), clinobisvanite (if V is present)
- **Commonly associated minerals:** Bismuthinite, native bismuth, bismutite, bismoclite, arsenopyrite, pyrite, quartz
- **Zone:** Supergene/oxidation zone
- **Geological environment:** Oxidized portions of Bi-bearing hydrothermal veins, gossans, arid-climate oxidation zones

### Famous Localities
- **Classic locality 1:** Goldfield, Nevada, USA — type locality (1868), with bismuthinite
- **Classic locality 2:** Schneeberg District, Ore Mountains, Saxony, Germany — historic Bi-Ag-Co mining district
- **Classic locality 3:** Schlaggenwald (Horní Slavkov), Czech Republic — with bismuthinite and bismutite
- **Notable specimens:** None for display — bismite is a micromount/crust material, not a collector's mineral

### Fluorescence
- **Fluorescent under UV?** No documented fluorescence
- **SW color:** —
- **MW color:** —
- **LW color:** —
- **Activator:** None
- **Quenched by:** N/A

### Flavor Text

> Bismite is what happens when bismuth meets air and nothing else. No sulfur left to make bismuthinite, no vanadium to make clinobisvanite, no carbonate to make bismutite — just bismuth and oxygen, forming a yellow-green powder that weighs nearly twice what it looks like it should. Specific gravity 9.5 for something that resembles dried clay. It's the simplest end of the bismuth oxidation chain: Bi₂S₃ loses its sulfur, Bi⁰ loses its electrons, and both become Bi₂O₃ — the oxide so basic it doesn't even bother with crystals. In the simulator, bismite appearing on your bismuthinite means the oxidation zone has stripped away everything but the element itself. It's not pretty. It's geological honesty.

### Simulator Implementation Notes
- **New parameters needed:** None (trace_Bi, O₂ already in system)
- **New events needed:** `event_bismuth_oxidation` — when Eh rises and bismuthinite/native Bi are present
- **Nucleation rule pseudocode:**
```
IF temp < 80 AND Eh > 0.4 AND trace_Bi > 5 AND CO2 < 10 AND V < 5 AND no reducing agents
  → nucleate bismite (crust/powdery habit)
Priority: bismutite > clinobisvanite > bismite (Bi³⁺ prefers anions if available)
```
- **Growth rule pseudocode:**
```
IF σ_bismite > 0.5 AND temp < 80 AND Eh > 0.4 → grow at rate 1 (very slow, crust-forming)
Habit: always massive/powdery (no crystalline variant in nature)
```
- **Habit selection logic:** Always powdery/crust in simulator — no natural crystals exist.
- **Decomposition products:** Melts at 817°C → Bi₂O₃ liquid. Dissolves in acid → Bi³⁺ in solution.

### Variants for Game
- **Variant 1:** Goldfield Crust — type locality, yellow-green powdery coating on quartz
- **Variant 2:** Schneeberg Earth — grey-green massive variety from the Ore Mountains
- **Variant 3:** Pseudomorph after native bismuth — retains arborescent outline but converted to yellow oxide

---

## Species: Bismutite

### Identity
- **Formula:** Bi₂(CO₃)O₂ (or (BiO)₂CO₃ — bismuth subcarbonate)
- **Crystal system:** Orthorhombic
- **Mineral group:** Carbonate
- **Hardness (Mohs):** 2.5–3.5
- **Specific gravity:** 6.7–7.4 measured (8.15 calculated)
- **Cleavage:** Distinct/Good on {001} (microscopically observable)
- **Fracture:** Uneven
- **Luster:** Vitreous, waxy, may be dull to earthy

### Color & Appearance
- **Typical color:** Yellow to brown, greenish, green-grey, grey, or black
- **Color causes:** Bi³⁺ in layered structure; organic staining or iron inclusions darken color
- **Transparency:** Opaque to transparent in small grains
- **Streak:** Grey
- **Notable visual features:** Radially fibrous to spheroidal aggregates; pseudo-merohedral twinning simulates tetragonal symmetry under microscope

### Crystal Habits
- **Primary habit:** Radially fibrous to spheroidal aggregates; crusts and earthy to dense massive forms
- **Common forms/faces:** Very rare platy crystals; typically fibrous-radiating masses
- **Twin laws:** Pseudo-merohedral twinning (simulates tetragonal symmetry)
- **Varieties:** Beyerite (Ca₂Bi₂O₂(CO₃)₄) — Ca-bearing variety
- **Special morphologies:** Botryoidal crusts, powdery aggregates, replacement pseudomorphs after bismuthinite

### Formation Conditions

#### Temperature
- **Nucleation temperature range:** <80°C (supergene/oxidation zone)
- **Optimal growth temperature:** 20–50°C (ambient surface conditions)
- **Decomposition temperature:** Loses CO₂ at ~300–400°C; converts to bismite
- **Temperature-dependent habits:** None in natural range

#### Chemistry Required
- **Required elements:** Bi³⁺ (from oxidation of primary bismuth minerals), CO₃²⁻
- **Optional/enhancing elements:** Ca (forms beyerite variety)
- **Inhibiting elements:** High V⁵⁺ (favors clinobisvanite), very low CO₂ (favors bismite instead)
- **Required pH range:** Slightly acidic to neutral (5–7); alkaline pH favors carbonate precipitation
- **Required Eh range:** Oxidizing (>+0.3V) — must have Bi³⁺ available
- **Required O₂ range:** Moderate to high

#### Secondary Chemistry Release
- **Byproducts of nucleation:** Removes Bi³⁺ and CO₃²⁻ from solution
- **Byproducts of dissolution:** Releases Bi³⁺ and CO₂; can reprecipitate as bismite if heated

#### Growth Characteristics
- **Relative growth rate:** Very slow (supergene secondary mineral)
- **Maximum crystal size:** Microscopic platy crystals to 0.1 mm; aggregates to several cm
- **Typical crystal size in vugs:** 0.01–0.5 mm in fibrous crusts
- **Does growth rate change with temperature?** Not significantly in natural range
- **Competes with:** Bismite (when CO₂ is absent), clinobisvanite (when V is present), bismoclite (when Cl is present)

#### Stability
- **Breaks down in heat?** Yes — loses CO₂ at ~300–400°C, converts to bismite
- **Breaks down in light?** No
- **Dissolves in water?** Very low solubility
- **Dissolves in acid?** Soluble in acids with CO₂ release (effervesces)
- **Oxidizes?** Already fully oxidized (Bi³⁺)
- **Radiation sensitivity:** None known

### Paragenesis
- **Forms AFTER:** Bismuthinite (oxidized → Bi³⁺ + CO₃²⁻), native bismuth (oxidized → Bi³⁺ + CO₃²⁻), bismite (can convert if CO₂ infiltrates)
- **Forms BEFORE:** Nothing definitive — it's a stable supergene end product unless V or Ca alter the pathway
- **Commonly associated minerals:** Bismuthinite, native bismuth, bismite, arsenopyrite, quartz, calcite (as CO₂ source)
- **Zone:** Supergene/oxidation zone
- **Geological environment:** Oxidized portions of Bi-bearing hydrothermal veins and pegmatites; carbonate-bearing gossans

### Famous Localities
- **Classic locality 1:** Schneeberg, Ore Mountains, Saxony, Germany — type locality area, with bismuthinite and native bismuth
- **Classic locality 2:** Saxony broadly — the original "bismuthite" localities (note: "bismuthite" was once used for bismuthinite, causing historical confusion)
- **Classic locality 3:** Schlaggenwald (Horní Slavkov), Czech Republic — with bismuthinite in greisen
- **Notable specimens:** Fibrous-radiating aggregates from German localities; beyerite variety from rare Ca-rich environments

### Fluorescence
- **Fluorescent under UV?** No documented fluorescence
- **SW color:** —
- **MW color:** —
- **LW color:** —
- **Activator:** None
- **Quenched by:** N/A

### Flavor Text

> Bismutite is bismite that found some carbon dioxide. Same oxidation zone, same Bi³⁺ source, but here there's calcite nearby dissolving in groundwater, or soil CO₂ percolating down through fractures. The result is Bi₂(CO₃)O₂ — a carbonate that isn't really a carbonate in the calcite sense. It's a layered mineral: Bi–O sheets alternating with CO₃ sheets, like a geological mille-feuille. The crystals are too small to see without a microscope, but the aggregates are unmistakable: yellow-brown fibrous balls radiating from a center, sometimes coating the inside of a vug like velvet. It's soft (hardness 2.5), heavy, and entirely a surface-world mineral — the deepest it ever forms is the bottom of the oxidation zone, where descending carbonate-rich water meets ascending bismuth. In the simulator, bismutite means your bismuth deposit has been oxidized AND carbonated. Two different fluids had to meet. That's the story it tells.

### Simulator Implementation Notes
- **New parameters needed:** CO₃ already tracked (for carbonates); no new parameters
- **New events needed:** `event_bismuth_carbonation` — when oxidized Bi³⁺ meets CO₂-rich fluid
- **Nucleation rule pseudocode:**
```
IF temp < 80 AND Eh > 0.3 AND trace_Bi > 5 AND CO3 > 10 AND V < 5
  → nucleate bismutite (fibrous/crust habit)
Priority: bismutite > bismite (when CO3 present); clinobisvanite > bismutite (when V present)
```
- **Growth rule pseudocode:**
```
IF σ_bismutite > 0.5 AND temp < 80 AND Eh > 0.3 AND CO3 > 10 → grow at rate 1 (very slow)
```
- **Habit selection logic:** Always fibrous-radiating or crust in simulator (natural habit).
- **Decomposition products:** Heating to 300–400°C → loses CO₂ → converts to bismite (Bi₂O₃). Acid dissolution → Bi³⁺ + CO₂ gas.

### Variants for Game
- **Variant 1:** Saxony Fibrous — classic radiating fibrous aggregates, yellow-brown
- **Variant 2:** Beyerite — Ca-bearing variety, cream to white, requires Ca in fluid
- **Variant 3:** Pseudomorph after bismuthinite — retains needle-like outline but converted to fibrous carbonate aggregate

---

## Unified Paragenetic Sequence: The Bismuth Oxidation Zone

### Complete Reaction Chain

```
PRIMARY ZONE (reducing, high T >200°C):
  Bismuthinite (Bi₂S₃) — when S²⁻ is available
    ↓ sulfur depletion + Bi remains
  Native Bismuth (Bi⁰) — when S²⁻ is depleted but Bi remains
    ↓ temperature drops below 271.5°C
  [Bi is now solid metal, not liquid]

OXIDATION ZONE (oxidizing, low T <80°C):
  Bismuthinite → oxidation → Bi³⁺ + SO₄²⁻ + H⁺
  Native Bismuth → oxidation → Bi³⁺ + e⁻
    ↓ Bi³⁺ meets available anions
  Bismite (Bi₂O₃) — simplest: only O²⁻ available
  Bismutite (Bi₂(CO₃)O₂) — when CO₃²⁻ is present
  Clinobisvanite (BiVO₄) — when V⁵⁺ is present
  Bismoclite (BiOCl) — when Cl⁻ is present (not yet in simulator)
```

### Control Variables

| Stage | Controlling Variable | Threshold | Mineral Result |
|-------|---------------------|-----------|----------------|
| Primary | S²⁻ availability | >50 ppm → Bi₂S₃; <10 ppm → Bi⁰ | bismuthinite vs native bismuth |
| Temperature | T vs 271.5°C | >271.5°C → liquid Bi; <271.5°C → solid native Bi | native bismuth crystallizes |
| Oxidation | Eh | >+0.3V → oxidation starts | all supergene products |
| Anion competition | CO₃, V, O, Cl | CO₃ > V > O > Cl (rough priority) | bismutite > clinobisvanite > bismite > bismoclite |

### Simulator Events

1. **`event_bismuth_sulfur_depletion`** — When fluid S²⁻ drops below threshold while Bi remains high: native bismuth nucleates, bismuthinite stops growing.

2. **`event_bismuth_oxidation`** — When Eh rises in presence of Bi-bearing primary minerals: triggers oxidation cascade, releasing Bi³⁺ to fluid.

3. **`event_bismuth_carbonation`** — When oxidized Bi³⁺ meets CO₂-rich fluid: bismutite nucleates (if CO₃ > V).

4. **`event_bismuth_vanadation`** — When oxidized Bi³⁺ meets V⁵⁺-rich fluid: clinobisvanite nucleates (priority over bismutite/bismite if V is abundant).

### Cross-Zone Interactions

- **With copper oxidation zone:** Bismuth and copper can coexist in primary veins (e.g., Wittichen, Germany — Cu-Bi sulfosalts). Oxidation zone produces separate Bi and Cu products that may intermix.
- **With lead oxidation zone:** Aikinite (PbCuBiS₃) connects the Pb and Bi systems in primary zone. No direct oxidation zone linkage.
- **With iron oxidation zone:** Pyrite oxidation generates acid (H⁺), which accelerates bismuthinite dissolution and Bi³⁺ release.
- **With arsenic:** Arsenopyrite (FeAsS) common in Bi-bearing veins; As doesn't directly affect Bi oxidation products but shares the oxidation zone.

### Pseudomorph Mechanics

- **Bismuthinite → bismutite/bismite:** Oxidation pseudomorph — retains needle-like outline but mineral is now carbonate/oxide. Common in Schneeberg/Saxony specimens.
- **Native bismuth → bismite:** Oxidation pseudomorph — arborescent metal becomes yellow oxide crust, sometimes retaining the tree-like outline.
- **Bismutite → bismite:** Thermal pseudomorph — heating drives off CO₂, leaving bismite. Simulates post-depositional thermal events or wildfires.

### Builder Notes

- **No new trace elements needed:** Bi, S, O₂, CO₃, V all already tracked.
- **Nucleation priority:** In oxidation zone, Bi³⁺ prefers: clinobisvanite (if V>5) > bismutite (if CO₃>10) > bismite (default).
- **Morphology:** All oxidation-zone Bi minerals are powdery/crust/fibrous in simulator — no crystalline variants, matching natural occurrence.
- **Thermal decomposition:** Bismutite → bismite at 300–400°C (already in thermal decomposition system). Bismite melts at 817°C (add to system).
- **Wittichen scenario connection:** The v189 Wittichen five-element vein already includes native bismuth as dendritic rosettes. This paragenetic file provides the oxidation-zone backstory for what happens to that bismuth when the vein weathers.

---

*The bismuth story is one of sulfur control in the deep, and anion competition at the surface. First it finds sulfur and becomes a sulfide. Then the sulfur runs out and it becomes metal. Then air finds it, and it becomes oxide, or carbonate, or vanadate — depending on what else was in the groundwater. The mineral remembers all three chapters.*
