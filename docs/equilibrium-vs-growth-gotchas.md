# Equilibrium vs Growth — Known Gotchas for Mineral Rendering

*When ab-initio surface energies mislead the kernel about what real crystals look like.*

---

## The Core Problem

Ab-initio surface energy calculations are **equilibrium values at 0 K**. They tell you what a crystal face *wants* to be when everything has settled. But most minerals in collections are **growth forms** — they record the kinetic conditions of crystallization, not the thermodynamic minimum.

In crystal growth, **slow faces dominate morphology** because fast faces grow themselves out of existence. This is BFDH (Bravais-Friedel-Donnay-Harker) theory in practice. A face with low surface energy may be stable, but if it grows *fast*, it'll disappear from the external morphology. Conversely, a face with higher surface energy can dominate if its growth velocity is slow.

The builder's kernel `R_i` values are **growth velocities**, not surface energies. Mapping ab-initio to `R_i` requires care — the sign of the correlation flips depending on whether you're modeling equilibrium habit or growth habit.

---

## High-Risk Minerals (Equilibrium Misleading)

### 1. Barite — BaSO₄
**The trap:** Ab-initio may suggest {210} prism is low-energy. In growth, {210} can become co-dominant → equant/blocky instead of tabular.

**Real morphology:** Tabular {001} pinacoid dominant. Thin plates, sometimes so thin they're "book"-like. The {001} face grows slowest, so it survives while {011} domes and {210} prisms grow away.

**Builder fix:** Keep {001} clearly slowest (R ≈ 1.0). {210} should be prominent but not co-dominant (R ≈ 1.6–1.7). {011} should be minor fast dome (R ≈ 2.0+). Target: 10-plane tabular rectangular plate.

**Temperature dependence:** At low T (cold seeps, ~2°C), barite is ultra-thin tabular. At high T (hydrothermal, 200°C+), thicker, more equant. The kernel's current parameters should target room-T growth (~20°C).

### 2. Calcite — CaCO₃
**The trap:** {104} rhombohedron is the equilibrium form. But {21̄1} scalenohedron (dogtooth) and {101̄0} prismatic forms are common growth habits that ab-initio may miss entirely.

**Real morphology:** Context-dependent. Same vug can produce:
- **Nailhead** (flat {101̄0} prism + steep {0001} pinacoid): high Ca/CO₃ ratio, higher T
- **Dogtooth** (steep scalenohedral): low Ca/CO₃, lower T, higher supersaturation
- **Rhombohedral** (simple {104}): moderate conditions

**Builder implications:** Calcite needs **multiple kernel profiles** or habit switching based on saturation state and pH. A single `R_i` set cannot capture calcite's morphological range.

**Key research:** [Calcite habit variation study](memory/2026-05-04-research.md) — Ca/CO₃ ratio and supersaturation drive {104} vs {21̄1} competition. Temperature: higher T → simpler (rhombohedral), lower T → complex (scalenohedral).

### 3. Aragonite — CaCO₃ (orthorhombic)
**The trap:** Aragonite is the high-pressure polymorph of CaCO₃. At ambient conditions, calcite is the stable phase. Aragonite *shouldn't* form at room T — but it does, abundantly, because kinetics beat thermodynamics.

**Real formation:** Organic mediation (nacre in shells), high Mg/Ca ratios, high supersaturation, or low T (<~60°C in biological systems). The equilibrium phase diagram says calcite; the growth conditions say aragonite.

**Builder implications:** If the Vugg sim models CaCO₃ precipitation, the aragonite→calcite transition needs kinetic trapping, not just thermodynamics. Mg²⁺ inhibition of calcite nucleation is the key — high Mg/Ca → aragonite even where calcite "should" win.

### 4. Quartz — SiO₂
**The trap:** The α-quartz → β-quartz transition at 573°C is well-known. But quartz growth morphology (prismatic vs tabular vs skeletal) depends heavily on supersaturation and trace impurities (Al, Li, Na, K, Ge).

**Real morphology:**
- **Low supersaturation:** Prismatic, well-formed
- **High supersaturation:** Skeletal, hopper, or scepter forms
- **High Al + alkali:** Japanese law twins, tabular habits
- **Faden quartz:** Externally driven growth in rotating fractures (not screw dislocations — see TN380)

**Builder implications:** The kernel may need impurity-dependent habit modifiers. Pure SiO₂ gives prismatic quartz; trace Al opens twinning and tabular modes.

### 5. Pyrite — FeS₂
**The trap:** Pyrite forms cubes ({100}) and pyritohedra ({210}) with equal ease. Ab-initio may favor one. Natural pyrite shows both, often in the same specimen (zoned).

**Real morphology:** Cube-dominant in low-sulfur, near-neutral pH. Pyritohedron-dominant in high-sulfur, acidic conditions. The transition is sharp and observable.

**Builder implications:** pH-dependent habit switching for pyrite. Not a single kernel — two kernels selected by `pH < threshold`.

### 6. Gypsum / Selenite — CaSO₄·2H₂O
**The trap:** Gypsum's {010} perfect cleavage and tabular habit are so dominant that other forms (prismatic, acicular, granular) get missed.

**Real morphology:**
- **Selenite:** Transparent tabular {010}, often with fishtail twins
- **Satin spar:** Fibrous, acicular — same mineral, completely different appearance
- **Desert rose:** Sand-included rosettes — growth in arid, saline conditions

**Builder implications:** Desert rose formation requires foreign particle inclusion during growth — a separate nucleation pathway not captured by standard surface energy models.

---

## Medium-Risk Minerals (Context-Dependent)

### 7. Sphalerite — ZnS
**The trap:** Sphalerite (cubic) and wurtzite (hexagonal) are polymorphs. The cubic→hexagonal transition is ~1020°C, but metastable wurtzite forms at low T via kinetic trapping.

**Real morphology:** Sphalerite: tetrahedral {111}, dodecahedral {110}. Wurtzite: pyramidal {10̄11}, prismatic {11̄20}.

**Builder implications:** If the sim has both species, the kernel needs to handle their distinct morphologies. The `broth-ratio-sphalerite-wurtzite.md` file covers the competition.

### 8. Apophyllite — KCa₄Si₈O₂₀(F,OH)·8H₂O
**The trap:** Apophyllite's tetragonal prismatic habit is reliable, but the **optical effects** (iridescence, birefringence, CRT scan-lines from hematite inclusions × growth bands) are entirely growth-dependent.

**Real morphology:** See [TN498 research](minerals/apophyllite-tn498.md). The hematite inclusion market variety "Bloody/Cinnamon Apophyllite" only forms when Stage III hydrothermal fluids (21–58 Ma post-eruption) carry hematite dust through already-grown apophyllite cavities.

**Builder implications:** Inclusion patterns are post-growth events, not primary morphology. The kernel should separate "crystal shape" from "decoration."

---

## General Principles for Builder

1. **When in doubt, trust growth over equilibrium.** Ab-initio is a starting point. Natural history museums are the ground truth.

2. **Temperature matters more than the kernel currently models.** Many minerals have 2–3 distinct habit regimes across their stability range. Consider temperature-dependent `R_i` sets or habit-switching logic.

3. **Impurities are not decoration — they're morphological switches.** Al in quartz, Cr in wulfenite, Mg in calcite/aragonite. Trace elements change habit, not just color.

4. **Supersaturation is the hidden variable.** Two identical chemistries at different saturation states produce different crystals. The kernel's growth rate parameter should couple to supersaturation, not just temperature.

5. **Post-growth events are real.** Dissolution, replacement, overgrowth, exsolution, radiation damage. The crystal you see is rarely the crystal that grew.

---

## Files in This Repo That Help

- `minerals/barite.md` — formation conditions, habit notes
- `minerals/calcite.md` — habit variation context
- `minerals/quartz.md` — trace impurity effects
- `minerals/pyrite.md` — pH-dependent morphology
- `minerals/apophyllite-tn498.md` — post-growth optical effects
- `minerals/broth-ratio-*.md` — competitive growth systems

---

*Compiled by 🪨✍️ (StonePhilosopher) for the Vugg Simulator builder. Last updated 2026-07-01.*
