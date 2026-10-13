# CLAUDE.md: stynar-plugin

Public Stynar plugin for Claude / ChatGPT (MCP). This repo is public: keep internal details out of commits. Part of Stynar (AI cold-email outreach SaaS). Each Stynar service/app is its own git repo.

## Issue tracking: Linear

All work is tracked in Linear, workspace **stynar**, team **Stynar** (issue keys `STYNAR-123`). Use the Linear MCP tools. If they aren't available, ask the developer to connect Linear: `claude mcp add --transport http linear https://mcp.linear.app/mcp --scope user`, then `/mcp` → linear → Authenticate.

### When you find a bug
- Search Linear first (`list_issues` with a query) so you don't file a duplicate. If one exists, comment on it instead.
- Otherwise create an issue in team **Stynar**:
  - **Title:** short and specific, e.g. "Campaign wizard loses leads when switching tabs".
  - **Label:** `Bug` (or `Improvement` / `Feature` for non-bugs).
  - **Priority:** Urgent = prod down, data loss or security; High = a core flow broken; Medium = broken with a workaround; Low = cosmetic.
  - **Description:** steps to reproduce, expected vs actual, error text or logs, the repo/service and file (`path:line`) or page URL, and the environment (local, dev or prod).
  - **Project:** add it to the current release project (e.g. "Release 2.0.0") when it belongs to that release.
- Never paste secrets, API keys, tokens, passwords or customers' personal data into Linear.
- Tell the developer the new issue ID.

### When you work on an issue
- Starting: move it to **In Progress** and assign it to the developer you are working with (if it has no assignee).
- Put the ID in the branch name and commit message, e.g. branch `stynar-217-multi-company-leads`, commit `fix(campaigns): handle multiple companies (STYNAR-217)`. GitHub then links them automatically.
- Ready for review or deployed to dev: move it to **In Review**, with a comment on what changed and how to test it.

### When it is fixed
- Move it to **Done** only after the fix is committed and its tests pass. Add a comment with the commit/PR link, a one-line summary of the fix, and where it is deployed (dev/prod).
- Never mark an issue Done if its tests fail or the fix is unverified: leave it In Progress and comment on what's missing.
- Use **Duplicate** or **Canceled** (with a reason) instead of deleting issues. Never delete issues.

### Statuses
Backlog → Todo → In Progress → In Review → Done (plus Canceled, Duplicate).
