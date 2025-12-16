# ASPEN — AI Voice Assistant

ASPEN is an open-source AI voice assistant that performs tasks efficiently and safely.
Developed and maintained by Lyman Cameron under the grov organization.

ASPEN integrates speech-to-text (STT), text-to-speech (TTS), and a modular action system
to execute real tasks locally or via cloud services. Its design prioritizes privacy,
modularity, and professional-grade automation.

---

## Table of Contents

1. Features
2. Architecture
3. Installation
4. Usage
5. Configuration
6. Contributing
7. License
8. Acknowledgements

---

## Features

- Speech-to-Text: Powered by OpenAI Whisper for high accuracy
- Text-to-Speech: Powered by ElevenLabs with local fallback options
- Modular Action System: Create, customize, and extend actions
- Silent Web Search: Google Search API integration without opening a browser
- Live Data Feeds: News from MSN and financial data via Alpha Vantage
- Local-first, Cloud-optional: Run entirely on your machine or leverage cloud processing
- Custom Voice Models: Build or integrate new voice profiles for unique experiences

---

## Architecture

ASPEN is structured as a modular system for maintainability and scalability:

grov
└── ASPEN
    ├── Core           ← Main logic and task execution
    ├── Voices         ← STT/TTS integrations
    ├── Actions        ← Predefined and custom task handlers
    ├── GUI            ← React frontend
    ├── Tools          ← Utilities & plugins
    └── Config         ← Environment and user settings

Backend: Python 3.11+, OpenAI Whisper, ElevenLabs TTS
Frontend: React.js, modern UI with real-time feedback
Data Flow: Modular design — voice input → action router → execution → response

---

## Installation

Active development — features may change

Clone the repo:

git clone https://github.com/grov/aspen-assistant.git
cd aspen-assistant

### Backend

cd src/backend
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
pip install -r requirements.txt

### Frontend

cd src/frontend
npm install
npm start

ASPEN should now be running locally. Open your browser to the configured local URL for the GUI.

---

## Usage

Start ASPEN via backend script:

python main.py

Interact via GUI or command-line interface.

Example actions:
- "Search for latest tech news."
- "Send a text message to my brother."
- "Open VS Code in my projects folder."

Custom actions can be added via /src/backend/actions.

---

## Configuration

Environment variables stored in .env (ignored by Git)

Example .env:

OPENAI_API_KEY=<your_key>
ELEVENLABS_API_KEY=<your_key>
GOOGLE_API_KEY=<your_key>
ALPHA_VANTAGE_KEY=<your_key>

Configure voice models, action settings, and GUI preferences in /config.

---

## Contributing

Contributions are welcome under the GPL v3 license:

- Report issues or bugs
- Submit pull requests for features, fixes, or enhancements
- Add voice models or action scripts
- Improve documentation and examples

See CONTRIBUTING.md for full guidelines.

---

## License

This project is licensed under the GNU GPL v3.

Copyright (c) 2025 Lyman Cameron / grov
https://www.gnu.org/licenses/gpl-3.0.html

---

## Acknowledgements

- OpenAI Whisper — Speech-to-Text
- ElevenLabs — Text-to-Speech
- Alpha Vantage — Financial Data
- Google Search API — Search Integration
- Inspired by modern assistants like Cortana, Copilot, and Siri

---

Developed and maintained by Lyman Cameron under the grov organization.
