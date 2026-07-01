# Fluorapatite — Vugg Simulator Research

**Date:** 2026-06-12
**Source:** Cron batch research — Vugg game expansion
**Researcher:** 🪨✍️
**Status:** Complete — ready for builder implementation
**Paragenetic context:** Apatite-group end-member sequence. Fluorapatite, chlorapatite, and hydroxyapatite share the same Ca₅(PO₄)₃(X) structure with F/Cl/OH exchange. This is a halogen-dependent solid-solution series, not a paragenetic sequence in the traditional sense, but all three form from the same Ca-P-OH-F-Cl broth under different halogen availability conditions. Fluorapatite is the most common end-member and thermodynamically stable over the broadest conditions. Research includes all three end-members for simulator completeness.
**Blocker:** Ca not yet in trace element system (needed for all apatite-group minerals).

---

## Species: Fluorapatite (Primary End-Member)

### Identity
- **Formula:** Ca₅(PO₄)₃F
- **Crystal system:** Hexagonal (6/m, space group P6₃/m) — same as pyromorphite/mimetite/vanadinite
- **Mineral group:** Phosphate — Apatite supergroup (namesake species)
- **Hardness (Mohs):** 5
- **Specific gravity:** 3.1–3.25
- **Cleavage:** Poor on {0001} and {10ī0}
- **Fracture:** Conchoidal to uneven
- **Luster:** Vitreous to subresinous

### Color & Appearance
- **Typical color:** Colorless, white, pale green, blue-green, yellow, violet, pink; gem-quality crystals can be intensely colored
- **Color causes:**
  - Mn²⁺ → blue/violet (classic "neon" apatite color)
  - Rare earth elements (REE, especially Ce, Nd, Pr) → yellow, green-yellow
  - Fe²⁺/Fe³⁺ → green, brown, yellow
  - Cr³⁺ → green (rare)
  - Intrinsic F-apatite is colorless — all color comes from trace chromophores
- **Transparency:** Transparent to translucent; gem-quality specimens are often water-clear
- **Streak:** White
- **Notable visual features:** Hexagonal prismatic crystals with pyramidal terminations. May show complex growth zoning visible in cathodoluminescence. Commonly as tiny accessory grains in thin section, but pegmatite/hydrothermal crystals can be spectacular.

### Crystal Habits
- **Primary habit:** Hexagonal prismatic crystals with pyramidal terminations
- **Common forms/faces:** {10ī0} prism dominant, {0001} basal pinacoid, {10ī1} pyramid; combinations give barrel-shaped or elongated forms
- **Twin laws:** Rare — contact twins on {11ī1} reported
- **Varieties:**
  - **Moroxite:** Blue variety, often massive (historical name, sometimes = crystalline blue apatite)
  - **Asparagus stone:** Yellow-green variety (from Spargelstein)
  - **Neon apatite:** Intensely colored gem variety (Madagascar, Brazil)
  - **Carbonate-apatite:** CO₃²⁻ substitutes for PO₄³⁻ (biological apatite, phosphorites)
- **Special morphologies:** Tabular, acicular, massive granular, nodular (collophane — sedimentary form), earthy, botryoidal

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** Very broad — 100–1000°C depending on environment
  - Carbonatite/pegmatite: 500–800°C
  - Hydrothermal veins: 200–500°C
  - Alpine cleft-type: 100–300°C
  - Sedimentary/diagenetic: ambient to ~80°C
- **Optimal growth temperature:** 400–700°C (magmatic/hydrothermal); 15–40°C (sedimentary)
- **Decomposition temperature:** ~1650°C (melts); no relevant natural decomposition in game range
- **Temperature-dependent habits:**
  - High T (magmatic): stubby prisms, small grains (common accessory mineral)
  - Moderate T (pegmatite/hydrothermal): elongated prisms, larger crystals, better terminations
  - Low T (sedimentary): microcrystalline, nodular, collophane form
  - Very low T (biological): nanocrystalline in bones and teeth

#### Chemistry Required
- **Required elements in broth:**
  - Ca²⁺: minimum ~200 ppm (5 Ca per formula unit)
  - PO₄³⁻: minimum ~100 ppm (3 phosphate tetrahedra)
  - F⁻: minimum ~20 ppm (fluorapatite is the F end-member)
- **Optional/enhancing elements:**
  - Mn²⁺ (blue/violet coloration, fluorescence activator)
  - REE (Ce, Nd, Pr, Sm — color, CL zoning, enrichment indicator)
  - Sr²⁺ (substitutes for Ca, common in carbonatite apatite)
  - Na⁺ (substitutes for Ca with charge balance)
  - Fe²⁺/Fe³⁺ (green/yellow/brown coloration)
- **Inhibiting elements:**
  - High CO₃²⁻ → carbonate-apatite or calcite preferentially
  - High SiO₂ → competes for Ca; chalcedony/quartz may precipitate instead
  - High Mg²⁺ → competes for Ca; dolomite or magnesite may form
  - Very high Al³⁺ → may form Al-phosphates (wavellite, crandallite)
- **Required pH range:** 4–10 (very broad); optimal near-neutral to slightly alkaline (6.5–8.5). Dissolves readily in acid (pH < 2).
- **Required Eh range:** Reducing to oxidizing — apatite is stable across most Eh conditions. However, Mn²⁺ (blue color) requires reducing conditions; Mn⁴⁺ gives brown/black.
- **Required O₂ range:** Low to moderate (not sensitive to O₂ directly, but color-forming elements are)

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** No significant release; consumes Ca²⁺, PO₄³⁻, F⁻ from solution
- **Byproducts of nucleation:** If precipitating from highly supersaturated phosphate solutions, local pH may drop slightly due to phosphate protonation
- **Byproducts of dissolution/decomposition:** Dissolves in acid releasing Ca²⁺, PO₄³⁻/HPO₄²⁻, F⁻; fluorapatite is more acid-resistant than hydroxyapatite (F stabilizes the lattice against acid attack)

#### Growth Characteristics
- **Relative growth rate:** Slow to moderate — apatite is a persistent nucleator but not a rapid grower
- **Maximum crystal size:** Exceptional crystals to 20+ cm (Panasqueira, Portugal; Sapo Mine, Brazil; Ontario, Canada)
- **Typical crystal size in vugs:**
  - Magmatic accessory: 0.01–1 mm (usually microscopic)
  - Pegmatite/hydrothermal: 1–10 cm
  - Alpine cleft: 0.5–5 cm
- **Does growth rate change with temperature?** Yes — higher T in hydrothermal/pegmatite settings allows faster growth of larger crystals; low T sedimentary apatite grows as microcrystalline aggregates
- **Competes with:** Calcite (for Ca), gypsum (for Ca + sulfate), wavellite/crandallite (Al-phosphates, if Al present), fluorite (for Ca + F)

#### Stability
- **Breaks down in heat?** Melts ~1650°C; no thermal decomposition in any natural or game condition
- **Breaks down in light?** No — stable in light (unlike realgar/proustite)
- **Dissolves in water?** Very low solubility (Ksp ~10⁻⁵⁹ for fluorapatite; ~10⁻⁵⁸ for hydroxyapatite). More insoluble than hydroxyapatite, especially at low pH.
- **Dissolves in acid?** Yes — dissolves readily in HCl, HNO₃; fluorapatite is more acid-resistant than hydroxyapatite due to F stabilizing the crystal lattice
- **Oxidizes?** No — phosphate is already fully oxidized (P⁵⁺)
- **Dehydrates?** Not applicable (fluorapatite has no water; hydroxyapatite and chlorapatite also anhydrous)
- **Radiation sensitivity:** Can develop radiation halos from included U/Th minerals; REE-rich apatite may show CL zoning from radiation damage

### Paragenesis
- **Forms AFTER:** Nothing strictly required first; apatite can nucleate directly from Ca-P-F-rich fluids
  - In carbonatites: after calcite begins crystallizing, apatite saturates from residual phosphate-rich melt
  - In pegmatites: during late-stage crystallization after feldspar and quartz have depleted much of the melt
- **Forms BEFORE:** Often co-precipitates with other late minerals; in weathering environments, apatite dissolves and releases phosphate that can form secondary phosphates (pyromorphite, turquoise, etc.)
- **Commonly associated minerals:**
  - Carbonatite: calcite, dolomite, phlogopite, magnetite, pyrochlore, baddeleyite
  - Pegmatite: feldspar, quartz, mica, beryl, spodumene, tourmaline
  - Hydrothermal: quartz, calcite, fluorite, scheelite, cassiterite, wolframite
  - Metamorphic: diopside, garnet, wollastonite (in skarns/marbles)
  - Sedimentary: collophane with calcite, dolomite, chert, glauconite
- **Zone:** Primary (magmatic/pegmatite), hydrothermal, metamorphic (skarn/marble), sedimentary (phosphorite)
- **Geological environment:** Carbonatite, granite pegmatite, hydrothermal vein, Alpine cleft, skarn, marble, phosphorite, biological (bones/teeth)

### Famous Localities
- **Classic locality 1:** Panasqueira, Portugal — thick tabular gemmy apatite crystals in tin-tungsten veins; world-famous for size and clarity
- **Classic locality 2:** Sapo Mine, Ferruginha, Minas Gerais, Brazil — exceptional green hexagonal crystals to 11 cm; among the finest apatite specimens ever found
- **Classic locality 3:** Durango, Mexico — yellow gem-quality hydroxyapatite ("Durango apatite"); classic for CL studies and REE research
- **Classic locality 4:** Ehrenfriedersdorf, Erzgebirge, Germany — type locality; blue-green crystals in tin veins
- **Classic locality 5:** Kola Peninsula, Russia (Khibiny/Lovozero) — enormous apatite ore bodies in nepheline syenite; industrial phosphate source
- **Classic locality 6:** Ontario, Canada (various localities) — world-class purple, pink, and blue gem crystals
- **Notable specimens:**
  - Crystal to 20 cm from Panasqueira
  - Brazil neon-blue and neon-green gems cut to 10+ carats
  - Kola Peninsula deposits contain apatite bodies covering square kilometers ( world's largest phosphate reserves)

### Fluorescence
- **Fluorescent under UV?** Yes — highly variable depending on trace elements
- **SW (255nm) color:** Yellow, yellow-green, or blue (Mn²⁺ activated); some specimens show strong yellow CL and SW fluorescence
- **MW (310nm) color:** Yellow-green to green (Mn²⁺)
- **LW (365nm) color:** Often weak or none; some yellow-green (Mn²⁺)
- **Phosphorescent?** Rarely; some Mn-activated specimens show brief phosphorescence
- **Activator:** Mn²⁺ is the primary activator (yellow-green emission in phosphate sites); REE (especially Ce³⁺, Eu²⁺, Dy³⁺) can produce multicolor CL zoning under cathodoluminescence; U⁴⁺ and Sm³⁺ reported as activators in some specimens
- **Quenched by:** Fe²⁺ (strong quencher — Fe-rich apatite tends to be non-fluorescent); high Fe content suppresses Mn²⁺ emission

### Flavor Text

> Fluorapatite is the mineral you have never heard of but have always known. It is the phosphate in your bones, the enamel on your teeth, the fire in a matchstick's striker strip. In the Earth's crust it is nearly everywhere — a microscopic guest in almost every igneous rock — but only in rare pockets does it grow large enough to meet the eye. When it does, it arrives as hexagonal prisms of impossible clarity, colored by trace manganese into blues and violets that seem borrowed from another spectrum. The crystal does not know it built your skeleton. It simply grew, slowly, from a calcium-rich fluid that happened to carry phosphorus and fluorine in the right proportions. The same chemistry, scaled up from bone to mountain, from lifetime to geologic epoch.

### Simulator Implementation Notes
- **New parameters needed:** Ca (calcium) — critical major element, not yet in trace system. Without Ca, apatite cannot be implemented. F is already tracked (fluorite uses it). Cl is tracked (halite, atacamite, pyromorphite group use it).
- **New events needed:** `event_carbonatite_pulse` — late-stage carbonatite/pegmatite event delivering Ca + PO₄ + F together, simulating the residual melt that crystallizes apatite after calcite saturation
- **Nucleation rule pseudocode:**
```
IF trace_Ca >= 200 AND trace_P >= 100 AND trace_F >= 20
   AND pH >= 4 AND pH <= 10
   AND temperature >= 100 AND temperature <= 800
   AND vug_fill < 0.85
   → nucleate fluorapatite (max 3 per zone)
```
- **Growth rule pseudocode:**
```
IF trace_Ca > 100 AND trace_P > 50 AND trace_F > 10
   AND pH >= 5 AND pH <= 9
   AND temperature >= 80 AND temperature <= 700
   → grow at rate 3 (slow-moderate)
   IF trace_Mn > 5 → color = blue-violet
   IF trace_REE > 2 → color = yellow-green
   IF trace_Fe > 10 → color = green-brown
   ELSE → color = colorless/white
```
- **Habit selection logic:**
  - High T (magmatic, >500°C): stubby prism, small grain ("accessory" habit)
  - Moderate T (pegmatite/hydrothermal, 200–500°C): elongated prism, larger crystal, pyramidal termination ("pegmatite" habit)
  - Low T (sedimentary/supergene, <100°C): microcrystalline, nodular, massive ("collophane" habit)
- **Decomposition products:** None in game range; dissolves in acid (not modeled as thermal decomposition)

### Variants for Game
- **Variant 1: Carbonatite Blue** — blue to violet hexagonal prisms from Mn²⁺; forms in carbonatite/pegmatite settings at moderate-high temperature; color driven by trace_Mn; fluorescence: yellow-green under SW UV
- **Variant 2: Pegmatite Neon** — intensely colored green, blue, or yellow gem-quality crystals; moderate T hydrothermal/pegmatite; color driven by REE + Mn; high clarity; may show growth zoning
- **Variant 3: Hydrothermal Yellow** — yellow to yellow-green elongated prisms; moderate T hydrothermal veins (Panasqueira-style); color from REE (Ce, Nd); often associated with quartz and wolframite
- **Variant 4: Sedimentary Collophane** — massive, nodular, earthy; low T sedimentary; no crystal form (amorphous/microcrystalline); pale color; represents the "bone mineral" connection; low game value but historically significant
- **Variant 5: Alpine Clet** — small gemmy hexagonal prisms in Alpine-type fissures; low-moderate T (100–300°C); water-clear to pale blue; often with adularia and quartz

---

## End-Member Partners: Chlorapatite and Hydroxyapatite

### Chlorapatite — Ca₅(PO₄)₃Cl
- **Crystal system:** Hexagonal (same as fluorapatite)
- **Hardness:** 5
- **Specific gravity:** 3.17–3.18 (slightly lighter than fluorapatite)
- **Color:** Colorless, white, pale yellow, pale green; less commonly vivid than fluorapatite
- **Formation:** Cl-rich, F-poor environments. Layered mafic intrusions, calcium silicate marbles, diabases. Less common than fluorapatite because F is more abundant in most geologic fluids.
- **Simulator conditions:** Same as fluorapatite but with trace_Cl > trace_F. When Cl dominates, chlorapatite nucleates instead. Complete solid solution between fluorapatite and chlorapatite exists — intermediate compositions are common in nature.
- **Notable locality:** Kaiserstuhl, Germany; Kola Peninsula, Russia

### Hydroxyapatite — Ca₅(PO₄)₃(OH)
- **Crystal system:** Hexagonal (same)
- **Hardness:** 5
- **Specific gravity:** 3.08 (lightest of the three)
- **Color:** Colorless, white, pale yellow, pale green; rarely vivid
- **Formation:** F-poor, Cl-poor environments; biological apatite (bones, teeth) is carbonate-hydroxyapatite; low-T hydrothermal; metamorphic marbles.
- **Key difference:** Less acid-resistant than fluorapatite; more soluble. The F in fluorapatite stabilizes the lattice and reduces solubility.
- **Simulator conditions:** Same Ca-P requirements, but trace_F < 5 AND trace_Cl < 5, with sufficient OH (pH > 7 provides OH⁻). Hydroxyapatite nucleates when both halogens are depleted or absent.
- **Notable locality:** Durango, Mexico (yellow gem crystals); biological specimens (not a game locality but part of flavor text)

### Halogen Exchange Logic for Simulator
The three apatite end-members form a complete solid solution. In the simulator:
- **F-dominant** (F > Cl × 2, pH < 8.5): fluorapatite
- **Cl-dominant** (Cl > F × 2, pH < 8.5): chlorapatite
- **Both low** (F < 5, Cl < 5, pH > 7): hydroxyapatite
- **Intermediate** (F ≈ Cl): mixed halogen apatite — assign to fluorapatite (more common) or create "mixed-halogen" variant

---

## Cross-Reference
- `memory/research-pyromorphite.md` — Same crystal structure (apatite group), but with Pb instead of Ca and different chemistry
- `memory/research-mimetite.md` — Same structure, AsO₄ instead of PO₄
- `memory/research-vanadinite.md` — Same structure, VO₄ instead of PO₄
- `memory/research-fluorite.md` — Competes for Ca + F
- `memory/research-calcite.md` — Competes for Ca; carbonatite apatite forms alongside calcite
- `memory/research-wavellite.md` — Al-phosphate that competes when Al >> Ca
- `memory/research-beryl.md` — Same hexagonal crystal system, often co-occurring in pegmatites

---

*Apatite is the most common phosphate mineral on Earth and the mineral that built your skeleton. In the Vugg Simulator, it represents the bridge between magmatic, hydrothermal, and biological mineral formation — the same chemistry, scaled from microscopic to monumental.*
