# 🤖 n8n AI Automation Portfolio

This portfolio focuses on **practical automations** used in content creation, email management, knowledge systems, browser automation, and internal business tools.

---

## 🚀 What This Portfolio Shows

* Designing **production-ready n8n workflows**
* Building **AI agents** for decision-making and automation
* Implementing **RAG systems** using vector databases
* Automating **email, inventory, content, browser, and video workflows**
* Integrating **OpenAI, Pinecone, Gmail, Google Sheets, OneDrive, LinkedIn, RunwayML, YouTube, Airtop, and ElevenLabs APIs**

---

## 📂 Projects

### 1. RAG Knowledge Base (Chat with Data)

A private knowledge system that allows users to upload documents and “chat” with them using AI.

**Workflows**

* **rag-ingestion.json**
  *Function:* Document ingestion and learning pipeline
  *Features:*

  * Downloads files from **Microsoft OneDrive**
  * Splits text into chunks
  * Generates embeddings using OpenAI
  * Stores vectors in **Pinecone**

* **rag-chat.json**
  *Function:* Retrieval and chat interface
  *Features:*

  * AI Agent retrieves relevant context from Pinecone
  * Answers user queries using **only private data**
  * Prevents hallucinations by restricting responses to stored documents

**Tech Stack:** OpenAI, Pinecone, OneDrive, n8n AI Agents

---

### 2. Inventory Management Agent

An AI-powered virtual employee that manages inventory using natural language.

**Workflow**

* **inventory-agent.json**

**Function**

* Searches products
* Updates stock levels
* Responds to inventory queries via chat

**Features**

* Natural language interaction
* Google Sheets used as the inventory database
* Real-time stock updates

**Tech Stack:** OpenAI, Google Sheets, LangChain, n8n

**Setup Requirement:**
Google Sheet with columns: `Item Name` and `Quantity`

---

### 3. Smart Email Manager (Inbox Zero)

An intelligent email automation system designed to reduce inbox overload.

**Workflow**

* **email-classifier.json**

**Function**

* Reads incoming emails
* Classifies them by importance
* Drafts replies automatically

**Features**

* Categorizes emails (Sponsorship, High Priority, Test)
* Generates context-aware replies using AI
* Saves replies as **Gmail drafts** for manual review
* Designed to support real-world creator and business inboxes

**Tech Stack:** OpenAI, Gmail API, n8n

---

### 4. Simple Mail Sender

A lightweight workflow for sending emails using natural language commands.

**Workflow**

* **gmail-sender.json**

**Function**

* Sends emails based on user intent (e.g., “Send a report to Bob”)

**Features**

* Converts prompts into structured email actions
* Uses Gmail API for delivery

**Tech Stack:** OpenAI, Gmail API, n8n

---

### 5. AI-Powered LinkedIn Post Generator 📢

An end-to-end content automation workflow for LinkedIn.

**Workflow**

* **linkedin-post-generator.json**

**Function**

* Researches topics
* Writes LinkedIn-optimized posts
* Generates images
* Publishes posts automatically

**Features**

* AI Research Agent gathers topic context
* Human-like, Unicode-optimized LinkedIn content
* AI-generated images for better engagement
* Automatic posting via **LinkedIn API**
* Triggered via a form submission

**Tech Stack:** OpenAI (Chat & Image Models), LinkedIn API, n8n AI Agents

---

### 6. AI-Generated Video Automation (Idea → Video → YouTube 🎥)

A fully automated pipeline that turns video ideas into AI-generated videos and uploads them to YouTube.

**Workflow**

* **AI Generated Videos.json**

**Function**

* Reads video ideas from Google Sheets
* Converts ideas into cinematic AI prompts
* Generates videos using AI
* Uploads videos automatically to YouTube
* Updates video status back in Google Sheets

**Features**

* Scheduled execution (hands-free automation)
* AI Agent generates **high-density cinematic prompts**
* Video generation using **RunwayML**
* Automatic YouTube uploads
* Status tracking via Google Sheets (e.g., In Progress → Published)

**Tech Stack:** OpenAI, RunwayML, Google Sheets, YouTube API, n8n AI Agents

---

### 7. AI Browser Automation & Web Research Agent 🌐🧠 **(NEW)**

An advanced AI-powered browser automation system that can **navigate websites, interact with UI elements, extract data, and answer user queries in real time**.

This project is split into **two coordinated workflows**.

---

#### A. Browser Session Manager

**Workflow**

* **Browser.json**

**Function**

* Creates and manages live browser sessions
* Opens real browser windows with visual feedback
* Designed to be triggered by other workflows

**Features**

* Uses **Airtop** to launch real browser sessions
* Supports CAPTCHA solving
* Live browser window rendering (1280×720)
* Persistent browser profiles
* Designed for multi-workflow orchestration

**Tech Stack:** Airtop API, n8n

---

#### B. AI Web Search & Interaction Agent

**Workflow**

* **Searcher.json**

**Function**

* Allows users to chat with an AI agent that can browse the web, search, click, type, extract information, and respond intelligently.

**Features**

* Chat-triggered AI agent
* Dynamic browser creation via workflow tools
* Can:

  * Load URLs
  * Type into input fields
  * Click buttons or links
  * Extract structured data from pages
* Uses memory to maintain conversation context
* Terminates browser sessions automatically after task completion

**Tech Stack:**
OpenAI (GPT-4o-mini), Airtop API, LangChain Agents & Memory, n8n

---

### 8. AI Voice / Natural Language Email Agent ✉️🎙️ **(NEW)**

A webhook-driven AI agent that **accepts voice or natural language instructions and autonomously drafts and sends professional emails**.

**Workflow**

* **voice-agent.json**

**Function**

* Accepts **voice input converted to text using ElevenLabs**
* Accepts structured text instructions via webhook
* Identifies recipients
* Drafts professional emails using AI
* Sends emails automatically

**Features**

* Voice-enabled email automation via **ElevenLabs**
* Webhook-triggered execution
* AI Agent powered email drafting
* Contact lookup via Google Sheets
* Gmail-based email delivery
* Designed for hands-free, voice-assistant-style workflows
* Modular tool-based agent architecture

**Tech Stack:**
OpenAI (Chat Models), **ElevenLabs (Speech-to-Text / Voice Interface)**, Gmail API, Google Sheets, LangChain Agent Tools, n8n

**Setup Requirement:**
Google Sheet containing recipient names and email addresses

---

## 🛠️ Setup & Usage

### Import Workflows

1. Open **n8n**
2. Go to **Add Workflow → Import from File**
3. Import the required `.json` workflow files

### Required Credentials

You must configure your own credentials for:

* OpenAI API
* Pinecone (for RAG workflows)
* Google Cloud (Gmail & Google Sheets)
* Microsoft OneDrive (RAG ingestion)
* LinkedIn API (LinkedIn Post Generator)
* RunwayML API (Video Generation)
* YouTube API (Video Uploads)
* Airtop API (Browser Automation)
* **ElevenLabs API (Voice Input / Speech Processing)**

> ⚠️ Credentials are **not included** for security reasons.

---

## 📌 Notes

* All workflows are modular and customizable
* Designed for **real-world automation use cases**
* Supports **AI agents, browser automation, voice interfaces, content pipelines, and video publishing**
* Can be extended with additional tools, triggers, and agent logic

---

## 📄 License

This project is licensed under the **MIT License**.
See the `LICENSE` file for more details.
