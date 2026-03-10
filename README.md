<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&colors=0d1117,238636,2ea043&height=180&section=header&text=Luis%20Roberto%20G%C3%B3mez%20Veiga&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=32&desc=Full-Stack%20Engineer%20%E2%80%A2%20Software%20Architect%20%E2%80%A2%20CS%20%2B%20Business%20%40%20USAL&descAlignY=55&descSize=16"/>

<br/>

[![Email](https://img.shields.io/badge/gomez@usal.es-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:gomez@usal.es)
[![GitHub](https://img.shields.io/badge/lgomez15-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/lgomez15)
[![Location](https://img.shields.io/badge/Salamanca,%20Spain-4285F4?style=flat-square&logo=googlemaps&logoColor=white)](https://goo.gl/maps/salamanca)
[![CV](https://img.shields.io/badge/Download%20CV-00C49A?style=flat-square&logo=adobeacrobatreader&logoColor=white)](https://drive.google.com/uc?export=download&id=1CzzagODDGoxA4lorwUVpOsPBORfLpfj2)

<br/>

```

╔═══════════════════════════════════════════════════════════════╗
║  Building scalable systems, real-time architectures, and      ║
║  products that actually ship — from Panama to production.     ║
╚═══════════════════════════════════════════════════════════════╝

```

</div>

---

## `$ whoami`

Hey — I'm Luis Roberto. I'm a **Full-Stack Developer** finishing a **Dual Bachelor's in Computer Science + Business Administration** at the University of Salamanca (May 2026).

I spend my time building microservices at **Osprean Technologies**, doing research-grade full-stack work at **BISITE**, and architecting a multi-tenant SaaS voice assistant platform for my thesis.

I care about clean architecture, real-time systems, and software that doesn't fall apart at scale.

---

## `$ ls -la ./now`

> What I'm actively building right now:

| Status | Project | Stack |
|--------|---------|-------|
| 🟢 **Active** | Multi-tenant SaaS for intelligent voice assistants *(thesis)* | FastAPI · NestJS · K8s · WebSockets |
| 🟢 **Active** | Real-time messaging & microservices @ **Osprean Technologies** | Node.js · Docker · MongoDB · AWS |
| 🟢 **Active** | Full-stack web applications @ **BISITE Research Group** | React · FastAPI · PostgreSQL |

---

## `$ cat thesis/architecture.md`

> **Multi-tenant SaaS — Intelligent Booking Assistant**  
> A platform that lets any business offer an AI-powered booking assistant to their customers — accessible via **Telegram, WhatsApp, or phone call (VoIP)** — without writing a single line of code. Each business (tenant) gets a fully isolated environment: its own database, its own backend, and its own AI assistant configured to its services and schedule. Under the hood, **GPT-4o** understands natural language, resolves intent, and calls the right tools to create, modify, or cancel reservations in real time.

```mermaid
graph TB
    User["👤 User"] -->|natural language| CH["📲 Channel\nTelegram · WhatsApp · VoIP"]
    CH --> GW["📡 Gateway\n(channel adapter)"]
    GW --> MCP["🧠 MCP Server\n(GPT-4o + tool calling)"]
    MCP --> TenantAPI["🏢 Tenant API\n(isolated per client)"]
    TenantAPI --> TenantDB["🗄️ Tenant DB"]
    MCP --> GPT["☁️ OpenAI GPT-4o"]

    Admin["👨‍💼 Admin"] --> Frontend["🖥️ React SPA"]
    Frontend --> Core["⚙️ Core API\n(auth · tenants · RBAC)"]
    Core -->|Docker SDK| TenantAPI
    Core --> CoreDB["🗄️ Central DB"]
```

| Layer | Tech |
|-------|------|
| **AI / LLM** | OpenAI GPT-4o · dynamic tool calling |
| **Channels** | Telegram · WhatsApp · VoIP |
| **Backend** | FastAPI · SQLAlchemy · JWT + RBAC |
| **Frontend** | React 18 · Vite |
| **Infra** | Docker · Traefik · isolated network per tenant |

---

## `$ cat tech_stack.json`

<details open>
<summary><b>Frontend</b></summary>
<br/>

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

</details>

<details open>
<summary><b>Backend</b></summary>
<br/>

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)

</details>

<details open>
<summary><b>Databases & Data</b></summary>
<br/>

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=firebase&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=prisma&logoColor=white)

</details>

<details open>
<summary><b>DevOps & Cloud</b></summary>
<br/>

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</details>

<details>
<summary><b>Other Languages</b></summary>
<br/>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)

</details>

---

## `$ cat thesis2/uncertainty.md`

> **Uncertainty Indicators & Financial Market Volatility**  
> A quantitative research project analyzing how economic and geopolitical uncertainty indices (EPU, CNEPU) relate to asset volatility across the US and Chinese markets. Built end-to-end: from raw data ingestion and cleaning, through EDA, to GARCH-X predictive modeling — covering daily and monthly horizons across equities, gold, and crypto.

| Market | Key Finding |
|--------|-------------|
| **US EPU → S&P 500** | Correlation with 30d volatility: `0.625` — high-uncertainty regimes drive `1.93x` more vol |
| **US EPU → Gold** | Moderate correlation `0.545`, lag effect peaks at 2 days |
| **US EPU → Bitcoin** | Near-zero relationship `0.025` — crypto decoupled from policy uncertainty |
| **China CNEPU → CSI 300** | Negative correlation `-0.321`; strongest predictive lag at **12 months** |

| Layer | Tech |
|-------|------|
| **Languages** | Python · Jupyter |
| **Modeling** | GARCH-X · time-series regression |
| **Data** | EPU Index · CNEPU · S&P 500 · CSI 300 · Gold · Bitcoin |
| **Pipeline** | pandas · statsmodels · matplotlib · seaborn |

---

## `$ git log --oneline ./experience`

```

2024 → now   feat: Software Engineer @ Osprean Technologies
└─ Real-time messaging, microservices architecture, production systems

2024 → now   feat: TFG — Multi-tenant Voice Assistant SaaS
└─ Designing the full system from scratch: infra, backend, and AI integration

2024 → now   feat: TFG — Uncertainty Indicators & Market Volatility
└─ Quantitative analysis of EPU indices vs asset volatility (GARCH-X modeling)

2023 → now   feat: Full-Stack Developer @ BISITE Research Group (USAL)
└─ Research-grade web applications bridging science and engineering

2023 → 2025   past: Programming Instructor @ Academia Titania
└─ Taught PHP, SQL, networking, and fundamentals to aspiring devs

```

---

## `$ cat ./stats`

<div align="center">
<img src="https://github-readme-streak-stats.herokuapp.com/?user=lgomez15&theme=tokyonight&hide_border=true&background=0D1117&ring=00FFB2&fire=FF4D6D&currStreakLabel=00FFB2" />
</div>

---

## `$ ping -c 1 luis`

<div align="center">

| | |
|---|---|
| 📧 **Email** | [gomez@usal.es](mailto:gomez@usal.es) |
| 📱 **Phone** | +34 663 723 999 |
| 📄 **CV** | [Download here](https://drive.google.com/uc?export=download&id=1CzzagODDGoxA4lorwUVpOsPBORfLpfj2) |
| 💻 **GitHub** | [@lgomez15](https://github.com/lgomez15) |

*Always open to interesting projects, collaborations, and conversations about systems, architecture, or DevOps.*

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&colors=0d1117,238636,2ea043&height=100&section=footer"/>

</div>
