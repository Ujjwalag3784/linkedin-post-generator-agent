# LinkedIn Post Generator — AI Agent (n8n)

> A production-style AI automation agent for LinkedIn content creation, built with real integrations, persistent state, and human-in-the-loop feedback.

---

## 🚀 Why I Built This

Most “AI projects” stop at **prompt engineering demos**.

I wanted to build a **real AI agent** that:

- Runs **end-to-end**
- Interacts with **real external systems**
- Handles **human feedback loops**
- Survives **real-world edge cases**
- Resembles **production automation**, not a toy demo

This project is a **LinkedIn content generation AI agent**, orchestrated entirely in **n8n**, designed the same way AI agents are built in **marketing, growth, and ops teams**.

---

## 🤖 What This Agent Does

This agent automates **LinkedIn post creation** with a **human-in-the-loop approval workflow**.

### High-Level Flow

1. Receives structured input via **Webhook**
2. Uses an **LLM** to generate LinkedIn post content
3. Optionally generates and stores an image
4. Persists execution state in **Google Sheets** (acts as a lightweight DB)
5. Sends **approval emails** (Approve / Reject)
6. On rejection, regenerates content using human feedback
7. On approval, finalizes and stores all assets

This mirrors how **real AI agents operate in production environments**.

---

## 🧠 Core Features

- Multi-step AI reasoning
- Human-in-the-loop approval system
- Feedback-driven regeneration
- State persistence across executions
- Idempotent execution & retry safety
- Real external integrations
- Webhook-based API triggering

---

## 🛠️ Tech Stack

| Component | Technology |
|--------|------------|
| Agent Orchestration | n8n |
| Text Generation | OpenAI-compatible LLM |
| State Management | Google Sheets |
| Asset Storage | Google Drive |
| Approval Workflow | Email (SMTP / Gmail) |
| External Interface | Webhooks |

---

## 🔁 Workflow Architecture

- **Webhook Trigger** — API-style input
- **LLM Node** — Generates LinkedIn post copy
- **Conditional Logic** — Approval vs Rejection
- **Feedback Loop** — Regeneration on rejection
- **Persistent Storage** — Execution state & history
- **Finalization Step** — Asset storage & completion

This is **agent orchestration**, not a single prompt chain.

---

## 📁 Repository Structure

```plaintext
.
├── workflows/
│   └── post-generator.json   # Exported n8n AI agent workflow
└── README.md
```


▶️ How to Run the Agent

1️⃣ Import the Workflow

-Open n8n

-Go to Workflows

-Click Import

Upload post-generator.json

2️⃣ Configure Credentials

Set up credentials for:

-LLM Provider (OpenAI compatible)

-Google Sheets

-Google Drive

-Email (SMTP / Gmail)

⚠️ Credentials are not included in the repository for security reasons.

3️⃣ Activate & Trigger

Trigger the workflow via Webhook using JSON input:

{
  "post_topic": "AI agents in accounting automation",
  "target_audience": "Startup founders",
  "email": "example@email.com"
}

🎯 Why This Matters

This project demonstrates:

-Designing AI agents as systems, not demos

-Managing state across executions

-Handling human feedback loops

-Building resilient, production-style automations

-Integrating AI into real operational workflows

-It’s much closer to how AI agents are built in production than most portfolio projects.

👤 About Me
I’m actively exploring agentic AI, workflow orchestration, and real-world automation systems, and I enjoy debugging complex execution graphs more than writing prompts.
