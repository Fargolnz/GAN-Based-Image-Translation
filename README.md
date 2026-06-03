# 🖼️ GAN-Based Image Translation

A deep learning project for image-to-image translation using a Pix2Pix Conditional GAN implemented in PyTorch.

The model learns a mapping between paired images and generates realistic outputs from structured inputs such as edges and semantic representations.

---

## 📌 Introduction

This project was developed as part of a Computer Vision course and focuses on image translation using Generative Adversarial Networks (GANs).

The implementation is based on the Pix2Pix framework, combining a U-Net Generator with a PatchGAN Discriminator to generate high-quality translated images.

---

## 🧑🏻‍💻 Developers

This project was collaboratively developed by:

* **Seyyedeh Fargol Nazemzadeh**
* **Mahdi Emami**

---

## ✨ Features

* Pix2Pix Conditional GAN
* U-Net Generator Architecture
* PatchGAN Discriminator
* Paired Image Translation
* Automatic Checkpoint Saving
* Training Resume Support
* PSNR Evaluation
* SSIM Evaluation
* GPU Acceleration with CUDA
* PyTorch Implementation

---

## 🏗️ Model Architecture

### Generator

The generator is implemented as an 8-layer U-Net architecture featuring:

* Encoder-Decoder Structure
* Skip Connections
* Batch Normalization
* Dropout Regularization

### Discriminator

The discriminator follows the PatchGAN architecture and evaluates local image patches rather than the entire image.

This helps the model produce sharper and more realistic outputs.

---

## 🗂️ Dataset

This project uses the **Edges2Shoes** dataset, a widely used benchmark for image-to-image translation tasks.

The dataset consists of paired images where:

```text
Edge Map  →  Shoe Image
```

The model learns to translate edge representations of shoes into realistic shoe photographs using supervised training.

### Dataset Characteristics

* Paired training samples
* Edge-to-photo translation task
* Suitable for conditional GAN training
* Common benchmark for Pix2Pix models

### Data Preprocessing

Each dataset image contains:

```text
Input Edge Image | Target Shoe Image
```

The images are automatically split into input-target pairs during the preprocessing stage before being fed to the network.

---

## 📂 Project Structure

```text
GAN-Based-Image-Translation/
│
├── data/
│   ├── check_dataset.py
│   ├── dataset.py
│   └── edges2shoes/               # Place the Edges2Shoes dataset here
│
├── models/
│   ├── generator.py
│   └── discriminator.py
│
├── checkpoints/
│
├── outputs/
│
├── results/
│
├── train.py
├── evaluation.py
├── utils.py
├── train.ipynb
└── README.md
```

---

## 🚀 Installation

### Clone Repository

```bash
git clone https://github.com/Fargolnz/GAN-Based-Image-Translation.git
cd GAN-Based-Image-Translation
```

### Install Dependencies

```bash
pip install torch torchvision
pip install numpy pillow scikit-image
```

---

## ▶️ Training

```bash
python train.py
```

The model automatically:

* Saves checkpoints
* Generates sample outputs
* Supports training resumption

---

## 📊 Evaluation

```bash
python evaluation.py
```

Evaluation metrics include:

* PSNR (Peak Signal-to-Noise Ratio)
* SSIM (Structural Similarity Index)

---

## 🖼️ Results

The trained Pix2Pix model successfully generates realistic shoe images from edge maps.

### Example Translation

```text
Input Edge Map
       ↓
Generated Shoe Image
       ↓
Ground Truth Shoe Image
```

The model learns both the overall structure and fine visual details of shoes, producing outputs that closely resemble the target images.

---

## 🛠️ Technologies

| Technology   | Purpose                 |
| ------------ | ----------------------- |
| Python       | Core Implementation     |
| PyTorch      | Deep Learning Framework |
| CUDA         | GPU Acceleration        |
| NumPy        | Numerical Computing     |
| Pillow       | Image Processing        |
| scikit-image | Evaluation Metrics      |

---

## 🎯 Learning Objectives

This project demonstrates:

* Image-to-Image Translation
* Generative Adversarial Networks
* Conditional GANs
* U-Net Architectures
* PatchGAN Discriminators
* Computer Vision
* Deep Learning with PyTorch

---

## 📚 Future Improvements

Potential enhancements include:

* CycleGAN implementation
* Higher-resolution image generation
* Additional datasets
* FID Score evaluation
* Attention-based generators
* Multi-GPU training

---

## 🎓 Academic Project

This project was developed as part of a Computer Vision course and focuses on image translation using modern deep learning techniques.

---

## 🙏🏻 Acknowledgments

* Computer Vision Course
* Faculty of Farabi, University of Tehran
* Academic Year 1404–1405