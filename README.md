# Large Language Models - Homework 1

This homework is part of the **Large Language Model** course and explores different NLP model architectures, including N-Gram, RNN, and Transformer models, using real-world datasets.

---

## 📚 Table of Contents

- [📁 Dataset Description](#-dataset-description)
- [🧠 Part 1: N-Gram Model](#-part-1-n-gram-model)
- [🔁 Part 2: RNN Model](#-part-2-rnn-model)
- [🧲 Part 3: Self-Attention Layer in Transformer](#-part-3-self-attention-layer-in-transformer)
- [📊 Comparison and Analysis](#-comparison-and-analysis)
- [⚙️ Environment & Tools](#️-environment--tools)
- [🚫 Note](#-note)

---

## 📁 Dataset Description

- **Part 1 & 2**: Recipe step sentences from `Food.com Recipes and Interactions`  
  - `train.txt`: ~2.6M entries  
  - `test.txt`: ~650K entries  
  - `incomplete.txt`: 10 incomplete sentences

- **Part 3**: Emotion classification dataset  
  - `train.csv`, `val.csv`, `test.csv`  
  - Each line contains a sentence and its corresponding emotion tag (5 total emotions)

---

## 🧠 Part 1: N-Gram Model

Implemented bigram (n=2) and trigram (n=3) models from scratch using Python's `defaultdict`.

- ✅ **Test Accuracy**: ~24% to 25%, within the expected threshold.
- ✏️ **Sentence Completion**: Used the trigram model to extend each incomplete sentence to 20 words.

---

## 🔁 Part 2: RNN Model

Built an RNN using **PyTorch** with the following hyperparameters:

- `hidden_size = 128`  
- `num_layers = 2`  
- `learning_rate = 0.001`  
- `epochs = 10`  
- `batch_size = 32`  

### Results:
- 📉 Plotted training loss and accuracy curves.
- 🧪 Evaluated model accuracy on `test.txt`.
- ✍️ Used the model to complete the same 10 incomplete sentences from Part 1 and compared the results with the N-gram model.

---

## 🧲 Part 3: Self-Attention Layer in Transformer

This part focuses on implementing the core components of a Transformer model for emotion classification.

- 🧩 Completed the **Multi-head Attention** and **Transformer Encoder Layer** from scratch.
- 📈 Trained the model on the provided dataset. It achieved the expected accuracy threshold.
- ⚙️ Experimented with different **numbers of attention heads** (1, 4, 8) to observe performance variation.
  - The number of heads significantly impacted the model’s performance and training behavior.

---

## 📊 Comparison and Analysis

Compared the models based on:

- ✅ Accuracy  
- ⏱️ Computation time  
- 🧠 Memory and hardware usage  
- ✍️ Quality of sentence completion (N-Gram vs. RNN)  
- 🧲 Effect of attention heads on Transformer model performance

---

## ⚙️ Environment & Tools

- Python 3.x  
- PyTorch  
- `NumPy`, `Pandas`, `collections`, etc.  
- GPU support for RNN and Transformer training  
- No use of advanced NLP libraries for restricted parts (e.g., no `torch.nn.MultiheadAttention`)

---

## 🚫 Note

All implementations were done independently following assignment guidelines. No plagiarism or use of restricted libraries.
