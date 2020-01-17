---
id: bms-pmda
title: PMDA
---

* Name: **PMDA** (“Parallel MDAnalysis”)
* License: [GNU General Public License v2](https://github.com/MDAnalysis/pmda/blob/master/LICENSE)
* Home page: https://www.mdanalysis.org/pmda
* Source code: https://github.com/MDAnalysis/pmda
* Docs: https://www.mdanalysis.org/pmda/
* Citation: [1]


## Summary

PMDA parallelizes common analysis algorithms in [MDAnalysis](bms-mdanalysis.md) through a task-based approach with the [Dask](https://dask.org) library. Although still in early development, it is already used on resources ranging from multi-core laptops to XSEDE supercomputers to speed up analysis of molecular dynamics trajectories [1].

## Purpose and Capabilities

To speed up analysis of molecular dynamics trajectories, PMDA implements a simple split-apply-combined scheme for parallel trajectory analysis for MDAnalysis [1-3]. The trajectory is partitioned into blocks ("split") and analysis is performed separately and in parallel on each block (“apply”). The results from each block are gathered and combined (“combine”).

PMDA allows one to perform parallel trajectory analysis with pre-defined analysis tasks which have the same input and output as MDAnalysis.  In addition, it provides a common interface that makes it easy to create user-defined parallel analysis modules.

It contains a growing number of analysis capabilities such as RMSD, contacts, radial distribution functions [1], leaflet analysis [3], and RMSF and volumetric density  [4]. It also provides a framework for users to write their own parallel analysis tools [1].

## Who uses it?

The audience of this package are researchers who are familiar with MDAnalysis and want to speed up analysis of molecular dynamics trajectories. Best results are observed if expensive computations are performed for each frame because I/O (loading each trajectory frame into memory) represents a substantial cost.

PMDA is [easy to install](https://www.mdanalysis.org/pmda/#installation) and can improve performance of analysis on machines ranging from laptops to supercomputers with hundreds of cores. Like [MDAnalysis](bms-mdanalysis.md) it runs under Linux, Windows, and macOS and supports both Python 3.5+ and legacy Python 2.7.





## References

1. S. Fan, M. Linke, I. Paraskevakos, R. J. Gowers, M. Gecht, and O. Beckstein. PMDA — parallel molecular dynamics analysis. In C. Calloway, D. Lippa, D. Niederhut, and D. Schupe, editors, Proceedings of the 18th Python in Science Conference (SciPy 2019), Austin, TX, 2019. SciPy. doi: [10.25080/Majora-7ddc1dd1-013](https://doi.org/10.25080/Majora-7ddc1dd1-013).
2. M. Khoshlessan, I. Paraskevakos, S. Jha, and O. Beckstein. Parallel analysis in MDAnalysis using the Dask parallel computing library. *In* Katy Huff, David Lippa, Dillon Niederhut, and M. Pacer, editors, *Proceedings of the 16th Python in Science Conference*, pages 64–72, Austin, TX, 2017. SciPy. doi:[10.25080/shinma-7f4c6e7-00a](https://doi.org/10.25080/shinma-7f4c6e7-00a). 
3. Ioannis Paraskevakos, Andre Luckow, Mahzad Khoshlessan, George Chantzialexiou, Thomas E. Cheatham, Oliver Beckstein, Geoffrey C. Fox and Shantenu Jha. Task-parallel Analysis of Molecular Dynamics Trajectories. In *47th International Conference on Parallel Processing (ICPP 2018)*. doi: [10.1145/3225058.3225128](https://doi.org/10.1145/3225058.3225128).
4. Awtrey, Nikolaus. SPIDAL Summer REU 2019: Parallelizing DensityAnalysis and RMSF in PMDA. Technical report, Arizona State University, Tempe, AZ, 2019. doi: [10.6084/m9.figshare.9695852](https://doi.org/10.6084/m9.figshare.9695852)

