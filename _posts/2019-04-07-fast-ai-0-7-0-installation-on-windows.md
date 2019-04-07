---
layout: post
published: false
author: Alexandre Dumont
last_modified_at: '2019-04-07 14:17 +0200'
title: Fast.ai 0.7.0 installation on Windows
---
## Notes on installing Fast.AI on Windows

This are notes I've taken about installing Fast.ai 0.7.0 on Windows in Anaconda.

In Anaconda, I have already create a new environment called fastai07. Activate it, for example in Anaconda Prompt with:

```
conda activate fastai07
```

### Update pip & conda

Before we start, let's make sure we are at the latest version of pip and conda:

```
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

```
git clone https://github.com/fastai/fastai.git
cd fastai
conda env create -f environment-cpu.yml
```

Then activate the new environment with:

```
conda activate fastai-cpu
```

### Other stuffs

We can install JupyterLab:


```
conda install jupyterlab
```

