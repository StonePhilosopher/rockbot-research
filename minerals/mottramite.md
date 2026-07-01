# Research: Mottramite

**Date:** 2026-05-11
**Status:** Complete — ready for Vugg Simulator implementation
**Paragenetic partner:** Descloizite (see `memory/research-descloizite.md`)

---

## Species: Mottramite

### Identity
- **Formula:** PbCu(VO₄)(OH) — ideal end-member; natural material seldom pure, usually containing significant Zn
- **Crystal system:** Orthorhombic
- **Space group:** Pnma
- **Crystal class:** Dipyramidal (mmm)
- **Mineral group:** Adelite-Descloizite group / Vanadates
- **Hardness (Mohs):** 3 – 3.5
- **Specific gravity:** 5.9 (slightly lighter than descloizite due to Cu being lighter than Zn, but still exceptionally heavy from lead)
- **Cleavage:** None observed
- **Fracture:** Irregular/uneven, sub-conchoidal
- **Tenacity:** Brittle
- **Luster:** Greasy, slightly resinous to dull

### Color & Appearance
- **Typical color:** Grass-green, olive-green, yellow-green, siskin-green, blackish brown, nearly black
- **Color causes:** Cu²⁺ d-d transitions in distorted octahedral coordination; Cu²⁺ is a classic chromophore producing green/blue colors in minerals
- **Transparency:** Transparent to opaque
- **Streak:** Yellowish green
- **Notable visual features:** Strong pleochroism — X=Y= canary yellow to greenish yellow, Z= brownish yellow; arborescent (tree-like, branching) crystal aggregates from Tsumeb are world-famous; botryoidal forms have velvety surface sheen

### Crystal Habits
- **Primary habit:** Encrustations, aggregates of plume-like forms, radial crystals, botryoidal masses
- **Common forms/faces:** Short prismatic, acicular (needle-like), dendritic branching
- **Twin laws:** None commonly reported
- **Varieties:**
  - **Duhamelite:** Calcium- and bismuth-bearing variety, typically acicular (named for Duhamel du Monceau)
  - **Psittacinite:** Historical name for the grass-green variety (from Latin *psittacus*, parrot)
- **Special morphologies:** Arborescent dendrites, botryoidal spheres with velvety surface, drusy crusts, plumose aggregates, radiating sprays

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 15–80°C (supergene/oxidation zone)
- **Optimal growth temperature:** 20–40°C
- **Decomposition temperature:** ~600°C (dehydrates and oxidizes)
- **Temperature-dependent habits:** Lower temperatures favor botryoidal/dendritic forms; moderate temperatures favor prismatic crystals

#### Chemistry Required
- **Required elements in broth:** Pb (≥200 ppm), Cu (≥100 ppm), V (≥50 ppm)
- **Optional/enhancing elements:** Zn (up to significant substitution toward descloizite), Ca, Bi (forms duhamelite variety)
- **Inhibiting elements:** High Fe²⁺, high CO₃²⁻ (favors malachite/azurite/cerussite), high PO₄³⁻, high AsO₄³⁻ (competing anions)
- **Required pH range:** 5.5–8.5 (weakly acidic to mildly alkaline)
- **Required Eh range:** Oxidizing (>+0.2V)
- **Required O₂ range:** >2 ppm dissolved O₂

#### Secondary Chemistry Release
- **Does it release chemicals when forming?** Consumes OH⁻; may locally acidify
- **Byproducts of nucleation:** None significant
- **Byproducts of dissolution/decomposition:** Releases Pb²⁺, Cu²⁺, V⁵⁺; Cu may re-precipitate as malachite/azurite if CO₃ available

#### Growth Characteristics
- **Relative growth rate:** Moderate to fast (≈3–5× quartz baseline)
- **Maximum crystal size in nature:** Individual crystals to 2 mm; arborescent aggregates to 5+ cm; crusts to 10+ cm
- **Typical crystal size in vugs:** 0.1–1 mm in drusy/botryoidal masses
- **Does growth rate change with temperature?** Yes — faster at 30–50°C, slower below 15°C
- **Competes with:** Vanadinite, wulfenite, malachite, azurite, brochantite, antlerite, chrysocolla, descloizite (if Zn > Cu)

#### Stability
- **Breaks down in heat?** Yes — dehydrates ~300°C, decomposes by 600°C
- **Breaks down in light?** No — photostable
- **Dissolves in water?** Very low solubility; dissolves in acidic groundwater
- **Dissolves in acid?** Readily soluble in acids (noted as "readily soluble in acids" in mineralogical literature)
- **Oxidizes?** Already fully oxidized (Cu²⁺, V⁵⁺, Pb²⁺)
- **Dehydrates?** Yes — loses structural OH and hydration water above 300°C
- **Radiation sensitivity:** Mild — U/Th inclusions may darken specimen over time

### Paragenesis
- **Forms AFTER:** Chalcopyrite (CuFeS₂), bornite, or other Cu sulfides must oxidize to release Cu²⁺; galena must oxidize for Pb²⁺; primary V-bearing minerals must weather
- **Forms BEFORE:** Malachite/azurite may replace it if CO₃ becomes available; iron oxides may encrust it; descloizite may replace it if Zn/Cu ratio rises
- **Commonly associated minerals:** Vanadinite, wulfenite, descloizite, malachite, azurite, chrysocolla, cuprite, native copper, cerussite, smithsonite, anglesite
- **Zone:** Supergene/oxidation zone
- **Geological environment:** Oxidized portions of copper-lead vein deposits; gossans; particularly common where Cu and Pb mineralization overlap (e.g., Tsumeb: Cu-Pb-Zn-Ag-Ge-Cd deposit)

### Famous Localities
- **Tsumeb Mine, Namibia:** World-famous arborescent (tree-like branching) and botryoidal specimens — grass-green to olive, velvety surfaces, often intergrown with descloizite. The type locality for exceptional mottramite. Specimens from early 20th century mining are most prized.
- **Ojuela Mine, Mapimí, Durango, Mexico:** Fine drusy crusts and botryoidal masses, often with wulfenite. A close second to Tsumeb in collector esteem.
- **Mottram St Andrew, Cheshire, England:** Type locality (1876). Mineral was named for ore stockpiled at this locality, though probably mined from Pim Hill Mine, Shrewsbury. Named by miners' tradition, not discovery at the spot.
- **Berg Aukas, Namibia:** Fine crystals intergrown with descloizite, demonstrating the solid solution relationship.
- **Arizona and New Mexico, USA:** Encrustations in oxidized porphyry Cu and Pb-Zn deposits.

### Fluorescence
- **Fluorescent under UV?** No — non-fluorescent
- **Activator:** None
- **Quenched by:** Fe²⁺, Cu²⁺ (both are fluorescence quenchers)

### Flavor Text

> Mottramite is the copper voice in the vanadate choir — grass-green where descloizite sings in red, arborescent where its partner grows in blades. Named for a stockpile of ore at Mottram St Andrew in Cheshire, England, this mineral probably never saw its namesake town in crystal form; the finest specimens come from Tsumeb, Namibia, where it grows in branching dendrites like frozen lightning, or in botryoidal spheres with the velvet sheen of moss. It is the copper end of a bridge that stretches to descloizite, and nature builds that bridge in both directions within a single crystal: a green heart and a red rim, or vice versa, depending on which metal the groundwater favored that season. The pleochroism is unmistakable — canary yellow to brownish yellow depending on angle — a mineral that changes its tune when you turn it. It dissolves readily in acid, as if it knows it is only a temporary guest in the oxidation zone, a transient arrangement of copper, lead, and vanadium held together by a single hydroxyl and the patience of geological time. In the vug, it arrives with the cool oxidizing waters that follow the sulfides' surrender, and it leaves when the chemistry shifts, perhaps replaced by malachite, perhaps buried under iron oxides, perhaps simply — eventually — weathered back to the elements it came from.

---

## Shared Paragenetic Sequence: Descloizite-Mottramite Series

*(Full details in `memory/research-descloizite.md`)*

These two minerals share:
- Complete solid solution: Cu ↔ Zn substitution in the same orthorhombic Pnma structure
- Same formation environment: oxidation zone of base metal deposits
- Same temperature range: 15–80°C supergene
- Same geological associations
- Same exceptional density from lead content
- Same greasy luster and ~3–3.5 hardness

Natural specimens record the Cu:Zn evolution of their precipitating fluid. A zoned crystal is a chemical stratigraphy — each zone a season of groundwater chemistry frozen in vanadate.

---

### Simulator Implementation Notes

- **New parameters needed:** None — uses existing Pb, Cu, Zn, V, pH, Eh, O₂
- **New events needed:** `event_copper_pulse` (for mottramite-dominant scenarios)
- **Nucleation rule pseudocode:**
```
IF Pb ≥ 200 ppm AND Cu ≥ 100 ppm AND V ≥ 50 ppm
   AND pH 5.5–8.5 AND Eh > +0.2V AND T 15–80°C
   AND Cu:Zn_ratio > 1.0
   → nucleate mottramite (priority over descloizite if Cu dominates)
```
- **Growth rule pseudocode:**
```
IF σ_mottramite > 1.0 AND vug_fill < 0.85
   → grow at rate 4× quartz_baseline
   → habit: arborescent if T < 30°C + high σ
            botryoidal if T 20–35°C + moderate σ
            prismatic if T > 35°C + low σ
```
- **Habit selection logic:**
  - T < 25°C + high σ → arborescent/dendritic branching (Tsumeb-type)
  - T 25–40°C + moderate σ → botryoidal spheres with velvety surface
  - T > 35°C + low σ → short prismatic crystals
  - Very high σ + any T → drusy crusts
- **Decomposition products:** Above 600°C → lead vanadate oxide + CuO + H₂O vapor
- **Solid solution mechanic:** If Zn > Cu in fluid, crystal composition shifts toward descloizite; display as zoned color change (green core → red-brown rim)

### Variants for Game

- **Variant 1: Tsumeb Arborescent** — World-famous branching dendrites, grass-green, velvety surface. Requires low T (<25°C) + high Cu + moderate σ + slow growth over long time. The crown jewel of mottramite.
- **Variant 2: Botryoidal Velvet** — Spherical aggregates with velvety sheen, olive to moss-green. Moderate T (25–35°C) + moderate σ. Classic specimen habit.
- **Variant 3: Duhamelite Needles** — Acicular crystals, Ca- and Bi-bearing variety. Requires Ca >50 ppm and Bi trace in fluid. Slender prismatic habit, yellow-green.
- **Variant 4: Blackish Massive** — Nearly black, massive to granular, high Cu content with Fe impurities. Forms in Fe-rich oxidation zones where Cu is abundant but conditions are messy.

---

*Research compiled from Wikipedia, Mindat, Handbook of Mineralogy, and Millman (1960) American Mineralogist 45:763.*
