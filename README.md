Text Generation using RNN

Comparison of One-Hot Encoding vs Trainable Word Embeddings

📌 Objective

The objective of this project is to implement a Recurrent Neural Network (RNN) for text generation using:

One-Hot Encoding

Trainable Word Embeddings

The goal is to compare both approaches in terms of:

Training loss

Memory efficiency

Scalability

Quality of generated text

📂 Dataset

Dataset: 100 Poems

Format: CSV (poems-100 - poems-100.csv)

Column Used: text

The dataset consists of multiple lines of poetry used to train a next-word prediction model.

⚙️ Implementation Details
🔹 Part 1 – RNN from Scratch (NumPy)

A basic RNN was implemented using NumPy to understand:

Hidden state computation

Weight matrices (Wxh, Whh, Why)

Forward propagation

This part was for conceptual understanding only.

🔹 Part 2 – One-Hot Encoding Approach
Preprocessing

Tokenization using whitespace split

Vocabulary creation

Words converted into index sequences

One-hot representation simulated inside model

Model Architecture

RNN layer (nn.RNN)

Fully connected output layer

CrossEntropyLoss

Adam optimizer

Observations

Higher memory usage

Slower scalability

Less coherent generated text

🔹 Part 3 – Trainable Word Embeddings Approach
Preprocessing

Tokenization

Word-to-index mapping

Direct indexed sequences (no one-hot)

Model Architecture

Embedding Layer (nn.Embedding)

RNN layer

Fully connected output layer

Observations

Lower memory usage

Better scalability

More coherent poetic text generation

Smoother loss convergence

📊 Loss Comparison

Both models were trained for multiple epochs and compared.

General observation:

Embedding model converges more smoothly.

One-hot requires more memory.

Embedding-based model scales better for larger vocabulary.

📝 Sample Generated Text
🔵 One-Hot Model
love is brush a tree and fast, and the same and downy under the moon on a rhyme? grass of you,

🟠 Embedding Model
love my spirit eyes i said, "he thinks he may be dim, joy outposts of old salt and filter and little


The embedding model produced more semantically meaningful and structured text compared to the one-hot model.
