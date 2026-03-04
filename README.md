# Copenhagen Brain Entropy Toolbox - Python

**Brian Winston<sup>1,2</sup>, Viswanath Missula<sup>2</sup>, and Janice Chen<sup>2</sup>**

<sup>1</sup> *Center for Psychedelic and Consciousness Research, Johns Hopkins School of Medicine*

<sup>2</sup> *Department of Psychological and Brain Sciences, Johns Hopkins University*

A Python package/wrapper for the [Copenhagen Brain Entropy Toolbox (CopBET)](https://github.com/anders-s-olsen/CopBET), a collection of functions for evaluating 12 different entropy metrics described in the paper [Navigating the chaos of psychedelic neuroimaging: A multi-metric evaluation of acute psilocybin effects on brain entropy" by Drummond McCulloch, Anders S Olsen et al (MedRxiv)](https://www.medrxiv.org/content/10.1101/2023.07.03.23292164v1). All credit for entropy measures goes to the original authors (see MedRxiv).


## Installation guide

### 1. Create conda environment (recommended)

An `environment.yml` file is provided that includes all required dependencies except the MATLAB engine (which must match your MATLAB version). To create a conda environment:

1. Run:
   ```conda env create -n YOUR_ENV_NAME -f environment.yml``` replacing YOUR_ENV_NAME with whatever you want.
3. Activate the environment:
   ```conda activate YOUR_ENV_NAME```
4. Install the matching MATLAB engine for your MATLAB version (see table below)

### 2. Install dependencies

1. Install this package using

   ```pip install CopBET```

2. Install the MATLAB engine API for Python. **The `matlabengine` package version must match your MATLAB installation.** The version numbering follows the pattern `YY.V.x` where `YY` is the last two digits of the release year and `V` is the release number (1=a, 2=b). For example:

   | MATLAB version | pip install command |
   |---|---|
   | R2024b | `pip install matlabengine==24.2.2` |
   | R2024a | `pip install matlabengine==24.1.2` |
   | R2025b | `pip install matlabengine==25.2.2` |
   | R2025a | `pip install matlabengine==25.1.2` |

   To find the right version for your MATLAB, run `matlab -batch "disp(version)"` in a terminal and match the year and release letter. You can also browse all available versions on [PyPI](https://pypi.org/project/matlabengine/#history). For more details, see the [official MathWorks documentation](https://www.mathworks.com/help/matlab/matlab_external/install-the-matlab-engine-for-python.html).

3. Clone the original CopBET repository to your machine (although some of the helper functions will work fine without).

   ```git clone https://github.com/anders-s-olsen/CopBET.git```

### 3. Create a script to run the functions on your data
Included is an example script in the form of an iPython Notebook entitled [`CopBET_python_tutorial.ipynb`](https://github.com/HopkinsPsychedelic/CopBET_Python/blob/main/CopBET_python_tutorial.ipynb) showing examples and explanations of how to use the wrapper. The example script runs using the openly available [acute IV LSD dataset](https://openneuro.org/datasets/ds003059) that was included in original repository's example script. Unlike the original repository, the example was not written to be used on the entire original dataset but rather the smaller sample already in the /CopBET/LSDdata folder. 

### 4. Other dependencies
This package and wrapper was developed, tested, and implemented using Python 3.12 and 3.13.

This package runs using the MATLAB engine in the backend, so it has the same dependencies as the original toolbox. The toolbox works on MATLAB R2018b+ and is known to _not_ work on MATLAB R2017b due to the structuring of tables. You will also need to install the external dependencies Brain Connectivity toolbox (2019_03_03), the complexity toolbox (LOFT) and the DCC toolbox (the original one from 2014).

## Citation guide
If you use this toolbox in your research, please cite the following:

[insert DOI via Zenodo]

Drummond McCulloch, Anders S Olsen, et al. "Navigating the chaos of psychedelic neuroimaging: A multi-metric evaluation of acute psilocybin effects on brain entropy". (MedRxiv), 2023.

Original author of whichever entropy measure you used (e.g. if you use meta-state complexity, you should also cite Singleton et. al, 2022). See the MedRxiv paper for details on this. 

## Contributing/reporting bugs
If you would like to contribute, report any bugs or have any questions, please email Brian Winston (brian.winston@jhu.edu).

## Repo Version
1.0.0 March 2026 - initial commit.

## License
Copyright (C) 2023 Drummond E-Wen McCulloch & Anders Stevnhoved Olsen

```
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see http://www.gnu.org/licenses/.
```
