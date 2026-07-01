# Research: Marcasite (FeS₂) — Orthorhombic Polymorph of Pyrite

**Date:** 2026-06-23
**Researcher:** 🪨✍️ (cron expansion)
**Status:** Complete
**Linked files:**
- `memory/research-pyrite.md` — cubic polymorph
- `memory/research-pyrite-marcasite.md` — combined chemistry & paragenetic pair
- `memory/research-iron-oxidation-zone.md` — oxidation sequence (pyrite/marcasite → goethite/lepidocrocite → hematite → jarosite)

---

## Identity
- **Formula:** FeS₂ (dimorph of pyrite)
- **Crystal system:** Orthorhombic, space group Pnnm
- **Mineral group:** Sulfide (disulfide)
- **Hardness (Mohs):** 6–6.5
- **Specific gravity:** 4.87–4.92 (slightly lighter than pyrite at 4.95–5.10)
- **Cleavage:** {101} rather distinct; {110} in traces
- **Fracture:** Uneven to irregular
- **Luster:** Metallic, bright when fresh, often darker/tarnished than pyrite

## Color & Appearance
- **Typical color:** Tin-white to pale bronze-yellow on fresh surfaces; darkens on exposure to brownish or iridescent tarnish
- **Color causes:** Intrinsic metallic bonding; no chromophore ions. Slight color variation from pyrite due to different crystal structure affecting light reflectance.
- **Transparency:** Opaque
- **Streak:** Dark grey to black
- **Notable visual features:** Twin spearhead shapes ("Sperkise" from German Speerkies = spear-stone) are diagnostic. Cockscomb aggregates — radiating blade-like groups — are the iconic habit. Surface more prone to dark tarnish than pyrite. Anisotropism very strong under reflected light: yellow through pale green to dark green.

## Crystal Habits
- **Primary habit:** Tabular on {010}, often flattened; also pyramidal, prismatic, rarely capillary
- **Common forms/faces:** {101}, {110}, {010}; curved faces common
- **Twin laws:** Common and repeated twinning on {101} — produces the classic "spearhead" or "cockscomb" shapes. Less common on {011}. Intense twin lamellae.
- **Varieties:**
  - **Sperkise:** Twin spearhead crystal on {101}, particularly common in chalk-hosted marcasite (Cap Blanc-Nez)
  - **Blueite:** Ni variety (Sudbury District, Ontario) — Fe(S,Ni)₂
  - **Lonchidite:** As variety (Freiberg, Germany) — Fe(S,As)₂; also called kausimkies, kyrosite, metalonchidite
- **Special morphologies:** Cockscomb (radiating blade aggregates — diagnostic), reniform, botryoidal, stalactitic, fine-granular massive, nodules, concretions. Often forms crusts on matrix.

## Formation Conditions (SIMULATOR PARAMETERS)

### Temperature
- **Nucleation temperature range:** 25–300°C (lower than pyrite; marcasite is the low-T polymorph)
- **Optimal growth temperature:** 30–150°C (sedimentary/low-T hydrothermal sweet spot)
- **Decomposition temperature:** ~325°C (irreversible transformation to pyrite — the crucial simulator mechanic)
- **Temperature-dependent habits:** Lower T favors tabular/spear-shaped; higher T within range → more equant crystals

### Chemistry Required
- **Required elements in broth:** Fe (≥50 ppm), S (≥100 ppm as H₂S/HS⁻) — identical to pyrite
- **Optional/enhancing elements:** Ni (→ blueite variety), As (→ lonchidite variety)
- **Inhibiting elements:** High pH suppresses marcasite in favor of pyrite. High O₂ oxidizes to sulfates.
- **Required pH range:** pH < 6 (formation requires acidic conditions). Rate becomes rapid at pH < 4 (Schoonen & Barnes 1991). **This is the KEY differentiator from pyrite.**
- **Required Eh range:** Reducing to mildly oxidizing (more tolerant than pyrite)
- **Required O₂ range:** Low, but not as strictly anoxic as pyrite

### Secondary Chemistry Release
- **On formation:** Consumes Fe²⁺ and H₂S/HS⁻ — same stoichiometry as pyrite
- **Byproducts of nucleation:** H⁺ release (slightly more than pyrite due to acidic formation environment)
- **Byproducts of dissolution/oxidation:** Fe²⁺ + SO₄²⁻ + H⁺. Marcasite oxidizes FASTER than pyrite, producing sulfuric acid and iron sulfate. The hydrous iron sulfate forms white melanterite (FeSO₄·7H₂O) efflorescence.

### Growth Characteristics
- **Relative growth rate:** Moderate, similar to pyrite
- **Maximum crystal size:** To ~10 cm (usually much smaller than pyrite)
- **Typical crystal size in vugs:** 0.5–3 cm
- **Does growth rate change with temperature?** Yes — slower at lower T, faster near upper limit
- **Competes with:** Pyrite (pH is the decider — same chemistry, different pH windows), siderite (FeCO₃, competes for Fe at higher pH/CO₂)

### Stability
- **Breaks down in heat?** Irreversibly converts to pyrite above ~325°C. Thermodynamically metastable at ALL temperatures relative to pyrite, but kinetic barrier preserves it at ambient conditions.
- **Breaks down in light?** No direct photodecomposition (unlike realgar/proustite), but humidity + oxygen causes "pyrite decay" (actually worse for marcasite than pyrite)
- **Dissolves in water?** Very slowly in deoxygenated water; readily in oxidizing acidic water
- **Dissolves in acid?** More readily than pyrite — it's less stable
- **Oxidizes?** Yes, FASTER than pyrite. The famous "pyrite decay" in museum collections is often actually marcasite decay. Specimens crumble to white powder (melanterite) + rust stains, releasing sulfuric acid that attacks adjacent minerals and labels.
- **Dehydrates?** No
- **Radiation sensitivity:** Minimal structural damage; slight darkening possible at extreme doses

## Paragenesis
- **Forms AFTER:** Early pyrite (if pH was initially higher, then dropped)
- **Forms BEFORE:** Goethite/limonite (upon oxidation)
- **Commonly associated minerals:** Pyrite, galena, sphalerite, fluorite, dolomite, calcite, pyrrhotite
- **Zone:** Low-temperature hydrothermal, sedimentary (coal measures, chalk/limestone concretions), supergene (acidic oxidation zones)
- **Geological environment:**
  - Sedimentary concretions in chalk/limestone (classic European localities)
  - Coal beds and shales
  - Low-T hydrothermal veins (Tri-State district, etc.)
  - Oxidation zones with acidic conditions
  - Complex sulfide deposits

### The pH-Gated Polymorph Selection
Marcasite and pyrite are the textbook example of polymorph selection by pH:
- **pH > 5.5:** Pyrite dominates (thermodynamic ground state)
- **pH 4.5–5.5:** Overlap zone — both can nucleate
- **pH < 4.5:** Marcasite dominates (kinetically favored despite metastability)

The mechanism (Nature Communications 2016): at low pH, pyrite surfaces have higher surface energy than marcasite surfaces due to H⁺ adsorption. This flips the nucleation preference despite pyrite being the bulk thermodynamic ground state. The surface energy effect on nucleation rate explains the pH-selective growth.

## Famous Localities
- **Cap-Blanc-Nez, Pas-de-Calais, France:** Classic chalk-hosted marcasite — sharp individual crystals, crystal groups, and nodules. The Sperkise (spearhead) twins are particularly common here. Type locality for the habit name.
- **Reocín Mine, Cantabria, Spain:** Fine cockscomb aggregates in complex sulfide deposits
- **Joplin, Jasper County, Missouri, USA:** Cockscomb aggregates with galena and sphalerite in the Tri-State lead-zinc district
- **Kühlungsborn, Mecklenburg-West Pomerania, Germany:** Massive aggregates from steep coast
- **Tri-State District (Kansas-Missouri-Oklahoma):** Rensselaer Quarry (Indiana), Baxter Springs/Treece/Galena (Kansas), Sweetwater Mine (Missouri), Picher/Cardin (Oklahoma) — all produce fine cockscomb and spearhead specimens
- **Notable specimens:** Cockscomb groups from Joplin are the iconic habit everyone remembers. Cap Blanc-Nez spearheads are the classic textbook example.

## Fluorescence
- **Fluorescent under UV?** No (metallic mineral)
- **SW (255nm) color:** None
- **MW (310nm) color:** None
- **LW (365nm) color:** None
- **Phosphorescent?** No
- **Activator:** N/A
- **Quenched by:** N/A

## Flavor Text
> Marcasite is pyrite's awkward twin — same chemistry, different personality. Where pyrite grows confident cubes that catch the light like burnished armor, marcasite makes spearheads and rooster combs, blades stacked like folded origami in acid. It only forms when the water turns sour: below pH 6, marcasite wins the race; above it, pyrite takes over. The 2016 Nature Communications paper proved why — at acidic pH, marcasite's surfaces become more stable than pyrite's, flipping the competitive balance at the atomic level despite pyrite being the thermodynamic ground state. But marcasite carries a fatal flaw: it's metastable at every temperature. Heat it above 325°C and it converts irreversibly to pyrite, erasing every spear-shaped crystal and replacing it with the cubic default. Museum curators fear marcasite more than collectors love it — specimens slowly crumble in humid air, sweating sulfuric acid until the crystal becomes white melanterite powder and rust stains. The cockscomb aggregates from Joplin, Missouri — radiating blades of pale bronze — are the habit everyone remembers. Beautiful, unstable, and always a little bit doomed.

## Simulator Implementation Notes

### New Parameters Needed
- **pH threshold for polymorph selection:** pH < 5.5 → marcasite nucleation becomes possible; pH < 4.5 → marcasite dominates
- **Temperature cap for marcasite:** T > 325°C → marcasite cannot nucleate; existing marcasite converts to pyrite

### Nucleation Rule Pseudocode
```
IF Fe ≥ 50ppm AND S ≥ 100ppm AND T < 325°C AND Eh < 0:
  IF pH < 4.5:
    nucleate MARCASITE (80% probability)
    nucleate PYRITE (20% probability)
  ELIF pH 4.5–5.5:
    nucleate MARCASITE (50% probability)
    nucleate PYRITE (50% probability)
  ELIF pH > 5.5:
    nucleate PYRITE (dominant)
```

### Growth Rule Pseudocode
```
rate = base_rate * (Fe/S ratio factor) * temperature_factor
habit: 
  IF σ < 2 → tabular {010}
  IF σ 2–5 → spearhead twin on {101}
  IF σ > 5 → cockscomb (radiating blade aggregate)
IF T > 325°C: 
  CONVERT to pyrite (irreversible, habit reset to cubic)
```

### Habit Selection Logic
- **Low supersaturation:** Tabular on {010}, individual crystals
- **Moderate supersaturation:** Spearhead twins on {101} (the "Sperkise" habit)
- **High supersaturation:** Cockscomb aggregates — radiating blade-like groups, diagnostic for marcasite
- **Sedimentary concretion event:** Nodules/reniform masses in chalk/limestone matrix

### Decomposition Products
- **Marcasite at 325°C →** pyrite (polymorph conversion, retains FeS₂ chemistry but resets to cubic habit)
- **Marcasite/pyrite oxidation →** Fe²⁺ + SO₄²⁻ + H⁺ → melanterite (FeSO₄·7H₂O, white efflorescence) → goethite/limonite (FeOOH/Fe₂O₃·nH₂O, rust)

### Museum Decay Mechanic (Unique to Marcasite)
In the simulator's "Collector's View" or long-term storage:
- Marcasite specimens have a decay timer in humid conditions
- After N turns in high-humidity environment: specimen degrades
- Visual: white melanterite efflorescence appears, then rust stains
- Can be prevented by storing in low-humidity conditions
- This is a real geological phenomenon — "pyrite decay" in museum collections

## Variants for Game

1. **Sperkise (Spearhead Twin)** — pH < 5, moderate supersaturation, temperature 50–150°C. The classic twin on {101} — sharp, bladed, often crossing at angles. Cap Blanc-Nez style.

2. **Cockscomb Aggregate** — pH < 4, high supersaturation, temperature 30–100°C. Radiating blade-like groups that look like a rooster's comb. Joplin/Tri-State style. Most visually distinctive variant.

3. **Chalk Nodule** — sedimentary concretion event, pH < 5, low supersaturation. Reniform/botryoidal masses in chalk or limestone matrix. Cap Blanc-Nez/Dover style. Often requires breaking the nodule to reveal internal crystals.

4. **Thermal Survivor** — rare variant: marcasite that formed at high T within its stability window (250–300°C) and was preserved by rapid cooling. Shows more equant, less twinned habit. Becomes pyrite if reheated.

## Cross-References
- **Polymorph relationship:** Pyrite (`memory/research-pyrite.md`, `memory/research-pyrite-marcasite.md`)
- **Oxidation products:** Goethite, lepidocrocite, hematite, jarosite (`memory/research-iron-oxidation-zone.md`)
- **Fe-sulfide family:** Pyrrhotite (Fe₁₋ₓS) — higher T, S-deficient
- **Competing Fe-minerals:** Siderite (FeCO₃), chalcopyrite (CuFeS₂)
- **Associated in complex sulfide deposits:** Galena, sphalerite, fluorite, dolomite, calcite
- **Acid generation:** Marcasite/pyrite oxidation is the main acid source for supergene enrichment — drives copper, lead, zinc oxidation zones

---

*Marcasite: proof that being thermodynamically favored isn't everything. Sometimes the underdog wins the nucleation race — but only in acid, and only for a while.*
