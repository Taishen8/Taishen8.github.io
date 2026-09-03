---
layout: page
title: "SAPIENS: AI-Assisted Catalytic Peptide Discovery"
permalink: /projects/sapiens/
toc: true
---

## Summary

**Status:** ChemRxiv preprint; submitted to *JACS* after substantial revision informed by external peer review at *Nature Catalysis*.

SAPIENS uses literature-mined peptide self-assembly knowledge to support the discovery of catalytic self-assembling peptides. The project connects LLM-assisted literature mining, biased-data reconstruction, representation learning, candidate screening, and experimental validation.

This is the project that most clearly shaped my PhD direction: AI-driven discovery requires more than proposing molecules or sequences. It needs an evidence chain strong enough to justify which candidate should be tested next.

<style>
  .figure-center {
    margin: 1.5rem auto 0.4rem;
    text-align: center;
  }

  .figure-center .img-link,
  .figure-center > a {
    display: inline-block;
  }

  .figure-center img {
    width: auto;
    max-width: 100%;
    height: auto;
  }
</style>

![SAPIENS framework overview](/assets/source_figures/sapiens/sapiens_main_fig_01.png)
{: .figure-center }
_Figure 1. Overview of the SAPIENS workflow. The Data Engine starts from LLM-mined peptide self-assembly reports and combines them with length-matched unlabeled peptide sequences; positive-unlabeled learning and spy separation are then used to reconstruct a more reliable negative set. The AI Engine maps peptide sequences into a latent representation with a Transformer encoder and predicts both self-assembly propensity and catalytic proficiency. The Discovery Engine closes the loop by sending model-prioritized candidates to expert review and wet-lab validation, followed by structural analysis of the discovered peptide assemblies._

## Scientific Problem

Catalytic peptides are attractive because they are modular, chemically tunable, and potentially easier to connect with biological and materials contexts than many traditional catalyst platforms. The design problem is difficult because successful examples are sparse, negative examples are rarely reported, and design rules remain incomplete.

A useful AI workflow therefore needs to construct evidence from biased literature, recover useful supervision from incomplete reports, and make careful decisions about which candidates deserve experimental resources instead of treating the problem as a clean labeled benchmark.

## My Contribution

I was the first-listed co-first author. I led the LLM-assisted literature mining, dataset construction, machine-learning model development, computational analysis, and a major part of manuscript writing. Wet-lab validation was conducted by my experimental co-first authors.

The computational contribution was a discovery workflow rather than a single model: build a usable dataset from literature, transfer information from peptide self-assembly to catalytic-function prediction, screen a large design space, and prioritize candidates that collaborators could test.

## Workflow

1. Mine peptide self-assembly papers with LLM-assisted extraction.
2. Curate positive self-assembling peptide examples from literature.
3. Reconstruct high-confidence negative examples to address missing negative data.
4. Train Transformer-based models for self-assembly and catalytic-function prediction.
5. Screen a large HXH-motif heptapeptide candidate space.
6. Prioritize sequences for experimental validation.
7. Interpret why selected candidates deviate from conventional alternating hydrophobic/hydrophilic design rules.

## Main Lesson

The most important lesson is the evidence chain. Literature mining supplies imperfect but scalable information. Positive-unlabeled learning helps make missing negatives usable. Multi-task modeling transfers a richer self-assembly signal to a sparse catalytic target. Experimental validation tests whether the computational ranking was useful.

This is close to the kind of closed-loop scientific system I want to build during my PhD: a workflow that tracks evidence, uncertainty, feasibility, and validation feedback instead of acting as a black-box generator.

## Method Details

![SAPIENS dataset construction and PU learning](/assets/source_figures/sapiens/sapiens_main_fig_02.png)
{: .figure-center }
_Figure 2. Dataset construction and validation. Panel a shows the LLM-assisted extraction workflow with iterative extraction and majority-voting filters. Panel b summarizes how extraction precision and recall change with the voting threshold, motivating the use of repeated extraction rather than trusting a single LLM pass. Panel c illustrates the positive-unlabeled learning setup: known self-assembling peptides provide positive examples, while spy samples help distinguish reliable negatives from the unlabeled peptide pool. Panel d shows the resulting score distributions, where spies align with true positives and the denoised negative set separates more clearly after filtering. Panel e places the constructed positive and negative examples in peptide sequence space, showing how the dataset expands beyond sparse literature-reported examples._

**Literature extraction.** The first version of the pipeline aimed to extract a fully reproducible experimental record from peptide self-assembly papers, including sequence, assembly label, morphology, temperature, pH, incubation time, terminal modifications, and residue chirality. This more ambitious schema exposed two problems. First, LLM extraction was brittle for complex and inconsistently defined fields such as morphology and chemical modification. Second, early hand-curated experiments showed strong literature bias: paper-wise train/test splitting reduced prediction performance close to guessing, and random entry-wise splitting could produce high accuracy even when the peptide sequence was masked. These results pushed the project toward a more conservative and auditable target: extracting peptide sequences and self-assembly labels first.

**Negative-data construction.** Self-assembling sequences were far more common than non-assembling sequences in the mined literature. To address the missing-negative problem, I treated self-assembly prediction as a positive-unlabeled learning problem. Human peptide sequences were used as an unlabeled pool under the assumption that naturally occurring human peptides are less likely to be dominated by strongly self-assembling, potentially cytotoxic sequences. I then used spy separation to denoise the unlabeled pool, identify likely positives, remove them, and construct high-confidence negative examples for downstream training.

**Model input.** After testing different input designs, the final model used a simplified residue-level descriptor representation rather than a large hand-engineered condition table. Each residue was represented by five physicochemical descriptors: hydropathy, radius, electron-ion interaction potential, charge, and electrostatic-potential slope. This kept the model focused on sequence-derived properties while reducing the risk of learning paper-specific experimental artifacts.

**Multi-task prediction.** The model used two prediction heads: self-assembly probability and catalytic proficiency, measured by catalytic efficiency. I trained the tasks jointly because self-assembly and catalytic function were expected to share mechanistic information. Ablation studies supported this design by showing that multi-task learning improved catalytic prediction relative to single-task alternatives.

![SAPIENS multi-task learning and active-learning progress](/assets/source_figures/sapiens/sapiens_main_fig_03.png)
{: .figure-center }
_Figure 3. Multi-task learning and discovery progress. Panel a shows the shared-encoder architecture, where abundant self-assembly data and sparse catalytic data are learned jointly. Panels b and c compare virtual screening with catalytic labels alone versus the full SAPIENS framework; adding self-assembly and sequence-level supervision enriches high-activity candidates in the top-scoring region. Panel d summarizes the activity progression across discovery rounds, showing how the workflow moved from cold-start prediction to PU learning and multi-task learning before identifying the lead candidate GW1._

**Candidate prioritization.** The screened design space contained more than 9.4 million HXH-motif heptapeptide variants. Candidates were first narrowed by taking the intersection of the top-ranked sequences for predicted self-assembly and catalytic proficiency. I then inspected their distribution in an ESM-embedding UMAP space to check whether the selected candidates explored a distinct region rather than simply repeating known sequence patterns. The final choices were also reviewed by Prof. Dong, so the workflow combined model ranking, representation-space novelty, and expert chemical judgment.

![SAPIENS candidate novelty in sequence space](/assets/source_figures/sapiens/sapiens_si_fig_09.png)
{: .figure-center }
_Figure 4. Candidate novelty in peptide sequence space. Panel a places generated self-assembling sequences in an ESM-based embedding space against a broad peptide background. Panel b overlays predicted catalytic potential, turning the embedding into an activity map for candidate search. Panel c compares SAPIENS-selected candidates with literature rational-design peptides, showing that the selected sequences occupy high-activity regions that are spatially distinct from known designs rather than simply reproducing nearby literature examples._

**Experimental validation.** Experimental collaborators tested selected sequences by checking assembly behavior with circular dichroism, inspecting morphology with atomic force microscopy, and measuring catalytic performance. This validation step was essential because the model was designed to prioritize candidates, not to replace experimental evidence.

![SAPIENS experimental validation](/assets/source_figures/sapiens/sapiens_main_fig_04.png)
{: .figure-center }
_Figure 5. Experimental validation of the lead SAPIENS-designed peptide. Panel a compares catalytic activity for pNPA hydrolysis against sequence similarity to the reference peptide IIQ, showing that GW1 combines high activity with sequence novelty relative to literature benchmarks. Panel b tests whether GW1 generalizes across ester hydrolysis substrates. Panel c extends the validation to DMP oxidation, indicating broader catalytic relevance beyond a single assay._

**Current limitations.** The project still depends on sparse and delayed wet-lab supervision, expert review in the final candidate-selection step, and a dataset-construction strategy that must be interpreted carefully because human peptides and artificial peptide designs may differ in multiple correlated ways. The validated improvement over previous peptide catalysts was meaningful but incremental, which makes the project a strong starting point for closed-loop discovery rather than a finished AI-scientist system.

## Feedback Bottleneck

SAPIENS also made the feedback bottleneck concrete. Even when a computational workflow can screen millions of candidates, experimental supervision arrives slowly and sparsely. In this project, one validation batch could take roughly 20 to 30 days, with peptide synthesis alone requiring about two weeks. This delay changes the AI problem: the model should rank candidates and decide which experiment is worth spending a scarce validation slot on.

This experience motivates my interest in closed-loop discovery, self-driving laboratories, and evidence-grounded scientific agents. I view self-driving laboratories as more than automation platforms: they can make supervision more timely, structured, and useful for sequential decision-making. More broadly, I want to build discovery systems that remain reliable when feedback is expensive, delayed, and incomplete.

## Link

ChemRxiv preprint: [AI Unlocks Superior Catalytic Self-Assembly in Peptides](https://chemrxiv.org/doi/full/10.26434/chemrxiv.15002365/v1)
