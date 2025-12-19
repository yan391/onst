<div align="center">

# Prototypical Self-Training with Progress-Aware Update for Source-Free Domain Adaptation in Semantic Segmentation

[![ICASSP 2026](https://img.shields.io/badge/ICASSP%202026-Under%20Review-4b44ce)](http://2026.ieeeicassp.org/)
[![Pretrained Models](https://img.shields.io/badge/Models-Google%20Drive-orange)](https://drive.google.com/drive/folders/1CYooo-uTGEHzviT2smwlhHaXQCNimy2M?usp=sharing)

</div>

---

## 📖 Abstract

The remaining core code will be released once our paper is accepted. To demonstrate the authenticity of our results, we provide part of the core code, training logs, and the trained segmentation model.

## 📂 Downloads & Resources

We provide the training logs, trained models, and prediction results for verification.

| Resource | Link | Description |
| :--- | :---: | :--- |
| **Training Logs & Models** | [Download](https://drive.google.com/drive/folders/1CYooo-uTGEHzviT2smwlhHaXQCNimy2M?usp=sharing) | Contains `.log` files and checkpoints |
| **Test Results** | [Download](https://drive.google.com/drive/folders/1CYooo-uTGEHzviT2smwlhHaXQCNimy2M?usp=sharing) | Predicted segmentation masks |
| **Cityscapes Dataset** | [Website](https://www.cityscapes-dataset.com/) | Official dataset website |

## 🚀 Getting Started

### Testing
You can try testing the trained model on the validation set using the following command:

```bash
python test.py -cfg configs/deeplabv2_r101_dtst.yaml resume results/model_20000.pth
```
## 🎨 Visualization Results

### Qualitative results on GTA5 → Cityscapes
<div align="center">
  <img src="photos/1.jpg" width="100%" alt="Visualization Results"/>
</div>

## 📊 Comparison to State-of-the-Art

> **Note:** 'SF' represents whether the method is in a source-free setting. The **highest results** in UDA methods are in bold italics. The **best results** in SFDA methods are in bold.

### 1. GTA5 → Cityscapes
<div align="center">
  <img src="photos/3.png" width="95%" alt="GTA5 Results"/>
</div>

### 2. SYNTHIA → Cityscapes
<div align="center">
  <img src="photos/4.png" width="95%" alt="SYNTHIA Results"/>
</div>

## 📉 Ablation Study

Here we provide the sensitivity analysis of various hyperparameters used in our method.

| Momentum Bounds ($\gamma$) | Prototype Update ($\beta, I$) |
| :---: | :---: |
| <img src="photos/5.png" width="100%"> | <img src="photos/6.png" width="100%"> |
| **(a) Sensitivity of $\gamma_{min}$ and $\gamma_{max}$** | **(b) Sensitivity of momentum $\beta$ and interval $I$** |

| Sampling Parameters ($M, N\%$) | Hyperparameter $\lambda_{CGPL}$ |
| :---: | :---: |
| <img src="photos/7.png" width="100%"> | <img src="photos/8.png" width="100%"> |
| **(c) Sensitivity of sampled instances $M$ and top $N\%$** | **(d) Sensitivity of $\lambda_{CGPL}$** |

## 🔗 References

We would like to thank the following paper for providing code that was helpful to our work:

```bibtex
@inproceedings{zhao2023towards,
  title={Towards better stability and adaptability: Improve online self-training for model adaptation in semantic segmentation},
  author={Zhao, Dong and Wang, Shuang and Zang, Qi and Quan, Dou and Ye, Xiutiao and Jiao, Licheng},
  booktitle={Proceedings of the IEEE/CVF conference on computer vision and pattern recognition},
  pages={11733--11743},
  year={2023}
}
