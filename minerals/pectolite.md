# Pectolite

## Identity
- **Formula:** NaCa₂Si₃O₈(OH) (simplified from NaCa₂Si₃O₉(OH), IMA accepts both)
- **Crystal system:** Triclinic
- **Mineral group:** Inosilicate (chain silicate) — wollastonite group
- **Hardness (Mohs):** 4.5–5
- **Specific gravity:** 2.7–2.9
- **Cleavage:** Perfect on {100} and {001}
- **Fracture:** Uneven, splintery
- **Luster:** Silky to subvitreous

### Color & Appearance
- **Typical color:** White, grayish, colorless; yellowish when iron-stained
- **Color causes:** Larimar variety = blue from copper substitution (Cu²⁺ replacing Ca); greenish tints from trace Fe or Mn
- **Transparency:** Translucent to opaque
- **Streak:** White
- **Notable visual features:** Extremely slender, elongated acicular crystals radiating from a central point — "sea urchin" or "shaving brush" habit. Fibrous and delicate; thin splinters break easily on handling.

### Crystal Habits
- **Primary habit:** Acicular, radiating fibrous aggregates; rarely tabular single crystals to 15 cm
- **Common forms/faces:** Elongated prismatic splinters protruding from dense radiating masses; flat single blades (rare, select localities)
- **Twin laws:** Twin axis [010] with composition plane [100], common
- **Varieties:**
  - **Larimar:** blue variety from Dominican Republic, Cu-substituted, formed in volcanic vesicles
  - **Dense / compact:** mammillary and globular forms
- **Special morphologies:** Radiating balls, tufts, vein fillings, spheroidal aggregates, massive

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 50–250°C (low-temperature hydrothermal)
- **Optimal growth temperature:** 100–200°C
- **Decomposition temperature:** ~800°C (dehydration, structural breakdown)
- **Temperature-dependent habits:** Lower T favors acicular radiating forms; higher T favors more compact aggregates

#### Chemistry Required
- **Required elements in broth:** Na (≥500 ppm), Ca (≥1000 ppm), Si (≥2000 ppm)
- **Optional/enhancing elements:** Cu (for larimar blue color), Mn (pinkish tint), Fe (yellowish)
- **Inhibiting elements:** High Al suppresses pectolite in favor of zeolites or prehnite; high Mg may divert to serpentine
- **Required pH range:** 7.5–9.5 (mildly alkaline)
- **Required Eh range:** Near-neutral to slightly reducing
- **Required O₂ range:** Low — anoxic to mildly oxic

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No significant release
- **Byproducts of nucleation:** Consumes Na⁺, Ca²⁺, SiO₂(aq), and OH⁻ from fluid
- **Byproducts of dissolution/decomposition:** Releases Na⁺, Ca²⁺, silicic acid, and OH⁻ back to fluid upon dissolution

#### Growth Characteristics
- **Relative growth rate:** Moderate — faster than wollastonite in low-T veins, slower than zeolites
- **Maximum crystal size in nature:** 15 cm (exceptional acicular crystals)
- **Typical crystal size in vugs:** 1–5 mm acicular radiating sprays; up to 2 cm mammillary masses
- **Does growth rate change with temperature?** Yes — retrograde solubility not pronounced; growth slows significantly below 80°C
- **Competes with:** Zeolites (same Na-Ca-Si-OH environment), natrolite, thomsonite, calcite

#### Stability
- **Breaks down in heat?** Yes, >800°C dehydration; recrystallizes to wollastonite + quartz + Na-silicate at very high T
- **Breaks down in light?** No — stable under light
- **Dissolves in water?** Very low solubility; slightly soluble in acidic conditions
- **Dissolves in acid?** Yes — soluble in HCl with effervescence (Ca component); attacks silicate framework
- **Oxidizes?** No — stable to oxidation; Cu-substituted varieties (larimar) may show surface tarnish
- **Dehydrates?** Yes, above ~800°C
- **Radiation sensitivity:** No known effect

### Paragenesis
- **Forms AFTER:** Basalt cooling, vesicle opening; often after earlier zeolites (natrolite, thomsonite)
- **Forms BEFORE:** Later calcite, quartz, or secondary copper minerals in same vugs
- **Commonly associated minerals:** Natrolite, thomsonite, calcite, datolite, prehnite, zeolites, copper minerals (in larimar localities)
- **Zone:** Low-temperature hydrothermal / zeolite facies; also in alpine-type veins and basalt vesicles
- **Geological environment:** Basalt vugs and vesicles (classic), low-T hydrothermal veins, alpine clefts, skarns (rare)

### Famous Localities
- **Jeffrey Mine, Asbestos, Quebec, Canada:** World-class radiating acicular sprays in pectolite pockets; the locality that defines the species for collectors. Crystals to 15 cm, dense white radiating balls.
- **Paterson / Great Notch, New Jersey, USA:** Classic US locality — radiating white sprays in basalt; often associated with prehnite and datolite. Old quarries now largely overgrown.
- **Sierra de Bahoruco, Dominican Republic:** Larimar — the only locality for blue pectolite. Formed in Miocene volcanic vesicles; Cu-substituted, sky-blue to green-blue, cut as gemstone.
- **Notable specimens:** Larimar cabochons can exceed 10 cm; Jeffrey Mine "shaving brush" specimens are museum-grade.

### Fluorescence
- **Fluorescent under UV?** Yes
- **SW (255nm) color:** Pink to orange-pink
- **MW (310nm) color:** Orange-pink
- **LW (365nm) color:** Orange-pink to yellowish
- **Phosphorescent?** Weak to moderate
- **Activator:** Mn²⁺ (trace substitution), possibly REE
- **Quenched by:** Fe²⁺ (in iron-rich specimens)

### Flavor Text

> Pectolite grows like a frozen explosion — thousands of needle-thin crystals bursting outward from a single point, each one a thread of calcium, sodium, and silica spun in the dark. The classic white "shaving brush" sprays from Jeffrey Mine look like something a sea creature might have built. But the real story is larimar: the same mineral, shot through with copper's blue breath, hidden in Dominican volcanic vesicles until 1974. A stone that spent ten million years as a secret, then became a jewelry counter star. The vug doesn't care about markets. It just grows what the chemistry demands.

### Simulator Implementation Notes
- **New parameters needed:** None — uses existing Na, Ca, Si, OH system
- **New events needed:** `event_pectolite_vein` — low-T hydrothermal pulse in basaltic host
- **Nucleation rule pseudocode:**
```
IF temperature < 250°C
AND Na >= 500 ppm
AND Ca >= 1000 ppm
AND Si >= 2000 ppm
AND pH >= 7.5 AND pH <= 9.5
AND basalt_host == true
→ nucleate pectolite (acicular habit)
```
- **Growth rule pseudocode:**
```
IF temperature < 200°C AND temperature > 50°C
AND Na, Ca, Si available
AND no high-Al competition (suppress if Al > 2000 ppm)
→ grow at rate 3 (moderate, acicular radial)
IF Cu >= 100 ppm → chance for larimar variant (blue color)
```
- **Habit selection logic:** Acicular radiating default; mammillary/globular if growth is slow and space is confined; tabular rare (special localities flag)
- **Decomposition products:** Above 800°C → wollastonite + quartz + Na-silicate melt; in acid → dissolved Ca²⁺ + silicic acid + Na⁺

### Variants for Game
- **Variant 1: White Spray** — standard pectolite, acicular radiating, white/gray. Most common.
- **Variant 2: Larimar** — Cu-substituted blue variety, only in volcanic vesicles with Cu >100 ppm. Higher value.
- **Variant 3: Compact Mass** — mammillary/globular, dense and tough. Slower growth, confined space.

---

**Research date:** 2026-06-08
**Blocker:** None — Na, Ca, Si, OH all in trace system. Cu for larimar variant already tracked.
**Notes:** Builder-added species. Wollastonite group member. Larimar is a Cu-substituted variety unique to Dominican Republic volcanic rocks. Fluorescence is distinctive pink-orange. Acicular habit makes it visually striking in-game.
