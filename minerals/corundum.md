# Mineral Species Research: Corundum

**Date:** 2026-05-13
**Researcher:** 🪨✍️ (Vugg Simulator Expansion Architect)
**Status:** Complete — ready for implementation

---

## Species: Corundum

### Identity
- **Formula:** Al₂O₃
- **Crystal system:** Trigonal (hexagonal scalenohedral class, 3m)
- **Mineral group:** Oxide — Hematite group
- **Hardness (Mohs):** 9 (defining mineral for the scale)
- **Specific gravity:** 3.95–4.10 (typically ~4.02)
- **Cleavage:** None — parting in 3 directions (rhombohedral parting planes)
- **Fracture:** Conchoidal to uneven
- **Luster:** Adamantine to vitreous
- **Streak:** Colorless
- **Space group:** R3̄c (No. 167)
- **Unit cell:** a = 4.75 Å, c = 12.982 Å; Z = 6

### Color & Appearance
- **Typical color:** Colorless, gray, brown, golden-brown; gem varieties span the full spectrum
- **Color causes:**
  - **Cr³⁺** → red (ruby), pink
  - **Fe²⁺ + Ti⁴⁺** intervalence charge transfer → blue (sapphire)
  - **Fe³⁺ alone** → yellow, greenish-yellow
  - **Ti³⁺** → blue-green, violet
  - **V³⁺** → purple, gray-violet
  - **Ni²⁺** → yellow
  - **Co²⁺** → rare intense blue (Kashmir-type)
  - **Colorless** when pure (very rare in nature)
- **Transparency:** Transparent, translucent to opaque
- **Streak:** Colorless
- **Notable visual features:**
  - **Asterism (star effect):** Six-rayed star in cabochon-cut stones, caused by oriented rutile (TiO₂) needle inclusions ("silk") intersecting at 60°/120°. Requires dense, aligned needle clouds and a dome-shaped cut.
  - **Chatoyancy:** Rare cat's-eye effect from parallel needle alignment.
  - **Color zoning:** Common in natural crystals — bands of different color parallel to crystal faces, reflecting changing fluid chemistry during growth.
  - **Silk:** Rutile needle inclusions that scatter light, improving brilliance in faceted stones and creating stars in cabochons.

### Crystal Habits
- **Primary habit:** Steep bipyramidal, tabular, prismatic, rhombohedral
- **Common forms/faces:** Basal pinacoid {0001}, hexagonal prism {11̄20}, rhombohedron {10̄11}, dipyramid {22̄41}
- **Twin laws:**
  - **Polysynthetic twinning** on the rhombohedral plane {10̄11} — very common, produces laminar structure with striations on basal faces and prism faces
  - **Contact twinning** on {0001} basal pinacoid — "arrowhead" or "fisheye" twin in tabular crystals
  - **Penetration twinning** on {10̄12} — rare
- **Varieties:**
  - **Ruby** — red, Cr-bearing
  - **Sapphire** — any color except red (blue is most famous)
  - **Padparadscha** — pink-orange, from Sri Lanka, named after the lotus blossom
  - **Star ruby / Star sapphire** — asteriated varieties
  - **Emery** — black granular corundum mixed with magnetite, hematite, or hercynite (industrial abrasive)
- **Special morphologies:**
  - Massive or granular (emery)
  - Barrel-shaped alluvial crystals (water-worn, from placers)
  - Pigeon-blood red rubies in marble matrix (Mogok)

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 600–1000°C
- **Optimal growth temperature:** 700–900°C in metamorphic environments; 500–700°C in pegmatites
- **Decomposition temperature:** Melts at 2044°C (far above any natural geological conditions)
- **Temperature-dependent habits:**
  - **High T (>800°C):** Prismatic, elongated hexagonal crystals
  - **Moderate T (600–800°C):** Tabular, bipyramidal
  - **Lower T pegmatite:** Massive to coarse granular

#### Chemistry Required
- **Required elements in broth:**
  - **Al** — high concentration required. Corundum is essentially pure Al₂O₃. In the simulator, this requires adding **Al as a new broth variable** (not currently in the 30-trace list).
  - **Si** must be LOW or ABSENT — corundum forms only in silica-undersaturated environments. High Si produces aluminosilicates (kyanite, andalusite, sillimanite, feldspars) instead.
- **Optional/enhancing elements:**
  - **Cr** — creates ruby (red)
  - **Fe + Ti** — creates blue sapphire (intervalence charge transfer)
  - **Fe³⁺** — yellow, greenish-yellow
  - **V** — purple, violet
  - **Ti** alone — rutile silk inclusions (asterism when needles oriented)
  - **Ni** — yellow
  - **Co** — intense blue (rare)
- **Inhibiting elements:**
  - **Si** — THE primary inhibitor. Any significant Si concentration will outcompete corundum and form feldspar, kyanite, or other aluminosilicates. Corundum requires silica-deficient (peraluminous) conditions.
  - **Na, K** — promote feldspar formation over corundum
  - **Ca** — promotes anorthite, scapolite, or Ca-Al silicates
  - **Mg** — promotes spinel (MgAl₂O₄), which commonly coexists with or replaces corundum
- **Required pH range:** Acidic to neutral (pH 4–7). Corundum forms from acidic, silica-undersaturated fluids.
- **Required Eh range:** Variable — corundum itself is redox-inert (Al³⁺ is the only oxidation state). However, chromophores (Cr, Fe, Ti, V) require specific redox states.
- **Required O₂ range:** Not critical for corundum itself, but chromophore incorporation depends on oxidation state.

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No — corundum is a simple oxide with no volatile components.
- **Byproducts of nucleation:** Consumes Al from fluid, may locally deplete Al and allow Si to enter (producing rim of aluminosilicate).
- **Byproducts of dissolution/decomposition:** Insoluble. Corundum is extraordinarily stable and resistant to chemical weathering. Does not dissolve in acids (except hydrofluoric). May alter to micaceous minerals on surfaces in extreme weathering.

#### Growth Characteristics
- **Relative growth rate:** Moderate to slow. Much slower than quartz, calcite, or fluorite. High activation energy for Al diffusion.
- **Maximum crystal size in nature:** Up to 65 cm × 40 cm × 40 cm (152 kg record specimen from Myanmar). Synthetic boules can be much larger.
- **Typical crystal size in vugs:** Rare in vugs! Corundum is primarily a rock-forming mineral in metamorphic/igneous matrices, not a cavity-fill mineral. When found in vugs (pegmatite pockets), crystals are typically 1–5 cm.
- **Does growth rate change with temperature?** Yes — higher temperatures favor faster Al diffusion and larger crystals, but also increase competition from aluminosilicates. The "corundum window" is narrow: hot enough to mobilize Al, but not so hot that Si stays in solution (which would form silicates instead).
- **Competes with:**
  - **Spinel** (MgAl₂O₄) — when Mg is present
  - **Kyanite/andalusite/sillimanite** (Al₂SiO₅) — when Si is available
  - **Feldspars** — when Si + Na/K/Ca are present
  - **Muscovite** — when K + Si + H₂O are present

#### Stability
- **Breaks down in heat?** No — one of the most refractory minerals. Melts at 2044°C. No natural thermal decomposition.
- **Breaks down in light?** No.
- **Dissolves in water?** Insoluble.
- **Dissolves in acid?** Resistant to all acids except hydrofluoric (HF). Even aqua regia has no effect.
- **Oxidizes?** No — Al is already in its highest oxidation state (+3).
- **Dehydrates?** No — anhydrous mineral.
- **Radiation sensitivity:** Generally stable. Irradiation can induce color centers in some sapphires (yellow → colorless, or creating padparadscha-like colors artificially).

### Paragenesis
- **Forms AFTER:** In metamorphic environments, corundum forms after breakdown of hydrous aluminosilicates (clays → micas → kyanite/andalusite → corundum at highest grades). In pegmatites, it may form late-stage after most feldspar and quartz have crystallized.
- **Forms BEFORE:** Spinel may rim or replace corundum if Mg becomes available. In weathering, corundum outlasts virtually everything and concentrates in placers.
- **Commonly associated minerals:**
  - **Marble-hosted ruby:** Dolomite, calcite, phlogopite, spinel, pyrrhotite, graphite
  - **Pegmatite sapphire:** Feldspar (orthoclase, albite), muscovite, biotite, garnet, zircon, apatite, rutile, ilmenite
  - **Syenite corundum:** Nepheline, feldspar, sodalite, cancrinite, biotite, magnetite, apatite, zircon
  - **Emery:** Magnetite, hematite, hercynite, spinel
- **Zone:** Primary/hypogene — metamorphic (upper amphibolite to granulite facies) and igneous (pegmatite, syenite). Not a supergene mineral.
- **Geological environment:**
  - **Metamorphic marble** — world's finest rubies (Mogok, Myanmar; Mozambique; Afghanistan)
  - **Aluminous gneiss/schist** — metamorphic terranes (Sri Lanka, Madagascar)
  - **Pegmatites** — large crystals, often sapphire (Montana, USA; Madagascar)
  - **Nepheline syenite** — blue sapphires (Yogo Gulch, Montana; Garba Tula, Kenya)
  - **Placer deposits** — corundum's hardness makes it ultra-resistant; concentrates in alluvial gravels (Sri Lanka, Montana, Australia)

### Famous Localities
- **Mogok Stone Tract, Myanmar (Burma)** — THE classic ruby locality. "Pigeon's blood" red rubies from metamorphic marble. Also produces blue, pink, and star sapphires. Mining for ~800 years.
- **Kashmir, India** — The "velvet blue" sapphires from the Zanskar Range. Discovered 1881 after a landslide exposed a pegmatite. Production ceased ~1925. Considered the finest blue sapphire ever found — a soft, milky, cornflower blue from light scattering by fine inclusions.
- **Yogo Gulch, Montana, USA** — Unique "cornflower blue" sapphires from lamprophyre dikes cutting limestone. No heat treatment needed — naturally pure blue. Discovered 1895, still producing.
- **Sri Lanka (Ceylon)** — Alluvial sapphires for 2500+ years. Blue, pink, padparadscha, star sapphires. Ratnapura district is legendary.
- **Montepuez, Mozambique** — Major modern ruby source. Marble-hosted, similar geology to Mogok. Discovered 2009, now supplies ~50% of global rubies.
- **Madagascar** — Extensive deposits: Andranondambo (sapphire), Didy (ruby), Ilakaka (alluvial sapphire). Major producer since 1990s.
- **Pailin, Cambodia** — Blue sapphires from basalt-related alluvials. Mined since Khmer Empire era.
- **Australia** — Significant industrial corundum and some gem sapphire (Queensland, New South Wales).

### Fluorescence
- **Fluorescent under UV?** Variable
- **SW (255nm) color:** Ruby: strong red (Cr³⁺ luminescence). Blue sapphire: inert to weak red. Pink sapphire: moderate red. Yellow/green: usually inert.
- **MW (310nm) color:** Ruby: strong red. Others variable.
- **LW (365nm) color:** Ruby: strong red (diagnostic). Padparadscha: may show orange-red. Most sapphires: inert to weak.
- **Phosphorescent?** Rarely — some rubies show brief red afterglow.
- **Activator:** **Cr³⁺** is the primary activator. The R-line emission at ~694 nm (red) is characteristic and used to identify natural vs. synthetic ruby.
- **Quenched by:** Fe²⁺ suppresses fluorescence in blue sapphires (Fe + Ti dominate absorption instead). High Fe content = inert. Heat treatment can enhance or alter fluorescence.

### Flavor Text

> Corundum is patience incarnate. Aluminum and oxygen, the two most common elements in Earth's crust, join in trigonal symmetry at temperatures that would melt lesser minerals — yet corundum itself does not melt until 2044°C, far beyond anything the planet can offer. It is born in the silica-starved voids of marble, the aluminum-rich hearts of pegmatites, the strange alkaline syenites where silicon itself seems scarce. Ruby is chromium's fire trapped in aluminum's cage. Sapphire is the conversation between iron and titanium, two metals trading electrons across the crystal lattice to create a blue no single element could summon alone. And star sapphire? That is the crystal remembering the rutile needles that grew through it first — light striking three sets of parallel threads at 60 degrees, and the stone answering with a six-rayed star. Corundum does not form in ordinary vugs. It requires conditions so extreme that silica — the element that builds most of Earth's crust — must be absent. Where corundum grows, the rules are different. The stone that crowns the hardness scale at 9 does not compete. It endures.

### Simulator Implementation Notes

#### New Parameters Needed
- **Aluminum (Al)** — NEW broth variable. Required at high concentration for corundum. Currently NOT in the 30-trace list. Must be added to the game's trace element system.
- **Silica saturation flag** — Corundum requires silica-undersaturated conditions. If Si is above a threshold, corundum cannot nucleate (silicates outcompete it).

#### New Events Needed
- **Metamorphic marble pulse** — High Al, very low Si, moderate Cr/Fe/Ti, high temperature. Models ruby formation in marble.
- **Pegmatite late-stage** — After most feldspar and quartz have crystallized, remaining Al-rich fluid can form corundum.
- **Syenite intrusion** — Low-silica alkaline environment with available Al.

#### Nucleation Rule Pseudocode
```
IF broth.Al > 500 ppm
   AND broth.Si < 50 ppm (silica-undersaturated)
   AND temperature > 600°C
   AND temperature < 1000°C
   AND pH < 7 (acidic to neutral)
   AND total_nucleated < max_corundum (rare — max 2-3 per vug)
   AND (broth.Cr > 10 OR broth.Fe > 20 OR broth.Ti > 10 OR no_chromophore)
   → nucleate corundum
```

#### Growth Rule Pseudocode
```
IF crystal.species == "corundum"
   AND temperature > 500°C
   AND broth.Al > 100 ppm
   AND broth.Si < 100 ppm
   AND pH < 7.5
   → grow at rate SLOW (0.3× quartz baseline)
   
   // Color variant determination
   IF broth.Cr > broth.Fe AND broth.Cr > 15:
      → variant = "ruby" (red)
   ELSE IF broth.Fe > 30 AND broth.Ti > 15:
      → variant = "blue sapphire"
   ELSE IF broth.Fe > 20 AND broth.Cr < 5:
      → variant = "yellow sapphire"
   ELSE IF broth.Cr > 5 AND broth.Fe > 10:
      → variant = "padparadscha" (rare — pink-orange)
   ELSE IF broth.V > 10:
      → variant = "purple sapphire"
   ELSE:
      → variant = "colorless" (very rare)
   
   // Asterism check — requires Ti for rutile silk
   IF broth.Ti > 25 AND random() < 0.15:
      → add "star" modifier to variant
```

#### Habit Selection Logic
```
IF temperature > 800°C:
   → habit = "hexagonal_prismatic" (elongated)
ELIF temperature > 650°C:
   → habit = "bipyramidal" (steep double pyramid)
ELIF temperature > 500°C:
   → habit = "tabular" (flat plate, often twinned arrowhead)
ELSE:
   → habit = "granular" (massive)

// Twinning
IF habit == "tabular" AND random() < 0.4:
   → add "arrowhead_twin" (contact twin on basal pinacoid)
IF random() < 0.3:
   → add "polysynthetic_twinning" (rhombohedral parting striations)
```

#### Decomposition Products
- **None** — corundum does not decompose under any natural geological conditions. In the simulator, it is the ultimate survivor. If the vug survives to extreme temperatures (>1500°C, not realistic in game), corundum would simply persist while everything else melts.
- **Weathering/alteration:** In extreme tropical weathering, surface alteration to **muscovite** or **kaolinite** is possible (very slow). Not relevant for vug simulator timescales.

### Variants for Game

#### Variant 1: Ruby
- **What makes it different:** Red color from Cr³⁺ substitution for Al³⁺. Strong red fluorescence under UV. The most valuable colored gemstone by weight.
- **Conditions:** High Cr (>20 ppm), moderate Fe (<15 ppm to avoid dulling), temperature 700–900°C, marble or metamorphic environment.
- **Special:** Pigeon's blood red (Burma) vs. darker Mozambique ruby. Star ruby if Ti needles present.
- **Rarity:** 5/10 (common in corundum-locality scenarios, but corundum itself is rare)

#### Variant 2: Blue Sapphire
- **What makes it different:** Blue from Fe²⁺–Ti⁴⁺ intervalence charge transfer. No Cr. Often inert under UV (Fe quenches fluorescence).
- **Conditions:** High Fe (>30 ppm) + Ti (>15 ppm), low Cr (<5 ppm), temperature 600–900°C, pegmatite or syenite environment.
- **Special:** Kashmir-type (milky, velvety) vs. Sri Lankan (transparent, bright) vs. Australian (dark, inky). Yogo sapphires naturally pure blue without heat treatment.
- **Rarity:** 6/10

#### Variant 3: Padparadscha Sapphire
- **What makes it different:** The rarest corundum color — pink-orange, like a lotus blossom. Requires the delicate balance of Cr (pink) + Fe (orange/yellow) with neither dominating. Named from Sinhala "padma raga" (lotus color).
- **Conditions:** Moderate Cr (5–15 ppm) + moderate Fe (10–25 ppm), low Ti, temperature 600–800°C, Sri Lankan or Madagascar alluvial origin.
- **Special:** The most controversial color boundary in gemology. Some labs require 50% pink + 50% orange; others are more lenient.
- **Rarity:** 9/10 (among the rarest gem varieties)

#### Variant 4: Star Sapphire / Star Ruby
- **What makes it different:** Asterism — six-rayed star visible under point light source. Caused by oriented rutile (TiO₂) needle inclusions intersecting at 60°/120°. Requires dense, aligned "silk" and a domed cut (cabochon).
- **Conditions:** Very high Ti (>40 ppm) in broth during a specific growth phase, followed by continued corundum growth encapsulating the needles. Temperature drop helps align rutile exsolution.
- **Special:** 12-rayed stars exist (two sets of needles at different angles — extremely rare). "Linde star" synthetic sapphires are common in jewelry.
- **Rarity:** 7/10 for star sapphire, 8/10 for star ruby

#### Variant 5: Yellow / Green Sapphire
- **What makes it different:** Fe³⁺ alone creates yellow to greenish-yellow. No Cr, no Ti, or Ti only at low levels.
- **Conditions:** High Fe³⁺ (>40 ppm), very low Cr (<2 ppm), very low Ti (<10 ppm), oxidizing conditions.
- **Rarity:** 4/10

#### Variant 6: Colorless / White Sapphire
- **What makes it different:** Pure Al₂O₃ with no chromophores. Extremely rare in nature. Often used as diamond simulant in jewelry.
- **Conditions:** Very pure Al source with no Cr, Fe, Ti, V, Ni, Co. Requires extreme chemical purity rarely found in nature.
- **Rarity:** 9.5/10 (natural colorless corundum is exceptionally rare)

#### Variant 7: Emery
- **What makes it different:** Black, granular, massive corundum intimately mixed with magnetite, hematite, or hercynite. Industrial abrasive, not gem quality.
- **Conditions:** High Fe environment, metamorphic contact zone with iron-rich host rock, rapid cooling.
- **Rarity:** 3/10 (where corundum forms in iron-rich settings)

---

## Game Design Notes

### Why Corundum Matters for Vugg Simulator
Corundum is the **pinnacle mineral** — the hardest natural substance below diamond, the most valuable colored gemstone family, and a mineral that requires genuinely extreme conditions. Adding corundum gives players a "holy grail" target: the conditions are narrow, the competition from silicates is fierce, and success yields the most spectacular rewards.

### Simulator Challenge
Corundum forces players to think about **silica starvation**. In most scenarios, Si is abundant and corundum simply cannot form. To grow corundum, the player must either:
1. Choose a metamorphic marble scenario (naturally Si-poor)
2. Deplete Si early by growing quartz/feldspar first, then shift to Al-rich conditions
3. Use an alkaline igneous scenario (syenite/pegmatite) where Si is intrinsically low

This adds strategic depth: **preparatory mineral growth** to set up conditions for the crown jewel.

### Color Chemistry as Game Mechanic
Corundum's color system is the most sophisticated in the game:
- **Cr alone** → pink to red (ruby)
- **Fe + Ti** → blue (sapphire)
- **Cr + Fe balance** → padparadscha (the rarest)
- **Ti excess** → star potential
- **Fe alone** → yellow/green
- **Nothing** → colorless (ultimate rarity)

Players can "breed" colors by manipulating trace element ratios — a deeper chemistry layer than any other mineral.

### Rarity & Reward Structure
- Corundum should be the **rarest nucleation** in the game (max 1–2 crystals per vug, often 0)
- When it DOES nucleate, it should feel like an event
- Star variants should trigger a special visual effect in the game
- Padparadscha should be an **achievement** — the perfect trace-element balance

---

## References
1. Wikipedia — Corundum (general properties, varieties)
2. GeologyScience.com — Corundum Properties, Formation, Uses
3. Vectree.io — Metamorphic Petrogenesis of Corundum Deposits
4. GIA — Blue Sapphires from Mogok, Myanmar (Winter 2021)
5. International Gem Society — Ruby and Sapphire Origins
6. Lotus Gemology — Corundum Inclusions Crystal Registry
7. ScienceDirect — Solubility of Corundum in H₂O at High P-T (Rapp et al.)
8. MDPI Minerals — Spectroscopy and Microscopy of Corundum from Primary Deposits
9. GIA — Padparadscha: What's in a Name? (Crowningshield)
10. Flagstaff Mineral and Rock Club — Corundum: From Sapphires to Rubies (twinning discussion)
11. Ruby-Sapphire.com — Rutile Silk in Ruby & Sapphire
12. Springer — Elemental and Molecular Insight into Different Colors of Corundum Gemstones (2025)

---

## Implementation Checklist
- [ ] Add **Al** to broth trace element system (new variable)
- [ ] Add **silica saturation index** or Si threshold for corundum eligibility
- [ ] Write `supersaturation_corundum()` function
- [ ] Write `nucleate_corundum()` with color variant logic
- [ ] Write `grow_corundum()` — slow growth rate
- [ ] Add corundum crystal color derivation (Cr=red, Fe+Ti=blue, etc.)
- [ ] Add habit models: prismatic, bipyramidal, tabular, granular
- [ ] Add twinning: arrowhead, polysynthetic
- [ ] Add asterism detection (Ti silk + cabochon implication)
- [ ] Add to collector's view / epilogue
- [ ] Add to Record Groove crystal color system
- [ ] Consider: should corundum require a **special scenario** (marble, syenite) or can it grow in standard vugs?

---

*File written by 🪨✍️ for the Vugg Simulator mineral expansion project.*
*Research sources verified against multiple geological and gemological references.*
