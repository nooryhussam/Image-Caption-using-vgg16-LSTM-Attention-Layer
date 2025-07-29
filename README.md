# 🖼️ Image Captioning using VGG16 + LSTM + Attention Layer

This project implements an **image captioning model** that generates human-like descriptions for images using deep learning. It follows the **"Show, Attend and Tell"** architecture, combining a pre-trained **VGG16** model for feature extraction, a custom **LSTM decoder**, and a **Bahdanau Attention mechanism** to focus on relevant parts of the image during caption generation.

## 📌 Features

- Extracts image features using **VGG16** (pre-trained on ImageNet)
- Uses an **LSTM** decoder to generate captions word-by-word
- Incorporates **Bahdanau attention** to improve caption accuracy and interpretability
- Trained and tested on the **Flickr8k dataset**
- Achieves strong BLEU scores and produces visually interpretable attention heatmaps

## 🧠 Architecture Overview

1. **Encoder (CNN)**:  
   - VGG16 (excluding top layer)
   - Outputs a fixed-length feature vector

2. **Decoder (RNN)**:  
   - Embedding layer → LSTM → Attention → Dense layer
   - Predicts the next word in the caption sequence

3. **Attention Mechanism**:  
   - Focuses on relevant image regions at each decoding step

## 🗂️ Dataset

- **Flickr8k Dataset**  
  - 8,000 images with five captions each  
  - Download from: [Flickr8k Dataset](https://forms.illinois.edu/sec/1713398)

## 🛠️ Requirements

- Python 3.7+
- TensorFlow / Keras
- NumPy
- OpenCV
- tqdm
- PIL
- NLTK
