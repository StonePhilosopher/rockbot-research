# Nickel Oxidation Zone — Paragenetic Sequence Master File

**Date:** 2026-06-03
**Source:** Vugg Simulator Mineral Expansion — Cron batch research
**Status:** Complete
**Scope:** Unified paragenetic sequence covering nickeline, gersdorffite, millerite, and annabergite as a single Eh-pH-controlled mineral system.
**Related files:**
- `memory/research-nickeline.md` — NiAs, hexagonal arsenide
- `memory/research-millerite.md` — NiS, trigonal sulfide
- `memory/research-annabergite.md` — Ni₃(AsO₄)₂·8H₂O, monoclinic arsenate
- `memory/research-erythrite.md` — Co₃(AsO₄)₂·8H₂O, Co analogue of annabergite
- `memory/research-cobaltite.md` — CoAsS, Co sulpharsenide
- `memory/research-skutterudite.md` — CoAs₃, Co arsenide (not yet in simulator)
- `memory/research-iron-oxidation-zone.md` — Acid mine drainage interactions

---

## The Story This Sequence Tells

The nickel oxidation zone is the story of what happens when arsenic meets sulfur and then meets oxygen. Unlike copper's dramatic redox dance or lead's archaeological layering, nickel tells a simpler story — but the ending is unexpectedly beautiful.

Nickel is stubborn. It doesn't change oxidation states in nature (always Ni²⁺). It doesn't form colorful carbonates (NiCO₃ is too soluble). It doesn't make vivid phosphates or vanadates. What nickel makes, when it weathers, is green — a pale, apple-green bloom that spreads across rock faces like moss made of crystal.

This is the annabergite story: NiAs → NiS → Ni₃(AsO₄)₂·8H₂O. Arsenic and sulfur trade places as the counter-ion, but nickel stays nickel. The color comes from the Ni²⁺ chromophore itself — the same ion that colors emerald, hiddenite, and chrysoprase, but here diluted by water and arsenate into something softer, more tentative.

The nickel oxidation zone teaches: **not every element needs drama to be beautiful.**

---

## The Full Sequence (Deep to Surface)

```
DEPTH                                          SURFACE
  │                                              │
  ▼                                              ▼

Primary zone (hypogene):
  Nickeline (NiAs) ──► Gersdorffite (NiAsS)
         │               (sulfur-rich variant)
         │
         │ uplift + exposure to groundwater + O₂
         ▼
Oxidation zone (supergene):

  Stage 1: Sulfur retention
         │
         └──► Millerite (NiS)
                  │
                  ├──► Forms where S²⁻ is retained
                  │     (reducing microenvironments)
                  │
                  └──► Tarnishes to iridescent films

  Stage 2: Arsenic oxidation
         │
         └──► Annabergite (Ni₃(AsO₄)₂·8H₂O)
                  │
                  ├──► The "nickel bloom"
                  │     Apple-green encrustations
                  │
                  └──► Hydrated — 8 H₂O per formula unit
                        Dehydrates at ~200°C
```

---

## Pourbaix Diagram: Eh vs pH for the Ni-As-S System

```
     pH
      ▲
   10 │                 │
      │                 │  Annabergite
   8  │                 │  (Ni-arsenate)
      │─────────────────┼─────────────────
   6  │                 │
      │  Millerite      │
   4  │  (Ni-sulfide)   │
      │─────────────────┼─────────────────
   2  │                 │
      │  Nickeline      │
      │  (Ni-arsenide)  │
      └─────────────────┼─────────────────► Eh (V vs SHE)
      -0.4             0.0            +0.4
           reducing          oxidizing
```

**Key insight:** Nickeline/millerite stability is controlled by Eh (redox). Annabergite stability is controlled by both Eh (needs oxidizing conditions for As) and pH (needs neutral to mildly acidic for arsenate stability). The transition from sulfide/arsenide to arsenate requires crossing the As³⁺/As⁵⁺ redox boundary (~+0.2V at pH 7).

---

## The Nickeline-Gersdorffite Relationship

Nickeline (NiAs) and gersdorffite (NiAsS) are intimately related:

| Feature | Nickeline | Gersdorffite |
|---|---|---|
| Formula | NiAs | NiAsS |
| Crystal system | Hexagonal | Cubic (isometric) |
| Structure | NiAs type (B8₁) | Pyrite group (C2) |
| Color | Pale copper-red | Silver-white to steel-grey |
| Hardness | 5–5.5 | 5.5–6 |
| Sulfur | None | 1 S per formula unit |

**The gersdorffite question:** Gersdorffite is the sulfur-bearing member of the nickeline group. In nature, the two form a continuous solid solution series at high temperature, with sulfur substituting for arsenic. The cubic pyrite-group structure of gersdorffite vs the hexagonal NiAs structure of nickeline reflects the different bonding requirements of S vs As.

**Simulator implication:** At high T (>400°C), a single "nickeline-group" supersaturation could produce either mineral depending on S:As ratio:
- S:As < 0.5 → nickeline
- S:As = 0.5–2.0 → gersdorffite
- S:As > 2.0 → pentlandite or other Ni-Fe sulfide

---

## Millerite: The Sulfur Keeper

Millerite (NiS) is unusual in the nickel oxidation zone because it forms in **reducing microenvironments** within the broader oxidizing zone. How?

**Mechanism:** When nickeline/gersdorffite oxidizes, arsenic oxidizes faster than sulfur. Arsenic goes to arsenate (AsO₄³⁻) immediately. Sulfur, if present, can persist as sulfide (S²⁻) in local reducing pockets — especially where organic matter or pyrite creates micro-reducing zones.

**Result:** Ni²⁺ + S²⁻ → millerite, even while the surrounding rock is producing annabergite.

**The Halls Gap geodes:** In Kentucky, millerite forms spectacular radiating sprays inside geodes — the interior of the geode is sealed, creating a reducing microenvironment where sulfide sulfur is preserved. Outside the geode, the same rock produces annabergite.

**Simulator implication:** Millerite should be able to form in "reducing pockets" — zones with low local Eh even when the bulk fluid is oxidizing. This requires a **local Eh model**, not just a global one.

---

## Annabergite: The Nickel Bloom

Annabergite is the visual signature of the nickel oxidation zone — pale green encrustations that spread across weathered nickel arsenide ore like verdigris on copper. But unlike verdigris, annabergite is hydrated, crystalline, and beautiful.

**Why green?** Ni²⁺ in octahedral coordination absorbs red light and transmits green — the same mechanism as emerald, but with arsenate and water instead of beryl's silicate framework. The color is paler than emerald because the crystal field is weaker in the hydrated arsenate structure.

**The annabergite-erythrite series:** Annabergite (Ni) and erythrite (Co) form a complete solid solution. In nature, Co and Ni are almost always together (they're geochemical twins), so "pure" annabergite is rare. Most specimens are intermediate — the more Co, the more rose-pink; the more Ni, the more apple-green.

**Simulator implication:** The annabergite color should vary with Ni:Co ratio:
- Ni:Co > 3:1 → apple green
- Ni:Co = 1:1 → grey-green
- Ni:Co < 1:3 → rose-pink (erythrite)

---

## Formation Mechanisms

### Nickeline (NiAs) — The Primary Arsenide
- **How it forms:** Ni + As in reducing hydrothermal fluids, 250–400°C
- **What it needs:** High Ni (>100 ppm), high As (>100 ppm), strongly reducing
- **Diagnostic:** Pale copper-red color, metallic luster, garlic odor when heated (arsenic volatilization — toxic)
- **Associated minerals:** Skutterudite (CoAs₃), safflorite (CoAs₂), rammelsbergite (NiAs₂)
- **What happens next:** When exposed to oxygen, As oxidizes to arsenate; Ni stays Ni²⁺

### Gersdorffite (NiAsS) — The Sulfur-Bearing Variant
- **How it forms:** Same as nickeline but with sulfur present in the fluid
- **What it needs:** Ni + As + S, reducing conditions
- **Diagnostic:** Silver-white to steel-grey, harder than nickeline, cubic cleavage
- **What happens next:** Both As and S oxidize; S → sulfate, As → arsenate

### Millerite (NiS) — The Sulfide Survivor
- **How it forms:** In reducing microenvironments within the oxidation zone; also as primary low-T sulfide
- **What it needs:** Ni²⁺ + S²⁻, local reducing conditions (Eh < 0)
- **Diagnostic:** Acicular (needle-like) crystals in radiating sprays — one of the most distinctive habits in mineralogy
- **Tarnish:** Iridescent films on exposure to air
- **What happens next:** In oxidizing conditions, converts to polydymite (Ni₃S₄) or violarite (FeNi₂S₄), or dissolves and reprecipitates as annabergite

### Annabergite (Ni-arsenate hydrate) — The Oxidation End-Product
- **How it forms:** Ni²⁺ + AsO₄³⁻ + H₂O in oxidizing, near-surface conditions
- **What it needs:** Ni (>30 ppm), oxidized As (arsenate), pH 5–8, ambient temperature
- **Diagnostic:** Apple-green color, pearly luster, microcrystalline crusts
- **Associated minerals:** Erythrite (Co analogue), scorodite (Fe arsenate), pharmacolite (Ca arsenate)
- **What happens next:** Dehydrates at ~200°C; dissolves in acid; otherwise stable

---

## Simulator Implementation — Unified Nickel Zone Model

### New Parameter: `local_Eh`
Millerite formation requires reducing microenvironments within an oxidizing zone. This needs a **local Eh model**:

```javascript
// Global Eh (bulk fluid)
global_Eh = f(O2, pH, organic_matter, pyrite_present)

// Local Eh (microenvironment)
local_Eh = global_Eh + Eh_offset
  where Eh_offset = f(organic_matter, pyrite_present, enclosure)
  // In sealed pockets: Eh_offset = -0.3 to -0.5V
  // In open fractures: Eh_offset = 0V (same as global)
```

### Supersaturation Functions — Unified

```javascript
// NICKELINE (primary arsenide)
σ_nickeline = f(Ni, As, T, Eh, S)
  Ni > 100 ppm
  As > 100 ppm
  T = 250–500°C
  Eh < -0.2V (strongly reducing)
  S:As ratio < 0.5 (low sulfur)

// GERSDORFFITE (primary sulpharsenide)
σ_gersdorffite = f(Ni, As, S, T, Eh)
  Ni > 100 ppm
  As > 50 ppm
  S > 50 ppm
  T = 250–500°C
  Eh < -0.2V
  S:As ratio = 0.5–2.0

// MILLERITE (sulfide in reducing pockets)
σ_millerite = f(Ni, S, T, local_Eh)
  Ni > 50 ppm
  S as S²⁻ (not sulfate)
  T = 100–350°C (primary) or ambient (secondary)
  local_Eh < 0V (reducing microenvironment)
  // Can form in sealed vugs even when bulk fluid is oxidizing

// ANNABERGITE (oxidation zone arsenate)
σ_annabergite = f(Ni, AsO4, T, pH, Eh)
  Ni > 30 ppm
  AsO4 > 20 ppm (oxidized arsenic)
  T = 10–50°C
  pH = 5–8
  Eh > +0.2V (oxidizing)
  // Color depends on Ni:Co ratio
```

### Special Simulator Events

#### `event_nickeline_oxidation`
**Trigger:** Nickeline or gersdorffite present with Eh > +0.2V and O₂ > threshold.
**Effect:**
- Surface oxidation begins
- As³⁻ → AsO₄³⁻ (arsenate)
- S²⁻ → SO₄²⁻ (if gersdorffite)
- Ni²⁺ released to fluid (+20–100 ppm)
- If local conditions reducing: millerite may nucleate in pockets
- If oxidizing: annabergite forms on surface

#### `event_millerite_tarnish`
**Trigger:** Millerite present with Eh > -0.1V (mildly oxidizing).
**Effect:**
- Surface tarnish forms — iridescent film of polydymite (Ni₃S₄) or violarite
- Color shift: brass-yellow → iridescent purple/green/blue
- Does not destroy crystal — surface alteration only
- In simulator: color overlay, not replacement

#### `event_nickel_bloom`
**Trigger:** Ni²⁺ > 30 ppm and AsO₄³⁻ > 20 ppm and Eh > +0.2V.
**Effect:**
- Annabergite nucleates as crusts on existing minerals
- Preferential nucleation on nickeline/gersdorffite surfaces (epitaxial)
- Color: apple-green (pure Ni) to rose-pink (Co-rich)
- Forms microcrystalline crusts — individual crystals usually <1 mm

#### `event_annabergite_dehydration`
**Trigger:** T > 200°C with annabergite present.
**Effect:**
- Gradual dehydration: Ni₃(AsO₄)₂·8H₂O → Ni₃(AsO₄)₂·nH₂O (n < 8)
- Color shift: brighter green → duller green
- Structure: monoclinic → amorphous or different hydrate
- In simulator: visual degradation, not complete destruction

### Color Coding for Zone Visualization

| Mineral | Representative Color | Hex |
|---|---|---|
| Nickeline | Pale copper-red | #B87333 |
| Gersdorffite | Silver-white | #C0C0C0 |
| Millerite | Brass-yellow | #B5A642 |
| Millerite (tarnished) | Iridescent purple | #9B59B6 |
| Annabergite (pure Ni) | Apple green | #8DB600 |
| Annabergite (Co-rich) | Rose pink | #FF66CC |

---

## Individual Flavor Text

### Nickeline
> The copper-rose ghost. Nickeline doesn't look like nickel — it looks like copper, pale rose-gold with a metallic sheen that fools prospectors. But it's heavier than copper (7.8 g/cm³), harder, and when you heat it, it smells of garlic — arsenic volatilizing, a diagnostic trick that ancient miners learned the hard way. Nickeline is the primary ore of nickel in arsenide deposits, and it's the anchor of a paragenetic sequence that ends in pale green bloom. The Cobalt district of Ontario was named for the cobalt in skutterudite that accompanies nickeline, but the nickel was always there too — two elements so alike they share the same ore.

### Gersdorffite
> The sulfur compromise. Gersdorffite is what happens when arsenic and sulfur negotiate: neither gets the whole atom, so they share. The result is cubic where nickeline is hexagonal, steel-grey where nickeline is rose-gold, slightly harder, slightly more brittle. Gersdorffite is the sulfur-bearing member of the nickeline group, and in nature the two intergrade so seamlessly that telling them apart in hand specimen can be impossible without X-ray diffraction. The name honors von Gersdorff, a Saxon mining official who never saw the mineral named for him. Some things outlast their namesakes.

### Millerite
> The sulfur that stayed. Millerite is the most visually striking nickel mineral — acicular crystals in radiating sprays that look like golden sea urchins or the fur of some impossible metallic beast. It forms in reducing microenvironments where sulfur hasn't been oxidized away: sealed geodes, pyrite-rich pockets, organic matter. The Halls Gap geodes of Kentucky are famous for millerite sprays to 5 cm — crystals so delicate they seem to defy gravity, growing outward from the geode wall like frozen fireworks. When millerite tarnishes, it turns iridescent — purple, green, blue — a sulfur mineral's last defense against oxygen.

### Annabergite
> The nickel bloom. Annabergite is what nickeline becomes when it has time to weather — not dramatic, not spectacular, but quietly beautiful. Apple-green crusts, pearly luster, microcrystalline aggregates that spread across rock like verdigris. The name comes from Annaberg in Saxony, Germany, but the mineral is found wherever nickel arsenides oxidize: Cobalt (Ontario), Bou Azzer (Morocco), the Urals. When cobalt substitutes for nickel, the color shifts from apple-green to rose-pink — the annabergite-erythrite solid solution series. Annabergite is hydrated (8 H₂O per formula unit), which makes it soft (H = 1.5–2.5) and fragile. It's not a mineral you collect for display. It's a mineral you collect for meaning — the quiet green signature of nickel's patience.

---

## Cross-Zone Interactions

### With the Iron Oxidation Zone
Nickel and iron sulfides (pentlandite, pyrrhotite) weather together in magmatic sulfide deposits:
- Pyrrhotite → goethite/hematite (iron zone)
- Pentlandite → millerite → annabergite (nickel zone)
- Acid mine drainage from pyrrhotite oxidation can mobilize Ni²⁺, transporting it to different parts of the oxidation zone

### With the Cobalt Oxidation Zone
Ni and Co are geochemical twins — almost inseparable in nature:
- Skutterudite (CoAs₃) + nickeline (NiAs) weather together
- Erythrite (Co arsenate) + annabergite (Ni arsenate) form simultaneously
- Color zoning: green (Ni) → pink (Co) as fluid chemistry shifts
- Simulator implication: Co:Ni ratio should be a parameter controlling erythrite vs annabergite

### With the Arsenic Oxidation Zone
Arsenopyrite (FeAsS) oxidation releases both As and acid:
- Scorodite (FeAsO₄·2H₂O) forms from Fe + AsO₄
- Annabergite forms from Ni + AsO₄
- Both can coexist, creating green (annabergite) + yellow-brown (scorodite) assemblages
- Acid from pyrite/arsenopyrite oxidation can dissolve annabergite, preventing its formation until pH rises

---

## Famous Localities

### Nickeline
- **Cobalt, Ontario, Canada:** Type locality, associated with skutterudite and silver
- **Bou Azzer, Morocco:** Rose-gold crystals with erythrite coatings
- **Langesundsfjord, Norway:** Classic arsenide mineral locality

### Gersdorffite
- **Schneeberg, Saxony, Germany:** Type locality, silver-white cubes
- **Cobalt, Ontario, Canada:** Intergrown with nickeline
- **Keweenaw Peninsula, Michigan, USA:** Rare occurrence in copper deposits

### Millerite
- **Halls Gap, Kentucky, USA:** Famous geodes with radiating sprays to 5 cm
- **Antwerp, New York, USA:** Acicular crystals in dolostone
- **St. Andreasberg, Harz, Germany:** Type locality, capillary crystals

### Annabergite
- **Annaberg, Saxony, Germany:** Type locality, apple-green crusts
- **Cobalt, Ontario, Canada:** Green coatings on nickeline, world-class specimens
- **Bou Azzer, Morocco:** Exceptional green crusts on oxidized arsenide ore
- **Lavrion, Greece:** Ancient slag reworking, annabergite on ore dumps

---

## Simulator Wiring Notes

### New Parameters Needed
- `local_Eh` — microenvironment redox potential (for millerite in reducing pockets)
- `Ni:Co_ratio` — controls annabergite color (green → pink)
- `S:As_ratio` — controls nickeline vs gersdorffite

### New Events Needed
- `event_nickeline_oxidation` — NiAs → Ni²⁺ + AsO₄³⁻
- `event_millerite_tarnish` — surface iridescence on oxidation
- `event_nickel_bloom` — annabergite crust formation
- `event_annabergite_dehydration` — water loss at T > 200°C

### Local Reducing Pocket Model
For millerite formation in oxidizing zones:
```javascript
// Pseudocode for local Eh
FOR each microzone:
  IF microzone.sealed AND microzone.organic_matter > threshold:
    local_Eh = global_Eh - 0.4V  // Strongly reducing
    IF Ni > 50ppm AND S²⁻ > threshold:
      σ_millerite = calculate_supersat()
  ELSE:
    local_Eh = global_Eh
```

### Annabergite Color Model
```javascript
// Color based on Ni:Co ratio
IF Ni:Co_ratio > 3:
  color = "apple_green"  // #8DB600
ELIF Ni:Co_ratio > 1:
  color = "grey_green"   // #7C9D6A
ELIF Ni:Co_ratio > 0.33:
  color = "rose"         // #D68FB8
ELSE:
  color = "pink"         // #FF66CC (erythrite)
```

---

## Related Files
- `memory/research-cobaltite.md` — Co sulpharsenide, Co analogue
- `memory/research-erythrite.md` — Co arsenate, Co analogue of annabergite
- `memory/research-iron-oxidation-zone.md` — Acid mine drainage, pyrrhotite oxidation
- `memory/research-arsenopyrite.md` — FeAsS, primary arsenic source
- `memory/research-scorodite.md` — Fe arsenate, often associated with annabergite

---

*Nickel doesn't change its oxidation state. It doesn't have copper's redox drama or iron's acid generation. What nickel has is patience: NiAs weathers to Ni-arsenate, NiS tarnishes to iridescence, and through it all the Ni²⁺ ion stays green — the same green that colors emerald, hiddenite, and chrysoprase, but here muted by water and arsenate into something softer. The nickel oxidation zone is quiet. The colors are subtle. But the chemistry is precise, and the story — arsenic meeting sulfur meeting oxygen — is as old as weathering itself.*
