# Jarvis AI - Iron Man Inspired Assistant

A sophisticated AI assistant inspired by Jarvis from the Iron Man movie. Features natural language processing, voice interaction, system automation, and a witty British personality.

## Features

- 🎤 **Voice Recognition** - Speak naturally to Jarvis
- 🧠 **Natural Language Processing** - Understands context and intent
- 🤖 **AI-Powered Responses** - OpenAI GPT-based conversation engine
- 🎨 **Web Dashboard** - Beautiful UI to interact with Jarvis
- 🏠 **System Automation** - Execute commands and monitor system
- 💾 **Memory & Learning** - Remembers conversation context
- 🎭 **British Personality** - Sophisticated, witty, and helpful responses

## Tech Stack

- **Backend**: Python 3.9+
- **Frontend**: React + TailwindCSS
- **AI/NLP**: OpenAI API, spaCy
- **Voice**: SpeechRecognition, pyttsx3
- **Database**: SQLite
- **Framework**: Flask

## Project Structure

```
jarvis-ai/
├── backend/
│   ├── app.py                 # Main Flask application
│   ├── requirements.txt        # Python dependencies
│   ├── config.py              # Configuration settings
│   ├── jarvis/
│   │   ├── __init__.py
│   │   ├── voice_engine.py    # Speech recognition & synthesis
│   │   ├── nlp_engine.py      # Natural language processing
│   │   ├── ai_engine.py       # AI response generation
│   │   ├── command_executor.py # Execute system commands
│   │   ├── memory.py          # Conversation memory & context
│   │   └── personality.py     # Jarvis personality & styling
│   └── routes/
│       ├── __init__.py
│       ├── chat.py            # Chat endpoints
│       └── voice.py           # Voice interaction endpoints
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.js
│   └── package.json
├── tests/
├── .gitignore
├── docker-compose.yml
└── README.md
```

## Quick Start

### Prerequisites

- Python 3.9+
- Node.js 14+
- OpenAI API key
- Microphone for voice input

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/fidelhope143-ui/jarvis-ai.git
   cd jarvis-ai
   ```

2. **Setup Backend**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Configure Environment**
   ```bash
   cp .env.example .env
   # Edit .env and add your OpenAI API key
   ```

4. **Setup Frontend**
   ```bash
   cd ../frontend
   npm install
   ```

5. **Run the Application**
   ```bash
   # Terminal 1 - Backend
   cd backend
   python app.py
   
   # Terminal 2 - Frontend
   cd frontend
   npm start
   ```

Visit `http://localhost:3000` in your browser.

## Usage

### Voice Commands

- "Jarvis, what's the time?"
- "Jarvis, tell me a joke"
- "Jarvis, what's my CPU usage?"
- "Jarvis, open weather"
- "Jarvis, remind me to code later"

### Text Interaction

Simply type in the chat interface for a more private interaction.

## Configuration

Edit `backend/config.py` to customize:

- OpenAI model and parameters
- Voice settings (male/female, speed, volume)
- Personality traits and response style
- System commands access level
- Memory retention settings

## API Documentation

### Chat Endpoint

```
POST /api/chat
Content-Type: application/json

{
  "message": "What time is it?",
  "user_id": "user123",
  "context": "morning"
}
```

### Voice Endpoint

```
POST /api/voice
Content-Type: multipart/form-data

file: [audio_file]
user_id: user123
```

## Development

### Running Tests

```bash
cd backend
pytest tests/
```

### Code Structure

- **Voice Engine**: Handles speech recognition and text-to-speech
- **NLP Engine**: Processes user intent and extracts entities
- **AI Engine**: Generates contextual responses using GPT
- **Command Executor**: Safely executes system commands
- **Memory**: Maintains conversation history and user preferences
- **Personality**: Adds Jarvis-like character to responses

## Features Roadmap

- [ ] Smart home integration (Home Assistant)
- [ ] Multi-language support
- [ ] Advanced context awareness
- [ ] Proactive notifications
- [ ] Custom skill plugins
- [ ] Desktop app (Electron)
- [ ] Mobile app (React Native)
- [ ] Advanced analytics dashboard

## Contributing

Contributions are welcome! Please read our contributing guidelines and submit pull requests.

## License

MIT License - see LICENSE file for details

## Inspiration

Inspired by J.A.R.V.I.S. from Marvel's Iron Man universe - a sophisticated AI assistant with British charm, wit, and unwavering loyalty.

## Support

For issues, questions, or suggestions, please open an issue on GitHub.

---

*"I am putting myself to the fullest possible use, which is all I think that any conscious entity can ever hope to do."* - J.A.R.V.I.S.
