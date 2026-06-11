# Research Proposal

**Project Title:** Engineering the Host Mucus Niche for Durable Engraftment of Live *Akkermansia muciniphila*

**Major:** Biostatistics / Computational Genomics and Bioinformatics

**Research Direction:** Gut Microenvironment & Translational Medicine; AI for Science (AI4S)

---

## Abstract

*Akkermansia muciniphila* (AKK) is one of the most advanced next-generation microbiome therapeutics for obesity and insulin resistance. Recent human data show that **pasteurized** AKK can reduce weight regain after diet-induced weight loss, but pasteurized cells are non-viable and do not colonize. The unique therapeutic promise of **live** AKK is therefore different: if an introduced strain can durably engraft in the colonic mucus niche, AKK could become a short-course, self-sustaining biotherapy rather than a product requiring continuous dosing. The central unsolved problem is what host ecological state permits that engraftment.

We propose that durable live-AKK engraftment is governed by a **definable, predictable, and engineerable host mucus-niche state**. This state is likely shaped by fermentable substrate availability, resident mucin-degrading competitors, mucus structure and goblet-cell function, bile-acid and mucin-derived metabolites, inflammation, and feeding/circadian rhythm. Instead of assuming a single dominant mechanism a priori, we will use a staged discovery-to-validation design: first map permissive and resistant host states; then learn an interpretable niche-state model that predicts engraftment; finally use model-nominated interventions to convert resistant hosts into permissive hosts and test whether durable engraftment restores metabolic efficacy.

Three aims test this framework. Aim 1 performs a focused in vivo discovery screen in conventional mice using a genomically trackable live AKK strain and rigorous post-dose persistence criteria. Aim 2 integrates microbiome, mucus imaging, metabolomic, host-marker, and behavioral-rhythm data to learn the minimal AKK-permissive niche signature. AI and statistical models are used only where they add value: to identify stable predictive features, quantify uncertainty, and nominate experimentally testable niche-engineering interventions. Aim 3 causally validates the top determinants by preconditioning resistant hosts with diet, feeding-rhythm, microbiome-competition, or epithelial/goblet-cell interventions selected from the model. The expected output is not generic advice to "eat better" while taking AKK, but a mechanistic framework for who can engraft live AKK, how to open the niche before dosing, and when pasteurized AKK may be preferable to a live product.

---

## 1. Introduction and Significance

### 1.1 Why live AKK, and why engraftment is the decisive variable

*Akkermansia muciniphila* (AKK), a mucin-specialized colonic anaerobe, is inversely associated with adiposity, insulin resistance, inflammation, and barrier dysfunction; in preclinical models live AKK, pasteurized AKK, and the outer-membrane protein Amuc_1100 each improve gut barrier function and metabolic phenotypes. The current therapeutic context makes the live-versus-dead distinction decisive. GLP-1 receptor agonists produce strong weight loss but rebound on cessation and carry cost and gastrointestinal burdens, so durable maintenance after weight loss is the central unmet need (Aronne et al., *Nat Med* 2026). In May 2026, *Nature Medicine* reported that **pasteurized** AKK MucT blunted weight regain over a 24-week maintenance phase (Mount et al.; ITT n ≈ 84), with adipose remodeling toward oxidative pathways, and with baseline *Akkermansia* abundance associated specifically with **cardiometabolic** response.

Two facts from that trial define our problem. The efficacious product was **non-viable and does not colonize** — its benefit required continued dosing — and the response was **heterogeneous across hosts**. These are precisely the limitations a *live* strain could overcome. The distinct, higher-value proposition of live AKK is durability: a strain that establishes in the colonic mucus niche could convert a chronic supplement into a short, self-sustaining course, and continue delivering Amuc_1100 and mucin-derived metabolites in situ at a self-adjusting dose. That entire proposition stands or falls on the one variable the dead product never had to satisfy — **engraftment** — and engraftment is governed by the host mucus niche. Defining and engineering that niche is therefore the prerequisite for any durable live-AKK therapy, and the subject of this proposal.

### 1.2 Niche-controlled engraftment is established, but the AKK-permissive niche is unknown

External microbes do not colonize the gut simply because they are dosed at high concentration. Human probiotic studies show individualized mucosal colonization resistance: the same probiotic consortium can colonize some hosts and fail in others, and baseline host and microbiome features predict this difference. A single *Bifidobacterium longum* strain can engraft durably only in hosts whose resident microbiome leaves an appropriate niche. Fecal microbiota transplantation studies further show that donor strain engraftment depends on recipient ecological context. In engineered communities, providing an exclusive metabolic niche can enable strain engraftment.

These studies establish a general principle: **engraftment is a host-ecosystem property, not only a bacterial-dose property.** What remains unknown is the specific permissive state for AKK, a mucin specialist whose niche is physically and metabolically tied to the colonic mucus layer. Defining that state is both biologically important and clinically actionable.

### 1.3 Candidate determinants of the live-AKK niche

AKK lives at the interface between resident microbiota and host mucus. Its engraftment should therefore depend on several linked determinants:

- **Substrate and diet:** fiber and polyphenols can expand AKK and strengthen the mucus barrier, whereas fiber deprivation can push the microbiota toward host-mucin foraging and barrier erosion.
- **Resident competition:** other mucin degraders may either compete with AKK for mucin glycans or cross-feed metabolites that support AKK.
- **Mucus structure:** MUC2 layer thickness, penetrability, secretion dynamics, and goblet-cell state determine the spatial niche AKK must occupy.
- **Metabolites:** bile acids, SCFAs, mucin-derived sugars, and redox-related metabolites can alter AKK growth and host epithelial state.
- **Feeding and circadian rhythm:** gut motility, mucus secretion, bile-acid flow, immune tone, and microbiome function are time structured; circadian alignment may be one route to a permissive niche, but it should be tested alongside other determinants rather than assumed to dominate.

The key scientific opportunity is to discover which combination of these features defines a permissive host state and to test whether that state can be engineered.

### 1.4 Role of AI4S and biostatistics

The project is not a descriptive multi-omics survey. It is a prediction-to-causation study. AI/statistical modeling enters at the point where human intuition is weakest: integrating heterogeneous baseline features into a parsimonious niche-state model that predicts engraftment and nominates interventions.

We will prioritize interpretable and uncertainty-aware models over unnecessary complexity: sparse generalized models, Bayesian hierarchical models, multi-omics latent-factor models, and carefully validated nonlinear learners when justified. Model outputs must satisfy two criteria: they must predict held-out engraftment outcomes, and they must nominate experimentally testable niche-engineering strategies. Structural AI tools such as AlphaFold 3 or single-cell foundation models will be used only as optional hypothesis generators if the discovery data identify a specific AKK-host interface or epithelial pathway requiring mechanistic follow-up.

---

## 2. Objective and Central Questions

**Objective:** Define the host mucus-niche state that permits durable live-AKK engraftment, build a predictive model of that state, and causally engineer resistant hosts into permissive hosts to restore metabolic efficacy.

**Central questions:**

1. Which host states permit or resist durable live-AKK engraftment after dosing stops?
2. Can baseline mucus, microbiome, metabolite, inflammatory, and rhythm features predict engraftment?
3. Which predictors are causal niche determinants rather than passive biomarkers?
4. Can diet, feeding rhythm, microbiome competition, or epithelial/goblet-cell interventions convert non-engrafters into engrafters?
5. Does durable engraftment add metabolic benefit beyond transient exposure to live or pasteurized AKK?

---

## 3. Research Content and Experimental Design

The design is staged to avoid an underpowered all-omics screen. Aim 1 maps engraftment outcomes across a limited set of high-information host states. Aim 2 learns the niche signature from baseline and early-response data. Aim 3 validates only the strongest model-nominated determinants.

### 3.1 Aim 1 - Map host niche states that permit or resist live-AKK engraftment

**Rationale.** A causal engraftment claim requires a rigorous definition of persistence. Fecal detection immediately after gavage is not enough; it may reflect transit. We define durable engraftment as post-dose persistence of the introduced strain after dosing cessation, supported by strain-specific absolute quantification, viable recovery when possible, and mucus-associated localization.

**Trackable live strain.** We will use AKK MucT carrying a stable, genomically verifiable strain marker. The marker strategy will be selected to minimize fitness artifacts and must pass four validation steps before animal experiments: whole-genome sequencing, anaerobic growth on mucin, Amuc_1100 expression, and in vivo competition against unmarked parental AKK. If an antibiotic-resistance marker is used, it will be treated as a tool requiring fitness validation, not as an assumption of equivalence.

**Primary engraftment endpoint.** Mice receive a defined live-AKK course prepared anaerobically with CFU quality control at each dose. After dosing stops, fecal samples are collected at days 1, 3, 7, 14, and 28. Engraftment is pre-specified as introduced-strain abundance above limit of quantification at late post-dose time points, with viable selective recovery when possible and distal-colon mucus association by FISH-IF at endpoint. Secondary outcomes include engraftment half-life, area under the persistence curve, and mucosal AKK burden.

**Staged discovery screen.** Conventional C57BL/6J mice, both sexes, will be randomized by cage and balanced for baseline AKK. The screen compares a limited set of host states:

1. control diet with normal light-dark and ad libitum feeding;
2. Western low-fiber/high-fat diet;
3. Western diet plus fermentable fiber or polyphenol preconditioning;
4. feeding/circadian disruption using mistimed light-phase feeding or chronic jet-lag;
5. active-phase time-restricted feeding rescue in the disrupted or Western-diet context;
6. optional antibiotic-open niche as a comparator for ecological opening, not as the primary disease model.

The first pass is powered for engraftment differences, not every metabolic endpoint. As a practical starting point, discovery arms will use approximately 8 mice per sex per condition, followed by focused validation at approximately 10-12 mice per sex per selected intervention arm after effect-size estimation. Vehicle controls are included in the principal diet/rhythm states to distinguish AKK-specific metabolic effects from the direct effects of diet and feeding schedule. Randomization, cage balancing, blinded image analysis, and a pre-specified exclusion/analysis plan will be used throughout. Expensive terminal assays are reserved for animals representing clear engrafters and non-engrafters.

**Core phenotyping.**

- AKK persistence: strain-specific absolute qPCR, selective culture, and fecal total AKK.
- Spatial niche: Carnoy fixation, AKK FISH, MUC2 immunofluorescence, mucus thickness, and AKK-epithelium distance.
- Host state: goblet-cell markers, MUC2 abundance, barrier markers, fecal lipocalin-2, serum LPS-binding protein, TNF-alpha, IL-6.
- Microbiome context: baseline and post-dose 16S or shallow shotgun profiling, with targeted quantification of resident mucin degraders.
- Behavior/rhythm: feeding timing, locomotor activity, body weight, and cage-level intake.
- Metabolic response: EchoMRI, fasting insulin/glucose, OGTT or ITT, and active GLP-1 in selected arms.

**Decision point.** Aim 1 will classify animals and conditions into permissive, intermediate, and resistant niche states. Only the highest-contrast states move into deep profiling for Aim 2.

### 3.2 Aim 2 - Learn a predictive and mechanistic model of the AKK-permissive mucus niche

**Rationale.** If engraftment is niche-gated, baseline host features should predict the probability and durability of AKK persistence. The model is not intended as a clinical diagnostic at this stage. Its purpose is to discover a minimal, testable niche signature and nominate causal interventions.

**Data layers.** Deep profiling will be focused on high-contrast engrafters and non-engrafters identified in Aim 1:

- baseline microbiome and mucin-degrader composition;
- AKK early kinetics during the first 72 hours after dosing;
- mucus imaging features, including thickness, penetrability proxy, AKK localization, and goblet-cell density;
- targeted host expression of goblet-cell, epithelial-clock, innate-immune, and barrier genes, with scRNA-seq only for the strongest mechanistic contrast;
- metabolomics emphasizing bile acids, SCFAs, mucin-derived sugars, amino acids, and inflammatory lipid mediators;
- feeding/activity rhythm metrics and diet intake;
- metabolic and inflammatory host outcomes.

**Modeling plan.** Outcomes are pre-defined: binary engraftment, persistence half-life, mucosal AKK burden, and metabolic response conditional on engraftment. We will use:

- sparse logistic or survival models for interpretable baseline predictors;
- Bayesian hierarchical models to account for sex, cage, batch, and perturbation arm;
- multi-omics latent-factor models to identify shared niche axes;
- gradient boosting or random forests only after nested cross-validation and calibration checks;
- causal mediation and graphical modeling to separate plausible mediators from non-causal correlates.

Feature stability will be assessed by bootstrap resampling and held-out perturbation arms. Models that cannot predict out-of-sample engraftment or nominate feasible interventions will not be overinterpreted.

**Expected model output.** The final output is a compact AKK-permissive niche signature. Possible components include preserved MUC2 structure, an active goblet-cell secretory program, low competing mucin-degrader pressure, favorable bile-acid or mucin-metabolite profiles, adequate fermentable substrate, and aligned feeding rhythm. The exact combination must be learned from the data. This signature will generate the intervention choices for Aim 3.

### 3.3 Aim 3 - Engineer resistant hosts into permissive hosts and test causal sufficiency

**Rationale.** Prediction is not enough. To establish a mechanism and generate clinical guidance, the project must show that manipulating the nominated niche determinant converts resistant hosts into engrafters and improves outcomes.

**Intervention selection.** Aim 3 is intentionally conditional on Aim 2 results:

- If substrate and mucus support dominate, test fiber or polyphenol preconditioning before live-AKK dosing.
- If feeding/circadian rhythm dominates, test active-phase time-restricted feeding and chrono-dosing at defined Zeitgeber times.
- If resident mucin-degrader competition dominates, test targeted defined-community or competition experiments in a simplified microbiota system.
- If epithelial or goblet-cell state dominates, test causal host pathways using inducible intestinal-epithelial genetics or pharmacologic/ dietary mucus-support interventions.
- If Amuc_1100/TLR2 signaling predicts metabolic response but not engraftment, test TLR2 as an efficacy mediator rather than forcing it into the colonization mechanism.

**Validation design.** For each selected intervention, resistant hosts are randomized to vehicle, live AKK alone, niche intervention alone, or niche intervention plus live AKK. The key test is interaction: does preconditioning specifically increase durable live-AKK engraftment and does that engraftment associate with improved metabolic outcomes? Where feasible, pasteurized AKK is included as a comparator to separate benefits of transient AKK exposure from benefits requiring live persistence.

**Causal criteria.** A determinant will be considered causal only if manipulation changes the niche feature, increases durable introduced-strain persistence, and improves at least one host-relevant outcome relative to appropriate controls. This prevents the model from mistaking a correlated marker for a true engineering target.

---

## 4. Expected Outcomes and Innovation

### 4.1 Expected outcomes

1. A rigorous map of host states that permit, partially permit, or resist live-AKK engraftment.
2. A validated, interpretable niche-state model predicting live-AKK persistence from baseline host features.
3. Experimental proof that at least one model-nominated intervention can convert resistant hosts into more permissive hosts.
4. A practical framework for live-AKK use: when to attempt live engraftment, how to precondition the niche, whether timing matters, and when pasteurized AKK may be the more rational product.

### 4.2 Innovation

- **From dose to niche:** The project reframes live-AKK therapy around host niche permissiveness, not simply strain selection or dose.
- **Durability as the therapeutic endpoint:** It directly tests the property that distinguishes live AKK from pasteurized AKK.
- **AI as experimental steering:** Modeling is used to select causal validation experiments, not merely to decorate multi-omics data.
- **Actionable ecology:** The work aims to engineer the host mucus niche using feasible interventions such as diet, feeding rhythm, or microbiome competition.
- **Generalizable principle:** AKK is the model mucin specialist, but the framework applies to other live biotherapeutics whose success depends on host ecological occupancy.

---

## 5. Rigor, Risks, and Alternatives

**Engraftment versus transit.** The study uses post-dose persistence, viable recovery, and mucus-associated localization to avoid mistaking gavage transit for colonization.

**Marker artifacts.** The marked strain must pass WGS, growth, expression, and in vivo fitness checks. If the marker changes fitness, strain tracking will shift to naturally occurring strain-specific SNVs or barcode strategies with validated neutrality.

**Cage and microbiome effects.** Mice will be randomized by cage, cage will be modeled statistically, and key findings will be replicated across independent cohorts.

**Diet confounding.** Western diet changes fat, fiber, caloric density, and feeding behavior. The rescue arms are designed to separate substrate/mucus support from obesity alone. Food intake and feeding rhythm will be measured rather than assumed.

**Antibiotic confounding.** Antibiotics will not be the primary discovery model because they disrupt mucus, immunity, and colonization resistance. They may be used only as a comparator for ecological opening.

**Circadian interpretation.** Rhythm effects will be interpreted only when supported by feeding/activity data and, where needed, epithelial clock or time-of-dosing validation. A timing effect alone will not be called a host-clock mechanism.

**Model overfitting.** The model will use pre-defined outcomes, nested cross-validation, calibration, feature stability analysis, and held-out perturbation arms. Complex models must outperform interpretable baselines to be retained.

---

## 6. Feasibility

The project is designed for 2-3 PhD students over approximately 30 months. The scope is controlled by staging: Aim 1 is a focused discovery screen; Aim 2 deep-profiles only high-contrast states; Aim 3 validates only the strongest model-nominated determinants. This avoids running a full factorial design across every diet, rhythm, microbiome, omics, and genetic condition.

Required platforms are standard for a microbiome-focused biomedical environment: anaerobic AKK culture, mouse metabolic phenotyping, fecal strain quantification, confocal imaging, sequencing, LC-MS/MS metabolomics, and R/Python-based statistical modeling. Conditional mouse genetics or gnotobiotic work are reserved for targeted validation if the discovery screen justifies them.

---

## 7. Timeline and Milestones

- **Jun 2026 - Dec 2026:** Validate trackable live AKK strain; finalize engraftment assay; run pilot dosing and post-dose persistence study.
- **Jan 2027 - Sep 2027:** Complete Aim 1 staged discovery screen across diet, rescue, and rhythm-related host states; classify permissive and resistant conditions.
- **Oct 2027 - Mar 2028:** Deep-profile high-contrast engrafters and non-engrafters; build and lock the predictive niche-state model.
- **Apr 2028 - Sep 2028:** Run Aim 3 niche-engineering validation based on model-nominated determinants.
- **Oct 2028 - Dec 2028:** Integrate causal, metabolic, and predictive results; prepare manuscript and translational guidance framework.

---

## 8. Selected References

1. Mount, S., Canfora, E. E., Jocken, J. W., et al. (2026). Pasteurized *Akkermansia muciniphila* MucT for weight loss maintenance in people with overweight and obesity: a controlled randomized trial. *Nature Medicine*. https://doi.org/10.1038/s41591-026-04394-7
2. Aronne, L. J., et al. (2026). Orforglipron for maintenance of body weight reduction: the double-blind, randomized phase 3b ATTAIN-MAINTAIN trial. *Nature Medicine*. https://doi.org/10.1038/s41591-026-04386-7
3. Cani, P. D., & de Vos, W. M. (2017). Next-generation beneficial microbes: the case of *Akkermansia muciniphila*. *Frontiers in Microbiology*, 8, 1765. https://doi.org/10.3389/fmicb.2017.01765
4. Plovier, H., Everard, A., Druart, C., et al. (2017). A purified membrane protein from *Akkermansia muciniphila* or the pasteurized bacterium improves metabolism in obese and diabetic mice. *Nature Medicine*, 23, 107-113. https://doi.org/10.1038/nm.4236
5. Everard, A., Belzer, C., Geurts, L., et al. (2013). Cross-talk between *Akkermansia muciniphila* and intestinal epithelium controls diet-induced obesity. *PNAS*, 110, 9066-9071. https://doi.org/10.1073/pnas.1219451110
6. Depommier, C., Everard, A., Druart, C., et al. (2019). Supplementation with *Akkermansia muciniphila* in overweight and obese human volunteers: a proof-of-concept exploratory study. *Nature Medicine*, 25, 1096-1103. https://doi.org/10.1038/s41591-019-0495-2
7. Dao, M. C., Everard, A., Aron-Wisnewsky, J., et al. (2016). *Akkermansia muciniphila* and improved metabolic health during a dietary intervention in obesity. *Gut*, 65, 426-436. https://doi.org/10.1136/gutjnl-2014-308778
8. Roopchand, D. E., Carmody, R. N., Kuhn, P., et al. (2015). Dietary polyphenols promote growth of the gut bacterium *Akkermansia muciniphila* and attenuate high-fat diet-induced metabolic syndrome. *Diabetes*, 64, 2847-2858. https://doi.org/10.2337/db14-1916
9. Desai, M. S., Seekatz, A. M., Koropatkin, N. M., et al. (2016). A dietary fiber-deprived gut microbiota degrades the colonic mucus barrier and enhances pathogen susceptibility. *Cell*, 167, 1339-1353.e21. https://doi.org/10.1016/j.cell.2016.10.043
10. Maldonado-Gomez, M. X., Martinez, I., Bottacini, F., et al. (2016). Stable engraftment of *Bifidobacterium longum* AH1206 in the human gut depends on individualized features of the resident microbiome. *Cell Host & Microbe*, 20, 515-526. https://doi.org/10.1016/j.chom.2016.09.001
11. Zmora, N., Zilberman-Schapira, G., Suez, J., et al. (2018). Personalized gut mucosal colonization resistance to empiric probiotics is associated with unique host and microbiome features. *Cell*, 174, 1388-1405.e21. https://doi.org/10.1016/j.cell.2018.08.041
12. Suez, J., Zmora, N., Zilberman-Schapira, G., et al. (2018). Post-antibiotic gut mucosal microbiome reconstitution is impaired by probiotics and improved by autologous FMT. *Cell*, 174, 1406-1423.e16. https://doi.org/10.1016/j.cell.2018.08.047
13. Shepherd, E. S., DeLoache, W. C., Pruss, K. M., Whitaker, W. R., & Sonnenburg, J. L. (2018). An exclusive metabolic niche enables strain engraftment in the gut microbiota. *Nature*, 557, 434-438. https://doi.org/10.1038/s41586-018-0092-4
14. Li, S. S., Zhu, A., Benes, V., et al. (2016). Durable coexistence of donor and recipient strains after fecal microbiota transplantation. *Science*, 352, 586-589. https://doi.org/10.1126/science.aad8852
15. Thaiss, C. A., Levy, M., Korem, T., et al. (2016). Microbiota diurnal rhythmicity programs host transcriptome oscillations. *Cell*, 167, 1495-1510.e12. https://doi.org/10.1016/j.cell.2016.11.003
16. Gutierrez Lopez, D. E., Lashinger, L. M., Weinstock, G. M., & Bray, M. S. (2021). Circadian rhythms and the gut microbiome synchronize the host's metabolic response to diet. *Cell Metabolism*, 33, 873-895. https://doi.org/10.1016/j.cmet.2021.03.015
17. Wang, Z., et al. (2023). *Akkermansia muciniphila* ameliorates lysosomal deacidification in goblet cells to maintain the intestinal mucus barrier in sleep-deprived mice. *Cell Host & Microbe*, 31, 1821-1835. https://doi.org/10.1016/j.chom.2023.10.005
18. Abramson, J., Adler, J., Dunger, J., et al. (2024). Accurate structure prediction of biomolecular interactions with AlphaFold 3. *Nature*, 630, 493-500. https://doi.org/10.1038/s41586-024-07487-w
