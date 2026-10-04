# Making Health Advice Clear
| Evaluating and simplifying complex health and medical literature using quantitative NLP metrics in Python.

---

## 📌 Overview

Medical jargon and complex health instructions often make medical advice difficult for patients to understand. **Making Health Advice Clear** is a Natural Language Processing (NLP) tool designed to evaluate the reading grade level and accessibility of medical text.

By analyzing key linguistic features—such as total sentence length, word count, and syllable density—this notebook computes standardized readability scores (such as the **Flesch Reading Ease** and **Flesch-Kincaid Grade Level**). This enables medical communicators, students, and healthcare developers to assess whether health advice is written at a clear, patient-friendly reading level.

---

## 🎯 Aim & Objectives

- **Primary Goal:** Quantify the readability of complex health and medical text using automated linguistic formulas in Python.
- **Learning Objectives:** 
  - Understand textual metrics, tokenization, and syllable estimation algorithms.
  - Apply standard readability formulas (Flesch Reading Ease, Flesch-Kincaid Grade Level).
  - Practice text preprocessing techniques without relying exclusively on heavy third-party models.

---

## 🔬 Readability Metrics & Formulas

The analyzer processes input passages through three core counts:
$$\text{Total Sentences } (S), \quad \text{Total Words } (W), \quad \text{Total Syllables } (Y)$$

### 1. Flesch Reading Ease Score
Measures overall readability on a scale of **0 to 100** (higher score = easier to read).

$$\text{Score} = 206.835 - 1.015 \left( \frac{W}{S} \right) - 84.6 \left( \frac{Y}{W} \right)$$

| Score Range | Difficulty Level | Target Audience |
| :--- | :--- | :--- |
| **90.0 – 100.0** | Very Easy | 5th grade level (Ideal for patient care guides) |
| **60.0 – 70.0** | Plain English | 8th – 9th grade level |
| **0.0 – 30.0** | Very Confusing | University graduates / Specialized medical journals |

### 2. Flesch-Kincaid Grade Level
Translates the readability score directly into a **U.S. education grade level**.

$$\text{Grade} = 0.39 \left( \frac{W}{S} \right) + 11.8 \left( \frac{Y}{W} \right) - 15.59$$

---

## ✨ Key Features

- **Multi-Metric Text Analysis:** Calculates sentence count, word count, syllable distribution, and target readability scores.
- **Medical Text Evaluation:** Tailored for checking patient information leaflets, prescription instructions, and health blogs.
- **Interactive Notebook Controls:** Allows users to paste raw paragraphs or health passages for immediate analysis.
- **Syllable Counting Engine:** Implements lightweight heuristic rules (vowel group detection, silent 'e' handling) for accurate counting.
- **Interpretation Engine:** Automatically maps numeric outputs to qualitative reading tiers (e.g., *Easy*, *Moderate*, *Difficult*).

---

## 🛠️ Tech Stack & Dependencies

| Layer | Technology |
| :--- | :--- |
| **Programming Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook / JupyterLab / Google Colab |
| **Libraries Used** | `re` (Regular Expressions), `math`, standard string manipulation tools |
| **Optional Libraries** | `textstat` (for metric cross-validation), `matplotlib` (for visual statistics) |

---

## 📁 Project Structure

```text
.
├── Making_Health_Advice_Clear.ipynb   # Main Jupyter notebook containing logic & analysis
├── sample_health_texts.txt            # Sample patient guides vs. medical research papers
├── README.md                          # Comprehensive project documentation
└── requirements.txt                   # Optional dependencies list
