# Mineral Species — Colemanite

## Species: Colemanite

### Identity
- **Formula:** Ca₂B₆O₁₁·5H₂O (or CaB₃O₄(OH)₃·H₂O in some notations)
- **Crystal system:** Monoclinic (2/m)
- **Mineral group:** Borate (inoborate subgroup)
- **Hardness (Mohs):** 4.5
- **Specific gravity:** 2.42
- **Cleavage:** Perfect on {010}, distinct on {001}
- **Fracture:** Brittle, uneven to subconchoidal
- **Luster:** Vitreous

### Color & Appearance
- **Typical color:** Colorless, white, yellowish, pale grey; rarely pink or greenish from trace impurities
- **Color causes:** Pure colemanite is colorless; yellow tones from iron oxide staining, blue from clay inclusions
- **Transparency:** Transparent to translucent
- **Streak:** White
- **Notable visual features:** Most commonly nodular or massive granular; well-formed crystals show brilliant vitreous luster. Exfoliates on heating (dehydration cracking). Produces a characteristic green flame in flame test (boron). Pyroelectric and piezoelectric at very low temperatures.

### Crystal Habits
- **Primary habit:** Massive granular to coarsely crystalline; most commonly nodular
- **Common forms/faces:** Short prismatic crystals when well-formed; equant to flattened habit
- **Twin laws:** Contact twins on {100} reported
- **Varieties:** None formally recognized
- **Special morphologies:** Nodular masses, thin crusts, fibrous aggregates; rarely forms euhedral crystals in vugs

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 20–60°C (evaporite basin, alkaline lacustrine)
- **Optimal growth temperature:** 30–50°C
- **Decomposition temperature:** ~200°C (loses water of crystallization progressively)
- **Temperature-dependent habits:** Warmer temperatures favor larger nodules; cooler conditions may produce more crystalline forms

#### Chemistry Required
- **Required elements in broth:** Ca²⁺, B (as borate, B₄O₇²⁻ or BO₃³⁻), H₂O
- **Optional/enhancing elements:** Na⁺ (promotes earlier borax/ulexite stages, setting up late colemanite alteration)
- **Inhibiting elements:** High sulfate (competes for Ca²⁺ → gypsum/anhydrite), high Mg²⁺ (→ kieserite, dolomite)
- **Required pH range:** 8–10.5 (strongly alkaline — borate stability requires high pH)
- **Required Eh range:** Not redox-sensitive
- **Required O₂ range:** Irrelevant (non-redox)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No direct byproducts, but progressively dehydrating colemanite concentrates residual brine in other ions
- **Byproducts of nucleation:** Minor OH⁻ consumption
- **Byproducts of dissolution/decomposition:** Dissolves in hot water, releasing Ca²⁺ + borate ions; dehydration → metacolemanite + H₂O vapor

#### Growth Characteristics
- **Relative growth rate:** Slow — requires long evaporative cycles; secondary after borax/ulexite
- **Maximum crystal size:** Nodules to 30+ cm in some deposits; individual crystals rarely exceed a few cm
- **Typical crystal size in vugs:** 1–5 cm nodular masses; rarely euhedral crystals
- **Does growth rate change with temperature?** Warmer = faster evaporation = faster growth but lower crystal quality
- **Competes with:** Ulexite (earlier stage, lower Ca), borax (earlier stage, higher Na), howlite (similar chemistry, different structure)

#### Stability
- **Breaks down in heat?** Exfoliates and dehydrates starting around 150–200°C; progressively loses 5 H₂O
- **Breaks down in light?** No
- **Dissolves in water?** Slightly soluble in cold water; more soluble in hot water (retrograde solubility like gypsum)
- **Dissolves in acid?** Yes — soluble in HCl with decomposition
- **Oxidizes?** No
- **Dehydrates?** Yes — metacolemanite at ~150°C, then anhydrous calcium borate at higher T
- **Radiation sensitivity:** Not documented

### Paragenesis
- **Forms AFTER:** Borax (Na₂B₄O₇·10H₂O) and ulexite (NaCaB₅O₆(OH)₆·5H₂O) — colemanite is a secondary/tertiary borate derived from alteration of earlier borates as brine evolves toward Ca-dominance
- **Forms BEFORE:** Probertite, howlite, or late-stage Ca-Mg borates in fully mature brine
- **Commonly associated minerals:** Borax, ulexite, kernite, howlite, gypsum, anhydrite, calcite, halite
- **Zone:** Evaporite (late-stage, alkaline lacustrine), also as diagenetic alteration product in buried borate beds
- **Geological environment:** Arid-climate alkaline playa lakes fed by geothermal/volcanic borate springs; also Tertiary lacustrine borate deposits (Death Valley-type)

### Famous Localities
- **Classic locality 1:** Furnace Creek area, Death Valley, Inyo County, California, USA — type locality (1884), Harmony Borax Works
- **Classic locality 2:** Emet mine, Kütahya Province, western Turkey — ~40% of world known reserves, massive nodular ore
- **Classic locality 3:** Bigadiç district, Balıkesir Province, Turkey — second major Turkish borate district
- **Notable specimens:** Brilliant transparent crystals from Death Valley (historic, rare); large nodular masses from Turkish mines; pink tints from some localities

### Fluorescence
- **Fluorescent under UV?** Yes — bright pale yellow fluorescence is diagnostic
- **SW (255nm) color:** Pale yellow to cream
- **MW (310nm) color:** Pale yellow (strongest response)
- **LW (365nm) color:** Pale yellow to greenish yellow
- **Phosphorescent?** Yes — may phosphoresce pale green after UV exposure
- **Activator:** Borate lattice itself (intrinsic fluorescence of BO₃/BO₄ groups); trace Mn²⁺ may contribute
- **Quenched by:** Iron oxide staining can reduce fluorescence intensity

### Flavor Text
> Colemanite is what remains when a lake full of borax has died and been buried. First the sodium crystallizes out as borax, then as the brine leaches calcium from surrounding mud, ulexite bridges the gap, and finally — when almost everything volatile has left — colemanite forms: a calcium borate with five waters still clinging to its skeleton, nodular and massive, the mineral equivalent of a body that refused to fully mummify. It was the backbone of the borax industry until 1926, when kernite displaced it, and the mineral world moved on. But Death Valley still remembers. The old Harmony Borax Works crumbled, but colemanite nodules remain in the playa mud, still fluorescing pale yellow under a blacklight, still exfoliating when heated, still producing that green boron flame. Some minerals are remembered for their beauty. Colemanite is remembered for what it made possible — glass that withstands thermal shock, ceramics that survive the kiln, antiseptics that saved lives. It is the foundation stone beneath modern boron chemistry, and it looks like nothing special: white lumps in alkaline mud. The most important minerals often do.

### Simulator Implementation Notes
- **New parameters needed:** Boron (B) as trace element; brine concentration index; alkaline lake scenario
- **New events needed:** Evaporite sequence event: borax → ulexite → colemanite progression; seasonal evaporation/recharge cycles
- **Nucleation rule pseudocode:**
```
IF scenario == "alkaline_lake" OR scenario == "evaporite_basin"
  AND trace_B > very_high AND trace_Ca > high
  AND pH > 8.5 AND brine_concentration > colemanite_saturation
  AND borax_already_nucleated == true (earlier stage)
  AND temperature > 20 AND temperature < 60
  → nucleate colemanite (max 3 nuclei, nodular habit)
```
- **Growth rule pseudocode:**
```
IF σ_colemanite > 1.0 AND vug_fill < 1.0
  → grow at slow rate
  habit = "nodular" (default) | "prismatic" (if slow growth + open vug)
```
- **Habit selection logic:** Default nodular/massive (evaporite character). Open vug + slow growth → rare euhedral crystals. High pH + low competition → larger nodules.
- **Decomposition products:** Dehydration → metacolemanite + H₂O vapor; further heating → anhydrous calcium borate

### Variants for Game
- **Variant 1:** Standard colemanite — white to colorless nodular masses (typical evaporite)
- **Variant 2:** Iron-stained colemanite — yellow to brown surface staining from goethite/limonite inclusions
- **Variant 3:** Death Valley crystal — rare transparent prismatic crystals from vugs in altered borate beds (collectible, high clarity, strong fluorescence)
