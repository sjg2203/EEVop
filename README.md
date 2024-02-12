# SleeVop
<img src="./docs/SleeVop_logo.png" width="300"/>

[![PyPI - Version](https://img.shields.io/pypi/v/SleeVop?logo=pypi)](https://pypi.python.org/pypi/SleeVop)
[![Conda (channel only)](https://img.shields.io/conda/vn/conda-forge/SleeVop?logo=anaconda&color=green)](https://anaconda.org/conda-forge/SleeVop)
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/SleeVop.svg?logo=python)](https://pypi.python.org/pypi/SleeVop)
[![License](https://img.shields.io/github/license/sjg2203/SleeVop?logo=apache)](https://github.com/sjg2203/SleeVop/blob/main/LICENSE)
[![Security: bandit](https://img.shields.io/badge/security-bandit-yellow.svg)](https://github.com/PyCQA/bandit)
[![PyPI - Status](https://img.shields.io/pypi/status/SleeVop)](https://pypi.python.org/pypi/SleeVop)
[![Hit](https://img.shields.io/endpoint?url=https%3A%2F%2Fhits.dwyl.com%2Fsjg2203%2FSleeVop.svg&color=red)](http://hits.dwyl.com/sjg2203/SleeVop)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

[SleeVop](https://github.com/sjg2203/SleeVop) (sleep envelope synchronisation) toolbox analyses EEG envelopes to compare them to reference envelopes.

The toolbox is optimised for Python 3.10 and above and was tested on both Windows and macOS ARM.

> [!NOTE]
> All dependencies are listed in [requirements](docs/requirements.txt), Python 3.10 minimum.

## Citation [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10651391.svg)](https://doi.org/10.5281/zenodo.10651391)

If you use this toolbox, please cite as followed:

 - Guillot, S.J.<a id="cy-effective-orcid-url" class="underline" href="https://orcid.org/0000-0002-1623-7091" target="orcid.widget" rel="me noopener noreferrer" style="vertical-align: top"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width: 1em; margin-inline-start: 0.5em" alt="ORCID"/></a> (2023). SleeVop (2023.04.03-post1). GitHub, Zenodo. https://doi.org/10.5281/zenodo.10651391

## Contribution [![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/sjg2203/SleeVop/issues)

These pipelines were created and is maintained by SJG.

Contributions are more than welcome so feel free to submit a [pull request](https://github.com/sjg2203/SleeVop/pulls)!

To report a bug, please open a new [issue](https://github.com/sjg2203/SleeVop/issues).

Note that this program is provided with NO WARRANTY OF ANY KIND under Apache 2.0 [license](LICENSE).

## Installation of Python package

To install the toolbox, simply use:

- Using conda [![Board Status](https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/ssp_detector-feedstock?branchName=main)](https://anaconda.org/conda-forge/SleeVop)

```python
conda install -c cf-staging sleevop
```

- Using pip [![Pypi package](https://github.com/sjg2203/SleeVop/actions/workflows/pypi_publish.yml/badge.svg?branch=main)](https://github.com/sjg2203/SleeVop/actions/workflows/pypi_publish.yml) [![PyPI - Wheel](https://img.shields.io/pypi/wheel/SleeVop)](https://pypi.python.org/pypi/SleeVop)

```python
pip install sleevop
```

Everything worked if the following command do not return any error:

```python
import mne
from sleevop import sleep_env
from tkinter import filedialog as fd

#Load an EDF file using MNE
edf_ref=fd.askopenfilename(title='SELECT EDF FILE',filetypes=(("EDF files","*.edf"),("all files","*.*")))
edf_test=fd.askopenfilename(title='SELECT EDF FILE',filetypes=(("EDF files","*.edf"),("all files","*.*")))
raw_ref=mne.io.read_raw_edf(edf_ref,preload=True)
raw_test=mne.io.read_raw_edf(edf_test,preload=True)
sfreq=raw_ref.info['sfreq']

#Return sleep envelope synchronisation and latency
sleep_env(raw_ref,raw_test,sf=sfreq,start='min',stop='max')
```
