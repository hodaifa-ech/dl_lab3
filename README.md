# 🧠 Arabic NLP: Classification & Text Generation with Deep Learning

This project is a two-part NLP system focused on the Arabic language:

---

## 🧩 Part 1: Classification Task (RNN, LSTM, GRU)

We scrape Arabic text data related to a specific topic (e.g., education, technology, politics), label them with relevance scores (0-10), and train multiple deep learning models for text classification.

### 🔧 Tools & Technologies
- Python
- BeautifulSoup (Web scraping)
- TensorFlow / Keras
- Arabic NLP tools (Stopwords, Stemming, etc.)
- RNN, Bidirectional RNN, GRU, LSTM
- BLEU Score, Accuracy, F1

### 🛠️ Steps:
1. **Data Collection**: Web scraped Arabic text with BeautifulSoup from trusted websites.
2. **Dataset Format**:
    | Text (Arabic) | Score |
    |---------------|-------|
    | النص الأول     | 6     |
    | النص الثاني    | 7.5   |

3. **Preprocessing Pipeline**:
    - Normalization
    - Tokenization
    - Arabic stopwords removal
    - Lemmatization / Stemming
    - Discretization of the score (rounded to integer)

4. **Model Architectures**:
    - Simple RNN
    - Bidirectional RNN
    - GRU
    - LSTM

5. **Hyperparameter Tuning**:
    - Learning Rate
    - Batch Size
    - Dropout
    - Optimizer

6. **Evaluation Metrics**:
    - Accuracy
    - F1 Score
    - BLEU Score (optional)

7. **Results**:
    - LSTM showed the best generalization ability.
    - Bidirectional RNN captured context well for longer sentences.
    - GRU achieved fast convergence.

---

## 🤖 Part 2: Transformer for Arabic Text Generation

We fine-tuned the GPT-2 Transformer model using Hugging Face Transformers library on a small custom dataset of Arabic sentences, and generated coherent Arabic paragraphs from prompts.

### 🔧 Tools & Technologies
- Hugging Face `transformers`
- GPT-2 Pretrained Model
- PyTorch
- Google Colab
- Custom Arabic Text Corpus

### 🛠️ Steps:
1. **Install Requirements**:
   ```bash
   pip install transformers datasets torch

2. **Fine-tuning GPT-2:**:


Tokenized with GPT-2 tokenizer

Trained using Hugging Face Trainer

Used early stopping and small batch sizes for efficient training on Colab GPU

## 📊 Sample Results

### Classification Accuracy:

Model	Accuracy	F1 Score
RNN	72.5%	0.69
Bi-RNN	76.2%	0.73
GRU	78.1%	0.75
LSTM	81.4%	0.79
