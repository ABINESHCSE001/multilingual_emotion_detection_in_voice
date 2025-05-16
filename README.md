
````markdown
# 🌍 Multilingual Emotion Detection in Voice

This project combines **speech recognition** and **emotion detection** from voice recordings. It supports **multilingual transcription** using OpenAI's Whisper model and analyzes **emotional tone** from vocal features using machine learning.

## 🧠 Key Features

- 🎤 Convert MP4 audio to WAV format
- 🌐 Transcribe speech using OpenAI Whisper (supports multiple languages)
- 😃 Detect emotions (happy, sad, angry, neutral) from speech using MFCC and pitch features
- 🔎 Extract MFCC and pitch features with `librosa`
- 🤖 Classify emotions with a Support Vector Machine (SVM)

## 📦 Dependencies

Install the following Python packages:

```bash
pip install openai-whisper librosa scikit-learn moviepy
````

On Ubuntu systems, you may also need:

```bash
sudo apt-get install ffmpeg
```

## 📁 File Structure

* `multilingual_emotion_detection_in_voice.ipynb` – Main notebook with code to transcribe and classify emotions from voice input.

## 🔧 How It Works

1. **Convert** MP4 to WAV using `moviepy`.
2. **Transcribe** voice using Whisper (`base` model).
3. **Extract features** from WAV file using MFCCs and pitch.
4. **Train SVM** on simulated emotion-labeled data.
5. **Classify** the emotion from the speech input.
6. **Output** the detected emotion, transcription, and language.

## ▶️ Usage

Edit the last line in the notebook to point to your MP4 audio file:

```python
audio_path = "/content/your_audio_file.mp4"
emotion_aware_speech_recognition(audio_path)
```

## 📌 Notes

* This example uses synthetic training data for emotion classification. For real-world accuracy, train the classifier with labeled audio-emotion datasets like RAVDESS, CREMA-D, etc.
* Make sure Whisper supports the language spoken in your audio file.


```
