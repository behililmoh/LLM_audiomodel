# 🎙️ M4A Audio Transcription to Text with Python

This project uses several Python libraries to transcribe an M4A audio file into text.

## 🛠️ Main Steps

### 1. Installing Dependencies
The code installs the required libraries (`pydub`, `transformers`, `torchaudio`) using pip.

### 2. Converting M4A to WAV
It uses `pydub` to read an M4A file (`Enregistrement4.m4a`) and convert it to WAV format (`converted.wav`), which is more compatible with most audio processing models.

### 3. Loading and Resampling
The WAV file is loaded using `torchaudio`. It is resampled to 16,000 Hz, the sampling rate expected by the transcription model.

### 4. Transcription with Wav2Vec2.0
Using Hugging Face’s `transformers` library:
- Loads the pre-trained model `facebook/wav2vec2-base-960h`
- Preprocesses the audio data
- Passes it through the model to get predictions
- Decodes the predicted tokens into readable text

### 5. Displaying the Transcription
The transcribed text is printed to the console.

## 🚀 Uploading to GitHub

To add this project to your Git repository:
1. Create a file named `transcription.py` and paste the code into it.
2. Add a `requirements.txt` file with the following content:
