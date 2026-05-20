<div align="center">

<img src="https://img.shields.io/badge/DiagramForge-v1.0.2-6366f1?style=for-the-badge&labelColor=0f172a" alt="Version"/>
&nbsp;
<img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-3b82f6?style=for-the-badge&labelColor=0f172a" alt="Platform"/>
&nbsp;
<img src="https://img.shields.io/badge/License-Apache%202.0-10b981?style=for-the-badge&labelColor=0f172a" alt="License"/>
&nbsp;
<img src="https://img.shields.io/badge/Price-Free-f59e0b?style=for-the-badge&labelColor=0f172a" alt="Free"/>

<br/><br/>

# 🧩 DiagramForge

### Make changes to your Architecture Diagrams on the fly by talking to DiagramForge

*Combine the full draw.io editor with AI chat — describe what you want, watch the diagram update.*

<br/>

[![Download for Windows](https://img.shields.io/badge/⬇️%20Download%20for%20Windows-6366f1?style=for-the-badge)](https://github.com/dataamigos/diagramforge-releases/releases/latest)
&nbsp;
[![Download for macOS](https://img.shields.io/badge/⬇️%20Download%20for%20macOS-6366f1?style=for-the-badge)](https://github.com/dataamigos/diagramforge-releases/releases/latest)
&nbsp;
[![How to Use](https://img.shields.io/badge/📖%20How%20to%20Use-0f172a?style=for-the-badge)](https://dataamigos.github.io/diagramforge-releases/)

</div>

---

## ✨ What is DiagramForge?

DiagramForge is a **free desktop app** that lets you design and modify architecture diagrams just by describing what you want in plain English.

- 🎨 **Full draw.io editor** — runs 100% offline, no internet needed for diagramming
- 🤖 **AI chat panel** — describe changes, the diagram updates instantly
- 🔌 **Multi-provider AI** — use Gemini, GPT-4, Claude, Ollama, Azure, AWS Bedrock, DeepSeek, OpenRouter
- 🔒 **Your data stays local** — diagrams never leave your machine
- 💸 **Completely free** — no account, no subscription, no telemetry

---

## ⬇️ Download

| Platform | File | Notes |
|----------|------|-------|
| 🪟 **Windows Installer** | `DiagramForge.Setup.1.0.2.exe` | Standard installer |
| 🪟 **Windows Portable** | `DiagramForge.1.0.2.exe` | No installation needed — just run it |
| 🍏 **macOS Intel** | `DiagramForge-1.0.2.dmg` | For Intel Macs |
| 🍏 **macOS Apple Silicon** | `DiagramForge-1.0.2-arm64.dmg` | For M1/M2/M3 Macs |

**👉 [Go to Latest Release →](https://github.com/dataamigos/diagramforge-releases/releases/latest)**

---

## 🚀 How to Use

### Step 1 — Install

Run the installer or the portable EXE (no installation needed). draw.io is bundled and works fully offline.

### Step 2 — Configure Your AI Provider

Click the **⚙ Settings icon** → **AI Model Configuration** → Add a provider and paste your API key.

| Provider | Notes |
|----------|-------|
| ✨ **Google Gemini** | Recommended · Free tier at [aistudio.google.com](https://aistudio.google.com) |
| 🤖 **OpenAI** | GPT-4o and GPT-4 family |
| 🧠 **Anthropic Claude** | Claude Sonnet & Opus |
| 🏠 **Ollama** | 100% local, no API key needed |
| ☁️ **Azure OpenAI / AWS Bedrock** | Enterprise providers supported |
| 🔀 **DeepSeek / OpenRouter** | Additional model options |

> 💡 **Tip:** Gemini 2.5 Pro produces the most accurate diagrams. Get a free API key from Google AI Studio.

### Step 3 — Describe Your Diagram

Select your model from the dropdown and start typing:

```
Create a C4 container diagram for a microservices e-commerce platform
```
```
Add a Redis cache between the API gateway and the product service
```
```
Arrange the services in a left-to-right flow with the database at the bottom
```

The diagram updates instantly. Keep iterating — every message builds on the previous one.

---

## 💡 Prompt Ideas

| Type | Example Prompt |
|------|---------------|
| **C4 Architecture** | *"C4 context diagram for a banking app — mobile clients, API gateway, PostgreSQL"* |
| **Microservices** | *"Microservices diagram with auth, order, inventory services and a message queue"* |
| **Data Pipeline** | *"Data pipeline from S3 through Spark to Redshift with a BI layer"* |
| **Sequence** | *"OAuth2 login flow — client, auth server, resource server, token refresh"* |
| **Cloud** | *"AWS serverless API — API Gateway, Lambda, DynamoDB, CloudWatch"* |
| **Iterate** | *"Add a CDN in front of the load balancer and a read replica for the database"* |

---

## 🛠️ Pro Tips

- **Be specific about diagram type** — say "C4 container diagram" or "sequence diagram" for better results
- **Name your components** — use real names like `OrderService`, `PostgreSQL`, `Kafka` for precise edits
- **Iterate in small steps** — one change at a time works better than one massive prompt
- **Export anytime** — File → Export as PNG, SVG, or PDF directly from the draw.io editor

---


## 🤖 Use with AI Agents — MCP Server

DiagramForge ships with a built-in **MCP (Model Context Protocol) server** that lets AI coding agents generate and update diagrams as a native tool call — no browser required.

Once the desktop app is installed, point any MCP-compatible agent host at the bundled server:

### Claude Code

Add to `.claude/settings.json` in your project:

```json
{
  "mcpServers": {
    "diagramforge": {
      "command": "node",
      "args": ["<path-to-DiagramForge>/packages/mcp-server/dist/index.js", "--no-preview"]
    }
  }
}
```

### What your agent can do

| Tool | What it does |
|------|-------------|
| `start_session` | Open DiagramForge with a live browser preview |
| `create_new_diagram` | Generate a new diagram from draw.io XML |
| `edit_diagram` | Add, update, or delete specific elements in an existing diagram |
| `get_diagram` | Fetch the current diagram XML (including manual edits) |
| `export_diagram` | Save the diagram as `.drawio`, `.svg`, or `.png` |

### With browser preview (default)

```bash
# Agent calls start_session → DiagramForge opens in browser
# Every diagram change appears in real time
node packages/mcp-server/dist/index.js
```

### Headless / CI mode

```bash
# No browser — pure XML in, XML out
node packages/mcp-server/dist/index.js --no-preview
```

> 💡 **Tip:** Use `--no-preview` in CI/CD pipelines. Use default (with preview) when you want to watch the agent build diagrams live in the draw.io editor.

---

## 📋 Requirements

- **Windows:** Windows 10/11 (64-bit)
- **macOS:** macOS 12+ (coming soon)
- **AI:** Your own API key for your chosen provider (Gemini free tier works great)

---

<div align="center">

Built by **Venkat Meruva** &nbsp;·&nbsp; Free to use, free to share &nbsp;·&nbsp; Apache 2.0

[![Download Latest Release](https://img.shields.io/badge/⬇️%20Download%20Latest%20Release-6366f1?style=for-the-badge)](https://github.com/dataamigos/diagramforge-releases/releases/latest)

</div>
