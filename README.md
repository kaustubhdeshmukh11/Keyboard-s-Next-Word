# LSTM-Based Next Word Prediction Tool

A proof-of-concept implementation of a next-word prediction system using an LSTM neural network. The core pipeline is contained in a single Jupyter notebook (`keyboard.ipynb`), which handles data preprocessing, model definition, training, and evaluation. 

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Requirements](#requirements)   

---

## Project Overview

This project builds an LSTM-based next-word prediction tool using Python, Keras, TensorFlow. Given a large text corpus, it performs all necessary preprocessing steps, constructs an LSTM model, and trains it to predict the most likely next word in a sequence. The entire workflow is contained in one Jupyter notebook (`.ipynb`), which you can execute end-to-end or step through to inspect intermediate outputs.

---

## Features

1. **Text Preprocessing & Sequence Generation**  
   - Tokenizes input corpus. 
   - Builds a word-index mapping (vocabulary) and converts raw text into integer sequences.  
   - Uses sliding-window batching (sequence length \(= N\)) to generate input–output pairs for training.  

2. **LSTM Model Definition & Training**  
   - Defines a multi-layer LSTM network in Keras:  
     - Embedding layer → turns each token index into a dense vector.  
     - One or more LSTM layers to capture temporal dependencies.  
     - Dense (softmax) output layer over the vocabulary for next-word probabilities.  
   - Specifies hyperparameters:  
     - Embedding dimension (e.g., 100 or 200).  
     - Sequence length (e.g., 20 tokens per input).  
     - Number of LSTM units, dropout rates, activation functions.  
     - Batch size, learning rate, number of epochs.  
   - Compiles the model with categorical cross-entropy loss and trains it on the generated sequences.  

---

## Requirements

- Python 3.7+  
- Jupyter Notebook  
- TensorFlow 2.x  
- Keras (usually bundled with TensorFlow 2.x)  
- Pandas (for any auxiliary data handling)  
- (Optional) Matplotlib or Seaborn if you wish to visualize training curves  



