# 🤖 Jarvis AI Agent

A powerful, autonomous AI assistant that controls your computer like a digital assistant. Inspired by Manus AI, Jarvis can open applications, search the web, control Spotify, automate tasks, and more—all through natural language commands.

## ✨ Features

- 🖥️ **Desktop Automation**: Open applications, control windows, click and type
- 🎵 **Spotify Integration**: Play songs, artists, playlists, and control playback
- 🌐 **Web Control**: Search Google, Wikipedia, check weather, open websites
- ⌨️ **Keyboard & Mouse**: Full control over input devices
- 🔧 **System Commands**: Execute system-level commands
- 💬 **Natural Language**: Just tell Jarvis what you want in plain English

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- An Anthropic API key (get one free at [console.anthropic.com](https://console.anthropic.com))
- (Optional) Spotify API credentials

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/devmata707-alt/jarvis-ai.git
   cd jarvis-ai
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```

5. **Edit `.env` with your API keys**
   ```
   ANTHROPIC_API_KEY=your_api_key_here
   SPOTIFY_CLIENT_ID=your_spotify_id (optional)
   SPOTIFY_CLIENT_SECRET=your_spotify_secret (optional)
   ```

6. **Run Jarvis**
   ```bash
   python jarvis_agent.py
   ```

## 📝 Usage Examples

Once Jarvis is running, try these commands:

### Desktop & Applications
```
"Open Chrome"
"Open Spotify"
"Open VS Code"
"Take a screenshot"
```

### Web Searching
```
"Search Google for Python tutorials"
"Look up artificial intelligence on Wikipedia"
"What's the weather in New York?"
"Open GitHub"
```

### Spotify Music Control
```
"Play Blinding Lights by The Weeknd"
"Play artist Drake"
"Play my Workout playlist"
"Skip to the next song"
"Pause the music"
"Resume playback"
```

### System Control
```
"Click at coordinates 500, 300"
"Type hello world"
"Press Enter"
"Open a new tab with Ctrl+T"
"Execute ls command"
```

## 🏗️ Project Structure

```
jarvis-ai/
├── jarvis_agent.py          # Main agent core
├── computer_control.py      # Desktop automation
├── spotify_control.py       # Spotify integration
├── web_search.py           # Web searching
├── requirements.txt        # Python dependencies
├── .env.example           # Environment template
├── README.md              # This file
└── .gitignore
```

## 🔑 Getting API Keys

### Anthropic API Key (Required)
1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up for a free account
3. Navigate to API keys
4. Create a new API key
5. Copy it to your `.env` file

### Spotify Credentials (Optional)
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new app
3. Accept the terms and create
4. Copy your Client ID and Client Secret
5. Add them to your `.env` file
6. First time you use Spotify features, it will open a browser for authentication

## 🛠️ Architecture

```
┌─────────────────────────────────┐
│   Claude AI (claude-3-5-sonnet) │
└──────────────┬──────────────────┘
               │
        ┌──────▼────────┐
        │  Jarvis Agent │
        └──────┬────────┘
               │
      ┌────────┴────────┬───────────┬──────────────┐
      │                 │           │              │
┌─────▼─────┐  ┌───────▼──┐  ┌──────▼──┐  ┌──────▼──┐
│ Computer  │  │ Spotify  │  │   Web   │  │ System  │
│ Control   │  │ Control  │  │ Search  │  │Commands │
└───────────┘  └──────────┘  └─────────┘  └─────────┘
      │              │           │              │
      └──────────────┴───────────┴──────────────┘
                     │
            ┌────────▼─────────┐
            │ Your Computer &  │
            │ External Services│
            └──────────────────┘
```

## 📚 Available Tools

### Desktop Control
- `open_application` - Open apps
- `click_mouse` - Click at coordinates
- `type_text` - Type text
- `press_key` - Press keys
- `hotkey` - Keyboard shortcuts
- `execute_command` - Run system commands

### Music
- `play_song` - Play specific songs
- `play_artist` - Play by artist
- `play_playlist` - Play playlists
- `spotify_next/previous` - Skip tracks
- `spotify_pause/resume` - Control playback

### Web
- `search_google` - Google search
- `search_wikipedia` - Wikipedia search
- `get_weather` - Weather information
- `open_website` - Open URLs

## 🔒 Security Notes

- Never share your API keys
- Keep your `.env` file private
- Use environment variables for sensitive data
- Be careful with system commands

## 🤝 Contributing

Feel free to fork, improve, and submit pull requests!

## 📄 License

This project is open source and available under the MIT License.

## 🆘 Troubleshooting

### "ANTHROPIC_API_KEY not found"
- Make sure you've created a `.env` file
- Copy from `.env.example`
- Add your actual API key

### Spotify not working
- Spotify credentials are optional
- First use will open a browser for authentication
- Make sure you have a Spotify account (free or premium)

### Mouse/Keyboard not responding
- Ensure Jarvis has necessary permissions
- On macOS, may need accessibility permissions
- On Windows, run as Administrator if needed

### Import errors
- Make sure all dependencies are installed: `pip install -r requirements.txt`
- Use a virtual environment to avoid conflicts

## 🌟 Future Enhancements

- Voice input/output
- Computer vision for GUI automation
- Task scheduling and reminders
- More app integrations (YouTube, Gmail, etc.)
- Web interface dashboard
- Multi-user support
- Plugin system for custom tools

## 💬 Support

If you encounter issues or have questions, please open an issue on GitHub.

---

**Made with ❤️ by devmata707-alt**

Start chatting with Jarvis now: `python jarvis_agent.py`
