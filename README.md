# Perspectives on Infertility in Chinese Social Media: A Comparative Content Analysis

This is a Python-based Natural Language Processing (NLP) project designed to explore the evolution of public discourse, attitudes, and social psychology regarding "infertility" on Sina Weibo. By comparing datasets from **2018** and **2023**, the study identifies shifting socio-cultural trends over a five-year span.

[简体中文](./README_zh.md) | **English**

---

## 🌟 Project Highlights

- **Comparative Analysis**: Investigates shifts in public anxiety, attitudes toward Assisted Reproductive Technology (ART), and responses to population policies across two distinct time points.
- **Automated Preprocessing**: Features custom regex-based cleaning for Weibo's unique `#Topic#` formats and batch generalization of sensitive entities (cities, doctors, and hospitals).
- **Intelligent Semantic Filtering**: Integrated Large Language Model (LLM) APIs to automatically identify and filter out noisy or irrelevant text.
- **Deep Text Mining**: Leverages TF-IDF weighting, LDA (Latent Dirichlet Allocation) topic modeling, and K-Means clustering for robust thematic discovery.

## 🛠 Environment & Dependencies

The project has been tested and verified with the following core libraries:

### Core Processing Logic:
* **Data Handling**: `pandas`, `numpy`, `openpyxl`
* **NLP & Tokenization**: `jieba`
* **Machine Learning**: `scikit-learn` (LDA, KMeans, PCA, CountVectorizer)
* **Visualization**: `matplotlib`, `wordcloud`, `mglearn`
* **Networking**: `requests` (for LLM API interactions)

## 📂 File Structure

* `2018.ipynb`: Main analysis pipeline for the 2018 Weibo dataset.
* `2023.ipynb`: Main analysis pipeline for the 2023 Weibo dataset.
* `low_2018.xlsx` / `low_2023.xlsx`: Raw scraped Weibo datasets.
* `stop_words.txt`: Optimized Chinese stop-words dictionary for tokenization.

## 🚀 Quick Start

1. **Data De-identification**:
   The program automatically invokes the `replace_sensitive_words` function. This replaces specific hospital and physician names with generic tags (e.g., "Hospital", "Doctor") to comply with research ethics and privacy standards.

2. **Topic Extraction**:
   Run the LDA modules to iterate through different topic counts $k \in [3, 6]$. The system utilizes `mglearn` to output the top 20 high-frequency keywords for each identified theme.

3. **Result Visualization**:
   Execute the visualization cells to generate Word Clouds and PCA-reduced (Principal Component Analysis) cluster distribution maps.

## 📊 Methodology

This project utilizes a **Comparative Content Analysis** framework:

1. **Text Acquisition**: Keyword-based data retrieval from the Sina Weibo platform.
2. **Relevance Filtering**: LLM-assisted "Yes/No" relevance labeling to ensure high-quality data input.
3. **Feature Engineering**: Construction of a TF-IDF Document-Term Matrix.
4. **Thematic Evolution**: Analysis of Topic Weight distributions in LDA models to track shifts in social hotspots between 2018 and 2023.

---
*Note: This project is strictly for academic research purposes.*