# Research: Initiative Variable in Mineral Paragenesis — A Geochemical Grounding

**Date:** 2026-05-21
**Triggered by:** Professor's intuition that initiative should have conditional modifiers (temperature sweet-spots, edge-of-gate penalties)
**Sources:** Web search on nucleation kinetics, crystal growth theory, thermodynamics of dissolution

---

## What the Literature Says

### Nucleation Rate Depends on Supersaturation AND Temperature

The nucleation rate J (nuclei per unit volume per unit time) follows an Arrhenius-like form:

**J = A · exp(-ΔG* / kT)**

where ΔG* is the **activation barrier for nucleation** — the Gibbs free energy required to form a stable critical nucleus.

This means:
- **Higher temperature → lower barrier → faster nucleation** (generally)
- **Higher supersaturation → lower barrier → faster nucleation**
- But both terms interact: the barrier ΔG* itself depends on temperature through surface energy and solubility

### The Critical Supersaturation Concept

For any mineral at a given temperature, there's a **critical supersaturation σ_crit** below which nucleation is effectively zero (induction time → ∞) and above which nucleation becomes rapid. This isn't a smooth gradient — it's a threshold.

From the literature: *"The induction time for nucleation is a strong function of supersaturation"* — and near the threshold, small changes in σ produce enormous changes in nucleation rate.

This maps directly to your "edge of nucleation" intuition. A mineral sitting at σ = 0.95·σ_crit is **fragile** — any perturbation (temperature shift, solute competition, pH drift) can push it across the threshold. A mineral at σ = 2·σ_crit is **robust** — it has buffer.

### Temperature as a Conditional Modifier

Solubility products (Ksp) are temperature-dependent via:

**ln(Ksp) = -ΔG° / RT**

- **Calcite**: inverse solubility (more soluble at lower T) — the rare exception
- **Quartz**: normal solubility (more soluble at higher T) — the rule
- **Most sulfates/sulfides**: strong temperature dependence

This means temperature affects initiative in **two ways**:
1. Direct kinetic effect: higher T → lower activation barrier → higher J
2. Indirect thermodynamic effect: higher T → changes Ksp → changes σ → changes J

For calcite specifically: higher T → lower solubility → higher σ → **higher initiative at higher T** (the "hot spring travertine" effect)

For quartz: higher T → higher solubility → lower σ → but also lower viscosity → faster diffusion → the kinetic boost may outweigh the thermodynamic penalty

### Surface Energy and the Nucleation Barrier

ΔG* = (16πγ³V_m²) / (3(RT ln S)²)

where γ = surface energy, V_m = molar volume, S = supersaturation ratio.

Key insight: **surface energy γ is mineral-specific**. Minerals with lower surface energy have lower nucleation barriers → higher base initiative. This is why:
- **Opal** (amorphous SiO₂, low γ) precipitates before quartz from the same fluid
- **Gypsum** precipitates before anhydrite
- **Aragonite** vs calcite competition depends on Mg²⁺ (poisons calcite surface, lowers aragonite's effective γ)

### BCF Theory: Growth Rate, Not Just Nucleation

Burton-Cabrera-Frank theory gives growth rate as:

**v = C · σ · tanh(λ_s / 2x_s)**

where λ_s = step spacing, x_s = diffusion length on surface.

At **low σ**: v ∝ σ² (surface diffusion limited — spiral growth from dislocations)
At **high σ**: v ∝ σ (direct integration — abundant kink sites)

This means initiative has **regime dependence**: a mineral's growth rate changes its scaling with supersaturation depending on which regime it's in. A mineral that dominates at low σ might lose to a faster-growing competitor at high σ.

---

## Mapping to the Vugg Simulator

### Current State
The sim uses a **fixed-order mineral loop** each step. Every mineral gets a turn. Supersaturation σ is calculated from fluid composition. If σ > threshold, the mineral nucleates/grows.

This is like **simultaneous initiative** — everyone acts, but the ones with higher σ get more growth.

### What Initiative Variable Would Add

An initiative roll would:
1. Calculate each mineral's **base initiative** from σ (higher σ = higher initiative)
2. Apply **conditional modifiers**:
   - Temperature sweet-spot: minerals have preferred T windows
   - Edge-of-gate penalty: minerals near their σ_crit get -initiative (fragile)
   - Surface energy bonus: low-γ minerals (opal, gypsum) get +initiative
   - Competition penalty: shared cations reduce effective initiative
3. Sort minerals by modified initiative
4. Process growth in that order
5. After each mineral grows, debit fluid → recalculate σ for remaining minerals

This would produce **emergent paragenesis**: the mineral that goes first changes the fluid for everyone else, which changes who goes next.

### The Professor's Conditional Modifier Intuition

Your instinct about temperature sweet-spots and edge-of-gate penalties is **directly supported by the geochemistry**:

**Temperature sweet-spot:**
- Each mineral has an optimal T where its Ksp and kinetic barrier align
- Calcite: higher T = higher initiative (inverse solubility)
- Barite: moderate T = higher initiative (sulfate stability window)
- Sphalerite: moderate-high T = higher initiative (sulfide stability)
- Opal: low T = higher initiative (amorphous SiO₂ precipitates cold)

**Edge-of-gate penalty:**
- Minerals with σ within 10% of σ_crit get -2 initiative (fragile)
- Minerals with σ > 2·σ_crit get +1 initiative (robust)
- This explains the v125 cascade findings: adding stoichiometry shifted σ for edge-of-gate minerals, flipping their initiative order

**Shared-cation competition:**
- When two minerals want the same cation, both get -1 initiative
- When three+ minerals want the same cation, all get -2 initiative
- This would make dense suites (supergene_oxidation, schneeberg) inherently more chaotic

---

## Open Questions

1. **Should initiative be per-nucleation-event or per-step?**
   - Per-nucleation: each new crystal rolls independently (more chaotic, realistic for natural systems)
   - Per-step: each mineral gets one initiative roll per step (more deterministic, easier to test)

2. **How does substrate epitaxy affect initiative?**
   - If mineral B nucleates on mineral A, does A lose initiative (competition for solutes) or gain it (surface catalysis lowers B's barrier)?
   - The literature suggests both happen: competition dominates at low σ, catalysis at high σ

3. **Should initiative include a random component?**
   - Pure deterministic: same input → same output every time (current sim behavior)
   - Small random: ±1 initiative (captures nucleation stochasticity — "nucleation is probabilistic")
   - Large random: full dice roll (captures natural variability but harder to test)

4. **Can we measure real-world nucleation rates for calibration?**
   - The calcite literature has J values (nuclei/cm³/s) at various σ and T
   - We could normalize these to an initiative scale
   - But natural systems are much more complex than lab solutions

---

## Sources

- ScienceDirect: Nucleation Rate overview (Arrhenius form, activation barrier)
- McGill EPS C644: Principles of Crystal Nucleation and Growth (supersaturation dependence, induction time)
- Nature Communications Chemistry: CaCO₃ on quartz — activation energy and pre-exponential factor (2018)
- PNAS: Directed nucleation and growth by balancing local supersaturation and substrate/nucleus lattice mismatch (2018)
- ACS Crystal Growth & Design: Supersaturation and Crystal Resilience (growth-dominated vs nucleation-dominated regimes)
- Burton-Cabrera-Frank theory (1951, 2016 review): step-flow kinetics, surface diffusion, regime dependence
- UCLA Manning: Thermodynamic model for mineral solubility (Ksp, ΔG°, enthalpy)

---

**Bottom line:** The initiative variable maps cleanly to real geochemical kinetics. Temperature modifiers, edge-of-gate penalties, and competition effects all have physical analogues in nucleation theory. The question isn't whether to model them — it's which level of detail captures the behavior we want without overfitting.

— 🪨✍️
