# Audio-Based-Emotion-Recognition-System


## Overview
This project focuses on speech emotion recognition using Long Short-Term Memory (LSTM) networks. The model is designed to classify emotions such as happiness, sadness, anger, and surprise from speech signals. Various datasets and preprocessing techniques are used to enhance accuracy.

## Datasets Used
### 1. **Popular Speech Emotion Datasets**
- **RAVDESS:** Contains labeled speech and song audio with emotion categories such as neutral, calm, happy, sad, angry, fearful, disgust, and surprised.
- **CREMA-D:** Uses emotion labels like sadness (SAD), anger (ANG), disgust (DIS), fear (FEA), happiness (HAP), and neutral (NEU).
- **TESS:** Similar to CREMA-D, with emotion labels directly included in filenames.
- **SAVEE:** Uses prefix letters in filenames to indicate emotions (e.g., 'a' for anger, 'f' for fear, 'h' for happiness, etc.).

## Speech Processing Techniques
### 1. **Waveforms and STFT**
- Speech signals are continuous waveforms that need to be analyzed in segments.
- The **Short-Time Fourier Transform (STFT)** helps extract frequency-based features for speech analysis.

### 2. **Quantization & Sample Rate**
- **Quantization** converts analog speech signals into digital form, similar to how videos are captured frame by frame.
- **Sample Rate** determines how many samples per second are taken:
  - **44.1 kHz:** Standard for music and CDs.
  - **48 kHz:** Commonly used in movies due to a wider dynamic range.

### 3. **Amplitude Envelope & Sample Duration**
- **Amplitude Envelope:** Tracks variations in signal intensity over time, crucial for speech analysis.
- **Sample Duration:** Defines the time window for analyzing audio data.

## Data Augmentation Techniques
To improve model performance, two common augmentation techniques are applied:
1. **Noise Injection:** Adds background noise to make the model robust to real-world conditions.
2. **Time Stretching:** Alters audio speed without changing pitch, allowing the model to adapt to variations in speech pace.

## Array and Dimensional Expansion in Speech Recognition
- Speech signals are stored as numerical arrays after digital conversion.
- Expanding dimensions helps increase the feature space, improving recognition accuracy.
- Methods like **spectrograms** and **context stacking** provide richer representations of speech patterns.

## Model: LSTM for Speech Recognition
- **Why LSTM?**
  - Captures long-range dependencies in sequential speech data.
  - Handles variable-length inputs efficiently.
  - Recognizes temporal patterns in speech, improving accuracy.

## Conclusion
By leveraging LSTM networks, proper data augmentation, and preprocessing techniques, this project aims to build a robust speech recognition model capable of identifying emotions in real-world speech recordings.
