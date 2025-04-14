# StutterAssist

# 🗣️ StutterAssist: A Deep Learning Framework for Dysfluency Detection and Speech Reconstruction

**StutterAssist** is a deep learning-based research project that addresses the dual challenges of detecting stuttering dysfluencies and reconstructing fluent speech. Designed with the goal of enabling better communication for individuals with speech disorders, this project integrates advanced speech processing models into a unified pipeline.

---

## 🚀 Project Overview

Traditional approaches to stuttering often focus solely on detection or require manual intervention. **StutterAssist** proposes an end-to-end deep learning framework that performs:

- ✅ **Multi-label dysfluency detection** using a **Multi-Head Attention Transformer Encoder**
- 🎯 **Speech reconstruction** from stuttered input using a custom **STRC-ED (Sequence-to-Sequence Reconstruction Encoder-Decoder)**
- 💡 Support for **overlapping dysfluencies**, **speaker identity preservation**, and **temporal alignment**

---

## 📂 Components

### 🔍 Dysfluency Detection
- **Model:** Transformer encoder + BiLSTM
- **Features:** Wav2Vec2 embeddings
- **Labels:** Repetition, Prolongation, Block, Interjection
- **Datasets Used:** SEP-28k, FluencyBank, LibriStutter

### 🔁 Stuttered Speech Reconstruction
- **Model:** STRC-ED (Convolution + BiLSTM encoder, attention-guided LSTM decoder)
- **Input/Output:** Mel Spectrograms
- **Evaluation:** MSE, SSIM, Cosine Similarity

---

## 📊 Results Summary

| Task                       | Dataset      | Accuracy | F1-Score | UAR   | AP    |
|---------------------------|--------------|----------|----------|-------|-------|
| Binary Classification     | SEP-28K      | 83.16%   | 53.30%   | 69.57 |   -   |
| Multi-Label Classification| FluencyBank  | 75.72% (Interj.) | 71.96% | 72.43 | 40.86 |

For detailed evaluation and confusion matrices, refer to the **results** folder.

---

## 📁 Datasets

All datasets used in this project are publicly available:

- [SEP-28k](https://zenodo.org/record/5226654)
- [FluencyBank](https://fluency.talkbank.org/access/)
- [LibriStutter](https://zenodo.org/record/6950392)
- [LibriSpeech](http://www.openslr.org/12)

---

## 📜 License

This project is released as part of an academic research submission.  
It is intended for **non-commercial research and educational use only**.  
All rights reserved by the authors.

For other usage inquiries, please contact the corresponding author.

