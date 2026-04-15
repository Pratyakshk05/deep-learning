
EXPERIMENT 7 Sequence-to-Sequence Learning with Transformers
English → Spanish Machine Translation
📌 Objective
The objective of this experiment is to implement a Sequence-to-Sequence (Seq2Seq) model using the Transformer architecture for machine translation from English to Spanish. The model leverages self-attention mechanisms instead of recurrent networks to improve parallelization and performance.

📂 Dataset
The dataset consists of English–Spanish sentence pairs stored in a text file (spa.txt). Each line contains one pair separated by a tab:

Hello.	Hola.
How are you?	¿Cómo estás?
I am fine.	Estoy bien.
⚙️ Features Implemented
Word Embeddings for source and target languages
Sinusoidal Positional Encoding
Multi-Head Self-Attention
Transformer Encoder–Decoder Architecture
Teacher Forcing during training
Greedy Decoding for inference
BLEU Score evaluation with smoothing
Model saving after training
🧠 Model Architecture
Embedding Dimension: 128 / 256 (configurable)
Attention Heads: 4 / 8
Encoder Layers: 2–3
Decoder Layers: 2–3
Optimizer: Adam
Loss Function: CrossEntropy with padding mask
🚀 Installation
Install required libraries:

pip install torch nltk scikit-learn
▶️ How to Run
Place spa.txt in the project directory.
Run the notebook or Python script:
python transformer_translation.py
If using Google Colab, upload the dataset when prompted.

📊 Expected Output
Epoch 1
Loss: 5.4
BLEU: 0.05
----------------
Epoch 5
Loss: 2.8
BLEU: 0.30
----------------
Training Complete
Loss decreases and BLEU score increases over epochs.

🌍 Example Translations
English	Predicted Spanish
Hello	Hola
Run!	¡Corre!
Thank you	Gracias
I love you	Te amo
⏱ Training Time
Training time depends on hardware:

Hardware	Time
CPU	5–20 minutes
GPU	2–5 minutes
📈 Evaluation Metric
BLEU (Bilingual Evaluation Understudy) score is used to measure translation quality by comparing predicted sentences with reference translations.

💾 Output
Trained model file: transformer_translation.pth
Console logs with Loss and BLEU scores
📚 Key Concepts Learned
Transformer Architecture
Self-Attention Mechanism
Positional Encoding
Sequence Modeling
Machine Translation
BLEU Score Evaluation
✅ Conclusion
The Transformer-based Seq2Seq model successfully learns English-to-Spanish translation. The experiment demonstrates that attention-based architectures provide improved performance and faster convergence compared to traditional recurrent neural networks.

👨‍💻 Author
Pratyaksh Kumar M.Tech Artificial Intelligence
