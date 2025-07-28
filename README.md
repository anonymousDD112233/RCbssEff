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

## Repository Structure

- **Agent_Goal_locations_files/** – Agent and goal configuration files used in experiments.  
- **ExperimentalResults/** – Processed experimental data including success rates, runtimes, and ablation results.  
- **Maps/** – Benchmark grid maps (from [Stern et al., 2019](https://movingai.com/benchmarks/)) used in experiments.  
- **AAAI-2026_technicalAppendix.pdf** – Technical appendix with proofs, pseudocode, and additional experimental details.  
- **FindConflict.py** – Conflict detection module (vertex, edge, and delay conflicts) with p‑robust conflict handling.  
- **LowLevelPlan.py** – Low‑level single‑agent planner supporting orientation‑aware movement and kinematic constraints.  
- **NodeStateConstClasses.py** – Data structures for representing agent states, configurations, and constraints in the search.  
- **README.md** – This documentation file.  
- **Run_Robust_Cbss_Framework.py** – Main entry point to execute RCbssEff and RCbssBase on selected problem instances.  
- **Simulation_for_AblationStudy.py** – Script for running ablation studies (e.g., disabling delay modeling or rotation costs).  
- **TestRCbssEffAblationStudy.py** – Script for testing RCbssEff with ablation settings across various scenarios.  
- **TestRCbssEffScalability.py** – Script for scalability experiments over varying numbers of agents and goals.  
- **TestRCbssEffVsRCbssBase.py** – Script comparing RCbssEff against RCbssBase across benchmark tasks.  
- **Verify.py** – Probabilistic verification of p‑robustness using deterministic and Monte Carlo checks.  
- **createMap.py** – Utility for generating or preprocessing maps for experiments.  
- **kBestSequencing.py** – Implementation of the K‑best‑Sequencing algorithm for TSP‑based allocation (RCbssBase).  
- **kBestSequencingWithGLKH.py** – Extended K‑best‑Sequencing for E‑GTSP allocation (RCbssEff).  
