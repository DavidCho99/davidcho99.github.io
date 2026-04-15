---
layout: page
title: Structure Learning + BBN
permalink: /research/structure-learning-bbn/
nav_exclude: true
description: "Notes on Bayesian belief networks and structure learning (score-based, constraint-based, hybrid)."
---

## What I’m building

- A practical pipeline to learn a Bayesian Network structure from data, fit parameters, and run inference.
- A clean set of experiments: reproducible datasets, metrics, and ablations.

## Topics to cover (roadmap)

- Structure learning
  - Score-based (Hill Climbing, TABU), constraints (PC), and hybrid approaches
  - Regularization / sparsity, prior knowledge, and stability
- Parameter learning
  - MLE / Bayesian parameter estimation for discrete nodes
- Inference
  - Exact vs approximate, caching evidence, batch querying
- Evaluation
  - Predictive metrics (AUC/F1), calibration, and structure quality

## Links

- Lab notes / internal guidelines: [Bayesian Network post]({{ '/2025/01/02/implementation_plan.html' | relative_url }})

