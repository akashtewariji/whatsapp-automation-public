# WhatsApp Automation Suite - User Manual

Welcome to the comprehensive guide for using the WhatsApp Automation suite. This document covers setup, usage, and frequently asked questions for all versions from V1 to V6.

---

## 🚀 Quick Start Guide

### For Browser Extensions (V1 - V5)
1. **Installation**:
   - Open Chrome and go to `chrome://extensions/`.
   - Enable **Developer Mode** (top right).
   - Click **Load unpacked** and select the folder of the version you wish to use (e.g., `v5`).
2. **Accessing the UI**:
   - Open [WhatsApp Web](https://web.whatsapp.com).
   - Look for the **⚡** or **⚙️** floating button on the bottom right of the screen.
3. **Enabling Automation**:
   - Click the button to open the **Control Panel**.
   - Toggle the **Automation Status** to "ON".

### For Standalone Web App (V6)
1. **Launch**:
   - Open the [v6/index.html](v6/index.html) file in any modern web browser.
2. **Setup**:
   - Navigate to the **Automations** tab to add your rules.
   - Use the **NLP Match Bench** to test if your messages will trigger the correct response.

---

## 🛠 Features by Version

| Version | Requirement | Key Highlights |
| :--- | :--- | :--- |
| **V1** | "tell " prefix | Basic hardcoded automation. |
| **V2** | "tell " prefix | Stability locking & heartbeat monitor. |
| **V3** | No prefix | Fuzzy inclusive matching & Action cooldowns. |
| **V4** | No prefix | Glassmorphism UI & persistent Rule Management. |
| **V5 (Golden)** | No prefix | **NLP Standardization** & Response Templates. |
| **V6** | Standalone | Full Dashboard & Cross-browser compatibility. |

---

## 📝 Customizing Responses (V4 - V6)

### Adding Rules
- **Pattern**: The keyword or phrase to look for (e.g., "iphone screen").
- **Response**: The text to send back (e.g., "$50").
- **NLP Matching (V5/V6)**: Our matching is smart! If your rule is "iphone screen," it will match "How much for iphone11 screen repair?"

### Using Templates (V5/V6)
You can customize how the final message looks in Settings using:
- `{incoming}`: Inserts the matched keyword.
- `{response}`: Inserts your defined reply.
- **Example**: `{incoming}\nPrice: {response}` becomes:
  > iphone screen
  > Price: $50

---

## ❓ Frequently Asked Questions (FAQ)

### 1. Why isn't the bot replying?
- **Extension (V1-V5)**: Ensure you are on `web.whatsapp.com` and the "Automation Status" is ON.
- **Rules Match**: Check if your message contains the *exact* keywords from your rule. Use the V6 Match Bench to test.
- **Self-Replies**: The bot is designed to ignore messages sent by *you* to prevent loops.

### 2. Can I use multiple lines in my reply?
Yes! Use `\n` in the response input field to indicate a line break. 
- **Example**: `Hello!\nHow can I help?`

### 3. I see a Voice Message (Mic) icon instead of the Send button.
This happens if WhatsApp's React state doesn't sync correctly. 
- **Fix**: We resolved this in the **V5 Golden Version**. Ensure you are using V5 or V6 for the most reliable sending logic.

### 4. How do I share logs with a developer?
Open the Control Panel and click **📧 Share Logs with Developer**. It will automatically format and send the technical logs to the dev team.

---

## 🛡 Stability & Privacy
- **Local Storage**: All your rules and settings are stored *locally* in your browser. No data is sent to external servers.
- **Echo Protection**: The bot will never reply to itself or get stuck in a "ping-pong" loop.
- **Cooldowns**: Standard 3-second delay between actions to mimic natural human behavior.
