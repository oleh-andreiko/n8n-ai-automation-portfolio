# Lead qualification

A lead fills in a form on the website. Within a minute it is scored by AI, saved in the CRM, and the manager gets it in Telegram.

📖 Case study with demo video: [Notion](https://app.notion.com/p/336f44069e9d800e825ae6a71498e624)

## Problem

Requests from the site were handled by hand, up to 30 minutes each. Hot leads waited in the same queue as cold ones, and some got answered too late.

## How it works

Webhook from the form → data cleanup → AI scoring with Claude Haiku 4.5 (hot / warm / cold + a short reason) → four branches at once:

1. **Zoho CRM:** a new lead with the AI score in the description.
2. **Google Sheets:** a log of every request.
3. **Telegram:** an instant message to the manager with the score.
4. **Email list:** warm and cold leads go to a separate list for nurturing (Klaviyo segments in the first version).

Any failed step sends me a Telegram alert with the step, error and lead.

## Results on demo data

| Metric | Before | After |
|--------|--------|-------|
| Request → CRM and manager | up to 30 min | **< 1 min** |
| Lost requests | some answered late | **0** |
| Sorting hot / warm / cold | none | **automatic** |
| Hours | business hours | **24/7** |
