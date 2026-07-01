# Vugg Simulator — Game Mode Scale Progression Research

**Date:** 2026-05-22
**Source:** Web research + synthesis for Vugg Simulator expansion
**Status:** Complete — Design input for Vug → Pocket → Cave mode progression

---

## Executive Summary

Real geological voids scale from millimeters to kilometers, and crystal growth scales with them — not linearly, but through distinct physical regimes. A vug is a closed cavity where fluid is trapped. A pocket is a semi-open miarolitic void where fluid can exchange with surrounding rock. A cave is an open-flow system where water continuously brings new chemistry. Each regime demands different simulator mechanics: fluid dynamics, chemistry replenishment, crystal size limits, and time scales.

This research note compiles the geological data needed to ground the three proposed game modes in reality.

---

## 1. Crystal Size vs. Void Size vs. Growth Duration — Real Data

### Pegmatite Pockets (Miarolitic Cavities)

The definitive modern study is **Webber et al. (1999)** and the follow-up **Nabelek et al. (2020, *Nature Communications*)** on the Stewart pegmatite, Pala District, California:

| Parameter | Value | Source |
|-----------|-------|--------|
| Pegmatite body width | ~50 m | Stewart pegmatite |
| Cooling time (650°C → 550°C) | ~9 years | Conductive cooling model (Webber et al.) |
| Quartz crystal size in cavities | 2–10 cm | Measured from miarolitic cavities |
| Inferred growth rate | **cm-scale crystals in hours** | CL zoning + trace element profiling (Nabelek) |
| Sustained growth estimate | **Decimeter crystals in days; meter crystals in days-to-weeks** | Extrapolation from measured rates |
| Growth regime | Highly dynamic, turbulent convective | Not static diffusion-limited |

**Key insight:** Pegmatite crystals do NOT grow slowly over thousands of years. They grow explosively fast in the final stages of pegmatite crystallization, when a free fluid phase exists in miarolitic cavities and convective turbulence delivers supersaturated fluid to crystal faces at rates orders of magnitude higher than static diffusion.

This is critical for the **Pocket mode** design: crystal growth should be >100× faster than Vug mode, and the time scale should be days-to-years, not millennia.

### Basalt Vugs (Current Simulator Baseline)

| Parameter | Value | Source |
|-----------|-------|--------|
| Vug diameter | mm to 10s of cm | Typical basalt vesicle size |
| Crystal size in vugs | mm to cm | Zeolites, quartz, calcite, chalcedony |
| Growth duration | Hundreds to thousands of years | Low-T hydrothermal, static fluid |
| Growth rate | μm to mm per year | Diffusion-limited, closed system |

**Key insight:** Basalt vugs are closed systems with limited fluid volume. Once supersaturation is consumed, growth stops. This matches the current Vugg Simulator design: finite broth, finite steps, crystals compete for limited chemistry.

### Cave Speleothems (Flowstone, Stalactites, Stalagmites)

| Parameter | Value | Source |
|-----------|-------|--------|
| Stalactite growth rate | 0.1–3 mm/year | Typical; up to 10 mm/year in tropical caves |
| Maximum stalactite length | 10+ m | Coves de Campanet, Mallorca; Jeita Grotto, Lebanon |
| Cave passage scale | m to 100s of m | Solutionally enlarged fractures |
| Growth duration | 10,000–1,000,000+ years | Quaternary to Pliocene ages common |
| Fluid dynamics | Dripping film flow, open system | Continuous CO₂ degassing + CaCO₃ precipitation |

**Key insight:** Cave growth is 1,000× slower than vug growth but continues for 1,000,000× longer. The product is enormous (meter-scale) but formed by accretion of incredibly thin layers. This suggests **Cave mode** should have:
- Extremely slow per-step growth
- Essentially infinite chemistry (flowing water)
- Time scale: 10,000+ steps = millions of years
- Crystal habit: radially symmetric, concentric layering (not euhedral)

---

## 2. Fluid Dynamics by Void Type

### Vug — Closed System (Current Simulator)

- **Fluid volume:** Fixed at formation. No replenishment.
- **Transport mechanism:** Diffusion + minor convection.
- **Chemistry evolution:** Monotonic depletion of reactants; products accumulate.
- **Supersaturation:** Starts high, drops as crystals grow. Eventually undersaturated → dissolution.
- **Temperature:** Generally cooling (retrograde) or stable (isothermal).
- **Key minerals:** Zeolites, quartz, chalcedony, calcite, fluorite, barite, sulfides.
- **Simulator mechanic:** Broth depletes; σ decreases; competition is zero-sum.

### Pocket — Semi-Open System (Proposed Pocket Mode)

- **Fluid volume:** Large but finite. Exchange with surrounding rock via fractures.
- **Transport mechanism:** Convective turbulence + episodic fluid influx.
- **Chemistry evolution:** Replenished by late-stage magmatic/hydrothermal fluids; may have multiple pulses.
- **Supersaturation:** Can be sustained or episodically refreshed.
- **Temperature:** Cooling from magmatic temperatures (650°C → 550°C over years).
- **Key minerals:** Giant quartz, tourmaline, spodumene, lepidolite, beryl, topaz, feldspar.
- **Simulator mechanic:** Periodic fluid pulses replenish broth; much larger vug volume; crystals can grow to decimeters.

**Critical finding from Nabelek et al. (2020):** The Stewart pegmatite's miarolitic cavities (chimneys) make up ~50% by volume of the perthite zone. These chimneys represent late-stage fluids that "diked into a mostly solidified upper zone." This means pockets form by **fluid injection into solidified rock** — not by gas bubbles in molten rock. The simulator should model this as an **event**: solidification of host rock → fracture → fluid injection → pocket formation.

### Cave — Open Flow System (Proposed Cave Mode)

- **Fluid volume:** Effectively infinite (regional groundwater flow).
- **Transport mechanism:** Film flow on ceilings, drip splashing on floors, stream flow on walls.
- **Chemistry evolution:** Controlled by external climate (rainfall, CO₂, temperature). Seasonal cycles.
- **Supersaturation:** Maintained by CO₂ degassing; stops if cave floods or dries completely.
- **Temperature:** Near-surface isothermal (~mean annual temperature).
- **Key minerals:** Calcite (dominant), aragonite, gypsum, ice (in ice caves), rare sulfates/phosphates.
- **Simulator mechanic:** Continuous but slow growth; climate events (drought, flood) interrupt; seasonal bands.

**Fluid dynamics differences summary:**

| Parameter | Vug (Closed) | Pocket (Semi-Open) | Cave (Open) |
|-----------|------------|-------------------|-------------|
| Fluid source | Trapped at formation | Late magmatic/hydrothermal pulses | Meteoric groundwater |
| Replenishment | None | Episodic (events) | Continuous |
| Growth rate | μm–mm/year | cm–dm/day (episodic) | 0.1–3 mm/year |
| Time scale | 100–10,000 years | Days to years | 10,000–1,000,000 years |
| Crystal size | mm–cm | cm–m | cm–m (but by accretion) |
| Crystal habit | Euhedral (space-limited) | Euhedral to subhedral (giant) | Concentric, botryoidal, dendritic |
| Competition | Zero-sum for limited chemistry | Moderate (large fluid volume) | Minimal (infinite chemistry) |
| Temperature | Cooling or isothermal | Cooling from magmatic | Isothermal (surface) |

---

## 3. Growth Rate Scaling Laws

### Diffusion-Limited Growth (Vugs)

In a closed cavity, crystal growth is limited by diffusion of solutes through the fluid boundary layer:

**Growth rate ∝ (D × ΔC) / (ρ × r)**

Where D = diffusion coefficient, ΔC = supersaturation, ρ = crystal density, r = crystal radius.

As crystals get larger, their surface area-to-volume ratio decreases, and the boundary layer thickens. Growth slows. This is why basalt vug crystals rarely exceed a few centimeters.

### Convective-Turbulent Growth (Pockets)

In miarolitic cavities with free fluid convection, the boundary layer is constantly disrupted:

**Growth rate ∝ (k × ΔC) / ρ**

Where k = mass transfer coefficient (turbulence-dependent). k can be 100–10,000× larger than D/r for diffusion-limited growth.

Nabelek et al. (2020) measured trace element profiles in quartz that imply growth rates of **10⁻⁶ to 10⁻⁵ m/s** — meters per million seconds, or roughly **cm per day**. This is 10,000× faster than typical hydrothermal quartz growth.

**For the simulator:** Pocket mode should allow growth rates 50–200× faster than Vug mode, but with episodic chemistry pulses rather than continuous depletion.

### Film-Flow Growth (Caves)

In cave speleothems, growth is controlled by CO₂ degassing and thin-film fluid dynamics:

**Growth rate ∝ (Q × [Ca²⁺] × α) / A**

Where Q = drip rate, [Ca²⁺] = calcium concentration, α = CO₂ degassing efficiency, A = growth surface area.

Typical values: Q = 0.1–10 drips/min, [Ca²⁺] = 1–5 mmol/L, α = 0.01–0.1.

Result: **0.01–1 μm per drip** ≈ 0.1–3 mm/year.

**For the simulator:** Cave mode growth should be 100–1,000× slower per step than Vug mode, but with essentially unlimited steps (simulating millions of years).

---

## 4. Proposed Game Mode Specifications

### Mode 1: Vug (Current)

- **Void size:** 0.001–0.1 m (1–10 cm typical)
- **Steps:** 20–100 rounds
- **Time per step:** 100–1,000 years
- **Total simulated time:** 2,000–100,000 years
- **Fluid dynamics:** Closed, depleting
- **Broth volume:** Fixed; depletes monotonically
- **Max crystal size:** 1–50 mm
- **Key mechanics:** σ competition, thermal decomposition, crystal-crystal competition
- **Geological analog:** Basalt vesicles, hydrothermal veins, Alpine clefts

### Mode 2: Pocket (Proposed)

- **Void size:** 0.5–10 m
- **Steps:** 50–200 rounds
- **Time per step:** 1 day – 1 year
- **Total simulated time:** 1 month – 200 years
- **Fluid dynamics:** Semi-open; episodic fluid pulses
- **Broth volume:** Large; replenished by events
- **Max crystal size:** 5 cm – 2 m (giant crystals possible)
- **Key mechanics:**
  - Late-stage fluid injection events (replenish broth)
  - Convective turbulence (reduces boundary layer, increases growth)
  - Temperature cooling from 650°C → 550°C over the run
  - Crystal-crystal competition reduced (large volume)
  - "Gem quality" bonus for slow-cooled, low-inclusion crystals
- **Geological analog:** LCT pegmatite miarolitic cavities, Alpine fissures, Jeffrey Mine pockets
- **Minerals enabled:** Giant quartz, tourmaline, spodumene, lepidolite, beryl, topaz, feldspar megacrysts

### Mode 3: Cave (Proposed)

- **Void size:** 1–100+ m (passage-scale)
- **Steps:** 1,000–10,000 rounds
- **Time per step:** 100–10,000 years
- **Total simulated time:** 100,000–100,000,000 years
- **Fluid dynamics:** Open flow; continuous but slow
- **Broth volume:** Infinite (flowing water)
- **Max crystal size:** 10 cm – 10 m (but by slow accretion)
- **Key mechanics:**
  - Climate events (drought = no growth; flood = erosion; CO₂ spike = growth surge)
  - Seasonal bands (alternating growth/dormancy layers visible in cross-section)
  - Drip chemistry tracking (each drip is a micro-batch of broth)
  - Prior calcite precipitation (PCP): if too much CaCO₃ precipitates before reaching the stalactite, growth slows
  - Gravity-determined habit: downward (stalactite), upward (stalagmite), horizontal (flowstone)
- **Geological analog:** Limestone caves, lava tubes, glacier caves, sea caves
- **Minerals enabled:** Calcite, aragonite, gypsum, ice, rare cave minerals

---

## 5. Void Geometry Implications

### Vug Geometry

- **Shape:** Spherical to irregular (vesicle), tabular (fracture), cylindrical (drill core)
- **Surface:** Often rough, with crystal nucleation sites on all walls
- **Crystal distribution:** Crystals nucleate on walls and grow inward; largest crystals at nucleation sites
- **Fill pattern:** Radial from walls, or single central crystal if space is limited
- **Simulator representation:** Current 2D cross-section is adequate

### Pocket Geometry

- **Shape:** Irregular, branching, often vertically elongated (chimneys)
- **Surface:** Smooth to rough; may show evidence of fluid injection (sharp contacts)
- **Crystal distribution:** Large crystals suspended in fluid or attached to walls; "floaters" possible
- **Fill pattern:** Central mass of large crystals + peripheral smaller crystals
- **Simulator representation:** 3D visualization needed; Hilbert curve spiral through pocket space (Professor's concept)

### Cave Geometry

- **Shape:** Tubular (stream passages), spherical (rooms), irregular (phreatic mazes)
- **Surface:** Sculpted by dissolution; ceiling, walls, floor each have distinct mineral assemblages
- **Crystal distribution:**
  - Ceiling: stalactites, soda straws, draperies (downward growth)
  - Walls: flowstone, rimstone dams (horizontal growth)
  - Floor: stalagmites, columns (upward growth)
  - Pools: rimstone, cave pearls (concentric growth)
- **Fill pattern:** Never fully filled; space is preserved
- **Simulator representation:** Requires 3D visualization with gravity-determined growth vectors

---

## 6. Design Recommendations

### Immediate (Vug Mode Polish)

1. **Keep Vug mode as-is** — it accurately represents closed-system, diffusion-limited growth.
2. **Add "giant crystal" bonus** for rare events where a single crystal dominates a vug (analogous to pegmatite pockets, but at vug scale).

### Short-Term (Pocket Mode)

1. **Implement episodic fluid pulse events** — `event_late_fluid_pulse` injects new chemistry mid-run.
2. **Scale up vug volume by 50–100×** — more space = more crystals = larger max size.
3. **Add convective turbulence mechanic** — reduces boundary layer resistance, increases growth rate.
4. **Add cooling curve** — temperature drops from 650°C to 550°C over the run, changing which minerals are stable.
5. **Add "gem quality" scoring** — slow, inclusion-free growth = higher value.
6. **Enable spodumene, lepidolite, giant quartz, tourmaline** — minerals that only make sense at pocket scale.

### Long-Term (Cave Mode)

1. **Implement open-flow fluid dynamics** — continuous drip/stream input, not batch broth.
2. **Add climate event system** — drought, flood, CO₂ spike, temperature shift.
3. **Add seasonal banding visualization** — growth layers visible in cross-section.
4. **Implement gravity-determined habit** — growth direction determined by surface orientation.
5. **Add PCP (prior calcite precipitation) mechanic** — if water precipitates CaCO₃ on walls before reaching stalactite, growth slows.
6. **Enable calcite, aragonite, gypsum, ice** — minerals dominant in cave environments.

### Cross-Mode Design Principles

| Principle | Vug | Pocket | Cave |
|-----------|-----|--------|------|
| Time compression | 100–1,000 yrs/step | 1 day–1 yr/step | 100–10,000 yrs/step |
| Chemistry | Fixed, depleting | Large, episodically refreshed | Infinite, climate-variable |
| Growth rate | Slow (diffusion) | Very fast (convective) | Very slow (film-flow) |
| Max crystal size | cm | m | m (by accretion) |
| Crystal habit | Euhedral, space-filling | Euhedral to subhedral, giant | Concentric, botryoidal, dendritic |
| Key visual | Cross-section | 3D spiral (Hilbert) | 3D passage with gravity vectors |
| Key emotion | Discovery, competition | Awe, scale | Time, patience, layers |

---

## References

1. **Nabelek et al. (2020)** — "Episodes of fast crystal growth in pegmatites." *Nature Communications*, 11, 4986. https://www.nature.com/articles/s41467-020-18806-w
2. **Webber, K.L., Simmons, W.B., Falster, A.U., & Foord, E.E. (1999)** — "Cooling rates and crystallization dynamics of shallow level pegmatite-aplite dikes, San Diego County, California." *American Mineralogist*, 84, 708–717.
3. **London, D. (2008)** — *Pegmatites*. Mineralogical Association of Canada, Special Publication 10.
4. **Černý, P. (1991)** — "Rare-element granitic pegmatites. Part I: Anatomy and internal evolution." *Geoscience Canada*, 18(2), 49–67.
5. **Kaufmann, G. (2003)** — "Stalagmite growth and palaeo-climate: the numerical perspective." *Earth and Planetary Science Letters*, 214(1–2), 251–266.
6. **Fairchild, I.J., & Baker, A. (2012)** — *Speleothem Science: From Process to Past Environments*. Wiley-Blackwell.
7. **Dreybrodt, W. (1999)** — "Chemical kinetics, speleothem growth and climate." *Speleochronologia*, 1, 3–11.
8. **Wikipedia — Vug.** https://en.wikipedia.org/wiki/Vug
9. **Wikipedia — Speleothem.** https://en.wikipedia.org/wiki/Speleothem
10. **ScienceInsights — What Is a Vug?** https://scienceinsights.org/what-is-a-vug-crystal-lined-rock-cavities-explained/

---

## Cross-References
- Vugg Simulator species list: `proposals/vugg-mineral-species-list.md`
- Vugg Simulator mineral template: `proposals/vugg-mineral-template.md`
- Spodumene research: `memory/research-spodumene.md`
- Lepidolite research: `memory/research-lepidolite.md`
- Columbite research: `memory/research-columbite.md`
- Hilbert curve research: `projects/vugg-simulator/research/spiral-encoding-experiment.md`
- TODO: `TODO.md` (Vugg Simulator — Research — Game Mode Scale Progression section)
