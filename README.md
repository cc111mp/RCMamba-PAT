# RCMamba-PAT

Official PyTorch implementation of:

**Wavelet-Enhanced Residual Optimal Transport for Mamba-Based Image Restoration in Photoacoustic Tomography**  
Simon C. K. Chan, Bingxin Huang, Hannah H. Kim, Victor T. C. Tsang, Terence T. W. Wong  
*Photoacoustics*, 2025  

[Paper](https://doi.org/10.1016/j.pacs.2025.100749)

---

## Introduction

This repository provides the implementation of **Residual Condition Optimal Transport Mamba (RCMamba)** for sparse photoacoustic tomography (PAT) image restoration.

RCMamba is designed to reconstruct high-quality PAT images from sparse-view measurements. The framework combines wavelet-enhanced residual optimal transport with a hybrid multi-scale Mamba backbone to suppress streak artifacts while preserving fine anatomical details and long-range structural information.

---

## Highlights

- Wavelet residual-enhanced transport plan for sparse-view PAT restoration.
- Hybrid multi-scale Mamba architecture with local and global state-space scanning.
- Designed for sparse acquisition settings such as 16, 32, and 64 projections.
- Evaluated on vessel phantom and in vivo mouse model reconstruction tasks.

---

## Results

Quantitative results and visual comparisons will be added with the full code release.

| Method | Sparse 16 | Sparse 32 | Sparse 64 |
|---|---|---|---|
| RCMamba | Coming soon | Coming soon | Coming soon |

---

## Installation

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

```bash
python test.py \
  --config configs/rcmamba_16.yml \
  --checkpoint checkpoints/rcmamba_16.pth
```

---

## Pretrained Models

| Model | Setting | Link |
|---|---|---|
| RCMamba | 16 projections | Coming soon |
| RCMamba | 32 projections | Coming soon |
| RCMamba | 64 projections | Coming soon |

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
