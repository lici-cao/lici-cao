# Hi, I'm lici-cao 👋

*English · [简体中文](README.md)*

I build products that actually land on the desktop: full-stack systems with Spring Boot + Vue, then built in the cloud with GitHub Actions and packaged by jpackage into a Windows installer you can double-click. I care less about getting a demo to run than about whether it installs cleanly on someone else's machine, keeps working, and recovers when something fails.

[All projects](https://github.com/lici-cao?tab=repositories) · [AI apps](#-ai-apps) · [Coursework & systems](#-coursework--systems) · [Stack](#-stack)

---

## 📝 Currently building: FitLife

Turning training plans from gut feeling into something executable. FitLife is an AI-powered workout plan generator that uses a 100-exercise reviewed library as its knowledge source, chaining user profile, rule-based filtering, and LLM orchestration into a verifiable pipeline that outputs daily exercises, sets, RPE, and estimated calories.

[fitlife-desktop](https://github.com/lici-cao/fitlife-desktop) · Spring Boot 3 + Vue 3

Diet and workout logging, calorie balance charts, BMI / BMR / TDEE calculation, and a workstation-style AI chat page.

Chat as execution: say "build me a one-week fat-loss plan, dumbbells only, bad knees" and it really filters exercises under those constraints, arranges a weekly plan, and persists it; ask "how should I pair chest day", and it picks a structured set of exercises with sets and form notes from the library.

Model choice and graceful degradation: switch between DeepSeek, Doubao, and GLM in the chat page; models without a key are greyed out, and when AI is unavailable the system falls back to a built-in rule engine — still functional, never a blank screen.

Built for delivery, not for demos: one-click script with idempotent database migration, exercise library auto-seeded on startup, Windows installer built in the cloud, and no plaintext keys in the repo.

---

## 🧠 AI apps

Let the model do what it is good at; keep validation and fallbacks on the engineering side.

🍎 [**FitLife**](https://github.com/lici-cao/fitlife-desktop) · Java

AI workout plan generator. Retrieval-augmented exercise library plus rule filtering and LLM orchestration, with out-of-range exerciseId rejected; a unified `LlmGateway` speaks to multiple OpenAI-compatible providers with SSE streaming.

🤖 [**ASu-skills**](https://github.com/lici-cao/ASu-skills)

A practical collection of AI Skills for job hunting and development: resume polishing, job applications, interview prep, and dev productivity.

---

## 🖥️ Coursework & systems

Turning textbook layered architecture into complete systems that run and can be demoed.

📦 [**jxcexample**](https://github.com/lici-cao/jxcexample) · Java

An inventory management system example with a complete loop of products, stock, documents, and statistics — usable as a course design foundation.

📚 [**booksmanagement**](https://github.com/lici-cao/booksmanagement) · Java

A book management system for coursework: classic CRUD plus permission practice.

🎵 [**licimusic**](https://github.com/lici-cao/licimusic) · JavaScript

An immersive music player built around cinematic shots, particle visuals, and a lyric stage.

---

## 🛠️ Stack

| Layer | Tech |
| --- | --- |
| Backend | Java 17, Spring Boot 3, Spring Security, JWT, Spring Data JPA |
| Frontend | Vue 3, TypeScript, Vite, Element Plus, Pinia, ECharts |
| Data | MySQL 8 (utf8mb4), idempotent migration scripts |
| AI | DeepSeek, Doubao (Volcengine Ark), Zhipu GLM behind one OpenAI-compatible gateway with SSE |
| Delivery | GitHub Actions cloud build, jpackage Windows installer, one-click start scripts |

---

If something here solves a problem for you, give it a try and tell me in that project's Issues what does not work. Real feedback is usually where the next improvement starts.
