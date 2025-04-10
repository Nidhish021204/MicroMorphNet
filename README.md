# 🌼 MicroMorphNet: Intelligent Detection of Pollen Morphologies using Faster R-CNN

![Pollen Detection Banner](https://raw.githubusercontent.com/bjin96/pollen-detection/main/assets/banner.png)

MicroMorphNet is an advanced deep learning-based solution that automatically detects and classifies pollen grains in microscopic images using Faster R-CNN. This system is particularly useful for allergen monitoring, environmental studies, and medical diagnostics.

---

## 🚀 Project Overview

- **Model:** Faster R-CNN with custom TIMM backbones
- **Data:** Synthesized and raw microscope datasets from Augsburg
- **Augmentations:** Rotation, flip, crop, and more
- **Training Strategy:** Supervised learning via PyTorch Lightning

---

## 🧪 Dataset & Augmentations

- **Train:** Raw + Synthesized Pollen Images (2016 & 2018)
- **Validation:** Mixed evaluation datasets with image augmentations:
  - Horizontal & vertical flips
  - Random crop
  - Rotation with cutoff

---

## 📊 Results

| Backbone        | mAP (%) | IoU Threshold | Dataset                          |
|----------------|---------|----------------|----------------------------------|
| ResNet-50      | 73.4    | 0.5            | 2016 + 2018 Raw                  |
| EfficientNet-V2| 76.8    | 0.5            | 2016 + 2018 Synthesized          |
| MobileNet-V3   | 69.2    | 0.5            | 2016 Synthesized + Raw Combined |

> 📌 *Best performance achieved with EfficientNet-V2 backbone on the synthesized dataset group.*

---

## 📷 Sample Outputs

<p float="left">
  <img src="https://raw.githubusercontent.com/bjin96/pollen-detection/main/assets/pred1.png" width="45%"/>
  <img src="https://raw.githubusercontent.com/bjin96/pollen-detection/main/assets/pred2.png" width="45%"/>
</p>

---

## 🛠️ Setup & Installation

```bash
git clone https://github.com/bjin96/pollen-detection.git
cd pollen-detection
pip install -r requirements.txt
