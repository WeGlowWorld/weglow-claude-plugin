---
name: monthly-donation-page
description: Use when someone wants regular or monthly givers, a permanent "support us" page for general gifts that is not tied to one campaign, or a donation page in their own look and feel.
---

# Donation page for monthly givers

Reply in the user's own language throughout.

A donation page is the organisation's own page for one-off and monthly gifts. It can follow the organisation's look closely.

## Steps

1. Call `whoami` for the organisation.
2. Ask with `ask_questions` only what you cannot decide: what a monthly gift makes possible, and a photo if there is one (store it with `upload_image` or `request_files`).
3. Write the title, a short story about what a monthly gift makes possible, and the thank-you texts in every language the organisation uses. Suggest one-off amounts and monthly amounts, each with a line on what it pays for. Do not invent impact figures; use only what the user told you.
4. Call `create_donate_page_draft`, then show it with `show_donate_page_preview`.
5. Ask how it should look and propose a preset that fits (warm, gala, speels or sportief) with `ask_questions`. Apply wishes with `update_donate_page_draft` or `set_page_design`.
6. Publishing a donation page happens in WeGlow itself. Give the `open_in_weglow` link when the user is happy, and explain the last step in plain words.

## What a good answer looks like

The user has seen the real page, with amounts that each say what they pay for, and knows the one step left to go public.
