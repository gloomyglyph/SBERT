# Summary: Semantic Search Engine using Sentence-BERT (SBERT)

## Overview

This project implements a semantic search engine using the Quora Question Pairs dataset and the Sentence-BERT (SBERT) model. The goal is to retrieve semantically similar questions based on user input, leveraging embeddings to understand the meaning of sentences.

## Key Components

### 1. Introduction

- **Objective**: To build a semantic search engine that retrieves relevant questions based on user queries, focusing on semantic meaning rather than exact matches.
- **Dataset**: Utilizes the Quora Question Pairs dataset, which consists of pairs of questions that may be semantically similar.

### 2. Libraries Used

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations and array handling.
- **Regular Expressions (re)**: For text processing and cleaning.
- **Sentence Transformers**: To load the pre-trained SBERT model for generating sentence embeddings.
- **Scikit-learn**: For calculating cosine similarity between embeddings.

### 3. Data Cleaning

A `clean_text` function is implemented to:
- Convert text to lowercase.
- Remove non-alphabetic characters.
- Replace multiple spaces with a single space and strip leading/trailing spaces.

### 4. Loading the Dataset

The dataset is loaded, and the following operations are performed:
- Cleaning text data in both question columns.
- Removing duplicate entries and handling missing values to maintain data integrity.

### 5. SBERT Model

- **SBERT**: A variant of the BERT model designed for generating sentence embeddings, capturing semantic meanings in a lower-dimensional space, making it efficient for tasks like similarity search.

### 6. Batch Processing for Encoding

Questions are encoded in batches to:
- Manage memory usage effectively.
- Speed up the processing of embeddings.
- The `encode_questions` function handles the encoding of questions in smaller groups.

### 7. User Query and Similarity Calculation

- A user query is transformed into an embedding.
- Cosine similarity is calculated between the query embedding and the question embeddings to find semantically similar questions.
- The top N similar questions are retrieved based on similarity scores.

### 8. Conclusion

The project successfully demonstrates the capability of SBERT to perform semantic searches. By generating embeddings for questions, the system can retrieve relevant queries based on user input, showcasing the power of modern NLP techniques.

## References

- [Sentence Transformers Documentation](https://www.sbert.net/)
- [Quora Question Pairs Dataset](https://www.kaggle.com/c/quora-question-pairs)
