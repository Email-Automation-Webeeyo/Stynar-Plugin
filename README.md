# Stynar

Run cold email outreach from Claude or ChatGPT with your Stynar account: find B2B prospects in a licensed people database, reveal verified work emails, write and launch campaigns that send from your own mailbox, track results, and answer replies.

## What's inside

- **Stynar connector**: a remote MCP server at `https://mcp.stynar.com/mcp`. It covers your account overview, campaigns, Lead Finder, saved leads, replies and meetings.
- **Skills**:
  - `stynar-outreach` walks through finding leads, writing the email and launching it.
  - `stynar-replies` sorts and answers prospect replies.
  - `stynar-campaign-report` reads results against benchmarks.

## Use it

1. Add the plugin, then connect Stynar. You'll sign in to Stynar and choose whether the assistant can only view your data or can also make changes.
2. Ask in plain words, for example:
   - "Find heads of marketing at SaaS companies in Bengaluru."
   - "How did my campaigns do this month?"
   - "Go through my new replies and draft answers."

The assistant always tells you the credit cost before searching or revealing emails. It always shows you the email, the sending mailbox and the number of recipients, and waits for your yes, before anything is sent.

You need a Stynar account with a connected sending mailbox to run campaigns. Lead Finder and sending use the credits on your Stynar plan.

## Data

The plugin sends your requests and the data they need to your Stynar account through `mcp.stynar.com`. That covers search filters, lead details, email content and replies. The plugin itself stores nothing. Stynar processes it under its [privacy policy](https://stynar.com/privacy).

To disconnect at any time, go to **Settings → API keys → Connected AI apps** in Stynar. Disconnecting revokes access immediately.

## Support

support@stynar.com · https://stynar.com/support
