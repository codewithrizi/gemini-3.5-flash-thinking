# gemini-3.5-flash-thinkingComplete Setup Guide (Everything Included)
1. Install Python

Download from: https://www.python.org/downloads/
During installation, check Add python.exe to PATH
Verify:

PowerShellpython --version
2. Install Node.js (for Claude Code)

Download from: https://nodejs.org
Install LTS version
Verify:

PowerShellnode --version
3. Install Claude Code (Optional)
PowerShellnpm install -g @anthropic-ai/claude-code
4. Download Gemini Web2API

Download the project ZIP from GitHub
Extract to Desktop
Folder path should be:

textC:\Users\YourName\Desktop\gemini-web2api-main\gemini-web2api-main
5. Install Dependencies
PowerShellcd $env:USERPROFILE\Desktop\gemini-web2api-main\gemini-web2api-main
pip install httpx
6. Start Gemini Server
PowerShellpython gemini_web2api.py
You should see:
textListening: http://0.0.0.0:8081
Keep this terminal open.

VS Code + Continue.dev Setup

Install extension: Continue - open-source AI code agent
Create config file:

PowerShellnotepad "$env:USERPROFILE\.continue\config.yaml"
Paste this:
YAMLname: Local Gemini
version: 1.0.0
schema: v1

models:
  - name: Gemini Local
    provider: openai
    model: gemini-3.5-flash-thinking
    apiBase: http://localhost:8081/v1
    apiKey: sk-123

Restart VS Code
Press Ctrl + L and select Gemini Local


ChatBox Setup

Download: https://chatboxai.app
Settings → Model:

textAPI Mode  : OpenAI API Compatible
API Host  : http://localhost:8081/v1
API Key   : sk-123
Model     : gemini-3.5-flash-thinking

Cherry Studio Setup

Download: https://cherry-ai.com
Settings → Providers → OpenAI Compatible:

textAPI Base URL : http://localhost:8081/v1
API Key      : sk-123
Model        : gemini-3.5-flash-thinking

Useful Commands
PowerShell# Start Gemini Server
cd $env:USERPROFILE\Desktop\gemini-web2api-main\gemini-web2api-main
python gemini_web2api.py

# Edit Continue Config
notepad "$env:USERPROFILE\.continue\config.yaml"

# Check Python
python --version

# Check Node
node --version

Important Notes

Always start the Gemini server first
Keep the server terminal open
Open a folder in VS Code before creating files with Continue
Recommended model: gemini-3.5-flash-thinking
