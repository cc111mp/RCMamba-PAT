# RCMamba-PAT

Official PyTorch implementation of:

**Wavelet-Enhanced Residual Optimal Transport for Mamba-Based Image Restoration in Photoacoustic Tomography**  
Simon C. K. Chan, Bingxin Huang, Hannah H. Kim, Victor T. C. Tsang, Terence T. W. Wong  
*Photoacoustics*, 2025  

[Paper](https://doi.org/10.1016/j.pacs.2025.100749)

---

## Overview

This repository provides the implementation of **Residual Condition Optimal Transport Mamba (RCMamba)** for sparse photoacoustic tomography (PAT) image restoration.

RCMamba is designed to reconstruct high-quality PAT images from sparse-view measurements. The framework combines wavelet-enhanced residual optimal transport with a hybrid multi-scale Mamba backbone to suppress streak artifacts while preserving fine anatomical details and long-range structural information.

PAT provides optical-absorption contrast with ultrasonic detection, but sparse acquisition can introduce strong streak artifacts. RCMamba addresses this restoration problem by combining frequency-aware residual transport with state-space modeling, targeting both artifact removal and structural fidelity.

---

## Release Status

The repository page is being prepared for the full code release.

| Component | Status |
|---|---|
| Paper link | Available |
| Source code | Preparing for release |
| Training and testing configs | Preparing for release |
| Quantitative results table | Preparing for release |
| Visual comparison figures | Preparing for release |
| Pretrained checkpoints | Preparing for release |

---

## Paper Details

| Item | Description |
|---|---|
| Task | Sparse-view PAT image restoration |
| Input setting | Sparse-view reconstructions from 16, 32, and 64 projections |
| Target setting | Dense-view PAT reconstruction |
| Core method | Wavelet-enhanced residual optimal transport with a hybrid multi-scale Mamba backbone |
| Evaluation data | Vessel phantom and in vivo mouse model experiments |
| Main focus | Artifact suppression, fine-detail recovery, and long-range structural preservation |

---

## Highlights

- Wavelet residual-enhanced transport plan for sparse-view PAT restoration.
- Hybrid multi-scale Mamba architecture with local and global state-space scanning.
- Restoration pipeline designed for sparse acquisition settings such as 16, 32, and 64 projections.
- Evaluation on vessel phantom and in vivo mouse model reconstruction tasks.

---

## Key Ideas

- **Wavelet-enhanced residual transport:** Uses multi-resolution wavelet analysis to model scale-dependent sparse-view artifacts.
- **Wavelet coherence regularization:** Encourages consistency in frequency-aware residual restoration.
- **Hybrid multi-scale Mamba backbone:** Combines window-based and global state-space scanning for local detail and long-range structure.
- **Sparse-sampling restoration:** Targets diagnostically useful PAT reconstruction when acquisition views are limited.

---

## Method Summary

RCMamba restores sparse-view PAT images through a residual learning strategy guided by optimal transport. The wavelet-enhanced residual formulation helps model high-frequency details and artifact patterns, while the Mamba-based restoration backbone captures both local image structures and long-range spatial dependencies.

The full implementation will include model definitions, configuration files, training scripts, testing scripts, and pretrained checkpoints.

---

## Keywords

Photoacoustic tomography, sparse-view reconstruction, image restoration, state space models, Mamba, optimal transport, wavelet analysis, deep learning.

---

## Results

Quantitative results and visual comparisons will be added together with the full code release.

| Model | Sparse setting | Metrics | Status |
|---|---|---|---|
| RCMamba | 16 projections | PSNR / SSIM | Preparing for release |
| RCMamba | 32 projections | PSNR / SSIM | Preparing for release |
| RCMamba | 64 projections | PSNR / SSIM | Preparing for release |

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

Please organize the dataset as follows:

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

The sparse input images are reconstructed from 16, 32, or 64 projections.  
The target images are reconstructed from dense-view measurements.

---

## Training

Example training commands for the planned release:

```bash
python train.py --config configs/rcmamba_16.yml
```

For other sparse settings:

```bash
python train.py --config configs/rcmamba_32.yml
python train.py --config configs/rcmamba_64.yml
```

---

## Testing

Example testing command for the planned release:

```bash
python test.py \
  --config configs/rcmamba_16.yml \
  --checkpoint checkpoints/rcmamba_16.pth
```

---

## Pretrained Models

| Model | Setting | Link |
|---|---|---|
| RCMamba | 16 projections | Preparing for release |
| RCMamba | 32 projections | Preparing for release |
| RCMamba | 64 projections | Preparing for release |

---

## Release Checklist

- [x] Repository page
- [x] Paper link
- [ ] Source code
- [ ] Environment file
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
