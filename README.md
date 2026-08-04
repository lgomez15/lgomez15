<!-- ═══════════════════════════════════════════════════════════════════════════
                    LUIS ROBERTO GÓMEZ VEIGA · README
        terminal-native profile · built to ship, not to decorate
═══════════════════════════════════════════════════════════════════════════ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,8,12,20,24&height=200&section=header&text=luis@m2g:~$&fontSize=52&fontColor=e6fff0&animation=fadeIn&fontAlignY=36&desc=Full-Stack%20Engineer%20·%20Software%20Architect%20·%20CS%20%2B%20Business%20@%20USAL&descAlignY=58&descSize=15&stroke=2ea043&strokeWidth=1"/>

<!-- Live "typing" terminal — the closest a GitHub README gets to interactive -->
<a href="https://github.com/lgomez15">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=900&color=2EA043&center=true&vCenter=true&width=720&height=52&lines=%24+whoami+%E2%86%92+Luis+Roberto%2C+builder+of+systems+that+ship;%24+cat+m2g%2FREADME+%E2%86%92+fintech+moving+real+money%2C+in+prod;%24+ls+~%2Ftfg+%E2%86%92+2+theses%3A+voice-AI+SaaS+%2B+market+volatility;%24+sudo+make+it+scale+%E2%80%94+then+make+it+boring" alt="typing"/>
</a>

<br/>

[![mail](https://img.shields.io/badge/luis@m2g.dev-0d1117?style=for-the-badge&logo=maildotru&logoColor=2ea043&labelColor=0d1117)](mailto:luis@m2g.dev)
[![github](https://img.shields.io/badge/@lgomez15-0d1117?style=for-the-badge&logo=github&logoColor=2ea043&labelColor=0d1117)](https://github.com/lgomez15)
[![loc](https://img.shields.io/badge/Panam%C3%A1%20City-0d1117?style=for-the-badge&logo=googlemaps&logoColor=2ea043&labelColor=0d1117)](https://maps.google.com/?q=Panama+City)
[![cv](https://img.shields.io/badge/./cv.pdf-0d1117?style=for-the-badge&logo=readthedocs&logoColor=2ea043&labelColor=0d1117)](https://drive.google.com/uc?export=download&id=1CzzagODDGoxA4lorwUVpOsPBORfLpfj2)

</div>

```console
╭─────────────────────────────╮
│  ● ● ●          zsh · 80×24 │   host     Panamá City · remote-first
├─────────────────────────────┤   edu      USAL · CS + Business (dual BSc)
│                             │   role     full-stack engineer · architect
│  $ whoami                   │   stack    FastAPI · React · k8s · Postgres
│  ▸ luis roberto gómez veiga │   shipping M2G — fintech, in production
│  ▸ i build money that       │   theses   voice-AI SaaS · market volatility
│    reconciles.              │   since    2000 · powered by caffeine-507
│                             │   status   ● online — open to hard problems
│  $ ▏                        │
╰─────────────────────────────╯
```

---

## `luis@m2g:~$ whoami`

I build backends that hold up when real money and real users hit them — and I like the part where the architecture gets *simpler* as it scales, not scarier.

Right now I'm shipping **M2G** (below), a fintech platform that's live in production; doing microservices work at **Osprean Technologies**; research-grade full-stack at **BISITE (USAL)**; and closing a **dual degree in Computer Science + Business** with two theses in parallel. I care about clean boundaries, real-time systems, and software that stays boring under load.

<div align="center">

`FastAPI` · `TypeScript` · `React` · `Kubernetes` · `PostgreSQL` · `GitOps` · `Docker` · `WebSockets`

</div>

---

## `luis@m2g:~$ cat m2g/README.md` &nbsp;`# the flagship`

> **M2G — fintech, in production, moving real money.**
> A multi-tenant platform whose first product, **Pago Venezuela**, moves remittances **Mexico → Venezuela**: a payer funds a transfer in MXN (SPEI / OXXO), and the beneficiary receives VES (Pago Móvil / bank transfer) — reconciled end-to-end against payment providers. Not a demo. Real payers, real payouts, real reconciliation, shipped continuously.

<p>
<img src="https://img.shields.io/badge/status-in%20production-2ea043?style=flat-square&labelColor=0d1117"/>
<img src="https://img.shields.io/badge/architecture-multi--tenant%20RLS-2ea043?style=flat-square&labelColor=0d1117"/>
<img src="https://img.shields.io/badge/delivery-GitOps%20·%20ArgoCD-2ea043?style=flat-square&labelColor=0d1117"/>
<img src="https://img.shields.io/badge/money-idempotent%20·%20reconciled-2ea043?style=flat-square&labelColor=0d1117"/>
</p>

```mermaid
graph LR
    Payer["Payer · MX"] -->|SPEI · OXXO| Portal["Client Portal<br/>React · white-label"]
    Portal --> API["Core API<br/>FastAPI · multi-tenant RLS"]
    API --> Ledger["PostgreSQL<br/>row-level security"]
    API -->|collect MXN| PSP["Payment providers"]
    API -->|payout VES| Off["Off-ramp<br/>Pago Móvil · transfer"]
    Off --> Beneficiary["Beneficiary · VE"]
    Ops["Operator"] --> Panel["Ops Panel<br/>envíos · reconciliation"]
    Panel --> API
    API -. GitOps .-> Argo["ArgoCD → k8s"]
```

<table>
<tr><td><b>Domain</b></td><td>Cross-border payments · remittances · reconciliation</td></tr>
<tr><td><b>Backend</b></td><td>FastAPI · SQLAlchemy · multi-tenant with Postgres <b>RLS</b> · Celery</td></tr>
<tr><td><b>Frontend</b></td><td>React 18 · Vite · white-label per merchant</td></tr>
<tr><td><b>Infra</b></td><td>Kubernetes · ArgoCD <b>GitOps</b> · GHCR · tag-driven releases</td></tr>
<tr><td><b>The hard parts</b></td><td>idempotent money flows · provider failover · resilient UX when an upstream runs dry — never charge twice, never lose a payout</td></tr>
</table>

---

## `luis@m2g:~$ ls -la ~/thesis` &nbsp;`# two degrees, two theses`

<table>
<tr>
<td width="50%" valign="top">

### `tfg-cs/`
**Multi-tenant Voice-Assistant SaaS**

Any business gets an **AI booking assistant** — over **Telegram · WhatsApp · phone (VoIP)** — with zero code. Each tenant is fully isolated: own DB, own backend, own assistant. **GPT-4o** parses intent and calls tools to create, move, or cancel reservations in real time; a Core API spins up per-tenant stacks via the Docker SDK.

`FastAPI` · `NestJS` · `K8s` · `WebSockets` · `GPT-4o`

</td>
<td width="50%" valign="top">

### `tfg-ade/`
**Uncertainty Indicators & Market Volatility**

*The Business-degree thesis.* A quantitative study of how economic-policy uncertainty (**EPU / CNEPU**) relates to asset volatility in US & Chinese markets — unified monthly panels **2014–2025** (139 obs), taken end-to-end from ingestion & EDA through correlation, uncertainty-regime, **Granger-causality** and **GARCH(1,1)-t** analysis over equities, gold and Bitcoin.

`Python` · `GARCH` · `pandas` · `statsmodels` · `arch`

</td>
</tr>
</table>

<details>
<summary><b><code>tfg-cs/</code> — expand system architecture</b></summary>
<br/>

```mermaid
graph TB
    User["User"] -->|natural language| CH["Channel<br/>Telegram · WhatsApp · VoIP"]
    CH --> GW["Gateway<br/>channel adapter"]
    GW --> MCP["MCP Server<br/>GPT-4o + tool calling"]
    MCP --> TAPI["Tenant API<br/>isolated per client"]
    TAPI --> TDB["Tenant DB"]
    Admin["Admin"] --> FE["React SPA"]
    FE --> Core["Core API<br/>auth · tenants · RBAC"]
    Core -->|Docker SDK| TAPI
    Core --> CDB["Central DB"]
```

| Layer | Tech |
|-------|------|
| **AI / LLM** | OpenAI GPT-4o · dynamic tool calling |
| **Channels** | Telegram · WhatsApp · VoIP |
| **Backend** | FastAPI · SQLAlchemy · JWT + RBAC |
| **Frontend** | React 18 · Vite |
| **Infra** | Docker · Traefik · isolated network per tenant |

</details>

<details>
<summary><b><code>tfg-ade/</code> — expand key findings</b></summary>
<br/>

| Market | Key finding |
|--------|-------------|
| **US EPU → Gold** | strongest link: corr `0.510` — the only asset EPU *Granger-causes* (`F=7.45`, `p=0.007`) |
| **US EPU → S&P 500** | corr `0.453` · top-uncertainty months carry `2.08×` the vol of calm ones · relationship jumps `0.10 → 0.41` after 2020 |
| **US EPU → Bitcoin** | near-zero `-0.050` — crypto decoupled from policy uncertainty |
| **China CNEPU → CSI 300** | **negative** `-0.197` · high-CNEPU regimes show *less* vol (`0.76×`) — the inverse of the US pattern |

*Stack:* Python · Jupyter · pandas · statsmodels · `arch` (GARCH(1,1)-t) · matplotlib · seaborn — monthly panels 2014-01 → 2025-07, results serialized to `resultados.json`.

</details>

---

## `luis@m2g:~$ ./stack --list`

<table>
<tr><td valign="top" width="33%">

**`backend/`**

![FastAPI](https://img.shields.io/badge/FastAPI-05122A?style=flat-square&logo=fastapi&logoColor=009688)
![NestJS](https://img.shields.io/badge/NestJS-05122A?style=flat-square&logo=nestjs&logoColor=E0234E)
![Node](https://img.shields.io/badge/Node.js-05122A?style=flat-square&logo=nodedotjs&logoColor=43853D)
![Express](https://img.shields.io/badge/Express-05122A?style=flat-square&logo=express&logoColor=fff)
![Python](https://img.shields.io/badge/Python-05122A?style=flat-square&logo=python&logoColor=3776AB)
![PHP](https://img.shields.io/badge/PHP-05122A?style=flat-square&logo=php&logoColor=777BB4)

</td><td valign="top" width="33%">

**`frontend/`**

![React](https://img.shields.io/badge/React-05122A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-05122A?style=flat-square&logo=typescript&logoColor=3178C6)
![Vue](https://img.shields.io/badge/Vue-05122A?style=flat-square&logo=vuedotjs&logoColor=4FC08D)
![Vite](https://img.shields.io/badge/Vite-05122A?style=flat-square&logo=vite&logoColor=646CFF)
![Flutter](https://img.shields.io/badge/Flutter-05122A?style=flat-square&logo=flutter&logoColor=02569B)
![Tailwind](https://img.shields.io/badge/Tailwind-05122A?style=flat-square&logo=tailwindcss&logoColor=38BDF8)

</td><td valign="top" width="33%">

**`infra/ · data/`**

![Kubernetes](https://img.shields.io/badge/Kubernetes-05122A?style=flat-square&logo=kubernetes&logoColor=326CE5)
![Docker](https://img.shields.io/badge/Docker-05122A?style=flat-square&logo=docker&logoColor=2496ED)
![ArgoCD](https://img.shields.io/badge/ArgoCD-05122A?style=flat-square&logo=argo&logoColor=EF7B4D)
![AWS](https://img.shields.io/badge/AWS-05122A?style=flat-square&logo=amazonwebservices&logoColor=FF9900)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-05122A?style=flat-square&logo=postgresql&logoColor=4169E1)
![MongoDB](https://img.shields.io/badge/MongoDB-05122A?style=flat-square&logo=mongodb&logoColor=47A248)

</td></tr>
</table>

<details>
<summary><b>./stack --all &nbsp;<code># the long tail</code></b></summary>
<br/>

![GraphQL](https://img.shields.io/badge/GraphQL-05122A?style=flat-square&logo=graphql&logoColor=E10098)
![Prisma](https://img.shields.io/badge/Prisma-05122A?style=flat-square&logo=prisma&logoColor=fff)
![Redis](https://img.shields.io/badge/Redis-05122A?style=flat-square&logo=redis&logoColor=FF4438)
![Celery](https://img.shields.io/badge/Celery-05122A?style=flat-square&logo=celery&logoColor=37814A)
![MySQL](https://img.shields.io/badge/MySQL-05122A?style=flat-square&logo=mysql&logoColor=4479A1)
![Firebase](https://img.shields.io/badge/Firebase-05122A?style=flat-square&logo=firebase&logoColor=FFCA28)
![GitHub Actions](https://img.shields.io/badge/Actions-05122A?style=flat-square&logo=githubactions&logoColor=2088FF)
![Linux](https://img.shields.io/badge/Linux-05122A?style=flat-square&logo=linux&logoColor=FCC624)
![Java](https://img.shields.io/badge/Java-05122A?style=flat-square&logo=openjdk&logoColor=fff)
![C](https://img.shields.io/badge/C-05122A?style=flat-square&logo=c&logoColor=A8B9CC)
![C#](https://img.shields.io/badge/C%23-05122A?style=flat-square&logo=csharp&logoColor=fff)
![Dart](https://img.shields.io/badge/Dart-05122A?style=flat-square&logo=dart&logoColor=0175C2)
![R](https://img.shields.io/badge/R-05122A?style=flat-square&logo=r&logoColor=276DC3)

</details>

---

## `luis@m2g:~$ git log --oneline ~/experience`

```console
* 2024 → now   feat(work):   Software Engineer @ Osprean Technologies
|              real-time messaging · microservices · production systems
|
* 2024 → now   feat(m2g):    Founder-engineer @ M2G — fintech in production
|              multi-tenant payments · GitOps on k8s · money that reconciles
|
* 2024 → now   feat(thesis):  TFG (CS) — multi-tenant voice-assistant SaaS
|              full system from scratch: infra · backend · AI integration
|
* 2024 → now   feat(thesis):  TFG (ADE) — uncertainty indices vs. volatility
|              end-to-end quant pipeline · GARCH volatility modelling
|
* 2023 → now   feat(work):   Full-Stack Dev @ BISITE Research Group (USAL)
|              research-grade web apps bridging science and engineering
|
* 2023 → 2025  feat(teach):  Programming Instructor @ Academia Titania
|              PHP · SQL · networking · fundamentals to aspiring devs
|
* 2000        init: Luis Roberto Gómez Veiga
```

---

## `luis@m2g:~$ cat /proc/github/stats`

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=lgomez15&hide_border=true&background=0d1117&stroke=2ea043&ring=2ea043&fire=2ea043&currStreakLabel=2ea043&sideNums=c9d1d9&currStreakNum=c9d1d9&dates=8b949e&sideLabels=c9d1d9"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=lgomez15&bg_color=0d1117&color=2ea043&line=2ea043&point=e6fff0&area=true&hide_border=true"/>

</div>

---

## `luis@m2g:~$ ping -c 1 luis`

<div align="center">

```console
PING luis (luis@m2g.dev): reply in 64ms — always up for a good problem.
```

[![mail](https://img.shields.io/badge/luis@m2g.dev-2ea043?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:luis@m2g.dev)
[![github](https://img.shields.io/badge/@lgomez15-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/lgomez15)
[![phone](https://img.shields.io/badge/+34%20663%20723%20999-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](tel:+34663723999)
[![cv](https://img.shields.io/badge/Download%20CV-EA4335?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://drive.google.com/uc?export=download&id=1CzzagODDGoxA4lorwUVpOsPBORfLpfj2)

*Open to interesting projects, collaborations, and any conversation about systems, architecture, or the art of making things boring at scale.*

</div>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,8,12,20,24&height=110&section=footer&text=make%20it%20scale%20—%20then%20make%20it%20boring&fontSize=15&fontColor=e6fff0&fontAlignY=72&descAlignY=52"/>
</div>
