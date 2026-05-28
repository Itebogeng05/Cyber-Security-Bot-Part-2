# CyberSecurity Awareness Bot — Part 2

A WPF desktop chatbot application built in C# that educates users about cybersecurity threats through a chat interface. With a mordern text style and Sentiment detection to make it feel a little more comfortable.

---

## How to Run

1. Open the solution in **Visual Studio 2019 or 2022**
2. Press the "run program" button to launch it.
3. The chat window will open and the bot will greet you

---

## Features

| Feature | Description |
|---|---|
| **WhatsApp-style GUI** | Bot messages bubble on the left, user messages on the right |
| **Keyword Recognition** | Detects topics like password, phishing, malware, privacy, 2FA, and more |
| **Random Responses** | Randomly picks from a list of tips so responses stay varied |
| **Sentiment Detection** | Detects if the user is worried, frustrated, or curious and responds accordingly |
| **Memory & Recall** | Remembers the user's name and favourite topic to personalise responses |
| **Conversation Flow** | Say "tell me more" or "give me another tip" to continue on the last topic |
| **Error Handling** | Returns a helpful default message for unrecognised inputs |
| **Voice Greeting** | Plays a greeting sound on startup if `greeting.wav` is found |
| **Online & Typing Indicator** | Bot shows "typing..." before responding and "Online" on top to feel more natural |

---

## Supported Keywords

Type any of these to get a cybersecurity tip:

- `password` — Password safety tips
- `phishing` / `scam` / `email fraud` — Phishing awareness
- `privacy` — Protecting personal data
- `browsing` / `website` / `internet` — Safe browsing habits
- `malware` / `virus` — Virus and malware protection
- `social engineering` / `vishing` / `smishing` — Manipulation tactics
- `2fa` / `two factor` / `authentication` — Two-factor authentication

---

## Conversation Examples

**Memory:**
> User: "I'm interested in privacy"
> Bot: "Got it! I'll remember you're interested in privacy..."

**Sentiment:**
> User: "I'm worried about scams"
> Bot: "It's completely understandable to feel that way. Scammers can be very convincing..."

**Follow-up:**
> User: "Tell me more"
> Bot: *(continues with another tip on the last topic)*

**Exit:**
> User: "bye"
> Bot: "Goodbye! Stay safe online — think before you click!"

---

## Project Structure

```
CyberSecurityBot_Part2/
├── App.xaml                  — Application entry point
├── App.xaml.cs
├── MainWindow.xaml           — WhatsApp-style UI layout (WPF)
├── MainWindow.xaml.cs        — All chatbot logic
├── App.config
└── CyberSecurityBot_Part2.csproj
```

---

## Key Classes & Methods

| Method | Purpose |
|---|---|
| `GetResponse()` | Main method — processes all user input |
| `GetSentimentPrefix()` | Detects user emotion and adds empathetic opening |
| `GetFollowUp()` | Continues the last topic when user asks for more |
| `Personalise()` | Uses stored favourite topic to personalise tips |
| `GetRandom()` | Picks a random tip from a list |
| `AddBotMessage()` | Creates a left-aligned chat bubble |
| `AddUserMessage()` | Creates a right-aligned chat bubble |
| `PlayGreeting()` | Plays greeting.wav on startup |

---

## Linking to Part 1

The voice greeting from Part 1 is automatically loaded if `greeting.wav` is found at either:
- The same folder as the `.exe` ← recommended
- `C:\Users\itebo\source\repos\CyberSecurityBot prt2\CyberSecurityBot prt2\greeting.wav`
-I used the same tips i used in part one

---
## Another additional thing
I added a picture of myself next to the name of the chatbot

## Requirements

- Visual Studio 2019 or 2022
- .NET Framework 4.7.2 (comes with Windows)
- No additional packages required
