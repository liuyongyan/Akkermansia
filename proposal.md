# Research Proposal

**Project Title:** Host Diet and Circadian Rhythm Gate the Engraftment and Metabolic Efficacy of Live *Akkermansia muciniphila*: A Mechanistic and AI-Assisted Framework for Durable, Lifestyle-Optimized Live Biotherapy
**Major:** Biostatistics / Computational Genomics and Bioinformatics
**Research Direction:** Gut Microenvironment & Translational Medicine; AI for Science (AI4S)

---

## Abstract

Live *Akkermansia muciniphila* (AKK) is a leading next-generation probiotic for obesity and insulin resistance. Its central therapeutic promise over the pasteurized (non-viable) product is **durability**: a live strain that engrafts in the colonic mucus niche could provide a lasting benefit from a short course, rather than requiring indefinite daily supplementation. A 2026 *Nature Medicine* trial (Mount et al.) established clinical efficacy for *pasteurized* AKK in weight-maintenance but, by design, that product does not colonize, and it reported large inter-individual heterogeneity tied to baseline Akkermansia abundance. The decisive open question for *live* biotherapy is therefore not whether AKK can act, but **what determines whether an introduced live strain establishes, persists, and remains metabolically active in a given host.**

We test the hypothesis that two modifiable host behaviors — **diet composition and circadian alignment** — gate live-AKK engraftment by controlling its mucus niche. The diet axis is well supported: dietary fiber and polyphenols promote AKK, whereas Western high-fat/low-fiber diets shift the community toward mucus depletion (Desai 2016; Roopchand 2015; Everard 2013). The circadian axis is the novel claim: because goblet-cell mucin secretion is under peripheral-clock control, we propose that circadian misalignment desynchronizes the niche and impairs colonization of freshly introduced live AKK. Across three experimental modules we (1) quantify, in a factorial mouse design with vehicle controls, how diet and circadian misalignment modulate engraftment and metabolic efficacy of a genetically trackable live AKK strain; (2) resolve the spatiotemporal colonization kinetics and the goblet-cell/mucus mechanism using time-resolved strain-specific qPCR, FISH, metatranscriptomics, scRNA-seq, and metabolomics, with AI used appropriately — AlphaFold 3 for AKK–host interface structural hypotheses and a single-cell foundation model for clock-controlled regulators — followed by causal validation in intestinal-epithelial *Bmal1* and *Tlr2* knockouts; and (3) deliver the actionable payoff: whether active-phase time-restricted feeding or circadian-timed dosing **rescues** efficacy in disrupted hosts, plus a parsimonious statistical model that predicts engraftment from baseline host features. Because efficacy is shown to depend on lifestyle, the work also reframes diet and sleep as part of the prescription itself — giving patients a concrete, mechanistic reason to sustain healthy habits.

---

## 1. Introduction & Significance

### 1.1 Why live AKK, and why durability is the right target
GLP-1 receptor agonists (e.g., semaglutide, orforglipron) produce strong weight loss but rebound on cessation and carry cost and gastrointestinal burdens (Aronne et al., *Nat Med* 2026). *A. muciniphila*, a mucosal anaerobe, is inversely associated with adiposity, inflammation, and insulin resistance, and improves these in preclinical and early clinical work. In May 2026, *Nature Medicine* reported that **pasteurized** AKK (MucT) blunted weight regain during a 24-week maintenance phase after diet-induced weight loss (Mount et al.; ITT n ≈ 84), with adipose transcriptional remodeling toward mitochondrial/oxidative pathways.

Two facts from that trial define our problem. First, the efficacious product was **non-viable and does not colonize** — efficacy came from a sustained pharmacological signal requiring continued dosing. Second, response was **heterogeneous and associated with baseline Akkermansia abundance**. The distinct, higher-value proposition of a *live* biotherapeutic is durability: a strain that establishes in the mucus niche could convert a chronic supplement into a short, self-sustaining course. That proposition stands or falls on a single variable the dead product never had to satisfy — **engraftment** — and engraftment is governed by the host niche. Understanding and controlling that niche is the prerequisite for any durable live-AKK therapy, and it is what this project addresses.

### 1.2 The mucus niche is controlled by diet and by the circadian clock
The colonic mucus layer (principally MUC2 from goblet cells) is AKK's ecological niche and carbon source. Two host inputs shape it:

- **Diet (established).** Fiber and polyphenols expand AKK and reinforce the mucus barrier; fiber deprivation drives the microbiota to forage host mucin and thins the barrier; Western high-fat/low-fiber diets reduce AKK (Desai 2016; Roopchand 2015; Everard 2013; Dao 2016). Diet is thus a validated lever on the niche and serves as our anchor axis.
- **Circadian rhythm (hypothesis).** The intestinal epithelium is under peripheral-clock control (*Bmal1, Clock, Per*), and mucus thickness, immune sampling, and bile-acid profiles oscillate diurnally (Gutierrez Lopez et al., *Cell Metab* 2021). Shift work, late eating, and circadian misalignment uncouple peripheral clocks from the central pacemaker. We hypothesize that this desynchronizes the secretory niche and impairs colonization of newly introduced live AKK.

A tension we address directly: AKK itself can *repair* sleep-deprivation-induced goblet-cell/mucus damage (Wang et al., *Cell Host Microbe* 2023). Whether chronic misalignment nonetheless prevents an introduced strain from establishing in the first place — engraftment versus repair — is precisely the unresolved, non-trivial question, and the contrast motivates the design below.

### 1.3 Appropriate use of AI4S
Multi-omics spanning host behavior, bacterial metatranscriptomics, metabolomics, and host scRNA-seq exceeds linear-correlation methods. We use AI where it is genuinely informative and within its validated capability: **AlphaFold 3** to generate structural hypotheses for AKK outer-membrane-protein/host-receptor complexes (using model confidence, e.g., ipTM/pTM, with binding energetics estimated by downstream MD/MM-GBSA — *not* by AlphaFold itself), and a **single-cell foundation model (Geneformer)** for in silico perturbation of goblet-cell regulatory networks. All computational predictions are treated as hypotheses and tested with genetic knockouts.

---

## 2. Objectives & Central Questions

**Objective.** Establish the causal chain *host diet/circadian state → mucus niche → live-AKK engraftment and transcription → metabolic efficacy*, and convert it into actionable rules (lifestyle and dosing) for durable live-AKK therapy.

**Central questions.**
1. **Phenotype.** Do Western diet and circadian misalignment, separately and jointly, reduce the engraftment and the anti-obesity/insulin-sensitizing efficacy of a single course of live AKK?
2. **Niche & kinetics.** How do diet and clock disruption alter the spatiotemporal colonization kinetics and biogeography of introduced live AKK, and is this mediated by the goblet-cell/MUC2 secretory rhythm?
3. **Mechanism.** What transcriptional and metabolic state does the host niche impose on engrafted AKK, and which host receptor/clock axes (e.g., TLR2; epithelial *Bmal1*) are causally required?
4. **Rescue & prediction.** Can active-phase time-restricted feeding or circadian-timed dosing rescue efficacy in disrupted hosts, and can baseline host features predict engraftment?

---

## 3. Research Content & Experimental Design

A single mechanistic spine runs through three modules. The in vivo phenotype is mapped broadly; expensive deep-omics and causal-genetic work are focused on the most informative arms.

### 3.1 Module 1 — Does host lifestyle gate live-AKK engraftment and efficacy? (*in vivo*)

**Trackable strain.** To distinguish introduced from endogenous AKK, we use a marked live strain — a spontaneous rifampicin-resistant derivative of AKK MucT verified to retain growth and Amuc_1100 expression — enabling selective culture **and** strain-specific qPCR. Mice receive a short antibiotic pre-treatment to open the niche prior to a defined-course gavage (anaerobically prepared, viability QC by CFU at each dose).

**Factorial design.** A 2 × 2 × 2 design in C57BL/6J mice, **both sexes**, for 12 weeks:
- **Diet:** control (low-fat, high-fiber) vs Western (high-fat, low-fiber).
- **Circadian:** normal 12h:12h light–dark vs chronic misalignment (weekly 8-h phase advances — an automated, low-labor "chronic jet-lag" paradigm that avoids the stress confounds of mechanical sleep deprivation; mistimed light-phase feeding used as an orthogonal misalignment driver in a confirmatory subset).
- **Treatment:** vehicle (PBS) vs a defined course of live AKK.

Vehicle arms within every diet × circadian cell are essential: they separate "lifestyle worsens metabolism" from "lifestyle blocks AKK specifically." **Sample size** is set a priori by power analysis (target: detect a 30% reduction in the AKK efficacy effect on fat mass, two-sided α = 0.05, power = 0.8; ~10–12 mice/sex/group), pre-registered with predefined exclusion criteria and blinded phenotyping.

**Phenotyping.** Body composition (EchoMRI, biweekly); glucose homeostasis (OGTT/ITT with AUC, HOMA-IR at weeks 8 and 12); systemic inflammation and incretin tone (serum LPS, TNF-α, IL-6, fasting active GLP-1).

### 3.2 Module 2 — Colonization kinetics, biogeography, and the niche mechanism

- **Temporal kinetics.** After a standardized dose, feces are sampled at 1, 3, 6, 12, 24 h and 1, 2, 4 weeks; strain-specific absolute qPCR (plus selective CFU) yields clearance/persistence curves fit with mixed-effects nonlinear models across lifestyle arms. Dosing is performed at fixed circadian times to keep timing controlled (and varied deliberately in Module 3's chrono-dosing test).
- **Spatial biogeography (FISH-IF).** Distal colon fixed in Carnoy's to preserve mucus; dual FISH (validated AKK-specific probe, e.g., MUC-1437; sequence and specificity controls reported) with anti-MUC2 immunofluorescence and confocal imaging to quantify AKK-to-epithelium distance and mucus thickness — testing whether disruption forces AKK into epithelial contact (symbiont→irritant shift).
- **Niche rhythm.** MUC2 secretion and goblet-cell markers are sampled across the 24-h cycle to test whether loss of the secretory rhythm, not mean mucus level alone, predicts engraftment failure.

### 3.3 Module 3 — Mechanism: multi-omics, AI hypotheses, and causal validation (*in silico* + *in vivo*)

Deep-omics are run on the four highest-contrast arms (control/normal, Western/normal, control/misaligned, Western/misaligned; ± AKK).

- **Metatranscriptomics + metabolomics.** Luminal RNA (host/rRNA-depleted) profiles the *engrafted AKK transcriptome*; untargeted LC-MS/MS gives cecal metabolites (notably secondary bile acids). Multi-omics integration (e.g., mixOmics/DIABLO) tests whether disrupted niches push AKK toward mucin-foraging glycoside hydrolases or away from Amuc_1100.
- **Host single-cell.** scRNA-seq of colonic mucosa; a single-cell foundation model (Geneformer) performs in silico perturbation to nominate clock-controlled upstream regulators of the goblet-cell secretory program. We frame the target as transcriptional control of the secretory/MUC2 program — not post-transcriptional O-glycosylation, which is enzyme-level and validated separately.
- **AlphaFold 3 structural hypotheses.** Candidate AKK outer-membrane proteins (e.g., Amuc_1100, whose TLR2 signaling is established — Plovier 2017) are modeled in complex with host receptors (TLR2/TLR4); complex plausibility is judged by AF3 confidence, and binding energetics/mutational effects are estimated by downstream MD/MM-GBSA and in silico mutagenesis. Outputs are explicit, falsifiable predictions for the validation step.
- **Causal validation (the closed loop).**
  - **Epithelial clock:** intestinal-epithelium-specific *Bmal1* knockout (*Bmal1*^fl/fl × *Villin-Cre*; lines available from Jackson, crossed in-house). Test: do *Bmal1*^ΔIEC mice under normal light–dark recapitulate the engraftment/efficacy failure seen in misaligned wild-types — establishing the epithelial clock as the upstream gate?
  - **Receptor axis:** *Tlr2*^−/− mice. Test: is TLR2 required for live-AKK metabolic rescue, confirming the predicted interface?

### 3.4 Module 4 — Rescue, chrono-dosing, and predictive modeling (the actionable payoff)

- **Lifestyle rescue.** In Western-diet, misaligned mice receiving live AKK, test whether **active-phase (dark-phase) time-restricted feeding** restores the mucus rhythm, AKK engraftment, and metabolic efficacy — the direct evidence for "lifestyle as part of the prescription."
- **Chrono-dosing.** Administer the same live-AKK course at different circadian phases to identify an optimal dosing window for engraftment — a cheap, immediately translatable variable.
- **Predictive model (biostatistics core).** Using the mouse cohort, (i) a formal **causal mediation analysis** quantifies how much of the lifestyle→metabolic-outcome effect is mediated by the MUC2 rhythm and by AKK engraftment; (ii) a parsimonious classifier (elastic-net / gradient boosting with nested cross-validation, calibrated and reported with appropriate small-n caveats) predicts engraftment/response from baseline features (baseline AKK, feeding-rhythm amplitude, fiber intake). This is positioned as hypothesis-generating for future human translation, not as a clinical tool.

---

## 4. Expected Outcomes & Innovations

### 4.1 Expected outcomes
1. Quantitative evidence on whether — and how strongly — diet and circadian misalignment gate live-AKK engraftment and efficacy, with vehicle-controlled attribution.
2. A causal mechanism linking the host epithelial clock and MUC2 secretory rhythm to colonization, validated genetically.
3. Actionable rules: a tested lifestyle rescue (active-phase TRF) and an optimal circadian dosing window, plus an open dataset of AKK–host interface structural models.

### 4.2 Key innovations
- **Engraftment as the decisive variable for live biotherapy.** Reframes the field from "does AKK act" (answered for the dead product) to "does a live strain establish," the only path to durable, low-burden therapy.
- **Circadian gating as a modifiable lever.** Establishes peripheral-clock control of an *introduced* strain's colonization, and shows it can be corrected by feeding timing and dosing timing.
- **Disciplined AI4S.** AlphaFold 3 and a single-cell foundation model generate falsifiable structural and regulatory hypotheses that are then tested in knockouts — AI as a hypothesis engine, with energetics computed by the correct downstream tools.
- **Behavioral co-benefit.** Because efficacy depends on lifestyle, the therapy itself motivates and rewards healthy diet and sleep — a clinically meaningful feedback loop.

---

## 5. Feasibility

1. **Scope and team.** The plan is sized for 2–3 PhD students with AI assistance over ~30 months, divided as in vivo/wet-lab, sequencing/omics, and computational/biostatistics. Deep-omics and the two knockout lines are deliberately limited to the most informative arms to keep workload realistic; the human/humanized work present in early drafts has been removed.
2. **Critical-path timing.** *Bmal1*^fl/fl × *Villin-Cre* breeding (~6–9 months to usable cohorts) and the marked-strain validation are started immediately, in parallel with Module 1, so they do not bottleneck later modules. *Tlr2*^−/− is commercially available.
3. **Platforms.** Germ-free/gnotobiotic and anaerobic culture facilities, confocal microscopy, LC-MS/MS, and single-cell library prep are operational. A departmental GPU cluster (H100/A100) supports AlphaFold 3 and foundation-model fine-tuning.
4. **Expertise.** The team has demonstrated proficiency in Python/R, scRNA-seq and metatranscriptomic pipelines, multi-omics integration, and statistical modeling, with preliminary cell–cell communication analyses in hand.

---

## 6. Timeline & References

### Milestones (~30 months)
- **Jun 2026 – Mar 2027:** Module 1 factorial phenotyping; Module 2 kinetics and FISH. In parallel: validate marked strain; begin *Bmal1*^ΔIEC breeding; acquire *Tlr2*^−/−.
- **Apr 2027 – Dec 2027:** Module 3 metatranscriptomics, scRNA-seq, metabolomics on focal arms; AlphaFold 3 / Geneformer pipelines; lock validation targets.
- **Jan 2028 – Jun 2028:** Causal validation in *Bmal1*^ΔIEC and *Tlr2*^−/− mice.
- **Apr 2028 – Dec 2028:** Module 4 rescue and chrono-dosing experiments; causal-mediation and predictive modeling; manuscript preparation.

### Selected References
1. Mount, S., Canfora, E. E., Jocken, J. W., … Blaak, E. E. (2026). Pasteurized *Akkermansia muciniphila* MucT for weight loss maintenance in people with overweight and obesity: a controlled randomized trial. *Nature Medicine*. https://doi.org/10.1038/s41591-026-04394-7
2. Aronne, L. J., et al. (2026). Orforglipron for maintenance of body weight reduction: the ATTAIN-MAINTAIN phase 3b trial. *Nature Medicine*. https://doi.org/10.1038/s41591-026-04386-7
3. Cani, P. D., & de Vos, W. M. (2017). Next-generation beneficial microbes: the case of *Akkermansia muciniphila*. *Frontiers in Microbiology*, 8, 1765.
4. Plovier, H., et al. (2017). A purified membrane protein from *Akkermansia muciniphila* or the pasteurized bacterium improves metabolism in obese and diabetic mice. *Nature Medicine*, 23(1), 107–113.
5. Everard, A., et al. (2013). Cross-talk between *Akkermansia muciniphila* and intestinal epithelium controls diet-induced obesity. *PNAS*, 110(22), 9066–9071.
6. Roopchand, D. E., et al. (2015). Dietary polyphenols promote growth of the gut bacterium *Akkermansia muciniphila* and attenuate high-fat diet-induced metabolic syndrome. *Diabetes*, 64(8), 2847–2858.
7. Desai, M. S., et al. (2016). A dietary fiber-deprived gut microbiota degrades the colonic mucus barrier and enhances pathogen susceptibility. *Cell*, 167(5), 1339–1353.
8. Dao, M. C., et al. (2016). *Akkermansia muciniphila* and improved metabolic health during a dietary intervention in obesity. *Gut*, 65(3), 426–436.
9. Gutierrez Lopez, D. E., Lashinger, L. M., Weinstock, G. M., & Bray, M. S. (2021). Circadian rhythms and the gut microbiome synchronize the host's metabolic response to diet. *Cell Metabolism*, 33(5), 873–895.
10. Wang, Z., et al. (2023). *Akkermansia muciniphila* ameliorates lysosomal deacidification in goblet cells to maintain the intestinal mucus barrier in sleep-deprived mice. *Cell Host & Microbe*, 31(11), 1821–1835. https://doi.org/10.1016/j.chom.2023.10.005
11. Abramson, J., Adler, J., Dunger, J., … Jumper, J. (2024). Accurate structure prediction of biomolecular interactions with AlphaFold 3. *Nature*, 630, 493–500.
</content>
</invoke>
