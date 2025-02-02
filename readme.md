# TOPSIS Method for Selecting the Best Pretrained Model

## Overview

This project implements the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method to evaluate and rank pretrained models based on various performance metrics. The models evaluated include **GPT-3**, **BERT-GPT**, **T5**, and **GPT-Neo**. The criteria used for evaluation are **Perplexity**, **BLEU**, **ROUGE**, and **Training Time**.

## 1. Models and Evaluation Criteria

The following pretrained models are evaluated:

- **GPT-3**
- **BERT-GPT**
- **T5**
- **GPT-Neo**

The criteria for evaluation include:

- **Perplexity** (Lower is better)
- **BLEU Score** (Higher is better)
- **ROUGE Score** (Higher is better)
- **Training Time (hours)** (Lower is better)

### Decision Matrix

| Model    | Perplexity | BLEU | ROUGE | Training Time (hrs) |
| -------- | ---------- | ---- | ----- | ------------------- |
| GPT-3    | 12.5       | 40.2 | 45.8  | 10                  |
| BERT-GPT | 14.2       | 38.7 | 43.2  | 8                   |
| T5       | 11.8       | 42.3 | 47.1  | 12                  |
| GPT-Neo  | 13.1       | 39.5 | 44.7  | 9                   |

## 2. Implementation Steps

The **TOPSIS method** is applied using the following steps:

1. **Normalization** of the decision matrix.
2. **Weighted normalization** of the decision matrix.
3. **Calculation of ideal best and worst solutions**.
4. **Distance computation** from the ideal solutions.
5. **Calculation of TOPSIS scores** for each model.
6. **Ranking of models** based on the scores.

## 3. Code Execution

The implementation is provided in the Python script `notebook.ipynb`.

## 4. Results

### Final Rankings:

| Model    | Perplexity | BLEU | ROUGE | Training Time | TOPSIS Score |
| -------- | ---------- | ---- | ----- | ------------- | ------------ |
| T5       | 11.8       | 42.3 | 47.1  | 12            | 0.622977     |
| GPT-3    | 12.5       | 40.2 | 45.8  | 10            | 0.607802     |
| GPT-Neo  | 13.1       | 39.5 | 44.7  | 9             | 0.500639     |
| BERT-GPT | 14.2       | 38.7 | 43.2  | 8             | 0.377023     |

## 5. Usage

1. Clone this repository.
2. Run `notebook.ipynb` in Jupyter Notebook.
3. Modify the dataset to evaluate different models.

## 6. Conclusion

Using the **TOPSIS method**, we effectively ranked pretrained models for text generation based on multiple criteria, providing a systematic approach for model selection.
