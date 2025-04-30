# 🗣️ Kinyarwanda Voice Q&A Bot

This is a Python-based voice assistant that listens to spoken Kinyarwanda, transcribes the audio using [Whisper](https://huggingface.co/mbazaNLP/Whisper-Small-Kinyarwanda), and speaks back using a Text-to-Speech (TTS) model ([facebook/mms-tts-kin](https://huggingface.co/facebook/mms-tts-kin)). It supports simple predefined questions and gives corresponding audio responses in Kinyarwanda.

## 📌 Features

- 🎧 **Speech Recognition in Kinyarwanda** using Whisper.
- 🗨️ **Text Matching** to predefined question-answer pairs.
- 🔊 **Text-to-Speech in Kinyarwanda** using Meta’s multilingual TTS model.
- 💾 Automatic saving and playback of response audio files.
- 🖥️ Simple and offline-ready Python script.

## 🛠️ Setup Instructions

### 1. Clone the Repository

git clone https://github.com/yourusername/kinyarwanda-voice-bot.git
cd kinyarwanda-voice-bot

### 2. Install Dependencies

Make sure you have Python 3.8+ installed. Then run:

pip install -r requirements.txt

The key libraries used:
- `transformers`
- `torchaudio`
- `soundfile`
- `dotenv`
- `huggingface_hub`

### 3. Add Your Hugging Face Token

## 📁 Folder Structure


.
├── audio/             # Input folder for your .wav files
├── outputs/           # Output folder for generated answer audios
├── main.py            # Main script
├── .env               # Contains Hugging Face token
├── requirements.txt   # Python dependencies
└── README.md          # You are here!


---

## 🎙️ How It Works

1. You place your `.wav` voice recordings in the `audio/` folder.
2. The script uses Whisper to **transcribe the audio** in Kinyarwanda.
3. It compares the transcribed text to predefined questions (like “amakuru”, “witwa nde”, etc.).
4. If a match is found, it **generates a spoken answer** using the VITS TTS model.
5. The response is saved as a `.wav` file and **automatically played** (Windows only).

---

## 🧠 Sample QA Pairs

| Question Contains         | Response                              |
|---------------------------|----------------------------------------|
| "amakuru"                 | Ni meza, urakoze!                      |
| "witwa nde"               | Nitwa Uwase                            |
| "ubuzima bumeze gute"     | Bumeze neza!                           |
| "ikinyarwanda ni iki"     | Ni ururimi kavukire ruvugwa n’Abanyarwanda. |
| "amakuru yawe"            | Ni meza, ndashima Imana!              |

## ✅ To Do / Improvements

- [ ] Add dynamic learning or fine-tuning for new questions.
- [ ] Add support for microphone input (real-time).
- [ ] Improve matching logic using semantic similarity (e.g., with sentence transformers).
- [ ] Cross-platform audio playback.

## 🔐 License

This project is under the MIT License.

---

## 👩🏾‍💻 Author

**Vanessa Seminega**  
