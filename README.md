# 🎯 Automated Event Lead Generation & Data Pipeline for Music Licensing (UPFR)

## 📌 Project Overview
This project is an automated Data Pipeline built using **Make.com**, **Apify (Google Search Scraper)**, and **Google Sheets**. The objective is to identify and structure public event lead opportunities (e.g., street food festivals, sports marathons, trade fairs, DJ sets) that utilize recorded background music, specifically targeting entities that require public performance licensing under **UPFR** regulations.

## 🏗️ Architecture & Workflow
1. **Trigger / Data Acquisition (Apify Actor):** Runs targeted Google Search queries dynamically to discover local event listings while excluding live concerts/orchestras.
2. **Data Extraction & Transformation (Make Scenario):** Programmatically fetches dataset items (`defaultDatasetId`), applies fallback mapping logic (`ifempty`), and parses event metadata (names, URLs, descriptions).
3. **Storage & Visualization (Google Sheets):** Automates row insertion and highlights records based on temporal and status filters using conditional formatting,
   
## 🛠️ Tech Stack & Tools
* **Integration & ETL:** Make.com (Integromat)
* **Web Scraping:** Apify Actors (Google Search Results Scraper)
* **Data Destination:** Google Sheets
* **Data Processing Concepts:** JSON Parsing, Dynamic Dataset Referencing, Boolean Search Queries, Data Filtering & Normalization

## 💡 Key Challenges & Technical Learnings
* **Dynamic Dataset Handling:** Configured Make to dynamically reference `defaultDatasetId` across executions to prevent hardcoded mapping failures.
* **Query Optimization:** Formulated strict search strings (`-concert -live -orchestra`) to isolate events using recorded music background rather than live musical performances.
* **Data Sanitization:** Implemented `ifempty` formulas within scenario mappings to handle missing meta-descriptions gracefully.

## 🚀 Future Enhancements
* Adding automated email notifications for newly qualified leads.
* Integrating a Python NLP script to score lead probability based on description keywords.
