# Hexium Staff Tools & Infrastructure 🛡️⚙️

A collection of custom-developed tools, moderation bots, and resources built to maintain, secure, and improve the **Hexium** community platform (11,000+ users).

These tools are designed to handle the heavy lifting of moderation, allowing the staff team to focus on community engagement rather than manual policing.

## 📦 Contents

### 1. `hexium_mod.py` (Discord Auto-Moderator)
A powerful, local-first Discord bot that automatically deletes messages containing severe slurs, bypasses, and spam.
- **Regex Filter:** Catches hard slurs, soft slurs, and bypasses (e.g., `n1gg3r`, `m3gga`).
- **Human-in-the-Loop:** Does not auto-ban. It deletes the message, times out the user for 10 minutes, and sends an alert to the head moderator.
- **Spam Protection:** Detects rapid-fire messages and flags them for review.

### 2. `asset_sentinel.py` (AI Asset Scanner)
An advanced pre-check bot for Roblox clothing templates and audio files.
- **Local AI Vision:** Uses Ollama (`llava`) to scan clothing templates for hate symbols, NSFW content, and offensive text.
- **Audio Bypass Detection:** Uses `ffmpeg` and `mutagen` to catch corrupted headers and malicious files disguised as audio.
- **Approval Workflow:** Sends a preview and AI report to a private staff channel. Staff can reply with `!approve` or `!reject`. If rejected, a local LLM generates a polite TOS-compliant rejection message for the user.

### 3. `Hexium Community Rules.txt`
The official, comprehensive ruleset for the platform. This is used as the source of truth for all moderation actions and AI prompts.

## 🛠️ Prerequisites
To run these tools locally, you will need:
- **Python 3.10+**
- **Ollama** (Running locally with `llava` and `llama3.2` pulled)
- **FFmpeg** (Added to your system PATH)
- **Discord Bot Token**

## 🚀 Setup & Usage
*(See the individual files for detailed setup instructions)*

1. Clone the repository:
   ```bash
   git clone https://github.com/Qrdz0/hexium-stuff.git
