# Next Word Prediction using LSTM (PyTorch)

A deep learning project that implements a **Next Word Prediction system** using an LSTM-based neural network in PyTorch. The model learns patterns from raw text data and predicts the most likely next word given a sequence of input words.

This project was built for **learning purposes**, focusing on Natural Language Processing (NLP), sequence modeling, and deep learning fundamentals.

---

## 📌 Project Overview

The objective of this project is to build a language model capable of:
- Predicting the next word in a sequence
- Generating text from a given seed sentence
- Understanding contextual relationships between words

The model is trained on a large text corpus and learns to approximate natural language structure using sequential modeling.

---

## 📊 Dataset

This project uses the following Kaggle dataset:

🔗 https://www.kaggle.com/datasets/ronikdedhia/next-word-prediction

### Dataset Characteristics:
- Large-scale raw text data (book-style corpus)
- Contains Project Gutenberg-style text content
- Requires extensive preprocessing before training
- Includes noise such as headers, metadata, and special formatting

---

## 🛠️ Tech Stack

- Python
- PyTorch
- NumPy
- Pandas
- Matplotlib
- KaggleHub (dataset download utility)
- Regular Expressions (text preprocessing)

---

## 🧠 Model Architecture

The model is based on a **Bidirectional LSTM neural network**:

- Embedding Layer (word representations)
- Dropout Layer (regularization)
- 2-layer Bidirectional LSTM
- Fully Connected Linear Layer
- Softmax activation for probability distribution over vocabulary

### Hyperparameters:
- Sequence Length: 10
- Embedding Dimension: 256
- Hidden Dimension: 512
- Number of LSTM Layers: 2
- Dropout: 0.3
- Optimizer: AdamW
- Loss Function: CrossEntropyLoss
- Batch Size: 128
- Epochs: 10

---

## 🔄 Project Pipeline

### 1. Data Loading
- Dataset downloaded via KaggleHub
- Extracted and loaded into memory

### 2. Data Preprocessing
- Removed metadata (titles, authors, headers)
- Cleaned special characters, URLs, and noise
- Converted text to lowercase
- Tokenized text into words

### 3. Vocabulary Construction
- Built word frequency distribution
- Filtered rare words (minimum frequency = 5)
- Created word-to-index and index-to-word mappings

### 4. Sequence Generation
- Converted tokens into fixed-length sequences
- Each sequence is paired with the next word as target

### 5. Model Training
- Trained using LSTM-based architecture
- Applied gradient clipping for stability
- Used learning rate scheduler for optimization

### 6. Evaluation
- Monitored training and validation loss
- Visualized performance using loss curves

---

## 📈 Key Learnings

This project provided practical experience in several areas:

### ✔️ Importance of Text Preprocessing
Raw text data contains noise that significantly affects model performance if not cleaned properly.

### ✔️ Sequence Modeling with LSTM
LSTMs are effective for capturing sequential dependencies in language.

### ✔️ Impact of Vocabulary Design
Reducing rare words improves training stability but may reduce semantic richness.

### ✔️ Training Stability Techniques
Gradient clipping helps prevent exploding gradients during training.

### ✔️ Overfitting Behavior
Validation performance highlighted the need for better regularization or more diverse data.

---

## 🚀 Future Improvements

This project can be further enhanced in the following ways:

- Replace LSTM with Transformer-based architectures (e.g., GPT-style models)
- Use advanced tokenization techniques (BPE, WordPiece)
- Train on larger and more diverse datasets
- Perform hyperparameter optimization
- Implement beam search for improved text generation
- Deploy as a web application using Flask/FastAPI + frontend UI

