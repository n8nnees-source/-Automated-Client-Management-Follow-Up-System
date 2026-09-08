# ⚙️ Automated Client Management & Follow-Up System

An automated client management and follow-up system built with **n8n, Supabase, Google Forms, Google Sheets, and Gmail**.

The system automates the client journey from the initial service request to call scheduling, follow-ups, and final request closure — while keeping client information organized and synchronized.

---

## 🔄 How It Works

```text
                 CLIENT
                   │
                   ▼
            Initial Request
                   │
                   ▼
                Webhook
                   │
                   ▼
               Supabase
          ┌────────┴────────┐
          │                 │
          ▼                 ▼
    Request ID        Client Data
          │                 │
          └────────┬────────┘
                   ▼
          Confirmation Email
                   │
                   ▼
          Scheduling Form
                   │
                   ▼
          ┌────────────────┐
          │ Has it been    │
          │ completed?     │
          └───────┬────────┘
              YES │ NO
                  │
        ┌─────────┘
        ▼
   Continue Process
                  │
                  ▼
             Wait 2 Days
                  │
                  ▼
        ┌────────────────┐
        │ Still pending? │
        └───────┬────────┘
            YES │ NO
                │
       ┌────────┘
       ▼
 Follow-Up Email
       │
       ▼
 Second Scheduling Form
       │
       ▼
   Wait 2 Days
       │
       ▼
 ┌─────────────────┐
 │ Form completed? │
 └───────┬─────────┘
     YES │ NO
         │
    ┌────┘
    ▼
 Continue       Goodbye Email
 Process        & Close Request
```

---

## 🧩 Tech Stack

| Technology        | Purpose                                |
| ----------------- | -------------------------------------- |
| **n8n**           | Workflow automation and business logic |
| **Supabase**      | Client database and request management |
| **Google Forms**  | Client intake and call scheduling      |
| **Google Sheets** | Scheduling response tracking           |
| **Gmail**         | Automated client communication         |

---

## 🎯 Features

### 📥 Automated Client Intake

Client requests enter the system automatically through a webhook and are stored in Supabase.

### 🆔 Unique Request IDs

Each request receives a unique identifier that allows the workflow to track the client throughout the process.

### 📧 Automated Email Communication

Clients automatically receive confirmation, scheduling reminders, and follow-up emails without manual intervention.

### 📅 Call Scheduling

Clients receive a personalized scheduling form with their request information pre-filled.

### 🔁 Automated Follow-Up System

If a client does not complete the scheduling form, the system automatically follows up after a defined period.

A second scheduling form can be sent if the client still has not completed the process.

### 🗄️ Centralized Client Data

Client information is stored and managed through Supabase while scheduling responses are tracked through Google Sheets.

### ⏳ Time-Based Automation

The workflow uses automated waiting periods to determine when follow-ups should be sent.

### 👋 Automatic Request Closure

If the client remains inactive after multiple follow-ups, the system sends a final email informing them that the request has been closed.

---

## 🧠 Workflow Logic

The system uses conditional logic to determine what happens at each stage:

```text
New Client Request
        ↓
Create Client Record
        ↓
Generate Request ID
        ↓
Send Confirmation
        ↓
Request Call Scheduling
        ↓
       IF
      /  \
    YES   NO
     │     │
     │    Wait
     │     ↓
     │  Follow-Up
     │     ↓
     │ Second Form
     │     ↓
     │   Wait
     │     ↓
     │    IF
     │   /  \
     │ YES   NO
     │  │     │
     │  │  Close Request
     │  │
     └──┴──→ Continue
```

---

## ✉️ Automated Client Experience

The client receives different communications depending on their progress:

**1. Confirmation**

Confirms that the initial request has been received.

**2. Scheduling Email**

Invites the client to complete the call scheduling form.

**3. Follow-Up**

If the scheduling form has not been completed, an automated reminder is sent.

**4. Final Follow-Up**

A second opportunity is provided to complete the scheduling process.

**5. Closure**

If the client remains inactive, the request is automatically closed.

---

## 🔐 Request Tracking

The system uses unique request identifiers to connect information between the different stages of the workflow.

Example:

```text
request_id
REQ-1788869588841

request_id2
[Generated for follow-up process]
```

This allows the automation to distinguish between different client requests and maintain the relationship between the initial request and subsequent scheduling attempts.

---

## 🚀 Why This System?

Many businesses lose potential clients because inquiries are received but never properly followed up.

This system turns that manual process into an automated workflow that:

* Captures every request
* Organizes client information
* Communicates automatically
* Tracks scheduling progress
* Follows up with inactive clients
* Reduces manual administrative work
* Prevents leads from being forgotten

The goal is to create a **reliable, repeatable client management process** that can be adapted to different businesses and services.

---

## 📂 Project Structure

```text
Automated-Client-Management-Follow-Up-System/
│
├── README.md
├── workflow/
│   └── n8n-workflow.json
│
└── screenshots/
    └── workflow.png
```

> Workflow files and screenshots can be added depending on the version of the project published in this repository.

---

## 🛠️ Built With

**Automation:** n8n
**Database:** Supabase
**Forms:** Google Forms
**Data Tracking:** Google Sheets
**Email Automation:** Gmail

---

## 📌 Project Status

🟢 **Completed**

The core client intake, scheduling, follow-up, tracking, and closure automation is implemented and ready to be demonstrated.

---

### 👨‍💻 Automation Studio

Built as an automation system designed to streamline client management and follow-up processes.

