# ROOT training for STAR/EIC workshop

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/aprozo/binder_cern_root/main?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252Faprozo%252Froot_workshop%26urlpath%3Dtree%252Froot_workshop%252F%26branch%3Dmain)
[![Github Codespace](https://img.shields.io/badge/open-GH_Codespaces-blue?logo=github)](https://codespaces.new/aprozo/root_workshop?quickstart=1)

This is a self-contained tutorial for STAR/EIC workshop aimed at learning some ROOT basics

---
# How to start:
For running on Github Codespaces submit an application for Free [Github Education](https://github.com/education) benefits.
Then click on [Github Codespace button](https://codespaces.new/aprozo/root_workshop?quickstart=1)
 to start a container (predefined software environment).
 
### What is Jupyter notebook?
Start at [extra_jupyter.ipynb](extra_jupyter.ipynb) and optionally more detailed info [extra_jupyter_more.ipynb](extra_jupyter_more.ipynb)

## Physics tutorials:
- [00_Intro.ipynb](00_Intro.ipynb) what is ROOT
- [01_SimpleHistogramGraphFunction.ipynb](01_SimpleHistogramGraphFunction.ipynb) - basics of data representation - `Histograms`
- [02_ExcerciseCentralLimitTheorem.ipynb](02_ExcerciseCentralLimitTheorem.ipynb) - try using histogram in a simple experiment of Galton problem and then fit the distribution
- [03_TreesAndFiles.ipynb](03_TreesAndFiles.ipynb) - how to save data in file and read it after + optionally `RDataFrames`
- [04_InvariantMass.ipynb](04_InvariantMass.ipynb) - all tutorials combined and used for [OpenData](https://opendata.cern.ch/record/5203)  $J/\psi$ decaying to 2 muons - final boss tutorial

---

## What are files for:

- [.devcontainer](.devcontainer/) - special folder for running in Container (like Github Codespaces)
- [data](data/) - backup input data in case some problems
- [img](img/) - images used in notebooks
- [.gitignore](.gitignore) - special file for git (not to track)
- [.rootlogon](.rootlogon) - your own default style for CERN ROOT settings which loads after ROOT starts
- [00_* - 04_**.ipynb](00_Intro.ipynb) - actual tutorials
- [README.md](README.md) - current displayed text page
- [environment.yml](environment.yml) - container settings used for Binder
- [extra_*.ipynb](extra_jupyter.ipynb) - supplementary material for what is Jupyter Notebook

---

## I like to run it on my own system:

- Git clone this repo:

```bash
git clone https://github.com/aprozo/root_workshop
```

- One needs to install [ROOT](https://root.cern/install/)

- Then install some additional packages with

```bash
sudo apt-get update && apt-get install -y git python3-pip
python3 -m pip install --upgrade wheel jupyter metakernel dask distributed pyspark
```

- After it run

```bash
root --notebook
```

---

Part of the material has been reused from:

- https://github.com/root-project/training
- https://github.com/root-project/software-carpentry



If facing a problem with ROOT kernel [ROOT C++ kernel](https://github.com/root-project/root/tree/master/bindings/jupyroot), one has to run it in terminal

```bash
mkdir -p  ~/.local/share/jupyter/kernels
cp -r $ROOTSYS/etc/notebook/kernels/root ~/.local/share/jupyter/kernels
jupyter notebook --allow-root
```

Then, wait untill the page is reloaded and choose Jupyter Kernel -> ROOT
