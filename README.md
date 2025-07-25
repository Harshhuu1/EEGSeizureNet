# 🧠 EEGSeizureNet

> **Enhanced EEG Seizure Detection using EfficientNet-B0 and Classic GAN-based Augmentation**

[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Deploy-red.svg)](https://streamlit.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📌 Overview

EEGSeizureNet is a research-grade deep learning pipeline built for accurate seizure prediction using EEG spectrogram images. It combines:

- ✅ EfficientNet-B0 for high-performance classification
- 🎯 Focal Loss for imbalanced learning
- 🧬 Classic GAN to augment synthetic EEG spectrograms
- 📊 CHB-MIT EEG dataset
- 🚀 Streamlit frontend + FastAPI backend for real-time predictions

---

## 📂 Project Structure

├── dataset/ # Contains 'seizure/' and 'non_seizure/' spectrogram images
├── gan_generator.py # GAN training for data augmentation
├── spectrogram.py # Converts EEG .edf files to spectrograms
├── train_model.py # Main training script (EfficientNet-B0)
├── app.py # Streamlit frontend
├── api.py # FastAPI backend (optional)
├── requirements.txt
├── best_fast_model.pth # Trained model checkpoint
├── train_val_accuracy.png #


---

## 📥 Dataset

**Source**: [CHB-MIT Scalp EEG Database](https://physionet.org/content/chbmit/1.0.0/)

```bash
# Download EEG dataset (bash)
wget -r -N -c -np https://physionet.org/files/chbmit/1.0.0/

Convert EEG .edf signals to spectrograms using:
python spectrogram.py

| Component        | Description                  |
| ---------------- | ---------------------------- |
| Backbone         | EfficientNet-B0 (pretrained) |
| Loss             | Focal Loss (α=0.25, γ=2.0)   |
| Optimizer        | AdamW                        |
| Scheduler        | OneCycleLR                   |
| Augmentation     | Albumentations + Classic GAN |
| Accuracy (Train) | 92.5%                        |
| Accuracy (Val)   | 91.5%                        |


💡 Author
Harsh Yadav







