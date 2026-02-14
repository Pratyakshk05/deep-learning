

# experiment 6 Sequence-to-Sequence Learning with LSTM

## English → Spanish Machine Translation

---

## Overview

This project implements Sequence-to-Sequence (Seq2Seq) models for English to Spanish machine translation using:

* LSTM Encoder–Decoder (Without Attention)
* LSTM + Bahdanau (Additive) Attention
* LSTM + Luong (Multiplicative) Attention

The models are evaluated using BLEU Score and attention weights are visualized for interpretability.

---

## Objective

* Implement vanilla Seq2Seq using LSTM
* Extend model with:

  * Bahdanau Attention
  * Luong Attention
* Compare performance
* Evaluate using BLEU score
* Visualize attention weights

---

## Dataset

* File: spa.txt
* Format:
  English sentence \t Spanish sentence

Example:
Hello.	Hola.
How are you?	¿Cómo estás?
I am fine.	Estoy bien.

If dataset is large:

* Sample ~10,000 sentence pairs
* Split:

  * 80% Training
  * 10% Validation
  * 10% Testing

---

## Preprocessing

* Lowercasing
* Tokenization
* Vocabulary creation
* Special tokens:

  * <sos>
  * <eos>
  * <pad>
* Convert text to indices
* Padding sequences

---

## Model Architectures

### 1. LSTM Encoder–Decoder (Without Attention)

Encoder:

* Embedding layer
* LSTM
* Outputs final hidden and cell states

Decoder:

* Embedding layer
* LSTM
* Linear layer → vocabulary size
* Uses teacher forcing during training

---

### 2. LSTM + Bahdanau Attention (Additive)

* Alignment score:
  score = v^T tanh(W1 h_enc + W2 h_dec)
* Context vector computed as weighted sum of encoder outputs
* Improves long-sequence translation
* Better word alignment

---

### 3. LSTM + Luong Attention (Multiplicative)

* Alignment score:
  score = h_dec^T W h_enc
* Faster than Bahdanau
* Efficient and performs well

---

## Training Details

* Loss: CrossEntropyLoss
* Optimizer: Adam
* Teacher Forcing used
* Batch training
* Evaluation on validation set

---

## Evaluation Metric

BLEU Score:

* Measures n-gram overlap between predicted and reference translations
* Higher BLEU indicates better translation quality



## Run Training

python train.py

---

## Run Evaluation

python evaluate.py

---

## Results Summary

| Model           | Attention | Observation                     |
| --------------- | --------- | ------------------------------- |
| LSTM            | No        | Struggles with long sentences   |
| LSTM + Bahdanau | Yes       | Better alignment, improved BLEU |
| LSTM + Luong    | Yes       | Faster and efficient            |

---

## Key Learnings

* Seq2Seq architecture
* Encoder–Decoder mechanism
* Teacher forcing
* Attention mechanisms
* BLEU evaluation
* Model interpretability



# Experiment 5- Text Generation using RNN

**Comparison of One-Hot Encoding vs Trainable Word Embeddings**

---

## 📌 Objective

The objective of this project is to implement a Recurrent Neural Network (RNN) for text generation using:

* One-Hot Encoding
* Trainable Word Embeddings

The goal is to compare both approaches in terms of:

* Training loss
* Memory efficiency
* Scalability
* Quality of generated text

---

##  Dataset

* Dataset: 100 Poems
* Format: CSV (`poems-100 - poems-100.csv`)
* Column Used: `text`

The dataset consists of multiple lines of poetry used to train a next-word prediction model.

---

##  Implementation Details

### 🔹 Part 1 – RNN from Scratch (NumPy)

A basic RNN was implemented using NumPy to understand:

* Hidden state computation
* Weight matrices (Wxh, Whh, Why)
* Forward propagation

This part was for conceptual understanding only.

---

### 🔹 Part 2 – One-Hot Encoding Approach

#### Preprocessing

* Tokenization using whitespace split
* Vocabulary creation
* Words converted into index sequences
* One-hot representation simulated inside model

#### Model Architecture

* RNN layer (`nn.RNN`)
* Fully connected output layer
* CrossEntropyLoss
* Adam optimizer

#### Observations

* Higher memory usage
* Slower scalability
* Less coherent generated text

---

### 🔹 Part 3 – Trainable Word Embeddings Approach

#### Preprocessing

* Tokenization
* Word-to-index mapping
* Direct indexed sequences (no one-hot)

#### Model Architecture

* Embedding Layer (`nn.Embedding`)
* RNN layer
* Fully connected output layer

#### Observations

* Lower memory usage
* Better scalability
* More coherent poetic text generation
* Smoother loss convergence

---

##  Loss Comparison

Both models were trained for multiple epochs and compared.

General observation:

* Embedding model converges more smoothly.
* One-hot requires more memory.
* Embedding-based model scales better for larger vocabulary.

---

##  Sample Generated Text

### 🔵 One-Hot Model

```
love is brush a tree and fast, and the same and downy under the moon on a rhyme? grass of you,
```

### 🟠 Embedding Model

```
love my spirit eyes i said, "he thinks he may be dim, joy outposts of old salt and filter and little
```

The embedding model produced more semantically meaningful and structured text compared to the one-hot model.

---

## 📈 Key Comparison

| Feature           | One-Hot  | Embedding       |
| ----------------- | -------- | --------------- |
| Memory Usage      | High     | Low             |
| Scalability       | Poor     | Good            |
| Semantic Learning | No       | Yes             |
| Text Quality      | Moderate | Better          |
| Practical Use     | Rare     | Standard in NLP |

---

