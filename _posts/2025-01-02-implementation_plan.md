---
layout: post
title: "Bayesian Network"
category: AI/ML
author: Gwangseong Cho
---

# AIM3 Lab - Modular BBN Platform Guidelines

## Goal 
The objective is to refactor the current Bayesian Belief Network (BBN) codebase into a **centralized, generalized, modular platform**. This platform allows different team members to research, implement, and test their own Data Engineering (preprocessing) approaches and Structure Learning algorithms

### Folder Structure
Team members will add their custom scripts inside the specific folders (`data_handlers/` and `structure_algorithms/`).

```text
AIM3_Lab/
├── core/
│   ├── bbn_model.py            # Core model logic (Do not modify)
│   └── inference.py            # Evaluation and querying (Do not modify)
├── main.py                     # Entry point (Selects data & algorithms)
├── data_handlers/              # ⬅️ Team Data Engineering folder
│   ├── __init__.py
│   ├── default_handler.py      # The baseline data prep
│   └── seong_handler.py        # Custom data prep by Seong
└── structure_algorithms/       # ⬅️ Team Algorithms folder
    ├── __init__.py
    ├── pc_algorithm.py         # Baseline PC Algorithm
    └── hill_climbing.py        # Team member's custom algorithm
