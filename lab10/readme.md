# 🧠 Image Classification using Vision Transformer (ViT) vs ResNet-18

## 📌 Objective

* Implement **Vision Transformer (ViT)** for image classification
* Compare performance with **ResNet-18 (CNN)**
* Analyze:

  * Data augmentation impact
  * Loss functions & optimizers
  * Model performance

---

## 📊 Dataset

* **CIFAR-10**
* 60,000 images (32×32 RGB)
* Split:

  * 80% Training
  * 10% Validation
  * 10% Testing

---

## ⚙️ Preprocessing

* Normalization
* Data Augmentation:

  * Horizontal Flip
  * Vertical Flip

---

## 🧠 Models

### 🔹 Vision Transformer (ViT)

* Patch Embedding (8×8 patches)
* Positional Encoding
* Transformer Encoder (Self-Attention)
* CLS Token
* Fully Connected Head

### 🔹 ResNet-18

* Standard CNN architecture
* Residual connections

---

## 📉 Loss Functions

* Cross-Entropy Loss
* Label Smoothing
* Focal Loss

---

## ⚡ Optimizers

* SGD
* Adam / AdamW
* RMSprop

---

## 📈 Experiment Tracking

* Used **Weights & Biases (W&B)**
* Metrics tracked:

  * Training Loss
  * Validation Loss
  * Accuracy

🔗 W&B Project:
https://wandb.ai/pratyakshk05-delhi-technological-university/ViT-vs-ResNet

---

## 📊 Results

### 🔥 Model Comparison

| Model     | Accuracy |
| --------- | -------- |
| ViT       | ~60–70%  |
| ResNet-18 | ~80–85%  |

---

## 📉 Visualization

* ViT vs ResNet accuracy comparison plotted
* Shows ResNet outperforming ViT on small dataset

---

## 🔍 Key Observations

### 1. ViT vs CNN

* CNN performs better on small datasets
* ViT requires large data to generalize well

### 2. Data Augmentation

* Improves generalization
* Reduces overfitting

### 3. Loss Functions

* Cross-Entropy → stable
* Focal Loss → handles hard samples

### 4. Optimizers

* Adam → fast convergence
* SGD → stable but slower

---

## ⚠️ Challenges

* ViT training is slower
* Requires tuning (patch size, layers, optimizer)
* Lower accuracy without pretraining

---

## ✅ Conclusion

* ResNet-18 outperforms ViT on CIFAR-10
* ViT improves with better tuning and more data
* Transformers are powerful but data-hungry

---

## 🚀 Future Work

* Use pretrained ViT
* Increase dataset size
* Hyperparameter tuning
* Advanced augmentation

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Torchvision
* Weights & Biases

---

## 👤 Author

**Pratyaksh Kumar**
