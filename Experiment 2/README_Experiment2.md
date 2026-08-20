# Experiment 2: Basic Text Preprocessing

## 📌 Project Overview

This project demonstrates fundamental **Natural Language Processing (NLP)** text preprocessing techniques using Python.

The notebook performs three main experiments:

1. **Basic Text Preprocessing**
2. **Tokenization**
3. **Stop Word Removal**

The project uses libraries such as **NLTK**, **spaCy**, and Python's built-in modules to process and analyze text data.

## 🛠️ Technologies and Libraries Used

- Python
- NLTK
- spaCy
- Regular Expressions (`re`)
- String Module (`string`)
- Jupyter Notebook / Google Colab

## 📂 Project Structure

```text
Experiment-2-NLP/
│
├── Experiment2_NLP.ipynb
├── data/
│   ├── 2.1_text_data.txt
│   ├── 2.2_tokenization_data.txt
│   └── 2.3_clean_data.txt
│
└── README.md
```

## 🧪 Experiments Performed

### Experiment 2.1: Basic Text Preprocessing

This experiment performs basic cleaning operations on a text file:

- Counting uppercase characters
- Converting text to lowercase
- Identifying punctuation characters
- Removing punctuation
- Identifying digits
- Removing digits
- Removing extra whitespace

Example:

```python
def experiment_2_1(file_path):
```

#### Reading the File

```python
with open(file_path, 'r') as f:
    text = f.read()
```

#### Counting Uppercase Characters

```python
upper_count = sum(1 for c in text if c.isupper())
```

#### Converting Text to Lowercase

```python
text = text.lower()
```

#### Removing Punctuation

```python
text = "".join(c for c in text if c not in string.punctuation)
```

#### Removing Digits

```python
text = "".join(c for c in text if not c.isdigit())
```

#### Removing Extra Whitespace

```python
cleaned = " ".join(text.split())
```

### Experiment 2.2: Tokenization

This experiment demonstrates tokenization using:

- NLTK
- spaCy
- Pure Python

Tokenization splits text into smaller units such as words and sentences.

#### NLTK Word Tokenization

```python
nltk.word_tokenize(raw_text)
```

#### NLTK Sentence Tokenization

```python
nltk.sent_tokenize(raw_text)
```

#### spaCy Tokenization

Load the English language model:

```python
nlp = spacy.load('en_core_web_sm')
```

Process the text:

```python
doc = nlp(raw_text)
```

Extract tokens:

```python
[t.text for t in doc]
```

Extract sentences:

```python
[s.text for s in doc.sents]
```

#### Pure Python Tokenization

Word tokenization:

```python
words = raw_text.split()
```

Sentence tokenization:

```python
sents = re.split(r'(?<=[.!?]) +', raw_text)
```

### Experiment 2.3: Stop Word Removal

This experiment removes common English stop words from text.

Examples include:

```text
the
is
and
in
of
to
```

Convert text to lowercase:

```python
text = f.read().lower()
```

Tokenize the text:

```python
tokens = nltk.word_tokenize(text)
```

Load English stop words:

```python
stop_words = set(stopwords.words('english'))
```

Identify stop words:

```python
isolated_stops = [t for t in tokens if t in stop_words]
```

Remove stop words and punctuation tokens:

```python
filtered = [
    t for t in tokens
    if t not in stop_words and t.isalnum()
]
```

## 📦 Installation

Install the required libraries:

```bash
pip install nltk spacy
```

Download the spaCy English language model:

```bash
python -m spacy download en_core_web_sm
```

The notebook downloads the required NLTK resources:

```python
nltk.download('punkt_tab')
nltk.download('stopwords')
```

## ▶️ How to Run

1. Clone or download the project.
2. Open `Experiment2_NLP.ipynb`.
3. Place the required text files in the `data` folder or update the file paths.
4. Install the required libraries.
5. Run the notebook cells sequentially.

If using Google Colab:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Update the file paths according to your Google Drive location.

## 📚 Concepts Covered

- Text preprocessing
- Text normalization
- Lowercasing
- Punctuation removal
- Digit removal
- Whitespace normalization
- Word tokenization
- Sentence tokenization
- NLTK tokenization
- spaCy tokenization
- Regular expressions
- Stop word identification
- Stop word removal

## 🎯 Learning Objectives

After completing this experiment, you will understand how to:

- Read text files using Python
- Clean raw textual data
- Normalize text
- Remove unwanted characters
- Tokenize text into words and sentences
- Compare tokenization methods
- Use NLTK for NLP tasks
- Use spaCy for NLP processing
- Remove English stop words
- Prepare text data for further NLP analysis

## 📊 Conclusion

This project introduces essential text preprocessing techniques used in Natural Language Processing. It demonstrates how raw text can be cleaned, tokenized, and filtered before being used for further NLP tasks such as text classification, sentiment analysis, information retrieval, and machine learning.
