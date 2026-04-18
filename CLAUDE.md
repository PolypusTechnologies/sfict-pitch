# SAGE — SF-ICT AI Guidance Engine
# Claude Code Memory File | Victor Citroen | Polypus Intelligence

## Project Overview
Building SAGE (SF-ICT AI Guidance Engine) for SF-ICT — a Dutch MSP in Noord-Brabant, Den Dungen.
Owner wants Victor as Head of AI (12-month employee contract) to build an internal AI department.
Monday April 20 meeting to close the contract.

## What SAGE Is
6-layer AI system built on SF-ICT's 20 years of operational data:
- Layer 1: Ticket Intelligence Engine — NLP classifies Dutch tickets, semantic search against 500k history
- Layer 2: Vague Resolution Decoder — decodes "opnieuw opgestart" into structured root cause
- Layer 3: Fleet Monitor — 1,024 endpoints via RMM API, real-time telemetry
- Layer 4: Predictive Failure Engine — ML model predicts hardware failures 48-72h in advance
- Layer 5: Update Intelligence — daily 06:00 scan of Windows Update, M365, FortiGate, NCSC-NL
- Layer 6: Client Predictor — behavioural AI predicts upcoming client requests

## Tech Stack
- Frontend: HTML/CSS/JS, ApexCharts, Tailwind, Lucide Icons, GSAP, Notyf, Marked
- Backend: FastAPI + uvicorn, PostgreSQL, Redis, WebSockets
- AI: Anthropic Claude (Azure OpenAI private), LangChain, LlamaIndex, ChromaDB, FAISS
- NLP: spaCy nl_core_news_sm (Dutch), sentence-transformers
- ML: scikit-learn, XGBoost, PyTorch
- Scraping: httpx, aiohttp, BeautifulSoup4, playwright
- Infra: Vercel (frontend), Azure Netherlands (backend, GDPR compliant)

## File Structure
```
~/sfict-pitch/
├── index.html          # Main pitch deck (live: sfict-pitch.vercel.app)
├── sage-demo.html      # Live SAGE demo dashboard (sfict-pitch.vercel.app/sage-demo.html)
├── CLAUDE.md           # This file
└── assets/             # Images and fonts
```

## Live URLs
- Pitch deck: sfict-pitch.vercel.app
- Demo dashboard: sfict-pitch.vercel.app/sage-demo.html
- GitHub: github.com/PolypusTechnologies/sfict-pitch

## SF-ICT Brand Colors
- Dark: #232430
- Light bg: #EAF2FB
- Blue: #1BA2D2
- Dark blue: #0477AE
- Pink: #E4067D
- Purple: #766A86
- Border: #c8dff0

## Key Business Numbers
- FCR before SAGE: 61% → after SAGE: 83% (+22pp)
- Avg resolution time: 47 min → 11 min
- Build cost: €28,400 (one-time, 12-month contract)
- Monthly running: €2,850/mo (100 clients)
- Monthly time saved: €18,500/mo @ €75/hr
- Net benefit: €15,675/mo
- Payback period: 1.8 months
- Year 1 net benefit: €159,700

## Contract Options
- ZZP: €85-110/hr
- 12-month employee (RECOMMENDED): €4,200-5,500 gross/mo + performance bonus
- Hybrid 3+2: €2,800-3,500/mo

## The One-Sentence Pitch
"Every ticket your engineers have ever solved is trapped knowledge. SAGE makes it available in seconds — to every engineer, on every new ticket, forever."

## MSP Terminology
- RMM: Remote Monitoring and Management (NinjaOne/Datto) — hands of the system
- PSA: Professional Services Automation (Autotask/HaloPSA) — ticketing + billing
- FCR: First Call Resolution — % tickets resolved without callback
- SLA: Service Level Agreement — P1=1hr response, P2=4hr, P3=next day
- MRR: Monthly Recurring Revenue — the lifeblood
- Ontzorgen: Dutch for "unburden" — the core MSP promise
- Entra ID: Microsoft cloud identity (formerly Azure AD)
- NCSC-NL: Dutch national cybersecurity centre

## Known Issues / Pending
- Resolution time bar chart (before vs after SAGE) — bars still overlapping on live Vercel
  Fix: the chart needs `grouped:true` and simplified plotOptions in ApexCharts
- Chart fix is in local sage_demo.html but needs re-push to Vercel

## Workflow Rules (Boris Cherny Method)
1. PLAN MODE: For any non-trivial change (3+ steps), write a plan first. Ask before implementing.
2. VERIFY BEFORE DONE: Never mark complete without proving it works. Run, check, demonstrate.
3. DEMAND ELEGANCE: Before any non-trivial change, ask "is there a more elegant way?"
4. AUTONOMOUS BUG FIXING: When given a bug, just fix it. Read logs, find root cause, resolve.
5. MINIMAL IMPACT: Only touch what's necessary. No side effects with new bugs.
6. TASK TRACKING: Write plan → verify → track progress → document results → capture lessons

## Do NOT
- Use dark backgrounds for this project (SF-ICT uses light theme #EAF2FB)
- Use purple/dark color schemes — SF-ICT colors are blue-grey professional
- Break Dutch MSP terminology — always use correct terms (Entra ID not Azure AD)
- Hardcode API keys — always use environment variables / .env
- Push broken code to Vercel — verify locally first
- Change the pitch deck structure without asking — slides are presentation-ready
