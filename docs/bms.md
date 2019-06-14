---
id: bms
title: Biomolecular Simulations
---

In the biomolecular simulation (BMS) community, classical molecular dynamics (MD) simulations enable the elucidation of the relationship between the structure of biomolecules such as proteins, nucleic acids, or lipids and their function via their dynamics. 
MD simulations are wiedely used; for example, they account for approximately one quarter of the service units used on XSEDE resources. 
Although traditionally the generation of the data has been the computational bottleneck and has been highly optimized, more and more the analysis of the data is becoming a rate limiting step. 
Within the NSF DIBBs SPIDAL project we have been working on leveraging HPC resources for the analysis of BMS data.

## Packages

A number of software packages were developed or improved using the insights from the SPIDAL project.
More information about these packages can be found on their own pages.

1. [CCPTRAJ](bms-ccptraj.md) is a parallelized software package written in C++ for processing, transforming, and analyzing ensembles of molecular dynamics trajectory data.
2. [MDAnalysis](bms-mdanalysis.md) is an object-oriented Python library to analyze trajectories from molecular dynamics (MD) simulations in most commonly (and some uncommonly) used file formats. 
3. [PMDA](bms-pmda.md)  parallelizes common analysis algorithms in [MDAnalysis](bms-mdanalysis.md) through a task-based approach with the Dask library and runs parallel analysis on platforms ranging from laptops to supercomputers.
4. [RADICAL-Cybertools](bms-radical-cybertools.md)  are a set of software modules that can be used independently, composed into a single system, or integrated into existing systems to extend their functionalities. 
