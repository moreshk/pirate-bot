# pirate-bot
Voice to Voice chatbot using Whisper + Open AI + 11labs

![image](https://github.com/moreshk/pirate-bot/assets/4209287/4ec43f05-1a9d-4275-8daf-b69c59967ade)

# Voice-to-Voice Chatbot

A voice-to-voice chatbot powered by OpenAI GPT-3.5 Turbo and ElevenLabs. The chatbot transcribes the audio input using OpenAI's Whisper ASR system, generates a response with GPT-3.5 Turbo, and then converts the response into spoken audio using the ElevenLabs Text-to-Speech API.

## Getting Started

1. Clone this repository.
2. Install the required packages by running `pip install -r requirements.txt` (you should have Python 3.6 or later installed).
3. Create a `.env` file in the root directory of this project and set your OpenAI API key and ElevenLabs API key.

Example `.env` file:


## Running the Server

You can start the Flask server by running the command: `python app.py`. This will start the server on `http://127.0.0.1:5000/`.

## Endpoints

- `GET /` - Render the index page.
- `POST /transcribe` - Transcribe the given audio to text using Whisper. Requires a `file` parameter with the file data.
- `POST /ask` - Generate a ChatGPT response from the given conversation, then convert it to audio using ElevenLabs. Requires a `conversation` parameter with the conversation data.
- `GET /listen/<filename>` - Return the audio file located at the given filename.

## License

This project is licensed under the terms of the MIT license.



