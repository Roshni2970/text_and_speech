# Making Sense of Commands
> A voice-driven control pipeline that transcribes spoken audio and routes recognized commands to automated system actions.

---

## 📌 Overview

**Making Sense of Commands** is a lightweight voice recognition and command parsing tool implemented in Python. It bridges live audio recording with rule-based system execution by capturing vocal inputs, converting them to text via Automated Speech Recognition (ASR), and mapping key command keywords to specific functions (e.g., `START`, `STOP`, `PAUSE`, `EXIT`).

This project serves as a foundational step toward building offline voice assistants, hands-free IoT interfaces, and voice-controlled accessibility tools.

---

## 🎯 Aim & Objectives

- **Primary Goal:** Detect, parse, and execute predefined spoken commands from live microphone input or pre-recorded audio.
- **Learning Objectives:**
  - Understand real-time audio sampling and speech recognition APIs.
  - Implement intent parsing and string normalization algorithms.
  - Handle audio exception states (e.g., background noise, unknown commands, network timeouts).

---

## 🗣️ Supported Commands & Action Map

The speech analyzer normalizes transcription strings (lowercasing, punctuation removal) and maps spoken triggers to predefined system routines:

| Spoken Command | Trigger Terms | Executed Action |
| :--- | :--- | :--- |
| **Greeting** | `"hello"`, `"hi"`, `"hey"` | Initializes session & returns welcome feedback |
| **Start** | `"start"`, `"begin"`, `"run"` | Triggers process execution / starts audio stream |
| **Pause** | `"pause"`, `"wait"`, `"hold"` | Temporarily suspends active process |
| **Stop** | `"stop"`, `"halt"`, `"cancel"` | Terminates current task execution |
| **Exit** | `"exit"`, `"quit"`, `"bye"` | Safely closes the application/session |

---

## ✨ Key Features

- **Real-Time Voice Recognition:** Captures live audio streams directly via system microphone.
- **Command Intent Parser:** Matches spoken phrases against structured command rules using fuzzy and exact string matching.
- **Ambient Noise Adjustment:** Calibrates microphone sensitivity against background noise prior to audio capture.
- **Interactive Feedback Loop:** Provides immediate visual logging and console feedback upon command detection.
- **Lightweight Architecture:** Runs seamlessly inside Jupyter environments without requiring heavy GPU frameworks.

---

## 🛠️ Tech Stack & Dependencies

| Layer | Technology |
| :--- | :--- |
| **Programming Language** | Python 3.8+ |
| **Environment** | Jupyter Notebook / Google Colab / VS Code |
| **Speech Processing** | `SpeechRecognition` |
| **Audio I/O** | `PyAudio` |
| **System Libraries** | `os`, `sys`, `time` |

---

## 📁 Project Structure

```text
.
├── Making_Sense_of_Commands.ipynb   # Main interactive notebook with recognition pipeline
├── sample_audio/                   # Pre-recorded command test files (.wav)
├── README.md                       # Project documentation
└── requirements.txt                # Project dependency list
