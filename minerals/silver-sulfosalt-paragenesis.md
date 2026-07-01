# Silver Sulfosalt Paragenesis — Proustite + Pyrargyrite Master File

**Date:** 2026-06-11
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering the "ruby silver" sulfosalt pair — proustite (Ag₃AsS₃) and pyrargyrite (Ag₃SbS₃) — as a single As:Sb-controlled mineral system with shared light-sensitive decomposition mechanics.
**Related files:**
- `memory/research-proustite.md` — Ag₃AsS₃, scarlet ruby silver
- `memory/research-pyrargyrite.md` — Ag₃SbS₃, dark ruby silver
- `memory/research-acanthite.md` — Ag₂S, monoclinic low-T polymorph
- `memory/research-argentite.md` — Ag₂S, cubic high-T polymorph
- `memory/research-native-silver.md` — Ag⁰
- `memory/research-silver-oxidation-zone.md` — Broader silver system (argentite → acanthite → native silver)
- `memory/research-realgar.md` — Light-sensitive As-sulfide (shares photodecomposition mechanic)
- `memory/research-orpiment.md` — Light-sensitive As-sulfide (shares photodecomposition mechanic)
- `memory/research-tetrahedrite.md` — Cu₁₂Sb₄S₁₃ (Sb-rich, may co-precipitate)
- `memory/research-tennantite.md` — Cu₁₂As₄S₁₃ (As-rich, may co-precipitate)

---

## The Story This Sequence Tells

The silver sulfosalts are the most emotionally complicated minerals in the Vugg Simulator. They are beautiful, fragile, and self-destructive — a mineralogical tragedy in trigonal symmetry.

Proustite and pyrargyrite are isostructural twins separated by a single atomic substitution: arsenic vs. antimony in the pyramidal anion group. They share the same space group (R3c), the same lattice parameters, the same crystal habits, the same hardness, the same density, and the same fate. Both are called "ruby silver" because thin splinters glow blood-red in transmitted light. Both darken irreversibly when exposed to light. Both slowly transform into acanthite in museum drawers, even in darkness, because the silver in their lattices is never fully at rest.

The As:Sb ratio in the hydrothermal fluid is the only thing that decides which one grows. Arsenic-dominant fluids produce proustite — the scarlet sister, rarer, more vivid. Antimony-dominant fluids produce pyrargyrite — the dark sister, more common, heavier, slightly more metallic. Most natural fluids are antimony-dominant, which is why pyrargyrite outcrops are more common and proustite specimens command higher prices.

Both form late in the epithermal sequence, after the major base metal sulfides have claimed their share of sulfur and silver. They are the residue — the last negotiation between silver, sulfur, and a group-V element in a cooling, depleting fluid. They grow where the temperature has dropped below 350°C but above 100°C, where the fluid is still reducing enough to keep sulfur as S²⁻, and where arsenic or antimony is abundant enough to form the (AsS₃)³⁻ or (SbS₃)³⁻ pyramids that lock the silver in place.

And then the light finds them.

---

## The Full Sequence (Temperature + As:Sb Controlled)

```
HIGH TEMPERATURE ──────────────────────── LOW TEMPERATURE
        │                                        │
        ▼                                        ▼

Hypogene zone (epithermal, 200–300°C):
  Tetrahedrite/Tennantite ──► Galena ──► Sphalerite
  (Cu-Sb/As sulfosalts)       (PbS)      (ZnS)
        │
        │ fluid cools, Ag concentrates, S depletes
        ▼

Late epithermal (100–350°C):
        │
        ├──► IF X_As = As/(As+Sb) > 0.5
        │      │
        │      ▼
        │    Proustite (Ag₃AsS₃) — scarlet, rarer
        │      │
        │      │  Trigonal R3c
        │      │  (AsS₃)³⁻ pyramids
        │      │  2.5× baseline growth rate
        │      │
        │      └──► Further cooling < 100°C
        │            │
        │            ▼
        │          Acanthite (Ag₂S) — replacement
        │            │
        │            └──► Native Silver (Ag⁰)
        │                  (most reducing, sulfur exhausted)
        │
        └──► IF X_As = As/(As+Sb) < 0.5
               │
               ▼
             Pyrargyrite (Ag₃SbS₃) — dark ruby, more common
               │
               │  Trigonal R3c (isostructural)
               │  (SbS₃)³⁻ pyramids
               │  2.8× baseline growth rate
               │
               └──► Further cooling < 100°C
                     │
                     ▼
                   Acanthite (Ag₂S) — replacement
                     │
                     └──► Native Silver (Ag⁰)
```

---

## The As:Sb Fork — Controlling Variable

The X_As ratio is the master variable that determines which ruby silver forms. This is the chromophore diva principle applied to mineral selection: same structure, different group-V element, different mineral identity.

| X_As = As/(As+Sb) | Dominant Mineral | Notes |
|-------------------|------------------|-------|
| > 0.7 | Pure proustite | Rare; requires As-rich fluid (Carlin-type, fumaroles) |
| 0.5 – 0.7 | Proustite-dominant | May have Sb traces; still classified as proustite |
| 0.3 – 0.5 | Pyrargyrite-dominant | May have As traces; classified as pyrargyrite |
| < 0.3 | Pure pyrargyrite | Most common; Sb dominates in most epithermal fluids |

**Geological significance:** Pyrargyrite is ~3–5× more common than proustite in nature because antimony is generally more abundant than arsenic in epithermal silver systems. Proustite is restricted to:
- Carlin-type gold-silver systems (As-rich)
- Volcanic fumaroles (As-sublimate)
- Specific arsenic-silver districts (Chanarcillo, Chile)
- Oxidation zones where As has been concentrated by weathering

---

## Phase Diagram: Temperature vs X_As at Fixed Ag, S

```
     Temperature (°C)
       ▲
  350  │  ┌─────────────────────┐
       │  │   Proustite field   │
       │  │   (X_As > 0.5)      │
  250  │  │  ←── As:Sb fork ──→ │  Pyrargyrite field
       │  │                     │  (X_As < 0.5)
  150  │  └─────────────────────┘
       │           │
       │           ▼
  100  │  ─────────┼───────── Acanthite stability line
       │           │
        └───────────┼──────────────────► X_As
                   0.5
       reducing ←──┼──→ oxidizing
                  Eh
```

At temperatures below 100°C, both proustite and pyrargyrite become metastable relative to acanthite + native silver. However, kinetic barriers mean they can persist for geological timescales at low temperature.

---

## The Photodecomposition Pathway (Shared Mechanic)

Both proustite and pyrargyrite share a unique degradation pathway: **light-induced internal acanthite nucleation**. This is the defining gameplay mechanic for the silver sulfosalts.

### Mechanism
1. Photon absorption mobilizes Ag⁺ ions in the lattice
2. Silver ions migrate through the trigonal structure (the lattice has channels along [001])
3. Mobile Ag⁺ finds reduced sulfur (residual S²⁻ or from trace sulfide inclusions)
4. Nucleates microscopic acanthite (Ag₂S) crystals internally
5. Acanthite inclusions scatter light, darkening the crystal from within
6. Process is **irreversible** — the acanthite inclusions are stable and do not redissolve

### Rates
- **Proustite:** Darkens in direct sunlight within hours to days; complete blackening in weeks
- **Pyrargyrite:** Slightly more resistant — days to weeks for initial darkening; complete blackening in months
- **Thermal darkening:** Even in total darkness, slow internal silver migration occurs at rates dependent on temperature. A century-old specimen is not the same mineral it was when mined.

### Game Implementation
```
IF crystal_exposed_to_light_steps > threshold
THEN internal_acanthite_nucleation += 1
IF internal_acanthite_nucleation > cosmetic_threshold
THEN crystal_color shifts: scarlet → dark red → gray → black
IF internal_acanthite_nucleation > structural_threshold
THEN crystal may develop visible metallic specks (acanthite inclusions)
```

**Gameplay consequence:** Players who grow beautiful ruby silver crystals must choose between displaying them (risking darkening) or storing them in darkness (preserving color but hiding them from view). The "curator's dilemma."

---

## Individual Flavor Text

### Proustite
> Proustite is the color of arterial blood in crystal form — scarlet, vermilion, alive. Hold a thin splinter to lamplight and it glows ruby-red from within, which is why miners called it "ruby silver" and Chanarcillo prospectors named it Sangre de Toro, Blood of the Bull. But light is its enemy. Leave a specimen on a sunny windowsill and within days the scarlet dies, bleeding inward to black as silver ions migrate through the lattice and nucleate acanthite in the heart of the crystal. The darkening is permanent — an internal wound that cannot heal. Joseph Proust, who gave his name to this mineral, discovered that chemical compounds always hold their elements in fixed proportions. Proustite honors that law absolutely: three silvers, one arsenic, three sulfurs, locked in trigonal symmetry. Until the light breaks the lock.

### Pyrargyrite
> Pyrargyrite carries two identities in one body. Hold a thick crystal in your hand and it is gunmetal gray, dull, almost disappointing — a metallic rock like any other. But crack it, or find a thin edge where light can pass, and it ignites: deep ruby-red, cherry, the color of heart's blood seen by candle flame. The Greeks named it for fire and silver — *pyr* and *argyros* — and Glocker gave it that name in 1831 because he understood what it was: not a gray mineral that happens to be red at the edges, but a red mineral imprisoned in its own opacity. It is the dark ruby silver, heavier and slightly more common than its scarlet sister proustite, born in the same epithermal wombs where silver, antimony, and sulfur negotiate their slow crystalline treaty. Like proustite, it carries a death sentence in light. The silver in its lattice is restless. Given time and photons, the Ag⁺ ions will migrate, find each other, and nucleate acanthite in the heart of the crystal — black inclusions that spread like a mineral cancer. The process is thermal as well as optical. Even in darkness, the internal silver is never fully at rest. A century-old specimen in a museum drawer is not the same mineral it was when it came out of the ground. It is a crystal in the process of becoming something else.

---

## Cross-Zone Interactions

### With Tetrahedrite/Tennantite
Tetrahedrite (Cu₁₂Sb₄S₁₃) and tennantite (Cu₁₂As₄S₁₃) are the high-temperature Cu-dominant analogues of pyrargyrite and proustite. They form earlier in the epithermal sequence (300–400°C) and share the same As:Sb fork logic. In the game:
- High Cu, moderate Ag, high Sb → tetrahedrite
- High Cu, moderate Ag, high As → tennantite
- High Ag, moderate Cu, high Sb → pyrargyrite
- High Ag, moderate Cu, high As → proustite

This creates a four-way competition for Ag, Cu, Sb, As, and S in the 100–350°C window.

### With Acanthite/Native Silver
Both proustite and pyrargyrite can be overgrown by, or replace, acanthite in the cooling sequence. In the oxidation zone, they may dissolve and reprecipitate as secondary enrichment phases. Native silver forms when all sulfur is exhausted — the ultimate reducing end point.

### With Realgar/Orpiment
The silver sulfosalts share the **light-sensitive decomposition** mechanic with realgar and orpiment. However:
- Realgar → pararealgar (same formula, different structure; reversible with heat)
- Orpiment → arsenolite (oxidation to oxide; irreversible)
- Proustite/pyrargyrite → acanthite + native silver (internal reduction; irreversible)

The game should track `light_exposure` as a global vug property that affects all four species simultaneously.

---

## Simulator Events

### `event_As_Sb_fork`
Triggered when temperature drops below 350°C with Ag > 2000 ppm and S > 500 ppm.
- Calculates X_As = As_ppm / (As_ppm + Sb_ppm)
- If X_As > 0.5 → nucleates proustite
- If X_As < 0.5 → nucleates pyrargyrite
- If both As and Sb are very low → routes to acanthite instead (simple sulfide pathway)

### `event_photodecomposition`
Triggered when a proustite or pyrargyrite crystal has accumulated `light_exposure_steps > threshold`.
- Internal acanthite_nucleation counter increases
- Cosmetic color shift applied
- At maximum darkening, crystal may "drop" a separate acanthite crystal in the vug (simulating inclusion growth)

### `event_ruby_silver_discovery`
Rare positive event — when both proustite and pyrargyrite are present in the same vug, the player receives a "Ruby Silver Suite" bonus, representing the rare geological coincidence of an As:Sb balanced fluid.

---

## Summary for Builder

The silver sulfosalt pair requires:
1. **X_As tracking** — As/(As+Sb) ratio as a new derived variable
2. **Light exposure tracking** — shared mechanic with realgar/orpiment
3. **Photodecomposition pipeline** — internal state change on crystals, not just vug chemistry
4. **Two new mineral species** with isostructural logic (same structure, different element)

No new base elements needed — Ag, As, Sb, S are all already in the trace system.

The gameplay value is high: these are visually striking (ruby-red), emotionally resonant (self-destructing beauty), and scientifically accurate (light degradation is real and documented). The "curator's dilemma" creates genuine player choice about display vs. preservation.

---

## References
- Keighin, C.W. & Honea, R.M. (1969). The proustite-pyrargyrite phase diagram. *American Mineralogist* 54, 1511–1516.
- Engel, P. & Nowacki, W. (1966). Die Verfeinerung der Kristallstruktur von Proustit, Ag₃AsS₃, und Pyrargyrit, Ag₃SbS₃. *Neues Jahrbuch für Mineralogie*.
- Handbook of Mineralogy, Vol. 1 — Proustite and Pyrargyrite entries.
- Mindat.org — Locality data for both species.
- Rock & Gem Magazine — "What is Proustite?" (September 2022).
- CSMS Geology Post — "Ruby Red Silver; Proustite & Pyrargyrite" (October 2013).
- Dana's System of Mineralogy, 7th Edition.
- Knipe, S.W. et al. (1995). Mechanism of photodecomposition of proustite. *Canadian Mineralogist*.
