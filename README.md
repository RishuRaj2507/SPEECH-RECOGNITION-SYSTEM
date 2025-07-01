# SPEECH-RECOGNITION-SYSTEM

*Company* - *CODTECH IT SOLUTIONS*

*NAME* - *RISHU RAJ*

*INTERN ID* - *CT04DF2641*

*DOMAIN* - *ARTIFICIAL INTELLIGENCE*

*DURATION* - *4 WEEKS*

*MENTOR* - *NEELA SANTHOSH KUMAR*

---

## 🎙️ Real-Time Speech-to-Text using Python and Google Speech Recognition API

This project is a simple yet powerful Python script that converts spoken words into text using the microphone and Google's Speech Recognition API. Built with the `speech_recognition` library, it allows users to interact with their computer using natural voice input, opening the door to hands-free control, voice-activated systems, and accessibility features.

---

### 🧠 What This Project Does

The script listens to your voice through your system’s microphone, processes the input audio, and converts it into written text using Google’s free Web Speech API. It automatically adjusts for ambient noise to improve accuracy and provides basic error handling for common issues like unrecognized speech or network problems.

---

### 📌 Features

* 🎧 **Microphone Input**: Uses the default microphone to capture real-time voice.
* 🌍 **Google Web Speech API**: Performs speech-to-text conversion in the cloud.
* 🔈 **Ambient Noise Adjustment**: Automatically adjusts sensitivity based on background noise.
* ⚠️ **Exception Handling**: Handles common errors like unclear audio and API connection failures.
* 🧪 **Beginner-Friendly**: Clean, minimal code ideal for learning and experimentation.

---

### 🛠️ How It Works

1. **Initialize Recognizer**: The `Recognizer()` object from `speech_recognition` is used to manage audio input and recognition tasks.
2. **Capture Audio**: The system microphone is accessed as the audio source, and the script listens for spoken input.
3. **Noise Calibration**: The script calibrates itself to ignore ambient background noise using a one-second sample.
4. **Speech Recognition**: The captured audio is sent to Google’s Web Speech API, which returns the recognized text.
5. **Output**: The recognized speech is printed to the terminal. If the input is unclear or there's a network error, appropriate messages are shown.

---

### 💻 Code Snapshot

```python
import speech_recognition as sr

recognizer = sr.Recognizer()

with sr.Microphone() as source:
    print("Adjusting for ambient noise...")
    recognizer.adjust_for_ambient_noise(source, duration=1)
    print("Listening...")
    audio = recognizer.listen(source)

    try:
        print("Recognizing...")
        text = recognizer.recognize_google(audio)
        print("You said:", text)
    except sr.UnknownValueError:
        print("Could not understand the audio.")
    except sr.RequestError:
        print("Could not request results; check your internet connection.")
```

---

### 📦 Requirements

* Python 3.6+
* `speech_recognition` library
  Install with:

  ```
  pip install SpeechRecognition
  ```
* (Optional) `pyaudio` for microphone input:

  ```
  pip install pyaudio
  ```

  > Note: On some systems, installing PyAudio may require system-specific packages or precompiled binaries.

---

### 🚀 Use Cases

* Voice-controlled applications
* Assistive technology for accessibility
* Speech logging or transcription tools
* Natural language-based interfaces
* Educational demos of AI and speech processing

---

### 🧩 Future Improvements

* Add support for continuous listening or activation via a trigger word
* Save transcribed text to a file or database
* Add GUI for ease of use
* Integrate offline recognition using CMU Sphinx

---

### 🤝 Contributing

Feel free to fork this repository, suggest improvements, or submit pull requests. This is a great starting point for learning about real-time voice interaction in Python.

---

### Output

<img width="961" alt="Image" src="https://github.com/user-attachments/assets/6ea4d058-ceef-4ac1-8e0c-160d4712f6ef" />

