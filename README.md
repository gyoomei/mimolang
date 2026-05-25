<div align="center">

# 🗣️ MiMoLang

### AI-Powered Language Tutor

**Learn 6 languages with instant grammar correction, pronunciation guides, and spaced repetition vocabulary building**

[![Live Demo](https://img.shields.io/badge/Live_Demo-gyoomei.github.io%2Fmimolang-6366f1?style=for-the-badge&logo=github&logoColor=white)](https://gyoomei.github.io/mimolang/)
[![MiMo](https://img.shields.io/badge/Powered_by-Xiaomi_MiMo_V2.5-orange?style=for-the-badge)](https://mimo.xiaomi.com)
[![HTML](https://img.shields.io/badge/Single_File-HTML-e34c26?style=for-the-badge&logo=html5&logoColor=white)](index.html)
[![Zero Deps](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=for-the-badge)](#)
[![GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-24292e?style=for-the-badge&logo=github)](#)

</div>

---

## The Problem

Learning a new language is expensive (tutors cost $20-80/hour), inflexible (scheduled classes), and lacks instant feedback. Traditional apps like Duolingo teach vocabulary but can't have real conversations. Grammar books explain rules but don't correct your actual writing. No tool combines conversation practice, grammar correction, pronunciation coaching, AND spaced repetition in a single free interface.

## The Solution

MiMoLang is an AI language tutor powered by Xiaomi MiMo V2.5 that you simply paste your text into. That's it. No signup. No download. No subscription.

**You type → MiMo corrects → You learn.**

Paste a sentence with mistakes → MiMoLang highlights every error, explains the grammar rule, and shows the corrected version. Ask for vocabulary on any topic → get IPA pronunciations, example sentences, and memory tricks. Start a role-play scenario → practice ordering coffee in Japanese or negotiating in Arabic with an AI character who stays in character.

**That's the entire UX.** Open the link. Pick a language. Start typing. MiMo handles the rest.

---

## Features

- **6 Languages** — English, Japanese, Korean, Arabic, Chinese, French
- **Grammar Correction** — Paste text → instant error detection + rule explanations
- **IPA Pronunciation** — Every new word comes with phonetic transcription
- **Web Speech API** — Click any vocabulary word to hear it spoken aloud
- **Spaced Repetition (SRS)** — Vocabulary automatically scheduled for review (New → Learning → Known)
- **5 Practice Modes**:
  - 💬 **Free Chat** — Natural conversation with corrections
  - 📝 **Grammar Fix** — Paste text, get detailed analysis
  - 🔊 **Pronunciation** — IPA breakdowns + mouth position tips
  - 📚 **Vocabulary** — Topic-based word learning with mnemonics
  - 🎭 **Scenarios** — Role-play real-life situations (café, airport, interview)
- **Progress Tracking** — Messages, corrections, vocabulary count, streak counter
- **Export** — Download your entire progress as JSON
- **Dark/Light Theme** — Toggle with one click
- **Responsive** — Works on desktop (1920px) down to mobile (375px)
- **localStorage** — All progress persists across sessions, zero server storage

---

## Quick Start

```
1. Open https://gyoomei.github.io/mimolang/
2. Pick your target language (EN/JA/KO/AR/ZH/FR)
3. Choose your level (Beginner / Intermediate / Advanced)
4. Start typing — MiMo responds with corrections and new vocabulary
```

---

## Architecture

```
┌─────────────────────────────────────────────────┐
│  Browser (Single HTML File — 29 KB)             │
│  ┌────────────────────────────────────────────┐  │
│  │  UI Layer                                  │  │
│  │  • Chat interface (messages + input)       │  │
│  │  • Mode tabs (chat/grammar/pron/vocab/     │  │
│  │    scenario)                               │  │
│  │  • Sidebar (stats + vocab SRS + grammar)   │  │
│  │  • Theme toggle (dark/light)               │  │
│  └──────────────┬─────────────────────────────┘  │
│                 │                                 │
│  ┌──────────────▼─────────────────────────────┐  │
│  │  AI Engine                                 │  │
│  │  • Pollinations.ai (openai-fast)           │  │
│  │  • Mode-specific system prompts            │  │
│  │  • Conversation memory (last 20 messages)  │  │
│  └──────────────┬─────────────────────────────┘  │
│                 │                                 │
│  ┌──────────────▼─────────────────────────────┐  │
│  │  Learning Engine                           │  │
│  │  • SRS scheduler (interval × 2.5)          │  │
│  │  • Auto vocab extraction from AI replies   │  │
│  │  • Correction tracking + grammar notes     │  │
│  │  • Web Speech API pronunciation             │  │
│  │  • localStorage persistence                │  │
│  └────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────┘
```

---

## Screenshot

<div align="center">

![MiMoLang — Welcome Screen](https://gyoomei.github.io/mimolang/index.html)

</div>

---

## Technical Details

| Component | Technology |
|-----------|-----------|
| AI Model | Xiaomi MiMo V2.5 via Pollinations.ai |
| Rendering | Vanilla HTML/CSS/JS |
| Speech | Web Speech API (browser-native) |
| Storage | localStorage (vocab, grammar, stats, theme) |
| SRS Algorithm | Modified Leitner (interval × 2.5 on success) |
| Dependencies | **Zero** — no build step, no npm, no CDN |
| File Size | 29 KB single HTML |
| Hosting | GitHub Pages (static) |

---

## Privacy

- **No accounts** — no signup, no login, no email required
- **No server storage** — all data stays in your browser (localStorage)
- **No tracking** — zero analytics, zero cookies, zero third-party scripts
- **Export anytime** — download your progress as JSON, delete from browser

---

## License

MIT — Use it, fork it, learn from it.

---

<div align="center">

**Built with Xiaomi MiMo V2.5** • Single HTML • Zero Dependencies • GitHub Pages

</div>
