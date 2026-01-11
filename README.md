# 🛡️ Anvetra: Multimodal AI Content Authenticity Detector

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python&style=flat-square)](https://www.python.org/)
[![AI Models](https://img.shields.io/badge/Models-OpenAI%20%7C%20Gemini%20%7C%20CLIP-green?style=flat-square)](https://openai.com/)
[![Deep Learning](https://img.shields.io/badge/Framework-PyTorch%20%2F%20TensorFlow-EE4C2C?logo=pytorch&style=flat-square)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Demo](https://img.shields.io/badge/Demo-Live%20Link-brightgreen)](YOUR_DEMO_LINK_HERE)

> **An advanced AI system designed to restore digital trust by distinguishing between AI-generated synthetic media and authentic human content across text, audio, image, and video.**

---

## 🚀 Project Overview

In an era of hyper-realistic Deepfakes and Generative AI, distinguishing real from fake is critical. **Anvetra** is a comprehensive solution that leverages ensemble learning to detect synthetic manipulation across four distinct modalities.

By integrating state-of-the-art architectures like **Transformers, EfficientNet, and CLIP**, Anvetra provides enterprise-grade verification to combat misinformation and ensure media authenticity.

### 🎯 Key Capabilities

- **📸 Image Forensics:** Detects GAN/Diffusion-generated artifacts using Convolutional Neural Networks (EfficientNet).
- **🎥 Video Deepfake Detection:** Frame-by-frame analysis combined with temporal consistency checks.
- **🎙️ Audio Analysis:** Spectral feature analysis and frequency mapping to identify synthesized voice patterns (utilizing Whisper).
- **📝 Text Verification:** Transformer-based linguistic analysis to differentiate LLM outputs (GPT/Gemini) from human writing.

---

## 🏗️ Technical Architecture

Anvetra utilizes a **Multimodal Ensemble Pipeline** where different models specialize in specific data types, feeding into a final decision layer.

| Modality           | Technologies & Models Used                  | Technique                                                     |
| :----------------- | :------------------------------------------ | :------------------------------------------------------------ |
| **Visual (Image)** | **EfficientNet, CLIP**                      | Artifact detection, pixel-level consistency analysis.         |
| **Visual (Video)** | **CNN + RNN/LSTM**                          | Temporal feature extraction, frame-to-frame coherence.        |
| **Audio**          | **OpenAI Whisper, Librosa**                 | Mel-spectrogram analysis, spectral feature extraction.        |
| **Text**           | **Transformers (BERT/RoBERTa), Gemini API** | Perplexity scoring, burstiness analysis, stylistic forensics. |

---

## 🧠 Methodology

### 1. Data Ingestion & Preprocessing

Raw inputs (files or URLs) are normalized. Audio is converted to spectrograms; video is split into keyframes; text is tokenized.

### 2. Feature Extraction

- **Visual:** High-dimensional feature vectors are extracted to spot "invisible" noise patterns common in AI generation.
- **Audio:** Analysis of breathing patterns and background noise floor (often absent in AI audio).

### 3. Ensemble Classification

The system doesn't rely on a single metric. It aggregates confidence scores from multiple pipelines to output a final **"Authenticity Probability."**

---

## 🛠️ Installation & Usage

### Prerequisites

- Python 3.9+
- FFmpeg (for audio/video processing)
- API Keys (OpenAI/Gemini - optional for specific modules)

### Setup

```bash
# Clone the repository
git clone https://github.com/your-username/Anvetra.git
cd Anvetra

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the Application (Streamlit/Flask)
streamlit run app.py
```

## 📊 Performance & Impact

- **Multimodal Representation:** Successfully integrates disjointed data types into a unified verification framework.
- **High Accuracy:** Demonstrated robust performance against latest generative models (Stable Diffusion, Midjourney, ElevenLabs).
- **Digital Trust:** Designed for researchers, journalists, and enterprises to verify source credibility instantly.

## 🤝 Contributing

Contributions are welcome! Please focus on expanding the dataset support or integrating newer detection algorithms.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewAlgorithm`)
3. Commit your Changes (`git commit -m 'Add CLIP-based detection'`)
4. Push to the Branch (`git push origin feature/NewAlgorithm`)
5. Open a Pull Request

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
