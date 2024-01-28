# Changelog
All notable changes to this project will be documented in this file. \
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
### Added
+ **`PRE`** : Add assertion to check existance of protein `PDB` file
+ **`DCK`** : Add `vinardo` scoring option

### Changed
+ **`PKG`** : Update `condacolab` from `0.1.7` to `0.1.8` [#7](https://github.com/RyanZR/labodock/issues/7)
+ **`PKG`** : Swtich setup process to using `environment.yml`
+ **`SRC`** : Improve cell and output descriptions for better understanding 
+ **`PRE`** : Replace `extract_entity()` with `extract_protein()` and `extract_ligand()` for better extraction handling


### Fixed
+ **`PRE`** : Fix typo from `2>>` to `&>>` in `Generate ligand SD files` cell [#4](https://github.com/RyanZR/labodock/issues/4)

### Removed
+ **`SRC`** : Remove `import PLIP` and `from google.colab import files`

## [2.0.0] - 2023-10-12
🎉 **LABODOCK v2.0.0** is here! 

This update focuses on improving the code base, implementing informational molecular visualization, and fixing post-installation conda environment corruptions. 

Most functions have been refactored and improved, and previous molecular visualization options have been reduced with new being added to provide informative visual inspection 👀.

The conda environment is no longer corrupted by `MGLTools` package installation, and you can now install any other packages that require Python 3.10 or higher 🐍.

The native ligand preparation step is now **optional** by default. Should you proceed without this phase, skip the `03 | Preparing the Native Ligand (optional)` section ✨.


### Added
+ **`PKG`** : Add `meeko 0.5.0` to replace `MGLTools 1.5.7` for preparing `.pdbqt` files
+ **`PKG`** : Add `sPyRMSD 0.6.0` to include Hungarian's algorithm and symmetry corrected RMSD calculations
+ **`SRC`** : Add basic function type hints and annotations for better code understanding
+ **`PRE`** : Add bond order assignment for native ligand with RDKit `AllChem.AssignBondOrdersFromTemplate()` function
+ **`ENM`** : Add gradient option to select from `conjugate` (default) or `steepest` **
+ **`ENM`** : Add convergence criteria option to specify termination endpoint 
+ **`ENM`** : Add maximum steps option to specify allowed iteration step
+ **`ENM`** : Add logging into `_obmin.log` file to store ligand EGM record
+ **`GBX`** : Add residues-defined gird box option (`defined-by-res()` method) using `LaBOX` method and list of user-inpt residues 
+ **`RMS`** : Add maximum common substructrure PNG generation in `ComputeRMSD()` class
+ **`ANL`** : Add result clustring mode option to select from `Best-Pose` and `LABO-RMSD` **
+ **`ANL`** : Add ranking option for docking result ** (`Sort_by`, `Order`, `Top`, `Maximum_RMSD`)
+ **`ANL`** : Add ranking option for binding interactions with frequency bar chart ** (`Sort_by`, `Order`, `Hide_hydrophobic`, `Show_barchart`)
+ **`VIS`** : Add 8 new built-in py3Dmol stylings focusing on providing informational visualisation
+ **`VIS`** : Add 2 new protein surface representations with built-in colour scales (hydrophobicity, isoelectric points)
+ **`VIS`** : Add colour bar for displaying colour scale of surface representation with Matplotlib `pyplot.colorbar()` function
+ **`VIS`** : Add slab view option to display sagittal section of molecules
+ **`VIS`** : Add filter option to specify displaying binding interactions

### Changed
+ **`PKG`** : Update `Autodock Vina` from `1.2.0` to `1.2.5`
+ **`PKG`** : Update `PLIP` from `2.0.0` to `2.2.2`
+ **`SRC`** : Update source code to improve logic, clarity and compliance to PEP 8, PEP 3107
+ **`DSC`** : Rewrite cell description and form fields to improve clarity, accuracy and specificity
+ **`PRE`** : Enable native ligand preparation step as `optional` [#3](https://github.com/RyanZR/labodock/issues/3)
+ **`PRE`** : Replace molecule structure extraction code with vanilla `extract_entity()` function
+ **`PRE`** : Replace `separate_chain()` function with vanilla `extract_chains()` function
+ **`GBX`** : Encapsulate all grid box calculation functions into `GridBox()` class
+ **`DCK`** : Change `--exhaustiveness` default value to `16`
+ **`INT`** : Update `_cmpx.pdb` file generation code with `generate_cmpx_pdb()` function
+ **`INT`** : Refactor `interaction_profiler()` into nested function
+ **`RMS`** : Replace `get_RMSD()` function with `labo_RMSD()` method under `ComputeRMSD()` class to generate MCS-based RMSD
+ **`RMS`** : Replace `get_score()` function with `vina_report()` function and `rmsd_report()` method to generate docking report
+ **`VIS`** : Replace `VIEW()` function with `LaboSpace()` class to consolidate all visualisation functions

### Fixed
+ **`ENV`** : Conda base environment no longer corrupted from `MGLTools` installation
+ **`SRC`** : Replace non-standard `for` loop with pythonic-style `for` loop

### Removed
+ **`SRC`** : Remove `{'run': 'auto'}` options
+ **`DCK`** : Remove SDF generation step for docked ligand output file in `Process output file` cell

### Deprecated
+ **`PKG`** : Remove `MGLTools`, `Pybel`, `Biopython`, `xlswritter`

*\*\* Exclusively for virtual screening protocol.*

## [1.2.2] - 2023-08-14
### Changed
+ **`SRC`** : Update DataFrame merging method from `append()` to `concat()`
+ **`RMS`** : Rename `labogrid()` function to `labox()` as per version 1.2.1
+ **`VIS`** : Reset `count` to `0` in all `VIEW_****()` functions

### Fixed
+ **`VIS`** : Correct input arguments for `py3Dmol.view()` function call in all `VIEW_****()` functions

## [1.2.1] - 2023-08-12
### Added
+ **`DCK`** : Add `os.cpu_count()` to determine number of cpu cores available for `--cpu` parameter
+ **`DCK`** : Add `--cpu` parameter in `%vina` to maximise CPU resource

### Changed
+ **`DSC`** : Rename **`LABOGRID`** to **[`LaBOX`](https://github.com/RyanZR/LaBOX)**
+ **`PKG`** : Update packages: `py3Dmol 2.0.3`, `rdkit-pypi 2022.9.5`, `biopython 1.80`, `openbabel 3.1.1`, `zlib 1.2.13`
+ **`SRC`** : Update `mamba` installation process

### Fixed
+ **`VIS`** : Fix incomplete visualisation of binding interactions in `VIEW_PILE()` function

### Removed
+ **`SRC`** : Remove unused space characters to improve PEP8 compliance

## [1.2.0] - 2023-02-12
This update primarily focuses on improvements to [virtual_screening.ipynb](./notebooks/virtual_screening.ipynb)

### Added 
+ **`GBX`** : Add 5 new methods for defining grid box
+ **`VIS`** : Add `showHs` argument in `VIEW_LIG()`

### Fixed 
+ **`DSC`** : Correct several spellings mistake

### Removed
+ **`VIS`** : Remove `AllChem.MMFFOptimizeMolecule()` in `VIEW_LIG()`

## [1.1.0] - 2023-02-12
This update primarily focuses on improvements to [basic_molecular_docking.ipynb](./notebooks/basic_molecular_docking.ipynb)

### Added 
+ **`GBX`** : Add 5 new methods for defining grid box
+ **`VIS`** : Add `showHs` argument in `VIEW_LIG()`

### Removed
+ **`VIS`** : Remove `AllChem.MMFFOptimizeMolecule()` in `VIEW_LIG()`
+ **`VIS`** : Remove `showBestPose` argument in `VIEW_PILE()`

## [1.0.0] - 2023-02-08
### Added
+ Add [basic_molecular_docking.ipynb](./notebooks/basic_molecular_docking.ipynb) to supersede [🍊MOUNTAIN_V2.ipynb](./deprecated/%F0%9F%8D%8AMOUNTAIN_V2.ipynb)
+ Add [virtual_screening.ipynb](./notebooks/virtual_screening.ipynb) to supersede [🍊UNION_V2.ipynb](./deprecated/%F0%9F%8D%8AUNION_V2.ipynb)
+ Add binding interaction analysis (PLIP) into both [basic_molecular_docking.ipynb](./notebooks/basic_molecular_docking.ipynb) and [virtual_screening.ipynb](./notebooks/virtual_screening.ipynb)

### Deprecated
+ Deprecate [🍊MOUNTAIN_V2.ipynb](./deprecated/%F0%9F%8D%8AMOUNTAIN_V2.ipynb)
+ Deprecate [🍊UNION_V2.ipynb](./deprecated/%F0%9F%8D%8AUNION_V2.ipynb)
+ Deprecate [🍊PLIA_V2.ipynb](./deprecated/%F0%9F%8D%8APLIA_V2.ipynb)

## [0.0.0] - 2022-09-21
Initial commit. 

## Abbreviations
**`PKG`** : Packages, **`ENV`** : Environment, **`SRC`** : Source code, **`DSC`** : Description, **`PRE`** : Preparation, **`ENM`** : Energy minimisation, **`GBX`** : Grid box , **`DCK`** : Docking, **`INT`** : Binding interactions, **`RMS`** : RMSD, **`ANL`** : Analysis, **`VIS`** : Visualisation

[unreleased]: https://github.com/RyanZR/labodock/compare/v2.0.0...HEAD
[2.0.0]: https://github.com/RyanZR/labodock/compare/v1.2.2...v2.0.0
[1.2.2]: https://github.com/RyanZR/labodock/commit/07cc2ff324e0b23f82e8b28083da4a3068d520fe
[1.2.1]: https://github.com/RyanZR/labodock/commit/d394697a6d60041c5a0d2d358a1a6340eeace339
[1.2.0]: https://github.com/RyanZR/labodock/commit/8bca3ac5edea7edd52448ba96ead01f1986606fb
[1.1.0]: https://github.com/RyanZR/labodock/commit/253fab528c1fc1f0b876a85fdf655338eb5cec6e
[1.0.0]: https://github.com/RyanZR/labodock/commit/3b2805bf781e6a68ac33112b58a308edbdea5913
[0.0.0]: https://github.com/RyanZR/labodock/commit/dd4a6b77f7da21770a2c11a20eda40f2ee2e2059
