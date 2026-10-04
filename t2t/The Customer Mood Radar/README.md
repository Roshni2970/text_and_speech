# The Customer Mood Radar
> An NLP-driven text sentiment analysis engine designed to gauge customer feedback, reviews, and sentiment polarities in real time.

---

## 📌 Overview

**The Customer Mood Radar** is an accessible Python tool built to process customer statements, reviews, and feedback. By scoring and classifying input text into positive, negative, or neutral sentiment tiers, this notebook offers a practical implementation of rule-based natural language processing (NLP) for market research, customer service monitoring, and user feedback analysis.

---

## 🎯 Aim & Objectives

- **Primary Goal:** Parse raw user-submitted text and determine the underlying sentiment polarity using a transparent scoring methodology.
- **Learning Objectives:**
  - Learn fundamental text tokenization, normalization, and stop-word filtering.
  - Implement lexicon-based and rule-based sentiment scoring algorithms.
  - Interpret and visualize text analytics outputs within an interactive notebook framework.

---

## 🔬 Sentiment Scoring Mechanism

The application tokenizes input text, cleans noise, and evaluates individual terms against predefined sentiment lexicons:

1. **Text Preprocessing:** Converts text to lowercase, removes special characters, and splits text into individual word tokens.
2. **Lexicon Matching:** Cross-references tokens against positive ($L_+$) and negative ($L_-$) word lexicons.
3. **Polarity Calculation:**
   $$\text{Sentiment Score} = \sum (\text{Positive Words}) - \sum (\text{Negative Words})$$

| Final Score | Classification | Example Customer Output |
| :--- | :--- | :--- |
| **Score $> 0$** | **POSITIVE 😊** | *"The customer support team was incredibly helpful and quick!"* |
| **Score $= 0$** | **NEUTRAL 😐** | *"The package arrived on Tuesday at 3 PM as scheduled."* |
| **Score $< 0$** | **NEGATIVE 🙁** | *"The product quality was disappointing and delivery was delayed."* |

---

## ✨ Key Features

- **Instant Sentiment Classification:** Categorizes customer inputs as Positive, Negative, or Neutral.
- **Lexicon-Based Scoring:** Offers transparent, verifiable word-level scoring without black-box abstractions.
- **Interactive Input Interface:** Test custom customer reviews, feedback forms, or survey responses in real time.
- **Zero Heavy Dependencies:** Built cleanly on Python's native ecosystem for maximum compatibility and performance.

---

## 🛠️ Tech Stack & Dependencies

| Layer | Technology |
| :--- | :--- |
| **Programming Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook / JupyterLab / Google Colab |
| **Libraries Used** | Standard Python Libraries (`re`, `collections`, `string`) |
| **Optional Enhancements** | `TextBlob`, `NLTK`, `matplotlib` (for visual polarity distribution) |

---

## 📁 Project Structure

```text
.
├── The_Customer_Mood_Radar.ipynb   # Interactive notebook containing sentiment analysis logic
├── sample_reviews.txt              # Sample customer feedback dataset for batch testing
├── README.md                       # Comprehensive project documentation
└── requirements.txt                # Optional dependency specifications
