# what language is this
> A lightweight multilingual classification tool that identifies English, Tamil, and Hindi text using Unicode script range matching and character-pattern heuristics.

---

## 📌 Overview

**what language is this** is an accessible Natural Language Processing (NLP) tool designed to detect the script and language of raw text inputs. By examining Unicode character ranges and script-specific letter patterns, this notebook instantly classifies sample text into **English**, **Tamil**, or **Hindi** without needing large machine learning models or internet connectivity.

This project serves as a foundational implementation of multilingual text detection, script recognition, and Unicode analysis in Python.

---

## 🎯 Aim & Objectives

- **Primary Goal:** Identify whether a given input string is written in English, Tamil, or Hindi using rule-based character pattern analysis.
- **Learning Objectives:**
  - Understand Unicode character encoding blocks (Basic Latin, Tamil, Devanagari).
  - Practice string parsing, character frequency counting, and script mapping algorithms in Python.
  - Build deterministic classification logic for multi-script text verification.

---

## 🔤 Script Identification & Unicode Range Mapping

The language detection engine evaluates input characters against standardized **Unicode Standard Blocks**:

| Language | Target Script | Unicode Block Range (Hex) | Example Characters |
| :--- | :--- | :--- | :--- |
| **English** | Basic Latin | `U+0041` – `U+007A` | `A-Z`, `a-z` |
| **Tamil** | Tamil | `U+0B80` – `U+0BFF` | `அ`, `ஆ`, `க`, `ந` |
| **Hindi** | Devanagari | `U+0900` – `U+097F` | `अ`, `आ`, `क`, `न` |

### Classification Rule
$$\text{Language} = \arg\max_{L \in \{\text{English, Tamil, Hindi}\}} \left( \text{Count of Characters in } \text{Block}_L \right)$$

---

## ✨ Key Features

- **Multi-Script Support:** Seamlessly detects and distinguishes between Latin (English), Tamil, and Devanagari (Hindi) scripts.
- **Zero External Dependencies:** Runs natively using standard Python libraries without requiring internet APIs or external NLP models.
- **Interactive Input Processing:** Accept and evaluate custom phrases, sentences, or paragraphs in real time.
- **Detailed Script Breakdown:** Displays character distribution statistics and percentage confidence per detected script.

---

## 🛠️ Tech Stack & Dependencies

| Layer | Technology |
| :--- | :--- |
| **Programming Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook / JupyterLab / Google Colab |
| **Libraries Used** | Standard Python Libraries (`unicodedata`, `re`, `collections`) |
| **Optional Libraries** | `matplotlib` (for visual script distribution charts) |

---

## 📁 Project Structure

```text
.
├── what_language_is_this.ipynb   # Main interactive notebook with language detection logic
├── sample_texts.txt              # Sample multilingual test passages (English, Tamil, Hindi)
├── README.md                     # Comprehensive project documentation
└── requirements.txt              # Optional project dependencies
