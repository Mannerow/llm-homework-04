# llm-homework-04

## 📄 Overview

This Jupyter notebook evaluates the responses of a language model against a set of generated questions using cosine similarity and ROUGE scores. The analysis starts by loading a subset of data from a GitHub-hosted CSV file and employs various Python libraries such as `Pandas`, `NumPy`, `Sentence Transformers`, and `Rouge` to process and analyze the data effectively.

## 🚀 Installation

To set up the project, follow these steps:

```bash
pip install pipenv
pipenv install
```

Then, select the pipenv environment in the Jupyter kernel.

## 🛠 How It Works

### Ground Truth Dataset Usage:

The dataset includes several fields like 'answer_llm' and 'answer_orig' among others. 'answer_llm' contains the responses provided by the language model, while 'answer_orig' includes the original answers from the ground truth dataset used to generate the questions. This pairing is crucial as it serves as the basis for evaluating the language model’s performance, ensuring that the model's responses can be directly compared to a known correct answer.

### Evaluation Metrics:

The notebook utilizes the `multi-qa-mpnet-base-dot-v1` model from `Sentence Transformers` to transform these text responses into embeddings, allowing for the calculation of cosine similarities to quantitatively assess how closely the language model's responses match the original answers. Additionally, the `ROUGE` metric provides a qualitative evaluation by comparing the overlap of n-grams, word sequences, and word pairs between the model's responses and the original answers. Results from these evaluations are aggregated and analyzed to compute average F-scores across various metrics, highlighting the model's consistency and accuracy across the dataset.