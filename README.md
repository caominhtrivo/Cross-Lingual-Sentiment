# 🇻🇳 Cross-Lingual Sentiment Analyzer (Vietnamese to English)

A machine learning project that demonstrates **cross-lingual sentiment analysis** using a "translate-then-classify" methodology. This system allows you to evaluate the sentiment (**POSITIVE** or **NEGATIVE**) of Vietnamese text even though the core sentiment model is trained only on English.

## 🚀 How It Works

The project operates by chaining two independent Natural Language Processing (NLP) models together into a single pipeline:

1.  **Translation:** An input sentence in **Vietnamese (Vi)** is translated to **English (En)**.
2.  **Classification:** The resulting English text is fed into a fine-tuned English **sentiment analysis** model.
3.  **Result:** The final sentiment label (`POSITIVE` or `NEGATIVE`) is returned to the user.

## 💻 Tech Stack & Models

This project heavily relies on the **Hugging Face Transformers** library for powerful pre-trained models and **Gradio** for rapid deployment of the web interface.

| Component | Model / Technology | Purpose |
| :--- | :--- | :--- |
| **Translation (Vi $\to$ En)** | `Helsinki-NLP/opus-mt-vi-en` | Translates Vietnamese text into English. |
| **Sentiment Analysis** | `distilbert-base-uncased-finetuned-sst-2-english` (default) | Classifies the translated English text as positive or negative. |
| **Interface** | **Gradio** | Creates an interactive, shareable web application from the Python function. |
| **Core Libraries** | `transformers`, `gradio` | Required Python packages. |

## 🛠️ Installation

You can run this notebook directly in **Google Colab** (recommended) or in a local Python environment.

### Prerequisites

You need **Python 3.8+** installed.

### Step 1: Install Dependencies

```bash
pip install transformers torch gradio
