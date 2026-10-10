# Stynar

Run B2B prospecting and cold email outreach from ChatGPT with your Stynar account. Search a licensed people database, reveal verified work emails, create campaign drafts from your own mailbox, track results, and review prospect replies. Stynar is a standalone sales engagement platform; this plugin does not connect to Apollo or Instantly accounts.

Looking for a comparison? See [Stynar vs Apollo](https://stynar.com/alternatives/apollo) and [Stynar vs Instantly](https://stynar.com/alternatives/instantly). Those pages compare separate products; they do not describe integrations.

## What's inside

- **Stynar connector**: a remote MCP server at `https://mcp.stynar.com/mcp`. It covers your account overview, campaigns, Lead Finder, saved leads, replies and meetings.
- **Skills**:
  - `stynar-outreach` walks through finding leads, writing the email and launching it.
  - `stynar-replies` sorts and answers prospect replies.
  - `stynar-campaign-report` reads results against benchmarks.

## Use it

1. Find Stynar in the ChatGPT app directory after the public listing is published, add it, then connect your Stynar account. You'll sign in to Stynar and choose whether the assistant can only view your data or can also make changes.
2. Ask in plain words, for example:
   - "Find heads of marketing at SaaS companies in Bengaluru."
   - "How did my campaigns do this month?"
   - "Go through my new replies and draft answers."

Lead searches, email reveals, and sending may use Stynar credits. The assistant should state the expected cost before a paid action. Before sending a campaign or reply, review the email, sender, recipients, and cost and explicitly approve the send.

You need a Stynar account with a connected sending mailbox to run campaigns. Lead Finder and sending use the credits on your Stynar plan.

## Data

The plugin sends your requests and the data they need to your Stynar account through `mcp.stynar.com`. That covers search filters, lead details, email content and replies. The plugin itself stores nothing. Stynar processes it under its [privacy policy](https://stynar.com/privacy).

To disconnect at any time, go to **Settings → API keys → Connected AI apps** in Stynar. Disconnecting revokes access immediately.

## Support

support@stynar.com · https://stynar.com/support
