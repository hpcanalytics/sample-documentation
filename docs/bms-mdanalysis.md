---
id: bms-mdanalysis
title: MDAnalysis
---

* Name: **MDAnalysis**
* License: [GNU General Public License v2](https://github.com/MDAnalysis/mdanalysis/blob/develop/LICENSE)
* Home page: https://www.mdanalysis.org
* Source code: https://github.com/MDAnalysis/mdanalysis
* Docs: https://www.mdanalysis.org/docs/ and [tutorials](https://www.mdanalysis.org/pages/learning_MDAnalysis/#tutorials)
* Citation: [1] [2]

## Summary

MDAnalysis is a Python library to analyze trajectories from molecular dynamics (MD) simulations. It provides unified access to trajectory data that allows users to write portable analysis code at a high level of abstraction that is agnostic of the format of the input data.

MDAnalysis has an active and welcoming community of users and developers and extensive [documentation](https://www.mdanalysis.org/docs/) and [tutorials](https://www.mdanalysis.org/pages/learning_MDAnalysis/#tutorials).


## Purpose and Capabilities

The goal of MDAnalysis is to make it easy for users to analyze data that are produced by particle-based simulations (primarily [molecular dynamics simulations](https://en.wikipedia.org/wiki/Molecular_dynamics)) that run on some of the largest supercomputers in the world.  It accomplishes this goal by providing a toolkit of programming building blocks that provide an abstract interface to the simulation data that lends itself to interactive data exploration and rapid prototyping but is also a robust foundational library that can form the basis for new [computational tools](https://www.mdanalysis.org/pages/used-by/). It comes with a large [collection of analysis modules](https://www.mdanalysis.org/docs/documentation_pages/analysis_modules.html) that enable the researcher to immediately perform common analysis tasks.

The user interface and modular design work equally well in complex scripted work flows, as foundations for other packages, and for interactive and rapid prototyping work in IPython / Jupyter notebooks, especially together with molecular visualization provided by nglview and time series analysis with pandas. 

MDAnalysis can read and write a very [wide range of file formats](https://www.mdanalysis.org/docs/documentation_pages/coordinates/init.html#id2) that are used in the biomolecular and materials science simulation communities. The library abstracts  access to the raw simulation data and presents a uniform object-oriented Python interface to the user. It thus enables users to rapidly write code that is portable and immediately usable.                
MDAnalysis is written in Python and Cython and uses NumPy arrays for easy interoperability with the wider scientific Python ecosystem. 
            
<iframe width="420" height="315" src="https://www.youtube.com/embed/zVQGFysYDew" frameborder="0" allowfullscreen></iframe>        
     
## Who uses it?

MDAnalysis is used by hundreds of researchers in biophysics, materials sciences, and chemistry, with the papers [1] and [2] having been cited more than 650 times (source: Google Scholar, June 2019). It [forms a foundation](https://www.mdanalysis.org/pages/used-by/) for more specialized biomolecular simulation tools. MDAnalysis is written by Scientists for Scientists. The community is welcoming and helpful and [welcomes new contributions](https://www.mdanalysis.org/#participating).

MDAnalysis is [easy to install](https://www.mdanalysis.org/pages/installation_quick_start/) on Linux, Windows, and macOS, ranging from laptops to supercomputers. It supports Python 3.5+ and legacy Python 2.7. 


## References

1. N. Michaud-Agrawal, E. J. Denning, T. B. Woolf, and O. Beckstein. MDAnalysis: A Toolkit for the Analysis of Molecular Dynamics Simulations. *J. Comput. Chem.* **32** (2011), 2319–2327. doi:[10.1002/jcc.21787](http://dx.doi.org/10.1002/jcc.21787)
2. R. J. Gowers, M. Linke, J. Barnoud, T. J. E. Reddy, M. N. Melo, S. L. Seyler, D. L. Dotson, J. Domanski, S. Buchoux, I. M. Kenney, and O. Beckstein. MDAnalysis: A Python package for the rapid analysis of molecular dynamics simulations. *In* S. Benthall and S. Rostrup, editors, *Proceedings of the 15th Python in Science Conference*, pages 98-105, Austin, TX, 2016. SciPy. doi:[10.25080/Majora-629e541a-00e](https://doi.org/10.25080/Majora-629e541a-00e)


