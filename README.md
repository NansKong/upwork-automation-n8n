# Upwork Automation

## About

This project is an automated system built with **n8n** that continuously monitors new Upwork job postings and evaluates them using **AI-based scoring**.  
The goal is to identify high-value automation and AI-related jobs, prioritize them, and store structured results for easy tracking and decision-making.

The workflow runs on a schedule, processes multiple jobs per execution, and operates end-to-end without manual intervention.

---

## How It Works

1. **Scheduled Trigger**
   - The workflow runs automatically every **8 hours**.

2. **Job Fetching**
   - New Upwork jobs posted within the **last 6 hours** are fetched using an Apify scraper.

3. **Data Normalization**
   - Relevant job fields (title, description, URL, skills, experience level, created date) are extracted and standardized.

4. **Pre-Filtering**
   - Jobs are filtered based on:
     - Experience level
     - Keywords related to automation, APIs, AI, and workflows
   - Irrelevant jobs are discarded before AI processing.

5. **Batch Processing**
   - Jobs are processed in a loop, allowing **multiple jobs (10+)** to be handled in a single run.

6. **AI Scoring**
   - Each job is evaluated by an AI model which returns:
     - **Score (1–10)**
     - **Priority** (High / Medium / Low)
     - **Reasoning** explaining the score

7. **Priority Handling**
   - High-priority jobs trigger an email alert.
   - All scored jobs continue to storage.

8. **Data Storage**
   - Final structured job data, along with AI scores and reasoning, is stored in **Airtable** for review and tracking.

---

## Output

Each processed job includes:
- Job title
- Description
- URL
- Skills
- Experience level
- AI score
- Priority
- Reasoning
