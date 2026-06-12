# 🔤 Word Embedding Similarity Agent

A beginner-friendly NLP (Natural Language Processing) project built using Python and Word2Vec. This agent converts words into numerical vectors (embeddings) and finds semantically similar words based on learned relationships.

The project demonstrates the core concept behind modern AI systems, semantic search, recommendation systems, and Retrieval-Augmented Generation (RAG).

---

# 📌 Project Overview

Computers cannot understand words directly.

Word Embedding is a technique that converts words into numerical vectors while preserving their meaning and relationships.

Example:

```text
Word: Python

Embedding:
[0.123, -0.456, 0.789, ...]
```

Using these vectors, the agent can identify words with similar meanings.

---

# 🚀 Features

✅ Word Embedding Generation

✅ Similar Word Search

✅ Real-Time User Queries

✅ Word2Vec Training

✅ Semantic Similarity Detection

✅ Interactive NLP Agent

✅ Google Colab Compatible

✅ Beginner-Friendly Project

---

# 🛠️ Technologies Used

| Technology   | Purpose                     |
| ------------ | --------------------------- |
| Python       | Programming Language        |
| Gensim       | Word2Vec Implementation     |
| Word2Vec     | Word Embedding Generation   |
| NLP          | Natural Language Processing |
| Google Colab | Development Environment     |

---

# 📂 Project Structure

```text
word-embedding-agent/
│
├── app.ipynb
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

Install the required library:

```bash
pip install gensim
```

---

# 💻 Source Code

## Step 1: Create Dataset

```python
sentences = [

    ["python", "programming", "language"],

    ["machine", "learning", "artificial", "intelligence"],

    ["sql", "database", "query"],

    ["deep", "learning", "neural", "network"],

    ["data", "science", "python"]

]
```

---

## Step 2: Train Word2Vec Model

```python
from gensim.models import Word2Vec

model = Word2Vec(
    sentences,
    vector_size=100,
    window=5,
    min_count=1,
    workers=4
)
```

---

## Step 3: Generate Word Embeddings

```python
word = "python"

vector = model.wv[word]

print(vector)
```

---

## Step 4: Similar Word Search Agent

```python
def word_embedding_agent(word):

    try:

        similar_words = model.wv.most_similar(
            word,
            topn=5
        )

        return similar_words

    except:

        return "Word Not Found"
```

---

## Step 5: Run Agent

```python
while True:

    word = input(
        "Enter Word: "
    )

    if word.lower() == "exit":
        break

    print(
        word_embedding_agent(word)
    )
```

---

# 🔍 Complete Code Explanation

## What is Word2Vec?

Word2Vec is a neural network model that learns vector representations of words.

Words with similar meanings are placed closer together in vector space.

Example:

```text
King → Queen
India → Delhi
Python → Programming
```

---

## What is an Embedding?

An embedding is a numerical representation of a word.

Example:

```text
Python

↓

[0.23, -0.11, 0.78, ...]
```

These numbers capture the meaning of the word.

---

## vector_size

```python
vector_size=100
```

Determines the length of the embedding vector.

Example:

```text
Python

↓

100-dimensional vector
```

---

## window

```python
window=5
```

Defines how many neighboring words the model looks at during training.

---

## min_count

```python
min_count=1
```

Minimum frequency required for a word to be included in training.

---

## workers

```python
workers=4
```

Number of CPU threads used during training.

---

# 🔄 Agent Workflow

```text
Training Data
      │
      ▼
Word2Vec Training
      │
      ▼
Word Embeddings
      │
      ▼
User Word Query
      │
      ▼
Similarity Search
      │
      ▼
Top Similar Words
      │
      ▼
Display Output
```

---

# 📊 Example

## Input

```text
Enter Word:
python
```

## Output

```text
Top Similar Words:

programming ---> 0.82

data ---> 0.79

science ---> 0.75

learning ---> 0.72

language ---> 0.70
```

---

## Another Example

### Input

```text
Enter Word:
learning
```

### Output

```text
Top Similar Words:

machine ---> 0.88

deep ---> 0.84

artificial ---> 0.79

intelligence ---> 0.76

network ---> 0.71
```

---

# 🎯 Applications

* Search Engines
* Chatbots
* Recommendation Systems
* Semantic Search
* NLP Applications
* AI Assistants
* RAG Systems
* Text Similarity Analysis

---

# Advantages

* Learns semantic relationships
* Fast similarity search
* Lightweight implementation
* Easy to understand
* Foundation for advanced NLP

---

# Limitations

* Small dataset produces weak embeddings
* Limited vocabulary
* Cannot understand complex context
* Not as powerful as Transformer models

---

# Future Improvements

* Train on Large Datasets
* Use FastText
* Use GloVe Embeddings
* Use BERT Embeddings
* Build Semantic Search Engine
* Create RAG Agent
* Vector Database Integration
* Streamlit UI

---

# Learning Outcomes

After completing this project, you will understand:

* NLP Fundamentals
* Word Embeddings
* Word2Vec
* Semantic Similarity
* Vector Representations
* Similarity Search
* AI Agent Development

---

# Resume Description

Developed a Word Embedding Similarity Agent using Python and Word2Vec. The system generates vector representations of words, performs semantic similarity analysis, and identifies related words through embedding-based search.

---

# 👨‍💻 Author

## Ajay Sagar

* Python Developer
* AI & Machine Learning Enthusiast
* B.Tech CSE Student

### Connect With Me

🔗 LinkedIn: https://www.linkedin.com/in/engineerajay

🚀 Building AI Projects and Learning New Technologies Every Day.

**Code the Future with Us..!**
