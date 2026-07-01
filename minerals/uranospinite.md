# Species: Uranospinite

### Identity
- **Formula:** Ca(UO₂)₂(AsO₄)₂·10H₂O
- **Crystal system:** Orthorhombic
- **Mineral group:** Phosphate / Arsenate (Autunite group — uranyl arsenate)
- **Hardness (Mohs):** 2–3
- **Specific gravity:** 3.2–3.5
- **Cleavage:** Perfect on {001}, distinct on {100} — micaceous sheet structure
- **Fracture:** Brittle
- **Luster:** Pearly to vitreous; often waxy in fine-grained aggregates

### Color & Appearance
- **Typical color:** Yellow-green, lemon yellow, siskin green, pale greenish-yellow
- **Color causes:** Uranyl ion (UO₂²⁺) in sheets; Ca²⁺ is colorless, so uranospinite is lighter than Cu-bearing zeunerite
- **Transparency:** Transparent in thin crystals, translucent to opaque in aggregates/coatings
- **Streak:** Light yellow
- **Notable visual features:** Fine-grained waxy coatings or thin tabular crystals; often powdery or earthy in habit; epitaxial growth on zeunerite reported

### Crystal Habits
- **Primary habit:** Thin tabular crystals, flattened on {001}
- **Common forms/faces:** {001} dominant, crystals to 1 mm
- **Twin laws:** None reported
- **Varieties:** Metauranospinite (dehydration product, fewer water molecules)
- **Special morphologies:** Fine-grained waxy to powdery coatings; crusts and aggregates; epitaxial overgrowths on zeunerite crystals (rare, Piedmont)

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 10–50°C
- **Optimal growth temperature:** 15–30°C (near-surface weathering zone)
- **Decomposition temperature:** >300°C (uranyl sheet breakdown); dehydration begins ~60°C
- **Temperature-dependent habits:** Lower temperatures favor micro-crystalline coatings; slightly warmer and wetter conditions favor larger (still tiny) tabular crystals

#### Chemistry Required
- **Required elements in broth:**
  - U > 20 ppm (oxidized to U⁶⁺, uranyl form)
  - Ca > 20 ppm
  - As > 10 ppm (as AsO₄³⁻, from arsenopyrite/scorodite oxidation)
- **Optional/enhancing elements:** Cu (minor substitution possible, but Ca dominates)
- **Inhibiting elements:** Fe²⁺, high sulfate, high SiO₂ (forms uranophane at high pH)
- **Required pH range:** 5.5–7.5 (mildly acidic to neutral)
- **Required Eh range:** Oxidizing (+0.3 to +0.6 V) — U must be U⁶⁺
- **Required O₂ range:** Moderate to high (oxygenated groundwater)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No significant releases; consumes U⁶⁺, Ca²⁺, AsO₄³⁻ from solution
- **Byproducts of nucleation:** Local pH drop (uranyl hydrolysis releases H⁺)
- **Byproducts of dissolution/decomposition:** Releases U⁶⁺, Ca²⁺, AsO₄³⁻ back to fluid; dehydration releases H₂O vapor

#### Growth Characteristics
- **Relative growth rate:** Slow — Ca has lower mobility than Cu in groundwater, and AsO₄ is less abundant than PO₄ in most deposits
- **Maximum crystal size:** Up to 1 mm tabular crystals (exceptional); typically <0.3 mm
- **Typical crystal size in vugs:** 0.1–0.3 mm crystals or fine crusts
- **Does growth rate change with temperature?** Growth slows sharply above 50°C; optimal in 15–30°C weathering zone
- **Competes with:** Autunite (when PO₄ >> AsO₄), zeunerite (when Cu >> Ca), torbernite (when both Cu and PO₄ dominate)

#### Stability
- **Breaks down in heat?** Dehydrates to metauranospinite at ~60°C; structural breakdown >300°C
- **Breaks down in light?** No photochemical decomposition; fluorescence stable
- **Dissolves in water?** Very low solubility in neutral water; soluble in strong acid or strong alkali
- **Dissolves in acid?** Yes — dissolves in HCl, HNO₃
- **Oxidizes?** Already fully oxidized (U⁶⁺, Ca²⁺)
- **Dehydrates?** Yes — readily dehydrates to metauranospinite in dry air
- **Radiation sensitivity:** Self-irradiation causes gradual amorphization over geological time

### Paragenesis
- **Forms AFTER:** Uraninite/pitchblende oxidation; arsenopyrite or scorodite oxidation (As source); calcite dissolution or Ca-bearing groundwater
- **Forms BEFORE:** Further dehydration to metauranospinite; uranophane at higher pH
- **Commonly associated minerals:** Zeunerite (often epitaxial), scorodite, goethite, uraninite, quartz, calcite, gypsum
- **Zone:** Supergene oxidation zone (uppermost weathered portion of uranium deposits)
- **Geological environment:** Oxidized uranium deposits where Ca-bearing groundwater (from limestone, calcite, or dolomite) interacts with arsenic-bearing host rock

### Famous Localities
- **Classic locality 1:** Ellweiler, Rhineland-Palatinate, Germany — type locality
- **Classic locality 2:** Rabejac Deposit, Lodève, Hérault, France — fine-grained waxy coatings in extraordinary supergene uranyl mineralization
- **Classic locality 3:** Montoso Quarries, Bagnolo Piemonte, Cuneo Province, Piedmont, Italy — beautiful epitaxial crystals on zeunerite
- **Notable specimens:** Tyndrum, Perthshire, Scotland; Mas d'Alary village, Lodève, France

### Fluorescence
- **Fluorescent under UV?** Yes — moderate yellow-green
- **SW (255nm) color:** Yellow-green
- **MW (310nm) color:** Yellow-green
- **LW (365nm) color:** Yellow-green (stronger than Cu-members due to no Cu²⁺ quenching)
- **Phosphorescent?** No
- **Activator:** Uranyl ion (UO₂²⁺) — intrinsic fluorescence
- **Quenched by:** Fe²⁺, organic matter

### Flavor Text
> Uranospinite is the shy cousin of the autunite family. Where zeunerite flaunts emerald sheets and torbernite demands attention with its screaming green books, uranospinite hides as a waxy yellow-green film — a powdery coating you might mistake for moss or mold until you check it with a Geiger counter and it chatters back. It's the calcium-arsenate end member: lighter in color than its copper twin, more powdery in habit, and so much rarer that most collectors have never held a named specimen. The best ones grow epitaxially on zeunerite — a Ca-skin on a Cu-core, chemistry writing its own stratigraphy in crystals too small to see without magnification. From the Rabejac deposit in France, where the groundwater was calcium-rich and arsenic-tainted, uranospinite formed as the quiet whisper at the edge of a louder mineral conversation.

### Simulator Implementation Notes
- **New parameters needed:** U-oxidation-state (U⁶⁺ vs U⁴⁺), AsO₄ availability as distinct from PO₄
- **New events needed:** Arsenopyrite oxidation event (releases AsO₄); uraninite oxidation event (releases U⁶⁺)
- **Nucleation rule pseudocode:**
```
IF U6 > 20 ppm AND Ca > 20 ppm AND AsO4 > 10 ppm
   AND pH 5.5-7.5 AND T < 50°C AND Eh > +0.3V
   AND Ca/Cu ratio > 2.0 (Ca dominates over Cu)
   AND AsO4/PO4 ratio > 0.5 (arsenate significant)
   AND RH > 60% (hydrated form)
THEN nucleate uranospinite (micro-crystalline habit or thin tabular)
```
- **Growth rule pseudocode:**
```
IF uranospinite crystal exists AND U6 > 10 ppm AND Ca > 10 ppm AND AsO4 > 5 ppm
   AND T < 50°C AND pH 5.5-7.5
THEN grow at rate 0.15x quartz baseline (slow, Ca-limited)
     (sheet growth in a-b plane, minimal c-direction growth)
```
- **Habit selection logic:**
  - If growth space > 5 mm AND chemistry abundant: thin tabular crystals, 0.2-1 mm
  - If growth space < 5 mm OR chemistry limited: fine-grained crusts, waxy coatings
  - If epitaxial substrate (zeunerite present): prefer overgrowth on existing zeunerite sheets
- **Dehydration products:**
  - At RH < 40% or T > 60°C: convert to metauranospinite (color dulls, becomes more powdery)

### Variants for Game
- **Variant 1: Crystallized** — Thin tabular crystals, 0.2-1 mm, lemon yellow-green, transparent. Conditions: abundant space, moderate chemistry, slow growth. Rare.
- **Variant 2: Waxy Crust** — Fine-grained coating, pale yellow-green, waxy luster, powdery texture. Conditions: limited space, rapid precipitation, abundant Ca. Common.
- **Variant 3: Epitaxial Mantle** — Thin overgrowth on zeunerite crystals, same orientation, lighter color. Conditions: zeunerite substrate present, Ca/As chemistry shifts after zeunerite nucleation. Special paragenetic event.
