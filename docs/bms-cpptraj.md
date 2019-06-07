---
id: bms-cpptraj
title: CPPTRAJ
---

* Name: **CPPTRAJ**
* License: [GPL v3 or greater](https://github.com/Amber-MD/cpptraj/blob/master/LICENSE)
* Home page: https://github.com/Amber-MD/cpptraj and http://ambermd.org/AmberTools.php
* Source code URL: https://github.com/Amber-MD/cpptraj and http://ambermd.org/AmberTools.php
* Docs URL: https://github.com/Amber-MD/cpptraj/tree/master/doc and
  http://ambermd.org/doc12/Amber18.pdf and [CPPTRAJ tutorials](http://ambermd.org/tutorials/TrajectoryAnalysis.php#cpptraj)
* Citations: [1-3]

## Summary

CPPTRAJ is a parallelized software package written in C++ for processing, transforming, and analyzing ensembles of molecular dynamics trajectory data. It includes a rich set of commonly used analysis and transformative tools to be a versatile platform for extracting meaningful information in a general way from molecular dynamics simulation data.

## Purpose and Capabilities

Thanks to advances in, and the availability of, large-scale computing on both CPUs and GPUs, biomolecular simulation methods with molecular dynamics (MD) have advanced to become significant data producers, even in single straight MD, such as evidenced in long MD simulations on the Anton special purpose computers. With access to large scale compute resources, it is quite common today to apply MD as a large set of either disconnected or loosely coupled (for enhanced sampling with replica-exchange) ensembles of molecular dynamic simulations. This leads to the generation of a large series of MD trajectory data (which refers to the time series of atomic coordinates). In loosely coupled ensembles, the trajectory data may be scrambled and needs to be sorted into new MD trajectories along a given process various (for example temperature or ensemble instance or replica number or other variable like Hamiltonian). PTRAJ, and its successor CPPTRAJ, were developed starting in the 90’s with PTRAJ and 2000’s with CPPTRAJ to provide general purpose capabilities for analyzing MD trajectory data and for transforming, converting, and modifying the raw MD trajectories and derived data.

Almost all of the common capabilities for analyzing MD trajectories and the derived data are implemented in CPPTRAJ. In addition to accepting many common MD trajectory formats, analysis capabilities range from RMS fitting to imaging, clustering to energy analysis, to hydrogen bond and contact analysis. Refer to the published literature by Roe and Cheatham and see the documentation to better understand the full capabilities. Most notable is four levels of parallelism (MPI over ensemble instances, MPI over files, Open-MP, and CUDA for very time consuming analysis) and the ability to analyze full sets of ensemble or replica exchange simulations in a single run. The code is also fairly well optimized.

## Who uses it?

Distributed with the [AmberTools](http://ambermd.org/AmberTools.php) “open-source” set of MD set-up, simulation and analysis code and also with the latest “beta” version available on GitHub, CPPTRAJ is used by many users and developers of MD simulation codes. According to Google Scholar (December 2018), the main article from 2013 has been cited 1125 times.

The main data analyzed is time series or ensembles of time series of atomic coordinates generated from MD simulation. The code runs on everything from laptops to the Blue Waters Petascale Resource. Some recent work highlighting the capabilities from the Cheatham lab include large-scale analysis of multidimensional replica exchange data and showing full convergence and reproducibility in the elucidation of the conformational ensembles of various DNA and RNA molecules [4-8]. In each of our papers, the supporting information provides the CPPTRAJ scripts necessary to analyze similar data and we often endeavor to make our MD trajectory data available at http://amber.utah.edu. 



## References

1. DR Roe and TE Cheatham, III. “Parallelization of CPPTRAJ enables large scale analysis of molecular dynamics trajectory data” *J. Comp. Chem.* **39**, 2110-2117 (2018) doi: [10.1002/jcc.25382](https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.25382). 
2. Z Heidari, DR Roe, R Galindo-Murillo, JB Ghasemi and TE Cheatham, III. “Using Wavelet Analysis To Assist in Identification of Significant Events in Molecular Dynamics Simulations.” *J. Chem. Inf. Model.* **56**:1282-1291 (2016). doi: [10.1021/acs.jcim.5b00727](https://pubs.acs.org/doi/10.1021/acs.jcim.5b00727). 
3. DR Roe and TE Cheatham, III. “PTRAJ and CPPTRAJ: Software for processing and analysis of molecular dynamics trajectories.” *J. Chem. Theory Comp.* **9**, 3084-3095 (2013). Doi: [10.1021/ct400341p](https://doi.org/10.1021/ct400341p)
4. R Galindo-Murillo, JC Robertson, M Zgarbová, J Šponer, M Otyepka, P Jurečka, and TE Cheatham, III. “Assessing the Current State of Amber Force Field Modifications for DNA.” *J. Chem. Theory Comp.* **12**:4114-4127 (2016). doi: [10.1021/acs.jctc.6b00186](https://doi.org/10.1021/acs.jctc.6b00186)
5. C Bergonzo and TE Cheatham, III. “Improved Force Field Parameters Lead to a Better Description of RNA Structure.” *J. Chem. Theory Comp.* **11**:3969-3972 (2015). doi: [10.1021/acs.jctc.5b00444](https://doi.org/10.1021/acs.jctc.5b00444).
6. C Bergonzo, NM Henriksen, DR Roe, and TE Cheatham, III. “Highly sampled tetranucleotide and tetraloop motifs enable evaluation of common RNA force fields.” *RNA*. **21**:1578-1590 (2015). doi: [10.1261/rna.051102.115](https://doi.org/10.1261/rna.051102.115).
7. R Galindo-Murillo, DR Roe, and TE Cheatham, III. “Convergence and reproducibility in molecular dynamics simulations of the DNA duplex d(GCACGAACGAACGAACGC).” *Biochim Biophys Acta*. **1850**:1041-1058 (2015). doi: [10.1016/j.bbagen.2014.09.007](https://doi.org/10.1016/j.bbagen.2014.09.007)
8. R Galindo-Murillo, DR Roe, and TE Cheatham, III. “On the absence of intrahelical DNA dynamics on the μs to ms timescale.” *Nat Commun.* **5**:5152. doi: [10.1038/ncomms6152](https://doi.org/10.1038/ncomms6152).

