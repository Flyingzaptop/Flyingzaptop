# Hi, I'm Denis 👋

Engineering student at Wrocław University of Science and Technology, IT administrator, and co-founder & CTO of [Antillia Tech](https://antillia.tech). I build automation tools, web backends and applied AI. I work with AI coding assistants every day: I design the solution, split the problem, review and test the result.

**At Antillia we pre-train our own Polish language model from scratch** — Polish data, our own tokenizer, our own weights. Most "Polish" models are foreign models fine-tuned on Polish text; ours is not. → [lexpl overview](https://github.com/Flyingzaptop/LLM_notNDA)

---

## Projects

### 🧠 lexpl — Polish legal language model · [overview](https://github.com/Flyingzaptop/LLM_notNDA)
A language model for Polish law and tax, trained from scratch on one consumer GPU (code private).
- Built the whole pipeline: data collection from official sources → cleaning, deduplication, anonymisation → own tokenizer → pre-training → fine-tuning → search with verified citations → API gateway.
- 12.6 M documents / 25 B tokens; the 150 M pilot scores 71 % on official legal entrance exams (pass mark 66.7 %).
- Engineering: Python 3.12, strict typing, unit / integration / property-based tests, CI, resumable training, Rust for data processing, rate-limited streaming API behind a Cloudflare Tunnel.

### 🧪 [LabFlow](https://github.com/Flyingzaptop/LabFlow) — laboratory sample-flow system
Web system that coordinates laboratory procedures and samples across roles.
- **Backend:** Django REST Framework, PostgreSQL (SQLite in development), OpenAPI schema.
- **Security:** role-based access checked on the server, CSRF-protected sessions, throttling, an immutable audit log guarded at the database level.
- **Frontend:** React + TypeScript (Vite, Vitest).
- **Deployment:** Linux with systemd, Gunicorn and Caddy (reverse proxy + HTTPS), backup and upgrade scripts.
- ~130 backend tests; optional local AI assistant (Ollama) and transcription (Whisper).

### ⚙️ [jobhunter-n8n](https://github.com/Flyingzaptop/jobhunter-n8n) — automation pipeline
Local-first pipeline that collects job offers, removes duplicates and scores fit with a local LLM.
- Six n8n workflows calling Node.js services; PostgreSQL as the single source of truth (22 SQL migrations, constraints for deduplication and statuses).
- Docker Compose (PostgreSQL, core service, browser service, n8n) with health checks.
- LLM answers as structured JSON validated against a schema; the final score is computed in code.
- GitHub Actions CI runs the tests against a real PostgreSQL service.

### 🤖 [antillia-ml-portfolio](https://github.com/Flyingzaptop/antillia-ml-portfolio) — seven local ML/AI apps
Each project: own data split, trained model, FastAPI or Django API, React/TypeScript UI (PL/EN), tests and an honest model report.

| Project | Task |
|---|---|
| AI Desk | RAG assistant: answers only from company documents, with citations and role-based document access (Django REST, embeddings, Ollama, streaming) |
| DemandCast | 24-hour demand forecast from 168 hours of history |
| IntentRoute | Routing customer messages by intent (multilingual text encoder) |
| ReviewPulse | Classifying customer reviews |
| TerraVision | Land-use classification from Sentinel-2 satellite images |
| MachineSentinel | Predicting machine failures from sensor data |
| BasketWise | Product recommendations from purchase history |

### 🌐 [antillia.tech](https://antillia.tech) — company website and infrastructure
Static site on a Cloudflare Worker with automatic deploys from Git; the worker serves video with HTTP range requests (206) for iOS. A live chat connects through a Cloudflare Tunnel to a GPU machine at home — no open ports.

### Research and fundamentals
- [gc-mbo-research](https://github.com/Flyingzaptop/gc-mbo-research) — event-level market data research: Rust order-book replay, Python features, walk-forward evaluation, causality tests, and an honest negative result.
- [crypto-trend](https://github.com/Flyingzaptop/crypto-trend) — small, tested pandas backtest on public exchange data, with protection against look-ahead.
- [ARC](https://github.com/Flyingzaptop/ARC) — experimental D3D12 graphics runtime in C++ (CMake, CI): observing GPU work and testing reversible optimisations.
- [Project1_Informatyka_III](https://github.com/Flyingzaptop/Project1_Informatyka_III) — C++ OOP coursework: classes, operator overloading, dynamic memory (rule of three).

---

## Skills

| Area | Tools |
|---|---|
| Languages | Python · JavaScript / TypeScript · SQL · C++ · basics of Rust |
| Backend & APIs | Django REST Framework · FastAPI · Starlette · REST · streaming (SSE) |
| Data | PostgreSQL · SQLite · pandas · NumPy · Parquet |
| AI / ML | PyTorch · scikit-learn · training transformers from scratch · RAG · embeddings · Ollama · LLM APIs |
| Automation | n8n · Playwright · scripting (Python, PowerShell) |
| DevOps & infra | Docker / Compose · Git · GitHub Actions · Linux (systemd) · Caddy · Cloudflare Workers & Tunnel |
| Frontend | React · TypeScript · Vite · HTML / CSS |
| IT administration | preparing workstations, user support, office infrastructure |

## Education

- Wrocław University of Science and Technology — engineering studies
- IT STEP Academy — *Artificial Intelligence + Python* (9 months): Python, OOP, databases, data analysis, machine learning, neural networks, NLP
- IT STEP Junior Computer Academy (3 years): Python, JavaScript, HTML/CSS, Arduino, game development

## Contact

[LinkedIn](https://www.linkedin.com/in/antilliatechcto/) · [antillia.tech](https://antillia.tech)
