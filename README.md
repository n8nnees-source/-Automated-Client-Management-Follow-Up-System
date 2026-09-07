# -Automated-Client-Management-Follow-Up-System
An automated client management and follow-up system built with n8n, Supabase, Google Forms, Google Sheets, and Gmail. It automates client requests, generates unique request IDs, manages call scheduling, and keeps client information synchronized throughout the workflow.
# ⚙️ Automated Client Management & Follow-Up System

An automated client management system built with **n8n, Supabase, Google Forms, Google Sheets, and Gmail**.

The workflow automates the process from receiving a client request to scheduling a call and following up with clients who haven't scheduled.

## 🔄 How it works

```text
Client Request
      ↓
    Webhook
      ↓
   Supabase
      ↓
 Unique Request ID
      ↓
Google Sheets + Gmail
      ↓
Scheduling Form
      ↓
Update Client Data
      ↓
Follow-Up
```

## 🧩 Tech Stack

* **n8n** — Workflow automation
* **Supabase** — Database & Request IDs
* **Google Sheets** — Data management
* **Google Forms** — Call scheduling
* **Gmail** — Automated emails

## 🎯 Features

* Automated client intake
* Unique Request ID system
* Automated confirmation emails
* Call scheduling
* Client data synchronization
* Automated follow-ups
