# Text Mining and Natural Language Processing Home Assignment

## AI-Assisted Customer Support Analysis and Retrieval from Twitter

### Project Overview

This project focuses on analyzing customer service tweets using text mining and natural language processing techniques. The work includes data exploration, classical machine learning, neural models, and search methods for retrieving relevant tweets based on user queries.

The main goal is to understand customer complaints and build different search approaches that can return useful tweets from the dataset.

## Dataset

We use the Customer Support on Twitter dataset from Kaggle.
The dataset contains Twitter conversations between customers and company support accounts. It includes tweet text, author information, whether the tweet is inbound, and conversation links.

[Access Dataset](https://www.kaggle.com/datasets/thoughtvector/customer-support-on-twitter)

## Project Tasks

The project includes:

1. Data exploration and preparation
2. Classic machine learning model for classification
3. Fine-tuned neural model for classification
4. Prompting-based model for classification
5. TF-IDF search engine
6. Neural embedding search engine
7. Hybrid search engine

## Project Structure

```text
Data/
│── classic_model_tuning_results.csv
│── final_tweets.csv
│── manual_prompt_predictions.csv
│── manual_prompt_true_labels.csv
│── manual_prompts.csv
│── test_tweets.csv
│── top_company_tweets.csv
│── train_tweets.csv
│── twcs.csv
│── val_tweets.csv

Notebooks/
│── 01_data_exploration.ipynb
│── 02_classic_model.ipynbS
│── 03_neural_model_distilbert.ipynb
│── 04_prompting_model.ipynb
│── 05_tfidf_search.ipynb
│── 06_embedding_search.ipynb
│── 07_hybrid_search.ipynb

results/
│── figures/
│── models/
│── tables/

.gitignore
README.md
requirements.txt
```
## Notebooks

### 01_data_exploration.ipynb
Explores the dataset, checks missing values, class distribution, tweet lengths, companies, and basic text patterns.

### 02_classic_model.ipynb
Builds a classical machine learning classification model using TF-IDF features and compares different parameter settings.

### 03_neural_model_distilbert.ipynb
Uses a DistilBERT-based neural model for classification and compares it with the classic model.

### 04_prompting_model.ipynb
Uses manually designed prompts for classification and compares the generated predictions with the true labels.

### 05_tfidf_search.ipynb
Implements a TF-IDF search engine that retrieves tweets based on keyword similarity.

### 06_embedding_search.ipynb
Implements a neural embedding search engine that retrieves tweets based on semantic similarity.

### 07_hybrid_search.ipynb
Combines TF-IDF search and embedding search to create a hybrid retrieval method.

## Search Methods

Three search methods were implemented:

1. **TF-IDF Search**  
   Works well when the query words appear directly in the tweets.

2. **Neural Embedding Search**  
   Captures the meaning of the query and can find tweets with similar intent even when the wording is different.

3. **Hybrid Search**  
   Combines keyword similarity and semantic similarity to produce more balanced search results.

## Example Search Queries

The search methods were tested using the following queries:

```text
flight delayed customer service
refund for cancelled order
app not working
bad customer support
lost baggage complaint
```

## How to Run the Project

Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install the required packages:

```powershell
python -m pip install -r requirements.txt
```

Then open the notebooks in VS Code or Jupyter Notebook and run them from top to bottom.

## Requirements

The main Python libraries used in this project are:

```text
pandas
numpy
scikit-learn
sentence-transformers
torch
transformers
matplotlib
seaborn
jupyter
ipykernel
ipywidgets
```

## Conclusion

This project demonstrates how different NLP techniques can be used to analyze and retrieve customer support tweets. The classical TF-IDF model provides a simple and useful baseline, while the neural model adds more advanced language understanding. For search, TF-IDF works well for exact keyword matches, neural embedding search captures meaning better, and hybrid search combines both strengths to provide more reliable results.