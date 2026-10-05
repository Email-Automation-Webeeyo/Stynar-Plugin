---
name: stynar-campaign-report
description: Report how the user's Stynar email campaigns are performing and what to change. Use when the user asks how a campaign is doing, wants open/reply/bounce numbers, a weekly outreach summary, or advice on improving results.
---

# Stynar campaign performance

## 1. Pull the numbers

- `get_account_overview` for the last 30 days across all campaigns.
- `list_campaigns` to find the campaigns in question, then `get_campaign_report` for each one. It returns the send pipeline (pending, sent, failed…) and engagement with rates already calculated.

## 2. Read them against these benchmarks

| Metric | Healthy | Worry when |
|---|---|---|
| Reply rate | 3–10% | below 1% after 100+ sends |
| Bounce rate | under 2% | above 3% — stop and clean the list |
| Open rate | 30–60% | treat as a rough signal only; privacy proxies distort it |
| Failed sends | ~0 | any growth — usually a sender connection issue |

Small samples mislead. Under ~100 sends, describe what you see without drawing conclusions.

## 3. Report

Lead with one sentence on how things are going, then a small table per campaign (sent, reply rate, bounce rate, meetings). Finish with at most three concrete suggestions, for example:
- High bounces → save leads again from Lead Finder rather than reusing an old list; pause the campaign meanwhile (`pause_campaign`, with the user's OK).
- Low replies with healthy opens → the email isn't landing. Offer a shorter rewrite with a more specific first line.
- Low opens → check the subject line and that the sending mailbox is verified.
- Replies waiting → offer to go through them (stynar-replies).

Don't change or restart anything without the user asking.
