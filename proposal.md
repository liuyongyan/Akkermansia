# Research Proposal

**Project Title:** A Host Circadian Clock-Gated "Colonization Window" Determines Engraftment of Live *Akkermansia muciniphila*: Lifestyle- and Timing-Optimized Dosing for Durable Metabolic Biotherapy

**Major:** Biostatistics / Computational Genomics and Bioinformatics

**Research Direction:** Gut Microenvironment & Translational Medicine; AI for Science (AI4S)

---

## Abstract

Live *Akkermansia muciniphila* (AKK) is a leading next-generation probiotic for obesity and insulin resistance. Its central promise over the pasteurized (non-viable) product is **durability**: a live strain that engrafts in the colonic mucus niche could deliver lasting benefit from a short course rather than indefinite daily dosing. A 2026 *Nature Medicine* trial (Mount et al.) confirmed clinical efficacy for *pasteurized* AKK in weight maintenance, but that product does not colonize and showed large inter-individual heterogeneity. The decisive question for *live* biotherapy is therefore not whether AKK can act, but **what determines whether an introduced live strain engrafts** — and engraftment is governed by the host niche.

Our central hypothesis is that the host circadian clock opens a **colonization window**: because the mucus niche oscillates under peripheral-clock control, whether introduced AKK establishes depends on the niche's rhythmic state, so that **dosing time and lifestyle alignment — not just dose — set engraftment success.** This is not a blind guess: host-clock control of whether an *exogenous* microbe colonizes is already established for pathogen colonization resistance (Brooks et al., *Cell* 2021), and the niche's diurnal oscillation is well documented (Thaiss et al., *Cell* 2016) — we extend a demonstrated principle to therapeutic engraftment, where it is untested. We further propose that because engrafted AKK can itself repair the clock-controlled mucus niche (Wang et al., *Cell Host Microbe* 2023), host clock and microbe form a **feedback loop with two stable states** — engrafted versus cleared — reframing the clinical "responder/non-responder" split as a controllable bistable system rather than fixed patient luck.

Three modules test this. (1) A factorial mouse design with vehicle controls quantifies how diet and circadian misalignment gate engraftment and metabolic efficacy of a genetically trackable live AKK strain. (2) Strain-specific qPCR kinetics, FISH, metatranscriptomics, scRNA-seq, and metabolomics resolve the goblet-cell/MUC2 mechanism and test the feedback (does engraftment restore the mucus rhythm?), with AI used within its validated scope — AlphaFold 3 for AKK–host interface structural hypotheses, a single-cell foundation model for clock-controlled regulators — followed by causal validation in intestinal-epithelial *Bmal1* and *Tlr2* knockouts. (3) The actionable payoff: whether **circadian-timed dosing** and active-phase time-restricted feeding open the window and rescue efficacy in disrupted hosts, plus a causal-mediation and predictive model linking baseline host state to engraftment. The design is informative under either outcome — a strong window yields a chrono-dosing prescription; a weak one shows engraftment is timing-robust and identifies diet as the dominant lever. Either way, the work converts diet and sleep from generic advice into a mechanistic, testable part of the prescription.

---

## 1. Introduction & Significance

### 1.1 Why live AKK, and why engraftment is the decisive variable
GLP-1 receptor agonists (e.g., semaglutide, orforglipron) produce strong weight loss but rebound on cessation and carry cost and gastrointestinal burdens (Aronne et al., *Nat Med* 2026). *A. muciniphila*, a mucosal anaerobe, is inversely associated with adiposity, inflammation, and insulin resistance. In May 2026, *Nature Medicine* reported that **pasteurized** AKK (MucT) blunted weight regain during a 24-week maintenance phase (Mount et al.; ITT n ≈ 84), with adipose remodeling toward mitochondrial/oxidative pathways.

Two facts from that trial define our problem. The efficacious product was **non-viable and does not colonize** — its benefit required continued dosing — and response was **heterogeneous**. The distinct, higher-value proposition of a *live* biotherapeutic is durability: a strain that establishes in the mucus niche could convert a chronic supplement into a short, self-sustaining course. That proposition stands or falls on the one variable the dead product never had to satisfy — **engraftment** — which is governed by the host niche. Controlling that niche is the prerequisite for any durable live-AKK therapy.

### 1.2 The mucus niche is controlled by diet and by the circadian clock
The colonic mucus layer (principally MUC2 from goblet cells) is AKK's ecological niche and carbon source. Two host inputs shape it:

- **Diet (established).** Fiber and polyphenols expand AKK and reinforce the mucus barrier; fiber deprivation drives the microbiota to forage host mucin and thins the barrier; Western high-fat/low-fiber diets reduce AKK (Desai 2016; Roopchand 2015; Everard 2013; Dao 2016). Diet is a validated lever and serves as our anchor axis.
- **Circadian rhythm (the novel axis).** The intestinal epithelium is under peripheral-clock control (*Bmal1, Clock, Per*); mucus thickness, immune sampling, and bile-acid profiles oscillate diurnally (Gutierrez Lopez et al., *Cell Metab* 2021). Shift work, late eating, and misalignment uncouple peripheral clocks from the central pacemaker. We hypothesize this desynchronizes the secretory niche and impairs colonization of newly introduced live AKK.

### 1.3 The central hypothesis: a host clock-gated colonization window — and why it is a high-prior bet
We propose that the oscillating niche defines a **colonization window**: introduced AKK engrafts when delivered into a permissive niche state, and fails when the niche is desynchronized or depleted. The strong, falsifiable corollary is that **engraftment depends on dosing time and lifestyle alignment, not only on dose.**

This remains a hypothesis — no study has shown a time-gated engraftment window for a *therapeutic* strain — but it is well-motivated, not speculative. Two of its three logical links are already established: (i) the gut niche and epithelial-adherent microbiota oscillate diurnally (Thaiss et al., *Cell* 2016), and (ii) the host clock gates whether an *exogenous* microbe colonizes — time-of-day controls colonization resistance to *Salmonella* via rhythmic immunity (Brooks et al., *Cell* 2021). What is untested is link (iii): that this gating applies to, and can be exploited for, a beneficial introduced strain. We are extending a demonstrated principle into an open, high-value context.

**A feedback loop, and bistable responder states (the conceptual frame).** Engrafted AKK can itself repair clock-controlled goblet-cell/mucus damage (Wang et al., *Cell Host Microbe* 2023). So the host clock gates AKK *and* AKK reinforces the niche — a positive feedback. Such a loop predicts **two stable states**: successful engraftment that sustains a healthy rhythmic niche, versus failure that leaves the niche degraded. Lifestyle disruption is then the perturbation that pushes a host across the tipping point. This reframes the clinical responder/non-responder split as a **controllable bistable system** rather than fixed individual luck — and it directly motivates intervening on timing and lifestyle to flip the state.

### 1.4 Appropriate use of AI4S
Multi-omics spanning host behavior, bacterial metatranscriptomics, metabolomics, and host scRNA-seq exceeds linear methods. We use AI within its validated scope: **AlphaFold 3** to generate structural hypotheses for AKK outer-membrane-protein/host-receptor complexes (judged by model confidence, e.g., ipTM/pTM; binding energetics estimated by downstream MD/MM-GBSA — *not* by AlphaFold itself), and a **single-cell foundation model (Geneformer)** for in silico perturbation of goblet-cell regulatory networks. All predictions are treated as hypotheses and tested with genetic knockouts.

---

## 2. Objectives & Central Questions

**Objective.** Establish the causal chain *host diet/circadian state → rhythmic mucus niche → live-AKK engraftment and transcription → metabolic efficacy*, test whether it forms a bistable feedback loop, and convert it into actionable rules (dosing time and lifestyle) for durable live-AKK therapy.

**Central questions.**
1. **The window.** Do circadian misalignment and Western diet, separately and jointly, reduce live-AKK engraftment and anti-obesity/insulin-sensitizing efficacy — and does **dosing time** itself change engraftment?
2. **Mechanism.** Is gating mediated by the goblet-cell/MUC2 secretory *rhythm* (not just mean mucus), and which host axes (epithelial *Bmal1*; TLR2) are causally required?
3. **Feedback.** Does successful engraftment restore the host mucus rhythm, and does the system behave as two stable states (engrafted vs cleared) consistent with the responder/non-responder split?
4. **Control.** Can circadian-timed dosing or active-phase time-restricted feeding open the window and rescue efficacy in disrupted hosts, and can baseline host state predict engraftment?

---

## 3. Research Content & Experimental Design

A single mechanistic spine runs through three modules. The in vivo phenotype is mapped broadly; expensive deep-omics and causal-genetic work are focused on the most informative arms.

### 3.1 Module 1 — Does host lifestyle gate live-AKK engraftment and efficacy? (*in vivo*)

**Trackable strain.** To distinguish introduced from endogenous AKK, we use a marked live strain — a spontaneous rifampicin-resistant derivative of AKK MucT verified to retain growth and Amuc_1100 expression — enabling selective culture **and** strain-specific qPCR. Mice receive a short antibiotic pre-treatment to open the niche prior to a defined-course gavage (anaerobically prepared, viability QC by CFU at each dose).

**Factorial design.** A 2 × 2 × 2 design in C57BL/6J mice, **both sexes**, for 12 weeks:
- **Diet:** control (low-fat, high-fiber) vs Western (high-fat, low-fiber).
- **Circadian:** normal 12h:12h light–dark vs chronic misalignment (weekly 8-h phase advances — an automated, low-labor "chronic jet-lag" paradigm that avoids the stress confounds of mechanical sleep deprivation; mistimed light-phase feeding used as an orthogonal driver in a confirmatory subset).
- **Treatment:** vehicle (PBS) vs a defined course of live AKK.

Vehicle arms within every diet × circadian cell are essential: they separate "lifestyle worsens metabolism" from "lifestyle blocks AKK specifically." **Sample size** is set a priori by power analysis (target: detect a 30% reduction in the AKK efficacy effect on fat mass, two-sided α = 0.05, power = 0.8; ~10–12 mice/sex/group), pre-registered with predefined exclusion criteria and blinded phenotyping.

**Phenotyping.** Body composition (EchoMRI, biweekly); glucose homeostasis (OGTT/ITT with AUC, HOMA-IR at weeks 8 and 12); systemic inflammation and incretin tone (serum LPS, TNF-α, IL-6, fasting active GLP-1).

### 3.2 Module 2 — Colonization kinetics, the niche rhythm, and the feedback loop

- **Temporal kinetics.** After a standardized dose, feces are sampled at 1, 3, 6, 12, 24 h and 1, 2, 4 weeks; strain-specific absolute qPCR (plus selective CFU) yields clearance/persistence curves fit with mixed-effects nonlinear models across lifestyle arms.
- **Spatial biogeography (FISH-IF).** Distal colon fixed in Carnoy's to preserve mucus; dual FISH (validated AKK-specific probe, e.g., MUC-1437; sequence and specificity controls reported) with anti-MUC2 immunofluorescence and confocal imaging quantify AKK-to-epithelium distance and mucus thickness — testing whether disruption forces AKK into epithelial contact (symbiont→irritant shift).
- **Niche rhythm (the window).** MUC2 secretion and goblet-cell markers are sampled across the 24-h cycle to test whether loss of the secretory *rhythm*, not mean mucus alone, predicts engraftment failure — the direct test of a time-structured window.
- **Feedback / re-entrainment (test of bistability).** In disrupted hosts, we test whether successful AKK engraftment *restores* the MUC2 secretory rhythm — the return arm of the loop. Combined with the kinetics, this assesses whether outcomes cluster into two stable states (engrafted/rhythmic vs cleared/arrhythmic) rather than a continuum.

### 3.3 Module 3 — Mechanism: multi-omics, AI hypotheses, and causal validation (*in silico* + *in vivo*)

Deep-omics are run on the four highest-contrast arms (control/normal, Western/normal, control/misaligned, Western/misaligned; ± AKK).

- **Metatranscriptomics + metabolomics.** Luminal RNA (host/rRNA-depleted) profiles the *engrafted AKK transcriptome*; untargeted LC-MS/MS gives cecal metabolites (notably secondary bile acids). Multi-omics integration (e.g., mixOmics/DIABLO) tests whether disrupted niches push AKK toward mucin-foraging glycoside hydrolases or away from Amuc_1100 — the molecular "symbiont vs forager" switch.
- **Host single-cell.** scRNA-seq of colonic mucosa; a single-cell foundation model (Geneformer) performs in silico perturbation to nominate clock-controlled upstream regulators of the goblet-cell secretory program (framed as transcriptional control of the secretory/MUC2 program, not enzyme-level O-glycosylation).
- **AlphaFold 3 structural hypotheses.** Candidate AKK outer-membrane proteins (e.g., Amuc_1100, whose TLR2 signaling is established — Plovier 2017) are modeled in complex with host receptors (TLR2/TLR4); plausibility judged by AF3 confidence, energetics/mutational effects estimated by downstream MD/MM-GBSA and in silico mutagenesis, yielding falsifiable predictions for validation.
- **Causal validation (closing the loop).**
  - **Epithelial clock:** intestinal-epithelium-specific *Bmal1* knockout (*Bmal1*^fl/fl × *Villin-Cre*; lines from Jackson, crossed in-house). Test: do *Bmal1*^ΔIEC mice under normal light–dark recapitulate the engraftment failure of misaligned wild-types — establishing the epithelial clock as the upstream gate? This carries the generality claim: the gate is a *host clock gene*, not an AKK idiosyncrasy.
  - **Receptor axis:** *Tlr2*^−/− mice. Test: is TLR2 required for live-AKK metabolic rescue, confirming the predicted interface?

### 3.4 Module 4 — Chrono-dosing, lifestyle rescue, and predictive modeling (the actionable payoff)

- **Chrono-dosing (the headline test of the window).** Administer the same live-AKK course at different circadian phases in normal and disrupted hosts to map engraftment vs dosing time and identify an optimal window — a cheap, immediately translatable variable.
- **Lifestyle rescue.** In Western-diet, misaligned mice receiving live AKK, test whether **active-phase (dark-phase) time-restricted feeding** restores the mucus rhythm, AKK engraftment, and metabolic efficacy — direct evidence for "lifestyle as part of the prescription," and a test of flipping the bistable state.
- **Predictive model (biostatistics core).** Using the mouse cohort, (i) a formal **causal mediation analysis** quantifies how much of the lifestyle→metabolic-outcome effect is mediated by the MUC2 rhythm and by AKK engraftment; (ii) a parsimonious classifier (elastic-net / gradient boosting, nested cross-validation, calibrated, with appropriate small-n caveats) predicts engraftment/response from baseline features (baseline AKK, feeding-rhythm amplitude, fiber intake). Positioned as hypothesis-generating for future human translation, not a clinical tool.

---

## 4. Expected Outcomes & Innovations

### 4.1 Expected outcomes — and why the study is decisive either way
1. Vehicle-controlled evidence on whether, and how strongly, dosing time, circadian misalignment, and diet gate live-AKK engraftment and efficacy.
2. A genetically validated mechanism linking the host epithelial clock and MUC2 secretory rhythm to colonization, and a test of whether engraftment re-entrains the niche (the feedback loop).
3. Actionable rules: an optimal circadian dosing window and a tested lifestyle rescue (active-phase TRF), plus an open dataset of AKK–host interface structural models.

The design is **informative under both outcomes**, which de-risks the central hypothesis. If the window is strong, the deliverable is a chrono-dosing-plus-lifestyle prescription for durable live AKK. If it is weak, we will have shown that engraftment is robust to timing and that **diet is the dominant lever** — itself an important, publishable correction that simplifies clinical dosing. The primary risk — that AKK's self-repair capacity buffers away the timing effect — is exactly what the chrono-dosing and feedback experiments are built to measure rather than assume.

### 4.2 Key innovations
- **A colonization window for live biotherapy.** Reframes the field from "does AKK act" (answered for the dead product) to "when does a live strain establish," extending a host-clock gating principle proven for pathogens into therapeutic engraftment.
- **Chrono-dosing as a control lever.** "When you dose" as a determinant of engraftment — cheap, translatable, and untested for a beneficial strain.
- **Bistable responder states.** Recasts clinical heterogeneity as a controllable host-microbe feedback system, with a concrete way to flip it.
- **Disciplined AI4S.** AlphaFold 3 and a single-cell foundation model generate falsifiable hypotheses tested in knockouts — AI as a hypothesis engine, energetics by the correct downstream tools.
- **Behavioral co-benefit.** Because efficacy depends on lifestyle, the therapy itself rewards healthy diet and sleep — a clinically meaningful feedback.

---

## 5. Feasibility

1. **Scope and team.** Sized for 2–3 PhD students with AI assistance over ~30 months, divided as in vivo/wet-lab, sequencing/omics, and computational/biostatistics. Deep-omics and the two knockout lines are limited to the most informative arms; the human/humanized work in early drafts has been removed.
2. **Critical-path timing.** *Bmal1*^fl/fl × *Villin-Cre* breeding (~6–9 months to usable cohorts) and marked-strain validation start immediately, in parallel with Module 1, so they do not bottleneck later modules. *Tlr2*^−/− is commercially available.
3. **Platforms.** Germ-free/gnotobiotic and anaerobic culture facilities, confocal microscopy, LC-MS/MS, and single-cell library prep are operational. A departmental GPU cluster (H100/A100) supports AlphaFold 3 and foundation-model fine-tuning.
4. **Expertise.** Demonstrated proficiency in Python/R, scRNA-seq and metatranscriptomic pipelines, multi-omics integration, and statistical modeling, with preliminary cell–cell communication analyses in hand.

---

## 6. Timeline & References

### Milestones (~30 months)
- **Jun 2026 – Mar 2027:** Module 1 factorial phenotyping; Module 2 kinetics, FISH, and niche-rhythm sampling. In parallel: validate marked strain; begin *Bmal1*^ΔIEC breeding; acquire *Tlr2*^−/−.
- **Apr 2027 – Dec 2027:** Module 3 metatranscriptomics, scRNA-seq, metabolomics on focal arms; AlphaFold 3 / Geneformer pipelines; lock validation targets.
- **Jan 2028 – Jun 2028:** Causal validation in *Bmal1*^ΔIEC and *Tlr2*^−/− mice; feedback/re-entrainment experiments.
- **Apr 2028 – Dec 2028:** Module 4 chrono-dosing and rescue experiments; causal-mediation and predictive modeling; manuscript preparation.

### Selected References
1. Mount, S., Canfora, E. E., Jocken, J. W., … Blaak, E. E. (2026). Pasteurized *Akkermansia muciniphila* MucT for weight loss maintenance in people with overweight and obesity: a controlled randomized trial. *Nature Medicine*. https://doi.org/10.1038/s41591-026-04394-7
2. Aronne, L. J., et al. (2026). Orforglipron for maintenance of body weight reduction: the ATTAIN-MAINTAIN phase 3b trial. *Nature Medicine*. https://doi.org/10.1038/s41591-026-04386-7
3. Cani, P. D., & de Vos, W. M. (2017). Next-generation beneficial microbes: the case of *Akkermansia muciniphila*. *Frontiers in Microbiology*, 8, 1765.
4. Plovier, H., et al. (2017). A purified membrane protein from *Akkermansia muciniphila* or the pasteurized bacterium improves metabolism in obese and diabetic mice. *Nature Medicine*, 23(1), 107–113.
5. Everard, A., et al. (2013). Cross-talk between *Akkermansia muciniphila* and intestinal epithelium controls diet-induced obesity. *PNAS*, 110(22), 9066–9071.
6. Roopchand, D. E., et al. (2015). Dietary polyphenols promote growth of the gut bacterium *Akkermansia muciniphila* and attenuate high-fat diet-induced metabolic syndrome. *Diabetes*, 64(8), 2847–2858.
7. Desai, M. S., et al. (2016). A dietary fiber-deprived gut microbiota degrades the colonic mucus barrier and enhances pathogen susceptibility. *Cell*, 167(5), 1339–1353.
8. Dao, M. C., et al. (2016). *Akkermansia muciniphila* and improved metabolic health during a dietary intervention in obesity. *Gut*, 65(3), 426–436.
9. Thaiss, C. A., et al. (2016). Microbiota diurnal rhythmicity programs host transcriptome oscillations. *Cell*, 167(6), 1495–1510.
10. Brooks, J. F., et al. (2021). The microbiota coordinates diurnal rhythms in innate immunity with the circadian clock. *Cell*, 184(16), 4154–4167.
11. Gutierrez Lopez, D. E., Lashinger, L. M., Weinstock, G. M., & Bray, M. S. (2021). Circadian rhythms and the gut microbiome synchronize the host's metabolic response to diet. *Cell Metabolism*, 33(5), 873–895.
12. Wang, Z., et al. (2023). *Akkermansia muciniphila* ameliorates lysosomal deacidification in goblet cells to maintain the intestinal mucus barrier in sleep-deprived mice. *Cell Host & Microbe*, 31(11), 1821–1835. https://doi.org/10.1016/j.chom.2023.10.005
13. Abramson, J., Adler, J., Dunger, J., … Jumper, J. (2024). Accurate structure prediction of biomolecular interactions with AlphaFold 3. *Nature*, 630, 493–500.
</content>
