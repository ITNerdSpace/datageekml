---
layout: post
published: true
author: Alexandre Dumont
last_modified_at: '2019-04-07 14:17 +0200'
title: Fast.AI installation on Windows
tags:
  - Automaton
  - MachineLearning
---
## Notes on installing Fast.AI on Windows

This are notes I've taken about installing Fast.ai 0.7.0 on Windows in Anaconda.

In Anaconda, I have already create a new environment called fastai07. Activate it, for example in Anaconda Prompt with:

```nosynthax
conda activate fastai07
```

### Update pip & conda

Before we start, let's make sure we are at the latest version of pip and conda:

```nosynthax
pip install pip -U
conda update -n base conda
```

### Install Fast.ai

Fast.ai documentation is the right starting point:
- On Github https://github.com/fastai/fastai/blob/master/README.md#installation
- Some Installation Extras https://docs.fast.ai/install.html
- **Special instructions for fast.ai 0.7** are here: https://forums.fast.ai/t/fastai-v0-install-issues-thread/24652
- Instalation on Windows: https://forums.fast.ai/t/howto-installation-on-windows/10439

If you don’t have any NVIDIA GPU, build the fastai-cpu environment using this:

```nosynthax
git clone https://github.com/fastai/fastai.git
cd fastai
conda env create -f environment-cpu.yml
```

Then activate the new environment with:

```nosynthax
conda activate fastai-cpu
```

### Replace symlinks

For those doing the Machine Learning course, replace the linux symlink with a Windows one (this may require an admin command prompt if you don’t have a fully updated version of Windows 10):

```nosynthax
cd courses\ml1
del fastai
mklink /d fastai ..\..\old\fastai
```

### Other stuffs

We can install JupyterLab:

```nosynthax
conda install jupyterlab
```

### How to run?

From the courses/ml1 folder, launch "jupyter lab" and you can open the notebooks and run them :)
