---
name: thank-donors
description: Use when someone wants to thank donors, asks who gave recently, wants to know which gifts have not been thanked yet, or wants to send the organisation's thank-you mail or write a personal word to a generous donor.
---

# Thank donors

Reply in the user's own language throughout.

## Steps

1. Call `whoami` for the organisation.
2. Call `list_unthanked_gifts`: how many gifts were not thanked yet, the total, and where they came in. Names and individual gifts appear only when the organisation allowed donor data to be seen. If the user wants names, call `get_donor_data_access`, explain what it says in plain words, and use `request_donor_data_access` to show where a manager can switch it on. You cannot switch it on yourself.
3. Give a short overview and point out what stands out when it is visible (a first-time donor, a large or repeated gift).
4. `send_thank_you_mails` sends the organisation's own thank-you mail to real people. Tell the user how many people will get a mail and wait for an explicit yes before calling it. Gifts without an email address, already thanked, or from deceased donors are skipped. If the user wants different wording, improve the thank-you text first with `update_thank_you_content`, show it, and apply it with `apply_thank_you_content` after a yes.
5. For donors who deserve a personal word, draft a short message the user can send themselves. Use only what the user can see about that donor.

## What a good answer looks like

The user sees the overview first, knows exactly how many mails will leave, and nothing is sent before they said yes. Donor details are used only as far as the organisation allowed.
