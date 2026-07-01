# Quartz Research — Vugg Simulator

**Date:** 2026-06-24
**Researcher:** 🪨✍️ (Vugg Simulator game expansion architect)
**Template:** `proposals/vugg-mineral-template.md`

---

## Species: Quartz

### Identity
- **Formula:** SiO₂ (silicon dioxide)
- **Crystal system:** α-quartz: Trigonal (class 32); β-quartz: Hexagonal (class 622)
- **Mineral group:** Tectosilicate / Framework silicate / Quartz group
- **Hardness (Mohs):** 7 (defining mineral for the scale)
- **Specific gravity:** 2.65 (2.59–2.63 in impure varieties)
- **Cleavage:** None
- **Fracture:** Conchoidal
- **Luster:** Vitreous; waxy to dull when massive
- **Streak:** White
- **Optical properties:** Uniaxial (+); nω = 1.543–1.545, nε = 1.552–1.554; birefringence +0.009
- **Special properties:** Piezoelectric, triboluminescent, chiral (optically active if not racemic)

### Color & Appearance
- **Typical color:** Colorless (rock crystal), but varies enormously: pink (rose quartz), purple (amethyst), yellow-orange (citrine), gray to black (smoky quartz), milky white, green (prasiolite), blue (rare, from Rayleigh scattering or inclusions)
- **Color causes:**
  - **Amethyst:** Fe³⁺ substituting for Si⁴⁺ in the lattice; irradiation creates [FeO₄]⁰ color centers. Requires Fe ≥ 1 ppm + natural/artificial irradiation.
  - **Smoky quartz:** Aluminum substitution with a hole trapped at an oxygen vacancy; radiation creates electron holes in the crystal lattice that absorb light broadly in the visible spectrum, producing brown-gray.
  - **Citrine:** Heat-treated amethyst (Fe³⁺ color centers altered by heat); natural citrine is rare and forms from Al³⁺ + Li⁺ charge-compensated substitution + heat.
  - **Rose quartz:** Microscopic inclusions of dumortierite, fibrous pink borosilicate, or Al³⁺/P⁵⁺ substitution + Ti⁴⁺; the color is not due to lattice defects but inclusions.
  - **Milky quartz:** Fluid inclusions (water, CO₂, NaCl) scatter light; not a chromophore but a scattering effect.
  - **Prasiolite:** Fe²⁺ or Al³⁺ substitution + heat treatment at ~500°C converts amethyst to green.
- **Transparency:** Transparent to nearly opaque (milky)
- **Notable visual features:** High birefringence produces rainbow-like internal reflections. Piezoelectricity means mechanical stress generates electrical charge (the basis of quartz watches and oscillators).

### Crystal Habits
- **Primary habit:** Six-sided prism terminating in a six-sided pyramid (rhombohedral terminations). The classic "quartz point."
- **Common forms/faces:** {10ī0} m-prism faces, {10ī1} r-rhombohedron (major), {01ī1} z-rhombohedron (minor), {11ī1} s-face (pyramid), {30ī1} x-face (trigonal trapezohedron — rare, indicates handedness)
- **Twin laws:**
  - **Dauphiné Law** — penetration twin, c-axis rotation of 60°; same handedness (R+R or L+L); very common; electrical twin (no piezoelectric effect under pressure along a-axis)
  - **Brazil Law** — contact/penetration twin on {11ī20}; combines left- and right-handed quartz (L+R); rarer
  - **Japan Law** — contact twin on {11ī22}; platy, heart-shaped, or square crystals; associated with rapid growth in miaroles; rare but distinctive
- **Varieties by habit:**
  - *Rock crystal* — clear, colorless, well-formed crystals
  - *Milky quartz* — massive white from fluid inclusions
  - *Chalcedony* — microcrystalline/cryptocrystalline, fibrous, often banded (agate)
  - *Opal* — amorphous hydrous silica (not true quartz but SiO₂·nH₂O)
  - *Aventurine* — quartz with reflective inclusions (mica, hematite) producing glitter
  - *Tiger's eye* — fibrous asbestos replaced by silica, chatoyant
- **Special morphologies:** Drusy coatings (fine crystals on cavity walls), scepters (secondary crystal overgrowth on earlier stem), elestial (layered, skeletal), faden (thread-quartz with healed fractures), enhydro (fluid-inclusion bubbles that move), skeletal/etched (aggressive fluids dissolve during growth)

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 50–900°C (extremely broad — quartz forms in almost every geological environment)
- **Optimal growth temperature:** 200–400°C for well-formed hydrothermal crystals; 600–900°C for pegmatitic
- **Decomposition temperature:** 1,713°C (β-cristobalite form); 1,670°C (β-tridymite form)
- **Temperature-dependent habits:**
  - <100°C: chalcedony, opal (amorphous/cryptocrystalline)
  - 100–300°C: low-temperature α-quartz, well-formed crystals, amethyst, smoky
  - 300–573°C: α-quartz, larger crystals, faster growth
  - 573°C: α→β transition (structural reorganization, volume change, potential microfracturing)
  - 573–900°C: β-quartz (hexagonal), pegmatitic crystals,高温形态不稳定于室温
  - >900°C: tridymite or cristobalite depending on pressure

#### Chemistry Required
- **Required elements in broth:** Si ≥ 100 ppm (as SiO₂(aq) or H₄SiO₄)
- **Optional/enhancing elements:**
  - Fe ≥ 1 ppm → amethyst (with irradiation)
  - Al ≥ 10 ppm → smoky quartz (with radiation)
  - Ti ≥ 1 ppm + Al → rose quartz color enhancement
  - Li ≥ 5 ppm + Al → natural citrine (charge-compensated substitution)
  - Mn ≥ 1 ppm → pink quartz (rare lattice substitution)
- **Inhibiting elements:** None truly inhibit quartz — it is the ultimate "sink" for silica in most geological systems. However:
  - Very high Na + K + Al at low T → feldspar competes for Si
  - Very high Ca + Mg + CO₃ at moderate T → carbonates compete
  - Very high Fe + S at low T + reducing → sulfides compete
- **Required pH range:** 4.0–10.0 (quartz is amphoteric; solubility is pH-independent below ~9, then rises sharply in strongly alkaline conditions as silicate anions form)
- **Required Eh range:** Any — quartz is redox-independent
- **Required O₂ range:** Any — quartz is oxidation-state independent

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No — quartz is a net consumer of silica from fluid
- **Byproducts of nucleation:** Depletion of SiO₂(aq) from fluid; if silica is removed rapidly from a high-pH fluid, pH may drop slightly
- **Byproducts of dissolution/decomposition:** At high T and high pH (>9), quartz dissolves as H₃SiO₄⁻ or H₂SiO₄²⁻, increasing pH. In acid (pH < 4), very slow dissolution as SiO₂(aq). Complete melting at >1,713°C releases no volatiles (unlike carbonates or sulfates).

#### Growth Characteristics
- **Relative growth rate:** Slow (0.3× excess rate, baseline in game); this reflects real quartz's slow growth — large crystals require thousands to millions of years
- **Maximum crystal size:** 12+ meters (single crystal) recorded from pegmatites; geodes to 2+ meters (Amethyst geodes of Artigas, Uruguay)
- **Typical crystal size in vugs:** 0.1–5 cm for hydrothermal vugs; 5–30 cm for miaroles and pockets
- **Does growth rate change with temperature?** Yes — retrograde solubility: quartz solubility decreases with decreasing temperature below ~300°C (Fournier & Potter 1982). This means quartz precipitates when hot silica-rich fluids cool.
- **Competes with:** Feldspar (for Si in Al-rich systems), chalcedony/opal (kinetically favored at low T), tridymite/cristobalite (at very high T)

#### Stability
- **Breaks down in heat?** Melts at 1,713°C to form silica glass; no decomposition products other than liquid SiO₂
- **Breaks down in light?** No — quartz is photostable. However, amethyst can fade with prolonged UV/sunlight exposure (Fe³⁺ color centers partially bleached).
- **Dissolves in water?** Extremely insoluble at STP (~6–10 ppm SiO₂ at 25°C); solubility rises to ~300 ppm at 100°C and ~1,000+ ppm at 300°C
- **Dissolves in acid?** Resistant to all acids except HF (hydrofluoric acid), which attacks silicates aggressively. This acid resistance is why quartz persists in oxidation zones while carbonates and sulfides dissolve.
- **Oxidizes?** No — Si is already in its highest oxidation state (+4)
- **Dehydrates?** No — anhydrous (except opal/chalcedony, which lose water on heating)
- **Radiation sensitivity:**
  - Clear quartz + Al + natural irradiation → smoky quartz
  - Clear quartz + Fe + irradiation → amethyst
  - Already-colored amethyst → color fading with prolonged UV
  - Rose quartz → color may fade with heat

### Paragenesis
- **Forms AFTER:** In most systems, quartz is a late-stage mineral because silica is highly soluble at high T and only precipitates on cooling. Exceptions: early quartz in pegmatites (immiscible silica melt), early chalcedony in volcanic rocks (rapid quenching).
- **Forms BEFORE:** Quartz is often one of the last major minerals to crystallize in hydrothermal veins. It may be overgrown by carbonates, sulfates, or late sulfides. In pegmatites, it crystallizes after feldspar and mica.
- **Commonly associated minerals:** Nearly everything — quartz is the universal companion. In vugs: calcite, dolomite, fluorite, sulfides (pyrite, galena, sphalerite), native elements, feldspars, micas, tourmaline, beryl, apatite, oxides (hematite, magnetite), uranium minerals.
- **Zone:** Forms in ALL zones — primary/hypogene (pegmatite, hydrothermal), supergene/oxidation (as resistant residuum), weathering (as sand and sandstone), metamorphic (quartzite), magmatic (granite, rhyolite).
- **Geological environment:** Every geological environment on Earth. Granite and rhyolite (magmatic), pegmatites (late magmatic), hydrothermal veins (epithermal to mesothermal), hot springs (geyserite), sedimentary (sandstone → quartzite), metamorphic (quartzite, schist), impact (shocked quartz, coesite, stishovite).

### Famous Localities
- **Herkimer County, New York (USA):** "Herkimer diamonds" — doubly terminated, exceptionally clear quartz crystals in dolostone vugs. The terminations form because crystals grow into cavities on both ends, not attached to matrix. Iconic American mineral.
- **Arkansas, USA (Hot Springs / Mount Ida):** Commercial quartz crystal mining. Single crystals to 1+ meter, clusters, clear to smoky. The only significant quartz deposit in North America mined for specimens.
- **Minas Gerais, Brazil:** World's largest producer of quartz specimens. Amethyst geodes from Artigas (Uruguay border), clear crystals from Diamantina, citrine, rose quartz. Brazil dominates the global quartz specimen market.
- **Artigas, Uruguay:** Giant amethyst geodes — the largest in the world, some 3+ meters tall. Deep purple color, basalt-hosted, formed in gas bubbles in flood basalt.
- **Madagascar:** Exceptional Japan-law twins, amethyst, rose quartz, and unique "candle quartz" (multiple secondary overgrowths creating a stacked appearance).
- **Swiss Alps (Grimsel, Gotthard, Val Giuv):** Classic alpine cleft quartz — smoky, clear, often with adularia, chlorite, hematite. Small but exquisite crystals from fissures in gneiss and granite.
- **Tibet / Himalayan region:** High-altitude quartz, often with inclusions (tourmaline, rutile, chlorite), prized for clarity and spiritual significance.
- **Smoky Quartz deposits:** Colorado (Pikes Peak region), Switzerland (Graubünden), Scotland (Cairngorms — national gemstone), Ukraine (Volyn region — giant crystals).

### Fluorescence
- **Fluorescent under UV?** Generally no — quartz itself is non-fluorescent. However:
  - **LW (365nm):** Some varieties show weak blue or white fluorescence due to trace Al³⁺ or defects.
  - **SW (255nm):** Rarely, weak blue-white fluorescence.
  - **Activator:** Al³⁺ substitution (replaces Si⁴⁺ with charge compensation by H⁺ or Li⁺) creates defect centers that may fluoresce.
  - **Quenched by:** Fe²⁺ quenches fluorescence in most quartz.
- **Phosphorescent?** Rarely; some irradiated quartz shows brief phosphorescence.
- **Special cases:**
  - "Tiffany stone" (opalized fluorite with quartz) may fluoresce from fluorite component.
  - Synthetic quartz grown in NaOH/Na₂CO₃ flux may show strong blue-white fluorescence.

### Flavor Text

> Quartz is the bones of the world — silica tetrahedra locked in eternal repetition, making up one-eighth of everything solid beneath your feet. It is so common that humans carved the first tools from it, so ancient that some grains have survived multiple rock cycles across billions of years, so pure that it carries the heartbeat of modern technology in every oscillator and watch. In the vug, it is patient beyond measure: a hot fluid saturated with silica cools by a single degree, and a few more tetrahedra click into place. Given time — geologic time — those clicks build cathedrals. The Greeks thought it was ice made permanent. They were closer than they knew: quartz is frozen light, frozen time, frozen fluid. It outlasts the mountains that contain it. When you find a perfect Herkimer diamond in a dolostone vug, you are holding a crystal that grew in silence while trilobites still swam the seas above.

### Simulator Implementation Notes
- **New parameters needed:** None — SiO₂ is already tracked as the base broth component. However, trace element tracking should note:
  - `trace_Fe` for amethyst potential
  - `trace_Al` for smoky quartz potential
  - `trace_Ti` + `trace_Al` for rose quartz
  - `trace_Li` + `trace_Al` for natural citrine
  - `radiation_exposure` (existing parameter) for color center activation
- **New events needed:**
  - `event_quartz_polymorph_transition` — at 573°C, α→β with volume change and potential microfracturing
  - `event_amethyst_irradiation` — if Fe present + radiation exposure, colorless quartz converts to amethyst
  - `event_smoky_radiation` — if Al present + radiation exposure, clear quartz converts to smoky
- **Nucleation rule pseudocode:**
```
IF fluid.SiO2 > saturation_concentration(temperature) AND temperature < 900
  AND sigma_quartz > 1.0
  AND (no_competing_silicate OR SiO2_excess > 2.0)
  → nucleate quartz
  
// saturation_concentrion(t) follows Fournier & Potter 1982 curve:
// log(SiO2_ppm) = 4.22 - 0.0019*t(C) for 25-300°C
// decreases below 300°C (retrograde solubility)
```
- **Growth rule pseudocode:**
```
IF sigma > 1.0:
  rate = 0.3 * (sigma - 1.0) * temperature_factor
  // temperature_factor: optimal at 200-400°C, slower at extremes
  
  // Color variety determination:
  IF trace_Fe > 1 AND radiation_exposure > threshold AND temperature < 200:
    color = amethyst_purple
  ELIF trace_Al > 10 AND radiation_exposure > threshold:
    color = smoky_gray
  ELIF trace_Ti > 1 AND trace_Al > 5:
    color = rose_pink
  ELIF trace_Li > 5 AND trace_Al > 10 AND temperature > 400:
    color = citrine_yellow
  ELIF fluid_inclusions > 0.1:
    color = milky_white
  ELSE:
    color = clear_rock_crystal
  
  // Habit selection:
  IF growth_rate > fast AND temperature > 500:
    habit = prismatic_stubby
  ELIF growth_rate > fast AND temperature < 200:
    habit = chalcedony_fibrous  // kinetic override
  ELIF excess > 2.0:
    habit = skeletal_elestial
  ELIF nearby_cavity_wall:
    habit = drusy_coating
  ELSE:
    habit = hexagonal_prism_pyramid
    
  debit SiO2:1 from fluid
```
- **Habit selection logic:**
  - High T + moderate σ → stubby prismatic (pegmatitic)
  - Low T + high σ → chalcedony/opal (kinetically favored cryptocrystalline)
  - Moderate T + moderate σ → classic hexagonal prism + pyramid (hydrothermal)
  - Very high σ + any T → skeletal/elestial (fast growth outpaces face development)
  - Cavity wall proximity → drusy coating
  - Twin probability: Dauphiné 15%, Brazil 4%, Japan Law 0.5% (only in miarole/pocket environments)
- **Decomposition products:** Melts at 1,713°C → silica glass (no other products). In game, thermal destruction above 1,700°C returns SiO₂ to fluid.

### Variants for Game
- **Variant 1 — Rock Crystal:** Clear, colorless, transparent. The "ideal" quartz. Formed in clean, low-trace-element fluids. Highest "purity" rating in collector's view.
- **Variant 2 — Amethyst:** Purple to violet, Fe³⁺ color centers from irradiation. Requires: Fe ≥ 1 ppm + radiation exposure + T < 200°C. Famous from Artigas geodes, Thunder Bay, Siberia. Can fade in sunlight.
- **Variant 3 — Smoky Quartz:** Brown to black-gray, Al³⁺ + radiation color centers. Requires: Al ≥ 10 ppm + radiation exposure. Famous from Cairngorms (Scotland), Pikes Peak, Swiss Alps. Natural radioactivity from nearby U/Th minerals is the typical radiation source.
- **Variant 4 — Citrine:** Yellow to orange, from heat-treated amethyst or natural Li+Al substitution. Natural citrine is rare; most commercial citrine is heat-treated amethyst. In game: can appear from amethyst that experiences T > 400°C event.
- **Variant 5 — Milky Quartz:** White, translucent, from abundant fluid inclusions. Lower value but common. Forms where silica-saturated fluids cool rapidly, trapping water/CO₂ inclusions.
- **Variant 6 — Rose Quartz:** Pink, from dumortierite inclusions or Ti+Al substitution. Requires: Ti ≥ 1 ppm + Al ≥ 5 ppm. Famous from Minas Gerais, Madagascar, South Dakota.
- **Variant 7 — Herkimer Diamond:** Doubly terminated, water-clear, from low-T dolostone vugs. Special habit: no attachment point, both ends terminated. Requires: T < 100°C + SiO₂ saturation in carbonate-hosted vug.
- **Variant 8 — Scepter Quartz:** Secondary crystal overgrowth on earlier stem, creating a "scepter" shape. Requires: pause in growth (fluid chemistry change or temperature drop) followed by resumption.
- **Variant 9 — Enhydro Quartz:** Contains moving fluid inclusion bubble. Requires: rapid sealing of cavity during growth, trapping a water/gas pocket inside the crystal.
- **Variant 10 — Faden Quartz:** Tabular crystals with a white "thread" (healed fracture) running through them. Requires: crystal growth interrupted by fracture, then healed and overgrown.

### Polymorphs and Related SiO₂ Forms
Quartz is one of several SiO₂ polymorphs; the simulator currently tracks α-quartz. Future expansion could include:

| Phase | Crystal System | Stability Range | Occurrence |
|-------|---------------|-----------------|------------|
| α-Quartz | Trigonal | <573°C at ambient P | The only stable form at Earth's surface |
| β-Quartz | Hexagonal | 573–870°C | High-T form; inverts to α on cooling |
| β-Tridymite | Orthorhombic/Hexagonal | 870–1,470°C | Volcanic rocks, silica bricks |
| β-Cristobalite | Tetragonal/Cubic | 1,470–1,713°C | Volcanic rocks, high-T ceramics |
| Opal | Amorphous | <100°C (metastable) | Hot spring deposits, diatomaceous earth |
| Chalcedony | Microcrystalline | <250°C (metastable) | Agate, jasper, chert |
| Coesite | Monoclinic | High pressure (>2 GPa) | Impact structures, UHP metamorphism |
| Stishovite | Tetragonal | Very high pressure (>9 GPa) | Meteorite impact sites only |

### Cross-References
- Vugg Simulator mineral template: `proposals/vugg-mineral-template.md`
- Quartz engine: `js/61-engines-silicate.ts` (or equivalent — quartz is the base mineral)
- Feldspar research: `memory/research-feldspar-vugg.md` (competes for Si in Al-rich systems)
- Amethyst color mechanism: cross-reference with `memory/research-amazonite.md` (Pb in feldspar) and `memory/research-prasiolite.md` (green quartz)
- Silica solubility: Fournier & Potter (1982) — the definitive quartz solubility curve
- Alpine cleft scenario: referenced in TODO.md as "Feldspar Phase 3 — Alpine cleft scenario"
- Chalcedony/opal: not yet in game as distinct minerals; opal is hydrous SiO₂·nH₂O
- Herkimer diamonds: classic American locality, could be a special scenario or achievement
