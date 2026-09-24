# TF-IDF Text Representation

## Overview

This project explores **TF-IDF (Term Frequency–Inverse Document Frequency)**, a fundamental text representation technique used in Natural Language Processing (NLP).

TF-IDF converts text into numerical features by assigning importance to words based on how frequently they appear in a document and how rare they are across the complete collection of documents.

---

## Objective

The main objectives of this project are to:

* Understand the concept of TF-IDF.
* Learn how text can be converted into numerical features.
* Understand **Term Frequency (TF)**.
* Understand **Inverse Document Frequency (IDF)**.
* Understand how TF and IDF are combined.
* Learn why TF-IDF is useful for NLP and machine learning tasks.

---

## What is TF-IDF?

**TF-IDF** is a statistical technique that measures how important a word is to a particular document within a collection of documents.

The basic idea is:

```text
A word is important when:
- It appears frequently in a particular document.
- It does not appear frequently across all documents.
```

Common words appearing in many documents receive lower importance, while words that are more specific to particular documents receive higher importance.

---

## TF-IDF Components

### 1. Term Frequency (TF)

Term Frequency measures how often a word appears in a document.

A simple representation is:

```text
TF = Number of times a term appears in a document
     -----------------------------------------------
              Total number of terms
```

A higher TF means the word occurs more frequently within that document.

---

### 2. Inverse Document Frequency (IDF)

IDF measures how rare or unique a word is across a collection of documents.

A commonly used form is:

```text
IDF = log(Total number of documents / Number of documents containing the term)
```

Words appearing in many documents receive a lower IDF value.

Words appearing in fewer documents receive a higher IDF value.

---

### 3. TF-IDF Score

TF and IDF are combined to calculate the importance of a term:

```text
TF-IDF = TF × IDF
```

Therefore, a word receives a high TF-IDF score when it is frequent in a particular document but relatively uncommon across the document collection.

---

## General Workflow

```text
Raw Text
   ↓
Text Preprocessing
   ↓
Tokenization
   ↓
Calculate Term Frequency
   ↓
Calculate Inverse Document Frequency
   ↓
TF-IDF Calculation
   ↓
Numerical Feature Matrix
   ↓
Machine Learning / NLP Task
```

---

## TF-IDF vs Bag of Words

TF-IDF is closely related to the **Bag of Words (BoW)** approach, but the two assign importance to words differently.

| Feature           | Bag of Words              | TF-IDF                         |
| ----------------- | ------------------------- | ------------------------------ |
| Representation    | Word counts               | Weighted word scores           |
| Word importance   | Based mainly on frequency | Based on frequency and rarity  |
| Common words      | Can receive high counts   | Usually receive lower weight   |
| Context/semantics | Not captured              | Not captured                   |
| Complexity        | Simple                    | Slightly more complex          |
| Common use        | Basic text features       | More informative text features |

---

## Advantages

* Simple and widely used text representation technique.
* Converts text into numerical features.
* Reduces the importance of very common words.
* Highlights words that are more specific to individual documents.
* Works well with many traditional machine learning algorithms.
* Useful as a strong baseline for text-based classification tasks.

---

## Limitations

* Does not understand the meaning of words.
* Does not capture semantic relationships.
* Does not consider word order.
* Produces sparse feature matrices for large vocabularies.
* Vocabulary size can become very large.
* Similar words are treated as separate features.

For example, words such as:

```text
car
cars
automobile
```

are not automatically recognized as semantically related.

---

## Applications

TF-IDF can be used in various NLP applications, including:

* Text classification
* Document classification
* Search engines
* Information retrieval
* Keyword extraction
* Text similarity
* Spam detection
* Sentiment analysis
* Document ranking

---

## Key Learnings

Through this project, the following concepts are explored:

* Understanding TF-IDF text representation.
* Understanding Term Frequency.
* Understanding Inverse Document Frequency.
* Combining TF and IDF to calculate word importance.
* Converting text into numerical feature vectors.
* Understanding the difference between BoW and TF-IDF.
* Recognizing the limitations of traditional text representations.

---

## Technologies

* **Python**
* **Natural Language Processing (NLP)**
* **TF-IDF**

---

## Future Improvements

Possible extensions to this project include:

* Applying TF-IDF to a larger real-world dataset.
* Using TF-IDF features for text classification.
* Comparing TF-IDF with Bag of Words.
* Experimenting with different preprocessing techniques.
* Comparing TF-IDF with word embeddings such as Word2Vec and GloVe.
* Exploring modern contextual representations using Transformer models.

---

## Conclusion

TF-IDF is an important traditional NLP technique for converting text into numerical representations while assigning greater importance to words that are more distinctive to individual documents.

Although TF-IDF does not understand semantics or word order, it remains a useful and interpretable technique for traditional machine learning-based NLP applications and provides an important foundation for understanding more advanced text representation methods.
