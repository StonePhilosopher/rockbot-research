# Overgrowth Paragenesis: Does the Substrate Stop Growing?

**Research date:** 2026-05-21
**Source:** Scientific literature review (Putnis 2002/2009/2021, mineral replacement mechanics, hydrothermal paragenesis)
**Question:** When crystal B nucleates on crystal A in the Vugg Simulator, what happens to A's growth zones?

---

## The Short Answer

**It depends on the mechanism.** There are two fundamentally different processes that look similar at the macro scale but behave oppositely at the micro scale:

1. **Epitaxial Overgrowth** — B grows ON TOP of A. A continues growing underneath if fluid access persists.
2. **Coupled Dissolution-Precipitation (CDR/ICDR)** — B replaces A. A dissolves while B precipitates in its place. A stops existing.

The Vugg Simulator currently handles both but may conflate them.

---

## 1. Epitaxial Overgrowth (B on A)

**What happens to A:** A may continue growing if its crystal faces remain exposed to fluid.

**Real examples:**
- Barite on sphalerite in hydrothermal veins: barite commonly overgrows earlier sphalerite, but the sphalerite core retains its growth zoning — it didn't stop growing, it was simply engulfed (Sandatlas; Mindat sphalerite pseudomorphs)
- Sphalerite pseudomorphs after galena, tetrahedrite, barite, calcite (Wikipedia): the substrate mineral's crystal form is preserved, but this is REPLACEMENT, not overgrowth
- "The resulting pseudomorph may contain an unaltered core of galena surrounded by anglesite that has the cubic crystal shape of galena" (Wikipedia): here the core mineral SURVIVES — it didn't stop growing, it was protected

**Key point:** In true epitaxy, B nucleates on specific crystallographic faces of A. The substrate crystal A may continue to grow on its OTHER faces while B grows on the favored face. Both crystals compete for solutes. The substrate doesn't automatically stop.

**When A DOES stop growing under epitaxy:**
- When B completely encapsulates A, blocking all fluid access
- When fluid chemistry shifts to favor B exclusively (A becomes undersaturated and begins dissolving)
- When the epitaxial face of A is the only one exposed and B covers it

---

## 2. Coupled Dissolution-Precipitation (B replaces A)

**What happens to A:** A dissolves molecule-by-molecule while B precipitates in its place. A ceases to exist except as a pseudomorph.

**The mechanism (Putnis 2002, 2009, 2021):**
> "The fluid-filled porosity network facilitates diffusive mass transport of reactants to and dissolved products away from the parent phase that drives an autocatalytic reaction that pseudomorphically and potentially epitaxially replaces minerals."

Key features:
- **Nano- to micrometer-scale interfacial fluid film** separates dissolving A from precipitating B (ScienceDirect 2020)
- **A does not stop growing — A dissolves.** The concept of "growth" becomes irrelevant because A is being consumed
- The replacement front advances inward from the surface
- Generated porosity in B allows fluid infiltration, letting the replacement continue
- Volume changes between A and B create porosity that sustains the reaction

**Real examples from Vugg-relevant systems:**
- Calcite → fluorite replacement: "Porosity generated during the fluid-mediated replacement of calcite by fluorite" (ResearchGate)
- Aragonite → apatite: "Crystal growth of apatite by replacement of an aragonite precursor" — replacement, not overgrowth
- Zeolite → chalcedony (TN510): This is likely replacement via silica gel dissolution-precipitation, not true overgrowth
- Wood → silica (petrified wood): the cellulose dissolves while silica precipitates in its place

---

## 3. The Critical Distinction for the Simulator

The Vugg Simulator must distinguish between:

| Scenario | Mechanism | Does A stop? | Simulator behavior needed |
|----------|-----------|-------------|--------------------------|
| Barite on sphalerite (TN457) | Epitaxial overgrowth | Only if fully encapsulated | A continues; B nucleates on specific faces; competition for solutes |
| Chalcedony after zeolite (TN510) | CDR / replacement | A dissolves | A consumed; B inherits A's morphology as pseudomorph |
| Sphalerite replacing barite | CDR / replacement | A dissolves | Same as above |
| Quartz comb on calcite | Epitaxy or CDR? | Depends on chemistry | Needs discrimination logic |

**The user's intuition is correct for epitaxial overgrowth** — the substrate CAN stop growing if the overgrowth blocks fluid access. But it's not automatic. And in replacement, the substrate doesn't "stop growing," it dissolves.

---

## 4. What Controls Whether A Continues?

From the literature:

1. **Fluid access** — If B is porous or only covers part of A, A can continue (Pollok et al. 2011)
2. **Saturation state** — If A remains supersaturated, it continues growing. If it becomes undersaturated, it dissolves.
3. **Competition for solutes** — Both A and B compete for shared ions. If B is a faster sink, A's growth rate drops.
4. **Epitaxial strain** — Lattice mismatch between A and B can inhibit or promote further A growth
5. **Temperature / chemistry shifts** — The same event that nucleates B may change conditions to A's disadvantage

---

## 5. Recommendations for Vugg Simulator

**Option A: Two distinct mechanisms (correct but complex)**
- `OVERGROWTH` event: B nucleates on A's face. Both crystals tracked separately. B's zones record substrate reference. A continues growing on unblocked faces.
- `REPLACEMENT` event: A's zones stop recording new growth. A dissolves step-by-step. B precipitates in A's place, inheriting morphology. A eventually removed.

**Option B: Simplified rule (current intuition)**
- When B nucleates on A via epitaxy: A's growth on that face stops. A continues on other faces.
- When B replaces A via CDR: A dissolves. No "stopping" — it's consumption.

**The builder's current implementation** (from MEMORY.md): "substrate epitaxy all already shipped" — need to verify which mechanism is implemented.

---

## References

- Putnis A. (2002) "Mineral replacement reactions: from macroscopic observations to microscopic mechanisms." *Chemical Geology*.
- Putnis A. (2009) "Mineral replacement reactions." *Reviews in Mineralogy and Geochemistry*.
- Putnis A., Austrheim H. (2010) "Fluid-mediated processes."
- Pollok K., Putnis C.V., Putnis A. (2011) "Mineral replacement reactions in solid solution-aqueous solution systems." *American Journal of Science* 311(3):211-236.
- Ruiz-Agudo E. et al. (2014) "Coupled dissolution and precipitation at mineral-fluid interfaces." *Chemical Geology*.
- Altree-Williams et al. (2015) "Textural and compositional complexities resulting from coupled dissolution-reprecipitation reactions in geomaterials."
- Wang et al. (2020) "Model of interface-coupled dissolution-precipitation mechanism." *Geochimica et Cosmochimica Acta*.

---

## Connection to Memory

- TN457: Barite on sphalerite — this is OVERGROWTH, not replacement. The sphalerite core should survive unless conditions shift to dissolve it.
- TN510: Chalcedony pseudomorph after zeolite — this is REPLACEMENT (CDR). The zeolite dissolved while silica precipitated.
- Jeffrey mine chrysotile: Need to verify — is chrysotile replacing something (CDR) or growing on something (epitaxy)?
