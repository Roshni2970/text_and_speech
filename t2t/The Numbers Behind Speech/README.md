# The Numbers Behind Speech
> An audio analytics and speech transcription pipeline that measures acoustic duration, word counts, character density, and speaking pace (WPM).

---

## 📌 Overview

**The Numbers Behind Speech** is an interactive speech analysis tool designed to quantify spoken audio streams. Beyond simple speech-to-text conversion, this notebook extracts acoustic and textual metrics—such as total duration (seconds), total word count, character count, and speaking velocity in **Words Per Minute (WPM)**.

This project bridges digital audio signal processing with Natural Language Processing (NLP), making it ideal for evaluating public speaking pace, podcast transcriptions, customer call metrics, and educational speech analysis.

---

## 🎯 Aim & Objectives

- **Primary Goal:** Convert spoken audio into text while simultaneously measuring quantitative speech dynamics and cadence metrics.
- **Learning Objectives:**
  - Understand speech-to-text conversion pipelines using Python ASR libraries.
  - Measure audio duration and calculate temporal statistics like speaking rate (WPM).
  - Practice structured text tokenization and character-level statistical reporting.

---

## 📊 Calculated Speech Metrics

The application captures audio inputs and computes the following metrics upon transcription:

1. **Audio Duration ($T$):** Total elapsed recording length measured in seconds.
2. **Total Word Count ($W$):** Total number of spoken tokens extracted from the transcript.
3. **Total Character Count ($C$):** Total characters excluding whitespace.
4. **Speaking Rate / Pace ($\text{WPM}$):**
   $$\text{WPM} = \left( \frac{W}{T} \right) \times 60$$

| Speaking Pace (WPM) | Classification | Typical Context |
| :--- | :--- | :--- |
| **$< 110$ WPM** | Slow / Deliberate | Formal lectures, audiobooks, deliberate instruction |
| **$110 – 160$ WPM** | Conversational (Ideal) | Presentations, podcasts, casual conversation |
| **$> 160$ WPM** | Fast / Rapid | Fast-paced news broadcasts, auctioneering, excited speech |

---

## ✨ Key Features

- **Automated Transcription:** Uses `SpeechRecognition` to convert live voice recordings or `.wav` files into clean text.
- **Real-Time Pace Analysis:** Computes instantaneous WPM to gauge speaking rate and clarity.
- **Structural Text Breakdown:** Displays character density, average word length, and token counts.
- **Interactive Notebook Workflow:** Simply speak into your system microphone or load sample audio files to generate instant statistical reports.

---

## 🛠️ Tech Stack & Dependencies

| Layer | Technology |
| :--- | :--- |
| **Programming Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook / Google Colab / VS Code |
| **Speech Processing** | `SpeechRecognition` |
| **Audio Processing & I/O** | `wave`, `contextlib`, `PyAudio` |
| **Standard Libraries** | `time`, `re`, `string` |

---

## 📁 Project Structure

```text
.
├── The_Numbers_Behind_Speech.ipynb   # Main interactive notebook with metrics engine
├── sample_audio/                     # Sample audio files (.wav) for offline testing
├── README.md                         # Comprehensive project documentation
└── requirements.txt                  # Dependency list
