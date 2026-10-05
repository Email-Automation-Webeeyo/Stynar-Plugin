---
name: stynar-outreach
description: Build and launch a cold email campaign with Stynar — find prospects, reveal their work emails, write the email, and send it from the user's own mailbox. Use when the user wants leads or a prospect list, wants outreach or cold emails written or sent, or wants to start, pause or set up a Stynar campaign.
---

# Cold outreach with Stynar

Work through these steps in order. Stop and ask whenever the user hasn't decided something that affects who gets emailed, what it costs, or what the email says.

## 1. Check the account

Call `get_account_overview` first.
- Note the credit balance — Lead Finder and sending both spend credits.
- Check for at least one **verified** sender. If there is none, tell the user to connect a mailbox on Stynar's Email accounts page before going further; a campaign can't start without one.

## 2. Pin down who to reach

Agree on the ideal customer before searching: job titles or seniority, department, location, company size, industry. Turn rough terms into exact filter values with `suggest_filter_values` (free) — for example a city or an industry name.

## 3. Find people — confirm the cost

`find_leads` costs **1 credit per results page** (refunded if a page comes back empty). Run page 1, show the user a short table (name, title, company, location), and ask before fetching more pages.

Emails are masked at this stage. That's expected.

## 4. Save the chosen people — confirm the cost

`save_leads` reveals verified work emails: **1 credit per email**, plus **9 per mobile number** only if the user asks for mobiles. Say the number before calling, e.g. "Saving these 18 people will use up to 18 credits."

Always pass name, company and title for each person, and a clear label such as `Heads of Marketing – Bengaluru – Oct`. People already unsubscribed, bounced or contacted by this user are skipped and not charged.

## 5. Write the email

Write it yourself — don't ask the user to.
- **Short:** 50–120 words, one idea, one clear ask (a reply or a quick call).
- **Specific:** open with something relevant to the recipient's role or company, not with "I hope this finds you well".
- **Plain:** no images, no attachments, at most one link, and no ALL-CAPS or "free!!!" — they hurt deliverability.
- **Subject:** 2–6 words, lowercase-friendly, no clickbait.
- **Personalisation:** `{{firstName}}` is always set on saved leads. `{{company}}` and `{{jobTitle}}` are set only when the search result had them, so use them only if every person you saved shows one. A lead missing a variable used in the email is skipped at send time.

Show the draft and adjust it until the user is happy.

## 6. Build the campaign

1. `create_campaign` with the name, subject and body. This only creates a draft.
2. `add_leads_to_campaign` with `savedLeadsLabel` set to the label from step 4.
3. `get_campaign_report` to confirm the lead count and how the email reads in Stynar.

## 7. Launch — only on an explicit yes

Before calling `start_campaign`, show this summary and wait for a clear "yes, send it":
- Campaign name
- Sending account(s)
- Number of recipients
- The full subject and body
- That sending uses credits per email and can't be undone once emails go out

If the user hesitates, leave it as a draft — they can review it in Stynar. `pause_campaign` stops further sends at any time.

## Rules

- Never spend credits or send email without the user's go-ahead in this conversation.
- If a tool reports insufficient credits, tell the user and stop. Don't retry or work around it.
- Stynar handles unsubscribe links, suppression and sending limits. Don't promise the user anything beyond that.
