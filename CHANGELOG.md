# Change Log
All notable changes to this repository will be documented in this file. 

## [1.2.1] - 2023-08-12
### Changed
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MAJOR Upgraded packages: py3Dmol 2.0.3, rdkit-pypi 2022.9.5, biopython 1.80, openbabel 3.1.1, zlib 1.2.13
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MINOR Renamed LABOGRID to [LaBOX](https://github.com/RyanZR/LaBOX)
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MAJOR Upgraded packages: py3Dmol 2.0.3, rdkit-pypi 2022.9.5, biopython 1.80, openbabel 3.1.1, zlib 1.2.13
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MINOR Renamed LABOGRID to [LaBOX](https://github.com/RyanZR/LaBOX)

### Fixed
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MAJOR Fixed incomplete visualisation of protein-ligand interactions in `VIEW_PILE()`
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MAJOR Fixed incomplete visualisation of protein-ligand interactions in `VIEW_PILE()`

## [1.2.0] - 2023-02-12
### Added
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MAJOR Added 5 methods for defining grid box
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MINOR Added `showHs` argument in `VIEW_LIG()`
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MAJOR Added 5 methods for defining grid box
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MINOR Added `showHs` argument in `VIEW_LIG()`

### Changed
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MINOR Removed `showBestPose` argument in `VIEW_PILE()`
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MINOR Removed `AllChem.MMFFOptimizeMolecule()` in `VIEW_LIG()`
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MINOR Removed `AllChem.MMFFOptimizeMolecule()` in `VIEW_LIG()`

### Fixed
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MINOR Fixed spelling mistake in "*Display 3D binding mode*" section
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MINOR Fixed spelling mistake in "*Display 3D binding mode*" section

## [1.0.0] - 2023-02-08
### Added
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MAJOR Added into 📁 notebooks.
+ [virtual_screening](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb) MAJOR Added into 📁 notebooks.

### Changed
+ [🍊MOUNTAIN_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AMOUNTAIN_V2.ipynb) MAJOR No longer support and superseded by [basic_molecular_docking.ipynb](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb).
+ [🍊UNION_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8AUNION_V2.ipynb) MAJOR No longer support and superseded by [virtual_screening.ipynb](https://github.com/RyanZR/labodock/blob/main/notebooks/virtual_screening.ipynb).
+ [🍊PLIA_V2](https://github.com/RyanZR/labodock/blob/main/deprecated/%F0%9F%8D%8APLIA_V2.ipynb) MAJOR No longer support but integrated into respective notebooks

### Fixed
+ [basic_molecular_docking](https://github.com/RyanZR/labodock/blob/main/notebooks/basic_molecular_docking.ipynb) MINOR Fixed bug in `VIEW_PILE()`.
