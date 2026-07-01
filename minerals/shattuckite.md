# Research: Shattuckite — Cu₅(SiO₃)₄(OH)₂

## Species: Shattuckite

### Identity
- **Formula:** Cu₅(SiO₃)₄(OH)₂
- **Crystal system:** Orthorhombic
- **Mineral group:** Inosilicate (chain silicate)
- **Hardness (Mohs):** 3.5
- **Specific gravity:** 4.1 (rather heavy for a non-metallic mineral)
- **Cleavage:** Perfect along {010} and {100}
- **Fracture:** Uneven
- **Luster:** Dull to silky

### Color & Appearance
- **Typical color:** Dark azure blue to light blue, turquoise; may show color banding
- **Color causes:** Cu²⁺ in square planar and distorted octahedral coordination within the silicate chains
- **Transparency:** Translucent to opaque
- **Streak:** Blue
- **Notable visual features:** Strong pleochroism — X = very pale blue, Y = pale blue, Z = deep blue. Fibrous aggregates have a silky luster. Often found as botryoidal crusts or radial sprays of acicular crystals.

### Crystal Habits
- **Primary habit:** Spherulitic aggregates of acicular (needle-like) crystals; botryoidal masses
- **Common forms/faces:** Individual crystals are rare; typically fibrous aggregates
- **Twin laws:** Not commonly reported
- **Varieties:** None formally recognized; color varies from dark navy blue to bright turquoise depending on locality and associated minerals
- **Special morphologies:** 
  - Botryoidal (grape-like) masses and crusts
  - Radial sprays of elongated needle crystals
  - Pseudomorphs after malachite (at type locality — the Shattuck Mine)
  - Concentric circular clusters of spraying acicular crystals

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 20–100°C (supergene, low-temperature)
- **Optimal growth temperature:** 40–80°C
- **Decomposition temperature:** Not applicable at Earth-surface conditions; stable to ~250°C
- **Temperature-dependent habits:** Higher temperatures favor larger botryoidal masses; lower temperatures favor fibrous sprays and crusts

#### Chemistry Required
- **Required elements in broth:**
  - Cu: >40 ppm (oxidized to Cu²⁺)
  - SiO₂: >25 ppm (requires alkaline pH, like dioptase)
- **Optional/enhancing elements:**
  - Ca: may promote silicate mobilization
  - Al: traces may substitute into structure
- **Inhibiting elements:**
  - High Fe: competes for Si, favors iron oxides
  - Strongly acidic pH (<6): suppresses silica solubility
  - Very high carbonate: may favor malachite/azurite instead
- **Required pH range:** 7.5–9.5 (alkaline to mildly alkaline)
- **Required Eh range:** Oxidizing (+0.4 to +0.7 V)
- **Required O₂ range:** Moderate to high

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No significant byproducts
- **Byproducts of nucleation:** Consumes Cu²⁺ and SiO₂
- **Byproducts of dissolution/decomposition:** Dissolves in acid to release Cu²⁺ (toxic)

#### Growth Characteristics
- **Relative growth rate:** Moderate — faster than dioptase, slower than malachite
- **Maximum crystal size:** Individual crystals rarely exceed 1 cm; botryoidal masses up to 10+ cm
- **Typical crystal size in vugs:** 1–5 mm acicular crystals in radial sprays; botryoidal crusts 1–5 mm thick
- **Does growth rate change with temperature?** Yes — growth rate increases with temperature up to ~80°C
- **Competes with:** Dioptase (for Cu and Si), chrysocolla (for Cu and Si), malachite (for Cu), plancheite (similar chemistry)

#### Stability
- **Breaks down in heat?** Stable to ~250°C; gradual decomposition above
- **Breaks down in light?** No — color stable
- **Dissolves in water?** Very slightly; more soluble in acidic water
- **Dissolves in acid?** Yes — dissolves in HCl and H₂SO₄, releasing Cu²⁺
- **Oxidizes?** No — Cu already in +2 state
- **Dehydrates?** Minimal; the OH groups are structurally bound
- **Radiation sensitivity:** Not notably radiation-sensitive

### Paragenesis
- **Forms AFTER:** Primary copper sulfides oxidize to release Cu²⁺; silica becomes mobilized in alkaline conditions
- **Forms BEFORE:** May alter to chrysocolla or be coated by later malachite/azurite
- **Commonly associated minerals:** Malachite, chrysocolla, dioptase, plancheite, ajoite, quartz, calcite, bornite (as remnant primary mineral), azurite
- **Zone:** Supergene/oxidation zone — specifically silica-rich microenvironments within the oxidation zone
- **Geological environment:** Copper deposits in arid/semi-arid regions where silica is mobilized by alkaline groundwater. Type locality (Bisbee, Arizona) and Kaokoveld (Namibia) are classic.

### Famous Localities
- **Shattuck Mine, Bisbee, Arizona (USA):** Type locality (1915). Forms pseudomorphs after malachite — a mineral replacing another atom by atom while preserving the outward shape. The mine is the namesake.
- **Kaokoveld Plateau, Kunene Region, Namibia:** World-famous for vivid blue shattuckite with intense color. Radial sprays, spheres, botryoidal crusts. Often associated with malachite and quartz. The premier specimen locality.
- **New Cornelia Mine, Ajo, Arizona:** Polished specimens showing shattuckite with malachite — classic US material.
- **Tantara and M'Sesa, Katanga Province, Congo (DRC):** Significant African locality; specimens often associated with malachite, chrysocolla, and bornite.

### Fluorescence
- **Fluorescent under UV?** Generally no — non-fluorescent
- **SW (255nm) color:** None
- **MW (310nm) color:** None
- **LW (365nm) color:** None
- **Phosphorescent?** No
- **Activator:** N/A
- **Quenched by:** N/A

### Flavor Text
> Deep in the oxidation zone, where copper weathers out of its sulfide cage and meets silica in alkaline groundwater, a blue stranger appears. Shattuckite: named for an Arizona mine where it stole malachite's shape atom by atom, leaving the ghost of green in a body of blue. It grows in sprays and spheres — a copper sky frozen in stone.

### Simulator Implementation Notes
- **New parameters needed:** None beyond what dioptase requires (alkaline silica mobilization)
- **New events needed:** None beyond dioptase events
- **Nucleation rule pseudocode:**
```
IF Cu > 40 ppm AND SiO₂ > 25 ppm AND pH > 7.5 AND pH < 9.5 AND Eh > +0.4V AND T < 100°C:
    nucleate shattuckite
    // Note: pH window is slightly broader than dioptase, allowing earlier nucleation
```
- **Growth rule pseudocode:**
```
IF shattuckite_nucleated AND Cu > 25 ppm AND SiO₂ > 15 ppm AND pH > 7.0 AND Eh > +0.3V:
    grow at rate = 0.5 * base_rate  // Moderate grower
```
- **Habit selection logic:**
```
IF Cu:SiO₂_ratio > 2.0 AND slow_growth:
    habit = "botryoidal"  // Grape-like masses
ELSE IF Cu:SiO₂_ratio < 1.5:
    habit = "fibrous_spray"  // Radial acicular crystals
ELSE:
    habit = "crust"  // Massive coating

IF replacing_malachite:
    habit = "pseudomorph_after_malachite"
    // Rare but distinctive — preserves malachite's botryoidal shape
```
- **Decomposition products:** Amorphous silica + CuO at high temperature

### Variants for Game
- **Variant 1: Bisbee Blue** — Dark azure blue, from Arizona type locality; often pseudomorphic after malachite; nucleates at moderate pH (7.5–8.5)
- **Variant 2: Kaokoveld Spray** — Bright turquoise-blue, radial sprays of acicular crystals; requires stable, slow-growing conditions; the most visually striking variant
- **Variant 3: Congo Crust** — Botryoidal crusts with color banding (dark blue to turquoise); forms in more variable chemical conditions; commonly associated with malachite and chrysocolla

---

## Paragenetic Relationship with Dioptase

Shattuckite and dioptase are siblings in the copper oxidation zone — they require the same fundamental conditions (oxidized Cu + mobilized silica + alkaline pH) but differ in their Cu:Si ratio and crystal chemistry:

| Parameter | Dioptase | Shattuckite |
|-----------|----------|-------------|
| Formula | Cu₆Si₆O₁₈·6H₂O | Cu₅(SiO₃)₄(OH)₂ |
| Cu:Si ratio | 1:1 | 5:4 (1.25:1) |
| Crystal system | Trigonal | Orthorhombic |
| Structure type | Cyclosilicate (rings) | Inosilicate (chains) |
| Color | Emerald green | Azure blue |
| pH preference | 8.5–10.5 (strongly alkaline) | 7.5–9.5 (mildly alkaline) |
| Habit | Rhombohedral prisms | Botryoidal, fibrous |
| Hardness | 5 | 3.5 |

**Key insight:** Shattuckite can nucleate at slightly lower pH than dioptase, meaning it may appear earlier in the oxidation sequence when carbonate buffering is incomplete. As pH rises further (more complete buffering), dioptase becomes favored. In nature, the two often occur together — shattuckite as earlier, more massive crusts; dioptase as later, more crystalline drusy coatings.

**Simulator sequencing:**
```
Stage 1 (pH 7.5–8.5, moderate oxidation):
    Shattuckite nucleates first (broader pH tolerance)
    
Stage 2 (pH 8.5–10.5, strong oxidation):
    Dioptase nucleates (requires higher pH for silica mobilization)
    Both may coexist
    
Stage 3 (pH drops, acidity returns):
    Both dissolve; malachite/azurite may replace them
```

*Research date: 2026-06-06*
*Sources: Wikipedia, Mindat.org, Handbook of Mineralogy, Rocks & Minerals magazine (Bowell & Cook 2009)*
