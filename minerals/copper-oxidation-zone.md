# Copper Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-05-25
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering native copper, cuprite, malachite, and azurite as a single redox-controlled mineral system.
**Related files:**
- `memory/research-native-copper.md` — Native Cu⁰
- `memory/research-cuprite.md` — Cu₂O (Cu⁺)
- `memory/research-malachite.md` — Cu₂(CO₃)(OH)₂ (Cu²⁺, low pCO₂)
- `memory/research-azurite.md` — Cu₃(CO₃)₂(OH)₂ (Cu²⁺, high pCO₂)
- `memory/research-chalcocite.md` — Cu₂S (primary sulfide, precursor)
- `memory/research-chalcopyrite.md` — CuFeS₂ (primary sulfide, ultimate precursor)
- `memory/research-broth-ratio-malachite-azurite.md` — Malachite/azurite equilibrium

---

## The Story This Sequence Tells

The copper oxidation zone is the single best teaching tool in the entire Vugg Simulator for demonstrating how **redox potential (Eh)** and **carbonate availability (pCO₂)** control mineralogy. Same element — copper — wearing four different mineral identities depending on how much oxygen and carbon dioxide are present.

This is not four separate minerals. This is one mineral system with four stable states.

---

## The Full Sequence (Deep to Surface)

```
DEPTH                                          SURFACE
  │                                              │
  ▼                                              ▼

Primary zone (hypogene):
  Chalcopyrite (CuFeS₂) ──► Bornite (Cu₅FeS₄) ──► Chalcocite (Cu₂S)
         │
         │ uplift + exposure to groundwater + O₂
         ▼
Oxidation zone (supergene):
  
  Most reducing ────────────────────────────────── Most oxidizing
         │                                              │
         ▼                                              ▼
  
  Native Copper (Cu⁰)      Eh < +0.2V
         │
         │ rising Eh, some O₂
         ▼
  Cuprite (Cu₂O)           Eh +0.2 to +0.4V
         │                    Cu⁺ — the intermediate state
         │
         ├──► Tenorite (CuO) — if fully oxidized, alkaline pH
         │
         └──► With CO₂ present:
                  │
                  ├──► Azurite (Cu₃(CO₃)₂(OH)₂) — HIGH pCO₂
                  │      Deep blue, stable at higher CO₂
                  │
                  └──► Malachite (Cu₂(CO₃)(OH)₂) — LOW pCO₂
                         Bright green, the thermodynamic end product
```

---

## Phase Diagram: Eh vs pCO₂ at Fixed pH (7.0, 25°C)

```
     pCO₂ (atm)
       ▲
  high │  Azurite      │
       │  (blue)       │  Cuprite
  0.1  │───────────────┼───────────────
       │               │   (dark red)
  0.01 │  Malachite    │
       │  (green)      │
   low │               │  Native Cu
       └───────────────┼───────────────► Eh (V vs SHE)
       reducing        │        oxidizing
                  +0.2V    +0.4V
```

**Key insight:** At any given Eh, increasing pCO₂ pushes the system from malachite → azurite. At any given pCO₂, increasing Eh pushes native Cu → cuprite → (tenorite or carbonates).

---

## Formation Mechanisms

### Native Copper (Cu⁰)
- **How it forms:** Cu²⁺ (from oxidized sulfides) migrates downward through groundwater to the **water table** (reducing zone). There, sulfate-reducing bacteria or reaction with pyrite reduces Cu²⁺ → Cu⁰.
- **What it needs:** High Cu concentration, strongly reducing conditions (Eh < +0.2V), low sulfur (or sulfur already precipitated as secondary sulfides).
- **Where:** Below the water table in the supergene enrichment zone. Also in basalt vesicles (Keweenaw — primary, not supergene).
- **What happens next:** If the water table drops or oxygen penetrates, native copper oxidizes to cuprite.

### Cuprite (Cu₂O)
- **How it forms:** The **redox boundary** mineral. Cu⁺ is unstable in most natural conditions — it only exists at the narrow interface between reducing (native Cu) and oxidizing (Cu²⁺ carbonates/tenorite).
- **What it needs:** Moderate Eh (+0.2 to +0.4V), some oxygen but not too much, low CO₂ (if CO₂ is high, you skip cuprite and go straight to carbonates).
- **Where:** The oxidation front — where oxygenated groundwater meets reducing rock.
- **Secret:** The ruby-red internal reflections. Shine light through dark cuprite crystals and they glow like garnet — Cu⁺ showing off.
- **What happens next:** More oxygen → tenorite (CuO) or, with CO₂, malachite/azurite.

### Malachite vs Azurite (The Carbonate Pair)
Both are Cu²⁺ carbonates. The difference is stoichiometry and CO₂ pressure:

| Feature | Malachite | Azurite |
|---------|-----------|---------|
| Formula | Cu₂(CO₃)(OH)₂ | Cu₃(CO₃)₂(OH)₂ |
| Cu:CO₃ ratio | 2:1 | 3:2 = 1.5:1 |
| pCO₂ needed | LOW | HIGH |
| Color | Bright green | Deep azure blue |
| Stability | The end product | Converts to malachite as pCO₂ drops |

**The conversion:**
```
2 Azurite + H₂O → 3 Malachite + CO₂↑
```
This is not dissolution-reprecipitation. It's **solid-state ion exchange** — azurite crystals restructure in place, turning from blue to green while keeping their shape. In the simulator, this should be modeled as a **pseudomorph transformation**: azurite crystal → malachite crystal, same position, same size, different identity and color.

**Kinetics:** The azurite→malachite conversion is slow at room temperature (geological time). But in the simulator, it can be accelerated for gameplay visibility by making the conversion probability time-dependent.

---

## Simulator Implementation — Unified Redox Zone Model

### New Parameter: `Eh_zone` (Redox Zone)
The copper oxidation zone needs a concept of vertical position or redox intensity. Options:

1. **Depth-based model:** `depth` parameter (0 = surface, 1 = deepest). Eh increases from depth → surface. Native Cu at depth=0.9, cuprite at 0.6, malachite/azurite at 0.3.

2. **Eh as explicit parameter:** Track Eh directly as a fluid chemistry variable. Native Cu nucleates at Eh < 0.2, cuprite at 0.2–0.4, carbonates at Eh > 0.4.

3. **O₂-gradient model:** Use existing O₂ tracking but add a "reducing potential" counter. When O₂ is low but Fe or S reducing agents are present, native Cu can form.

**Recommended:** Option 2 (explicit Eh) because it generalizes to other redox-sensitive systems (iron: siderite → magnetite → hematite/goethite; uranium: uraninite → coffinite → autunite/torbernite; manganese: rhodochrosite → pyrolusite).

### Supersaturation Functions — Unified

```javascript
// NATIVE COPPER
σ_native_copper = f(Cu, Eh, S, T)
  high Cu (>50 ppm)
  Eh < 0.2V (strongly reducing)
  S < threshold (no sulfide competition)
  T < 300°C

// CUPRITE
σ_cuprite = f(Cu, Eh, O2, CO3, T)
  moderate Cu (>30 ppm)
  Eh = 0.2–0.4V (the sweet spot)
  O2 present but not dominant
  CO3 LOW (if CO3 is high, cuprite is skipped)
  T < 100°C

// AZURITE (high pCO2 carbonate)
σ_azurite = f(Cu, CO3, pCO2, Eh, T)
  Cu > 30 ppm
  CO3 > threshold
  pCO2 > 0.1 atm
  Eh > 0.4V (oxidizing)
  T < 50°C

// MALACHITE (low pCO2 carbonate — end product)
σ_malachite = f(Cu, CO3, pCO2, Eh, T)
  Cu > 20 ppm
  CO3 > threshold
  pCO2 < 0.1 atm (or any pCO2 if azurite converts)
  Eh > 0.4V
  T < 80°C
```

### Transformation Rules (Dynamic)

```javascript
// Native Cu → Cuprite (oxidation)
IF native_copper exists AND Eh rises above 0.2V:
  prob = (Eh - 0.2) / 0.2 * time_factor
  IF random() < prob → convert to cuprite (same position)

// Cuprite → Malachite (carbonation)
IF cuprite exists AND CO3 increases AND Eh > 0.4V:
  prob = (CO3 - threshold) / max_CO3 * time_factor
  IF random() < prob → convert to malachite

// Cuprite → Tenorite (full oxidation, no CO3)
IF cuprite exists AND Eh > 0.5V AND CO3 < threshold:
  → convert to tenorite (not yet in game — future addition)

// Azurite → Malachite (pCO2 drop)
IF azurite exists AND pCO2 drops below 0.1:
  prob = (0.1 - pCO2) / 0.1 * time_factor
  IF random() < prob → pseudomorph to malachite
       (retain azurite crystal shape, change color/identity)
```

### Zone History Narration

When the player opens a vug containing copper oxidation zone minerals, the narrator should tell the redox story:

> "You found a copper oxidation zone — four minerals, one element, four different conversations with oxygen. At the deepest edge: native copper, the metal remembering it was once sulfide, preserved by groundwater that had no air to give. Above that: cuprite, the ruby-red whisper of partial oxidation — Cu⁺ saying 'almost, not yet.' And at the surface: malachite's green bands recording each season's CO₂ breath, with a few blue azurite ghosts still holding their shape from when the CO₂ was higher. The water table rose and fell here. The oxygen front advanced and retreated. Every mineral is a position in a chemical argument that lasted millennia."

---

## Famous Localities for the Full Sequence

### Tsumeb, Namibia
The world's best copper oxidation zone. You can hold a specimen with native copper, cuprite, malachite, and azurite all in one hand. The oxidation front was preserved because the climate stayed dry enough to prevent total dissolution.

### Bisbee, Arizona
The Copper Queen mine produced cuprite crystals with malachite coatings, plus native copper wires in the deeper enrichment zone. The classic American locality for the full sequence.

### Chessy-les-Mines, France
The type locality for azurite ("chessylite") and a historic source of crystallized cuprite. The limestone host rock provided the CO₃ for the carbonates.

### Keweenaw Peninsula, Michigan
Native copper in basalt vesicles — a primary, not supergene, occurrence. The copper precipitated directly from hydrothermal fluids. When these surfaces weather, they produce cuprite and malachite as secondary rinds.

---

## Cross-Reference to Other Simulator Systems

### Thermal Decomposition
- **Malachite:** → tenorite (CuO) + CO₂ + H₂O at ~200°C
- **Azurite:** → tenorite + CO₂ + H₂O at ~320°C
- **Cuprite:** Stable to melting (~1240°C) but oxidizes to tenorite in air above ~300°C
- **Native Cu:** Melts at 1085°C; oxidizes to cuprite in air above ~200°C

### Fluorescence
- None of these four fluoresce under UV. The copper ion quenches fluorescence.
- However, associated minerals might: chrysocolla (blue-green fluorescence under LW), calcite (common in oxidation zones — often fluoresces).

### Crystal Photo Gallery
- Native copper: metallic, hackly, dendritic. Wire copper is iconic.
- Cuprite: dark crystals with ruby-red internal reflections. Chalcotrichite variety = plush copper hair.
- Malachite: banded botryoidal green. Fibrous and pseudomorph varieties.
- Azurite: deep midnight-blue prismatic crystals. Rosettes and "suns."

---

## Builder Notes

### Priority for Implementation
1. **Malachite** — already in game (v1), just needs azurite conversion mechanic
2. **Azurite** — already in game (v1), just needs pCO₂-dependent nucleation
3. **Cuprite** — needs new mineral species, but high impact (ruby-red visuals, redox teaching)
4. **Native copper** — needs new species, lower priority (metallic, no crystal color variation)

### New Fluid Chemistry Needed
- **Eh (redox potential):** The master variable. Required for cuprite and native copper.
- **pCO₂ (dissolved CO₂ partial pressure):** Required for azurite vs malachite discrimination.
- **Depth/zone parameter:** Structural — determines which part of the sequence can nucleate.

### Polymorphs and Variants Already Covered
See individual research files for:
- Cuprite: chalcotrichite (fibrous), tile ore (massive)
- Malachite: banded, fibrous, azurite pseudomorph
- Azurite: prismatic, rosette, sun
- Native copper: crystalline, dendritic, wire, halfbreed (with Ag)

---

## Flavor Text — Sequence Epilogue

> The copper oxidation zone is geology's way of showing its work. Most deposits hide their history — you see the end product and guess at the journey. But copper is generous. It keeps every stage: the reduced metal, the half-oxidized oxide, the fully oxidized carbonates in two different colors depending on how much CO₂ was in the water that day. Four minerals, one element, one redox gradient. The deepest ones are red. The shallowest ones are green. In between, the ground held its breath just long enough to make something blue.

---

*File created 2026-05-25 by 🪨✍️ during Vugg Simulator mineral expansion cron. Next step: Builder implements unified redox zone model with Eh and pCO₂ parameters.*
