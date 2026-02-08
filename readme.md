# Deep Learning Lab – Experiment 4

## Objective
To implement Convolutional Neural Networks (CNNs) for image classification using:
- CIFAR-10 Dataset
- Cats vs Dogs Dataset

The experiment compares:
- 3 Activation Functions (ReLU, Tanh, LeakyReLU)
- 3 Weight Initializations (Xavier, Kaiming, Random)
- 3 Optimizers (SGD, Adam, RMSprop)

Additionally, transfer learning using ResNet-18 was performed and compared with the custom CNN.

---

## Datasets Used

1. CIFAR-10
2. Dogs vs Cats (Kaggle Dataset)

---

## Experiment Details

### Custom CNN
- 3 Convolutional layers
- Batch Normalization
- MaxPooling
- Dropout
- Fully Connected layers

Total combinations tested: 27

Best configuration (CIFAR-10):
- Activation: LeakyReLU
- Initialization: Kaiming
- Optimizer: Adam
- Accuracy: 78.43%

---

### Transfer Learning – ResNet-18
- Pretrained on ImageNet
- Fine-tuned for classification
- Final layer modified for dataset

---

## Results Summary

### CIFAR-10
| Model | Accuracy |
|--------|----------|
| Custom CNN | 78.43% |
| ResNet-18 | ~85–90% |

### Cats vs Dogs
| Model | Accuracy |
|--------|----------|
| Custom CNN | ~88–92% |
| ResNet-18 | ~92–97% |

---

## Observations

- LeakyReLU performed better than ReLU and Tanh.
- Kaiming initialization worked best with ReLU-family activations.
- Adam optimizer converged faster and gave higher accuracy.
- Transfer learning significantly improved performance.

---


---

## Conclusion

Transfer learning with ResNet-18 outperformed the custom CNN model in both datasets. Proper activation-initialization pairing and adaptive optimizers significantly impact performance.


