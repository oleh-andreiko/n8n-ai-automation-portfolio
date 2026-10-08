# n8n AI Automation Portfolio · Oleh Andreiko

**AI Automation** · n8n · AI agents · CRM integrations

I build AI automations on n8n that take routine work off people: incoming leads, calls, sales dialogs, support requests. When something fails, the system sends me a Telegram alert.

Every case below is an implementation on a real business scenario, tested on demo data. The numbers come from those demo runs. "Before" values are typical times for the same work done by hand. Screenshots and demo videos are in the [Notion portfolio](https://app.notion.com/p/336f44069e9d80429b19d73c05d365e5).

## Cases

| # | Case | Stack | Result on demo data |
|---|------|-------|---------------------|
| [01](./01-lead-qualification/) | **Lead qualification** | n8n, Claude Haiku 4.5, Zoho CRM, Google Sheets, Telegram, Klaviyo | Form → CRM and manager's Telegram in **< 1 min** |
| [02](./02-call-analytics/) | **Call analytics** | n8n, AssemblyAI, OpenAI, AI Agent, Google Sheets | Every call transcribed and scored, **< 2 min** per call |
| [03](./03-sales-ecosystem/) | **AI sales ecosystem (BANT)** | n8n, Claude Sonnet, Zoho CRM, PostgreSQL, Telegram | Qualification **15–20 min → 3–5 min**, CEO report generated automatically |
| [04](./04-ticket-routing-sla/) | **Ticket routing & SLA escalation** | n8n, GPT-4o-mini, Google Sheets, Telegram, Gmail | Ticket sorting **2–5 min → 3–5 sec**, **0** duplicate alerts |
| [05](./05-dentaline/) | **DentaLine: AI front desk for a dental clinic** | n8n, Claude Sonnet, Qdrant (RAG), PostgreSQL, Google Calendar, Telegram | Answers patients in **seconds, 24/7**, ~10 UAH per dialog |

## How the systems are built

- **Several workflows per system:** intake, processing, reporting and errors are separate, so one can be changed without breaking the others.
- **One error workflow:** any failure → Telegram alert with the step, error and time.
- **Structured AI output:** JSON schemas and output parsers, with a fallback when the model returns something unexpected.
- **No duplicates:** upserts on key columns, deduplicated alerts.
- **Chat memory:** PostgreSQL-backed memory for conversational agents.

I don't publish the workflow files. If you want details on any of these systems, message me on LinkedIn or Telegram.

## Contact

- **LinkedIn:** [linkedin.com/in/oleh-andreiko](https://www.linkedin.com/in/oleh-andreiko/)
- **Telegram:** [@aov_0](https://t.me/aov_0)
- **Email:** olegaiautomator@gmail.com
- **Portfolio with demos:** [Notion](https://app.notion.com/p/336f44069e9d80429b19d73c05d365e5)
