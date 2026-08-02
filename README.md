
## Complete Setup Guide (Everything Included)

##  1. Install Python 
 1. Download From: Https://www.python.org/downloads/ 
 2. During Installation, Check **add Python.exe To Path**
 3. Verify:  ```powershell Python   Version
## 2. Install Node.js (for Claude Code)

 1.Download from: https://nodejs.org

2.Install LTS version
Verify:
PowerShell->node --version
## 3. Install Claude Code (Optional)

powershell:

npm install -g @anthropic-ai/claude-code
## 4. Download Gemini Web2API 

1.Download the project ZIP from GitHub 

2.Extract to Desktop 

3.Folder path should be:

C:\Users\YourName\Desktop\gemini-web2api-main\gemini-web2api-main
## 5. Install Dependencies

PowerShell-->

cd $env:USERPROFILE\Desktop\gemini-web2api-main\gemini-web2api-main
pip install httpx
## 6. Start Gemini Server

PowerShell-->

python gemini_web2api.py

You should see:

Listening: http://0.0.0.0:8081

Keep this terminal open.
## 🔷👨‍💻VS Code + Continue.dev Setup

1.Install extension: Continue - open-source AI code agent

2.Create config file:

PowerShell--> notepad "$env:USERPROFILE\.continue\config.yaml"

A Notepad will open. Type or paste the given code into it:

name: Local Gemini

version: 1.0.0

schema: v1

models:
  - name: Gemini Local

    provider: openai

    model: gemini-3.5-flash-thinking

    apiBase: http://localhost:8081/v1

    apiKey: sk-123

3.Restart VS Code

4.Press Ctrl + L and select Gemini Local


## 🤖💬ChatBox Setup

1.Download: https://chatboxai.app

2.Settings → Model:

API Mode  : OpenAI API Compatible

API Host  : http://localhost:8081/v1

API Key   : sk-123

Model     : gemini-3.5-flash-thinking
## 🍒Cherry Studio Setup

1.Download: https://cherry-ai.com

2.Settings → Providers → OpenAI Compatible:

API Base URL : http://localhost:8081/v1

API Key      : sk-123

Model        : gemini-3.5-flash-thinking
## 🏷️Useful Commands PowerShell

1.Start Gemini Server
cd $env:USERPROFILE\Desktop\gemini-web2api-main\gemini-web2api-main
python gemini_web2api.py

2.Edit Continue Config
notepad "$env:USERPROFILE\.continue\config.yaml"

3.Check Python
python --version

5.Check Node
node --version
## ✍Important Notes

1.Always start the Gemini server first

2.Keep the server terminal open

3.Open a folder in VS Code before creating files with Continue

5.Recommended model: gemini-3.5-flash-thinking
