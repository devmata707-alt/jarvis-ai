# 🚀 Jarvis AI - Complete Setup Guide

Follow these steps to get Jarvis AI running on your computer.

## Step 1: Prerequisites

Make sure you have the following installed:

### Windows
- Python 3.8 or higher: [Download Python](https://www.python.org/downloads/)
- Git: [Download Git](https://git-scm.com/download/win)

### macOS
```bash
# Install Homebrew first if you don't have it
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Python
brew install python
```

### Linux
```bash
sudo apt-get update
sudo apt-get install python3 python3-pip git
```

## Step 2: Get Your API Keys

### Get Anthropic API Key (FREE)

1. Visit [https://console.anthropic.com](https://console.anthropic.com)
2. Click "Sign Up" and create an account
3. Verify your email
4. Go to "API Keys" section
5. Click "Create Key"
6. Copy the key (you'll need it soon)

**Free tier includes**: 
- $5 free credits per month
- Perfect for testing Jarvis

### Get Spotify Credentials (OPTIONAL)

If you want music control:

1. Go to [https://developer.spotify.com/dashboard](https://developer.spotify.com/dashboard)
2. Log in with your Spotify account (create one if needed - free version works)
3. Click "Create an App"
4. Accept the terms and create
5. You'll see your "Client ID" and "Client Secret"
6. Copy both (you'll need them)

## Step 3: Clone the Repository

### Windows (Command Prompt)
```bash
cd Desktop
git clone https://github.com/devmata707-alt/jarvis-ai.git
cd jarvis-ai
```

### macOS/Linux (Terminal)
```bash
cd ~
git clone https://github.com/devmata707-alt/jarvis-ai.git
cd jarvis-ai
```

## Step 4: Set Up Virtual Environment

This keeps dependencies isolated from your system Python.

### Windows
```bash
python -m venv venv
venv\Scripts\activate
```

You should see `(venv)` at the start of your terminal line.

### macOS/Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

You should see `(venv)` at the start of your terminal line.

## Step 5: Install Dependencies

```bash
pip install -r requirements.txt
```

Wait for all packages to install. You should see a message like:
```
Successfully installed anthropic pyautogui pyperclip ...
```

## Step 6: Configure Environment Variables

### Create .env file

#### Windows (Command Prompt)
```bash
copy .env.example .env
```

#### macOS/Linux (Terminal)
```bash
cp .env.example .env
```

### Edit the .env file

#### Windows
- Right-click the `.env` file
- Select "Open with" → "Notepad"

#### macOS/Linux
```bash
nano .env
```

Add your API keys:

```
ANTHROPIC_API_KEY=your_api_key_from_anthropic
SPOTIFY_CLIENT_ID=your_spotify_id_here
SPOTIFY_CLIENT_SECRET=your_spotify_secret_here
SPOTIFY_REDIRECT_URI=http://localhost:8888/callback
DEBUG=False
LOG_LEVEL=INFO
```

**Save and close the file**

## Step 7: Run Jarvis!

```bash
python jarvis_agent.py
```

You should see:
```
============================================================
🤖 JARVIS AI AGENT
============================================================
Hello! I'm Jarvis, your AI assistant.
I can control your computer, search the web, play music, and more.
Type 'quit' or 'exit' to stop.

📝 You: 
```

## Step 8: Try Your First Commands

Type any of these:

```
"Say hello"
"Search Google for Python"
"What's the weather in New York?"
"Open Chrome"
"Play Blinding Lights"
"Take a screenshot"
```

Just type and press Enter!

## 🎉 Success!

If you see responses from Jarvis, you're all set! 

## ❌ Troubleshooting

### "ModuleNotFoundError: No module named 'anthropic'"
```bash
pip install anthropic
```

### "ANTHROPIC_API_KEY not found"
- Make sure `.env` file exists in the jarvis-ai folder
- Make sure you added your actual API key (not the text "your_api_key_from_anthropic")
- Save and close the file properly

### Virtual environment not activating
Windows:
```bash
venv\Scripts\activate
```

macOS/Linux:
```bash
source venv/bin/activate
```

### "Permission denied" on macOS/Linux
```bash
chmod +x jarvis_agent.py
python jarvis_agent.py
```

### Python not found
Make sure Python is installed:
```bash
python --version
# or
python3 --version
```

If not installed, download from [python.org](https://www.python.org/downloads/)

### Spotify authentication fails
- First time using Spotify features, a browser window will open
- Click "Agree" to authorize
- You'll be redirected back
- If stuck, manually create a `.cache` file or clear browser cookies

## 📚 Next Steps

- Read the main [README.md](README.md) for more examples
- Check out example commands in the Features section
- Explore what Jarvis can do by giving it creative tasks!

## 💡 Tips

1. **Quit Jarvis**: Type `quit` or `exit`
2. **Multi-step tasks**: Jarvis can break down complex requests
3. **Be specific**: "Play Levitating by Dua Lipa" works better than "Play something"
4. **Check permissions**: Some features may need system permissions
5. **Keep it running**: Jarvis works better with multiple commands in sequence

## 🆘 Still Having Issues?

1. Check your API key is correct (no spaces, not the example text)
2. Make sure `.env` file is in the jarvis-ai folder
3. Try `pip install -r requirements.txt` again
4. Restart your terminal
5. Open an issue on GitHub with error messages

---

**You're all set! Start chatting with Jarvis:** 🚀

```bash
python jarvis_agent.py
```
