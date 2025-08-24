# 🌀 FlowBack – Focus Flow Recorder & Replay Engine

[![Build Status](https://img.shields.io/github/actions/workflow/status/your-username/flowback/ci.yml?branch=main)](https://github.com/your-username/flowback/actions)
[![Azure Static Web Apps](https://img.shields.io/badge/Deployed%20on-Azure%20Static%20Web%20Apps-0089D6?logo=microsoft-azure)](https://azure.microsoft.com/en-us/services/app-service/static/)
[![Database](https://img.shields.io/badge/Database-Azure%20PostgreSQL-336791?logo=postgresql)](https://azure.microsoft.com/en-us/services/postgresql/)
[![AI](https://img.shields.io/badge/AI-Azure%20OpenAI-10A5F5?logo=openai)](https://azure.microsoft.com/en-us/products/ai-services/openai-service)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

FlowBack is a **web application** that helps developers, students, and knowledge workers capture their entire working flow across websites, code edits, notes, and commands.  
It organizes everything into a **searchable timeline**, provides **AI-powered summaries**, and lets you **replay your problem-solving sessions** like a movie.  

---

## 🚀 Problem Statement
Developers, designers, analysts, students, and founders often struggle with **losing context while switching tasks**.  
They forget how they solved tough issues, waste hours retracing old steps, and end the day wondering where their time went.  
Existing productivity tools only track time or tasks — **not the reasoning or problem-solving flow**.  

---

## ✅ Solution
**FlowBack** automatically captures activity (websites, code edits, notes, CLI commands), organizes it into a timeline,  
and uses **Azure OpenAI** to summarize reasoning steps. Users can search past sessions or replay them to recover lost context.  

---

## 🛠️ Tech Stack

### Frontend
- **React.js** – Timeline, Search, Replay UI  
- **Tailwind CSS / ShadCN** – Styling  
- **Deployed on Azure Static Web Apps**

### Capture Layer
- **Chrome Extension** – Track websites + scrolls  
- **VS Code Extension** – Track file edits  
- **CLI Logger (Optional)** – Capture git/docker commands  

### Backend
- **Node.js + Express.js** – REST API  
- **Azure App Service** – Deployment  

### Database & Search
- **Azure Database for PostgreSQL** – Structured logs & summaries  
- **Azure Cognitive Search** – Full-text & semantic search  

### AI Layer
- **Azure OpenAI Service** – Summarization, reasoning extraction, tagging  

### DevOps / Infra
- **GitHub Actions / Azure DevOps** – CI/CD  
- **Azure Monitor** – Logs & metrics  
- **Azure Blob Storage (optional)** – Screenshots/voice memos (future)  

---

## 🔄 Architecture Overview

1. User actions are captured via **extensions / notes / CLI**.  
2. Data flows into the **Backend API (Node.js on Azure App Service)**.  
3. Logs stored in **Azure PostgreSQL** and indexed in **Cognitive Search**.  
4. On demand, data is sent to **Azure OpenAI** for summaries + tags.  
5. **React Frontend (Azure Static Web Apps)** displays timeline, search, replay.  

---

## 🎯 Features (MVP)
- ✅ Capture websites, file edits, and notes  
- ✅ Timeline visualization of work sessions  
- ✅ AI-powered block summaries (Azure OpenAI)  
- ✅ Search across logs, tags, and notes  
- ✅ Replay mode for past sessions  

---

## 📦 Installation (Dev Mode)

### Backend
```bash
# Clone the repo
git clone https://github.com/your-username/flowback.git
cd flowback/backend

# Install dependencies
npm install

# Run server
npm run dev

