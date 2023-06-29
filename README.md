![LABODOCK](https://github.com/RyanZR/labodock/blob/main/res/labodock_banner.jpg)

# Effortless Docking with Google Colab
> UPDATE: Going to fix the condacolab and improve code base soon. Stay tuned. 
[![status](https://img.shields.io/badge/status-unstable-red)](https://github.com/RyanZR/labodock)
[![version](https://img.shields.io/badge/version-1.2.0-blue)](https://github.com/RyanZR/labodock/tree/main/notebooks)
[![size](https://img.shields.io/github/repo-size/RyanZR/labodock)](https://github.com/RyanZR/labodock)
[![license](https://img.shields.io/badge/license-MIT-informational)](https://github.com/RyanZR/labodock/blob/main/LICENSE)


**LABODOCK** is a repository where you can find a collection of Jupyter Notebooks for conducting structure-based molecular docking protocols interactively using Autodock Vina and PLIP on Google Colab. The main goal is to demonstrate the power of cloud-computing for conducting docking operations in an effortless and automated manner.

+ [Basic Molecular docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb)
+ [Virtual Screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) 

**Important:** Do not use the `Run all` option. Run the `Install dependencies and softwares` cell individually and wait for the session to restart. **After that**, you can run all cells if you want. Thank you for your support. 


## Features
+ Automated molecular docking operation 
+ intuitive and interactive user interface
+ Five grid box defining methods: [LABOGRID](https://github.com/RyanZR/labogrid), [eBoxSize](https://github.com/michal-brylinski/eboxsize) ...
+ Autodock Vina and Protein-Ligand Interaction Profiler integration
+ 3D Docking result and docking socres clustering


## Images
<div>
  <img align="top" src="https://github.com/RyanZR/labodock/blob/main/res/5YLU_vanoprazan_interaction.jpg" alt="vanoprazan" width="46.3%">
  <img align="top" src="https://github.com/RyanZR/labodock/blob/main/res/rank_score.jpg" alt="rank_score" width="35%">
</div>


## Limitation
+ There is no guarantee that these notebooks will run on platform other than Google Colab.
+ These notebooks do not necessarily reflect the standard protocol of docking operation. It is just a simple pipeple for illustrating molecular docking. 


## Bug
If you encounter any bugs, please report the issue to [https://github.com/RyanZR/labodock/issues](https://github.com/RyanZR/labodock/issues).


## References
1. Trott O, Olson AJ. AutoDock Vina: improving the speed and accuracy of docking with a new scoring function, efficient optimization, and multithreading. J Comput Chem. 2010 Jan 30;31(2):455-61. doi: 10.1002/jcc.21334. PMID: 19499576; PMCID: PMC3041641.
2. Salentin S, Schreiber S, Haupt VJ, Adasme MF, Schroeder M. PLIP: fully automated protein-ligand interaction profiler. Nucleic Acids Res. 2015 Jul 1;43(W1):W443-7. doi: 10.1093/nar/gkv315. Epub 2015 Apr 14. PMID: 25873628; PMCID: PMC4489249.
3. Feinstein WP, Brylinski M. Calculating an optimal box size for ligand docking and virtual screening against experimental and predicted binding pockets. J Cheminform. 2015 May 15;7:18. doi: 10.1186/s13321-015-0067-5. PMID: 26082804; PMCID: PMC4468813.


## License
These notebooks are licensed under MIT, see the [LICENSE](https://github.com/RyanZR/labodock/blob/main/LICENSE) file for details.
