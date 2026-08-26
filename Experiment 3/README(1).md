# Experiment 3: Stemming, Lemmatization and Regular Expressions

## Overview

This experiment demonstrates fundamental Natural Language Processing (NLP) techniques using Python. The notebook focuses on text preprocessing and information extraction through:

- Stemming using Porter Stemmer
- Lemmatization using WordNet Lemmatizer
- Information extraction using Regular Expressions

## Technologies Used

- Python
- NLTK
- Regular Expressions (`re`)
- Jupyter Notebook

## Installation

Install the required Python library:

```bash
pip install nltk
```

## Usage

Run the Jupyter Notebook:

```bash
jupyter notebook "Experiment_3 (1).ipynb"
```

## Experiment Components

### 1. Stemming

The experiment uses NLTK's `PorterStemmer` to reduce words to their stem or root form.

Example words include:

- playing
- played
- plays
- studies
- studying
- connected
- connection
- computers

### 2. Lemmatization

The experiment uses `WordNetLemmatizer` to convert words into their base or dictionary form.

Download the required WordNet resource:

```python
import nltk

nltk.download("wordnet")
```

### 3. Regular Expressions

Regular Expressions are used to extract structured information from text, including:

- Email addresses
- URLs
- Mobile numbers
- Hashtags
- Social media mentions

## Learning Outcomes

After completing this experiment, you will understand:

- The concept of stemming
- The concept of lemmatization
- The difference between stemming and lemmatization
- How to use NLTK for text processing
- How to use Regular Expressions for information extraction

## Author

**Experiment:** Experiment 3  
**Topic:** Stemming, Lemmatization and Regular Expressions

## License

This project is intended for educational purposes.
