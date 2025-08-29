# Automated Market Intelligence Digest

This project automates the creation and distribution of a weekly market intelligence newsletter. It is designed to help product and strategy teams stay updated on competitor moves, industry shifts, and domain trends without obsessing over endless scrolling and manual collection.

The workflow uses **n8n** as the orchestration tool, combining multiple data sources with AI summarization to produce a clean, contextual digest delivered directly to your inbox or Slack channel.

---

## Features

* **Automated sourcing**: Pulls information from competitor tweets, research AI models, RSS feeds, APIs, social scrapers (Apify), and HTML scraping.
* **AI summarization**: GPT based prompts transform raw updates into short, contextual insights (1 sentence summary + 1 sentence why it matters).
* **Flexible distribution**: Digest can be delivered via Gmail, Slack, Notion, or any connected app.
* **Lightweight and modular**: Easy to adapt for new companies, industries, or domains.

---

## Tech Stack

* [n8n](https://n8n.io/) — workflow automation
* [OpenAI models](https://platform.openai.com/) — summarization and contextual insights
* \[RSS feeds] — easy structured updates
* [Apify](https://apify.com/) — social media and web scraping
* HTML scraping (fallback)
* Gmail or Slack for delivery

---

## Workflow Overview

1. **Trigger**: Manual or scheduled run in n8n.
2. **Source collection**: Fetch competitor tweets (via Apify), run market research AI, and pull RSS/API data.
3. **Merge and clean**: Deduplicate and filter inputs.
4. **Summarize**: Pass inputs through OpenAI with a prompt template to generate newsletter content.
5. **Format**: Convert Markdown into HTML and plain text.
6. **Distribute**: Send via Gmail (in this example) or push to Slack/Notion.

---

## Getting Started

### 1. Download the workflow JSON

Download the provided JSON file from this repository

### 2. Import workflow into n8n

* Open n8n
* Import the provided JSON workflow file

### 3. Configure credentials

* **OpenAI** API key
* **Apify** API key
* **Gmail** or Slack credentials

### 4. Adjust sources

* Update competitor profiles, company names, and feeds inside the workflow.

### 5. Run

* Trigger manually or set a schedule (e.g. weekly)
* Digest will be generated and sent automatically

---

## Example Output

```markdown
# Weekly Market Intelligence Newsletter

## Top 5 Moves
- Market size projections and growth trends with citations. [Source]
- Adoption of AI-powered features across the industry. [Source]

## Product & Pricing Changes
- Example of a product integration or feature update from tracked sources. [Source]

## What to Watch Next Week
- Forward-looking insights and regulatory updates in the sector. [Source]
```

---

## Lessons Learned

* **Start small**: Even two sources are enough to show value.
* **Context matters**: Summaries are only useful when tied back to your product or industry.
* **Distribution > dashboards**: Deliver updates where the team already works.

---

## Links

* Full article about the build: \[link-to-article]

