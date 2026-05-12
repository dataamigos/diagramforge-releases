<div align="center">

<img src="https://img.shields.io/badge/DiagramForge-v1.0.2-6366f1?style=for-the-badge&labelColor=0f172a" alt="Version"/>
<img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-3b82f6?style=for-the-badge&labelColor=0f172a" alt="Platform"/>
<img src="https://img.shields.io/badge/License-Apache%202.0-10b981?style=for-the-badge&labelColor=0f172a" alt="License"/>
<img src="https://img.shields.io/badge/Price-Free-f59e0b?style=for-the-badge&labelColor=0f172a" alt="Free"/>

<br/><br/>

# 🧩 DiagramForge

### Make changes to your Architecture Diagrams on the fly by talking to DiagramForge

*Combine the full draw.io editor with AI chat — describe what you want, watch the diagram update.*

<br/>

[⬇️ Download for Windows](https://github.com/dataamigos/diagramforge-releases/releases/latest) &nbsp;·&nbsp; [🍏 Download for macOS](https://github.com/dataamigos/diagramforge-releases/releases/latest) &nbsp;·&nbsp; [📖 How to Use](#how-to-use)

</div>

---

## ✨ What is DiagramForge?

DiagramForge is a **free desktop app** that lets you design and modify architecture diagrams just by describing what you want in plain English.

- 🎨 **Full draw.io editor** — runs 100% offline, no internet needed for diagramming
- 🤖 **AI chat panel** — describe changes, the diagram updates instantly  
- 🔌 **Multi-provider AI** — use Gemini, GPT-4, Claude, Ollama, or any OpenAI-compatible endpoint
- 🔒 **Your data stays local** — diagrams never leave your machine
- 💸 **Completely free** — no account, no subscription, no telemetry

---

## ⬇️ Download

| Platform | File | Size |
|----------|------|------|
| 🪟 **Windows Installer** | `DiagramForge.Setup.1.0.2.exe` | 390 MB |
| 🪟 **Windows Portable** (no install) | `DiagramForge.1.0.2.exe` | 390 MB |
| 🍏 **macOS** | Coming soon | — |

👉 **[Go to Latest Release →](https://github.com/dataamigos/diagramforge-releases/releases/latest)**

---

## 🚀 How to Use

### Step 1 — Install

Run the installer (or the portable EXE — no installation needed). draw.io is bundled and works offline.

### Step 2 — Configure Your AI Provider

Click the **⚙ Settings icon** → **AI Model Configuration** → Add a provider and paste your API key.

| Provider | Notes |
|----------|-------|
| ✨ **Google Gemini** | Recommended · Free tier available at [aistudio.google.com](https://aistudio.google.com) |
| 🤖 **OpenAI** | GPT-4o and GPT-4 family |
| 🧠 **Anthropic Claude** | Claude 3.5 & 4 |
| 🏠 **Ollama** | 100% local, no API key needed |
| 🔌 **Any OpenAI-compatible** | Bring your own endpoint |

> 💡 **Tip:** Gemini 2.5 Pro produces the most accurate diagrams. Get a free API key from Google AI Studio.

### Step 3 — Describe Your Diagram

Select your model from the dropdown in the chat bar and start typing:

```
Create a C4 container diagram for a microservices e-commerce platform
```
```
Add a Redis cache between the API gateway and the product service
```
```
Arrange the services in a left-to-right flow with the database layer at the bottom
```

The diagram updates instantly. Keep iterating — every message builds on the previous one.

---

## 💡 Prompt Ideas

| Type | Example Prompt |
|------|---------------|
| **Architecture** | *"Draw a C4 context diagram for a banking app with mobile clients, API gateway, and PostgreSQL"* |
| **Microservices** | *"Create a microservices diagram with auth, order, inventory services and a message queue"* |
| **Data Pipeline** | *"Show a data pipeline from S3 through Spark to Redshift with a BI layer"* |
| **Sequence** | *"OAuth2 login flow — client, auth server, resource server, token refresh"* |
| **Cloud** | *"AWS serverless API — API Gateway, Lambda, DynamoDB, CloudWatch"* |
| **Iterate** | *"Add a CDN in front of the load balancer and a read replica for the database"* |

---

## 🛠️ Pro Tips

- **Be specific about diagram type** — say "C4 container diagram" or "sequence diagram" for better results
- **Name your components** — use real names like `OrderService`, `PostgreSQL`, `Kafka` for precise edits
- **Iterate in small steps** — one change at a time works better than one massive prompt
- **Export anytime** — File → Export as PNG, SVG, or PDF from the draw.io editor

---

## 🏗️ Built On

DiagramForge is built on two excellent Apache 2.0 open source projects:

- **[draw.io](https://github.com/jgraph/drawio)** by JGraph — the industry-standard open-source diagramming engine
- **[next-ai-draw-io](https://github.com/DayuanJiang/next-ai-draw-io)** by Dayuan Jiang — the AI + draw.io architecture foundation

---

## 📋 Requirements

- **Windows:** Windows 10/11 (64-bit)
- **macOS:** macOS 12+ (coming soon)
- **AI:** Your own API key for your chosen provider

---

<div align="center">

Built by **Venkat Meruva** &nbsp;·&nbsp; Free to use, free to share &nbsp;·&nbsp; Apache 2.0

[⬇️ Download Latest Release](https://github.com/dataamigos/diagramforge-releases/releases/latest)

</div>
