# 🧪 Experiment 9: Generative Adversarial Networks (GANs)

## 📌 Objective

The objective of this experiment is to implement and analyze **Generative Adversarial Networks (GANs)** for image generation using the Fashion-MNIST dataset.
We compare different architectures, loss functions, and optimizers to study training behavior and performance.

---

## 📂 Dataset

* **Fashion-MNIST**
* 28×28 grayscale images
* Preprocessing:

  * Normalized to [-1, 1]

---

## 🧠 Models Implemented

### 1. Vanilla GAN

* Fully connected layers
* Simple architecture
* Limited image quality

### 2. DCGAN

* Convolutional layers
* Batch Normalization
* Improved image quality and stability

---

## ⚙️ Experimental Setup

### Loss Functions:

* Binary Cross Entropy (BCE)
* Least Squares GAN (LSGAN)
* Wasserstein Loss (WGAN)

### Optimizers:

* SGD
* RMSprop
* Adam (best performance observed)

---

## 📊 Training Results

### 🔹 Discriminator Loss

![Discriminator Loss](./W&B Chart 4_16_2026, 7_43_00 PM.png)

### 🔹 Generator Loss

![Generator Loss](./W&B Chart 4_16_2026, 7_43_13 PM.png)

---

## 📈 Observations

### 1. Generator Improvement

* Initial epochs: Noisy and unclear images
* Mid training: Shapes of clothing emerge
* Final epochs: More structured and realistic outputs

---

### 2. Training Stability

* Discriminator loss stabilizes around **0.85–1.1**
* Generator loss fluctuates, indicating adversarial learning
* Oscillatory behavior confirms GAN dynamics

---

### 3. Quality vs Diversity Trade-off

* Improved image quality sometimes reduces diversity
* Occasional mode collapse observed
* DCGAN provides better balance than Vanilla GAN

---

### 4. Sensitivity to Hyperparameters

* Learning rate significantly affects convergence
* Adam optimizer gives stable and faster training
* Loss function choice impacts gradient behavior

---

## 🎯 Expected Outcomes

* DCGAN produces **higher quality images** than Vanilla GAN
* WGAN/LSGAN improves **training stability**
* Adam optimizer ensures **smooth convergence**
* GAN training demonstrates:

  * Oscillations
  * Mode collapse
  * Adversarial learning behavior

---

## 🚀 Conclusion

* DCGAN outperforms Vanilla GAN in both quality and stability
* Proper combination of **loss function + optimizer** is critical
* GAN training is inherently unstable but manageable with tuning
* Experiment provides strong understanding of generative modeling

---

## 📦 Outputs

* Generated images saved per epoch
* Trained models (`generator.pth`, `discriminator.pth`)
* W&B logs for visualization

---

## 🔗 Submission Components

* ✅ GitHub Repository (code + README)
* ✅ Weights & Biases dashboard
* ✅ Hugging Face model upload

---

## 🏁 Final Remark

This experiment demonstrates the practical challenges and strengths of GANs, highlighting the importance of architecture design and training strategies in deep generative models.
