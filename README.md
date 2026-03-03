# Copenhagen Brain Entropy Toolbox - Python

**Brian Winston<sup>1,2</sup>, Viswanath Missula<sup>2</sup>, and Janice Chen<sup>2</sup>**

<sup>1</sup> *Center for Psychedelic and Consciousness Research, Johns Hopkins School of Medicine*

<sup>2</sup> *Department of Psychological and Brain Sciences, Johns Hopkins University*

A Python package/wrapper for the [Copenhagen Brain Entropy Toolbox (CopBET)](https://github.com/anders-s-olsen/CopBET), a collection of functions for evaluating 12 different entropy metrics described in the paper [Navigating the chaos of psychedelic neuroimaging: A multi-metric evaluation of acute psilocybin effects on brain entropy" by Drummond McCulloch, Anders S Olsen et al (MedRxiv)](https://www.medrxiv.org/content/10.1101/2023.07.03.23292164v1). 


## Installation guide
To use this package follow the steps below.
1. Install this package using

   ```pip install CopBET```

2. [Install the MATLAB engine API for Python](https://www.mathworks.com/help/matlab/matlab_external/install-the-matlab-engine-for-python.html).

3. Clone the original CopBET repository to your machine (although some of the helper functions will work just fine without).

   ```git clone https://github.com/anders-s-olsen/CopBET.git```

## Example script
Included is an example iPython Notebook entitled `CopBET_python_tutorial.ipynb` showing examples and explanations of how to use the wrapper. The example script runs using the openly available [acute IV LSD dataset](https://openneuro.org/datasets/ds003059) that was included in original repository's example script. Unlike the original repository, the example was not written to be used on the entire original dataset but rather the smaller sample already in the /CopBET/LSDdata folder. We recommend that you make a script or notebook analogous to this one for your own dataset.

## Python versions and dependencies
This package and wrapper was developed, tested, and implemented using 3.12 and 3.13.

## MATLAB versions and dependencies
This package runs using the MATLAB engine in the backend, so it has the same dependencies as the original toolbox. The toolbox works on MATLAB R2018b+ and is known to _not_ work on MATLAB R2017b due to the structuring of tables. You will also need to install the external dependencies Brain Connectivity toolbox (2019_03_03), the complexity toolbox (LOFT) and the DCC toolbox (the original one from 2014).

## Contributing/reporting bugs
If you would like to contribute, report any bugs or have any questions, please email Brian Winston (brian.winston@jhu.edu) and/or Viswanath Missula (vmissul1@jh.edu). 

## References
If you use this toolbox in your research, please cite both the following:

[insert DOI via Zenodo]

Drummond McCulloch, Anders S Olsen, et al. "Navigating the chaos of psychedelic neuroimaging: A multi-metric evaluation of acute psilocybin effects on brain entropy". (MedRxiv), 2023.

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
