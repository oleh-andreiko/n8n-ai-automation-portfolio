# DentaLine: AI front desk for a dental clinic

An AI assistant in Telegram answers patients from the clinic's own documents, books them only into free slots, and hands the booking to the front desk for one-tap confirmation.

📖 Case study with a demo video and screenshots: [Notion](https://app.notion.com/p/3e5f44069e9d81f095f2dafa4da4e1cb)

## How it works

Nine workflows:

- **Knowledge base:** prices and answers come from the clinic's Google Docs, indexed into Qdrant (RAG).
- **AI assistant:** Claude with tools: searches the knowledge base, checks free slots in Google Calendar, books.
- **Front desk bot:** a separate Telegram bot where the administrator confirms or moves a booking with one tap.
- **Reminders and follow-ups:** a reminder before the visit, a rating request after it, a recall for the next cleaning.
- **Patient card:** a small CRM in PostgreSQL.

Qdrant and PostgreSQL run locally in Docker.

## Results on demo data

| Metric | Value |
|--------|-------|
| Patient gets an answer | **in seconds, 24/7** (without the bot: next morning) |
| Cost of one dialog | **~10 UAH** |
| Bookings | only into free calendar slots, confirmed by a person |
