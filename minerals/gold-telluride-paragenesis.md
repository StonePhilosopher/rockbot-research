# Gold-Telluride Paragenesis — Master File

**Date:** 2026-06-11
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering the epithermal gold-telluride system: calaverite (AuTe₂) → sylvanite ((Au,Ag)Te₂) → hessite (Ag₂Te) → native tellurium (Te) → native gold (Au), with petzite (Ag₃AuTe₂) and krennerite (orthorhombic AuTe₂) as variant branch members. Temperature-Au:Ag-Te compositional controls.
**Related files:**
- `memory/research-calaverite.md` — AuTe₂, monoclinic, Au-dominant telluride
- `memory/research-sylvanite.md` — (Au,Ag)Te₂, monoclinic, Au+Ag telluride
- `memory/research-hessite.md` — Ag₂Te, monoclinic/cubic polymorph, Ag-dominant telluride
- `memory/research-native-tellurium.md` — Te⁰, trigonal, residual element
- `memory/research-native-gold.md` — Au⁰, cubic, terminal liberation product
- `memory/research-silver-oxidation-zone.md` — Parallel silver system for cross-reference
- `memory/research-copper-oxidation-zone.md` — Cross-metal deposit overlaps

---

## The Story This Sequence Tells

Tellurium is a cosmic orphan — rarer than platinum in Earth's crust, stripped from the planet during accretion by volatile hydrides that escaped to space. When it does appear, it arrives in the latest, coolest fluids of epithermal gold systems, dissolved as HTe⁻ and Te²⁻, carrying gold and silver in complexes that crystallize only when the fluid has cooled past the sulfide stage, past the base-metal stage, into the realm of trace elements and stubbornness.

The gold-telluride sequence is governed by a single ternary diagram: Au-Ag-Te. The temperature, the metal ratios, and the exhaustion of sulfur determine which mineral forms. It's not a redox story like copper or iron — gold doesn't change valence here. It's a stoichiometric story: who gets paired with whom, in what ratio, at what temperature.

Gold arrives first. It has the strongest affinity for tellurium. Where Au and Te meet at 200–350°C, calaverite crystallizes — AuTe₂ in bladed monoclinic prisms with their famously incommensurate crystal structure. But most epithermal fluids carry silver too. As the Au:Ag ratio drops, calaverite gives way to sylvanite — (Au,Ag)Te₂ — the same structure but with silver sharing the gold sites. Drop the temperature further, let silver dominate, and hessite appears: Ag₂Te, silver's answer to calaverite. The Ag:Au ratio climbs through the sequence like a thermometer in reverse.

Only when every metal has been satisfied does native tellurium appear — the residue, the excess, the element that arrived too late for its own party. And when any of these tellurides encounters oxygen, they surrender their tellurium to the oxidizing fluid and liberate native gold — the terminal mineral of the sequence, the element that outlasts empires.

In the Cresson Mine at Cripple Creek, this sequence played out in real time: calaverite crystallized from the 300°C fluid, sylvanite from the 250°C continuation, hessite from the 200°C tail. Miners couldn't see the gold. It was locked in tellurium, chemically invisible. The ore looked like dull gray rock. Only roasting could liberate it — heating the tellurides until they decomposed, releasing gold that had been hiding in plain sight for twenty million years.

That's the vugg's lesson: sometimes the most valuable mineral is the one you can't see.

---

## The Full Sequence (T-Au:Ag-Te Controlled)

```
HIGH TEMPERATURE ──────────────────────── LOW
     │                                    │
     ▼                                    ▼
┌─────────────┐                    ┌─────────────┐
│ CALAVERITE  │  Au:Ag > 3:1       │  HESSITE    │  Ag >> Au
│  AuTe₂      │  T = 200–350°C     │  Ag₂Te      │  T = 100–250°C
│  monoclinic │  Au-dominant       │  monoclinic │  Ag-dominant
│  bladed     │                    │  massive/   │
│  prisms     │                    │  pseudocubic│
└──────┬──────┘                    └──────┬──────┘
       │                                    │
       │ Au:Ag = 1:1 to 3:1                 │
       ▼                                    │
┌─────────────┐                             │
│  SYLVANITE  │                             │
│ (Au,Ag)Te₂  │─────────────────────────────┘
│  monoclinic │        Both: Te-limited
│  bladed     │        Both: late-stage
└──────┬──────┘        Both: low-sulfidation epithermal
       │
       │ Te exceeds Au+Ag capacity
       ▼
┌─────────────┐
│ NATIVE Te   │  Residual Te
│  trigonal   │  T = 100–300°C
│  prismatic/ │  "The unclaimed guest"
│  filamentous│
└──────┬──────┘
       │
       │ OXIDATION (surface or vug reopening)
       ▼
┌─────────────┐
│ NATIVE Au   │  Terminal liberation
│  cubic      │  Au⁰ freed from telluride lattice
│  octahedral/│  "The metal that outlasts empires"
│  dendritic  │
└─────────────┘
```

### Branch Members (Less Common)
- **Krennerite** — orthorhombic AuTe₂, polymorph of calaverite (monoclinic). Same composition, different symmetry. Stable at slightly different T-P conditions. Visually similar; distinguishable by XRD or polished section optical properties.
- **Petzite** — Ag₃AuTe₂, cubic. Higher Ag:Au ratio than sylvanite. Distinct structure; forms in Ag-rich, Au-poor telluride fluids. Less common than hessite but documented at Cripple Creek and Kalgoorlie.
- **Stützite** — Ag₇Te₄, intermediate between hessite (Ag₂Te) and empressite (AgTe). Very rare; not in species list.

---

## Cross-Cutting Controls

### Temperature as the Primary Axis
| Temperature | Dominant Mineral | Crystal Form | Key Feature |
|-------------|------------------|--------------|-------------|
| 350–400°C | Calaverite | Bladed prisms | Au-dominant, highest T |
| 250–350°C | Calaverite + Sylvanite | Mixed | Au:Ag = 3:1 → 1:1 |
| 150–250°C | Sylvanite + Hessite | Bladed + massive | Ag rising, Au falling |
| 100–200°C | Hessite + Native Te | Pseudocubic + filiform | Ag-dominant, Te residual |
| <100°C | Native Te (+Au lib.) | Prismatic/dendritic | Oxidation liberation |

### Au:Ag Ratio as the Secondary Axis
The Au:Ag ratio in the fluid determines which telluride dominates, independent of temperature within broad ranges:
- **Au:Ag > 3:1** → Calaverite (even at relatively low T)
- **Au:Ag = 1:1 to 3:1** → Sylvanite
- **Au:Ag < 1:1** → Hessite or petzite
- **Ag >> Au, Te >> (Au+Ag)** → Hessite + native tellurium

### Te Availability as the Gatekeeper
Without sufficient tellurium, none of this sequence happens. Gold and silver form their sulfides instead (acanthite, electrum) or go into solid solution in pyrite/arsenopyrite. The telluride stage requires:
- **Sulfur depletion** — S must be consumed by earlier pyrite, chalcopyrite, galena, sphalerite
- **Te enrichment** — a late-stage magmatic-hydrothermal fluid pulse carrying volatiles (Te, Hg, Sb, As)
- **Reducing conditions** — Te must be present as Te²⁻ (or HTe⁻), not oxidized tellurite

### pH and Eh Windows
Unlike copper or iron oxidation zones, the gold-telluride sequence is **not strongly pH-dependent** — it forms across pH 4–8. The key variable is **Te speciation**:
- **Reducing (Eh < 0 mV, low O₂):** Te²⁻ stable → tellurides nucleate
- **Oxidizing (Eh > +200 mV):** Te²⁻ → TeO₃²⁻ (tellurite) or TeO₄²⁻ (tellurate); tellurides decompose, liberating native gold
- **Extremely reducing:** Native tellurium can form if Te exceeds metal binding capacity

---

## Paragenetic Position in Multi-Metal Deposits

### Typical Epithermal Sequence (Low-Sulfidation)
```
EARLY ───────────────────────────────────── LATE

Stage I:   Quartz + pyrite ± adularia
           (vein opening, fluid ascent)

Stage II:  Base metal sulfides
           Galena + sphalerite ± chalcopyrite
           (cooling, metal concentration)

Stage III: ⭐ GOLD-TELLURIDE STAGE ⭐
           Calaverite → sylvanite → hessite
           ± native tellurium
           ± petzite, krennerite
           (Te pulse, Au+Ag saturation)

Stage IV:  Native gold
           (from telluride oxidation/remobilization
            OR direct precipitation in bonanza zones)

Stage V:   Carbonates ± barite ± fluorite
           (late-stage, lowest T, neutralizing fluids)
```

### Cross-Zone Interactions
- **Silver sulfosalt zone:** Realgar/orpiment (As-S) and proustite/pyrargyrite (Ag-As-Sb-S) can overlap with the telluride stage in some epithermal deposits. These share the Ag budget but compete for As/S vs. Te.
- **Copper oxidation zone:** Below the telluride horizon, copper minerals (chalcopyrite → bornite → chalcocite → cuprite → malachite/azurite) form a separate redox ladder. No direct competition for elements except space.
- **Mercury zone:** Coloradoite (HgTe) and cinnabar (HgS) often accompany tellurides in epithermal systems. Hg competes for Te but forms its own discrete minerals.
- **Selenium crossover:** Naumannite (Ag₂Se) and clausthalite (PbSe) are the selenium analogs of hessite and altaite. When Se > Te in late fluids, the selenide branch activates.

---

## Key Geological Settings

### Cripple Creek, Colorado (USA)
The type locality for the gold-telluride paragenesis. Oligocene alkaline diatreme complex. Sequence: quartz-pyrite → calaverite + sylvanite + krennerite → native gold → fluorite-barite. The Cresson Mine produced bonanza ore — visible gold was rare; the wealth was in tellurides. Some of the finest gold-telluride specimens in the world come from here.

### Kalgoorlie, Western Australia
Archean greenstone belt. Telluride stage superimposed on older orogenic gold. Calaverite and sylvanite in late carbonate-quartz veins crosscutting earlier sulfide mineralization. The "Golden Mile" — one of the richest gold districts on Earth.

### Sacarîmb (Nagyág), Transylvania (Romania)
The namesake of sylvanite. Historic telluride deposit in Neogene volcanic rocks. Produced superb sylvanite crystals, hessite, native tellurium, petzite, and the rare mineral "nagyágite" (Pb₅Au(S,Te)₂). One of the most mineralogically complex telluride localities.

### Emperor Mine, Vatukoula (Fiji)
Low-sulfidation epithermal gold-telluride system in Pliocene volcanic rocks. Native gold + calaverite + sylvanite + tellurides in adularia-quartz veins. One of the few major telluride deposits in the Pacific.

### Zod (Vayk-Sisian), Armenia
Well-crystallized hessite and native tellurium in a lesser-known but mineralogically rich epithermal system. Good example of the late-stage telluride residue.

---

## Simulator Events

### `event_gold_telluride_pulse`
**Trigger:** Late-stage magmatic volatile release (Te, Hg, Sb, As) after main sulfide stage.
**Effect:** Injects trace_Te (+10–50 ppm), trace_Au (+0.5–2 ppm), trace_Ag (+1–5 ppm) into broth.
**Narrative:** "A late pulse of volatile-rich fluid enters the vug, carrying the rare elements that escaped earlier precipitation. The air smells faintly of garlic — tellurium's signature."

### `event_telluride_cooling`
**Trigger:** Temperature drops from 350°C → 200°C over multiple steps.
**Effect:** Progressive mineral zonation: calaverite (high T) → sylvanite (mid T) → hessite (low T).
**Narrative:** "The vein cools. Gold's grip on tellurium loosens as silver muscles in."

### `event_telluride_oxidation`
**Trigger:** Vug reopening or fluid influx with elevated O₂.
**Effect:** All tellurides (calaverite, sylvanite, hessite) begin slow oxidative decomposition. Each releases native gold over time. Native tellurium oxidizes to tellurite crust.
**Narrative:** "Oxygen enters the vug — the tellurides begin to surrender their gold."

### `event_native_gold_liberation`
**Trigger:** Any telluride reaches critical oxidation state OR temperature exceeds decomposition threshold (>450°C for calaverite, >350°C for sylvanite).
**Effect:** Telluride dissolves; native gold nucleates on the same site (pseudomorph-like). Au remains; Te exits to fluid as tellurite.
**Narrative:** "A crystal of calaverite darkens, then splits — and where the telluride stood, a flake of native gold gleams."

---

## Individual Species Flavor Text

### Calaverite
> Calaverite is the mineral that broke crystallography. For decades its faces refused to index — the laws of rational indices simply didn't apply. The reason: an incommensurate modulation wave rippling through the tellurium positions, driven by gold atoms fluctuating between Au⁺ and Au³⁺. The crystal is arguing with itself about what charge gold should be, and the result is a structure that never quite repeats. It's also, incidentally, one of the most important gold ores on Earth. Cripple Creek was built on calaverite. The gold is hiding in the tellurium — invisible to the naked eye, locked in a crystal that can't make up its mind.

### Sylvanite
> Sylvanite is the most common gold telluride, and also the one that can't sit in the sun. It's photosensitive — leave a specimen on the windowsill and it darkens, tarnishing from silver-white to a sullen black. The gold is still in there, locked in the crystal lattice, but the surface surrenders. Named not for sylvite (KCl) but for Transylvania, where it was first identified at the legendary Nagyág mining district. Miners called it "graphic tellurium" for the intergrown bladed crystals that looked like cuneiform scratched into the rock. The Au:Ag ratio varies from 1:1 to 3:1 — it can't decide if it's a gold mineral or a silver mineral.

### Hessite
> Hessite is the quiet rich one — silver and tellurium holding hands where the vein goes cold. It hides in the late fluids, after the pyrite party, after the quartz has mostly crystallized, when the broth is down to trace elements and stubbornness. At 155°C it snaps from cubic to monoclinic, a phase transition that writes itself into the crystal as fine lamellae — a ghost of the hotter world it came from. Most miners never see it. It's small, gray, and looks like galena's boring cousin. But crack the right vein and hessite means you're in the tellurium zone, and the tellurium zone means gold.

### Native Tellurium
> Tellurium is the element that arrived too late for the party. It's rarer than platinum in Earth's crust — a cosmic abundance that got stripped from the planet during formation by volatile hydrides escaping to space. When it does show up, it arrives in epithermal gold veins, dissolved in low-temperature hydrothermal fluids alongside the metals that covet it desperately. Gold forms calaverite; silver makes hessite. Native tellurium only crystallizes when every metal has had its fill and there's still tellurium left over — a rare extravagance. The resulting tin-white hexagonal prisms tarnish almost immediately in air, their metallic gleam fogging to a dull gray. It's one of the few minerals defined by what failed to happen: it exists because the metals couldn't consume all of it. A relic of excess, striated and fleeting.

### Native Gold
> Gold is the exception to every rule. It does not oxidize, does not tarnish, does not dissolve in water or single acids, does not decompose in heat, does not react with oxygen, does not corrode in salt. It is the most noble of the noble metals — the element that chemistry forgot how to touch. In a telluride vein, calaverite and sylvanite crystallize first, binding gold in telluride lattices. Only when the tellurium is exhausted, or the temperature drops, or the fluid evolves, does the gold appear — native, free, the terminal mineral of the paragenesis. The finest crystallized gold comes from open spaces: octahedra of impossible perfection, wire filaments thinner than hair and longer than fingers, dendrites that branch like frozen lightning. These are the shapes gold chooses for itself when it has room and time.

---

## Game Mechanics

### Unified Supersaturation Logic
Rather than separate supersaturation functions for each telluride, implement a **single `σ_gold_telluride`** that evaluates the Au:Ag:Te triangle:

```
σ_base = f([Te], [Au], [Ag], T)

IF Au:Ag > 3 AND T > 200 → calaverite_nucleation_preference = HIGH
IF 1 < Au:Ag < 3 AND T > 100 → sylvanite_nucleation_preference = HIGH
IF Ag > Au AND T < 250 → hessite_nucleation_preference = HIGH
IF Te > (Au + Ag) * 2 AND all_metals_bound → native_tellurium_preference = HIGH
```

Each mineral still gets its own supersaturation function for independent growth rates, but the **preference weights** are drawn from the unified paragenesis controller.

### Temperature-Dependent Polymorph Switches
- **Hessite:** Nucleation above 155°C → cubic habit flag. When system cools below 155°C, update flag to monoclinic + add "transformation lamellae" texture. No dissolution — just visual/state change.
- **Calaverite/Krennerite:** Random polymorph assignment at nucleation (85% calaverite/monoclinic, 15% krennerite/orthorhombic). Same growth rate, different visual.

### Photosensitivity Mechanic (Sylvanite)
- Sylvanite gains a `light_exposure` counter per step.
- After N steps in illuminated vug: color shifts silver-white → dark gray-black.
- Dark storage reverses slowly. In game terms: "store in dark" toggle in collector view.
- Narrative hook: "This sylvanite has been sitting in light. Its surface has surrendered."

### Telluride Decomposition → Native Gold
- Each telluride tracks an `oxidation_state` field.
- When O₂ spikes OR temp exceeds decomp threshold: telluride dissolves, releasing Au to fluid.
- If Au in fluid + open space: native gold nucleates at the same coordinates (pseudomorph effect).
- Visual: telluride crystal darkens, cracks, then "reshines" as native gold film/crystals on the surface.

### Cross-Zone Integration Points
- **Silver oxidation zone:** If the same vug has Ag-rich fluids post-telluride, acanthite or native silver may form on the telluride remnants. Document in zone history as "superimposed paragenesis."
- **Copper oxidation zone:** Independent but spatially overlapping in porphyry deposits. The simulator should allow both sequences to coexist — copper zone below, telluride zone above, gold appearing in both.
- **Mars mode:** Iron oxidation dominates Mars, but if a hypothetical telluride event fires, the sequence would proceed identically — gold doesn't care about planetary gravity.

---

## Blockers & Dependencies

- **Au not yet in trace element system.** Required for all five minerals in this sequence. Addition priority: HIGH — Au is fundamental to gold deposits, and the telluride paragenesis is one of the most distinctive mineral associations in economic geology.
- **Te is in the 30-element trace list.** Verify tracking implementation.
- **Ag is already tracked** (acanthite, argentite, native silver).
- **No new chemistry concepts needed.** Unlike copper/iron/lead/zinc oxidation zones, this sequence doesn't require new pH/Eh mechanics — it runs on temperature and compositional ratios within the existing framework.

---

## References
1. Markham, N.L. (1960). "The geology of the Kalgoorlie goldfield." *Geological Survey of Western Australia*, Bulletin 115.
2. Geller, M. & Atkinson, W.W. (1991). "Telluride mineralogy of the Cresson Mine, Cripple Creek, Colorado." *Colorado Geological Survey*, Resource Series 28.
3. Thompson, T.B. et al. (1985). "Gold-telluride mineralization at the Cripple Creek deposit, Colorado." *Economic Geology*, 80(6), 1869–1883.
4. Ciobanu, C.L. et al. (2006). "Te and Se mineralogy of the high-sulfidation Kochbulak and Kairagach epithermal gold telluride deposits." *Mineralogy and Petrology*, 87(3–4), 351–374.
5. Ahmad, M. et al. (2006). "Mineralogy, geochemistry and genesis of alkaline igneous rock-related gold-silver telluride deposits of central Montana." *Geological Magazine*, 143(2), 189–209.
6. Grundler, P.V. et al. (2013). "Gold-in-pyrite and telluride mineralogy at Cripple Creek." *Mineralium Deposita*, 48(3), 319–338.
7. Knipe, S.W. et al. (2021). "Types of tellurium mineralization of gold deposits of the Aldan Shield." *Minerals*, 11(7), 698.
8. Saunders, J.A. et al. (2014). "Hydrothermal transport, deposition, and fractionation of the REE." *Geochimica et Cosmochimica Acta*, 144, 39–59.
9. Grokipedia — Telluride mineral: https://grokipedia.com/page/Telluride_mineral (Au-Ag-Te ternary phase relations at 120–300°C)
10. Mindat.org — individual species pages for calaverite, sylvanite, hessite, native tellurium, native gold.

---

*"The gold is hiding in the tellurium — invisible to the naked eye, locked in a crystal that can't make up its mind."*
