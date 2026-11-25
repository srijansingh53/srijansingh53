<div align="center">

# 👋 Hey, I'm Srijan

**Ruby on Rails Developer · Backend & Distributed Systems · Agentic AI Builder**

Rails engineer by trade. I build backend systems that hold up under real traffic, and AI tools that are actually useful.

[![Portfolio](https://img.shields.io/badge/-Portfolio-0F172A?style=for-the-badge&logo=gatsby&logoColor=white)](https://srijansingh53.github.io/)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/srijan-singh-67538214a)
[![Email](https://img.shields.io/badge/-Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:srijansingh53@gmail.com)
[![X](https://img.shields.io/badge/-X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/SrijanS23563236)

**Jump to:** [🧭 At a glance](#-at-a-glance) · [🔭 Right now](#-what-im-doing-right-now) · [⭐ ATS Engine](#-ats-engine) · [🛠️ Projects](#️-projects) · [🧰 Stack](#-stack) · [📊 Stats](#-github-stats)

</div>

---

## 🧭 At a glance

| | |
|---|---|
| 💎 **What I do** | Ruby on Rails developer with 5+ years of production experience: Rails, PostgreSQL, Sidekiq, Kafka and Redis. Distributed systems, query performance, and breaking Rails monoliths into services without breaking production. |
| 🤖 **Agentic AI** | Building with the Claude Agent SDK and MCP, writing custom skills, and wiring LLMs into real workflows where the output has to be right, not just plausible. |
| 🧪 **Exploring** | Go for high-throughput services, and newer AI tooling: agent orchestration, evals, and MCP servers. |
| 🎓 **Background** | B.Tech, IIIT Jabalpur (2017–2021). Got into ML in college through computer vision and NLP projects, two of which reached national hackathon finals. |
| 📍 **Based in** | Bengaluru, India |

---

## 🔭 What I'm doing right now

- 🚀 **Shipped [ATS Engine](https://ats-engine-r2i1.onrender.com/)**: a resume-vs-JD scorer that explains every point and tells you what to fix first.
- 🤖 **Building with agents**: Claude Agent SDK, MCP servers, Claude Code skills, and agentic workflows for debugging, security audits and alerting.
- 🐹 **Go**: building small, fast services alongside Rails, for the workloads where throughput matters most.
- 🧪 **AI engineering**: agent orchestration, evals that catch regressions, and turning prompts into deterministic, testable pipelines.

---

## ⭐ ATS Engine

**Find out whether a typical ATS would filter your resume out, and exactly what to change first.** Upload a resume, paste a software engineering job description (entry or senior level), and get a score out of 100. Every point is explained, and the fixes are ranked by how much each one would actually raise your score.

<div align="center">

[![Live App](https://img.shields.io/badge/Try%20it-Live%20App-22C55E?style=for-the-badge&logo=render&logoColor=white)](https://ats-engine-r2i1.onrender.com/)
[![Repo](https://img.shields.io/badge/Source-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/srijansingh53/ATS-Engine)

</div>

```mermaid
flowchart LR
    in["Resume + JD"]:::you --> l0["L0 Parse<br/>PDF / DOCX / TXT<br/>hidden-text check"]:::step
    l0 --> llm["Claude<br/>structured extraction<br/>+ rubric judging"]:::ai
    llm --> l1["L1 Required criteria<br/>knockouts"]:::step
    l1 --> l2["L2 Skill gate"]:::step
    l2 --> l3["L3 Fit<br/>8 weighted dimensions"]:::step
    l3 --> l4["L4 Integrity<br/>stuffing, copy-paste,<br/>timeline conflicts"]:::step
    l4 --> out["Score + band<br/>+ ranked fixes"]:::out

    classDef you fill:#132a1f,stroke:#4ade80,color:#dcfce7
    classDef step fill:#0f2a3d,stroke:#38bdf8,color:#e0f2fe
    classDef ai fill:#1e1b3a,stroke:#a78bfa,color:#ede9fe
    classDef out fill:#3a2a0f,stroke:#fbbf24,color:#fef3c7
```

- 🧮 **Claude extracts, Python scores.** The LLM turns text into structured JSON and quotes evidence; all arithmetic is deterministic, and calls are cached by input hash, so the same input always gets the same score.
- ✅ **Honest fixes.** Each fix's gain comes from rescoring with that gap closed, and it never suggests adding skills you don't have.
- 🔒 **Privacy first.** Resumes are processed in memory, never written to disk or logged. Name, gender, age, photo and address never feed the score.
- 🛡️ **Production-hardened.** Per-IP rate limits, input caps, magic-byte upload checks, CSP and HSTS, request IDs, and health checks.

**Stack:** Flask (Python 3.13) · React 18 (Vite) · Claude API · Docker · GitHub Actions → GHCR · Render / Fly.io

---

## 🛠️ Projects

### 🤖 AI & NLP

| Project | What it does | Stack |
|---|---|---|
| **[ATS Engine](https://github.com/srijansingh53/ATS-Engine)** | Resume-vs-JD ATS scorer with explainable points and gain-ranked fixes. | Flask · React · Claude API · Docker |
| **[atithi](https://github.com/srijansingh53/atithi)** | WhatsApp conversational assistant for tourism in India. **Smart India Hackathon 2020 finalist** ([writeup](https://medium.com/mindmeld/conversational-ai-at-smart-india-hackathon-2020-1793dfa0b574#SIH2020)). | MindMeld · Elasticsearch · Twilio · Azure |
| **[hatErase](https://github.com/srijansingh53/hatErase)** | Tracks hate speech on Twitter in real time with an NLP classifier and emails you when a tracked handle posts. | Django · NLTK · Twitter API · AWS |
| **[Spam Identifier](https://github.com/srijansingh53/Spam-Identifier-Website)** | Spam/ham message classifier served as a web app. | Multinomial NB · scikit-learn · Node.js |
| **[Twitter Sentiment Analysis](https://github.com/srijansingh53/Twitter-Sentiment-Analysis)** | Sentiment classification for an Analytics Vidhya challenge (top 50 on the leaderboard). | Python · NLP |

### 👁️ Computer vision

| Project | What it does | Stack |
|---|---|---|
| **[FORID](https://github.com/srijansingh53/FORID-Build-4-India)** | Field-orbiting robot that maps crop disease, with an Android app. Google Build for Digital India regionals. | Raspberry Pi · Keras · OpenCV · Flask |
| **[CXR Segmentation](https://github.com/srijansingh53/Semantic-Segemtation-of-CXR)** | Lung-field segmentation in chest X-rays with U-Net. | Keras · OpenCV |
| **[MammoHance](https://github.com/srijansingh53/MammoHance)** | Implementation of an adaptive mammographic image-enhancement paper, to make micro-calcifications easier to spot. | OpenCV · scikit-image |
| **[Neuralifer](https://github.com/srijansingh53/Neural-Style-Transfer)** | Neural style transfer for artistic image generation. | Keras · OpenCV |

### 🌐 Web & backend

| Project | What it does | Stack |
|---|---|---|
| **[traXee](https://github.com/srijansingh53/traxee)** | Tracks e-commerce price movements with async workers and alerts. | Django · Celery · Redis · AWS |
| **[Portfolio](https://github.com/srijansingh53/srijansingh53.github.io)** | My personal site. | Gatsby · React |

---

## 🧰 Stack

<div align="center">

![Ruby](https://img.shields.io/badge/Ruby-CC342D?style=flat-square&logo=ruby&logoColor=white)
![Rails](https://img.shields.io/badge/Rails-D30001?style=flat-square&logo=rubyonrails&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Sidekiq](https://img.shields.io/badge/Sidekiq-B1003E?style=flat-square&logo=sidekiq&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)

![Claude](https://img.shields.io/badge/Claude%20Agent%20SDK-D97757?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=anthropic&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI%20Codex-412991?style=flat-square&logo=openai&logoColor=white)

</div>

---

## 📊 GitHub Stats

<div align="center">
  <img height="170em" alt="Srijan's GitHub stats" src="https://github-readme-stats.vercel.app/api?username=srijansingh53&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true"/>
  <img height="170em" alt="Most used languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=srijansingh53&layout=compact&theme=tokyonight&hide_border=true&langs_count=8"/>
</div>

<div align="center">
  <img alt="Contribution streak" src="https://streak-stats.demolab.com?user=srijansingh53&theme=tokyonight&hide_border=true"/>
</div>

---

## 🤝 Say hi

Happy to talk Rails, backend systems, agentic AI, and side projects. Open an issue on a repo, or reach out on [LinkedIn](https://linkedin.com/in/srijan-singh-67538214a) or by [email](mailto:srijansingh53@gmail.com).

<div align="center">
<sub>💎 Rails | ⚙️ Backend | 🤖 Agentic AI | 🐹 Go</sub>
</div>
