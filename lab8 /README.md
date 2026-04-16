# Autoencoder and Variational Autoencoder (VAE) on Fashion-MNIST

## 📌 Objective

This experiment implements **Autoencoders (AE)** and **Variational Autoencoders (VAE)** to:

* Learn latent representations of image data
* Perform image reconstruction
* Generate new samples from latent space
* Compare deterministic vs probabilistic models

---

## 📂 Dataset

* **Fashion-MNIST**
* Grayscale images (28×28)
* Classes: shirts, shoes, bags, etc.
* Split:

  * 80% Training
  * 10% Validation
  * 10% Testing

---

## ⚙️ Implementation Details

### 🔹 Autoencoder (AE)

* Deterministic latent representation
* Encoder → compresses image
* Decoder → reconstructs image
* Loss:

  * Binary Cross Entropy (BCE)
  * Mean Squared Error (MSE)

---

### 🔹 Variational Autoencoder (VAE)

* Probabilistic latent space
* Learns:

  * Mean (μ)
  * Variance (σ)
* Uses reparameterization trick:

  ```
  z = μ + σ · ε,  ε ~ N(0,1)
  ```
* Loss:

  * Reconstruction Loss (BCE/MSE)
  * KL Divergence

---

## 🧪 Experiments Conducted

### ✔ Latent Dimensions Tested

* 2, 8, 16, 32

### ✔ Optimizers Used

* SGD
* RMSprop
* Adam

### ✔ Analysis Performed

* Reconstruction quality
* Latent space visualization
* Interpolation between samples
* Generation capability

---

## 📊 Results & Observations

### 🔹 Autoencoder

* Sharper reconstructions
* Deterministic latent space
* Limited generative capability

### 🔹 VAE

* Slightly blurry reconstructions
* Smooth latent space
* Strong generative capability

---

### 🔹 Loss Function Comparison

* **BCE** → sharper images
* **MSE** → smoother but blurrier output

---

### 🔹 Optimizer Comparison

* **Adam** → fastest convergence
* **RMSprop** → stable
* **SGD** → slower training

---

### 🔹 Latent Space Insights

* Low dimensions (2) → easy visualization but limited detail
* Higher dimensions (16, 32) → better reconstruction
* VAE shows smoother interpolation than AE

---

## 🔄 Latent Space Interpolation

* Smooth transition between categories observed in VAE
* AE transitions less meaningful

---

## 📈 Experiment Tracking (W&B)

👉 **Weights & Biases Dashboard:**
https://wandb.ai/pratyakshk05-delhi-technological-university/Autoencoder-VAE?nw=nwuserpratyakshk05

Includes:

* Training loss curves
* Model comparisons
* Experiment logs

---

## 📦 Files Included

* `lab8.ipynb` → Implementation notebook
* `autoencoder.pth` → Trained AE model
* `vae.pth` → Trained VAE model

---

## 🚀 Key Takeaways

* AE excels in reconstruction
* VAE excels in generation
* Latent space structure is critical
* KL divergence ensures smooth latent distribution

---

## 📚 Conclusion

This experiment demonstrates the fundamental difference between **deterministic and probabilistic generative models**, highlighting the importance of latent space design for real-world applications like image generation and representation learning.

---
