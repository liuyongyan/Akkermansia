# Design Notes — Strategic Decisions Behind the Proposal

These notes record *why* the proposal is shaped the way it is, so collaborators and advisors can see the reasoning, not just the result. They complement `proposal.md`.

## 1. Live vs pasteurized AKK
- The landmark trial (Mount et al., *Nat Med* 2026) used **pasteurized (non-viable)** AKK, which does not colonize and requires continuous dosing. Pasteurized AKK can even outperform live in some metabolic readouts (Cani & de Vos 2017; Plovier 2017).
- We deliberately study **live** AKK. Rationale: the unique, higher-value proposition of a live strain is **durability** — a short course that engrafts and self-sustains, instead of indefinite supplementation — plus a behavioral co-benefit (efficacy that depends on lifestyle gives patients a concrete reason to maintain good diet/sleep).
- Consequence: **engraftment** (does the introduced strain establish?) becomes the decisive variable the dead product never had to satisfy. The whole proposal is built around it.

## 2. Why "sleep/lifestyle effect" alone is not enough for CNS
- Diet → AKK is **already established** (Desai 2016; Roopchand 2015; Everard 2013) → used as the *anchor* axis, not the novelty.
- Circadian × microbiome × immunity is **already established** (Thaiss 2016; Brooks 2021).
- Sleep → AKK/mucus is **already published** (Wang 2023).
- So "bad lifestyle → worse colonization" is a descriptive phenotype = a solid specialist-journal paper, not a CNS-main thesis. Sleep/circadian disruption must be the **perturbation tool**, not the headline.

## 3. The chosen novelty: A + B (not a second strain)
- **A — Host clock-gated "colonization window."** The scientific contribution: an introduced live strain engrafts only into a permissive, rhythmic niche state, so **dosing time and lifestyle alignment — not just dose — set engraftment**. The translational contribution (the "how"): chrono-dosing + lifestyle prescription for durable AKK. Both layers are required — "how" alone reads as lifestyle advice; "why" alone has no payoff.
- **B — Feedback loop / bistability.** Host clock gates AKK, and engrafted AKK repairs the clock-niche (Wang 2023) → positive feedback with two stable states (engrafted vs cleared). Reframes clinical responder/non-responder as a **controllable bistable system**, not fixed patient luck. Adds conceptual depth with near-zero extra experiments (one re-entrainment test in Module 2).
- **Why not a second strain:** its only job would be to claim generality ("a law of live biotherapeutics, not an AKK quirk"). But our mechanism is specific to a **mucin specialist**; a mismatched second strain tests a *different* mechanism and could fail for unrelated reasons. Generality is instead carried by **host-side causal genetics** — *Bmal1*^ΔIEC shows the gate is a host clock gene, which logically extends to any niche-dependent colonizer. A second (mechanism-matched) strain remains an optional light-touch confirmatory add-on if a reviewer demands it.

## 4. Is the "colonization window" established, or our hypothesis?
**Still our hypothesis** — but a high-prior one, not a guess. The claim decomposes into three links:
1. The gut/mucus niche oscillates diurnally — **established** (Thaiss 2016: epithelial-adherent microbiota up to ~10× higher in active phase; rhythmic mucus thickness). High confidence.
2. The host clock gates whether an *exogenous* microbe colonizes — **established for pathogens** (Brooks 2021: time-of-day colonization resistance to *Salmonella* via rhythmic immunity). Strong support.
3. This gating applies to and is exploitable for a *therapeutic introduced strain* (chrono-dosing → engraftment) — **untested = our original contribution.**

Rough subjective priors: niche is circadian-gated (~0.9); introduced-AKK engraftment shows a measurable time-of-day window (~0.7); chrono-dosing yields a *large, translationally actionable* effect (~0.4–0.6, highest risk/reward).

**Main threats to the window being real or strong:**
- **AKK self-repair (biggest):** a robust strain may engraft regardless of timing, buffering away the window. This is the crux ("engraftment vs repair") and is what the chrono-dosing + feedback experiments are designed to *measure*, not assume.
- **Colonization resistance** in conventional mice may swamp timing effects (mitigated by antibiotic pre-treatment, which itself perturbs the niche).
- **Mean vs rhythm:** if engraftment tracks mean mucus (diet-set) more than its rhythm (clock-set), the window is real but small and diet dominates.

**De-risking:** the design is informative either way — strong window → chrono-dosing prescription; weak window → engraftment is timing-robust and diet is the dominant lever (a publishable correction). Built into Expected Outcomes.

## 5. Major scope/rigor decisions already applied
- Dropped the human cohort and humanized germ-free / human ML responder work (no data source, infeasible for 2–3 students; biostatistics modeling moved onto the mouse cohort).
- Clean **2×2×2 factorial (diet × circadian × ±AKK), both sexes**, with vehicle arms in every cell + a priori power analysis.
- **Trackable marked strain** (rifampicin-resistant MucT derivative + strain-specific qPCR) to separate introduced from endogenous AKK; antibiotic pre-treatment to open the niche.
- Circadian disruption via **chronic light-phase advance ("jet-lag")**, not 12-week mechanical sleep deprivation (avoids stress confounds).
- **AI claims corrected:** AlphaFold 3 gives structures/confidence (ipTM/pTM), *not* ΔG — energetics via downstream MD/MM-GBSA; Amuc_1100→TLR2 cited to Plovier 2017; Geneformer scoped to transcriptional control of the secretory program, not O-glycosylation.
- **Citations fixed:** corrected Cani & de Vos 2017 (was mis-cited), replaced the circadian ref with the actual Gutierrez Lopez 2021, dropped the off-topic blunt-chest-trauma paper, added Plovier/Everard/Roopchand/Desai/Dao/Thaiss/Brooks.

## 6. Open items to revisit
- Control diet currently low-fat/high-fiber (clean fiber↔fat contrast vs Western); decide whether to also keep a standard-chow reference arm.
- Whether to run the full 8-group factorial or a lighter circadian-focused subset if feasibility tightens.
- Optional mechanism-matched second strain as a generality safeguard (only if requested in review).
