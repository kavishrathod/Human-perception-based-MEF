# Human Perception-Based Deep Learning Model for Weight-Map Guided Multi-Exposure Image Fusion

## 📘 Overview
Modern imaging systems struggle to capture both very bright and dark regions within a single shot due to limited dynamic range.

This project presents a **Human-Perception-Based Deep Learning Model** that uses **Convolutional Neural Networks (CNNs)** to generate perceptually guided **weight maps** for **multi-exposure image fusion (MEF)**.

Unlike traditional fusion methods, this model integrates perceptual cues such as **contrast, color saturation, well-exposedness, local entropy, and visibility** — enabling image fusion that mimics **human visual perception**.

## 🧠 Motivation
Traditional MEF methods fail under extreme exposure variations or in real-time scenarios due to manual weight computation and poor perceptual adaptation.

Inspired by how the human brain balances brightness and color under diverse lighting conditions, this model seeks to integrate **AI-based perceptual learning** into exposure fusion.

## 🎯 Objectives
- Develop a deep learning-based framework for **weight map generation** guided by human perceptual features.
- Implement and analyze five perceptual quality parameters:
  - Contrast
  - Saturation
  - Well-exposedness
  - Local entropy
  - Visibility
- Train on a dataset of over **10,000 HDR images** covering diverse illumination conditions.
- Achieve **real-time** and **artifact-free** exposure fusion comparable with or superior to existing MEF methods.

## ⚙️ Methodology
1. **Input**  
   Multiple images of the same scene captured at different exposure levels (under, normal, over-exposed).

2. **Feature Extraction**  
   For each image, the CNN extracts five perceptual features:
   - **Contrast** — via Laplacian gradients.
   - **Saturation** — via RGB standard deviation.
   - **Well-exposedness** — via Gaussian distribution centered at mid-intensity.
   - **Local Entropy** — via local texture complexity.
   - **Visibility** — via gradient magnitude.

3. **Weight Map Generation**  
   The CNN learns to assign pixel-wise perceptual weights balancing brightness and contrast intelligently.

4. **Fusion Process**  
   Multi-scale representation using **Gaussian and Laplacian pyramids** ensures natural blending and accurate edge preservation.

5. **Output**  
   A single **perceptually optimized** fused image maintaining visibility, contrast, and natural illumination.

## 🧩 Technologies Used
- Python 3.x
- TensorFlow / PyTorch (Deep Learning Framework)
- OpenCV (Image Processing)
- NumPy, Matplotlib (Computation and Visualization)
- Google Colab / Jupyter Notebook (Model Training & Testing)

## 🧪 Results
- Generated perceptual scores closely align with human visual judgment.
- Fused images demonstrate improved **clarity**, **contrast**, and **realism**.
- Effective for photography, surveillance, and medical imaging.

## 📊 Dataset
- Contains ~10,000 HDR images with varied illumination, textures, and contrast.
- Used for future model training, evaluation, and optimization.
- Dataset planned for public release after model validation.

## 🔬 Future Scope
- **Indigenous Perception Model** — Tailoring fusion for specific lighting conditions or cultural visual biases.
- **Integration into Unified CNN Model** — Streamlined, perception-aware real-time fusion.
- **End-to-End Deep Fusion Network** — Replace pyramid-based fusion with trainable CNN/Transformer model for efficiency.

## 📚 References
The work builds upon seminal research in multi-exposure image fusion and perceptual modeling, including:

- **Mertens et al.**, *Exposure Fusion*: A Practical Alternative to HDR (2007)

- **Prabhakar et al.**, *DeepFuse*: A Deep Unsupervised Approach for Exposure Fusion (ICCV 2017)

- **Yang et al.**, *GANFuse*: Generative Adversarial Fusion Framework (2021)

- **Qu et al.**, *TransMEF*: Transformer-Based Self-Supervised Fusion (ICIP 2020)

---
📄 *Developed as part of a research project on human perception-guided deep learning for exposure fusion.*
