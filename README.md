# 🤖 Autonomous Multi-Agent Assistant in n8n

An end-to-end, multi-agent AI workflow built in **n8n** using **Google Gemini** models. This architecture leverages a central **Manager Agent** to orchestrate intent routing across specialized downstream sub-agents for Calendar, Contacts, and Email management.

![Workflow Screenshot](./image.png)

## 🏗️ Architecture & Agent Breakdown

- **Manager Agent (Orchestrator):** Analyzes incoming chat messages, evaluates intent, delegates execution to sub-agents, and aggregates responses.
- **Calendar Reservation Agent:** Interacts with Google Calendar APIs (`Get Availability`, `Search`, `Create`, `Update`, `Delete`).
- **Contacts Agent:** Handles contact directory actions (`Get`, `Create`, `Update`).
- **Email Agent:** Controls Gmail operations (`Fetch Unread`, `Send Email`, `Reply to Thread`, `Delete Email`).

## 🛠️ Tech Stack & Tools

- **Workflow Orchestration:** n8n
- **LLM Engine:** Google Gemini Chat Model
- **Memory Management:** Window Buffer Memory / Simple Memory per agent
- **Integrations:** Google Calendar API, Google Contacts API, Gmail API

## 🚀 Key Capabilities

- **Context Preservation:** Sub-agents maintain isolated conversation memory while reporting back to the parent orchestrator.
- **Tool Grounding:** Deterministic execution of external tool APIs based on autonomous LLM function calling.
- **Automated Scheduling & Communication:** Hands-free execution of cross-platform productivity tasks.
