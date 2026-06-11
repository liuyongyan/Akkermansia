# Revised Proposal Outline

## Working Title

**Engineering the Host Mucus Niche for Durable Engraftment of Live *Akkermansia muciniphila***

Alternative:

**A Predictable Host Mucus-Niche State Gates Durable Engraftment of Live *Akkermansia muciniphila***

## Central Thesis

Live *Akkermansia muciniphila* has a distinct therapeutic promise from pasteurized AKK: durable engraftment in the colonic mucus niche. The key unknown is not whether AKK can affect host metabolism, but what host ecological state permits an introduced live strain to persist.

**Central hypothesis:** Durable live-AKK engraftment is governed by a definable, predictable, and engineerable host mucus-niche state. Diet, resident mucin degraders, mucus structure, metabolites, and feeding/circadian rhythm are candidate determinants of this state. AI/statistical models will be used to learn the minimal niche signature that predicts engraftment and to nominate interventions that convert resistant hosts into permissive hosts.

## Specific Aims

### Aim 1. Map host niche states that permit or resist live-AKK engraftment

**Question:** Which diet, microbiome, mucus, metabolic, and rhythm states determine whether introduced live AKK persists after dosing stops?

**Core design:**

- Use a genetically or genomically trackable live AKK strain, validated for preserved growth, mucin utilization, Amuc_1100 expression, and in vivo fitness.
- Define engraftment rigorously as post-dosing persistence, not short-term fecal transit.
- Run a staged discovery screen in conventional C57BL/6J mice, both sexes.
- Perturb host niche state with a limited set of high-information conditions:
  - control diet
  - Western low-fiber/high-fat diet
  - Western diet plus fiber or polyphenol rescue
  - feeding/circadian misalignment
  - active-phase time-restricted feeding rescue
  - optional antibiotic-open niche as a mechanistic comparator, not the main model

**Primary readouts:**

- Strain-specific absolute qPCR and selective culture after dosing cessation
- mucus-associated AKK localization by FISH-IF
- mucus thickness and MUC2/goblet-cell markers
- baseline microbiome and resident mucin-degrader abundance
- feeding/activity rhythm
- metabolic outcomes: fat mass, OGTT/ITT, inflammatory markers

**Decision point:** Identify permissive versus resistant hosts and select the most informative arms for deep profiling.

### Aim 2. Learn a predictive and mechanistic model of the AKK-permissive mucus niche

**Question:** Can baseline host features predict live-AKK engraftment, and do those predictors reveal a causal niche state?

**Data layers:**

- baseline and early post-dose microbiome
- mucus imaging features
- mucin/goblet-cell gene expression
- metabolomics, especially bile acids, SCFAs, and mucin-derived metabolites
- feeding/activity rhythm metrics
- host inflammatory and metabolic markers

**Modeling strategy:**

- Use interpretable models first: elastic net, sparse logistic regression, Bayesian hierarchical models.
- Use nonlinear models cautiously: gradient boosting or random forest with nested cross-validation.
- Use latent-factor or multi-omics integration to identify a shared niche axis.
- Build models around pre-defined outcomes: engrafted versus cleared, engraftment half-life, mucus-associated AKK burden, and metabolic response.
- Treat AI as a hypothesis engine: models must nominate experimentally testable niche-engineering interventions.

**Expected deliverable:**

A minimal AKK-permissive niche signature, such as:

- preserved mucus layer plus high MUC2/goblet secretory program
- low competing mucin-degrader pressure
- favorable bile-acid/metabolite profile
- sufficient fermentable substrate or polyphenol exposure
- aligned feeding/activity rhythm

The exact signature should be learned from data, not assumed.

### Aim 3. Engineer resistant hosts into permissive hosts and test whether engraftment restores efficacy

**Question:** Can the model-predicted niche determinants be causally manipulated to convert non-engrafters into engrafters?

**Interventions selected from Aim 2:**

- fiber or polyphenol preconditioning if substrate/mucus support dominates
- active-phase time-restricted feeding or chrono-dosing if rhythm features dominate
- defined microbiome competition experiments if resident mucin degraders dominate
- epithelial clock or goblet-cell pathway validation if MUC2 rhythmicity emerges as causal

**Causal validation:**

- Test whether the selected intervention increases durable live-AKK engraftment.
- Test whether increased engraftment improves metabolic outcomes beyond vehicle and non-engrafted controls.
- Use epithelial *Bmal1* or *Tlr2* genetics only if justified by the discovery/modeling results, not as mandatory early scope.

**Translational endpoint:**

Convert the niche signature into actionable rules for live-AKK supplementation:

- who is likely to engraft
- what preconditioning improves engraftment
- whether timing/feeding alignment matters
- when pasteurized AKK may be preferable to live AKK

## CNS-Level Logic

The proposal should not be framed as "how to take AKK better." It should be framed as a general live-biotherapeutic principle:

> Durable engraftment of a therapeutic mucin specialist requires an engineerable host mucus-niche state.

AKK is the model organism and translational target. The broader impact is a framework for designing live biotherapeutics around host niche permissiveness rather than dose alone.

## Scope Control

To keep the project feasible for 2-3 PhD students:

- Make Aim 1 staged, not fully factorial across every variable.
- Keep deep omics restricted to engrafted versus non-engrafted high-contrast arms.
- Treat circadian experiments as targeted follow-up unless early data support them as dominant.
- Do not commit to both *Bmal1* and *Tlr2* knockout lines upfront.
- Avoid large human cohorts in the main proposal; use human data only as optional external relevance if available.

## Key Changes Needed in `proposal.md`

1. Replace the current circadian-window title with a mucus-niche engineering title.
2. Rewrite the abstract around live-AKK engraftment as a niche-state problem.
3. Move circadian rhythm from central hypothesis to candidate niche determinant.
4. Replace the 2 x 2 x 2 full factorial design with a staged discovery screen.
5. Define engraftment explicitly as durable post-dose persistence plus mucus-associated localization.
6. Make AI/modeling central to Aim 2 as predictive niche-state learning.
7. Make genetic validation conditional on discovery results.
8. Remove or soften bistability unless the design includes hysteresis/threshold experiments.
9. Clean references and remove unrelated papers.
