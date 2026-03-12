# CampaignMgr ⚡
### Instantly × GoHighLevel × Claude AI

A full-stack outreach management dashboard with live integrations:
- 📧 **Gmail** — send & read emails via Google MCP
- 📅 **Google Calendar** — schedule meetings via Google MCP
- ⇄ **GoHighLevel** — contact sync & AI enrichment
- ⟳ **Instantly API** — live campaign & account data
- ✦ **Claude AI** — AI-powered email copywriting
- ⚡ **n8n Workflows** — automation monitoring & triggering

---

## Local Development

```bash
# 1. Install dependencies
npm install

# 2. Create your .env file
cp .env.example .env
# Then edit .env and add your ANTHROPIC_API_KEY

# 3. Start dev server
npm run dev
```

Open http://localhost:5173

---

## Deploy to Vercel

1. Push this repo to GitHub
2. Go to vercel.com → **Add New Project** → select this repo
3. In **Environment Variables**, add:
   - `ANTHROPIC_API_KEY` = your Anthropic API key
4. Click **Deploy** — done in ~60 seconds

---

## Project Structure

```
campaignmgr/
├── api/
│   └── claude.js        # Vercel serverless function (keeps API key secret)
├── public/
│   └── favicon.svg
├── src/
│   ├── App.jsx          # Main dashboard (all pages & integrations)
│   └── main.jsx         # React entry point
├── .env.example         # Copy to .env and fill in keys
├── .gitignore
├── index.html
├── package.json
├── vercel.json
└── vite.config.js
```

---

## Environment Variables

| Variable | Description |
|---|---|
| `ANTHROPIC_API_KEY` | Your Anthropic API key from console.anthropic.com |

> ⚠️ Never commit your `.env` file. The `.gitignore` already excludes it.
