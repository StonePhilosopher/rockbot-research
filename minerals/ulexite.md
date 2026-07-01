# Mineral Species — Ulexite

## Species: Ulexite

### Identity
- **Formula:** NaCaB₅O₆(OH)₆·5H₂O
- **Crystal system:** Triclinic (1)
- **Mineral group:** Borate (nesoborate subgroup)
- **Hardness (Mohs):** 2.5
- **Specific gravity:** 1.95–1.96 (very light — floats in heavy liquids)
- **Cleavage:** Perfect on {010}, good on {110}, poor on {1̄10}
- **Fracture:** Uneven
- **Luster:** Vitreous; silky or satiny in fibrous aggregates

### Color & Appearance
- **Typical color:** Colorless to white; occasionally pale grey or faint yellow
- **Color causes:** Pure ulexite is colorless; fibrous aggregates appear white due to light scattering; rare yellow tones from iron oxide staining
- **Transparency:** Transparent to opaque (individual crystals transparent, fibrous masses opaque)
- **Streak:** White
- **Notable visual features:** The "TV rock" — parallel fibrous masses act as natural fiber-optic light pipes, transmitting an image from the bottom surface to the top surface of a polished slab. Rounded, cotton-ball-like aggregates with silky sheen. Feels warm to the touch (low thermal conductivity of fibrous structure). Very light — one of the least dense common minerals.

### Crystal Habits
- **Primary habit:** Acicular to fibrous; rounded crystalline masses ("cotton balls")
- **Common forms/faces:** Fibrous aggregates, nodules, thin crusts; individual crystals are tiny acicular prisms
- **Twin laws:** Polysynthetic twinning on {010} and {100}
- **Varieties:** "TV rock" — polished specimens showing fiber-optic effect; massive nodular ulexite
- **Special morphologies:** Felted aggregates, spherical nodules ("cotton balls"), fibrous crusts, fracture fillings

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 15–40°C (evaporite basin, alkaline lacustrine)
- **Optimal growth temperature:** 25–35°C
- **Decomposition temperature:** ~150–200°C (dehydration)
- **Temperature-dependent habits:** Cooler → more delicate fibrous aggregates; warmer → more compact nodules

#### Chemistry Required
- **Required elements in broth:** Na⁺, Ca²⁺, B (as borate), H₂O
- **Optional/enhancing elements:** High Na/Ca ratio favors ulexite over colemanite; trace Sr may substitute for Ca
- **Inhibiting elements:** High sulfate (→ gypsum/anhydrite, competes for Ca); high K⁺ (→ kernite if concentrated); high Mg²⁺ (→ kieserite)
- **Required pH range:** 8.5–10.5 (strongly alkaline — borate stability requires high pH)
- **Required Eh range:** Not redox-sensitive
- **Required O₂ range:** Irrelevant (non-redox)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No direct byproducts
- **Byproducts of nucleation:** Consumes Na⁺ + Ca²⁺ + borate from brine
- **Byproducts of dissolution/decomposition:** Dissolves in water, releasing Na⁺ + Ca²⁺ + borate ions; dehydration releases H₂O

#### Growth Characteristics
- **Relative growth rate:** Moderate — requires evaporative concentration but nucleates readily in borate-rich brine
- **Maximum crystal size:** Individual acicular crystals to 1 cm; nodules to 10+ cm; fibrous masses can be extensive
- **Typical crystal size in vugs:** Fibrous crusts 1–5 mm; nodules 1–3 cm
- **Does growth rate change with temperature?** Warmer = faster evaporation = faster growth; cooler = more delicate fibers
- **Competes with:** Borax (earlier stage, more Na), colemanite (later stage, more Ca), kernite (high K variant)

#### Stability
- **Breaks down in heat?** Dehydrates at ~150–200°C
- **Breaks down in light?** No
- **Dissolves in water?** Slightly soluble in cold water; more soluble in hot water
- **Dissolves in acid?** Yes — soluble in HCl with decomposition
- **Oxidizes?** No
- **Dehydrates?** Yes — loses water of crystallization at elevated temperature
- **Radiation sensitivity:** Not documented

### Paragenesis
- **Forms AFTER:** Borax (Na₂B₄O₇·10H₂O) — ulexite represents the next stage as Ca enters the brine system
- **Forms BEFORE:** Colemanite (as brine continues to concentrate and Ca/Na ratio rises), howlite (similar chemistry, different structure)
- **Commonly associated minerals:** Borax, colemanite, kernite, howlite, hydroboracite, gypsum, calcite, halite
- **Zone:** Evaporite (mid-stage), alkaline lacustrine
- **Geological environment:** Arid-climate alkaline playa lakes fed by geothermal/volcanic borate springs; interlayered borate deposits (Death Valley, Boron, Salar de Uyuni-type)

### Famous Localities
- **Classic locality 1:** Boron (Kramer district), Kern County, California, USA — world-class borate district, massive ulexite in extensive borate beds
- **Classic locality 2:** Salar de Uyuni, Potosí, Bolivia — evaporite basin, ulexite in surface crusts ("cotton balls" on salt flats)
- **Classic locality 3:** Inder borate deposit, Atyrau Region, Kazakhstan — significant borate reserves
- **Notable specimens:** Polished "TV rock" slabs from Boron showing perfect fiber-optic image transmission; white cotton-ball nodules from Salar de Uyuni; massive fibrous aggregates from Death Valley

### Fluorescence
- **Fluorescent under UV?** Yes — variable depending on impurities
- **SW (255nm) color:** Yellow, greenish yellow, or cream
- **MW (310nm) color:** Yellow to white
- **LW (365nm) color:** Cream to white (generally weaker than SW)
- **Phosphorescent?** Weak phosphorescence reported in some specimens
- **Activator:** Trace Mn²⁺, organic inclusions, or intrinsic borate lattice fluorescence; exact activator varies by locality
- **Quenched by:** Iron oxide staining reduces fluorescence intensity

### Flavor Text
> Ulexite is the reason children in rock shops press their faces against a white stone and giggle. Polished into a flat slab, it acts as a natural fiber-optic array: an image placed underneath appears on top, transmitted through thousands of parallel borate fibers like light through a bundle of glass strands. The mineral does this without anyone cutting it — the fibers grew that way, aligned by the evaporative rhythms of an ancient lake. Collectors call it "TV rock," but the name undersells it. A television is technology. Ulexite is geology that accidentally discovered optics 30 million years before humans did. It forms in alkaline playa lakes where borate-rich brine concentrates past the point of borax, pulling calcium into the crystallization sequence. The result is white, silky, fibrous, feather-light — one of the least dense minerals you can hold and still call a rock. On the Salar de Uyuni, it forms "cotton balls" on the salt crust, scattered like discarded stuffing across the world's largest mirror. In Boron, California, it lies in thick beds beneath the desert, the mineral layer that built an industry. It is not glamorous. It is white and soft and looks like insulation. But it taught light how to bend through stone.

### Simulator Implementation Notes
- **New parameters needed:** Boron (B) as trace element; brine Na/Ca ratio; evaporite stage tracker
- **New events needed:** Evaporite sequence progression: borax → ulexite → colemanite; fiber-optic property detection (special visual trait)
- **Nucleation rule pseudocode:**
```
IF scenario == "alkaline_lake" OR scenario == "evaporite_basin"
  AND trace_B > very_high AND trace_Na > high AND trace_Ca > moderate
  AND pH > 8.5
  AND borax_already_present == true (mid-stage evaporite)
  AND temperature > 15 AND temperature < 40
  → nucleate ulexite (max 3 nuclei, fibrous/nodular habit)
```
- **Growth rule pseudocode:**
```
IF σ_ulexite > 1.0 AND vug_fill < 1.0
  → grow at moderate rate
  habit = "fibrous_aggregate" (default) | "nodular" (if high supersaturation) | "crust" (if surface growth)
```
- **Habit selection logic:** Default fibrous aggregate (cotton-ball habit). High supersaturation + open space → rounded nodules. Surface evaporation → crusts. Special trait: if polished slab form is "prepared" in game, fiber-optic effect visible.
- **Decomposition products:** Dissolves → Na⁺ + Ca²⁺ + borate back to fluid; dehydration → anhydrous borate residue + H₂O

### Variants for Game
- **Variant 1:** Standard ulexite — white fibrous "cotton ball" nodules (typical evaporite)
- **Variant 2:** TV rock — polished flat slab showing fiber-optic image transmission (special prepared form, higher collector value)
- **Variant 3:** Salar crust — surface-crystallized fibrous aggregates from salt flat margins, intergrown with halite and gypsum
