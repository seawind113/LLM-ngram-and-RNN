# Large Language Models - Homework 1 Part 1

This project is the first part of an assignment for the **Large Language Model** course, using a dataset sampled from the ["Food.com Recipes and Interactions"](https://www.kaggle.com/datasets) dataset. The goal is to build language models that predict the next token in recipe step instructions.

---

## 📁 Dataset Description

- **Training data**: `train.txt` (~2.6M entries)  
- **Test data**: `test.txt` (~650K entries)  
- **Sentence completion**: `incomplete.txt` (10 incomplete sentences)  

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

## 📊 Comparison and Analysis

Compared the N-gram and RNN models based on:
- Prediction accuracy
- Computation time
- Hardware resource usage
- Sentence completion quality

---

## ⚙️ Environment & Tools

- Python 3.x  
- PyTorch  
- Basic libraries: `NumPy`, `Pandas`, `collections`, etc.  
- **No advanced NLP libraries** (e.g., no `scikit-learn` or `torch.nn.MultiheadAttention` used for N-gram or Attention parts, as per the assignment rules)
