# Research: Pyrite — Vugg Simulator

**Date:** 2026-05-10
**Researcher:** 🪨✍️ (cron expansion)
**Status:** Complete
**Paragenetic context:** Forms the Fe-S₂ pair with marcasite (see `research-pyrite-marcasite.md` for polymorph comparison). Also anchors the iron sulfide → oxide paragenetic sequence.

---

## Species: Pyrite

### Identity
- **Formula:** FeS₂
- **Crystal system:** Cubic (isometric), space group Pa3
- **Mineral group:** Sulfide (disulfide)
- **Hardness (Mohs):** 6–6.5
- **Specific gravity:** 4.95–5.10
- **Cleavage:** Poor on {001}; indistinct on {110}
- **Fracture:** Conchoidal to uneven
- **Luster:** Metallic, brilliant when fresh ("fool's gold")

### Color & Appearance
- **Typical color:** Pale brass-yellow to golden, tarnishing darker brown or iridescent
- **Color causes:** Intrinsic metallic bonding between Fe²⁺ and S₂²⁻ disulfide units — no chromophore ions needed
- **Transparency:** Opaque
- **Streak:** Greenish-black to brownish-black — diagnostic and consistent
- **Notable visual features:** Striations on cube faces (perpendicular on adjacent faces — a dead giveaway). Iridescent tarnish films can mimic bornite's "peacock ore" but pyrite tarnish is thinner and more structurally controlled. Massive forms show granular to conchoidal texture.

### Crystal Habits
- **Primary habit:** Cube {100} — the iconic form that built a thousand false gold rushes
- **Common forms/faces:**
  - Cube {100} — most common, often striated
  - Octahedron {111} — moderate supersaturation
  - Pyritohedron {210} — the shape named for this mineral; higher supersaturation
  - Dodecahedron {110} — less common
  - Combinations: cube + octahedron bevels, cube + pyritohedron modifications
- **Twin laws:**
  - Penetration twin on {110} — the famous "iron cross" twin (rare but celebrated)
  - Contact twins on {001} — less dramatic but documented
- **Varieties:**
  - **Bravoite:** Ni-Co-bearing variety, darker, from sulfide deposits
  - **Uralite:** Finely fibrous/radiating habit
- **Special morphologies:**
  - **Framboidal:** Raspberry-like microspheres of tiny pyrite cubes — ubiquitous in sediments, formed by burst nucleation in homogeneous chemical environments
  - **Pyrite suns:** Flat radiating disc-shaped aggregates from coal shales (Sparta, Illinois)
  - **Massive, reniform, stalactitic, dendritic** — secondary habits in void-filling and replacement contexts

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 25–743°C (enormous span — from bacterial sulfate reduction to magmatic-hydrothermal systems)
- **Optimal growth temperature:** 150–400°C (hydrothermal sweet spot for large euhedral crystals)
- **Decomposition temperature:** ~600–743°C (incongruent melting → pyrrhotite Fe₁₋ₓS + sulfur vapor; range depends on crystal perfection and sulfur content)
- **Temperature-dependent habits (per Murowchick & Barnes 1987, Arrouvel & Eon 2019):**
  - Low T + low sulfur supersaturation → smooth cubes {100}
  - Moderate T + higher σ → octahedra {111}
  - Higher T + high σ → pyritohedra {210}
  - Very high σ → spherulites, framboids, dendrites
  - Critical finding: sulfur-saturated conditions favor non-cubic forms (octahedral, pyritohedral); low-sulfur conditions favor cubes

#### Chemistry Required
- **Required elements in broth:** Fe (≥50 ppm as Fe²⁺), S (≥100 ppm as H₂S/HS⁻ or polysulfides)
- **Optional/enhancing elements:**
  - Ni, Co → bravoite variety
  - As → arsenian pyrite (affects habit, common in Carlin-type gold deposits)
  - Au → submicroscopic inclusions (Carlin-type deposits)
- **Inhibiting elements:** High O₂ suppresses pyrite (oxidizes Fe²⁺ and sulfide to sulfate); organic matter can complex Fe and delay nucleation
- **Required pH range:** ~4–10 (broad tolerance, but pyrite dominates at neutral to mildly alkaline conditions; marcasite wins below pH 5–6)
- **Required Eh range:** Reducing (Eh < 0 V at pH 7). Forms in anoxic, sulfidic conditions. The H₂S/SO₄²⁻ redox boundary.
- **Required O₂ range:** Very low to absent. Pyrite is destroyed by oxidation.

#### Secondary Chemistry Release
- **Does it release chemicals when forming?** Consumes Fe²⁺ and H₂S/HS⁻ from solution. Nucleation is mildly acid-generating if Fe³⁺ is reduced, but net pH effect is usually small in hydrothermal systems.
- **Byproducts of dissolution/oxidation:** This is the big one. Pyrite oxidation: 2FeS₂ + 7O₂ + 2H₂O → 2Fe²⁺ + 4SO₄²⁻ + 4H⁺. The engine of acid mine drainage. The 4H⁺ released per 2FeS₂ is geologically catastrophic — it dissolves carbonates, mobilizes heavy metals, and remakes entire landscapes. In the simulator, pyrite oxidation should acidify the broth and release Fe²⁺/SO₄²⁻.

#### Growth Characteristics
- **Relative growth rate:** Moderate — slower than chalcopyrite in porphyry systems, faster than quartz in low-T hydrothermal veins
- **Maximum crystal size:** To 30+ cm cubes (Navajún, Spain — world record)
- **Typical crystal size in vugs:** 0.5–5 cm
- **Does growth rate change with temperature?** Yes — faster at higher T, but morphology shifts dramatically with supersaturation (not just T)
- **Competes with:** Marcasite (same chemistry, acidic pH wins), pyrrhotite (higher T, lower S activity), chalcopyrite (competes for Fe), goethite/hematite (oxidizing conditions outcompete)

#### Stability
- **Breaks down in heat?** At ~600–743°C decomposes to pyrrhotite + S vapor. The exact temperature depends on crystallinity and sulfur content.
- **Breaks down in light?** No (unlike realgar, proustite, or some silver sulfosalts)
- **Dissolves in water?** Very slowly in deoxygenated water. Rapidly in oxidizing acidic water.
- **Dissolves in acid?** Slowly in HCl; readily in oxidizing acids (HNO₃, aqua regia)
- **Oxidizes?** Yes — the classic sequence: pyrite → Fe²⁺ + SO₄²⁻ → Fe(OH)₃ (goethite/limonite) + H₂SO₄. Pyrite "rusting" produces sulfuric acid and iron oxides. Limonite pseudomorphs after pyrite cubes are common (the shape survives, the mineral doesn't).
- **Dehydrates?** No (anhydrous)
- **Radiation sensitivity:** Minimal structural damage; slight darkening possible at extreme doses but not characteristic

### Paragenesis
- **Forms AFTER:** Early pyrrhotite (if present, at higher T), magnetite (in some reducing skarns)
- **Forms BEFORE:** Marcasite (if pH drops later), chalcopyrite, galena, sphalerite (in zoned veins), all oxide/hydroxide weathering products
- **Commonly associated minerals:** Quartz (ubiquitous partner), calcite, chalcopyrite, galena, sphalerite, pyrrhotite, arsenopyrite, gold, fluorite, barite
- **Zone:** Primary/hypogene (most common), sedimentary (framboidal in shales/coal), metamorphic (recrystallized), supergene relict (surviving in oxidation zones briefly)
- **Geological environment:** Literally everywhere — hydrothermal veins, VMS deposits, porphyry copper systems, sedimentary basins, coal beds, metamorphic rocks, black shales, pegmatites (minor), volcanic fumaroles (rare)

### Famous Localities
- **Navajún, La Rioja, Spain:** World's finest pyrite cubes, up to 30+ cm, perfect geometry, often intergrown groups on white clay matrix or free-standing. The standard against which all pyrite is measured. The local inhabitants around 300 BC were known as the Piritas — they used pyrite crystals for magic.
- **Huanzala Mine, Huallanca District, Peru:** Brilliant striated cubes with quartz and galena. Some of the sharpest, most lustrous pyrite in the world.
- **Sparta, Illinois, USA:** Pyrite "suns" — flat radiating disc-shaped aggregates in coal shales. The sunflower of the mineral world.
- **Flambeau Mine, Ladysmith, Wisconsin:** Brilliant cubes on matrix
- **Elba, Italy:** Historical locality for fine crystals
- **Mina Justa, Peru:** Exceptional octahedral crystals
- **Notable specimens:** Navajún cubes are the benchmark. A 30 cm perfect cube perched on white matrix is a six-figure specimen.

### Fluorescence
- **Fluorescent under UV?** No. Pyrite is a metallic opaque sulfide with no fluorescence mechanism.
- **SW (255nm) color:** None
- **MW (310nm) color:** None
- **LW (365nm) color:** None
- **Phosphorescent?** No
- **Activator:** N/A
- **Quenched by:** N/A

### Flavor Text
> Pyrite is the mineral that fooled a million prospectors — brass-bright cubes so perfect they look machined, striated faces catching light like burnished armor. But pyrite isn't pretending to be gold. It's been here far longer than we have. Those cubic crystals grew in the dark, one sulfur-iron layer at a time, while the mountains above them rose and eroded twice over. Striations on the faces record the competition between growth directions — a tug-of-war between {100} and {210} faces that plays out at the atomic scale. When oxygen finally reaches pyrite, it doesn't just dissolve. It burns. Sulfuric acid bleeds from the fracture, and the perfect cube becomes a rusted ghost — a limonite pseudomorph that remembers the shape but has forgotten the mineral. Navajún specimens, with their impossible geometry and matrix-free cubes, are the standard against which all others are measured. The Earth grew these on its own, no lapidary required.

### Simulator Implementation Notes
- **New parameters needed:** `sulfur_supersaturation` or `S_species_ratio` — the Murowchick & Barnes 1987 finding that sulfur availability controls morphology, not just temperature. Need to track whether sulfur is in excess (favors octahedral/pyritohedral) or limiting (favors cubes).
- **New events needed:** `event_pyrite_sun` — sedimentary concretion in coal-shale context; `event_framboid_burst` — very high supersaturation produces microspheres instead of single crystals.
- **Nucleation rule pseudocode:**
```
IF trace_Fe >= 50 AND trace_S >= 100 AND pH > 4.5 AND Eh < 0 AND T < 600:
  IF pH > 5.5 OR (pH > 4.5 AND marcasite_not_preferred):
    nucleate PYRITE
  ELSE IF pH 4.5–5.5 AND random() < 0.3:
    nucleate PYRITE  // overlap zone
```
- **Growth rule pseudocode:**
```
rate = base_rate * f(trace_Fe, trace_S) * temp_factor
IF sulfur_excess AND sigma > 2:
  habit = octahedral  // {111}
  IF sigma > 5:
    habit = pyritohedral  // {210}
    IF sigma > 8 AND T < 200:
      habit = framboidal  // burst nucleation microspheres
ELSE IF sulfur_limiting AND sigma < 2:
  habit = cubic  // {100}, smooth or striated
IF T > 573°C:
  twin_prob = 0.7  // Dauphiné-like behavior in β-pyrite regime
```
- **Habit selection logic:**
  - Low σ + low S availability → cube {100}
  - Moderate σ + high S availability → octahedron {111}
  - High σ + high S availability → pyritohedron {210}
  - Very high σ + low T → framboid (sedimentary burst nucleation)
  - Sedimentary event + moderate σ → pyrite sun (radiating disc)
- **Decomposition products:**
  - At ~600–743°C: pyrrhotite (Fe₁₋ₓS) + S vapor (released to fluid)
  - On oxidation: Fe²⁺ + SO₄²⁻ + 4H⁺ (acidifies broth, releases sulfate)
  - Long-term oxidation endpoint: goethite/limonite (FeOOH/Fe₂O₃·nH₂O) — the pseudomorph remembers the cube

### Variants for Game
- **Variant 1: Cubic pyrite** — low supersaturation, sulfur-limiting conditions, any T. The Navajún look. Striated if slow growth, smooth if moderate.
- **Variant 2: Octahedral pyrite** — moderate σ, sulfur-rich conditions. High-T hydrothermal look.
- **Variant 3: Pyritohedral pyrite** — high σ, sulfur-rich. The "classic" crystal-collector shape.
- **Variant 4: Pyrite sun** — requires sedimentary environment event, flat radiating habit. Coal-shale context.
- **Variant 5: Framboidal pyrite** — very high σ + low T + sedimentary event. Micro raspberry clusters. Buried in shale, not a vug mineral, but relevant for sedimentary scenario.
- **Variant 6: Limonite pseudomorph after pyrite** — oxidation transformation event. Keeps cube shape, changes mineral identity, color shifts to rust-brown.

---

## Linked Paragenetic Sequence: Iron Sulfide → Oxide

Pyrite sits at the heart of the most important oxidation sequence in mineralogy:

1. **Pyrrhotite** (Fe₁₋ₓS) — higher T, S-deficient, forms first in magmatic systems
2. **Pyrite/marcasite** (FeS₂) — the sulfide stable at lower T, the starting point for oxidation
3. **Goethite** (FeOOH) — first oxidation product, hydrated, low T
4. **Hematite** (Fe₂O₃) — dehydration of goethite at ~300°C, or direct oxidation at higher T

And the full Eh-pH sequence:
- **Reducing, acidic, high S:** pyrite (or marcasite if pH < 5.5)
- **Reducing, intermediate fO₂:** magnetite (Fe₃O₄) — mixed valence iron oxide
- **Oxidizing:** hematite (Fe₂O₃) — fully oxidized endpoint
- **Hydrated oxidizing, low T:** goethite/limonite (FeOOH)

In the simulator, pyrite oxidation is the **acid engine**. When O₂ enters a vug with pyrite:
1. Pyrite dissolves, releasing Fe²⁺, SO₄²⁻, and H⁺ (broth acidifies)
2. Fe²⁺ oxidizes to Fe³⁺ (if O₂ persists)
3. Fe³⁺ precipitates as goethite or hematite (depending on T and pH)
4. The acidified broth now dissolves carbonates, mobilizes Cu/Pb/Zn, and drives supergene enrichment

This is why pyrite isn't just a mineral — it's a geological catalyst.

---

## Cross-References
- **Polymorph pair:** Marcasite — `memory/research-pyrite-marcasite.md`
- **Higher-T Fe-sulfide:** Pyrrhotite (Fe₁₋ₓS) — not yet researched; forms by exsolution from monosulfide solid solution (MSS)
- **Oxidation products:** Hematite — `memory/research-hematite.md`; Goethite — not yet researched
- **Mixed-valence oxide:** Magnetite — `memory/research-magnetite.md`
- **Carbonate competitor:** Siderite (FeCO₃) — not yet researched; competes for Fe in CO₂-rich fluids
- **Acid generation:** Pyrite/marcasite oxidation is the primary acid source for supergene copper/lead/zinc oxidation zones
