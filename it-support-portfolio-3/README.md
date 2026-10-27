# Fadil Nizar — IT Support Portfolio

**Target roles:** IT Support Tier 1, SaaS Technical Support, Implementation / Onboarding
**Location:** Mississauga, ON
**Links:** GitHub: github.com/Fadilniz | LinkedIn: linkedin.com/in/fadilnizar | Email: fadil@aira.company

## Summary
- Sheridan College graduate, Dec 2025, Computer Systems Technology — Software Development and Network Engineering
- Seeking a first IT support role in the GTA
- Lab and demo projects only, no paying clients, no production use
- Practice data only throughout this portfolio

## Technical Skills

- **Identity and administration:** Microsoft Entra ID, Microsoft 365, user lifecycle, Security groups, password resets, MFA re-registration
- **Support and ticketing:** Zendesk, incident triage, priority assignment, internal notes, escalation paths
- **Systems and networking:** Windows 11 troubleshooting, DNS, DHCP, Wi-Fi, VPN basics
- **Automation and APIs:** n8n, webhooks, REST APIs, Twilio, HubSpot basics
- **AI and retrieval:** OpenAI embeddings, Pinecone vector search, Google Drive document retrieval
- **Scripting:** PowerShell basics

## Projects

### Zendesk Ticket Simulation — Lab, Test Users Only
- **Stack:** Zendesk
- **Scope:** 5 tickets, all marked Solved
- **Ticket types:** POS terminal frozen mid-order, receipt printer offline, POS login locked out, card reader failing, menu price mismatch on POS vs menu board
- **Workflow per ticket:** intake, reproduction checks, fix or escalation, internal note, priority, Solved status
- **Next step:** expansion to 15-20 tickets, planned, not done yet

### n8n Appointment Booking Lifecycle — Demo, AIRA, No Paying Clients
- **Stack:** n8n, webhooks, Google Sheets, Google Calendar, Gmail
- **Size:** 20 nodes
- **Flow:** webhook request, availability check, Sheets record write, Calendar event write, Gmail confirmation, webhook response
- **Lifecycle covered:** book, availability check, update, cancel, delete
- **Known limits:** booking-confirmation timeouts, wrong-row Sheet updates in demo

### Multi-Tenant Call Concurrency — Demo, AIRA
- **Stack:** n8n, Twilio, HTTP calls
- **Size:** 25 nodes
- **Flow:** webhook request, tenant routing, concurrency check, overflow path when capacity is reached, webhook response
- **Design goal:** route and overflow under load instead of dropping calls

### Call Intake and Emergency Triage — Demo, AIRA
- **Stack:** n8n, Gmail, Google Calendar, AI agent, branching logic
- **Size:** 11 nodes
- **Flow:** webhook request, data capture, case-type branching, Calendar check, AI agent step
- **Scope note:** standalone Emergency Triage file is 2 nodes only, a routing piece inside intake, not a full system on its own

### RAG Knowledge Base — Demo, AIRA
- **Stack:** n8n, Google Drive, OpenAI embeddings, Pinecone, AI agent
- **Size:** 13 nodes, plus a memory workflow
- **Flow:** Drive trigger, document loading, text splitting, embedding generation, Pinecone storage, agent retrieval
- **Design:** retrieval-first answering, documents searched before an answer is generated

### Entra User Lifecycle — Lab, Completed Oct 26, 2026
- **Stack:** Microsoft Entra ID Free
- **Company:** Northline HVAC, not a real company
- **Scope:** 12 practice users, 3 Security groups, Assigned membership

| Group | Access |
| --- | --- |
| Office | Billing, schedules — no payroll |
| Technicians | Job sheets only |
| Dispatch | Assign jobs, schedules — no payroll |

- **Joiner:** created a practice user account, enabled account, assigned Office group, verified group membership
- **Mover:** moved the same user from Office to Dispatch, same login kept, verified access change in both groups
- **Password reset:** reset to a temporary password, change required on next sign-in
- **Leaver:** blocked sign-in, removed user from Dispatch, verified blocked status, account left blocked, not deleted, to preserve the record
- **Full write-up:** entra-user-lifecycle/README.md
- **Entra ID Free limits:** no Conditional Access, no Lifecycle Workflows, no Microsoft 365 licences, no mailbox administration, no paid Azure services

## Experience

### Food Service Supervisor — Harveys, Feb 2023 – Present
- Supervised 3-4 staff per shift
- Trained 4-5 new hires
- Handled around 400 orders per shift
- Triaged competing orders and issues by impact and urgency during peak periods
- Documented recurring POS issues for managers and handled guest escalations

## Education
- Sheridan College — Ontario College Advanced Diploma, Computer Systems Technology — Software Development and Network Engineering, Dec 2025

## Notes
- Northline HVAC is not a real company
- Zendesk requesters are test users only, no real customers, clients, or coworkers
- No raw n8n JSON published — exports contain real emails and credential references, descriptions only until a full redaction pass
