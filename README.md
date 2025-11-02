# Applied NLP with BERT: A Toolkit for Sentiment Analysis and Topic Modeling

This project demonstrates and compares different methods for applying BERT to common Natural Language Processing tasks. It provides hands-on examples for both **supervised text classification** (sentiment analysis) and **unsupervised text mining** (topic modeling).

## 🚀 Project Components

This repository is broken down into three main demonstrations, each contained in its own notebook within the `/notebooks` directory.

### 1. Sentiment Analysis (Method 1: TensorFlow Hub + Keras)
* **Notebook:** `1_Sentiment_Analysis_TFHub.ipynb`
* **Goal:** To build a sentiment classifier by fine-tuning a BERT model directly within a Keras workflow.
* **Key Features:**
    * Uses **TensorFlow Hub (`tfhub`)** to load a `small_bert` model.
    * Integrates a matching preprocessing layer from `tensorflow_text` directly into the `tf.keras.Model`.
    * Demonstrates a simple and efficient way to fine-tune a model for a custom dataset (IMDB reviews).

### 2. Sentiment Analysis (Method 2: Hugging Face Transformers)
* **Notebook:** `2_Sentiment_Analysis_Transformers.ipynb`
* **Goal:** To build a sentiment classifier using the Hugging Face `transformers` library.
* **Key Features:**
    * Uses `TFBertForSequenceClassification` from the `transformers` library.
    * Shows a more manual data processing pipeline using `InputExample` and `InputFeatures`.
    * This approach is powerful when you need more granular control over the tokenization and model configuration.

### 3. Topic Modeling (BERTopic)
* **Notebook:** `3_Topic_Modeling_BERTopic.ipynb`
* **Goal:** To perform unsupervised topic modeling on the US Airline Tweets dataset to discover key themes and complaints.
* **Key Features:**
    * Uses the **`bertopic`** library, which leverages BERT embeddings for document clustering.
    * Demonstrates how to extract and visualize topics, topic relationships (heatmaps, hierarchy), and topic evolution over time.

---

## 🛠️ Setup and Installation

To run this project, follow these steps.

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/Applied-NLP-with-BERT.git](https://github.com/your-username/Applied-NLP-with-BERT.git)
    cd Applied-NLP-with-BERT
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
    The topic modeling notebook (`3_Topic_Modeling_BERTopic.ipynb`) requires a spaCy model.
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

* **IMDB Movie Reviews:** Used by both sentiment analysis notebooks. The data is downloaded automatically by the scripts from `https://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz`.
* **Twitter US Airline Sentiment:** Used by the `3_Topic_Modeling_BERTopic.ipynb` notebook. The `Tweets.csv` file is included in the `/data` directory.
