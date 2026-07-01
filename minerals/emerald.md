# Species Research: Emerald

**Date:** 2026-05-24
**Source:** Vugg Simulator Mineral Expansion
**Status:** Complete — Blocked on Be + Al + Cr/V trace element addition
**Base mineral:** Beryl (Be₃Al₂Si₆O₁₈) — see `memory/research-beryl.md` for shared identity, crystal system, hardness, etc.

---

## Species: Emerald (Variety of Beryl)

### Identity
- **Formula:** Be₃Al₂Si₆O₁₈ with Cr³⁺ and/or V³⁺ substituting for Al³⁺
- **Crystal system:** Hexagonal (same as beryl)
- **Mineral group:** Cyclosilicate — beryl variety
- **Hardness (Mohs):** 7.5–8.0
- **Specific gravity:** 2.67–2.78 (slightly higher than pure beryl due to heavy chromophores)
- **Cleavage:** Imperfect on {0001} (basal)
- **Fracture:** Conchoidal to irregular; *emeralds are brittle and prone to chipping along fractures*
- **Luster:** Vitreous
- **Streak:** White
- **Optical:** Uniaxial (−); nω = 1.564–1.595, nε = 1.568–1.602; birefringence δ = 0.004–0.007

### Color & Appearance
- **Typical color:** Deep, vivid green — from bluish-green to slightly yellowish-green. "Grass green" to "forest green."
- **Color causes:**
  - **Primary:** Cr³⁺ substituting for Al³⁺ in octahedral sites — produces the pure green
  - **Secondary:** V³⁺ also substitutes for Al³⁺ and produces green; many emeralds contain both
  - **Modifying:** Fe²⁺/Fe³⁺ can add blue or yellow tones; Colombian emeralds are Fe-poor → pure green; Brazilian emeralds are Fe-rich → slightly bluish or yellowish
  - **Quantitative:** Muzo emeralds typically contain 0.1–0.5 wt% Cr₂O₃ and <0.2 wt% FeO. Zambian emeralds may have higher Fe, producing a bluer tone.
- **Transparency:** Transparent to translucent; most emeralds are heavily included ("jardin" — garden of inclusions)
- **Streak:** White
- **Notable visual features:**
  - **Jardin:** The mossy, garden-like inclusion pattern diagnostic of natural emeralds. Every emerald has them.
  - **Three-phase inclusions:** Liquid + gas + solid crystal (often halite or calcite) trapped in fluid pockets — classic for Colombian emeralds.
  - **Hexagonal prism habit:** Long prismatic crystals with flat basal pinacoid terminations, like all beryl.
  - **Trapiche emeralds:** Rare Colombian variety with six-rayed spokes of dark carbon impurities radiating from a central core.
  - **Doublets/triplets:** Common in lower-grade material — assembled stones with green cement or caps.

### Crystal Habits
- **Primary habit:** Long prismatic hexagonal crystals, striated parallel to c-axis. Terminated by flat basal pinacoid {0001}.
- **Common forms/faces:** {1010} prism, {0001} basal pinacoid, occasional {1120} or {1121} pyramidal faces.
- **Twin laws:** Very rare; contact twins on {0001} reported from a few localities.
- **Varieties:**
  - **Classic Colombian:** Deep pure green, Fe-poor, heavily included with jardin and three-phase inclusions.
  - **Zambian:** Slightly bluish-green, higher Fe, often cleaner (fewer inclusions), darker tone.
  - **Brazilian (Itabira/Santa Terezinha):** Yellowish-green to bluish-green, Fe- and V-rich, sometimes large crystals.
  - **Russian (Ural Mts):** Slightly yellowish-green, often small but intense color. Historic source (1830s–1980s).
  - **Trapiche:** Six-rayed black carbon spokes in Colombian emeralds. Cut as cabochons.
  - **Cat's-eye emerald:** Very rare; chatoyancy from parallel needle inclusions.
- **Special morphologies:**
  - Etched crystals common in pocket environments.
  - Massive, granular emerald (non-gem) in schist-hosted deposits.

### Formation Conditions (SIMULATOR PARAMETERS)

Emerald has **two distinct geological environments** that must be modeled separately:

#### Type I: Magmatic-Pegmatite / Hydrothermal Vein (Classic)
- **Temperature:** 300–650°C (hydrothermal vein deposition)
- **Optimal growth temperature:** 350–500°C for gem-quality
- **Required elements:** Be, Al, Si (for beryl) + Cr or V (for color)
- **pH:** Slightly acidic to neutral (5–7)
- **Eh:** Mildly oxidizing to neutral
- **Environment:** Fractures and breccias in granitic rocks; hydrothermal veins; skarn contacts; black shale-hosted systems (Colombia)

#### Type II: Schist-Hosted / Metamorphic-Hydrothermal (Colombian Model)
This is the **dominant commercial source** and the most geologically unusual:
- **Temperature:** 200–350°C (much lower than pegmatite beryl)
- **Optimal growth temperature:** ~250–300°C
- **Required elements in broth:**
  - **Be:** sourced from leached granitic rocks or evaporites (gypsum/anhydrite beds in Colombia)
  - **Cr/V:** sourced from **black carbonaceous shales** — the organic-rich host rock provides the chromophore
  - **Al:** from clays and shales
  - **Si:** from quartz veins and surrounding rock
- **Fluid chemistry:** Hot, saline, basinal brines (10–40 wt% NaCl eq.) that have scavenged Be from nearby evaporites and Cr/V from black shales
- **Required pH range:** Neutral to slightly alkaline (pH 6.5–8.5) — the black shale buffer keeps pH in this range
- **Required Eh range:** Reducing to weakly oxidizing — organic matter in shales maintains reducing conditions
- **Structural control:** Emeralds form in **extensional fractures and breccias** within the shale/limestone sequence, where fluids can circulate

**Key insight:** Colombian emeralds form from **sedimentary/hydrothermal fluids**, not pegmatite melts. The Be comes from evaporite leaching, the Cr/V from organic-rich shales, and the fluids are low-T basinal brines. This is radically different from aquamarine or morganite formation.

#### Chemistry Required (for Simulator)
- **Required elements in broth:**
  - Be: minimum ~10 ppm (as for all beryl)
  - Al: significant concentration
  - Si: abundant
  - **Cr: minimum ~50 ppm for color development** (or V: ~30 ppm)
- **Optional/enhancing elements:**
  - V: can substitute for Cr as green chromophore
  - Fe²⁺: adds blue tone (desirable in small amounts, excess muddies color)
  - Fe³⁺: adds yellow tone
  - Na, Cs, Li: channel-site occupants; alkali-rich emeralds are more inclusion-prone
- **Inhibiting elements:**
  - High Fe (>1000 ppm): suppresses pure green, adds blue/yellow, reduces transparency
  - High Ti: forms rutile instead of entering beryl
  - High Ca: incompatible with beryl structure
- **Required O₂ range:** Low to moderate

#### Secondary Chemistry Release
- **Byproducts of nucleation:** Consumes Be, Al, Si, Cr/V from fluid; depletes local Be concentration
- **Byproducts of dissolution:** At very high T (>800°C), decomposes to chrysoberyl (BeAl₂O₄) + quartz

#### Growth Characteristics
- **Relative growth rate:** Slow (same as beryl — 0.3× quartz baseline)
- **Maximum crystal size:** Exceptional. The **Empress of Ireland** emerald crystal: 5 cm wide, deep green, from Colombian Muzo mine. Crystals to 15+ cm known.
- **Typical crystal size in vugs:** 1–5 cm for gem quality; up to 20 cm for non-gem material
- **Growth rate vs. temperature:** Lower T (250–350°C) = slower growth but purer color and fewer inclusions. Higher T = faster but muddier.
- **Competes with:** Quartz (for Si), albite (for Al), calcite/dolomite (in Colombian system — carbonates often intergrow with emerald)

#### Stability
- **Breaks down in heat?** Yes, above ~800°C → chrysoberyl + quartz
- **Breaks down in light?** No — unlike maxixe (deep blue beryl), emerald color is stable
- **Dissolves in water?** Essentially insoluble
- **Dissolves in acid?** Insoluble in acids
- **Oxidizes?** No — Cr³⁺ and V³⁺ are stable in beryl structure
- **Dehydrates?** No water in structure
- **Radiation sensitivity:** Stable

### Paragenesis

#### Colombian (Schist-Hosted) Paragenesis
1. **Host rock:** Lower Cretaceous black carbonaceous shale and shaley limestone (Villeta Formation, 120–130 Ma)
2. **Fluid source:** Basinal brines heated by regional tectonics; leach Be from evaporites (gypsum/anhydrite), Cr/V from black shales
3. **Alteration:** Albitization, carbonatization, pyritization of host rock around veins
4. **Emerald precipitation:** In extensional fractures and breccias where hot, saline, Be-Cr-V-rich fluids cool and mix with carbonate-buffered fluids
5. **Associated minerals:**
   - Calcite, dolomite (carbonate veins)
   - Albite (albitized wall rock)
   - Pyrite (from shale sulfur)
   - Quartz (late veins)
   - Ankerite, siderite
   - Halite, gypsum (evaporite remnants)

#### Pegmatite/Hydrothermal Paragenesis
1. **Host rock:** Granite, granodiorite, or metamorphic rocks
2. **Fluid source:** Late-stage pegmatite fluids or hydrothermal solutions from cooling granite
3. **Emerald precipitation:** In fractures, miarolitic cavities, or along contacts with Cr/V-bearing wall rock (ultramafic rocks, chromium-rich schists)
4. **Associated minerals:**
   - Quartz, albite, K-feldspar (pegmatite minerals)
   - Muscovite, biotite
   - Tourmaline (schorl, dravite)
   - Topaz
   - Fluorite
   - Apatite
   - Cassiterite, wolframite (in Sn-W districts)
   - Chromite (if hosted in ultramafic rock — Russian Ural type)

**Key distinction:** Pegmatite emeralds require Cr/V in the wall rock (ultramafic inclusions, chrome-rich schists). Colombian emeralds get their Cr/V from the black shale itself.

### Famous Localities

#### Colombia (Western Emerald Belt)
- **Muzo Mine, Vasquez-Yacopí District:** The world's most famous emerald mine. Produces the deepest, purest green emeralds. Operated since pre-Columbian times; Spanish exploited it from 1537. Still active. Three-phase inclusions and jardin are diagnostic.
- **Coscuez Mine, Vasquez-Yacopí District:** Near Muzo; produces slightly lighter green, often cleaner stones. Historic rival to Muzo.
- **Chivor Mine, Eastern Emerald Belt:** Produces bluish-green emeralds in a different geological setting (older, more metamorphosed). Pre-Columbian mining; rediscovered 1896.
- **La Pita, La Marina, Peñas Blancas:** Modern Colombian mines with significant production.

#### Zambia
- **Kagem Mine, Kafubu River area:** World's largest emerald mine by volume. Produces bluish-green, often cleaner (fewer inclusions) stones. Significant modern production.

#### Brazil
- **Itabira, Minas Gerais:** Historic source; yellowish-green to bluish-green emeralds.
- **Santa Terezinha de Goiás:** Important modern source; crystals to 10+ cm.
- **Socotó, Bahia:** Produces emeralds in talc schist and black shale — geologically similar to Colombia.

#### Other Notable Sources
- **Russia (Ural Mountains):** Historic source (Malysheva Mine); small, intense yellowish-green crystals associated with chromite in ultramafic rock. Mostly depleted by 1990s.
- **Afghanistan (Panjshir Valley):** Produces fine emeralds, sometimes rivaling Colombian quality. In remote mountain valleys.
- **Pakistan (Swat Valley):** Small but high-quality production; similar to Afghanistan geologically.
- **Zimbabwe (Sandawana):** Small, intense green emeralds, often with high Cr. Historic but limited modern production.
- **Madagascar:** Occasional fine emeralds from pegmatite and metamorphic environments.

### Fluorescence
- **Fluorescent under UV?** Essentially **no**. Natural emerald is non-fluorescent under standard UV lamps.
- **SW (255nm):** None
- **MW (310nm):** None
- **LW (365nm):** None
- **Phosphorescent?** No
- **Important caveat:** **Fracture-filling materials** (oils, resins, polymers like Opticon) used to improve clarity MAY fluoresce. Cedar oil: weak yellowish. Synthetic polymers: may fluoresce more strongly. This is a gemological diagnostic — fluorescence from fillings, not from the emerald itself.
- **Activator:** N/A for natural emerald
- **Quenched by:** Fe²⁺ suppresses any potential luminescence (as in all beryl)

### Flavor Text

> **The Green That Seduced Empires**
>
> Emerald is beryl that has been touched by chromium — the same element that colors ruby, that makes blood look like blood, that turns an ordinary silicate into the most coveted green on Earth. But emerald's story is stranger than most gems because its two greatest sources formed in completely different ways.
>
> In Colombia, the world's finest emeralds grow in black shale — organic, carbon-rich mudstone from the Cretaceous ocean floor. The chromium that colors them does not come from deep magma or ultramafic rock. It comes from the shale itself: chromium locked in organic complexes, released by hot saline brines that also leached beryllium from ancient evaporites. The fluids were barely 300°C — cooler than a kitchen oven. The emeralds formed in fractures, in breccias, in the dark chemistry of sedimentary rock altered by tectonic heat. This is not how gemstones are supposed to form. It is how they did.
>
> The pre-Columbian Muzo people mined these emeralds before Columbus. The Spanish Empire built its treasury on them. The Mughal emperors of India inscribed them with sacred verse and wore them as talismans. Cleopatra's legendary emerald mines in Egypt — long exhausted, now ruins — were the only ancient source. Every emerald since has had to compete with that memory.
>
> In the vugg, emerald would be the rarest of the beryl variants. It requires not just Be, Al, and Si, but chromium or vanadium in sufficient concentration to override the colorless default. It would form at lower temperature than aquamarine or morganite — in the schist-hosted system, the cooler hydrothermal veins, or where pegmatite fluids have scavenged Cr from wall-rock ultramafics. Its inclusions — the jardin, the three-phase bubbles, the mossy fractures — would be visible in the simulator's crystal detail view, not as flaws but as fingerprints of formation. And like the real stone, it would be brittle: prone to chipping, demanding care, carrying the weight of five thousand years of human desire in every green face.

### Simulator Implementation Notes

**CRITICAL: Emerald requires a separate formation model from other beryl varieties.**

#### New parameters needed
- `Cr_ppm` — **new trace element** (not in current 30-element system)
- `V_ppm` — **new trace element** (not in current system)
- `Al_ppm` — **new trace element** (affects beryl, feldspar, many silicates)
- `Be_ppm` — **new trace element** (affects all beryl varieties)
- `black_shale_environment` — boolean flag for Colombian-style formation
- `evaporite_proximity` — boolean flag for Be source in sedimentary systems

#### New events needed
- `event_schist_hosted_emerald` — black shale + evaporite + basinal brine event (low T, neutral pH)
- `event_pegmatite_emerald` — pegmatite fluid + Cr/V wall rock (higher T, acidic pH)
- `event_fracture_breccia` — structural opening for emerald deposition

#### Nucleation rule pseudocode

**Type I — Colombian/Schist-Hosted:**
```
IF black_shale_environment = true
  AND evaporite_proximity = true
  AND trace_Be > 10 ppm
  AND trace_Al > 1000 ppm
  AND (trace_Cr > 50 ppm OR trace_V > 30 ppm)
  AND SiO2 > 400
  AND temperature BETWEEN 200 AND 350
  AND pH BETWEEN 6.5 AND 8.5
  AND fracture_or_breccia = true
THEN nucleate emerald
  color_intensity = MIN(trace_Cr / 50, trace_V / 30) * (1 - trace_Fe / 1000)
  IF trace_Fe > 500 THEN tone = bluish_green
  IF trace_Fe < 200 THEN tone = pure_green
```

**Type II — Pegmatite/Hydrothermal:**
```
IF pegmatite_environment = true
  AND trace_Be > 10 ppm
  AND trace_Al > 1000 ppm
  AND (trace_Cr > 50 ppm OR trace_V > 30 ppm)
  AND SiO2 > 400
  AND temperature BETWEEN 300 AND 650
  AND pH BETWEEN 5 AND 7
  AND (ultramafic_wall_rock = true OR chromite_present = true)
THEN nucleate emerald
```

#### Growth rule pseudocode
```
IF emerald exists
  AND trace_Be > 5 ppm
  AND (trace_Cr > 25 OR trace_V > 15)
  AND temperature < 700
THEN grow at rate = SLOW (0.25× quartz baseline)
  // slower than other beryl varieties due to restrictive chemistry
  inclusion_density = INVERSE(color_intensity)  // more color = more inclusions
  IF temperature > 500 THEN inclusion_density *= 1.5  // high T = more inclusions
```

#### Habit selection logic
- Schist-hosted, T < 350°C: smaller, more euhedral, heavily included (jardin)
- Pegmatite, T 400–550°C: larger, prismatic, may be less included
- Rapid cooling or fluid mixing: trapiche pattern (rare, Colombian only)

#### Decomposition products
- At T > 800°C: chrysoberyl (BeAl₂O₄) + quartz + fluid (same as beryl)

### Variants for Game

- **Variant 1: Colombian Classic (Pure Green)** — Deep vivid green, Fe < 200 ppm. Heavy jardin inclusions. Three-phase bubbles visible in detail view. Forms in black shale + evaporite system at 250–300°C. Highest gem value.
- **Variant 2: Zambian (Bluish-Green)** — Higher Fe (~500–1500 ppm), producing bluer tone. Often cleaner (fewer inclusions). Darker, more saturated. Forms in schist-hosted or pegmatite system with Fe-rich fluids.
- **Variant 3: Trapiche (Six-Rayed)** — Rare Colombian variant. Six black carbon spokes radiating from core. Requires specific fluid flow conditions and rapid nucleation in breccia. Cut as cabochon, not faceted. Unique visual in simulator.
- **Variant 4: Russian/Ural (Yellowish-Green)** — Small crystals associated with chromite in ultramafic rock. Slightly yellowish due to Fe³⁺. Intense color in small size. Historic source, depleted. Pegmatite/hydrothermal model.
- **Variant 5: Cat's-Eye (Chatoyant)** — Extremely rare. Parallel needle inclusions (tourmaline or actinolite) produce line of light across cabochon. Requires specific inclusion orientation.

---

## Paragenetic Context

Emerald occupies a unique position: it is the **only major gemstone whose primary source is sedimentary/hydrothermal, not magmatic.** This distinguishes it from:

| Mineral | Formation Environment | Key Difference from Emerald |
|---------|----------------------|---------------------------|
| Aquamarine | Pegmatite, hydrothermal | Fe²⁺ chromophore, no Cr/V needed, typically cleaner |
| Morganite | Pegmatite | Mn²⁺ chromophore, pink, same T range as aquamarine |
| Heliodor | Pegmatite | Fe³⁺ chromophore, yellow/gold, same T range |
| Ruby | Marble, basalt | Corundum structure, Cr³⁺ chromophore, much higher T (~800°C) |
| Tsavorite | Skarn, metamorphic | Grossular garnet, Cr³⁺/V³⁺, Ca-Al silicate, not beryl |
| Dioptase | Copper oxidation zone | Cyclosilicate like beryl, but Cu-colored, Cu-silicate, much lower T |

The Colombian emerald model is particularly significant because it demonstrates **sedimentary metal concentration** — rare elements (Be, Cr) scavenged from ordinary rocks by fluids, then precipitated in fractures. This is a different metallogenic model from the magmatic-hydrothermal systems that produce most other gems.

---

## Cross-References
- Base beryl research: `memory/research-beryl.md`
- Tourmaline (associated in pegmatites): `memory/research-tourmaline.md`
- Feldspar (associated): `memory/research-feldspar-vugg.md`
- Chromite (Cr source in Ural type): `memory/research-chromite.md`
- Calcite/dolomite (associated in Colombian system): `memory/research-calcite.md` (not yet written but in game)
- Pyrite (associated in Colombian system): `memory/research-pyrite.md`

---

## Implementation Blockers

| Blocker | Element/Feature | Notes |
|---------|----------------|-------|
| **Be not in trace system** | Beryllium | Required for all beryl varieties |
| **Al not in trace system** | Aluminum | Required for beryl, feldspar, many silicates |
| **Cr not in trace system** | Chromium | Required for emerald color (and ruby, tsavorite, chromian minerals) |
| **V not in trace system** | Vanadium | Alternative emerald chromophore |
| **Schist-hosted event** | Environment | New geological scenario: black shale + evaporite + basinal brine |
| **Fracture/breccia mechanic** | Structure | New void type: extensional fractures in shale |

**Estimated effort to implement:** High. Emerald is the most complex beryl variety because it requires two new trace elements (Cr, V), a new geological scenario (Colombian schist-hosted), and separate nucleation rules from other beryl varieties. However, it is also the most famous and valuable green gemstone — high payoff for implementation.

**Recommended priority:** Implement after base beryl system is in place (Be + Al added). Then add Cr/V and the Colombian scenario as a "premium" unlock.

---

## References
1. Wikipedia — Emerald. https://en.wikipedia.org/wiki/Emerald
2. Geology Science — Emerald Properties, Formation, Occurrence. https://geologyscience.com/minerals/silicates-minerals/emerald/
3. Pala International — The Emerald Deposits of Muzo, Colombia. http://www.palagems.com/emerald-colombia
4. GIA — Emerald Geographic Origin Determination. https://www.gia.edu/doc/WN19-emerald-geographic-origin-determination.pdf
5. MDPI Minerals — Emerald Deposits: A Review and Enhanced Classification (2019). https://mdpi.com/2075-163X/9/2/105/htm
6. ResearchGate — Formation of the Muzo Hydrothermal Emerald Deposit in Colombia. https://www.researchgate.net/publication/232753943
7. GemLab CDTEC — Chromium and Vanadium from Host Rock to Emerald. https://gemlabcdtec.com/wp-content/uploads/2023/07/Garcia-Toloza_22-Chromium-and-vanadium-from-host-rock-to-emerald.pdf
8. The Natural Emerald Company — Chemistry and Geology. https://emeralds.com/education/emerald-characteristics/chemistry-and-geology/
9. London, D. (2008). Pegmatites. *Mineralogical Association of Canada*, Special Publication 10.
10. Černý, P. (1991). Rare-element granitic pegmatites. *Geoscience Canada*, 18(2), 49–67.
11. Giuliani, G., et al. (2015). Emerald mineralization in Colombia: A review. *Ore Geology Reviews*, 75, 251–266.
12. Branquet, Y., et al. (1999). Fluid pressure and structural control of emerald mineralization in the Colombian cordillera. *Economic Geology*, 94, 77–88.

---

*"Emerald is proof that the most precious things can grow from the darkest mud. Black shale, hot brine, a fracture in the earth — and five thousand years later, the color of empires."*
