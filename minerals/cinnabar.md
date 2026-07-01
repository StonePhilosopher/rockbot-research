# Cinnabar + Metacinnabar Research — Vugg Simulator

**Date:** 2026-06-13
**Researcher:** 🪨✍️ (Vugg Simulator game expansion architect)
**Template:** `proposals/vugg-mineral-template.md`

---

## CINNABAR — α-HgS

### Identity
- **Formula:** HgS (mercury(II) sulfide)
- **Crystal system:** Trigonal (hexagonal scalenohedral)
- **Mineral group:** Sulfide (cinnabar group)
- **Hardness (Mohs):** 2.0–2.5
- **Specific gravity:** 8.176 (exceptionally heavy for a non-metallic mineral)
- **Cleavage:** Prismatic {1010}, perfect
- **Fracture:** Uneven to subconchoidal
- **Luster:** Adamantine to dull

### Color & Appearance
- **Typical color:** Cochineal-red to bright scarlet, brick-red, occasionally brownish-red or lead-gray when impure
- **Color causes:** Charge-transfer transition between Hg²⁺ and S²⁻ ions; the Hg–S bond length and coordination environment produce the characteristic red absorption edge in the visible spectrum
- **Transparency:** Transparent in thin pieces; translucent to opaque in thicker masses
- **Streak:** Scarlet red (diagnostic)
- **Notable visual features:** Highest refractive index of any common mineral (mean n ≈ 3.08, birefringence δ = 0.351); second only to diamond in optical density among gemstones. Crystals exhibit strong internal reflections and adamantine luster.

### Crystal Habits
- **Primary habit:** Rhombohedral to tabular crystals; more commonly massive, granular, earthy, or as incrustations
- **Common forms/faces:** {1010} prisms, {0001} basal pinacoid; rhombohedra common
- **Twin laws:** Simple contact twins on {0001} (basal pinacoid); twinning relatively common
- **Varieties:**
  - *Hepatic cinnabar* — impure brownish variety from Idrija, Slovenia, mixed with bituminous and earthy matter
  - *Stalactitic cinnabar* — forms dripstone-like encrustations in hot spring deposits
  - *Massive cinnabar* — granular to compact ore, the most common form
- **Special morphologies:** Incrustations on rock surfaces, vein fillings, disseminated fine grains in sediments

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 50–200°C (epithermal range); optimal at ~100°C
- **Optimal growth temperature:** 80–120°C
- **Decomposition temperature:** >500°C — decomposes to Hg vapor + SO₂
- **Temperature-dependent habits:**
  - <100°C: rhombohedral crystals, deep cochineal-red, well-formed euhedra
  - 100–150°C: stout rhombohedral prisms, still well-formed but less distinct
  - >150°C: massive granular habit predominates; crystals rare

#### Chemistry Required
- **Required elements in broth:** Hg ≥ 5 ppm, S ≥ 10 ppm
- **Optional/enhancing elements:** Se (forms complete solid solution series HgS–HgSe, producing darker, more metallic varieties); trace As can darken color; bituminous organics produce hepatic variety
- **Inhibiting elements:** Fe²⁺ (stabilizes pyrite over cinnabar); Cu²⁺ (competes for S in oxidizing conditions); high Cl⁻ (forms soluble HgCl complexes)
- **Required pH range:** 2.0–9.0 — unusually acid-tolerant for a sulfide; persists in mildly acidic to near-neutral conditions
- **Required Eh range:** Slightly reducing to mildly oxidizing; stable across broader redox range than most sulfides
- **Required O₂ range:** Low to moderate; high O₂ triggers oxidative sublimation (HgS → Hg° vapor + SO₄²⁻)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No — straightforward Hg + S precipitation
- **Byproducts of nucleation:** None
- **Byproducts of dissolution/decomposition:** Oxidative sublimation releases elemental mercury vapor (Hg°) and sulfate (SO₄²⁻) into fluid; this is a key environmental mercury mobilization pathway

#### Growth Characteristics
- **Relative growth rate:** Moderate (3.0× excess rate, baseline)
- **Maximum crystal size:** Individual crystals to 10 cm (Hunan, China); massive ore bodies to meters
- **Typical crystal size in vugs:** 0.1–2 mm crystals in vein coatings; up to 5 mm in exceptional vugs
- **Does growth rate change with temperature?** Yes — slower at low T where well-formed crystals develop; faster at higher T producing massive habit
- **Competes with:** Native sulfur (for S in low-T conditions); metacinnabar (same composition, different structure); realgar/orpiment (for As-S system in same temperature range); pyrite/marcasite (for S)

#### Stability
- **Breaks down in heat?** Yes — >500°C, decomposes to Hg vapor + SO₂
- **Breaks down in light?** No — unlike realgar, cinnabar is photostable. However, impure hepatic varieties may darken
- **Dissolves in water?** Extremely insoluble — Ksp = 2×10⁻³² at 25°C (1.04×10⁻²⁵ g/100 ml)
- **Dissolves in acid?** Resistant to non-oxidizing acids; dissolves in aqua regia and hot concentrated H₂SO₄. This acid tolerance is why cinnabar persists in oxidation zones while other sulfides dissolve
- **Oxidizes?** At very high O₂ and in presence of oxidizing bacteria, cinnabar can undergo oxidative dissolution: HgS + 2O₂ → Hg²⁺ + SO₄²⁻. Natural weathering produces metacinnabar or native mercury droplets
- **Dehydrates?** No — anhydrous
- **Radiation sensitivity:** Darkens under prolonged UV exposure (archaeological pigments show this degradation)

### Paragenesis
- **Forms AFTER:** Native sulfur (cinnabar commonly nucleates on native sulfur surfaces — the substrate preference in the game engine reflects this); also after opal/chalcedony in hot spring deposits
- **Forms BEFORE:** Metacinnabar (can invert to β-HgS at >344°C, but α is the stable form at ambient conditions); native mercury (forms from cinnabar decomposition); calomel (Hg₂Cl₂) in Cl-rich environments
- **Commonly associated minerals:** Native mercury, stibnite, realgar, pyrite, marcasite, opal, chalcedony, barite, dolomite, calcite, quartz, orpiment
- **Zone:** Epithermal/hydrothermal (primary), hot spring/fumarolic (secondary), oxidation zone (tertiary — due to acid tolerance)
- **Geological environment:** Epithermal vein systems in volcanic rocks; hot spring sinters; disseminated in sedimentary rocks near volcanic centers; mercury mines in ophiolitic and volcanic settings

### Famous Localities
- **Almadén, Spain:** The world's largest and most productive mercury deposit. Mined for 2,000+ years by Romans, Moors, and modern operators. Cinnabar in quartz-carbonate veins in Silurian slates. UNESCO Geoheritage site. ~7,000,000 flasks of mercury produced.
- **Idrija, Slovenia:** Europe's second-largest mercury mine (closed 1990s). Hepatic cinnabar variety named from here. UNESCO World Heritage site (shared with Almadén). Bituminous-organic cinnabar in carbonate-hosted deposits.
- **Sulphur Bank, California (USA):** The type locality for metacinnabar-cinnabar association. Hot spring mercury deposit on the shores of Clear Lake. Black metacinnabar coatings on red cinnabar in opal sinter — the classic surface-to-depth zonation.
- **Mount Diablo Mine, Contra Costa County, California:** Exceptional metacinnabar crystals in silica-carbonate gangue.
- **Hunan Province, China:** Exceptional twinned crystals, deep cochineal-red, up to several centimeters. Tsar Tien mine particularly noted.
- **Guizhou Province, China:** Major modern producer; fine crystals from Tongren and Wanshanchang.
- **Huancavelica, Peru:** "The Miner's Cemetery" — high-altitude mercury deposit exploited by Inca and Spanish colonial miners.
- **Terlingua District, Texas (USA):** Classic locality for both cinnabar and metacinnabar in Tertiary volcanic rocks.

### Fluorescence
- **Fluorescent under UV?** No — cinnabar is generally non-fluorescent. However, associated calcite/dolomite may fluoresce.
- **Phosphorescent?** No
- **Note:** Native mercury droplets associated with cinnabar may show weak fluorescence in some specimens due to organic inclusions, but the mineral itself does not fluoresce.

### Flavor Text

> The dragon's blood of the mineral kingdom — cinnabar is so heavy you feel the weight of the mercury before you see the color. It forms where hot, acidic waters bleed through fractured volcanic rock, depositing scarlet coatings that ancient miners chased through tunnels by torchlight. The Romans used it for wall paint; the Maya for ritual pigment; the Chinese for the red lacquer of emperors. Handle it with respect — the same mercury that gives it that impossible refractive index will find your nerves if you breathe the dust or heat it carelessly. In the vug, it nucleates on native sulfur, grows rhombohedra that catch light like garnet, and persists where other sulfides dissolve because cinnabar laughs at weak acids. Watch for the black rim — that's metacinnabar, its shadow-self, telling you the surface has gone oxidizing.

### Simulator Implementation Notes
- **New parameters needed:** Hg (mercury) trace element — currently tracked in the game engine
- **New events needed:** `event_mercury_pulse` — episodic Hg release from deep hydrothermal sources; `event_cinnabar_metacinnabar_inversion` — temperature-triggered polymorph switch
- **Nucleation rule pseudocode:**
```
IF fluid.Hg > 5 AND fluid.S > 10 AND temperature < 200 AND sigma_cinnabar > 1.0
  AND (nearby_native_sulfur OR nearby_opal OR nearby_chalcedony)
  → nucleate cinnabar
```
- **Growth rule pseudocode:**
```
IF sigma > 1.0:
  rate = 3.0 * (sigma - 1.0)
  IF excess > 1.5:
    habit = massive_red (granular ore)
  ELIF temperature < 100:
    habit = rhombohedral_cochineal (well-formed crystals)
  ELSE:
    habit = rhombohedral_cochineal (prismatic)
  debit Hg:1, S:1 from fluid via stoichiometry
```
- **Habit selection logic:** High supersaturation → massive granular; low T + moderate σ → rhombohedral crystals; T > 150°C → stout prisms
- **Decomposition products:** Oxidative sublimation → Hg° vapor (released to fluid), S → SO₄²⁻. At very high T (>500°C): Hg vapor + SO₂

### Variants for Game
- **Variant 1 — Vermillion Massive:** High supersaturation (>2.5), fine-grained granular habit, the classic "red ore" appearance. Forms where fluids are Hg-rich and rapidly cooling.
- **Variant 2 — Almadén Rhombohedron:** Low temperature (<100°C), moderate supersaturation (1.0–2.0), well-formed cochineal-red crystals on white quartz matrix. The specimen-grade variety.
- **Variant 3 — Sulphur Bank Coating:** Nucleates on native sulfur surfaces, thin red coatings with black metacinnabar rims. The oxidation-zone transition variety.
- **Variant 4 — Hepatic Cinnabar:** Organic/bituminous impurity variant, brownish-red to almost black, dull luster, from Idrija-type deposits. Lower value but historically significant.
- **Variant 5 — Selenian Cinnabar:** Se-bearing (Hg(S,Se)), darker, more metallic luster, from Se-rich systems. Complete HgS–HgSe solid solution.

---

## METACINNABAR — β-HgS

### Identity
- **Formula:** HgS (same as cinnabar — dimorphous)
- **Crystal system:** Cubic (isometric)
- **Mineral group:** Sulfide (sphalerite group)
- **Hardness (Mohs):** 2.5–3.0 (slightly harder than cinnabar)
- **Specific gravity:** 7.7–8.1 (slightly lower than cinnabar)
- **Cleavage:** None (isotropic fracture)
- **Fracture:** Conchoidal to uneven
- **Luster:** Metallic to submetallic (distinctly different from cinnabar's adamantine luster)

### Color & Appearance
- **Typical color:** Iron-black, steel-gray, lead-gray
- **Color causes:** Same Hg-S composition but different electronic structure due to sphalerite-type (zincblende) crystal lattice; the cubic symmetry changes the bandgap and absorption characteristics
- **Transparency:** Opaque
- **Streak:** Gray to black (diagnostic — contrasts sharply with cinnabar's scarlet streak)
- **Notable visual features:** Often forms sooty, botryoidal, or crust-like coatings on cinnabar or opal sinter. The black-on-red contrast with cinnabar is visually striking and diagnostic.

### Crystal Habits
- **Primary habit:** Microcrystalline crusts, botryoidal coatings, fine-grained disseminations; rarely as small cubic crystals
- **Common forms/faces:** Cubic {100}, octahedral {111} when crystalline
- **Twin laws:** None common
- **Varieties:** None formally recognized, but selenium-rich varieties grade toward tiemannite (HgSe)
- **Special morphologies:** Sooty coatings on cinnabar, botryoidal masses on opal sinter, fine disseminations in silica-carbonate rock

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** <100°C (strictly low-temperature)
- **Optimal growth temperature:** 20–80°C
- **Decomposition temperature:** Converts to α-cinnabar at 400–550°C (irreversible on heating); metastable at room temperature but persists for geological time
- **Temperature-dependent habits:** Not strongly — always fine-grained to cryptocrystalline due to low T kinetic constraints

#### Chemistry Required
- **Required elements in broth:** Hg ≥ 3 ppm, S ≥ 5 ppm
- **Optional/enhancing elements:** Se (forms solid solution toward tiemannite HgSe); higher S/Hg ratios favor metacinnabar over cinnabar
- **Inhibiting elements:** Same as cinnabar, but metacinnabar is LESS O₂-tolerant
- **Required pH range:** 4.0–8.0 — narrower than cinnabar, prefers slightly less acidic conditions
- **Required Eh range:** Reducing to very mildly oxidizing — more sensitive to oxidation than cinnabar
- **Required O₂ range:** Very low; O₂ > 1.0 triggers rapid oxidative destruction (Hg° vapor + sulfate)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No
- **Byproducts of nucleation:** None
- **Byproducts of dissolution/decomposition:** Oxidative destruction → Hg° vapor + SO₄²⁻ (same as cinnabar but at lower O₂ threshold)

#### Growth Characteristics
- **Relative growth rate:** Moderate to fast (3.5× excess rate — slightly faster than cinnabar)
- **Maximum crystal size:** Rarely >1 mm; usually <0.1 mm as crusts
- **Typical crystal size in vugs:** 0.01–0.5 mm as coatings and disseminations
- **Does growth rate change with temperature?** Yes — very slow at ambient T, faster at 50–80°C
- **Competes with:** Cinnabar (same composition, structure competition); native sulfur; opal/chalcedony (for surface area in hot spring deposits)

#### Stability
- **Breaks down in heat?** Converts to α-cinnabar at 400–550°C (irreversible on heating)
- **Breaks down in light?** No
- **Dissolves in water?** Extremely insoluble (same Ksp as cinnabar)
- **Dissolves in acid?** More reactive than cinnabar; dissolves in hot concentrated HNO₃
- **Oxidizes?** More readily than cinnabar — the reason Sulphur Bank surface metacinnabar weathers first
- **Dehydrates?** No
- **Radiation sensitivity:** No special sensitivity

### Paragenesis
- **Forms AFTER:** Cinnabar (often as overgrowth/crust on cinnabar surfaces in oxidizing conditions); native sulfur; opal/chalcedony sinter
- **Forms BEFORE:** Native mercury (from oxidative weathering); cinnabar (on reheating to >400°C)
- **Commonly associated minerals:** Cinnabar (substrate), opal, chalcedony, native sulfur, pyrite, marcasite, dolomite, calcite
- **Zone:** Hot spring/fumarolic deposits (surface), oxidation zone (shallow), epithermal (rare)
- **Geological environment:** Hot spring sinters (Sulphur Bank type); surficial mercury deposits; opalite-hosted mercury deposits; shallow oxidized zones of Hg deposits

### Famous Localities
- **Sulphur Bank, California (USA):** The classic metacinnabar locality. Black crusts on red cinnabar in opal sinter. Type example of surface oxidation zonation.
- **Mount Diablo Mine, Contra Costa County, California:** Exceptional crystallized specimens in silica-carbonate gangue.
- **McDermitt, Nevada-Oregon (USA):** Large mercury district; metacinnabar common in opalite-hosted deposits.
- **Almadén, Spain:** Rare at depth but reported in some oxidized zones.
- **Terlingua District, Texas (USA):** Both cinnabar and metacinnabar in volcanic-hosted deposits.

### Fluorescence
- **Fluorescent under UV?** No
- **Phosphorescent?** No

### Flavor Text

> Metacinnabar is cinnabar's shadow — same atoms, different arrangement, like two ways of telling the same story. Where cinnabar blazes scarlet, metacinnabar is iron-black and metallic. It forms at the surface of hot spring deposits, coating the red crystals beneath with soot that looks like it came from a candle flame. The Romans never knew this form — it was named in 1870 from Greek meta- (after, beside) + kinnabari. In the vug, it grows faster than cinnabar but dies easier: give it oxygen and it crumbles to mercury vapor and sulfate, which is why Sulphur Bank's surface is black and its depths are red. The two can coexist — black on red, cubic on trigonal — and when they do, the specimen tells you the red came first and the black came after, a palimpsest written in crystal structures.

### Simulator Implementation Notes
- **New parameters needed:** None beyond Hg and S (shared with cinnabar)
- **New events needed:** `event_metacinnabar_oxidation` — low-threshold oxidative destruction; `event_cinnabar_to_metacinnabar_inversion` — not naturally occurring at ambient T (requires >344°C)
- **Nucleation rule pseudocode:**
```
IF fluid.Hg > 3 AND fluid.S > 5 AND temperature < 100
  AND sigma_metacinnabar > 1.0
  AND (nearby_cinnabar OR nearby_opal OR nearby_native_sulfur)
  → nucleate metacinnabar
```
- **Growth rule pseudocode:**
```
IF sigma > 1.0:
  rate = 3.5 * (sigma - 1.0)
  IF position includes 'cinnabar':
    habit = overgrowth_on_cinnabar (black coating on red)
  ELIF position includes 'opal' or 'native_sulfur':
    habit = sooty_on_sinter
  ELIF excess > 1.2:
    habit = botryoidal_black
  ELIF excess > 0.4:
    habit = massive_sooty
  ELSE:
    habit = fine_grained_disseminated
  debit Hg:1, S:1 from fluid
```
- **Habit selection logic:** Proximity to cinnabar → overgrowth coating; proximity to opal/sinter → sooty coating; high σ → botryoidal masses; low σ → fine disseminations
- **Decomposition products:** Oxidative destruction at O₂ > 1.0 → Hg° vapor + SO₄²⁻ (same as cinnabar but lower threshold)

### Variants for Game
- **Variant 1 — Sulphur Bank Surface:** Overgrowth on cinnabar, iron-black metallic crusts on scarlet crystals. The diagnostic field association.
- **Variant 2 — Sinter Coating:** Sooty black coatings on opal/chalcedony sinter in hot spring deposits. Forms where Hg-rich waters cool rapidly at the surface.
- **Variant 3 — Botryoidal Mass:** Black botryoidal crusts, matte to slightly metallic, from high-supersaturation nucleation on silica substrates.
- **Variant 4 — Crystalline (Rare):** Small cubic crystals in silica-carbonate matrix. Rare in nature but distinctive — the "ideal" form that nature rarely grants.

---

## POLYMORPH RELATIONSHIP (Cinnabar ↔ Metacinnabar)

The cinnabar–metacinnabar system is one of the classic examples of temperature-controlled polymorphism in mineralogy:

- **α-cinnabar** (trigonal) is the stable form at all temperatures below ~344°C (some sources say 673 K / 400°C for the onset of transition, with complete conversion by ~550°C)
- **β-metacinnabar** (cubic) is metastable at room temperature but kinetically persistent; it forms at low temperatures from aqueous solutions where the sphalerite-type structure nucleates faster than the cinnabar structure
- The α→β transition is **reversible on heating** but the β→α transition at room temperature is **kinetically inhibited** — metacinnabar can persist for geological time
- **Hypercinnabar** (γ-HgS) is a hypothetical hexagonal high-temperature polymorph stable above ~400°C; rarely observed

In the Vugg Simulator, the polymorph competition can be modeled as:
- High T (>150°C) + slow cooling → cinnabar (thermodynamically stable)
- Low T (<100°C) + rapid nucleation → metacinnabar (kinetically favored)
- Oxidizing conditions → metacinnabar destroyed first, cinnabar persists deeper
- Reheating to >500°C → both decompose to Hg vapor

The Sulphur Bank zonation — black metacinnabar at surface, red cinnabar at depth — is the textbook example of this polymorph + oxidation zonation in nature.

---

## CROSS-REFERENCES

- Vugg Simulator mineral template: `proposals/vugg-mineral-template.md`
- Cinnabar engine: `js/61-engines-sulfide.ts` (lines 780–830)
- Metacinnabar engine: `js/61-engines-sulfide.ts` (lines 990–1030)
- Stibnite research: `memory/research-stibnite.md` (often associated with cinnabar)
- Realgar/orpiment research: `memory/research-realgar.md`, `memory/research-orpiment.md` (same epithermal environment)
- Native sulfur research: `memory/research-native-sulfur.md` (substrate mineral)
- Pyrite/marcasite research: `memory/research-pyrite.md`, `memory/research-pyrite-marcasite.md` (associated sulfides)
- Barite research: `memory/research-barite.md` (common gangue)
- Mercury in trace system: Present in Vugg Simulator (MINERAL_STOICHIOMETRY.cinnabar = {Hg: 1, S: 1})
