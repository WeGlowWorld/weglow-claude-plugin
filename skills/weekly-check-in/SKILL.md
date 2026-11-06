---
name: weekly-check-in
description: Use when someone asks what to do this week for their fundraising, how they are doing, for a quick overview of results, or opens a conversation about their organisation without a specific task.
---

# Weekly check-in

Reply in the user's own language throughout.

Keep it short and concrete.

## Steps

1. Call `whoami` for the organisation.
2. Call `get_suggested_actions`. If the organisation is not live yet, `get_setup_status` says what is missing; that comes first (see setup-organisation).
3. For how they are doing, call `show_dashboard` to show the figures inside the chat, or `get_insights` and `get_fundraising_overview` for a comparison with last year. Quote only numbers these tools return.
4. Give at most three things to do this week, most impactful first. For each: why (the number behind it) and what you can prepare right now, for example a campaign update (`create_campaign_update_draft`), thanking donors (thank-donors), a message to people who gave last year but not yet this year (`find_lapsed_donors`), or a share kit (`get_share_kit`).
5. Offer to prepare the first one. Publish or send nothing without a yes.

## What a good answer looks like

Three items or fewer, each with a reason and a ready next step. Totals are fine; donor names only appear when the organisation allowed it.
