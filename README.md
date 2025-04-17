# LLM-ngram-and-RNN
Large Language Models - Homework 1
This project is the first part of an assignment for the LLM course, based on the Food.com Recipes and Interactions dataset (steps portion only). The task was to build language models that predict the next token in recipe step sentences.

Part 1: N-Gram Model
I implemented both bigram (n=2) and trigram (n=3) models using a custom Python implementation. The model was trained on train.txt (about 2.6 million entries), and its prediction accuracy was evaluated on test.txt (about 650K entries).

Test Accuracy: Around 24% to 25%, which falls within the expected threshold.

Sentence Completion: The trigram model was also used to complete 10 incomplete sentences from incomplete.txt, each extended to a length of 20 words.

Part 2: RNN Model
Using PyTorch, I built a Recurrent Neural Network (RNN) with the following hyperparameters:

Hidden size: 128

Number of layers: 2

Learning rate: 0.001

Epochs: 10

Batch size: 32

The model was trained on the same dataset and used to:

Plot training loss and accuracy curves.

Predict tokens on the test set and calculate accuracy.

Complete the same incomplete sentences from Part 1 for comparison with the n-gram results.
