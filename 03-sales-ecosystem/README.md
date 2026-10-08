# AI sales ecosystem (BANT)

Three linked workflows: a chatbot qualifies leads 24/7 → the dialogs are analyzed daily → the CEO gets a weekly report in Telegram.

📖 Case study with a dialog example and demo video: [Notion](https://app.notion.com/p/368f44069e9d8165baedf3ac1314fad5)

## How it works

| Workflow | What it does | When |
|----------|--------------|------|
| Qualification chatbot | Claude talks to the lead and asks about budget, decision maker, need and timing (BANT). Scores the lead 0–100 and creates it in Zoho CRM | 24/7 |
| Dialog analysis | Reads the dialogs from PostgreSQL memory, finds where the bot lost a lead and what worked → Google Sheets | daily |
| CEO report | CRM numbers + dialog insights → short summary in Telegram: hot leads, top questions | weekly |
| Errors | Telegram alert on any failure | on event |

Details:

- **BANT score:** budget, authority, need, timing, 0–25 each. The lead never sees the score.
- **Memory:** PostgreSQL, the session ID is stored in the CRM lead.
- **Prompt injection:** I tested the bot with 5 attempts to break its instructions. It blocked all 5.

## Results on demo data

| Metric | Before | After |
|--------|--------|-------|
| Lead qualification | 15–20 min | **3–5 min** |
| Weekly CEO report | 1–2 h by hand | **automatic** |
| Hours | business hours | **24/7** |

A test run of the report on demo data: 11 leads, 6 hot, top-3 customer questions.
