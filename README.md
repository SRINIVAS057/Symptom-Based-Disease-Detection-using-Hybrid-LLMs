<h1>🧠 Symptom-Based Disease Detection using Hybrid LLMs</h1>

<h3>🚀 Project Overview</h3>

This project aims to build an AI-driven medical assistant that predicts possible diseases based on symptom descriptions provided by users. The system leverages hybrid transformer-based language models (LLMs) to understand clinical symptom patterns and classify diseases with higher accuracy and interpretability.

We developed and compared three hybrid deep learning models:

XLM-RoBERTa + ERNIE

ERNIE + ELECTRA

ELECTRA + XLNet

Each hybrid model captures complementary linguistic and contextual information from medical symptom datasets to enhance diagnostic precision.

<h3>🩺 Motivation</h3>

Traditional symptom-based disease detection systems often rely on rule-based or single-model approaches, which struggle to handle ambiguous or overlapping symptoms.
By fusing two complementary LLMs, this project aims to:

Improve multi-symptom understanding

Reduce false positives in diagnosis

Provide a more reliable disease prediction framework

<h3>🧩 Hybrid Model Architecture</h3>

Each hybrid model follows this pipeline:

Symptom Encoding:
The input symptoms are tokenized and embedded using two pretrained transformer encoders.

Feature Fusion:
The contextual embeddings from both models are concatenated or averaged to form a hybrid feature representation.

Classification Layer:
A dense neural layer maps the fused features to the disease output class.

<h3>🧬 Models Used:</h3>

| Model Pair              | Description                                                                                     | Key Strengths                                          |
| ----------------------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| **XLM-RoBERTa + ERNIE** | Combines multilingual context (XLM-RoBERTa) with knowledge-enhanced text understanding (ERNIE). | Excellent for semantic comprehension of medical terms. |
| **ERNIE + ELECTRA**     | Integrates knowledge-based reasoning (ERNIE) with efficient token discrimination (ELECTRA).     | High-speed training and contextual robustness.         |
| **ELECTRA + XLNet**     | Merges ELECTRA’s replaced-token detection with XLNet’s permutation-based learning.              | Strong bidirectional context and generalization.       |


<h3>📂 Dataset</h3>

Dataset Type: diseases-and-symptoms-dataset
Records: 246,000+ samples
Attributes: Symptom_1, Symptom_2, ..., Symptom_n, Disease
Format: CSV
Source: Curated symptom-based medical datasets (cleaned and preprocessed)

<h3>⚙️ Methodology</h3>

1.Data Preprocessing
  Tokenization, text normalization, and label encoding.

2.Feature Extraction
  Contextual embeddings from LLM pairs.

3.Feature Fusion
  Concatenation of embeddings or attention-based fusion.

4.Model Training
  Fine-tuning using Adam optimizer and cross-entropy loss.

5.Evaluation
  Classification report, confusion matrix, and F1-scores.


<h3>📊 Results Summary</h3>

| **Model**           | **Precision** | **Recall** | **F1-Score** |
| ------------------- | ------------- | ---------- | ------------ |
| XLM-RoBERTa + ERNIE | 0.823         | 0.816      | 0.816        |
| ELECTRA + ERNIE     | 0.826         | 0.820      | 0.812        |
| XLNet + ELECTRA     | 0.826         | 0.816      | 0.820        |

