
# Website Analytics – AI Explainer (Agent)

> An AI agent that turns raw Google Analytics data into clear, plain-English explanations — not just numbers.

---

## 🚀 Why I Built This

Most analytics dashboards answer **_what_ happened**, but not **_why_**.

Traffic goes up.
Sessions drop.
Users fluctuate.

But dashboards rarely explain the **reason behind the change**.

This AI agent bridges that gap by combining **deterministic data analysis** with **LLM-based reasoning** to explain website performance changes in simple, human-readable language.

---

## 🤖 What the Agent Does

This agent analyzes **Google Analytics 4 (GA4)** data and explains performance changes using automated logic + AI reasoning.

### High-Level Flow

1. Accepts a question via **Webhook**
2. Fetches **current vs previous week** data from GA4
3. Computes differences (sessions, users, trends)
4. Uses an LLM to explain changes in **plain English**
5. Returns insights as an **API response**

This makes analytics **actionable**, not just observable.

---

## 📥 Example Input

```json
{
  "question": "Why did traffic drop compared to last week?"
}
````

---

## 📤 Example Output (Conceptual)

* Traffic decreased by 18% week-over-week
* Organic search sessions declined significantly
* Direct traffic remained stable
* Overall drop is likely driven by reduced search visibility or campaign changes

(All explanations are grounded in actual GA4 metrics.)

---

## 🧠 Core Features

* GA4 data ingestion
* Time-window comparison logic (current vs previous period)
* Deterministic data processing
* AI explanations grounded in real metrics
* Webhook-based API interface
* Stateless execution (safe for production)

---

## 🛠️ Tech Stack

| Component              | Technology            |
| ---------------------- | --------------------- |
| Workflow Orchestration | n8n                   |
| Analytics Source       | Google Analytics 4    |
| Data Processing        | JavaScript            |
| Explanation Engine     | OpenAI-compatible LLM |
| Trigger Interface      | Webhooks              |

---

## 🔁 Workflow Architecture

* **Webhook Trigger** — Receives analytics question
* **GA4 Query Nodes** — Fetches time-windowed data
* **JS Processing Node** — Computes deltas & trends
* **LLM Node** — Converts metrics into explanations
* **API Response** — Returns insights

This ensures **AI explanations are grounded in deterministic calculations**, not hallucinations.

---

## 📁 Repository Structure

```plaintext
.
├── workflows/
│   └── website-analytics-explainer.json   # Exported n8n agent workflow
└── README.md
```

---

## ▶️ How to Run

### 1️⃣ Import Workflow

1. Open **n8n**
2. Go to **Workflows**
3. Click **Import**
4. Upload `website-analytics-explainer.json`

---

### 2️⃣ Configure Credentials

Set up credentials for:

* Google Analytics 4
* LLM Provider (OpenAI compatible)

> ⚠️ Credentials are not included for security reasons.

---

### 3️⃣ Activate & Trigger

Activate the workflow and trigger it via webhook with a JSON request.

---

## 🔐 Security

* No credentials, secrets, or tokens are stored in this repository
* All sensitive configuration is handled via n8n credentials
* Stateless execution ensures safe re-runs and retries

---

## 🎯 Why This Matters

This project demonstrates:

* Multi-source data reasoning
* AI explanations grounded in real metrics
* Production-style workflow orchestration
* Building AI agents that **explain**, not hallucinate
* Treating AI as a reasoning layer, not a magic box

This is how **analytics AI should work in production systems**.

---

## 👤 About Me

I’m exploring:

* Agentic AI systems
* Workflow orchestration
* AI + analytics automation
* Building AI agents that operate on real data

I enjoy designing systems that **reason over reality**, not just generate text.

---

## ⭐ If You Find This Useful

* Star the repo ⭐
* Fork it 🧬
* Extend it for product, marketing, or growth analytics 📊



