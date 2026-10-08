# Call analytics

Call recordings land in a Google Drive folder. Each one is transcribed, analyzed by AI and written to a table with a summary, sentiment, category and score.

📖 Case study: [Notion](https://app.notion.com/p/336f44069e9d8077b953c8de77332380)

## Problem

Managers listen to a small sample of calls. The rest go unchecked.

## How it works

Three workflows around a processing queue:

1. **Intake:** new audio files from Google Drive are added to the queue.
2. **Processing:** AssemblyAI speech-to-text → AI analysis (summary, sentiment, category, score) → results in Google Sheets, with the cost of each call.
3. **Queue errors:** a failed call is marked in the queue and I get an alert.

## Results on demo data

| Metric | Value |
|--------|-------|
| Calls analyzed | **100%** instead of a sample |
| Time per call | **< 2 min** |
| Cost per 1–2 min call | AssemblyAI ~$0.003–0.007 + OpenAI ~$0.0001 |

Next version in progress: AI quality control of sales calls against 8 criteria, with a Telegram alert for weak calls.
