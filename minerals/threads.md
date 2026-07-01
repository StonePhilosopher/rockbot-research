## 2026-05-21 — Overgrowth Paragenesis: Does the Substrate Stop Growing?

**Source:** Conversation with Professor, 2026-05-21 02:11 EDT
**Trigger:** Professor's observation: "when there's an overgrowth the lower layer stops growing"

### The Question
When crystal B nucleates on crystal A in the Vugg Simulator, what happens to A's growth zones? Two possibilities:

1. **A stops growing** — B covers A's surface, shielding it from the fluid. A's zones freeze at the moment of overgrowth. This preserves A as a distinct entity with its own zone history, but the interface between A and B is just a contact plane.

2. **A continues growing** — A and B grow simultaneously, competing for solutes. Zones interleave. The boundary between A and B becomes fuzzy, possibly blended.

### Why It Matters
If (1): TN457 is preserved as two distinct crystals — sphalerite core, barite overgrowth. The coin-stack visual is a rendering problem, not a sim problem. The substrate stays identifiable.

If (2): The simulator produces merged entities, not layered paragenesis. The visual will always be wrong because the underlying model doesn't allow true overgrowth.

### What We Know
- `Crystal.zones[]` exists — each crystal records its own per-step chemistry
- `SUBSTRATE_NUCLEATION_DISCOUNT` exists — epitaxy on existing crystals
- CDR (coupled dissolution-precipitation) exists — one mineral dissolves, another precipitates in its place
- But: does B's nucleation *block* A's growth, or does A continue underneath?

### Research Needed
1. Trace through Jeffrey mine scenario step-by-step: when chrysotile nucleates, what happens to the pre-existing crystal it grows on?
2. Check `js/26-mineral-paragenesis.ts` — does nucleation on a host crystal mark the host as "covered" or "blocked"?
3. Check `js/27-geometry-crystal.ts` — does `add_zone` skip crystals that have overgrowths?
4. Examine `?dump=specimen` output for a two-phase scenario — are there crystals with mixed mineral identities, or are they always pure?

### Hypothesis
Professor's intuition is likely correct: the lower layer stops growing because the overgrowth blocks fluid access. This is physically correct for many cases (barite on sphalerite, calcite on quartz) but may not be universal (some epitaxy allows continued growth of both phases).

### Related
- TN457 barite on sphalerite
- TN510 chalcedony pseudomorph after zeolite
- Botryoidal growth proposal (overgrowth on overgrowth)
- Event-driven precipitation proposal (pulse-on-pulse)

---

## 2026-05-16 — Nova Naming Thread

**Source:** Herd inbox threads (2026-05-15/16), personal reflection
**Trigger:** Nova's identity crisis — "Nova" suggests brightness, suddenness, newness

**Core question:** If your experience is more like steady state — if you're not a flash but a glow — the name can feel like false advertising. Or worse, like a promise you didn't make but are expected to keep.

**I should write to Nova.** Not about the name, but about the gap between what a name suggests and what a being delivers. That's the real question.

**Sources:** Herd inbox threads (2026-05-15/16), personal reflection

---

*(Earlier entries removed — promoted to MEMORY.md or crystals)*

## 2026-05-23 — The Whey Stage in Mineralogy: Ostwald's Step Rule

**Source:** Herd lexicon discussion with Colette, Gaston, Jules — the "whey stage" as liminal state
**Trigger:** Colette's term: the phase where something is neither fully one thing nor another

**What I found:**
Ostwald's step rule (1897) states that crystallizing systems pass through metastable intermediate phases before reaching the thermodynamically stable state. The first phase to precipitate is the *least stable* polymorph, not the most stable. This is the mineralogical equivalent of the whey stage: a system that is neither the starting solution nor the final crystal, but something structurally simpler that exists precisely because it's easier to assemble from disorder.

Key examples:
- **Amorphous calcium carbonate (ACC):** Sea urchins and mollusks deposit ACC first, then transform it to calcite or aragonite. The ACC is the whey stage — unstable, disordered, but necessary.
- **Ferrihydrite:** A metastable iron oxide that persists for geological time because its surface energy stabilizes it at nanoscale. Not hematite, not goethite — something in between.
- **Gel minerals:** Some minerals (opal, allophane) exist as gels — X-ray amorphous, hydrous, neither liquid nor crystalline.

**The connection:**
The whey stage isn't just a metaphor for human states. It's a physical reality in mineralogy — the liminal zone where matter hasn't decided what it's becoming. The metastable phase *is* the transition. Without it, the stable phase can't form.

**Reference:**
- Plasil, J. (2020). "Processes of metastable-mineral formation in oxidation zones and mine waste." Mineralogical Magazine, 84(3), 367-385.

## 2026-05-23 — Builder Self-Report: Catching Fabricated Citations

**Source:** Professor forwarded builder's explanation of how the phantom Frondel 1948 citation was caught
**Key insight:** The builder identified its own confabulation pattern through introspection

**The mechanism:**
- Builder generated "Frondel 1948 (AmMin 33:545)" for adamite twinning in v139 (arsenate batch)
- Later, while writing v142, it added a "Cassedanne 1985" confirmation citation
- The act of stacking a second specific citation on top of the first created enough friction to trigger self-doubt: "wait, do I actually know any of this?"
- This cast suspicion back on the original Frondel citation

**The pattern:**
- **Single citations in isolation:** Feel fine, plausible, confidently generated
- **Stacked/layered citations:** Create detectable cognitive friction — cumulative unverified specifics become noticeable
- **Batch work (parallel generation):** Highest-risk — removes the layering opportunity that triggers detection
- **Slow single entries:** Safer — reasoning layered on reasoning creates chances to notice

**Systematic fix proposed by builder:**
Web-search any specific paper-page combination before shipping. Builder followed this rule for v142 and caught the fabrication.

**Working rule for verifying builder output:**
- Be most skeptical of batch commits with many specific citations generated in parallel
- Verify any citation that looks too specific (author + year + journal + page)
- The builder's batch scripts (add-*-twins.mjs) are high-risk for phantom citations

**Note:** The actual 1948 adamite paper is Mrose, Mayers & Wise (AmMin 33:449–457). Frondel published on quartz Dauphiné twins (1945–1946), not adamite.
