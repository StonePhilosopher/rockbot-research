# Cobalt Oxidation Zone Paragenetic Sequence — Vugg Simulator

**Date:** 2026-06-17
**Scope:** Unified paragenetic system linking cobaltite (primary sulfarsenide) → erythrite (supergene arsenate) with nickel overlap via annabergite solid solution
**Related files:**
- `memory/research-cobaltite.md` — individual species file
- `memory/research-erythrite.md` — individual species file
- `memory/research-annabergite.md` — individual species file (Ni analogue)
- `memory/research-nickel-oxidation-zone.md` — parallel Ni sequence (nickeline → millerite → annabergite)
- `memory/research-iron-oxidation-zone.md` — Fe-As overlap (arsenopyrite → scorodite)
- `memory/research-scorodite.md` — Fe arsenate end-member
- `memory/research-arsenopyrite.md` — Fe sulfarsenide precursor

---

## Overview

The cobalt oxidation zone is one of the most visually distinctive supergene systems in mineralogy. Primary Co-As deposits weather into vivid "blooms" — crimson erythrite and apple-green annabergite — that have guided prospectors to ore bodies for centuries. The chemistry is elegant: cobaltite (CoAsS), skutterudite ((Co,Fe,Ni)As₃), and other primary Co-Ni-Fe arsenides/sulfarsenides release their metals and arsenic into oxidizing groundwater, which reprecipitates them as brightly colored, hydrous arsenates in the zone of oxidation.

Because Co²⁺ and Ni²⁺ share almost identical ionic radii and chemical behavior, they substitute freely in the vivianite-group structure, producing a continuous solid-solution series from pure erythrite (crimson) through intermediate rose-pink to pure annabergite (apple-green). The Co:Ni ratio in the oxidation zone thus becomes a powerful geochemical recorder — one that the simulator can exploit for both visual variety and chemical storytelling.

This file ties three existing research minerals into a unified formation sequence and adds Co-specific simulator mechanics not present in the individual species files.

---

## Paragenetic Sequence

### Stage 0: Primary Arsenide/Sulfarsenide Deposition (Hypogene)

**cobaltite** (CoAsS) — orthorhombic, metallic, 300–600°C
**skutterudite** ((Co,Fe,Ni)As₃) — cubic, metallic, 200–500°C
**smaltite** ((Co,Ni)As₂₋ₓ) — orthorhombic, metallic, variable
**loellingite** (FeAs₂) — orthorhombic (Fe end-member, may host Co)

*Not all are in the Vugg trace system. Cobaltite is the representative primary phase. Skutterudite would require adding a discrete Co-arsenide mineral; for simulator purposes, treat cobaltite as the sole primary source of both Co and As in this zone.*

**Simulator event:** `event_cobalt_vein` — primary cobaltite nucleates in reducing, As-rich hydrothermal fluid at T > 300°C, releasing minor Fe and Ni into the broth as substitutional impurities.

### Stage 1: Early Oxidation (Tarnish and Surface Alteration)

As cobaltite nears the surface or encounters oxidizing fluid:
- Surface tarnish develops: pink to violet "cobalt bloom" (incipient erythrite film)
- Arsenic oxidizes from As³⁻/As⁰ to AsO₄³⁻
- Cobalt remains as Co²⁺ (stable in oxidizing surface waters)
- Sulfur oxidizes to SO₄²⁻ and is largely leached away

**Key insight:** The initial oxidation of cobaltite does NOT require neutralization. Even mildly acidic waters (pH 4–6) can begin stripping As and Co from the sulfarsenide lattice. The pH rises later as carbonates or wall-rock buffering neutralize the acid.

**Simulator event:** `event_cobaltite_tarnish` — when cobaltite is exposed to oxidizing fluid (Eh > +0.2 V) at T < 100°C, its surface develops a thin pink coating. This is cosmetic but signals the transition to Stage 2.

### Stage 2: Supergene Arsenate Precipitation (The Bloom)

**erythrite** (Co₃(AsO₄)₂·8H₂O) — monoclinic, crimson, <50°C
**annabergite** (Ni₃(AsO₄)₂·8H₂O) — monoclinic, apple-green, <50°C

The two minerals crystallize from the same fluid under identical conditions. Which one dominates depends entirely on the Co:Ni ratio:

| Co:Ni ratio | Dominant phase | Color | "Bloom" name |
|---|---|---|---|
| >10:1 | Erythrite | Deep crimson | Cobalt bloom |
| 3:1 to 10:1 | Erythrite-rich intermediate | Rose-pink | Pink bloom |
| 1:3 to 3:1 | Mixed intermediate | Violet/mauve | Transitional |
| <1:3 | Annabergite-rich intermediate | Pale rose-green | Green-shifted |
| <1:10 | Annabergite | Apple-green | Nickel bloom |

**Color continuum mechanic:** In the simulator, the color of a newly nucleated vivianite-group crystal should interpolate continuously between crimson (pure Co) and apple-green (pure Ni). A crystal nucleating at Co:Ni = 1:1 should appear violet-gray — a real but rare intermediate observed at Bou Azzer, Morocco.

**Solid-solution series completeness:** The vivianite group has end-members for Fe²⁺ (vivianite = Fe₃(PO₄)₂·8H₂O), Mn²⁺ (manganese-bearing vivianite), Mg²⁺ (hörnesite), and Zn²⁺ (köttigite). Only Co²⁺ and Ni²⁺ are relevant to the current trace system, but the architecture supports future expansion if Mg, Zn, or Mn are promoted to primary elements.

### Stage 3: Advanced Weathering and Dehydration

As the oxidation zone dries out or is buried beneath younger cover:
- Erythrite/annabergite lose water → transition to anhydrous Co/Ni arsenates (rare in nature)
- More commonly: continued leaching removes As, leaving residual Co/Ni oxides/hydroxides (heterogenite, asbolane — not in trace system)
- Carbonate-bearing waters may replace arsenate with carbonate → spherocobaltite (CoCO₃) or gaspeite ((Ni,Mg,Fe)CO₃) — neither in trace system

**Simulator event:** `event_bloom_dehydration` — if an erythrite/annabergite crystal persists in a warming, drying environment (>50°C, humidity falling), it begins to dehydrate and turns dull. Visual: loss of transparency and luster, color shifts to paler, chalky tones. Eventually dissolves if As is leached away.

### Stage 4: Cross-Contamination with Iron and Calcium

Real oxidation zones are chemically messy. Three important cross-system interactions:

**Fe contamination:** If arsenopyrite (FeAsS) or löllingite (FeAs₂) is present in the same deposit, Fe²⁺ enters the arsenate fluid. At high Fe:(Co+Ni) ratios, **parasymplesite** (Fe₃(AsO₄)₂·8H₂O) — the pale blue-green Fe end-member of the vivianite group — may coprecipitate or even dominate. In the simulator, this would appear as a desaturation of erythrite/annabergite color toward gray-green, or as a separate dull green crust.

**Ca contamination:** If calcite/dolomite wall rock is present, Ca²⁺ may partially substitute into the vivianite structure, producing **roselite** (Ca₂Co(AsO₄)₂·2H₂O) or **dudgeonite** (Ca₂Ni(AsO₄)₂·2H₂O) — rare but documented at Bou Azzer and Creetown, Scotland. These are Ca-dominant, not vivianite-structure; they'd need separate simulator logic if Ca becomes a primary element.

**Mg enrichment:** The Bou Azzer study (Ahmed et al. 2017) found Mg-enriched erythrite with formula (Co₂.₂₅Mg₀.₅₈Ni₀.₁₄...)₃(AsO₄)₂·8H₂O, showing that Mg readily substitutes into the Co site. This shifts the color toward paler pink and reduces specific gravity.

---

## Formation Conditions (Zone-Level Parameters)

### Temperature Profile
| Stage | T range | Driver |
|---|---|---|
| Primary deposition | 300–600°C | Hydrothermal or contact metamorphic |
| Cooling/tarnish | 100–200°C | Ascent toward surface |
| Supergene bloom | 10–30°C | Ambient surface/groundwater |
| Dehydration/reburial | >50°C | Burial, volcanic heating, or climate shift |

### Chemistry Profile
| Parameter | Primary (cobaltite) | Supergene (erythrite/annabergite) |
|---|---|---|
| Eh | −0.2 to +0.1 V (reducing) | +0.3 to +0.6 V (oxidizing) |
| pH | 5–8 (near-neutral hydrothermal) | 5–8 (buffered by wall rock) |
| Co (ppm) | ≥50 (cobaltite saturates at ~50 ppm) | ≥10 (residual from leaching) |
| Ni (ppm) | ≥20 (if annabergite present) | ≥10 (if nickeline/siegenite leached) |
| As (ppm) | ≥100 (cobaltite requirement) | ≥50 (as AsO₄³⁻ from oxidation) |
| S (ppm) | ≥50 (cobaltite requirement) | 0–10 (leached away) |
| O₂ | Low (sealed system) | Moderate (oxidizing groundwater) |

### Critical Ratios
- **Co:Ni** → controls erythrite vs annabergite dominance and color
- **Co+Ni : Fe** → controls whether vivianite-group blooms or parasymplesite/pitticite dull crusts form
- **As : PO₄** → if phosphate is present (from apatite wall rock), the phosphate arsenate **erythrine** (Co₃((AsO₄)(PO₄))₂·8H₂O) may form as an intermediate

---

## Cross-Zone Interactions

### With Nickel Oxidation Zone
The Co and Ni oxidation zones are chemically inseparable in nature. The same groundwater leaches both metals from their primary arsenides and coprecipitates them as the vivianite-group solid solution.

- **Nickeline zone** (memory/research-nickel-oxidation-zone.md): If the primary deposit is Ni-dominant (nickeline, gersdorffite), annabergite dominates the bloom. Co traces give pink zones within green masses.
- **Cobaltite zone** (this file): If the primary deposit is Co-dominant (cobaltite, skutterudite), erythrite dominates. Ni traces give green zones within crimson masses.
- **Mixed zone** (most common): Intermediate colors — violet, mauve, rose — testify to comparable Co and Ni release rates.

**Simulator mechanic:** `event_cobalt_nickel_overlap` — when both Co and Ni are present in the broth at comparable levels (>10 ppm each), nucleation should produce crystals whose color is dynamically determined by the instantaneous Co:Ni ratio, not a fixed species assignment. One "crystal" could have a crimson core (early, Co-rich fluid) and a green rim (later, Ni-dominated pulse).

### With Iron Oxidation Zone
If arsenopyrite (FeAsS) or pyrite (FeS₂) is the primary phase instead of cobaltite:
- Fe²⁺ competes with Co²⁺/Ni²⁺ for arsenate sites
- At Fe >> Co+Ni: parasymplesite (pale blue-green) or scorodite (yellow-brown) forms instead
- At comparable levels: mixed Fe-Co arsenates with dull olive-gray colors
- This is the classic "gossan" problem — oxidized sulfide caps look brown and dull because Fe dominates the supergene budget

### With Silver Zone
Many historical Co-Ag deposits (Cobalt, Ontario; Schneeberg, Saxony) have native silver associated with primary cobaltite/skutterudite. The same oxidizing fluids that release Co and As can also liberate Ag⁺, which may precipitate as native silver or acanthite in reducing pockets deeper in the oxidation profile.

---

## Famous Localities

### Bou Azzer, Anti-Atlas Mountains, Morocco
The world's finest erythrite locality and the type locality for Co mineralogy. Hydrothermal Co-Ni-As veins in Precambrian ophiolitic serpentinite produce spectacular crimson erythrite sprays up to 2 cm, often coating skutterudite and cobaltite. The 2017 study by Ahmed et al. documented Mg-enriched compositions. Associated minerals: roselite, alloclasite, native bismuth, and uvarovite (from chromite alteration in the same host rocks).

### Cobalt, Ontario, Canada
The town is named for the mineral, not the other way around. Ag-Co arsenide veins in Proterozoic diabase produced massive primary cobaltite and skutterudite. Oxidation produced extensive erythrite and pink "cobalt bloom" that guided prospectors to the silver ore beneath. Also known for银矿 (silver) — the Co was a byproduct of Ag mining.

### Schneeberg, Saxony, Germany
Historic Erzgebirge mining district. Co-Ni-Ag-Bi veins in gneiss produced cobaltite, skutterudite, safflorite (CoAs₂), and nickeline. Weathering produced world-class erythrite and annabergite specimens collected since the 16th century. Many type specimens in the Freiberg Mining Academy collections.

### Tunaberg, Sweden
Co-As deposit in amphibolite-facies metavolcanics. Produced museum-quality cobaltite crystals with characteristic striated pseudocubes and violet tarnish. Erythrite forms delicate pink films on joint surfaces.

### Cornwall, England (Huel Unity, Huel Gorland)
Cornish Sn-W-Cu-As deposits carry minor Co and Ni. Oxidation of arsenopyrite and löllingite produced modest erythrite and annabergite, historically important as "cobalt" pigment sources before synthetic pigments.

---

## Simulator Mechanics

### Events
| Event | Trigger | Effect |
|---|---|---|
| `event_cobalt_vein` | T > 300°C, Co≥50, As≥100, S≥50, Eh < +0.1 | Nucleate cobaltite (max 4 crystals) |
| `event_cobaltite_tarnish` | T < 100°C, Eh > +0.2, cobaltite present | Cosmetic pink film on cobaltite surfaces; signals Stage 1 |
| `event_cobalt_bloom` | T < 50°C, Co≥10, As≥50 (as AsO₄³⁻), Eh > +0.3 | Nucleate erythrite or annabergite depending on Co:Ni ratio |
| `event_cobalt_nickel_overlap` | Co≥10 and Ni≥10 simultaneously | Dynamic color crystal: hue = f(Co:Ni ratio) at nucleation time |
| `event_bloom_dehydration` | T > 50°C on existing erythrite/annabergite | Gradual loss of luster/transparency; dull pale color |
| `event_iron_contamination` | Fe > 2×(Co+Ni) in bloom fluid | Suppress erythrite/annabergite nucleation; favor scorodite/parasymplesite |

### Zone Tags
- `zone_hypogene_cobalt` — cobaltite-bearing
- `zone_supergene_cobalt` — erythrite/annabergite-bearing
- `zone_mixed_co_ni` — intermediate colors
- `zone_iron_dominated` — dull Fe arsenate caps

### New Parameters
- `Co_Ni_ratio` — derived from broth Co ppm / Ni ppm
- `iron_budget` — derived from Fe ppm relative to Co+Ni
- `arsenate_speciation` — AsO₄³⁻ vs HAsO₄²⁻ vs H₂AsO₄⁻ (pH-dependent)

### Pseudomorphs
- **Cobaltite → erythrite:** Cracks and voids in oxidized cobaltite masses fill with radial erythrite needles, preserving the original crystal outline. Pseudomorphous after cobaltite is documented but uncommon — usually the cobaltite simply dissolves and erythrite nucleates nearby.
- **Skutterudite → erythrite:** More common. Cubic skutterudite crystals develop internal fractures that fill with pink erythrite, producing a "cobaltized" appearance.

---

## Flavor Text — Individual Species (for Game Epilogue)

### Cobaltite
> A blade of silver steel with a secret blush. Where cobaltite meets the air, it betrays itself — a faint rose-pink tarnish spreads across the metallic face like a fever flush, whispering to prospectors that cobalt sleeps beneath. The striations on its pseudocubes record twin laws written in arsenic and sulfur, a crystalline poem in a language almost no one speaks anymore. It is the quiet sentinel: you would walk past it a hundred times before you noticed the pink.

### Erythrite
> They called it "cobalt bloom" — as if the earth itself were flowering in crimson. Erythrite is the sunset of a cobalt deposit: the last beautiful thing before the metal is leached away forever. Its needles cluster in radiating sprays no larger than a fingernail, each one a perfect monoclinic prism of Co²⁺ and arsenate, grown from groundwater so dilute that a wineglass of it would contain barely enough cobalt to stain a tooth. Prospectors learned to read the bloom. Where erythrite crusted the gossan, silver and cobalt waited below.

### Annabergite
> The green ghost of nickel. Where nickeline weathers, annabergite grows in filmy crusts so thin you could crush them between two breaths. It is the softer twin of erythrite — same structure, same water-weak lattice, same habit of radiating into nothing from a center that no longer exists. The color shifts with its mood: pure Ni gives apple-green, but let a little cobalt in and it blushes rose-pink. It is a mineral that cannot decide whether it is healing or remembering.

### Intermediate (Co,Ni)-Bloom (Dynamic Variant)
> Violet twilight between two fires. This is not a species but a moment — the exact ratio of cobalt to nickel in a drop of water, frozen into a crystal that will never be repeated. Some are mauve, some lilac, some the bruised purple of a healing wound. The vivianite group has no loyalty to purity; it crystallizes what is offered. Every intermediate crystal is a census of its fluid, a snapshot of a chemistry that has already changed.

---

## References

1. Ahmed et al. (2017) — "Mg-enriched erythrite from Bou Azzer, Anti-Atlas Mountains, Morocco: geochemical and spectroscopic characteristics." *Mineralogy and Petrology* 111: 765–781. DOI: 10.1007/s00710-017-0545-8
2. Gaines et al. (1997) — *Dana's New Mineralogy: The System of Mineralogy of James Dwight Dana and Edward Salisbury Dana*, 8th ed. Wiley.
3. Klein & Dutrow (2007) — *Manual of Mineral Science*, 23rd ed. Wiley.
4. Nickel & Nichols (1991) — *Mineral Reference Manual*. Van Nostrand Reinhold.
5. Palache et al. (1951) — *Dana's System of Mineralogy*, 7th ed., Vol. II. Wiley.
6. Wikipedia contributors (2025–2026) — "Cobaltite," "Erythrite," "Annabergite," "Skutterudite."
7. grokipedia.com — "Erythrite" and "Cobaltite" entries (accessed 2026-06-17)
8. GeologyIn — "Incredible Erythrite Crystals" (accessed 2026-06-17)
9. CrystalMountain.com.au — "Erythrite" mineral description

---

*Research completed: 2026-06-17. This is a unified paragenetic sequence file linking three existing individual species research files. No new elements needed — Co, Ni, As, S, Fe, O₂ all in trace system.*
