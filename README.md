# Robust Multi‑Agent Combinatorial Path Finding

This repository contains the official code accompanying the AAAI‑2026 submission:  
> **Robust Multi‑Agent Combinatorial Path Finding**

It implements the **Robust CBSS framework**, including both algorithms presented in the paper:
- **RCbssBase** – a baseline algorithm using TSP‑based allocation  
- **RCbssEff** – an improved and efficient variant using orientation‑aware E‑GTSP allocation  

The framework extends the **Conflict‑Based Steiner Search (CBSS)** to support:
- **Dynamic goal allocation** with K‑best‑Sequencing  
- **Orientation‑aware kinematic constraints**  
- **Probabilistic robustness** against stochastic execution delays (p‑Robust CBS)  

This repository includes full source code, benchmark data, experiment scripts, and a technical appendix to enable **full reproducibility** of the results presented in the paper.

---
