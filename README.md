# ⚙️ Automated Client Management & Follow-Up System

An automated client management and follow-up system built with **n8n, Supabase, Google Forms, Google Sheets, and Gmail**.

It automates the process from receiving a client request to scheduling a call, following up with inactive clients, and closing the request.

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
Confirmation Email
      ↓
Scheduling Form
      ↓
   Check Status
    ↙       ↘
Completed   Pending
   ↓          ↓
Continue   Follow-Up
              ↓
       Second Form
              ↓
         Check Again
          ↙       ↘
     Completed   Pending
         ↓          ↓
      Continue   Close Request
```

## 🧩 Tech Stack

* **n8n** — Workflow automation
* **Supabase** — Database & request tracking
* **Google Forms** — Client forms
* **Google Sheets** — Scheduling tracking
* **Gmail** — Automated emails

## 🎯 Features

* Automated client intake
* Unique request IDs
* Personalized confirmation emails
* Call scheduling
* Automated follow-ups
* Second scheduling attempt
* Automatic request closure
* Centralized client data

### 🚀 Automation Studio

Automating client management from first contact to follow-up.

Built as an automation system designed to streamline client management and follow-up processes.

