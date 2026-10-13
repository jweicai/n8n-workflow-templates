# n8n Automation Showcase ⚙️

Three import-ready n8n workflows — the kind I build for clients.
Import any `workflows/*.json` into your n8n instance
(**Workflows → Import from File**), fill in credentials, done.

## Workflows

### 1. Lead Capture → CRM Sync ([workflow](workflows/01-lead-capture-to-crm.json))
Your web form posts to a webhook; the lead is normalized (messy field names,
timezone-safe timestamp) and pushed to your CRM/API.
Never copy-paste a form submission again.

```
form submit → normalize fields → push to CRM
```

### 2. Price Watch → Telegram Alert ([workflow](workflows/02-price-watch-alert.json))
Checks a product/API every 6 hours. Only when the price drops below your
target, you get a Telegram message. Quiet otherwise — no notification spam.

```
every 6h → fetch price → below target? → yes: Telegram alert / no: skip
```

### 3. Daily Report → Email Digest ([workflow](workflows/03-daily-report-email.json))
Every weekday at 8:00 AM: pull yesterday's numbers from your API, format a
clean email (with trend emoji), send it. Your morning dashboard, in your inbox.

```
weekdays 8AM → fetch stats → format email → send
```

## Why these three

They cover the 90% of what small businesses ask for on Upwork:

| Client pain | Workflow |
|---|---|
| "I manually copy form submissions into my CRM" | #1 |
| "I keep checking this price myself" | #2 |
| "I want my numbers every morning without logging in" | #3 |

## What you get when you hire me

1. **A Loom walkthrough video** of your finished workflow — no call required
2. **Written setup doc** (credentials, env vars, how to edit it yourself)
3. **2 weeks of free fixes** after delivery

*Note: JSON files use placeholder URLs/credentials — import them, wire in
your real endpoints, and they're production-ready skeletons.*
