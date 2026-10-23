# 🤖 Autonomous Multi-Source Job Scraper & AI Agent

An automated data aggregation pipeline built in n8n that scrapes job opportunities across multiple platforms, deduplicates and filters listings, evaluates candidate match using Groq LLMs, and dispatches real-time alerts to Telegram.

---

## 🏗️ Workflow Architecture

1. **Scheduled Ingestion:** Timed trigger initiates multi-source fetching.
2. **Data Scraping & RSS Fetching:** Ingests raw listings concurrently via RSS feeds and Apify web actors.
3. **Aggregation & Deduplication:** Merges data streams and removes duplicate entries[cite: 8].
4. **AI Match Analysis:** Loops each listing through a Groq Chat Model to evaluate job requirements against target candidate profiles[cite: 8].
5. **Conditional Routing:** Filters out low-match roles and formats relevant listings[cite: 8].
6. **Instant Alerts:** Pushes structured alerts with direct application links to Telegram[cite: 8].

---

## 🛠️ Tech Stack & Integrations

* **Automation Platform:** n8n[cite: 8]
* **Data Sources:** Apify Scraper Actor, RSS Feeds[cite: 8]
* **AI/LLM:** Groq Chat Model (Basic LLM Chain)[cite: 8]
* **Notifications:** Telegram Bot API[cite: 8]
* **Scripting:** Custom JavaScript[cite: 8]

---

## 🚀 How to Setup

1. Download the `workflow.json` from this repository[cite: 8].
2. Import it into your **n8n** instance[cite: 8].
3. Configure credentials for **Apify**, **Groq API**, and **Telegram Bot**[cite: 8].
4. Set your search terms in the scraper nodes and activate the schedule trigger[cite: 8]!
