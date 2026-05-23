# RCMamba-PAT

Official PyTorch implementation of:

**Wavelet-Enhanced Residual Optimal Transport for Mamba-Based Image Restoration in Photoacoustic Tomography**  
Simon C. K. Chan, Bingxin Huang, Hannah H. Kim, Victor T. C. Tsang, Terence T. W. Wong  
*Photoacoustics*, 2025  

[Paper](https://doi.org/10.1016/j.pacs.2025.100749)

---

## Overview

**RCMamba** restores sparse-view photoacoustic tomography (PAT) images by combining wavelet-enhanced residual optimal transport with a hybrid multi-scale Mamba backbone. The method targets streak-artifact suppression, fine-detail recovery, and long-range structural preservation under sparse acquisition.

This repository is prepared as the release page for the paper implementation. Source code, configs, checkpoints, and full reproduction commands will be added with the code release.

---

## At A Glance

| Item | Description |
|---|---|
| Task | Sparse-view PAT image restoration |
| Inputs | Sparse-view reconstructions from 16, 32, and 64 projections |
| Targets | Dense-view PAT reconstructions |
| Core method | Wavelet-enhanced residual optimal transport + hybrid multi-scale Mamba |
| Evaluation | Vessel phantom and in vivo mouse model experiments |
| Metrics | PSNR / SSIM |

---

## Highlights

- Wavelet-enhanced residual transport for sparse-view artifact modeling.
- Wavelet coherence regularization for frequency-aware restoration.
- Hybrid Mamba backbone with local and global state-space scanning.
- Restoration pipeline for 16, 32, and 64 projection sparse PAT settings.

---

## Release Status

| Component | Status |
|---|---|
| Paper link | Available |
| Repository scaffold | Available |
| Citation metadata | Available |
| Dependency entry point | Placeholder available |
| Source code | Preparing for release |
| Training / testing configs | Preparing for release |
| Pretrained checkpoints | Preparing for release |
| Results table and figures | Preparing for release |

---

## Repository Layout

```bash
.
|-- README.md
|-- CITATION.cff
|-- requirements.txt
|-- assets/
|-- checkpoints/
|-- configs/
|-- data/
|-- docs/
`-- src/
```

Each release directory currently contains a placeholder README so the intended structure is explicit before the full source code is published.

---

## Installation

The following setup will be used after the source code is released:

```bash
git clone https://github.com/cc111mp/RCMamba-PAT.git
cd RCMamba-PAT

conda create -n rcmamba python=3.9 -y
conda activate rcmamba

pip install -r requirements.txt
```

---

## Dataset

Expected data layout:

```bash
data/
|-- train/
|   |-- input/
|   `-- target/
|-- val/
|   |-- input/
|   `-- target/
`-- test/
    |-- input/
    `-- target/
```

Sparse inputs correspond to 16, 32, or 64 projection reconstructions. Targets correspond to dense-view reconstructions.

---

## Quick Start

Example commands for the planned release:

```bash
python test.py \
  --config configs/rcmamba_16.yml \
  --checkpoint checkpoints/rcmamba_16.pth
```

```bash
python train.py --config configs/rcmamba_16.yml
```

---

## Main Results

Quantitative results and visual comparisons will be added with the full code release.

| Model | Sparse setting | PSNR | SSIM | Checkpoint |
|---|---:|---:|---:|---|
| RCMamba | 16 projections | Preparing for release | Preparing for release | Preparing for release |
| RCMamba | 32 projections | Preparing for release | Preparing for release | Preparing for release |
| RCMamba | 64 projections | Preparing for release | Preparing for release | Preparing for release |

---

## Model Zoo

| Model | Setting | Link |
|---|---|---|
| RCMamba | 16 projections | Preparing for release |
| RCMamba | 32 projections | Preparing for release |
| RCMamba | 64 projections | Preparing for release |

---

## Release Checklist

- [x] Repository page
- [x] Paper link
- [x] Repository scaffold
- [x] Citation metadata
- [x] Dependency entry point
- [ ] Source code
- [ ] Training and testing configs
- [ ] Pretrained checkpoints
- [ ] Quantitative results
- [ ] Visual comparison figures

---

## Citation

If you find this work useful, please cite:

```bibtex
@article{chan2025wavelet,
  title={Wavelet-enhanced residual optimal transport for Mamba-based image restoration in photoacoustic tomography},
  author={Chan, Simon C. K. and Huang, Bingxin and Kim, Hannah H. and Tsang, Victor T. C. and Wong, Terence T. W.},
  journal={Photoacoustics},
  volume={45},
  pages={100749},
  year={2025},
  doi={10.1016/j.pacs.2025.100749}
}
```

---

## Contact

For questions or updates, please open an issue in this repository.
