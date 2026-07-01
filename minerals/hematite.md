# Species: Hematite

## Identity
- **Formula:** Fe₂O₃
- **Crystal system:** Trigonal (hexagonal scalenohedral class, space group R3̄c)
- **Mineral group:** Oxide (corundum group)
- **Hardness (Mohs):** 5.5–6.5
- **Specific gravity:** 5.26 (very dense — iron-dense crystal)
- **Cleavage:** None — parting on {0001} and {101̄1} due to twinning or deformation lamellae; no true cleavage
- **Fracture:** Subconchoidal to uneven
- **Luster:** Metallic to submetallic in crystalline varieties; earthy in massive ochre
- **Streak:** Cherry-red to reddish-brown (diagnostic)
- **Tenacity:** Brittle

## Color & Appearance
- **Typical color:** Steel-gray to iron-black in crystalline specimens; blood-red in powder/streak; red to reddish-brown in earthy forms (ochre)
- **Color causes:** Crystal-field transitions in Fe³⁺ in octahedral coordination; charge-transfer Fe³⁺→O²⁻ contributes to deep red-brown in fine-grained material. Crystalline hematite is dark because of strong light absorption in the visible spectrum; the red streak comes from remitted light after surface oxidation films are broken.
- **Transparency:** Opaque in all but the thinnest splinters (which may show deep blood-red translucency under strong light)
- **Notable visual features:** Specular hematite (specularite) shows bright metallic luster with mirror-like faces. Botryoidal/kidney ore shows concentric internal banding (Liesegang-type precipitation rings). Martite shows pseudomorphic outlines after magnetite octahedra. Micaceous hematite (iron rose) forms thin platy rosettes.

## Crystal Habits
- **Primary habit:** Tabular on {0001} (basal plates), rhombohedral {101̄4}, scalenohedral {21̄31} or {h0h̄l}. Most common natural habit is thin tabular or platy crystals stacked in rosettes.
- **Common forms/faces:** {0001} (basal pinacoid), {101̄0} (prism), {101̄4} (rhombohedron), {101̄1} and {022̄1} (scalenohedra). The basal pinacoid dominates in most occurrences.
- **Twin laws:** Penetration twins on {0001} (rare in nature, more common in synthetic); lamellar twinning on {101̄1} and {0001} producing the "parting" that mimics cleavage. Platy hematite often shows triangular growth patterns on {0001} surfaces — trigonal etch pits or growth hillocks marking sector boundaries.
- **Varieties:**
  - *Specularite / specular hematite:* Coarse crystalline, bright metallic luster, steel-gray, from metamorphic or hydrothermal environments.
  - *Micaceous hematite / iron rose:* Thin platy crystals in rosette aggregates, soft enough to write on paper (pencil ore). Elba, Italy; Brazilian iron formations.
  - *Kidney ore / botryoidal hematite:* Reniform to botryoidal masses with internal concentric banding, colloidal origin. Cumberland, UK; Marquette Range, Michigan.
  - *Ochre / earthy hematite:* Fine-grained, red to yellow-brown pigment material. Yellow ochre contains more goethite; red ochre is dominantly hematite. Used since the Paleolithic.
  - *Martite:* Pseudomorph of hematite after magnetite — retains magnetite's octahedral outline but is non-magnetic and shows red-brown streak.
  - *Iron rose (eiserne Rose):* Radial aggregates of thin hexagonal plates, typically from alpine clefts (Brasil, Swiss Alps).
  - *Pencil ore:* Very soft, micaceous hematite that marks paper; Cumberland, UK.
- **Special morphologies:** Dendritic hematite in agate or jasper (Dendritic agate — not truly dendritic crystals but iron oxide stains in crack patterns). Columnar/massive in BIFs (banded iron formations). Oolitic in sedimentary deposits.

## Formation Conditions (SIMULATOR PARAMETERS)

### Temperature
- **Nucleation temperature range:** 20–900°C (very broad — hematite forms across nearly all geological temperatures)
- **Optimal growth temperature:** 200–400°C for hydrothermal crystalline specularite; ~25–100°C for supergene/goethite replacement; >500°C for thermal oxidation of magnetite or dehydration of goethite
- **Decomposition temperature:** >1450°C (melts to maghemite then liquid; not relevant for simulator)
- **Temperature-dependent habits:**
  - Low-T (<150°C): Earthy/ochre, fine-grained, poor crystallinity, often mixed with goethite.
  - Medium-T (150–400°C): Tabular crystals, specularite, good crystallinity. Kidney ore forms from colloidal precursors in this range.
  - High-T (>400°C): Coarse specularite, martite (from magnetite oxidation), micaceous plates. At >500°C goethite dehydrates to hematite — this is a major formation pathway.
  - Contact metamorphic: Very coarse crystals in skarns and around intrusions (Elba crystals to 10 cm).

### Chemistry Required
- **Required elements in broth:** Fe (≥50 ppm for visible nucleation; can nucleate at lower Fe if Eh strongly oxidizing and pH near neutral), O₂ (oxidizing environment — hematite is the stable Fe³⁺ oxide)
- **Optional/enhancing elements:**
  - Al³⁺: Up to ~15% Al₂O₃ can substitute for Fe₂O₃; higher Al stabilizes corundum-structured α-phase, but hematite accepts moderate Al.
  - Ti⁴⁺: Up to ~10% TiO₂ in some igneous/magmatic contexts (ilmenite-hematite solid solution); gives darker, more metallic appearance.
  - Mn³⁺/Mn²⁺: Minor substitution; can shift color slightly.
  - Cr³⁺: Rare, but chromium hematite is known (though uvarovite is the stable Cr-garnet).
  - SiO₂: In BIF environments, silica precipitates in alternation with hematite, producing the classic banding. Not structurally incorporated.
- **Inhibiting elements:**
  - High S²⁻ (reducing sulfur): Stabilizes pyrite/marcasite instead; hematite needs oxidizing or at least sulfur-poor conditions.
  - High dissolved organic carbon / strongly reducing Eh: Fe²⁺ stays in solution as Fe²⁺(aq) or precipitates as siderite/pyrite rather than oxidizing to Fe³⁺.
  - High CO₂ with low Eh: Can form siderite instead.
  - Very high silica + low Eh: chrysoprase/iron silicate alternatives.
- **Required pH range:** 3–9 (very broad). Hematite is stable across most natural pH values except extremely acidic (pH <2, where Fe³⁺ stays soluble as Fe³⁺(aq) or [Fe(H₂O)₆]³⁺) or strongly alkaline (pH >11, where ferrihydrite or goethite may be favored). Optimal precipitation pH: 6–8.
- **Required Eh range:** Strongly oxidizing (+0.2 to +0.7 V at pH 7). The hematite stability field occupies the upper-right of the Pourbaix diagram. It is THE stable iron oxide under aerobic conditions at Earth-surface temperatures.
- **Required O₂ range:** >0.1 ppm dissolved O₂ (essentially any oxic water). In the simulator, hematite should form whenever Fe and oxidizing conditions coexist, unless another phase is thermodynamically favored.

### Secondary Chemistry Release
- **Does it release any chemicals when forming?**
  - Dehydration of goethite → hematite releases H₂O: 2 FeO(OH) → Fe₂O₃ + H₂O. In the simulator, this is a major late-stage event in iron oxidation zones — goethite that formed earlier dehydrates when temperature rises (burial, contact metamorphism, or deep supergene heating).
  - Oxidation of magnetite → hematite releases Fe²⁺ that re-oxidizes, consuming O₂ and producing acid if sulfides are present: 2 Fe₃O₄ + ½ O₂ → 3 Fe₂O₃.
  - Oxidation of pyrite → goethite/hematite releases H₂SO₄ and Fe²⁺, which then oxidizes and hydrolyzes to precipitate more hematite (acid mine drainage chemistry).
- **Byproducts of nucleation:** In iron oxidation zones, hematite formation after goethite dehydration releases H₂O vapor (in simulator: returns to fluid as H₂O, increasing local humidity/pore pressure slightly).
- **Byproducts of dissolution/decomposition:** Dissolves in hot concentrated HCl (not aqua regia — hematite resists nitric acid). In nature, reduction dissolves hematite: Fe₂O₃ + 2e⁻ + 6H⁺ → 2Fe²⁺ + 3H₂O. This is how BIFs were leached to form high-grade iron ore (supergene enrichment).

### Growth Characteristics
- **Relative growth rate:** Slow to moderate. Slower than goethite (which precipitates rapidly from Fe³⁺-rich solutions at low T). Hematite is the thermodynamically stable end product but often forms by transformation of metastable precursors (ferrihydrite → goethite → hematite, or direct from ferrihydrite at elevated T).
- **Maximum crystal size in nature:** 10+ cm for alpine cleft specularite (Brasil, Elba). BIF layers are stratiform deposits kilometers in extent but microcrystalline.
- **Typical crystal size in vugs:** 0.1–5 mm for hydrothermal specularite; earthy hematite is sub-micron to 0.1 mm. In oxidation-zone vugs, martite pseudomorphs after magnetite may retain original octahedron size (1–10 mm).
- **Does growth rate change with temperature?** Yes. At T >500°C, goethite dehydration to hematite is rapid (hours to days). At T <100°C, hematite forms very slowly from ferrihydrite aging, or not at all (goethite is the kinetically favored product). Growth rate increases exponentially with temperature in the 100–500°C range.
- **Competes with:** Goethite (kinetically favored at low T), magnetite (at moderate Eh and higher T), siderite (reducing, high CO₂), pyrite/marcasite (reducing, high S²⁻), jarosite (acidic, sulfate-rich, oxidizing).

### Stability
- **Breaks down in heat?** Dehydrates goethite precursor at ~250–400°C; hematite itself is stable to >1400°C. In simulator: goethite → hematite transition at T > 450°C (conservative, allows some overlap).
- **Breaks down in light?** No. Hematite is photostable (unlike realgar, proustite, etc.).
- **Dissolves in water?** Insoluble. Solubility of Fe³⁺ at pH 7 is ~10⁻¹⁸ M. Hematite does not dissolve in pure water.
- **Dissolves in acid?** Yes — dissolves in hot concentrated HCl. In the simulator: acid dissolution (pH <3) slowly attacks hematite, releasing Fe³⁺ to solution. Rate is slow unless acid is strong and hot.
- **Oxidizes?** No — hematite IS the fully oxidized iron oxide. Further oxidation is impossible under terrestrial conditions.
- **Dehydrates?** Hematite itself does not dehydrate. Its precursor goethite does (see above).
- **Radiation sensitivity:** Darkens slightly under heavy radiation but structurally stable. Hematite is actually used as a radiation shielding pigment.
- **Reduces?** Yes — under strongly reducing conditions (Eh <0.0 V at pH 7), hematite can be reduced to magnetite or dissolved as Fe²⁺. This is the key supergene enrichment reaction for iron ores.

## Paragenesis
- **Forms AFTER:**
  - Goethite (as dehydration product at T >450°C)
  - Magnetite (as oxidation product — martite)
  - Pyrite/marcasite (as oxidation product in supergene/weathering zones — via goethite intermediate or direct)
  - Siderite (as oxidation product in weathering)
  - Ferrihydrite (as aging product — ferrihydrite → goethite → hematite sequence)
- **Forms BEFORE:**
  - In regressive (cooling/rewetting) systems: goethite can re-form from hematite if T drops and water is available (very slow at T <100°C).
  - In reducing systems: magnetite can replace hematite if Eh drops and T is moderate.
- **Commonly associated minerals:**
  - Supergene iron zone: goethite, lepidocrocite, jarosite, quartz, chalcedony, manganese oxides.
  - Hydrothermal: quartz, chalcedony, siderite, dolomite, barite, fluorite, sulfides (pyrite, chalcopyrite, galena, sphalerite).
  - Contact metamorphic/skarn: magnetite, garnet, pyroxene, wollastonite, idocrase, epidote.
  - BIF: chert/jasper, magnetite, siderite, greenalite, minnesotaite, stilpnomelane, riebeckite.
  - Bauxite/aluminous laterite: gibbsite, boehmite, kaolinite, goethite.
- **Zone:** Supergene/oxidation (most common in surficial environments); hypogene hydrothermal (specularite); contact metamorphic; magmatic (as primary precipitate in some alkaline intrusions); sedimentary (BIF, oolitic ironstone, red beds).
- **Geological environment:** Universally distributed. The most common Fe-oxide on Earth after magnetite (and more abundant at the surface than magnetite). Forms in:
  - Supergene oxidation zones over sulfide deposits (after pyrite → goethite → hematite)
  - Banded iron formations (Archaean–Proterozoic chemical sediments)
  - Hydrothermal veins (specularite with quartz, barite, sulfides)
  - Contact metamorphic aureoles (coarse crystals)
  - Lateritic soils (residual enrichment)
  - Red bed sandstones (diagenetic cement)

## Famous Localities
- **Classic locality 1:** Elba Island, Italy — iron rose hematite (micaceous rosettes up to 10 cm), type locality for the variety. Associated with tourmaline (elbaite), quartz, and orthoclase in alpine clefts in the contact aureole of the Monte Capanne monzogranite.
- **Classic locality 2:** Cumberland (Cumbria), UK — kidney ore, pencil ore, and specularite from the west Cumbrian iron orefield. Jurassic limestone-hosted replacement deposits, some of the finest botryoidal hematite ever found.
- **Classic locality 3:** Minas Gerais, Brazil — specularite and iron rose from the Iron Quadrangle (Quadrilátero Ferrífero). World's largest reserves of high-grade hematite ore, source of most global iron ore production. Crystals to 5 cm from the Gandarela Formation and Itabira Group.
- **Notable specimens:**
  - The "Hope of the World" — a 9-cm iron rose from Brasil, Minas Gerais (private collection, photo in Bancroft).
  - Kidney ore from Florence Mine, Egremont, Cumbria — classic concentrically banded reniform masses to 30 cm.
  - Specularite from Michipicoten Island, Lake Superior — crystals to 2 cm in quartz veins, Ontario, Canada.
  - Martite pseudomorphs after magnetite from Savage River, Tasmania — perfect octahedral casts retaining magnetite morphology.
  - Blood-red ochre from Roussillon, Provence, France — pigment source since Roman times, still used in cosmetics.

## Fluorescence
- **Fluorescent under UV?** No. Hematite does not fluoresce under any UV wavelength. It is an iron-dominant mineral, and Fe³⁺ is a strong fluorescence quencher (paramagnetic ion that facilitates non-radiative decay).
- **SW (255nm):** None (quenched by Fe³⁺)
- **MW (310nm):** None
- **LW (365nm):** None
- **Phosphorescent?** No.
- **Activator:** None.
- **Quenched by:** Fe³⁺ (self-quenched). Any trace Mn²⁺ that might fluoresce in other matrices is quenched by the overwhelming Fe³⁺ concentration.

## Flavor Text

*Hematite carries the color of dried blood and the weight of a planet's core. It is the final oxidation state of iron — the thermodynamic graveyard where Fe²⁺ goes when it has given up its last electron to the air. Every red desert, every rusted hull, every Paleolithic handprint on a cave wall owes its color to this mineral. In the vug, it arrives late: goethite must dehydrate first, or magnetite must surrender its ferrous heart. But once hematite crystallizes, it endures. The stone does not care about your urgency. It was already red before the first lung drew breath.*

## Simulator Implementation Notes

### New parameters needed
- None — Fe and O₂ are already tracked. pH and Eh are already in the chemistry system.

### New events needed
- `event_goethite_dehydration`: When T > 450°C and goethite crystals are present, trigger dehydration → hematite + H₂O release. Should be a zone-wide transformation event (like a thermal pulse) rather than per-crystal, since goethite dehydration is rapid once triggered.
- `event_martite_formation`: When magnetite is present AND T > 300°C AND O₂ is available, gradual oxidation of magnetite surface → hematite rim. The interior may remain magnetite (titanomagnetite-style zoning) or fully convert. For simulator simplicity: full pseudomorph replacement over 5–10 steps, preserving original crystal shape but changing color/streak/properties.
- `event_bif_pulse`: Archaean-style banded iron formation event — alternating silica and hematite precipitation in thin layers. Could be a special scenario or a global event triggered by specific atmospheric chemistry.

### Nucleation rule pseudocode
```
IF Fe_ppm >= 20 AND Eh > 0.1 AND pH >= 3 AND pH <= 9 AND O2_ppm > 0.1:
    IF T > 450 AND goethite_present:
        # Dehydration pathway — no new nucleation, transformation
        trigger_event("goethite_dehydration")
    ELSE IF T >= 100:
        # Direct precipitation from Fe³⁺(aq)
        nucleation_probability = base_rate * (Fe_ppm / 100) * Eh_factor * temperature_factor
        IF nucleation_probability > threshold:
            nucleate hematite
    ELSE IF T < 100 AND aging_time > 50:
        # Ferrihydrite aging pathway — very slow
        low_prob_nucleation = base_rate * 0.05 * aging_factor
        IF low_prob_nucleation > threshold:
            nucleate hematite (earthy/microcrystalline habit)
```

### Growth rule pseudocode
```
IF crystal == hematite:
    IF T > 450 AND original_mineral == goethite:
        # Dehydration transformation — rapid conversion
        growth_rate = 0  # Not growth, phase transformation
        transform_to(hematite, preserve_shape = False)
        release H2O to fluid
    ELSE IF T > 300 AND original_mineral == magnetite:
        # Martite transformation
        growth_rate = 0
        transform_to(hematite, preserve_shape = True)  # pseudomorph
        consume O2 from fluid
    ELSE:
        # Normal growth from solution
        sigma = calculate_supersaturation(Fe, Eh, pH, T)
        growth_rate = base_rate * sigma * temperature_factor(T)
        IF T > 400:
            growth_rate *= 1.5  # faster at high T
        IF goethite_competing:
            growth_rate *= 0.3  # goethite kinetically favored at low-medium T
```

### Habit selection logic
- **T > 500°C + slow cooling:** Tabular/bladed specularite (coarse crystals, metallic luster)
- **T 300–500°C:** Micaceous hematite (thin plates, rosette aggregates)
- **T 100–300°C + colloidal precursor:** Kidney ore (botryoidal, concentric banding)
- **T < 100°C + long aging:** Earthy/ochre (fine-grained, dull, red-brown)
- **Pseudomorph after magnetite:** Martite (retains octahedral shape, but non-magnetic, red streak)
- **Pseudomorph after goethite:** Retains goethite needle/prismatic habit but becomes harder, darker
- **Very high Fe + rapid precipitation:** Dendritic hematite (thin branching crystal sprays)

### Decomposition products
- **Reduction (low Eh, moderate T):** Magnetite (Fe₃O₄) — 3 Fe₂O₃ + 2e⁻ → 2 Fe₃O₄ + ½ O₂ (simplified)
- **Reduction (low Eh, low T, acidic):** Fe²⁺(aq) — dissolves back to solution
- **Strong acid (pH <2):** Fe³⁺(aq) — dissolves as ferric ion
- **Thermal decomposition (>1450°C):** Maghemite (γ-Fe₂O₃) transient, then liquid melt (not relevant for simulator)

## Variants for Game

### Variant 1: Specularite
- **What makes it different:** Bright metallic luster, steel-gray color, tabular crystals with triangular growth markings on basal faces. High-T hydrothermal or contact metamorphic origin.
- **Conditions:** T > 400°C, slow cooling, moderate-high Fe (50–200 ppm), oxidizing Eh.
- **Visual:** Mirror-like faces, hexagonal tabular plates stacked in rosettes. Sparkles under light. Streak is still cherry-red (test the player knows).
- **Flavor addition:** *"The miner called it 'black diamond' — not for value, but for the way it threw light back at the lamp. Every face is a frozen mirror of the hydrothermal fluid it grew from."*

### Variant 2: Kidney Ore
- **What makes it different:** Botryoidal/reniform masses with internal concentric banding (Liesegang rings). Colloidal origin, softer than crystalline varieties.
- **Conditions:** T 50–150°C, moderate Fe (30–100 ppm), pH 6–7, oscillating supersaturation (periodic precipitation events).
- **Visual:** Smooth, rounded surfaces like kidneys or grapes. Cross-section shows alternating red-brown and darker bands. Resembles agate but is entirely iron oxide.
- **Flavor addition:** *"It grew like a tree ring, one colloidal shell at a time, each band recording a pulse of iron-rich water. Cut it open and you read the rainfall history of an ancient aquifer."*

### Variant 3: Martite
- **What makes it different:** Pseudomorph after magnetite — retains perfect octahedral crystal shape but is non-magnetic and shows red-brown streak instead of magnetite's black streak.
- **Conditions:** Magnetite present, T > 300°C, O₂ available, prolonged oxidizing conditions.
- **Visual:** Octahedral crystals that look like magnetite but don't stick to a magnet. Sometimes shows triangular etch pits on octahedron faces (oxidation front geometry). May retain magnetite core with hematite rim.
- **Flavor addition:** *"A ghost wearing its old body's clothes. The octahedron remembers magnetite's geometry, but the chemistry has moved on. Test it with a magnet — the silence is the proof."*

### Variant 4: Iron Rose
- **What makes it different:** Very thin micaceous plates in radial rosettes, soft enough to write with (pencil ore). Alpine cleft or contact metamorphic origin.
- **Conditions:** T 300–500°C, moderate Fe, space to grow (open vugs/clefts), slow cooling.
- **Visual:** Delicate, flower-like aggregates of hexagonal plates. Dark metallic with red edges where thin enough for light to pass through. Fragile — plates detach easily.
- **Flavor addition:** *"An iron flower that only blooms where granite has baked the country rock. The petals are single crystals thin enough to see through. It will mark your fingers red and your notebook permanently."*

### Variant 5: Ochre Pigment
- **What makes it different:** Earthy, fine-grained, no crystal form visible. Used as pigment since the Paleolithic. Forms in weathering zones, laterites, red beds.
- **Conditions:** T < 50°C, any Fe concentration, oxidizing, surficial/weathering environment.
- **Visual:** Red-brown powdery coating on other minerals or as soft earthy masses. No luster. Stains everything it touches.
- **Flavor addition:** *"This is the color of the first art. A hand pressed against a cave wall, blown ochre around it, leaving a negative ghost that survived forty thousand years. It is not a crystal. It is a memory of a hand."*
