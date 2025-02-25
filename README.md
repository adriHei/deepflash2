# Welcome too



![deepflash2](https://raw.githubusercontent.com/matjesg/deepflash2/master/nbs/media/logo/logo_deepflash2_transp-02.png)

Official repository of deepflash2 - a deep learning pipeline for segmentation of fluorescent labels in microscopy images.

![CI](https://github.com/matjesg/deepflash2/workflows/CI/badge.svg) 
[![PyPI](https://img.shields.io/pypi/v/deepflash2?color=blue&label=pypi%20version)](https://pypi.org/project/deepflash2/#description) 
[![PyPI - Downloads](https://img.shields.io/pypi/dm/deepflash2)](https://pypistats.org/packages/deepflash2)
[![Conda (channel only)](https://img.shields.io/conda/vn/matjesg/deepflash2?color=seagreen&label=conda%20version)](https://anaconda.org/matjesg/deepflash2) 
[![Build fastai images](https://github.com/matjesg/deepflash2/workflows/Build%20deepflash2%20images/badge.svg)](https://github.com/matjesg/deepflash2)
[![GitHub stars](https://img.shields.io/github/stars/matjesg/deepflash2?style=social)](https://github.com/matjesg/deepflash2/)
[![GitHub forks](https://img.shields.io/github/forks/matjesg/deepflash2?style=social)](https://github.com/matjesg/deepflash2/)
***

## Quick Start in 30 seconds

[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/matjesg/deepflash2/blob/master/deepflash2_GUI.ipynb)

![deepflash2 training getting started](https://raw.githubusercontent.com/matjesg/deepflash2/master/nbs/media/screen_captures/GUI_Train_start.gif)

Examplary training workflow.

## Why using deepflash2?

__The best of two worlds:__
Combining state of the art deep learning with a barrier free environment for life science researchers.

- End-to-end process for life science researchers
    - graphical user interface - no coding skills required
    - free usage on _Google Colab_ at no costs
    - easy deployment on own hardware
- Rigorously evaluated deep learning models
    - Model Library
    - easy integration new (*pytorch*) models
- Best practices model training
    - leveraging the _fastai_ library
    - mixed precision training
    - learning rate finder and fit one cycle policy 
    - advanced augementation 
- Reliable prediction on new data
    - leveraging Bayesian Uncertainties

**Kaggle Gold Medal and Innovation Price Winner**

*deepflash2* does not only work on fluorescent labels. The *deepflash2* API built the foundation for winning the [Innovation Award](https://hubmapconsortium.github.io/ccf/pages/kaggle.html) a Kaggle Gold Medal in the [HuBMAP - Hacking the Kidney](https://www.kaggle.com/c/hubmap-kidney-segmentation) challenge. 
Have a look at our [solution](https://www.kaggle.com/matjes/hubmap-deepflash2-judge-price)

![Gold Medal](https://www.kaggle.com/static/images/medals/competitions/goldl@1x.png)


## Citing

We're working on a peer reviewed publication. Until than, the preliminary citation is:

```
@misc{griebel2021deepflash2,
  author = {Matthias Griebel},
  title = {DeepFLasH2 - a deep learning pipeline for segmentation of fluorescent labels in microscopy images},
  year = {2021},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/matjesg/deepflash2}}
}
```

## Workflow

tbd

## Installing

You can use **deepflash2** by using [Google Colab](colab.research.google.com). You can run every page of the [documentation](matjesg.github.io/deepflash2/) as an interactive notebook - click "Open in Colab" at the top of any page to open it.
 - Be sure to change the Colab runtime to "GPU" to have it run fast!
 - Use Firefox or Google Chrome if you want to upload your images.

You can install **deepflash2**  on your own machines with conda (highly recommended):

```bash
conda install -c fastai -c pytorch -c matjesg deepflash2 
```
To install with pip, use

```bash
pip install deepflash2
```
If you install with pip, you should install PyTorch first by following the PyTorch [installation instructions](https://pytorch.org/get-started/locally/).

## Using Docker

Docker images for __deepflash2__ are built on top of [the latest pytorch image](https://hub.docker.com/r/pytorch/pytorch/) and [fastai](https://github.com/fastai/docker-containers) images. **You must install [Nvidia-Docker](https://github.com/NVIDIA/nvidia-docker) to enable gpu compatibility with these containers.**

- CPU only
> `docker run -p 8888:8888 matjesg/deepflash`
- With GPU support ([Nvidia-Docker](https://github.com/NVIDIA/nvidia-docker) must be installed.)
has an editable install of fastai and fastcore.
> `docker run --gpus all -p 8888:8888 matjesg/deepflash`
All docker containers are configured to start a jupyter server. **deepflash2** notebooks are available in the `deepflash2_notebooks` folder.

For more information on how to run docker see [docker orientation and setup](https://docs.docker.com/get-started/) and [fastai docker](https://github.com/fastai/docker-containers).

## Model Library

We provide a model library with pretrained model weights. Visit our [model library documentation](https://matjesg.github.io/deepflash2/model_library.html) for information on the datasets of the pretrained models.

## Creating segmentation masks with Fiji/ImageJ

If you don't have labelled training data available, you can use this [instruction manual](https://github.com/matjesg/DeepFLaSH/raw/master/ImageJ/create_maps_howto.pdf) for creating segmentation maps.
The ImagJ-Macro is available [here](https://raw.githubusercontent.com/matjesg/DeepFLaSH/master/ImageJ/Macro_create_maps.ijm).

## Acronym

A Deep-learning pipeline for Fluorescent Label Segmentation that learns from Human experts
