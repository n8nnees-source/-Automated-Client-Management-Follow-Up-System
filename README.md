# ⚙️ Automated Client Management & Follow-Up System

An end-to-end **client management and follow-up automation** built with **n8n, Supabase, Google Forms, Google Sheets, and Gmail**.

It automates the client journey from the initial request to **call scheduling, automated follow-ups, and request closure**, reducing manual work and preventing potential clients from being forgotten.

## 🔄 How It Works

```text
Client Request
      ↓
   Automated Intake
      ↓
   Client Database
      ↓
Confirmation Email
      ↓
  Call Scheduling
      ↓
 Check Response
   ↙         ↘
Completed   Pending
   ↓           ↓
Continue    Follow-Up
                ↓
          Second Attempt
                ↓
           Check Again
             ↙    ↘
        Completed  Pending
            ↓        ↓
         Continue   Close
```

## 🧩 Technologies

* **n8n** — Workflow automation & business logic
* **Supabase** — Client database & request tracking
* **Google Forms** — Client information & scheduling
* **Google Sheets** — Scheduling response tracking
* **Gmail** — Automated client communication

## ✨ Key Features

* Automated client intake
* Unique request ID generation
* Client data management
* Personalized automated emails
* Call scheduling workflow
* Multi-step automated follow-ups
* Second scheduling attempt
* Automatic request closure

## 🛠️ Technical Details

The workflow uses **conditional logic, database operations, unique identifiers, scheduled delays, and multiple form submissions** to track each client throughout the process.

Client information is stored in Supabase, while Google Sheets is used to detect scheduling responses. n8n connects the different services and controls the entire automation.

## 🎯 Purpose

The system is designed to help businesses **capture, manage, and follow up with potential clients automatically**, creating a consistent process from first contact to conversion.

---

### Automation Studio

**Client management. Automated.**
