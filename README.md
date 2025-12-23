# Claude-Code-with-Google-Gemini-on-Windows-WSL2

This repository provides a step-by-step guide to setting up Claude Code on Windows using WSL2, powered by Google Gemini via the Claude Code Router.
---

## 🛠 Step 0: Install Windows Subsystem for Linux (WSL)

**Important:** This is the first thing you need to do. We are setting up a Linux environment where **Claude Code** will run.

### 1. Open PowerShell as Administrator

* Press the **Windows** key
* Search for **PowerShell**
* Click **Run as administrator**
* Click **Yes**

### 2. Run the Install Command

```powershell
wsl --install
```

### 3. Downloading & Launching

* Windows will download and install WSL
* Ubuntu will launch automatically
* Stay in the same window while it provisions

### 4. Set Your Username & Password

* Enter a **username**
* Enter a **password**
* Confirm the password

> ⚠️ Password typing is hidden. This is normal in Linux.

### 5. Success

When you see something like:

```bash
hammad@PC:/mnt/c/WINDOWS/system32$

```

Keep this terminal open and continue.

---

## ⚡ Method 1: Automated "Speedrun" Script

### 1. Run the Installer
Inside your **WSL / Ubuntu** terminal, run:

```bash
curl -sSL https://raw.githubusercontent.com/devhammad0/claude-code-router-setup/main/scripts/install.sh | bash

```

> After the script finishes:

```bash
source ~/.bashrc
```

### 2. Set Your Google API Key
Replace `YOUR_KEY_HERE` with your key from <a href="https://aistudio.google.com/" target="_blank">Google AI Studio</a>:

```bash
echo 'export GOOGLE_API_KEY="YOUR_KEY_HERE"' >> ~/.bashrc
```

### 3. Reload your Environment

```bash
source ~/.bashrc
```

### 4. Laucnh Claude Code Router

```bash
ccr code
```
