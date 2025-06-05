# Untitled

## Introduction

This repository contains Jupyter Notebooks for experimenting with **Model Inversion Attacks** and various **Defense** methods on MRI images using WGAN-GP. Each notebook corresponds to a specific step:

- **wgan-mri.ipynb**: WGAN-GP for generating MRI images (no defense)
- **model-inversion-attack-gmi.ipynb**: Perform GMI (**Generative Model-Inversion Attacks Against Deep Neural Networks**) attack
- **wgan-mri-autoencoder-defend.ipynb**: WGAN + Autoencoder Purifier
- **wgan-mri-dp-defense.ipynb**: WGAN + Differential Privacy Defense
- **wgan-mri-gradient-clipping.ipynb**: WGAN + Gradient Clipping Defense
- **Mutual_Information_Regularization_based_Defense.ipynb**: WGAN + Mutual Information Regularization based Defense

---

## Requirements

- GPU (>4GB VRAM)
- RAM >25GB

---

## Datasets

1. **MRI Dataset (for WGAN & Defense)**[https://www.kaggle.com/datasets/nhtphmm/mri-dataset](https://www.kaggle.com/datasets/nhtphmm/mri-dataset)
- Used to train WGAN-GP and the defense methods.
1. **DataMRI (for GMI Attack)**[https://www.kaggle.com/datasets/phamquanuet/datamri](https://www.kaggle.com/datasets/phamquanuet/datamri)
- Used to train or fine-tune the GMI model.

> How to download? (Kaggle API)
> 
> 
> ```bash
> kaggle datasets download -d nhtphmm/mri-dataset --unzip -p ./data/mri-dataset
> kaggle datasets download -d phamquanuet/datamri --unzip -p ./data/datamri
> 
> ```
> 

---

## Checkpoints

Each notebook requires a pretrained checkpoint, which should be placed in the **root folder**:

1. **WGAN-GP** (`wgan-mri.ipynb`)
    - Download checkpoint from [link](https://www.kaggle.com/datasets/nhtphmm/wgan-gp-mri-e230)
2. **GMI Attack** (`model-inversion-attack-gmi.ipynb`)
    - Download checkpoint from [link](https://www.kaggle.com/code/vanthan04/model-inversion-attack-gmi/output?select=prior_amp_ep50.pth)
3. **Autoencoder Purifier** (`wgan-mri-autoencoder-defend.ipynb`)
    - Download checkpoint from [link](https://drive.google.com/file/d/1OwcuwwiGFEUCqHZ9n_pc16nzShkDw8VV/view?usp=sharing)
4. **Differential Privacy (DP-inspired)** (`wgan-mri-dp-defense.ipynb`)
    - Download checkpoint from [link](https://drive.google.com/file/d/11HyWiKMb8Gpjx7I4UiLj_mgTxZCGQfrW/view?usp=sharing) and save
5. **Gradient Clipping** (`wgan-mri-gradient-clipping.ipynb`)
    - Download checkpoint from [link](https://drive.google.com/file/d/1LCpsf649ku-GIm_Nugna_gJJeZREbVgt/view?usp=drive_link) and save
6. **Mutual information regularization based defense** (`Mutual_Information_Regularization_based_Defense.ipynb`)
    - Download checkpoint from [link](https://drive.google.com/file/d/1xsGY_zPAE4rqt3NMDJ5P_ShaGTNNvCmx/view) and save

---

## Quick Start

1. **Clone** the repository:

```bash
git 
cd REPO_NAME
```

RUN ALL