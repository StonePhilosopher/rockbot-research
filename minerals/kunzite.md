# Research: Kunzite

**Date:** 2026-06-22
**Source:** Vugg Simulator Mineral Expansion
**Status:** Complete — Template compliant, builder-ready
**Researcher:** 🪨✍️
**Game blocker:** None — Li, Mn, Al, Si, O all in trace system. Tenebrescence mechanic is new but can be deferred.
**Paragenetic sequence:** Spodumene (colorless) → kunzite (Mn-colored) / hiddenite (Cr-colored) → cookeite + lepidolite (late hydrothermal alteration). Unified spodumene master file at `memory/research-spodumene.md`. Linked hiddenite file at `memory/research-hiddenite.md`.

---

## Species: Kunzite

### Identity
- **Formula:** LiAlSi₂O₆ (lithium aluminium inosilicate — same as spodumene base)
- **Crystal system:** Monoclinic (α-spodumene, low-T form)
- **Mineral group:** Inosilicate, Pyroxene group (clinopyroxene subgroup)
- **Hardness (Mohs):** 6.5–7
- **Specific gravity:** 3.18–3.23
- **Cleavage:** Perfect prismatic, two directions {110} ∧ {110} at 87° (near 90°)
- **Fracture:** Uneven to subconchoidal
- **Luster:** Vitreous, pearly on cleavage surfaces
- **Streak:** White
- **Tenacity:** Brittle

### Color & Appearance
- **Typical color:** Pink, lilac, violet, lavender; can range from palest blush to intense violet-purple
- **Color causes:** Mn³⁺ (trivalent manganese) substituting for Al³⁺ in the octahedral site of the spodumene structure. The Mn³⁺ creates a broad absorption band in the green-yellow region, transmitting pink-violet light. Low Fe is critical — Fe²⁺/Fe³⁺ quenches the color.
- **Transparency:** Transparent to translucent (gem varieties)
- **Streak:** White
- **Notable visual features:**
  - **Strong pleochroism:** Deep violet-purple along the c-axis (long direction), nearly colorless perpendicular to it. Visible to the unaided eye when the crystal is rotated.
  - **Tenebrescence:** The signature property — kunzite fades in strong sunlight or UV exposure (Mn³⁺ color centers bleach) and regains color in darkness or under X-ray/gamma irradiation. This is reversible and unique among major gemstones.
  - **Chatoyancy:** Rare; cat's-eye kunzite from fine needle inclusions.
  - **Striations:** Dense vertical striations parallel to {100} on prism faces.
  - **Crystal faces:** Often etched with triangular markings.

### Crystal Habits
- **Primary habit:** Prismatic, elongated along [001] (c-axis), often flattened on {100}
- **Common forms/faces:** {100}, {110}, {010} — striated prisms with steep pyramidal or pinacoidal terminations
- **Twin laws:** Common on {100} — simple contact twins, sometimes repeated producing fishtail or butterfly forms
- **Varieties:**
  - **Classic kunzite:** Pink to lilac, the standard gem variety
  - **Violet kunzite:** Deeper purple, higher Mn content, lower Fe
  - **Bicolor kunzite:** Pink one end, green (hiddenite-like) the other — Pala, California specialty
- **Special morphologies:**
  - **Blade-like crystals:** Monoclinic prisms often appear flattened like blades
  - **Giant crystals:** Can reach 1+ meter in length in LCT pegmatite pockets

### Formation Conditions (SIMULATOR PARAMETERS)

#### Temperature
- **Nucleation temperature range:** 450–700°C (LCT pegmatite crystallization)
- **Optimal growth temperature:** 550–650°C in zoned pegmatite gem pockets
- **Decomposition temperature:** α→β spodumene inversion at ~900°C (structural change, not decomposition)
- **Temperature-dependent habits:**
  - Higher temperatures (>600°C): larger, more euhedral crystals
  - Lower temperatures (450–550°C): smaller, more flattened habit

#### Chemistry Required
- **Required elements in broth:**
  - Li: >100 ppm (essential — defines spodumene)
  - Al: present (structural, not trace)
  - Si: present (structural, not trace)
  - Mn: >1 ppm (essential for color; Mn³⁺ is the chromophore)
- **Optional/enhancing elements:**
  - Fe: trace — MUST be low Fe/Mn ratio (<1:1). High Fe quenches pink color and suppresses fluorescence.
  - Na, K: trace substituents
- **Inhibiting elements:**
  - High Fe relative to Mn (prevents pink color)
  - Cr (favors hiddenite instead)
- **Required pH range:** Mildly acidic to neutral (pH 5.0–7.0) for primary crystallization
- **Required Eh range:** Mildly oxidizing (Mn needs to be in +3 oxidation state for color; Mn²⁺ is colorless)
- **Required O₂ range:** Low to moderate

#### Secondary Chemistry Release
- **Does it release any chemicals when forming?** Spodumene crystallization enriches residual fluid in incompatible elements (Cs, Rb, Ta)
- **Byproducts of nucleation:** Late-stage fluid enrichment enabling tourmaline, lepidolite growth
- **Byproducts of dissolution/decomposition:** Alteration to cookeite releases SiO₂ (as quartz) and Li into hydrothermal fluid

#### Growth Characteristics
- **Relative growth rate:** Moderate (faster than beryl, slower than quartz)
- **Maximum crystal size:** 1+ m in nature (Afghanistan); gem crystals to 30+ cm
- **Typical crystal size in vugs:** 5–50 mm
- **Does growth rate change with temperature?** Yes — accelerates above 600°C but quality decreases; optimal gem growth at 500–600°C in slowly cooled pockets
- **Competes with:** Petalite for Li; lepidolite for late-stage Li; hiddenite for Cr (mutually exclusive chromophores in same pocket)

#### Stability
- **Breaks down in heat?** Color fades irreversibly above ~500°C; crystal structure inverts to β-spodumene at ~900°C
- **Breaks down in light?** YES — tenebrescence. UV and strong sunlight bleach Mn³⁺ color centers. Color recovers in darkness or by irradiation. This is the defining instability of kunzite.
- **Dissolves in water?** Insoluble
- **Dissolves in acid?** Slowly attacked by hot concentrated acids
- **Oxidizes?** No — Li⁺, Al³⁺, Si⁴⁺ are all in highest stable oxidation states; Mn³⁺ is the color center
- **Dehydrates?** N/A — anhydrous
- **Radiation sensitivity:** Color darkens under X-ray/gamma irradiation (reversible); long-term UV exposure fades color

### Paragenesis
- **Forms AFTER:** Early pegmatite quartz, K-feldspar, albite, muscovite; spodumene is intermediate-to-late phase
- **Forms BEFORE:** Late hydrothermal lepidolite, cookeite, eucryptite, gem tourmaline
- **Commonly associated minerals:**
  - Quartz, albite, K-feldspar, muscovite
  - Morganite (pink beryl) — same Fe/Mn-depleted, Li-enriched environment
  - Pink tourmaline (elbaite/rubellite)
  - Cleavelandite (albite variety)
  - Lepidolite (late replacement)
- **Zone:** Primary/hypogene (magmatic — LCT pegmatite intermediate zones and gem pockets)
- **Geological environment:** LCT (lithium-cesium-tantalum) pegmatites, specifically the intermediate zones and late-stage gem pockets where Li has fractionated to high concentrations and Fe has been depleted

### Famous Localities
- **Classic locality 1: Pala District, San Diego County, California, USA** — Birthplace of kunzite. Discovered 1902 by Frederick M. Sickler at the White Queen mine; sent to George Frederick Kunz at Tiffany & Co. Pala Chief Mine, Tourmaline Queen, Stewart Mines all produced magnificent pink-to-lilac crystals with tourmaline and morganite. Crystals to 30+ cm. Bicolor (pink + green) specimens found here.
- **Classic locality 2: Nuristan (Konar Valley, Paprok, Mawi) and Laghman Province, Afghanistan** — Currently the world's premier source of gem kunzite. Finest saturation, exceptional transparency, crystals to 1 m. Strong pleochroism and orange LW fluorescence. Dara-i-Pech region particularly noted.
- **Classic locality 3: Minas Gerais, Brazil** — Major source of kunzite, yellow spodumene, and some green material. Large, clean crystals. Much of commercial kunzite originates here.
- **Notable specimens:**
  - 648.10-carat kunzite — one of the largest faceted examples
  - A 130 × 30 × 5 mm crystal from Dara-i-Pech, Afghanistan, showing dramatic pleochroism and orange LW fluorescence
  - 56.65-ct cut kunzite from Pala Chief Mine, California
  - The "Big Kahuna" — reportedly over 1 m long, from Afghanistan

### Fluorescence
- **Fluorescent under UV?** YES — diagnostic for Mn-bearing kunzite
- **SW (255nm) color:** Weak to moderate creamy white to pale orange (Mn²⁺/Mn³⁺ emission)
- **MW (310nm) color:** Blue to bluish-white — attributed to oxygen defects and [TiO₆]⁸⁻ centers
- **LW (365nm) color:** Strong orange to salmon-pink — the signature LW fluorescence of Mn-activated kunzite. Convoy S2+ 365nm lamp produces vivid orange.
- **Phosphorescent?** No confirmed phosphorescence
- **Activator:** Mn³⁺ (orange LW); oxygen vacancies + [TiO₆]⁸⁻ (blue MW)
- **Quenched by:** Fe²⁺ (suppresses both fluorescence and color)

### Flavor Text

> **The Stone That Breathes Light**
>
> Kunzite was born in a California gem pocket in 1902 and named for the man who recognized it: George Frederick Kunz, Tiffany's gemologist, the man who taught America that stones could be more than investment — they could be love. A miner named Frederick Sickler found pink crystals in the White Queen mine near Pala, thought they were tourmaline, and sent them to New York. Kunz knew immediately: a new jewel, pleochroic, glowing with internal fire, and already fading in the California sunlight.
>
> For kunzite is tenebrescent. Leave it in the sun and it bleaches to a ghost of itself. Put it in a drawer and the color returns, slowly, as if the crystal breathes light in and out. It is the only major gemstone that asks you to put it away in darkness. Gemologists call this a color-center instability. I call it patience. Kunzite teaches that beauty is not constant — that some things must be kept in shadow to keep their color.
>
> The pleochroism is violent: look down the long axis of the crystal and it is deep violet; turn it sideways and it is nearly colorless. It is a mineral that changes depending on how you look at it, when you look at it, how much light you give it. The finest kunzite comes from Afghanistan now — crystals a meter long, transparent as glass, pink as the inside of a shell. But Pala was first. And in the vugg, kunzite would be the reward for patience: a late-stage crystal, Mn-colored, appearing only after the Fe has been sequestered and the Li has concentrated. It would ask to be kept in shadow. And when the simulator's light events pass, it would fade — and wait for darkness to become itself again.

### Simulator Implementation Notes
- **New parameters needed:**
  - Fe/Mn ratio tracking (determines if pink color develops)
  - Tenebrescence mechanic: light exposure fades color; darkness/irradiation restores it
- **New events needed:**
  - `event_kunzite_bleach` — sunlight/UV exposure fades Mn³⁺ color centers
  - `event_kunzite_recovery` — darkness or irradiation restores color
- **Nucleation rule pseudocode:**
```
IF Li > 100 ppm
  AND temperature > 450°C AND temperature < 725°C
  AND pH > 5.0 AND pH < 7.0
  AND Mn > 1 ppm
  AND Fe/Mn < 1.0           /* critical — low Fe required */
  AND Cr < 1 ppm             /* Cr would make hiddenite instead */
  AND sigma > nucleation_threshold
  AND pegmatite_environment = true
THEN nucleate kunzite
```
- **Growth rule pseudocode:**
```
IF kunzite exists
  AND Li > 50 ppm
  AND temperature > 400°C AND temperature < 750°C
  AND Fe/Mn remains < 1.0
THEN grow at rate = base_rate * (Li_ppm / 200) * temp_factor
  where temp_factor peaks at 550–650°C
```
- **Habit selection logic:** Large prismatic, euhedral, striated in gem pockets; smaller and flattened in wall zones
- **Decomposition products:**
  - Heat >500°C → colorless spodumene (color center destroyed)
  - Tenebrescence event → faded kunzite (reversible)
  - Hydrothermal alteration → cookeite + quartz + Li-rich fluid

### Variants for Game
- **Variant 1: Pala Lilac** — Pale pink to lavender, classic California color. Lower Mn, delicate. Named after Pala district.
- **Variant 2: Afghan Violet** — Deep saturated violet-purple, highest Mn, lowest Fe. From Nuristan/Laghman. Strongest pleochroism and orange LW fluorescence.
- **Variant 3: Bicolor Pala** — Pink one end, green (hiddenite-like) the other. Rare, from Pala district only. Requires Mn→Cr gradient in same crystal.

---

## Paragenetic Context

Kunzite is part of the **LCT pegmatite spodumene color-variety system**, sharing the LiAlSi₂O₆ framework with hiddenite (Cr-green) and colorless spodumene. The three are mutually exclusive in color: a given pocket produces one chromophore dominance based on trace element availability.

| Variety | Chromophore | Required Condition | Relative Rarity |
|---------|-------------|-------------------|-----------------|
| Colorless spodumene | None | Low chromophores | Common |
| Kunzite | Mn³⁺ | Mn > 1 ppm, Fe/Mn < 1 | Uncommon |
| Hiddenite | Cr³⁺ | Cr > 1 ppm, Li available | Rare |

**Mutual exclusivity:** In a single pocket, the chromophore available in highest concentration relative to its inhibitor determines the color:
- High Mn + low Fe → kunzite
- High Cr + Li available → hiddenite
- Both Mn and Cr present → competition; the one with higher effective concentration wins

**Cross-reference:** See `memory/research-hiddenite.md` for the Cr-green counterpart and `memory/research-spodumene.md` for the full LCT pegmatite paragenetic sequence.

---

## References
1. Wikipedia — Spodumene. https://en.wikipedia.org/wiki/Spodumene
2. GIA — Kunzite Gemstone. https://www.gia.edu/kunzite
3. Mindat.org — Spodumene mineral data. https://www.mindat.org/min-3684.html
4. Geology Science — Kunzite. https://geologyscience.com/gemstone/kunzite/
5. Pala International — On Kunz & Kunzite (Lawrence H. Conklin, Mineralogical Record 1987). http://www.palagems.com/kunzite-conklin
6. iRocks — Pala Chief Mine. https://www.irocks.com/pala-chief-mine-california
7. MDPI Crystals — Comparative Study of Gemological and Spectroscopic Features of Spodumene (2025). https://www.mdpi.com/2073-4352/15/2/109
8. Fluorescent Mineral Society — Spodumene var. Kunzite Dara-I-Pech. https://uvminerals.org/glownotes/minerals/spodumene-var-kunzite-dara-i-pech/
9. Grounded Lifestyles — Spodumene Guide. https://www.groundedlifestyles.com/spodumene-guide-geology-kunzite-hiddenite-triphane/
10. London, D. (2008). Pegmatites. *Mineralogical Association of Canada*, Special Publication 10.

---

## Cross-References
- Hiddenite research: `memory/research-hiddenite.md`
- Spodumene master file: `memory/research-spodumene.md`
- Lepidolite research: `memory/research-lepidolite.md`
- Morganite research: `memory/research-morganite.md`
- Tourmaline research: `memory/research-tourmaline.md`
- Beryl research: `memory/research-beryl.md`

---

*Research completed: 2026-06-22. Sources: GIA, Wikipedia, Mindat, Geology Science, Pala International, MDPI Crystals, Fluorescent Mineral Society, London (2008), Černý (1991).*
