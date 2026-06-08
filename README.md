# SSM-PixNav: State Space Models for Pixel-Guided Embodied Navigation

<p align="center">
  <img src="assets/ssm_pixnav_overview.png" width="800">
</p>

## SSM-PixNav: State Space Models for Pixel-Guided Embodied Navigation

This repository contains the official implementation of **SSM-PixNav**, a State Space Model (SSM)-based framework for pixel-guided embodied navigation.

Pixel-guided navigation enables an embodied agent to navigate toward a target specified by a single image observation rather than semantic labels or object categories. Existing approaches primarily rely on Transformer-based sequence modeling, which can become computationally expensive when processing long visual trajectories. SSM-PixNav investigates whether modern State Space Models can provide a more efficient and scalable alternative for embodied navigation while maintaining strong navigation performance.

Our approach replaces the Transformer policy backbone with a State Space Model architecture, enabling efficient long-horizon temporal reasoning over visual observations. We evaluate the method in Habitat environments under both seen and unseen scenes and compare against existing Pixel Navigation baselines.

This is the official implementation of the paper. Please refer to the paper for detailed methodology, experiments, and analysis.

---

## Features

* State Space Model policy for pixel-guided navigation
* Efficient long-horizon trajectory modeling
* Habitat-Sim and Habitat-Lab support
* Evaluation on HM3D and MP3D environments
* Support for pretrained checkpoints
* Reproducible benchmarking pipeline

---

## Dependencies

Our implementation is based on Habitat-Sim and Habitat-Lab.

Please install:

* Python >= 3.10
* PyTorch
* Habitat-Sim
* Habitat-Lab
* NumPy
* OpenCV
* tqdm
* torchvision
* einops
  

Make sure the following datasets are downloaded and configured correctly:

* HM3D
* Matterport3D (MP3D)
* Pixel Navigation episode datasets

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<username>/SSM-PixNav.git
cd SSM-PixNav
```

Create environment:

```bash
conda create -n ssm_pixnav python=3.10
conda activate ssm_pixnav
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Install Habitat:

```bash
pip install habitat-sim
pip install habitat-lab
```

'''---

## Repository Structure

```text
SSM-PixNav/
│
├── configs/
├── datasets/
├── checkpoints/
├── policies/
│   ├── ssm_policy.py
│   └── visual_encoder.py
├── trainers/
├── evaluation/
├── scripts/
└── README.md
```

---

## Pretrained Checkpoints

Pretrained checkpoints will be released upon publication.

| Model      | Dataset | Checkpoint  |
| ---------- | ------- | ----------- |
| SSM-PixNav | HM3D    | Coming Soon |
| SSM-PixNav | MP3D    | Coming Soon |

Place downloaded checkpoints inside:

```text
checkpoints/
```

---

## Training

Train the SSM navigation policy:

```bash
python train.py \
    --config configs/ssm_pixnav.yaml
```

---

## Evaluation

Evaluate the trained policy:

```bash
python evaluate.py \
    --checkpoint checkpoints/ssm_pixnav.ckpt
```

---

## Metrics

We report standard embodied navigation metrics:

* Success Rate (SR)
* SPL
* Distance-to-Goal (DTG)
* SoftSPL
* Episode Length

---'''

## Results

| Method            | SR ↑ | SPL ↑ | DTG ↓ |
| ----------------- | ---- | ----- | ----- |
| PixelNav Baseline | TBD  | TBD   | TBD   |
| SSM-PixNav        | TBD  | TBD   | TBD   |

---

## Acknowledgements

This project builds upon:

* Habitat-Sim
* Habitat-Lab
* Pixel Navigation

We thank the authors of these projects for making their code and datasets publicly available.

---

## Citation

```bibtex
@article{yourname2026ssmpixnav,
  title={SSM-PixNav: State Space Models for Pixel-Guided Embodied Navigation},
  author={Author Names},
  journal={arXiv},
  year={2026}
}
```
