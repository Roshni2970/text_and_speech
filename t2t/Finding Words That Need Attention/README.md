# Finding Words That Need Attention

> Real-time speech-to-text transcription and key-phrase monitoring powered by Python.

---

## 📌 Overview

**Finding Words That Need Attention** is a practical speech analysis application designed to monitor spoken input for target words. By bridging microphone capture with automated speech recognition (ASR) engines, this project instantly flags essential words or triggers alerts based on custom interest lists.

---

## 🛠️ Tech Stack & Dependencies

| Category | Technology |
|---|---|
| **Language** | Python 3.x |
| **Runtime** | Jupyter Notebook / Google Colab |
| **Libraries** | `SpeechRecognition`, `pyaudio` |

---

## ✨ Core Features

- **Audio Acquisition:** Captures audio directly through your system's microphone.
- **Automated Transcription:** Processes raw audio signals into readable text strings.
- **Target Phrase Matching:** Checks transcribed output against specified watch-words.
- **Modular Pipeline:** Easily swap speech recognition backends or update keyword targets.

---

## 📁 Project Structure

```text
├── Finding_Words_That_Need_Attention.ipynb   # Main interactive notebook
├── README.md                                  # Project documentation
└── requirements.txt                           # Dependency specifications
