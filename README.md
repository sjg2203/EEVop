# EEVop

<img src="./docs/EEVop_logo.png" width="300"/>

[![PyPI - Version](https://img.shields.io/pypi/v/EEVop?logo=pypi)](https://pypi.python.org/pypi/EEVop)
[![Conda (channel only)](https://img.shields.io/conda/vn/conda-forge/EEVop?logo=anaconda&color=green)](https://anaconda.org/conda-forge/EEVop)
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/EEVop.svg?logo=python)](https://pypi.python.org/pypi/EEVop)
[![License](https://img.shields.io/github/license/sjg2203/EEVop?logo=apache)](https://github.com/sjg2203/EEVop/blob/main/LICENSE)
[![Security: bandit](https://img.shields.io/badge/security-bandit-yellow.svg)](https://github.com/PyCQA/bandit)
[![PyPI - Status](https://img.shields.io/pypi/status/EEVop)](https://pypi.python.org/pypi/EEVop)
[![Hit](https://img.shields.io/endpoint?url=https%3A%2F%2Fhits.dwyl.com%2Fsjg2203%2FEEVop.svg&color=red)](http://hits.dwyl.com/sjg2203/EEVop)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)

[EEVop](https://github.com/sjg2203/EEVop) (EEG Envelope Synchronisation): a Python package to analyse sleep envelope synchronisation.

This package is optimised for Python 3.10 and above and was tested on both Windows and macOS ARM.

> [!NOTE]
> All dependencies are listed in [requirements](docs/requirements.txt), Python 3.10 minimum.

## Citation [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10651391.svg)](https://doi.org/10.5281/zenodo.10651391)

If you use this toolbox, please cite as follows:

- Guillot, S.J.<a id="cy-effective-orcid-url" class="underline" href="https://orcid.org/0000-0002-1623-7091" target="orcid.widget" rel="me noopener noreferrer" style="vertical-align: top"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width: 1em; margin-inline-start: 0.5em" alt="ORCID"/></a> (
  2023). EEVop (2023.04.03). GitHub, Zenodo. https://doi.org/10.5281/zenodo.10651391

This work is based on the following paper, citing it should be considered:

- Ujma, P.P., Dresler, M., Simor, P. <i>et al.</i> The sleep EEG envelope is a novel, neuronal firing-based human
  biomarker. <i>Sci Rep</i> <b>12</b>, 18836 (2022). https://doi.org/10.1038/s41598-022-22255-4

## Contribution [![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/sjg2203/EEVop/issues)

These pipelines were created and maintained by SJG.

Contributions are welcome, so feel free to submit a [pull request](https://github.com/sjg2203/EEVop/pulls)!

To report a bug, please open a new [issue](https://github.com/sjg2203/EEVop/issues).

Note that this program is provided with NO WARRANTY OF ANY KIND under Apache 2.0 [license](LICENSE).

## Installation of Python package

To install the toolbox, use:

- Using
  conda [![Board Status](https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/ssp_detector-feedstock?branchName=main)](https://anaconda.org/conda-forge/EEVop)

```python
conda install-c cf-staging eevop
```

- Using
  pip [![Pypi package](https://github.com/sjg2203/EEVop/actions/workflows/pypi_publish.yml/badge.svg?branch=main)](https://github.com/sjg2203/EEVop/actions/workflows/pypi_publish.yml) [![PyPI - Wheel](https://img.shields.io/pypi/wheel/EEVop)](https://pypi.python.org/pypi/EEVop)

```python
pip install eevop
```
