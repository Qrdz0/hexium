# 🛡️ Hexium Staff Tools & Community Guide

![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Role](https://img.shields.io/badge/Role-Senior%20Moderator%20%26%20QA-blue)
![Platform](https://img.shields.io/badge/Platform-Hexium-purple)

A comprehensive collection of custom-developed tools, moderation guides, and resources built to maintain, secure, and improve the **Hexium** community platform (11,900+ users).

This repository contains the heavy-lifting infrastructure for the staff team, alongside a complete guide for the community.

---

## 🕰️ History & Origins

Hexium was created on **July 13, 2026** by **tae** to pass the legendary **Roskid** revival. The platform is currently owned and operated by **EMP (Emperor)**.

I joined just **12 days after the very first account was created**, making me a **Senior Moderator** and one of the earliest staff members of the platform. I've watched this community grow from its absolute beginning to what it is today.

### 🚀 Current Growth
- **Website Users:** 11,900+
- **Discord Members:** 8,000+

### 🎯 The Vision
Hexium is still growing, and I want to see it become the best revival platform out there. My hope for the future is that we focus on bringing back **classic simulators and older games**, rather than just being another hangout spot or filled with AI slop (even if some of it is admittedly good). We're building a real community here.

---

## 🔗 Important Links

- **Main Website / Sign Up:** [hexium.zip](https://hexium.zip/)
- **Discord Server:** [discord.gg/hexium](https://discord.gg/hexium)
- **Download Client:** [hexium.zip/download](https://hexium.zip/download)
- **Builders Club:** [hexium.zip/buildersclub](https://hexium.zip/buildersclub)
- **Promo Codes:** [hexium.zip/promocodes](https://hexium.zip/promocodes)
- **Password Reset:** [hexium.zip/forgotpasswordOrUsername](https://hexium.zip/forgotpasswordOrUsername)
- **Heximons:** [heximons.lol](https://heximons.lol/)
- **Legacy/Other Site** *(Currently unstable)*: [le.baljeet.club](https://le.baljeet.club/)

### 💰 Donations & Support
- **Ko-fi:** [ko-fi.com/hexium](https://ko-fi.com/hexium)
- **Direct Donation** *(PayPal & Crypto)*: [hexium.zip/donation](https://hexium.zip/donation)

---

## 💵 Economy: How to Earn Tix & Robux

Getting Tix and Robux in Hexium isn't actually that hard once you understand the loop. Here is the meta:

1. **Get Builders Club (OBC):** This is your first step. It unlocks the ability to get item drops and participate in the economy.
2. **Wait for Item Drops:** What are item drops? **EMP (the Owner)** will drop a new limited item and put it up for a community vote in the Discord. 
   - **⏰ Drop Times:** Drops usually happen between **4:00 PM and 5:30/6:00 PM EST** *(which is around 10:00 PM to 12:00 AM CET for the European community)*.
3. **The Resell Loop:** The community votes on the item, EMP reveals the results, and then puts the limited up for sale. Buy the limited when it drops. Once it's sold out, you can resell it to other players for a higher price to get more Robux. Keep this loop going to build your wealth.

### 🛠️ Other Ways to Get Rich
- **Make a Game:** Developing games on the platform is a massive way to earn Tix/Robux.
- **Reselling Clothes:** Design or flip clothing items for a profit.
- **Donate:** You can also donate to get Robux, which directly supports Hexium and helps keep the servers up and running.

*Note: Users typically receive around 500+ TIX per 24 hours automatically. If a user reports not getting TIX, check their account status/playtime on the site.*

---

## 🛡️ Moderation Action Times (Discord)

Consistency is key. Use the following timeouts for Discord chat infractions:

| Offense | Action / Duration |
| :--- | :--- |
| **Slurs** (Hard R, extreme hate speech) | **1 Hour Timeout** |
| **KYS / Telling someone to self-harm** | **30 Minutes to 1 Hour Mute** |
| **Low-tier Offenses** (Arguments, inappropriate behavior, hostile behavior) | **10 Minutes Timeout** |
| **Promotion / Mentioning other sites** | **10 Minutes Timeout** |

## 🎮 Moderation Action Times (In-Game Bans)

For in-game violations, apply the following ban durations:

| Offense | Action / Duration |
| :--- | :--- |
| **Slurs** (Depending on severity/context) | **1 to 3 Days Ban** |
| **Ban Evasion** | **1 Week Ban** |
| **Alting** (For farming Robux/Exploiting) | **Permanent Ban** |

---

## 📦 Included Staff Tools

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

---

## 🚀 Setup & Prerequisites

To run these tools locally, you will need:
- **Python 3.10+**
- **Ollama** (Running locally with `llava` and `llama3.2` pulled)
- **FFmpeg** (Added to your system PATH)
- **Discord Bot Token**

1. Clone the repository:
   ```bash
   git clone https://github.com/Qrdz0/hexium-stuff.git
