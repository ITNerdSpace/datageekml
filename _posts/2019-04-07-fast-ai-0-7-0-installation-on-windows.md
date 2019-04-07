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

### Install PyTorch

Head to [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/), adjust parameters, for example like this:

![2019-04-07 14_19_13-Start Locally _ PyTorch.png]({{site.baseurl}}/images/2019-04-07 14_19_13-Start Locally _ PyTorch.png)

Run the command line the page gives us:

```
conda install pytorch torchvision cudatoolkit=9.0 -c pytorch
```

