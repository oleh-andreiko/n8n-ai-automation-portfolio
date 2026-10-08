# Ticket routing & SLA escalation

A customer email becomes a ticket with a category, priority and owner. If nobody reacts in time, the escalation goes up the chain: owner → team lead → director.

📖 Case study: [Notion](https://app.notion.com/p/37ff44069e9d81a7bb86cd3d7a6f645e)

## Problem

Requests were sorted by hand, 2–5 minutes each. Missed deadlines were noticed late, and repeated alerts spammed the team.

## How it works

1. **Routing:** AI (GPT-4o-mini) reads the request and sets the category, priority and owner. The SLA timer starts.
2. **Escalation:** on a timer, overdue tickets go up three levels via Telegram and Gmail. Each alert is sent once.

## Results on demo data

| Metric | Before | After |
|--------|--------|-------|
| Ticket sorting | 2–5 min | **3–5 sec** |
| Duplicate alerts | frequent | **0** |
| SLA control | manual | **automatic, 3 levels** |
