# Potato Leaves Blight Disease Classification (Bangladesh Perspective)

[![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)](https://jupyter.org/)
[![Python: 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Framework: TensorFlow / Keras](https://img.shields.io/badge/Framework-TensorFlow%20%2F%20Keras-red.svg)](https://www.tensorflow.org/)
[![Paper: Engineering Journal 2023](https://img.shields.io/badge/Publication-Engineering%20Journal%202023-brightgreen.svg)](https://jesminnipu.github.io/Portfolio/#publications)
[![Conference: IEEE ETCCE 2021](https://img.shields.io/badge/Conference-IEEE%20ETCCE%202021-blue.svg)](https://jesminnipu.github.io/Portfolio/#publications)

This repository contains the Jupyter Notebooks (`.ipynb`) and deep learning experimentation workflows for detecting and classifying potato leaf blight diseases (**Early Blight** and **Late Blight**) in the perspective of Bangladesh agriculture, evaluating custom Convolutional Neural Networks (CNN) alongside Transfer Learning backbones (**InceptionV3**, **ResNet-50**, and **VGG**).

---

## 📑 Associated Peer-Reviewed Publications

1. **J. Akther, M. Harun-or-roshid, and A. A. Nayan**  
   *"Potato Leaves Blight Disease Classification in Bangladesh Perspective Using Convolutional Neural Network (CNN)."*  
   **Engineering Journal**, Vol. 27, No. 7, pp. 27–38, 2023. *(Scopus-indexed)*

2. **J. Akther, M. Harun-or-roshid, A. A. Nayan, and M. G. Kibria**  
   *"Transfer learning on VGG16 for the classification of potato leaves infected by blight diseases."*  
   **IEEE Emerging Technology in Computing, Communication and Electronics (ETCCE)**, pp. 1–5, 2021.

---

## 🔬 Research Overview & Problem Statement

Potato is a vital staple food and cash crop in Bangladesh. However, severe foliar fungal and oomycete infections—specifically **Early Blight** (*Alternaria solani*) and **Late Blight** (*Phytophthora infestans*)—consistently inflict catastrophic damage on potato yields. 

Manual disease inspection is labor-intensive, error-prone, and often too late to prevent large-scale crop failure. This project establishes an automated visual diagnostics framework using deep learning to accurately categorize diseased leaves even in real-world agricultural conditions.

---

## 📓 Notebooks Included in this Repository

| Notebook | Focus & Architecture | Key Highlights |
| :--- | :--- | :--- |
| [**`earlylate.ipynb`**](./earlylate.ipynb) | **Custom CNN / SCNN Pipeline** | Full data preprocessing pipeline (RGB/Grayscale, normalization, resizing), custom multi-layer CNN training, validation splits, and TensorBoard hyperparameter monitoring for Early Blight vs. Late Blight detection. |
| [**`Inception V3.ipynb`**](./Inception%20V3.ipynb) | **Transfer Learning (InceptionV3)** | Implementation of Google's InceptionV3 architecture pretrained on ImageNet, with custom classification heads for fine-grained potato foliar disease diagnosis. |
| [**`Resnet 50.ipynb`**](./Resnet%2050.ipynb) | **Transfer Learning (ResNet-50 / VGG)** | Deep residual learning using ResNet-50 and VGG16/VGG19 backbones, analyzing residual connections and feature extraction capabilities for agricultural pathology. |

---

## 🧠 Methodology & Experimental Workflow

1. **Image Preprocessing & Augmentation:**
   * Image ingestion, dimension normalization (e.g., 50×50, 100×100, 224×224 pixels), and color-space transformations.
   * Geometric and photometric data augmentation (rotations, horizontal/vertical flips, zoom, shear) to enhance model generalizability.
2. **Deep Architecture Implementation:**
   * **Custom CNN / SCNN:** Sequential convolutional layers with progressive filter counts (e.g., 64, 128, 256), `ReLU` activations, `MaxPooling2D`, and `Dropout` regularization.
   * **Pretrained Deep Backbones:** Freezing early feature extraction layers in InceptionV3 and ResNet-50 while retraining dense classification heads.
3. **Training & Optimization:**
   * Cost function: Binary cross-entropy / Categorical cross-entropy.
   * Optimizer: Adaptive Moment Estimation (**Adam**).
   * Real-time metrics visualization using **TensorBoard**.

---

## 🚀 Getting Started

### Prerequisites

* Python 3.8, 3.9, or 3.10
* JupyterLab / Jupyter Notebook or Google Colab

### Installation & Execution

1. **Clone this repository:**
   ```bash
   git clone https://github.com/JesminNipu/Potato-Leaves-Blight-Disease-Classification-Bangladesh.git
   cd Potato-Leaves-Blight-Disease-Classification-Bangladesh
   ```

2. **Install required dependencies:**
   ```bash
   pip install tensorflow opencv-python matplotlib numpy pandas scikit-learn notebook
   ```

3. **Launch JupyterLab or Notebook:**
   ```bash
   jupyter notebook
   ```

4. **Run any of the notebooks:**
   * Open `earlylate.ipynb`, `Inception V3.ipynb`, or `Resnet 50.ipynb` in the browser.
   * Execute cells sequentially to inspect data loading, model compilation, training histories, and performance curves.

---

## 📂 Repository Structure

```text
Potato-Leaves-Blight-Disease-Classification-Bangladesh/
├── earlylate.ipynb       # Custom CNN training & evaluation for potato leaf blight
├── Inception V3.ipynb    # Transfer learning pipeline using InceptionV3
├── Resnet 50.ipynb       # Transfer learning pipeline using ResNet-50 / VGG
├── README.md             # Comprehensive research and technical documentation
└── .gitignore            # Jupyter checkpoints, cache, and model file exclusions
```

---

## 👩‍💻 Author & Contact

**Jesmin Akther**  
Mobile Application Developer & Computer Science Researcher  
* Department of Information and Communication Engineering (ICE), NSTU  
* **Email:** [jesminnipu1@gmail.com](mailto:jesminnipu1@gmail.com)  
* **GitHub:** [@JesminNipu](https://github.com/JesminNipu)  
* **Academic Portfolio:** [https://jesminnipu.github.io/Portfolio/](https://jesminnipu.github.io/Portfolio/)
