---
layout: page
title: "JCIM: Peptide Inhibitor Design for Hsp90"
permalink: /projects/jcim/
toc: true
---

## Summary

**Status:** Published in *Journal of Chemical Information and Modeling* (2024 JIF 5.3).

This project used model-guided two-mutation screening to support the design of peptide inhibitors targeting the N-terminal domain of Hsp90.

It was my entry point into molecular discovery and taught me to treat candidate selection as a decision problem: model predictions, docking evidence, sequence mutations, and mechanistic interpretation all provide partial signals.

<style>
  .project-figure {
    margin: 1.5rem auto;
    text-align: center;
  }

  .project-figure .img-link,
  .project-figure > a {
    display: inline-block;
  }

  .project-figure img {
    width: auto;
    max-width: 100%;
    height: auto;
  }

  .project-figure--wide img {
    max-width: min(100%, 760px);
  }

  .project-figure--medium img {
    max-width: min(100%, 560px);
  }

  .project-figure--narrow img {
    max-width: min(100%, 420px);
  }

  .project-figure figcaption {
    margin: 0.6rem auto 0;
    max-width: 760px;
    text-align: left;
    font-size: 0.92rem;
    color: var(--text-muted-color);
  }
</style>

<figure class="project-figure project-figure--wide">
  <img src="/assets/source_figures/jcim/jcim_main_fig_01.png" alt="JCIM computational peptide-screening workflow">
  <figcaption><strong>Figure 1. Multi-stage computational screening workflow.</strong> The workflow begins with candidate peptide generation and machine-learning binding-propensity prediction, then uses structural docking to check whether selected peptides occupy the desired dual-site binding geometry. The dashed validation branch in the original paper indicates biological experiments that were not part of the published computational study. This figure is useful for reading the project as staged evidence generation rather than a single black-box prediction.</figcaption>
</figure>

## Scientific Problem

Peptide inhibitors can be chemically flexible and target protein interfaces that are difficult for small molecules. However, sequence space grows quickly, and not every favorable mutation is useful in the full molecular context. A practical design workflow needs to narrow candidates while checking whether model scores remain chemically plausible.

In this project, peptide-variant scoring was only the first question. The harder question was whether those scores could be interpreted together with docking and the proposed dual-site targeting mechanism.

## My Contribution

I was a co-first author. I designed the two-mutation screening strategy, deployed the machine-learning model, ran inference for candidate prioritization, and analyzed the relationship between prediction scores and docking results.

This project gave me my first concrete experience with evidence agreement: when model ranking, docking trend, and structural rationale point in the same direction, a candidate becomes more convincing; when they disagree, the disagreement itself becomes useful information.

## Workflow

1. Start from known peptide inhibitors and mutation candidates.
2. Generate two-mutation variants for model-guided screening.
3. Run the trained model to prioritize candidate sequences.
4. Compare model rankings with docking-score trends.
5. Interpret whether predicted candidates were chemically consistent with the dual-site targeting mechanism.

## Main Lesson

The central lesson is that prediction alone is not enough. Molecular discovery needs decisions under imperfect evidence. Model scores can suggest candidates, docking can provide a structural proxy, and mechanistic interpretation can help judge plausibility, but none of these signals is complete by itself.

This project is one reason I now care about trustworthy scientific agents: useful systems should know when evidence agrees, when it conflicts, and when more expensive validation is justified.

## Method Details

**Mutation-space design.** The starting peptide was the Hsp90-binding heptapeptide GRDLYDD reported in a crystal structure study. I generated all single and double mutants around this reference sequence, producing 7,714 candidate peptides in total. This local mutation strategy was a practical compromise: CAMP inference is fast, but each candidate also requires secondary-structure and intrinsic-disorder features, including ANCHOR-related scores, which are much slower to generate. Searching the full heptapeptide sequence space would therefore have been computationally impractical for this workflow.

**CAMP implementation.** I set up the CAMP environment, prepared the protein-peptide inputs, batch-ran the candidate mutants, aggregated the 5-fold prediction scores, and produced the CAMP-score data used for screening. The model was used as a rapid first-stage filter, not as final evidence of binding.

**Hybrid screening criteria.** The primary target was human Hsp90-NTD. Dictyostelium Hsp90-NTD was used as an additional screening reference because the original peptide structure came from that system. We used two complementary criteria: candidates with high predicted binding to human Hsp90-NTD, and candidates whose predicted binding scores exceeded the reference peptide for both human and Dictyostelium Hsp90-NTD. Most of the high-level screening logic came from Prof. Dong, while I implemented the numerical workflow and candidate scoring.

<figure class="project-figure project-figure--narrow">
  <img src="/assets/source_figures/jcim/jcim_main_fig_03.png" alt="CAMP screening flowchart for Hsp90 peptide mutants">
  <figcaption><strong>Figure 2. CAMP-based mutation-screening logic.</strong> Starting from the reference heptapeptide, all single and double mutants were generated and evaluated against Hsp90 proteins from human and non-human sources. One branch selected high-scoring candidates for human Hsp90-NTD, while the other selected candidates whose predicted binding exceeded the reference peptide across both systems. The intersection strategy helped keep the candidate set tractable while preserving cross-system binding plausibility.</figcaption>
</figure>

**Model-docking consistency.** During revision, a reviewer asked us to justify the use of CAMP more clearly by checking whether its predictions related to docking scores. I conducted additional docking and machine-learning prediction analyses to examine this relationship. This became an important evidence-agreement step: CAMP was used to reduce sequence space, while HDOCK and later MD/MM-PBSA provided orthogonal structural and thermodynamic checks.

<figure class="project-figure project-figure--medium">
  <img src="/assets/source_figures/jcim/jcim_main_fig_02.png" alt="CAMP consensus score versus HDOCK score">
  <figcaption><strong>Figure 3. CAMP score versus HDOCK score.</strong> This reviewer-requested analysis groups mutants by CAMP consensus score, defined by how often a mutant outperformed the reference peptide across the 5-fold CAMP models. The HDOCK score distributions provide an orthogonal structural check. The point was to test whether the machine-learning filter produced candidates whose docking behavior was at least directionally meaningful, without treating CAMP as a replacement for docking.</figcaption>
</figure>

**Figures and tables.** I provided the CAMP scores in Table 1, drew the figure analyzing the relationship between CAMP score and HDOCK score, and prepared Figure 8b showing how selected mutants affect the distance between key ATP-pocket entrance residues. I also contributed to the JCIM inner-cover artwork for the issue, which was mainly drawn by me and selected as the inner cover.

<figure class="project-figure project-figure--wide">
  <img src="/assets/source_figures/jcim/jcim_main_fig_08.png" alt="ATP-binding pocket entrance width and binding energy analysis">
  <figcaption><strong>Figure 4. ATP-pocket entrance width as a mechanistic readout.</strong> Panel a shows the ATP-binding pocket entrance, where polar residues such as K58 and K112 shape peptide engagement near the pocket opening. Panel b compares the distribution of pocket widths across peptide complexes, with median values marked for each system. The inset links calculated binding free energy to pocket entrance width, supporting the proposed mechanism that selected mutants can tighten or block the ATP-binding entrance through altered interaction networks.</figcaption>
</figure>

<figure class="project-figure project-figure--narrow">
  <img src="/assets/source_figures/jcim/jcim_inner_cover.jpg" alt="JCIM inner cover artwork for the Hsp90 peptide inhibitor paper">
  <figcaption><strong>Figure 5. JCIM inner-cover artwork.</strong> The editorial office invited us to submit cover artwork for the issue, and this design was selected as the inner cover. I mainly drew the cover, which made this project also an exercise in scientific visual communication: translating a computational peptide-design story into a single visual concept for a journal audience.</figcaption>
</figure>

**Revision role.** I wrote the CAMP-method section and handled much of the manuscript revision after the first author left the group. This included responding to reviewer concerns around the machine-learning screening rationale and the connection between CAMP predictions and downstream docking evidence.

**Current limitations.** This was a focused local search around a known reference peptide rather than a global peptide-design campaign. The final validation in the paper was computational, relying on docking, MD, and MM/PBSA rather than reported wet-lab target-binding assays. The project is therefore best viewed as a mechanistic and computational screening study rather than a complete therapeutic-discovery workflow.

## Link

Publication: [Dual-site targeting by peptide inhibitors of the N-Terminal domain of Hsp90: mechanism and design](https://pubs.acs.org/doi/10.1021/acs.jcim.5c00629)
