# Species: Zeunerite

### Identity
- **Formula:** Cu(UO₂)₂(AsO₄)₂·(10-16)H₂O
- **Crystal system:** Tetragonal
- **Mineral group:** Phosphate / Arsenate (Autunite group — uranyl arsenate)
- **Hardness (Mohs):** 2–2.5
- **Specific gravity:** 3.2–3.4
- **Cleavage:** Perfect on {001}, distinct on {100} — micaceous sheet structure
- **Fracture:** Flexible, sectile (bends like mica before breaking)
- **Luster:** Vitreous to pearly on cleavage surfaces

### Color & Appearance
- **Typical color:** Yellow-green to emerald-green
- **Color causes:** Cu²⁺ in the interlayer position + uranyl (UO₂²⁺) sheets
- **Transparency:** Transparent when fresh, becoming translucent on dehydration
- **Streak:** Pale green
- **Notable visual features:** Micaceous sheets with subparallel growth; flat tabular crystals that overlap like pages in a book

### Crystal Habits
- **Primary habit:** Tabular, flat on {001}, square or octagonal in outline
- **Common forms/faces:** {001} dominant, {011}, {110}, rarely pyramidal {111}
- **Twin laws:** None common; subparallel aggregation is the dominant growth pattern
- **Varieties:** Metazeunerite (dehydration product, ~8H₂O, more opaque)
- **Special morphologies:** Micaceous books, crusts, subparallel stacks; crystals to 4 cm reported

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 10–50°C
- **Optimal growth temperature:** 15–30°C (near-surface weathering zone)
- **Decomposition temperature:** >300°C (uranyl sheet breakdown); dehydration begins ~60–80°C
- **Temperature-dependent habits:** None significant — always the sheet structure

#### Chemistry Required
- **Required elements in broth:**
  - U > 20 ppm (oxidized to U⁶⁺, uranyl form)
  - Cu > 20 ppm
  - As > 10 ppm (as AsO₄³⁻, from arsenopyrite/scorodite oxidation)
- **Optional/enhancing elements:** Ca (minor substitution possible but Cu dominates)
- **Inhibiting elements:** Fe²⁺ (competes for AsO₄), high sulfate (competes for Cu), SiO₂ (forms uranophane instead at high pH)
- **Required pH range:** 5.0–7.0 (mildly acidic to neutral)
- **Required Eh range:** Oxidizing (+0.3 to +0.6 V) — U must be U⁶⁺
- **Required O₂ range:** Moderate to high (oxygenated groundwater)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No significant releases; consumes U⁶⁺, Cu²⁺, AsO₄³⁻ from solution
- **Byproducts of nucleation:** Local pH drop (uranyl hydrolysis releases H⁺)
- **Byproducts of dissolution/decomposition:** Releases U⁶⁺, Cu²⁺, AsO₄³⁻ back to fluid; dehydration releases H₂O vapor

#### Growth Characteristics
- **Relative growth rate:** Moderate — faster than uranospinite (Cu has higher mobility than Ca), slower than autunite
- **Maximum crystal size:** Up to 4 cm tabular crystals (exceptional); typically 0.5–2 cm
- **Typical crystal size in vugs:** 0.2–1 cm sheets or crusts
- **Does growth rate change with temperature?** Growth slows sharply above 50°C; optimal in 15–30°C weathering zone
- **Competes with:** Torbernite (when PO₄ >> AsO₄), uranospinite (when Ca >> Cu), autunite (when both Ca and PO₄ dominate)

#### Stability
- **Breaks down in heat?** Dehydrates to metazeunerite at ~60–80°C; structural breakdown >300°C
- **Breaks down in light?** No photochemical decomposition; fluorescence is stable
- **Dissolves in water?** Very low solubility in neutral water; soluble in strong acid or strong alkali
- **Dissolves in acid?** Yes — dissolves in HCl, HNO₃ (uranyl arsenates are acid-soluble)
- **Oxidizes?** Already fully oxidized (U⁶⁺, Cu²⁺); no further oxidation pathway
- **Dehydrates?** Yes — readily dehydrates to metazeunerite in dry air or heated conditions
- **Radiation sensitivity:** Self-irradiation causes gradual amorphization over geological time (decades to centuries for visible darkening)

### Paragenesis
- **Forms AFTER:** Uraninite/pitchblende oxidation; arsenopyrite or scorodite oxidation (As source); copper sulfide oxidation (Cu source)
- **Forms BEFORE:** Further dehydration to metazeunerite; rarely, uranophane at higher pH
- **Commonly associated minerals:** Scorodite, olivenite, malachite, azurite, cuprite, uraninite, quartz, fluorite
- **Zone:** Supergene oxidation zone (uppermost weathered portion of uranium deposits)
- **Geological environment:** Oxidized uranium deposits in granite pegmatites, hydrothermal veins, or sandstone-hosted roll-front deposits with arsenic-bearing host rock

### Famous Localities
- **Classic locality 1:** Weißer Hirsch Mine, Schneeberg District, Erzgebirge, Saxony, Germany — type locality (1872)
- **Classic locality 2:** Zinnwald-Cínovec mining region, Ore Mountains (Czech/German border)
- **Classic locality 3:** Grandview Mine, Arizona, USA
- **Notable specimens:** Crystals to 4 cm from Cínovec; subparallel micaceous books from Schneeberg

### Fluorescence
- **Fluorescent under UV?** Yes — weak to moderate
- **SW (255nm) color:** Yellow-green
- **MW (310nm) color:** Yellow-green
- **LW (365nm) color:** Yellow-green (weaker than autunite due to Cu²⁺ quenching)
- **Phosphorescent?** No
- **Activator:** Uranyl ion (UO₂²⁺) — intrinsic fluorescence
- **Quenched by:** Cu²⁺ partially quenches compared to Ca-autunites

### Flavor Text
> Zeunerite is torbernite's arsenic twin — same emerald-green sheets, same micaceous habit, same uranium glow, but grown from arsenate instead of phosphate. Gustav Zeuner never asked for his name on a radioactive mineral, but the Erzgebirge miners gave it to him anyway, in 1872, when they pulled these green sheets from the Weisser Hirsch mine and noticed they grew alongside scorodite, not apatite. The difference is invisible to the eye — you need chemistry to tell them apart — but it's real: one poison (phosphate) swapped for another (arsenate), both trapped between uranyl sheets that glow faintly in the dark. Zeunerite dehydrates faster than its phosphate cousin; leave it on a dry shelf and it turns to dusty metazeunerite within months. Handle with care, store in a jar, and don't lick your fingers.

### Simulator Implementation Notes
- **New parameters needed:** U-oxidation-state (U⁶⁺ vs U⁴⁺), AsO₄ availability as distinct from PO₄
- **New events needed:** Arsenopyrite oxidation event (releases AsO₄); uraninite oxidation event (releases U⁶⁺)
- **Nucleation rule pseudocode:**
```
IF U6 > 20 ppm AND Cu > 20 ppm AND AsO4 > 10 ppm
   AND pH 5.0-7.0 AND T < 50°C AND Eh > +0.3V
   AND Cu/Ca ratio > 2.0 (Cu dominates over Ca)
   AND AsO4/PO4 ratio > 0.5 (arsenate significant)
   AND RH > 60% (hydrated form)
THEN nucleate zeunerite (tabular habit, sheet morphology)
```
- **Growth rule pseudocode:**
```
IF zeunerite crystal exists AND U6 > 10 ppm AND Cu > 10 ppm AND AsO4 > 5 ppm
   AND T < 50°C AND pH 5.0-7.0
THEN grow laterally along {001} at rate 0.3x quartz baseline
     (sheet growth: fast in a-b plane, very slow in c direction)
```
- **Habit selection logic:**
  - If growth space > 2 mm: tabular single crystals, square/octagonal
  - If growth space < 2 mm: micaceous crusts, subparallel aggregates
  - If competing with other autunite-group: smaller, more scattered
- **Dehydration products:**
  - At RH < 40% or T > 60°C: convert to metazeunerite (same position, color dulls, fluorescence weakens)

### Variants for Game
- **Variant 1: Emerald Sheets** — Large tabular crystals, >1 cm, deep emerald green. Conditions: abundant space, slow growth, high Cu/As ratio.
- **Variant 2: Micaceous Crust** — Thin overlapping sheets, pale yellow-green, waxy luster. Conditions: limited space, rapid growth, moderate chemistry.
- **Variant 3: Metazeunerite Ghost** — Dehydrated form, dull green, translucent to opaque, brittle. Forms when vug dries out (low humidity event). Same crystal positions, different appearance and properties.
