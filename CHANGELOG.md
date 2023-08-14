# Change Log
All notable changes to this repository will be documented in this file. 

<br/>

## [1.2.2] - 2023-08-14
This update applies to both [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) and [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb).
### Major Changes
+ 🐛 Corrected `py3Dmol.view()` function call in all `VIEW_****()` functions by providing valid width and height parameters.
+ 🐛 Changed initial `count` to `0` in all `VIEW_****()` functions as per above correction.
### Minor Changes
+ ⚙️ Renamed `labogrid()` function to `labox()` as per version 1.2.1.
+ ⚙️ Changed merging DataFrame method from `append()` to `concat()` in `interaction_profiler()` and "Rank docking scores" section*.
+ ⚙️ Rewritten [CHANGELOG.md](https://github.com/RyanZR/labodock/blob/main/CHANGELOG.md)

*\* For [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) only.*

<br/>

## [1.2.1] - 2023-08-12
This update applies to both [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) and [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb). 
### Major Changes
+ ⬆️ Upgraded packages to support python 3.10: py3Dmol 2.0.3, rdkit-pypi 2022.9.5, biopython 1.80, openbabel 3.1.1, zlib 1.2.13.
+ ➕ Added `--cpu` parameter in `%vina` for performance improvement.
+ ➕ Added `os.cpu_count()` to determine number of cpu cores available for `--cpu` usage.
+ 🐛 Fixed incomplete visualisation of protein-ligand interactions in `VIEW_PILE()`.
### Minor Changes
+ ⚙️ Renamed **`LABOGRID`** to **[`LaBOX`](https://github.com/RyanZR/LaBOX)**.

<br/>

## [1.2.0] - 2023-02-12
This update primarily focuses on improvements to [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb). 
### Major Changes
+ ➕ Added 5 new methods for defining grid box.
+ ➕ Added `showHs` argument in `VIEW_LIG()`.
### Minor Changes
+ ⚙️ Corrected a spelling error in the "Display 3D binding mode" section. 
+ ❌ Removed `AllChem.MMFFOptimizeMolecule()` in `VIEW_LIG()`.

<br/>

## [1.1.0] - 2023-02-12
This update primarily focuses on improvements to [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb). 
### Major Changes
+ ➕ Added 5 new methods for defining grid box.
+ ➕ Added `showHs` argument in `VIEW_LIG()`.
### Minor Changes
+ ⚙️ Corrected a spelling error in the "Display 3D binding mode" section.
+ ❌ Removed `AllChem.MMFFOptimizeMolecule()` in `VIEW_LIG()`.
+ ❌ Removed `showBestPose` argument in `VIEW_PILE()`.

<br/>

## [1.0.0] - 2023-02-08
### Major Changes
+ ➕ Added [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) to supersede [🍊MOUNTAIN_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AMOUNTAIN_V2.ipynb).
+ ➕ Added [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) to supersede [🍊UNION_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AUNION_V2.ipynb).
+ ➕ Integrated protein-ligand interaction analysis into [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) and [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb).
+ 🚫 Deprecated [🍊MOUNTAIN_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AMOUNTAIN_V2.ipynb), [🍊UNION_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AUNION_V2.ipynb) and [🍊UNION_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AUNION_V2.ipynb).
### Minor Changes
+ 🐛 Fixed bug in `VIEW_PILE()` for [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb).
