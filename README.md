# Robust Multiagent Combinatorial Path Finding

This repository implements the core algorithms and methods described in the paper "Robust Multi-Agent Combinatorial Path Finding".

## Files overview

* FindConflict.py — Implements the conflict detection logic used by the high-level CBS framework, identifying both standard and delay-based conflicts.
* LowLevelPlan.py — Contains the low-level planner responsible for computing individual agent paths given a set of constraints and a fixed goal sequence allocation.
* NodeStateConstClasses.py - Defines the data structures for representing constraint tree nodes, constraints, and agent states used throughout the planning process.
* Run_RobustCbss.py — Main entry point for running the Robust CBSS algorithm; handles initialization, parameter setup, and pipeline execution.
* Simulation_for_AblationStudy.py — Simulation script for evaluating planner performance under ablation study settings.
* TestRobustCbssAblationStudy.py — Runs the ablation study experiments.
* TestRobustCbssVsTSPA.py — Runs comparative experiments between Robust CBSS and the TSPA baseline.
* Verify.py — Provides utilities for verifying correctness and robustness of computed solutions.
* createMap.py - Utility script to create and initialize test maps/environments used in simulations, including agent and goal placements.
* kBestSequencing.py - Implements the core logic of the K-Best Sequencing procedure, generating multiple optimal goal sequence allocations by solving the problem as a standard TSP after applying a transformation.
* kBestSequencingWithGLKH.py - A variant of kBestSequencing.py that directly integrates the Generalized Lin-Kernighan-Helsgaun (GLKH) solver to solve the problem as an E-GTSP, allowing native handling of clusters and improving accuracy for complex goal structures.
* Technical_Appendix.pdf — Contains the technical appendix with the formal proofs presented in the paper.

## Directories Overview

* Agent_Goal_locations_files - Stores input files defining the initial configurations of agents and their corresponding goal locations. This folder provides the scenario setup for each experimental run.
* ExperimentalResults — Stores experimental results and output files.
* OurResearch.domain — Contains map files representing the testing environments

## Setup Note
To run the code, you will need to download and install the LKH or GLKH solvers. Please refer to the original solver papers cited in our paper for installation instructions and academic references.
