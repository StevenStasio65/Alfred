# Jarvis - Voice-Powered Ollama Interface

Jarvis is a sophisticated voice-powered interface for Ollama, enabling natural voice conversations with local AI models. This application combines the power of local AI models with voice recognition and high-quality text-to-speech capabilities to create a seamless, voice-first AI assistant experience.

![Jarvis Voice Interface](https://github.com/Joelsoncash/Jarvis-/raw/main/screenshots/jarvis-interface.png)

## 🌟 Features

- **Voice-Powered Interaction**: Speak naturally to your AI assistant and hear responses in a human-like voice
- **Local AI Processing**: Leverages Ollama to run AI models locally on your machine for privacy and speed
- **High-Quality Text-to-Speech**: Uses ChatTTS for natural-sounding voice responses
- **Multiple AI Models**: Support for various Ollama models including deepseek-r1, llama2, mistral, phi3, and gemma
- **Desktop Application**: Packaged as an Electron app for a native desktop experience
- **Real-time Audio Visualization**: Visual feedback for microphone input levels
- **Responsive Design**: Works well on various screen sizes
- **Audio Caching**: Caches generated speech for improved performance

## 🔧 Technology Stack

### Frontend
- HTML5, CSS3, JavaScript
- Web Speech API for voice recognition
- Audio visualization with Web Audio API

### Backend
- Node.js with Express
- WebSockets for real-time communication
- Python for text-to-speech processing

### AI Integration
- Ollama for local AI model execution
- ChatTTS for high-quality text-to-speech synthesis

### Desktop Application
- Electron for cross-platform desktop application

## 📋 Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [Python](https://www.python.org/) (v3.8 or higher)
- [Ollama](https://ollama.ai/) installed and running
- At least one Ollama model pulled (recommended: `deepseek-r1:1.5b`)

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/Joelsoncash/Jarvis-.git
cd Jarvis-
```

### 2. Install Node.js dependencies

```bash
npm install
```

### 3. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 4. Ensure Ollama is installed and running

```bash
# Install Ollama from https://ollama.ai/
# Start the Ollama service
ollama serve
```

### 5. Pull the recommended model

```bash
ollama pull deepseek-r1:1.5b
```

## 🎮 Usage

### Running as a Desktop Application

```bash
npm start
```

This will launch the Electron desktop application with the Jarvis interface.

### Running as a Web Application

```bash
npm run server
```

Then open your browser and navigate to `http://localhost:3000`.

## 🔍 How It Works

1. **Voice Input**: The application uses the Web Speech API to capture and recognize your voice input.
2. **AI Processing**: Your query is sent to the Ollama API, which processes it using the selected local AI model.
3. **Text-to-Speech**: The AI's text response is converted to speech using ChatTTS, a high-quality text-to-speech system.
4. **Audio Playback**: The generated speech is played back through your speakers.

## 📁 Project Structure

```
jarvis/
├── asset/                  # TTS model assets
├── audio_cache/            # Cached audio files
├── public/                 # Frontend files
│   ├── app.js              # Frontend JavaScript
│   ├── index.html          # Main HTML interface
│   └── style.css           # CSS styling
├── main.js                 # Electron main process
├── ollama_voice.py         # CLI voice interface for Ollama
├── package.json            # Node.js dependencies
├── requirements.txt        # Python dependencies
├── server.js               # Express server
└── tts_service.py          # Text-to-speech service
```

## 🛠️ Configuration

### Changing the Default AI Model

You can select different AI models from the dropdown in the interface. The default model is `deepseek-r1:1.5b`, but you can use any model available in your Ollama installation.

### Audio Settings

The application automatically configures audio settings for optimal performance, including:
- Echo cancellation
- Noise suppression
- Auto gain control

## 🔒 Privacy

Jarvis processes all data locally on your machine:
- Voice recognition uses your browser's Web Speech API
- AI processing happens locally through Ollama
- Text-to-speech generation occurs on your local machine

No data is sent to external servers, ensuring your conversations remain private.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- [Ollama](https://ollama.ai/) for the local AI model execution
- [ChatTTS](https://github.com/jnordberg/ChatTTS) for the text-to-speech capabilities
- [Electron](https://www.electronjs.org/) for the desktop application framework
- [Express](https://expressjs.com/) for the web server
