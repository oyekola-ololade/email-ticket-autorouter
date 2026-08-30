# Email Ticket Auto-Router

Classifies inbound support emails by priority and department with Claude, then files and confirms the ticket.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Claude (Anthropic API)](https://img.shields.io/badge/-Claude%20(Anthropic%20API)-333?style=flat-square) ![Ticketing system API](https://img.shields.io/badge/-Ticketing%20system%20API-333?style=flat-square) ![SendGrid](https://img.shields.io/badge/-SendGrid-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

**[Open the visual project page →](./index.html)**

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Demo status](#demo-status)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Overview

**Trigger:** Webhook (email ticket: subject, body, from)

Classifies inbound support emails by priority and department with Claude, then files and confirms the ticket.

### Key Features

- Priority + department classification in one call
- Fail-safe fallback ticket creation
- Automatic customer confirmation email

## Architecture

Open the [visual project page](./index.html#architecture) for the flow derived from the sanitized export.


## Workflow

1. Email ticket webhook receives the message
2. Parse subject, body, and sender
3. Claude classifies priority (urgent/normal/low) and department (sales/support/billing)
4. Create the ticket in the ticketing system and confirm by email
5. On classification failure, file a normal-priority fallback ticket instead

## Tech Stack

- n8n
- Claude (Anthropic API)
- Ticketing system API
- SendGrid

## Demo status

A configured live-run recording is not included yet. Credentials and service identifiers remain placeholders.


## Setup

1. Import `workflow/T10_Email_Ticket_AutoRouter.json` into your n8n instance (**Workflows → Import from File**).
2. Replace every placeholder credential/URL in the workflow (e.g. `YOUR_..._API_KEY`, `YOUR_..._URL`) with your own service credentials.
3. Activate the workflow and point the relevant integration (webhook source, scheduled trigger, etc.) at the generated webhook URL.
4. Test with a sample payload before going live.

## Repository Structure

```text
.
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── workflow/
    └── T10_Email_Ticket_AutoRouter.json
```


## Disclaimer

This workflow was built as a portfolio/template project to demonstrate n8n workflow automation and AI integration. API credentials and sensitive configuration have been removed before publication — replace all `YOUR_..._KEY` / `YOUR_..._URL` placeholders with your own before use.

---

Designed and engineered by

**Oyekola Ololade**

AI Systems & Integration Engineer

- LinkedIn: <http://linkedin.com/in/ololade-oyekola-5b1797397>
- Email: <oyekolaololade69@gmail.com>
