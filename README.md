# 🤖 n8n AI Automation Portfolio

This portfolio focuses on **practical automations** used in content creation, email management, knowledge systems, and internal business tools.

---

## 🚀 What This Portfolio Shows

* Designing **production-ready n8n workflows**
* Building **AI agents** for decision-making and automation
* Implementing **RAG systems** using vector databases
* Automating **email, inventory, content, and video workflows**
* Integrating **OpenAI, Pinecone, Gmail, Google Sheets, OneDrive, LinkedIn, RunwayML, and YouTube APIs**

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

### 6. AI-Generated Video Automation (Idea → Video → YouTube 🎥) **(NEW)**

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

> ⚠️ Credentials are **not included** for security reasons.

---

## 📌 Notes

* All workflows are modular and customizable
* Designed for real-world business and creator use cases
* Supports **content, email, and video automation**
* Can be extended with additional tools, triggers, and AI agents

---

## 📄 License

This project is licensed under the **MIT License**.
See the `LICENSE` file for more details.
