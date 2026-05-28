---
layout: page
title: "ChemBART: Reaction-Language-Model Pretraining"
permalink: /projects/chembart/
toc: true
---

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

## Summary

**Status:** Manuscript under review at *Nature Communications* (2024 JIF 15.7).

ChemBART is a reaction-language-model project for synthesis planning. My contribution focused on model deployment, workflow profiling, and large-scale pretraining acceleration.

This project expanded my view of AI for chemistry from molecular screening to scientific model infrastructure. A model is only useful if the data pipeline, training system, and deployment workflow make it practical to train, adapt, and evaluate.

<figure class="project-figure project-figure--wide">
  <a class="img-link" href="/assets/source_figures/chembart/chembart_main_fig_01.png">
    <img src="/assets/source_figures/chembart/chembart_main_fig_01.png" alt="Overview of the ChemBART reaction-language-model workflow">
  </a>
  <figcaption><strong>Project overview.</strong> ChemBART was designed as a reaction-language model pretrained on chemical reaction data through a mask-filling objective. The workflow connects pretraining, direct precursor and reagent prediction, downstream fine-tuning for reaction analysis and molecular-property prediction, and RL/MCTS-based multi-step synthesis planning. The final panel also frames the model as a component that can guide wet-lab validation and receive experimental feedback.</figcaption>
</figure>

## Scientific Problem

Reaction-language models can support synthesis planning, but their usefulness depends on more than architecture. Data preparation, tokenization, batching, numerical precision, and distributed training can determine whether a model is practical for larger-scale experiments.

The project also made me think about scientific AI tools as components inside a larger decision system. A synthesis model is powerful, but it remains an imperfect tool with cost, uncertainty, and domain limitations.

## My Contribution

I contributed to model deployment, workflow profiling, and pretraining acceleration. I identified repeated tokenization, sequence-length imbalance, and unnecessary numerical precision as major bottlenecks, then helped improve the pipeline using tokenization caching, length-aware batching, reduced precision, and ColossalAI-based distributed acceleration.

I describe the acceleration carefully because the earlier implementation was a weak baseline. The value of the project for me included both the speedup and the experience of turning a research model into a more practical scientific tool.

## Workflow

1. Deploy the reaction-language-model training pipeline.
2. Profile the baseline implementation to locate training bottlenecks.
3. Cache tokenization instead of recomputing it during training.
4. Use sequence-length grouping to reduce padding inefficiency.
5. Reduce unnecessary numerical precision where appropriate.
6. Apply distributed acceleration for larger-scale pretraining.
7. Prepare the workflow for downstream synthesis-planning tasks.

## Main Lesson

The main lesson is that scientific foundation models depend on systems engineering. If tokenization, batching, precision, and distributed execution are inefficient, model development becomes slow and difficult to iterate.

This experience connects to my PhD direction because agentic discovery systems will depend on many specialized tools. Each tool should be evaluated by scientific accuracy, uncertainty, failure modes, and operational cost.

## Method Details

**Profiling the pretraining bottleneck.** I joined ChemBART after the original pretraining run had already consumed several months on a rented 8-A100 machine without clear convergence. Prof. Dong asked me to inspect the pretraining process because the GPU cost was high and the training progress appeared to be slowing. After reviewing the source code, I found that the main bottlenecks came from avoidable engineering issues in the training pipeline rather than the BART architecture itself.

**Tokenization cache.** The original implementation read each reaction as a string during training and tokenized it repeatedly with a slow single-threaded tokenizer before sending batches to the GPU. This created a CPU-side bottleneck and broke the GPU training pipeline. I replaced this with a preprocessing and caching workflow: reactions were tokenized ahead of time with concurrency and saved to disk in batch files, allowing the model to train for long intervals without repeatedly reading raw strings or tokenizing during the training loop.

**Length-aware batching.** I analyzed the reaction-length distribution and found that many reactions were much shorter than the previous fixed 1024-token setting. Since Transformer computation scales roughly with sequence length squared, padding short reactions to 1024 tokens was highly inefficient. I grouped reactions into length pools, such as sequences shorter than 64 tokens and sequences between 64 and 128 tokens, then constructed batches from the same pool. This reduced padding waste while keeping each cached file small enough for practical memory use.

**Numerical precision and distributed training.** I switched pretraining from FP32 to BF16 and used ColossalAI for multi-GPU data parallelism. I also used ZeRO to reduce VRAM usage, which made it possible to increase the number of reactions processed across GPUs. Together with tokenization caching and length-aware batching, these changes made local-cluster pretraining practical.

<figure class="project-figure project-figure--medium">
  <a class="img-link" href="/assets/source_figures/chembart/chembart_si_fig_025.png">
    <img src="/assets/source_figures/chembart/chembart_si_fig_025.png" alt="Top-k success rate during ChemBART reactant-prediction pretraining">
  </a>
  <figcaption><strong>Pretraining convergence signal.</strong> The top-k success rate on USPTO-MIT reactant prediction increased during ChemBART training and showed convergence after approximately the seventh epoch. For my part of the project, this figure is useful because it shows why resolving training-system bottlenecks mattered: after the optimized pipeline made long training practical, convergence could be evaluated directly instead of inferred from a slow and expensive run.</figcaption>
</figure>

<figure class="project-figure project-figure--medium">
  <a class="img-link" href="/assets/source_figures/chembart/chembart_si_fig_026.png">
    <img src="/assets/source_figures/chembart/chembart_si_fig_026.png" alt="Top-k syntax error rate during ChemBART reactant-prediction pretraining">
  </a>
  <figcaption><strong>Generation validity during pretraining.</strong> The corresponding top-k syntax-error curves track whether the model is learning chemically valid sequence generation rather than only improving a ranking metric. I kept this figure because it complements the success-rate plot: synthesis-planning tools need useful candidates and valid outputs that can enter downstream decision workflows.</figcaption>
</figure>

**Outcome.** Relative to the inefficient baseline implementation, the optimized pipeline achieved about a 56x speedup and allowed the model to converge on our local cluster in less than 10 days. This removed an important uncertainty in the project: whether ChemBART was failing because the model design was flawed, or because the training system was too inefficient to reach convergence.

**LoRA fine-tuning.** After pretraining, some molecular-property tasks such as BBBP, BACE, Tox21, and ClinTox were difficult to improve with full-parameter fine-tuning. I proposed and conducted the LoRA fine-tuning plan, which produced more reasonable results and helped reduce overfitting in low-data property-prediction settings.

<figure class="project-figure project-figure--wide">
  <a class="img-link" href="/assets/source_figures/chembart/chembart_main_fig_05.png">
    <img src="/assets/source_figures/chembart/chembart_main_fig_05.png" alt="ChemBART task frameworks for classification regression generation policy and value functions">
  </a>
  <figcaption><strong>Task framework.</strong> The project used Transformer representations across classification, regression, generation, and synthesis-planning tasks. The BART scheme appends task-specific tokens and uses decoder outputs for labels or values; the BERT comparison uses encoder-side task tokens. The policy/value-function panel shows how a pretrained model can generate precursor options and then support MCTS through learned policy and value estimates.</figcaption>
</figure>

<figure class="project-figure project-figure--medium">
  <a class="img-link" href="/assets/source_figures/chembart/chembart_si_fig_034.png">
    <img src="/assets/source_figures/chembart/chembart_si_fig_034.png" alt="Validation RMSE comparison for value function training between ChemBART and ReSynZ">
  </a>
  <figcaption><strong>Value-function fitting.</strong> In value-function training, pretrained ChemBART-F and ChemBART-M achieved lower validation RMSE than the ReSynZ comparison, while ChemBART-R performed substantially worse. I kept this figure because it connects the infrastructure work to the synthesis-planning objective: a pretrained reaction model becomes more useful when its representations support decision functions inside search.</figcaption>
</figure>

**Current limitations.** My main contribution was engineering and optimization rather than inventing the ChemBART architecture or leading the synthesis-planning study. The 56x speedup should therefore be interpreted as a practical improvement over an inefficient training baseline rather than a new model architecture. The broader project still depends on noisy reaction-yield data and the coverage limits of public reaction datasets.

## Status

Manuscript under review at *Nature Communications* (2024 JIF 15.7).
