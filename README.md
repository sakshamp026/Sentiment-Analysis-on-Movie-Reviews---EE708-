
# 🎬 Sentiment Analysis of Movie Reviews  
*Using BiLSTM and Word2Vec*

## 📌 Overview

This project performs **binary sentiment classification** (positive/negative) on movie reviews using a deep learning model built with **Bidirectional LSTM layers** and **Word2Vec embeddings**. The system achieves **~88% accuracy** and provides a strong, efficient alternative to transformer-based models like BERT.

---

## 📁 Repository Structure

```
├── best_model.h5                         # Trained BiLSTM model
├── word2vec_model (1).model             # Pre-trained Word2Vec embeddings
├── SentimentAnalysisCodeImplementation_Group23.ipynb  # Main implementation notebook
├── Evaluation_Script_Team_23.ipynb      # Evaluation script with performance metrics
├── EE708_Report_final.pdf               # Detailed report with model insights
```

---

## ⚙️ How It Works

1. **Text Preprocessing**  
   - Lowercasing, HTML & special character removal  
   - Tokenization & lemmatization  
   - Word2Vec vectorization (100-dim)  
   - Padding to fixed length (200 tokens)

2. **Model Architecture**  
   - Two stacked **Bidirectional LSTM layers**
   - Dense layers with **ReLU** and **Dropout**
   - Final **sigmoid layer** for binary output

3. **Training Details**  
   - 25,000 labeled reviews  
   - Optimizer: Adam | Loss: Binary Crossentropy  
   - EarlyStopping & ModelCheckpoint used  
   - Accuracy: **87.7%**, F1: **0.876**

---

## 🧠 Why LSTM + Word2Vec?

- Word2Vec captures **semantic meaning**
- BiLSTM understands **context from both directions**
- Together, they offer strong generalization and interpretability

---

## 🏁 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/your-username/sentiment-analysis-lstm.git
cd sentiment-analysis-lstm
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
Open `SentimentAnalysisCodeImplementation_Group23.ipynb` in Jupyter or VSCode and run all cells.

> Make sure the `word2vec_model (1).model` and `best_model.h5` files are in the same directory.

---

## 📊 Results

| Metric     | Value    |
|------------|----------|
| Accuracy   | 87.7%    |
| Precision  | 89.27%   |
| Recall     | 86.00%   |
| F1 Score   | 87.61%   |
| Loss       | 0.2894   |

---

## 📈 Comparison with Other Models

| Model                      | Accuracy |
|---------------------------|----------|
| Logistic Regression       | 83.78%   |
| SVM (Linear)              | 82.29%   |
| Multinomial Naive Bayes   | 82.09%   |
| **LSTM + Word2Vec (Ours)**| **87.7%** |
| BERT                      | 88.74%   |

---

## 📚 References

- [Understanding LSTMs](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- [Word2Vec Explanation](https://radimrehurek.com/gensim/models/word2vec.html)
- [Sentiment Analysis Deep Dive](https://javilopezcastillo.medium.com/sentiment-analysis-using-lstm-networks-a-deep-dive-into-textual-data-61cdd2e43dec)

---

## 👩‍💻 Contributors

- Dharvi Singhal  
- Riya Agarwal  
- **Saksham Parihar**  
- Samyak Jain  

---

## 📄 License

This project is intended for academic and educational use only.
