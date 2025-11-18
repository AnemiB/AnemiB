<div align="center">

# 🌺 Hi — I’m Anemi Breytenbach (AnemiB) 🌺

![Anemi's avatar](https://github.com/AnemiB.png)

</div>

---

## 🫧 About Me
I’m a third-year **Interactive Development (DV)** student majoring in **User Experience (UX)** at **Open Window**. I build user-centered applications that merge strong UX with practical engineering. My focus is on crafting polished, accessible interfaces and scalable app architectures that solve real user problems.

- Career focus: **Front-end / Mobile-first UX, Product-minded development, and rapid prototyping with an emphasis on accessibility and low-friction experiences.**
- I enjoy combining gaming, art and interaction design to create intuitive, delightful digital products.

---

## 🧭 Core Values & Approach
I design and build with three guiding principles:

1. **User-first** — decisions grounded in empathy and research.
2. **Practical polish** — prioritize clarity and simplicity while delivering production-ready features.
3. **Iterative learning** — prototype, test, and refine; document the why + how of every major change.

---

## 🦎 Skills & Career-Focused Tech Stack

**Front-end & Mobile**
- HTML, CSS, JavaScript, TypeScript  
- React, React Native (Expo), React-Bootstrap  
- UI/UX patterns, accessibility, responsive/mobile-first design

**Back-end & Data**
- Node.js, Express, .NET Core (C#)  
- Firebase (Firestore, Auth), PostgreSQL, MongoDB, MySQL

**Tools & Dev Practices**
- Git, GitHub, Docker, Electron (desktop packaging)  
- CI basics, testing, API documentation (Swagger)  
- Data visualization (Chart.js), Axios, SignalR

---

## 🛠 Tech stack badges
<!-- Replace `<your-github-username>` if using dynamic cards that require it -->
![React](https://img.shields.io/badge/React-17.0-blue)
![React Native](https://img.shields.io/badge/React_Native-Expo-brightgreen)
![TypeScript](https://img.shields.io/badge/TypeScript-4.x-blue)
![Node.js](https://img.shields.io/badge/Node.js-16.x-green)
![Firebase](https://img.shields.io/badge/Firebase-Firestore-orange)
![.NET](https://img.shields.io/badge/.NET-.NET_Core-9cf)

---

## 📂 Portfolio — Primary Repositories (DV major projects)
Below are the three repositories that represent my DV major work. Each entry includes: a concise overview paragraph followed by bullet points (role, problem, highlights), then a short process section explaining the *how* and *why* — suitable to copy into each repo’s README for DV300 process documentation.

---

### 1) 🌟 Aureum Elegance — `Aureum-Elegance-Frontend`
**Overview**  
Aureum Elegance is a full-stack warehouse management system designed for the perfume industry — centralising inventory, batch tracking, production workflows and analytics into a desktop/web app.

- **Role:** Full-stack lead (frontend + integration with .NET backend & Electron desktop packaging).  
- **Problem:** Perfume warehouses needed better traceability for fragile packaging, perishable ingredients and batch expiry — current tools were fragmented and error-prone.  
- **Highlights:** Batch expiry logic, lot/batch tracing, real-time low-stock alerts (SignalR), production recipe workflow, JWT role-based auth + 2FA, API with Swagger, Electron cross-platform packaging.

**How & Why (process documentation)**  
Aureum’s UX was structured around the warehouse user’s daily tasks: receiving, batching, producing, and dispatch. I started with contextual interviews and mapped workflows, then built wireframes prioritising fast scanning flows and clear expiry indicators.

- **Architecture:** React frontend ↔ .NET Core API ↔ PostgreSQL. Real-time events via SignalR for alert delivery on low stock.  
- **Why choices:** .NET chosen for existing backend university modules and strong typed modelling for batch logic; Electron to deliver a familiar desktop experience for warehouse staff.  
- **Development process:** iterative sprints, daily standups, feature branches + PR reviews, unit tests for core batch logic and E2E checks for critical flows.  
- **Challenges & learnings:** modeling perishable ingredients required designing a flexible expiry and batch meta model; learned trade-offs for offline-first desktop sync.  
- **How to run (summary):**
  - `git clone https://github.com/Tsebo200/Aureum-Elegance-Frontend`
  - Install: `npm install` (or `yarn`)
  - Set `.env` values for API base URL
  - `npm start` (dev) — for production build use Electron packaging steps in `/docs`
- **Future improvements:** offline sync improvements, more robust audit logs and QA automation for the production workflow.

---

### 2) 🫗 SipStop — `SipStop`
**Overview**  
SipStop is a compassionate sobriety companion built with **Expo (React Native + TypeScript)** and Firebase. It provides low-friction drink logging, sober streak tracking, mood-tagged reflections, and a small community feed.

- **Role:** Mobile app developer (product-led, end-to-end mobile implementation).  
- **Problem:** People reducing alcohol intake need a supportive, low-friction tool. Heavy clinical trackers can demotivate; SipStop aims to be approachable and encouraging.  
- **Highlights:** Fast drink logging, time-since-last-drink tracking, mood-tagged reflections, encouragement engine, community feed using Firestore listeners.

**How & Why (process documentation)**  
I designed SipStop for minimal friction: logging must take 2 taps and be forgiving. UX decisions were validated with low-fi prototypes and a small test group.

- **Architecture:** Expo app (React Native) ↔ Firebase (Auth + Firestore + Cloud Functions).  
- **Why choices:** Expo for rapid cross-platform development and easy builds; Firestore for real-time feeds and simple offline persistence.  
- **Development process:** user story mapping → clickable prototype → iterative development with feature toggles for encouragement engine. Focus on privacy and low-friction onboarding.  
- **Challenges & learnings:** balancing privacy with social features; implementing encouragement engine logic to avoid triggering language. Learned to write clear transformation tests for streak calculations.  
- **How to run (summary):**
  - `git clone https://github.com/AnemiB/SipStop`
  - `yarn` or `npm install`
  - Configure Firebase: `GOOGLE_SERVICES` files + set environment variables (do not commit secrets)
  - `expo start` to run locally
- **Future improvements:** localized content, richer analytics dashboard for personal trends, additional privacy toggles for community posts.

---

### 3) 🍽️ Nerdy Nibbles — `Nerdy-Nibbles`
**Overview**  
Nerdy Nibbles is an AI-first mobile app for food literacy — on-demand lessons and quizzes generated by an LLM with a built-in chat tutor (“Nibble AI”) for real-time questions.

- **Role:** Mobile-first developer; responsible for LLM integration patterns and UX for regeneratable lessons.  
- **Problem:** Food knowledge is scattered and static; learners want short, practical, personalised lessons and immediate answers.  
- **Highlights:** AI-driven lesson & quiz generation, Nibble AI chat, progress tracking in Firestore, mobile-first low-friction UX.

**How & Why (process documentation)**  
The app uses an LLM as a content generator while ensuring the user receives concise, verifiable guidance. Each lesson is regeneratable to encourage repeat learning and adaptivity.

- **Architecture:** Expo React Native frontend ↔ Cloud function proxy → LLM provider (via secured backend) ↔ Firestore for progress.  
- **Why choices:** Offloading LLM calls to a Cloud Function proxy prevents exposing API secrets in the client and allows sanitisation & short-term caching. Expo chosen for mobile UX velocity.  
- **Development process:** prototype chat flows → safety & moderation rules in cloud proxy → iterative refinement based on usability tests. Focused on short lessons (bite-sized) and quick quiz flows to reinforce learning.  
- **Challenges & learnings:** ensuring LLM-generated content is accurate and actionable; implemented heuristics + fallback curated content. Learned to design regeneration UX that signals to the user that content may vary.  
- **How to run (summary):**
  - `git clone https://github.com/AnemiB/Nerdy-Nibbles`
  - `yarn` or `npm install`
  - Configure Cloud Function proxy (do **not** put secrets in the client `.env`; use function settings)
  - `expo start`
- **Future improvements:** verification layer for LLM responses; personalized learning paths and spaced repetition features.

---

## 📊 GitHub profile & repo stats
These visual cards help examiners quickly scan activity and repo stats — add them to your profile README and ensure your GitHub username is correct in the URLs below.

- GitHub stats (replace `AnemiB` with your username if different):  
  `![Anemi's GitHub stats](https://github-readme-stats.vercel.app/api?username=AnemiB&show_icons=true&count_private=false&theme=default)`

- Top languages:  
  `![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=AnemiB&layout=compact)`

> Tip: make sure your repositories are public and the `main` (or `master`) branch is up-to-date before your presentation so examiners can inspect commits and README process documentation.

---

## ✅ Submission checklist (DV300 brief compliance)
- [ ] Header & profile image present (this README header).  
- [ ] Short biography with career focus and relevant soft skills.  
- [ ] Tech stack badges and clear list of skills.  
- [ ] **3 main portfolio projects** documented (Aureum Elegance, SipStop, Nerdy Nibbles).  
- [ ] Each project README includes: Overview, Problem statement, Role, Tech stack, How & Why (process), Run instructions, Future improvements.  
- [ ] Repositories are set to **Public** and default branch is **main** with latest commits.  
- [ ] Contact info is accurate and visible.

---

## 📬 Contact & Links
- Email: `<your.email@domain.com>` — replace with your preferred contact email.  
- LinkedIn: `https://www.linkedin.com/in/<your-linkedin-handle>` — replace with your LinkedIn URL.  
- Portfolio / Live demo: `https://<your-portfolio-or-demo>` (optional)  
- CV: `https://<link-to-cv>` (optional)

---

## 🔒 Notes on secrets & presentation
- **Do not** store API keys or production secrets in client `.env` files — use Cloud Functions or server-side proxies (this README documents that pattern for Nerdy Nibbles).  
- Before your presentation: set repositories public and ensure each repo has a focused `README.md` with the process documentation sections shown above.

---

If you’d like, I can:
- generate **three full README.md files** (one per repo) using the process sections above (ready-to-copy),
- or produce a compact single-page PDF export of this profile for your slides.

Tell me which you want next and I’ll drop the full file content for each repo. (If you want the direct repo README files, I’ll include `How to run`, `Architecture diagram` text (ASCII or md), and `example .env` instructions with placeholders.)
