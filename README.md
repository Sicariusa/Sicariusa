<a href="https://abdullahsayed.vercel.app">
  <img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d0221,50:ff00aa,100:00e5ff&height=260&section=header&text=ABDULLAH%20MOHAMED&fontSize=58&fontColor=ffffff&fontAlign=50&fontAlignY=42&desc=security%20tooling%20%C2%B7%20distributed%20systems%20%C2%B7%20test%20automation&descSize=17&descAlign=50&descAlignY=62&animation=fadeIn&stroke=ff00aa&strokeWidth=1" width="100%" alt="header"/>
</a>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=900&color=FF00AA&center=true&vCenter=true&width=780&lines=I+build+scanners+that+prove+exploits%2C+not+just+flag+them.;140K%2B+lines+of+TypeScript+in+one+security+engine.;Kafka+microservices+%C2%B7+WebSocket+gateways+%C2%B7+WebRTC.;QA+engineer+who+automates+the+QA." alt="typing"/>
</p>

<p align="center">
  <a href="https://abdullahsayed.vercel.app"><img src="https://img.shields.io/badge/PORTFOLIO-0d0221?style=for-the-badge&logo=vercel&logoColor=00e5ff&labelColor=0d0221" /></a>
  <a href="https://www.linkedin.com/in/abdullah-mohamed-56a853254/"><img src="https://img.shields.io/badge/LINKEDIN-0d0221?style=for-the-badge&logo=linkedin&logoColor=ff00aa&labelColor=0d0221" /></a>
  <img src="https://komarev.com/ghpvc/?username=Sicariusa&label=PROFILE+VIEWS&color=ff00aa&style=for-the-badge" />
</p>

<br/>

```ts
const abdullah = {
  role:        "Software Engineer — Security Tooling & Full-Stack",
  experience:  ["QA & Testing Engineer — production fintech app @ Geidea",
                "Frontend / UI lead — Statements Corp (live financial-services site)"],
  building:    "SecureVibe — a static-analysis engine that grades exploitability",
  shipped:     { commitsToSecureVibe: 531, since: "May 2026", packages: 10 },
  thinksIn:    ["ASTs", "taint flow", "event streams", "permission bitfields"],
  rule:        "emit a finding only when you can prove it",
};
```

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## ⚡ Flagship — SecureVibe

> **A security scanner that argues with itself.** Regex rules cast a wide net, Tree-sitter ASTs cross-examine every hit,
> a code graph traces whether an attacker can actually reach it — and only proven findings get to be *critical*.

<table>
<tr>
<td width="50%" valign="top">

| Signal | Number |
|:--|--:|
| Security rules (regex + AST) | **150+** |
| Vulnerability categories | **16** |
| Scan throughput | **1.6M LOC / 10,690 files in 121 s** |
| DVNA documented-vuln recall | **81.3 %** (13 / 16) |
| False positives on `zod` (48 KLOC) | **0** |
| Hard FPs on a real AI app | **12 → 0** |
| Engine validation tests | **297** |
| TypeScript in the monorepo | **~140K lines** |

</td>
<td width="50%" valign="top">

**What's inside**

- 🌳 **Tree-sitter + ts-morph** AST engine reconciling regex hits with structural evidence
- 🕸️ **Knowledge + attack-surface graph** — routes, calls, DB, taint sources → sinks
- 🎯 **Deterministic exploitability** — `confirmed / reachable / unknown / dead_code`, 0–100 confidence, **no LLM**
- 🧭 **Multi-source BFS** from public routes to prove reachability
- 🩹 **Fix-with-AI** — review-first, exact-match patch agent
- 🗡️ **Pentest agent** — tool-using LLM that proves findings against a live target
- 📊 Benchmarked head-to-head vs **Semgrep, CodeQL, Snyk, SonarQube** on the OpenSSF CVE Benchmark (200+ real CVEs) and RealVuln (66 repos)

</td>
</tr>
</table>

```mermaid
flowchart LR
    A[Repo / ZIP / URL] --> B[150+ regex rules]
    A --> C[Tree-sitter AST]
    B --> D{Reconcile}
    C --> D
    D --> E[Knowledge graph]
    E --> F[Attack-surface overlay<br/>sources · sinks · paths]
    F --> G[Exploitability score<br/>0–100, deterministic]
    G --> H[A–F risk grade]
    G --> I[AI fix agent]
    G --> J[Pentest agent<br/>live PoC]
    style D fill:#ff00aa,stroke:#ff00aa,color:#fff
    style G fill:#00e5ff,stroke:#00e5ff,color:#0d0221
```

<p align="center">
  <img src="https://img.shields.io/badge/NestJS-Fastify-ff00aa?style=flat-square&logo=nestjs&logoColor=white&labelColor=0d0221" />
  <img src="https://img.shields.io/badge/Next.js-14-00e5ff?style=flat-square&logo=nextdotjs&logoColor=white&labelColor=0d0221" />
  <img src="https://img.shields.io/badge/Turborepo-monorepo-ff00aa?style=flat-square&logo=turborepo&logoColor=white&labelColor=0d0221" />
  <img src="https://img.shields.io/badge/Tree--sitter-AST-00e5ff?style=flat-square&labelColor=0d0221" />
  <img src="https://img.shields.io/badge/SSE-real--time-ff00aa?style=flat-square&labelColor=0d0221" />
  <img src="https://img.shields.io/badge/Docker-ready-00e5ff?style=flat-square&logo=docker&logoColor=white&labelColor=0d0221" />
</p>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🛰️ Latest Builds

<table>
<tr>
<td width="50%" valign="top">

### 📱 [Mobile QA Runner](https://github.com/Sicariusa/mobile-testing)
`Python` · `uiautomator2` · `Tesseract OCR` · `ADB`

Hand it an **APK + a YAML test case** — it installs, launches, taps, types, swipes and **validates every step two ways**: the accessibility tree *and* screenshot OCR for text the tree never exposes.

- 🔁 **Recovery ladder** — wait/retry → dismiss keyboard → scroll into view → OCR, before it gives up
- 🧾 Every step leaves evidence: before/after shots, hierarchy dump, recovery trace
- 📄 Self-contained **HTML report** per run
- 🩺 `--check-env` diagnoses the whole toolchain and **never throws**

<sub>Born from real fintech QA work — 63 commits, 25 test modules.</sub>

</td>
<td width="50%" valign="top">

### 🎧 [Discord Clone](https://github.com/Sicariusa/discord-clone)
`NestJS` · `React` · `PostgreSQL` · `Redis` · `LiveKit`

Not a UI copy — a **faithful rebuild of Discord's hard parts**: realtime chat, voice/video, and the permission model.

- 🔐 Permissions as a **`bigint` bitfield**, resolved in Discord's exact overwrite order — one engine **shared by client and server** so they can't disagree
- 🛰️ Raw **WebSocket gateway** with opcode/dispatch + **Redis pub/sub** fan-out for horizontal scale
- 🎙️ **LiveKit SFU** — the API mints tokens whose publish grants come from your role perms
- 🤖 First-class **bots** governed by the same permission engine

</td>
</tr>
</table>

## 🧩 More From The Lab

| | Project | The interesting part | Stack |
|:-:|:--|:--|:--|
| 🚗 | [**Carpooling System**](https://github.com/Sicariusa/carpooling-backend) | User · Booking · Ride microservices talking over **Kafka** topics, containerized end-to-end | NestJS · Kafka · MongoDB · Docker |
| ✈️ | [**SkyTracker**](https://github.com/Sicariusa/Flights) | Thousands of **live aircraft** on a 3D map — click any plane for ICAO details | React · Mapbox GL · OpenSky |
| 🌍 | [**Earth Visualization**](https://earth-threejs-eta.vercel.app) | Fresnel atmosphere shader, animated clouds, procedural starfield — **zero build step** | Three.js · WebGL |
| 🤖 | [**AI App Builder**](https://github.com/Sicariusa/chef) | Fork of Convex Chef with prompt-engineered codegen and **error auto-correction** | Gemini · Convex · Docker |
| 💼 | [**Statements Corp**](https://www.statements-corp.com) | **In production.** Contentful CMS, Mapbox service regions, SEO pipeline | React · Contentful · Framer Motion |
| 📚 | [**E-Learning Platform**](https://github.com/Sicariusa/E-Learning-Platform) | Full MERN platform deployed on Railway | MongoDB · Express · React · Node |

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🛠️ Arsenal

<p align="center">
  <b><sub>LANGUAGES</sub></b><br/>
  <img src="https://skillicons.dev/icons?i=ts,js,py,java,cs,cpp,dart,sql&theme=dark" />
  <br/><br/>
  <b><sub>BACKEND · DATA · INFRA</sub></b><br/>
  <img src="https://skillicons.dev/icons?i=nestjs,nodejs,express,kafka,redis,postgres,prisma,mongodb,docker,aws,linux&theme=dark" />
  <br/><br/>
  <b><sub>FRONTEND · MOBILE · 3D</sub></b><br/>
  <img src="https://skillicons.dev/icons?i=react,nextjs,vite,tailwind,threejs,flutter,firebase,figma&theme=dark" />
  <br/><br/>
  <b><sub>AI · TESTING · TOOLING</sub></b><br/>
  <img src="https://skillicons.dev/icons?i=tensorflow,sklearn,opencv,selenium,postman,git,github,vercel&theme=dark" />
</p>

## 📡 Signal

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Sicariusa&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d0221&title_color=ff00aa&icon_color=00e5ff&text_color=e6e6f0&ring_color=ff00aa" height="170"/>
  <img src="https://streak-stats.demolab.com?user=Sicariusa&hide_border=true&background=0d0221&ring=ff00aa&fire=00e5ff&currStreakLabel=00e5ff&sideLabels=ff00aa&dates=8888aa&currStreakNum=ffffff&sideNums=ffffff" height="170"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Sicariusa&bg_color=0d0221&color=e6e6f0&line=ff00aa&point=00e5ff&area=true&area_color=ff00aa&hide_border=true&custom_title=Contribution%20Pulse" width="100%"/>
</p>

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:00e5ff,50:ff00aa,100:0d0221&height=130&section=footer" width="100%"/>
