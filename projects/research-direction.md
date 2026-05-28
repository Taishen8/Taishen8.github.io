---
layout: page
title: "Research Direction"
permalink: /projects/research-direction/
toc: true
---

## Abstract

My research has evolved from model-guided peptide inhibitor screening, to scalable reaction-language-model training, to AI-assisted discovery of catalytic self-assembling peptides. Across these projects, I became interested in a broader problem: **how can AI systems make reliable discovery decisions when literature, simulations, learned predictors, and experiments are all incomplete?**

Modern generative models can propose huge numbers of molecules, peptides, proteins, or materials. Scientific workflows also contain many specialized tools: literature-mining LLMs, docking engines, molecular dynamics, DFT, structure predictors, retrosynthesis models, property predictors, and robotic experiments. The bottleneck is increasingly not generation alone. The harder question is how an AI system should decide which information to trust, which tool to call, and which candidate to test.

## Core Problem

Scientific evidence is imperfect. Literature is biased toward positive findings. Simulations are approximate. Learned predictors fail outside their training distributions. Experimental feedback is often slow and expensive.

A useful discovery agent therefore needs to do more than generate candidates or route tasks between tools. It should maintain provenance-aware beliefs, estimate uncertainty, detect proxy-reward failures, and select experiments that maximize information gain under realistic constraints.

## Research Vision

I want to build evidence-grounded and feedback-driven agents for molecular and materials discovery. In molecular discovery, this means deciding when a docking score is sufficient, when molecular dynamics or synthesis feasibility should override it, when a literature claim should be down-weighted, and when a surprising candidate deserves experimental validation.

The long-term goal is a scientific decision system rather than a black-box generator. Such a system should be able to:

- extract and audit evidence from literature;
- combine heterogeneous tools with known failure modes;
- reason about uncertainty and provenance;
- choose experiments under limited budget;
- learn from validation feedback;
- produce candidates that are chemically meaningful and experimentally testable.

## Why My Previous Work Points Here

JCIM taught me that model scores must be checked against docking and mechanistic evidence. ChemBART taught me that scientific AI tools require serious data and systems engineering before they become useful. SAPIENS taught me how literature mining, dataset construction, model transfer, candidate prioritization, and experimental validation can be connected into a discovery workflow.

Together, these experiences point toward a PhD direction centered on reliable sequential decision-making for AI-driven discovery.

## Domains I Am Most Interested In

- self-driving laboratories and closed-loop discovery;
- catalysis and materials/energy applications;
- peptide and protein design when validation is realistic;
- LLM agents for science, especially when grounded in tools, uncertainty, and experimental feedback.

## How I Want To Develop This Direction

The next step I want to pursue goes beyond applying larger models to more molecular datasets. I want to study how scientific AI systems can make better decisions when every evidence source is partial. This includes how to compare literature evidence with computational predictions, how to decide whether an expensive validation experiment is justified, and how to update a discovery strategy when feedback is delayed or sparse.

This is why I am especially interested in PhD environments that connect modeling with real validation. Self-driving laboratories, catalysis platforms, materials discovery workflows, and experimentally grounded biomolecular design all provide settings where an AI system can be judged by whether it makes useful scientific decisions, beyond generating plausible candidates.
