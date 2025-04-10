
# 🌼 MicroMorphNet: Intelligent Detection of Pollen Morphologies using Faster R-CNN

![MicroMorphNet Banner](https://raw.githubusercontent.com/bjin96/pollen-detection/main/assets/banner.png)

**MicroMorphNet** is a deep learning-based system that detects and classifies microscopic pollen grains using Faster R-CNN and pre-trained TIMM backbones. Designed to support allergen monitoring, ecological research, and biomedical diagnostics, it delivers robust and scalable object detection tailored for biological imaging.

---

## 📌 Project Highlights

- 🔍 Built on PyTorch Lightning using Faster R-CNN for high-performance detection
- 🧬 Integrates TIMM backbones (EfficientNet, ResNet, etc.)
- 🧪 Trained on specialized raw and synthetic pollen datasets
- 🧰 Includes preprocessing, augmentation, training, and evaluation modules

---

## 🧬 Dataset and Preprocessing

- Raw microscope images (2016 & 2018 Augsburg datasets)
- Synthetic image generation for class balancing
- Augmentations include: flip, rotation, cropping, brightness shift

---

## 📊 Detection Results

| Backbone        | mAP (%) | Dataset Group           |
|----------------|---------|--------------------------|
| ResNet-50      | 73.4    | Raw 2016 + 2018          |
| EfficientNet-V2| 76.8    | Synthesized (2016/2018)  |
| MobileNet-V3   | 69.2    | Mixed Raw + Synthetic    |

---

## 🖼️ Sample Visualizations

<p float="left">
  <img src="https://raw.githubusercontent.com/bjin96/pollen-detection/main/assets/pred1.png" width="45%"/>
  <img src="https://raw.githubusercontent.com/bjin96/pollen-detection/main/assets/pred2.png" width="45%"/>
</p>

---

## ⚙️ Setup Instructions

```bash
git clone https://github.com/bjin96/pollen-detection.git
cd pollen-detection
pip install -r requirements.txt
```

Place your dataset in `datasets/` and adjust configs accordingly.

---

## 🚀 Run Training

```bash
python lightning_training.py --experiment_name=microMorph_run1 --backbone=efficientnet_v2_s
```

### 📈 Evaluate Model

```bash
python run_evaluation.py --checkpoint_path=path/to/model.ckpt --evaluation_dataset_group=evaluate_2016augsburg15
```

---

## 👨‍💻 Author

**Nidhish Chettri**  
B.Tech Information Technology and Engineering (2nd Year)  
Maharaja Agrasen Institute of Technology, Delhi  

Connect on [LinkedIn]([https://www.linkedin.com/](https://www.linkedin.com/in/nidhish-chettri-b0378428b/)) | Drop a ⭐ if you find this useful!

---

## 📚 Reference

If this work helps your research, please consider citing:

```
@article{jin2023,
  title={Airborne pollen grain detection from partially labelled data utilising semi-supervised learning},
  journal={Science of The Total Environment},
  year={2023},
  doi={10.1016/j.scitotenv.2023.164295}
}
```

---

**MicroMorphNet** – Bringing Intelligence to Nature's Microscapes 🌿
