# Task 2 · Ayesha Fatima — Personal Portfolio

A personal portfolio / digital résumé for **Ayesha Fatima**, an undergraduate Software Engineer at NED University of Engineering & Technology, frontend-focused. Built as a single static HTML/CSS file with light vanilla JavaScript for scroll-reveal polish.

## File

- `portfolio.html` — the entire site (HTML + embedded CSS + a small inline `<script>` block)

## Concept

A "developer terminal" motif runs through the page — the hero includes a fake terminal window (`whoami`, `cat focus.txt`) as a nod to the subject being a software engineer, kept restrained so it doesn't overwhelm the rest of the clean, minimal layout.

## Section order (as requested)

1. **Hero / Intro** — name, role, a slightly longer intro paragraph (folds in "About Me" content), two CTAs, terminal-style visual, and a stat bar (projects shipped, internships, languages/frameworks, AI/ML projects)
2. **Skills** — grouped into 4 categories: Frontend, Backend & Databases, Languages, AI/ML & Tools
3. **Projects** — 6 project cards, each with a color-coded initial badge, description, tech tags, and a GitHub link
4. **Experience** — Research Intern and QA Intern roles at NED UET, in a timeline-style list
5. **Contact** — real email, GitHub, and LinkedIn, each clickable

## Content used

**Skills**, derived from the projects described:

| Category | Skills |
|---|---|
| Frontend | HTML5, CSS3, JavaScript, Responsive UI |
| Backend & Databases | Java, Maven, Oracle SQL, REST APIs |
| Languages | C++, Python, Java, JavaScript |
| AI/ML & Tools | Machine Learning, OpenCV, Raylib, Git & GitHub |

**Projects:**

| Project | Description | Tags |
|---|---|---|
| FindNED | Full-stack lost & found management system for NED University | Full-Stack, Web App, Database |
| CheckIn Mate | Hostel reservation system for NED's foreign students | Java, Oracle, Maven, JavaScript |
| Kisaan Dost | Bilingual agricultural forecasting app for Pakistani farmers with an AI chatbot | AI Chatbot, Bilingual UI, AgriTech |
| BeatSafe | Heart attack prediction system using Python & ML | Python, Machine Learning, Healthcare |
| Hand Gesture Control | Voice/brightness control via hand gestures using OpenCV | Python, OpenCV, Computer Vision |
| Bicycle Game | 2D bicycle game built in C++ with Raylib | C++, Raylib, Game Dev |

**Experience:** Research Intern and QA Intern, both at NED University of Engineering & Technology (application testing and documentation).

**Contact:** `ayeshafatima5466@gmail.com` · GitHub `ayeshafatima06` · LinkedIn `ayesha-fatima-2b97962b7`

## Design system

- **Palette:** warm paper background (`#FAF9F6`), ink (`#1C1E22`), single slate-blue accent (`#2F4B7C`) — kept consistent per the client's request to preserve the original color theme
- **Typography:** Space Grotesk (headings), Inter (body), JetBrains Mono (code-flavored labels, terminal text, tags)
- **Enhancement:** sections fade/slide in on scroll via `IntersectionObserver` (respects `prefers-reduced-motion`)

## Responsiveness

- `900px` — skills/project grids collapse to 2 → 1 columns, experience items stack
- `640px` — nav collapses into a toggle menu, all grids go single-column

## How to run

Open `portfolio.html` directly in a browser, or use VS Code's **Live Server** extension for auto-reload.

## Notes / things to fill in yourself

- Individual project GitHub links currently point to `#` placeholders — swap in your real repo URLs when ready
- No specific dates are shown for the two internships since none were provided — add them under "Internship" in the Experience section if you'd like

## Checklist coverage

- [x] Hero with name, role, avatar (terminal-style visual)
- [x] About content folded into a prominent intro paragraph
- [x] Skills shown as a categorized tag grid
- [x] 6 project cards with title, description, and GitHub link placeholder
- [x] Contact section with real email, GitHub, LinkedIn icons/links
- [x] Smooth scroll navigation (`scroll-behavior: smooth` + anchor nav)
- [x] Consistent color scheme and font family throughout
- [x] Fully responsive down to mobile