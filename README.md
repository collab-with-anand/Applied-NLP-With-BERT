# Applied NLP: A Toolkit for Text Classification & Topic Modeling

This repository provides a collection of practical, hands-on notebooks for common Natural Language Processing (NLP) tasks. It serves as a toolkit for comparing different architectures, including Transformer-based (BERT) and RNN-based (BiLSTM) models.

## 🚀 Project Components

This repository is broken down into four key demonstrations, each in its own notebook within the `/notebooks` directory.

### 1. Unsupervised Topic Modeling (BERTopic)
* **Notebook:** `1_Topic_Modeling_BERTopic.ipynb`
* **Task:** Unsupervised topic modeling on the US Airline Tweets dataset.
* **Method:** Uses the **`bertopic`** library, which leverages BERT embeddings for document clustering. It demonstrates how to extract and visualize topics, their relationships (heatmaps, hierarchy), and their evolution over time.

### 2. Sentiment Analysis (BERT via TensorFlow Hub)
* **Notebook:** `2_Sentiment_Analysis_BERT_TFHub.ipynb`
* **Task:** Binary sentiment analysis on IMDB movie reviews.
* **Method:** Fine-tunes a `small_bert` model loaded from **TensorFlow Hub (`tfhub`)** within a simple Keras workflow, integrating a `tensorflow_text` preprocessing layer directly into the `tf.keras.Model`.

### 3. Sentiment Analysis (BERT via Hugging Face)
* **Notebook:** `3_Sentiment_Analysis_BERT_Transformers.ipynb`
* **Task:** Binary sentiment analysis on IMDB movie reviews.
* **Method:** Uses the **Hugging Face `transformers`** library (`TFBertForSequenceClassification`) and shows a more manual data processing pipeline using `InputExample` and `InputFeatures` for greater control.

### 4. Text Classification (BiLSTM with Attention)
* **Notebook:** `4_Text_Classification_BiLSTM_Attention.ipynb`
* **Task:** Multi-class text classification on the 20 Newsgroups dataset.
* **Method:** Implements a **Bidirectional LSTM (BiLSTM)** with a **custom Attention layer** in TensorFlow/Keras. This demonstrates a powerful RNN-based architecture that serves as an excellent comparison to the Transformer models.

---

## 🛠️ Setup and Installation

To run this project, follow these steps.

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/Applied-NLP-Toolkit.git](https://github.com/your-username/Applied-NLP-Toolkit.git)
    cd Applied-NLP-Toolkit
    ```

2.  **Create a Virtual Environment** (Recommended)
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install Required Libraries**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download spaCy Model**
    The topic modeling notebook (`1_Topic_Modeling_BERTopic.ipynb`) requires a spaCy model.
    ```bash
    python -m spacy download en_core_web_lg
    ```

5.  **Launch Jupyter**
    ```bash
    jupyter notebook
    ```
    Navigate to the `/notebooks` directory to run the examples.

---

## 📊 Datasets

* **IMDB Movie Reviews:** Used by the sentiment analysis notebooks. The data is downloaded automatically by the scripts.
* **Twitter US Airline Sentiment:** Used by the topic modeling notebook. The `Tweets.csv` file is included in the `/data` directory.
* **20 Newsgroups:** Used by the BiLSTM notebook. The notebook expects `newsgroups-train.json` and `newsgroups-test.json`. These can be acquired from public sources (like Kaggle) or generated using `sklearn.datasets.fetch_20newsgroups`.
