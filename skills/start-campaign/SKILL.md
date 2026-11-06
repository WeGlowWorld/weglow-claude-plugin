---
name: start-campaign
description: Use when someone wants to raise money for one concrete cause with a goal amount, for example a new tent, a minibus, a project or an emergency, and wants a campaign page donors can give on. Also fits when they are unsure what kind of page they need and have not yet said event, monthly giving or website.
---

# Start a campaign

Reply in the user's own language throughout.

A campaign is one public page with a story, a goal amount and a photo. Build it as a draft in WeGlow, show it, and publish only after the user agrees.

## Steps

1. Call `whoami` to see which organisation the user manages. With several, ask which one. With none, offer `create_organization` (see the setup-organisation skill).
2. If it is not clear that a campaign is the right page, call `suggest_product` with the user's own words and read `references/choosing-a-product.md`. Propose one product in a sentence and let the user confirm with `ask_questions`.
3. Ask only what cannot be decided from the conversation: the cause, the goal amount, and whether there is a photo. Put these in one `ask_questions` call (at most four questions). Use `get_benchmarks` with kind `campaign` to say whether the goal is realistic, and say plainly when it has no answer.
4. Write the title, the story donors will read, the suggested amounts and the thank-you texts yourself, in every language the organisation uses and in its brand voice when `whoami` shows one. Use `fundraising_advice` for what makes a strong story. Leave out what you do not know instead of writing placeholders; improve the draft later.
5. If the user has a photo, store it first with `upload_image` (a link) or `request_files` (a file on their computer) and use the returned URL as the hero image.
6. Call `create_campaign_draft`. Change it afterwards with `update_campaign_draft`.
7. Show the real page in the chat with `show_campaign_preview`, and give the `open_in_weglow` link. Say what publishing will do, then ask whether to publish.
8. After a clear yes, call `publish_campaign`. If it fails because the organisation is not live yet, call `get_setup_status` and help with each missing step (see setup-organisation).
9. Once it is live, call `get_share_kit` and write posts for the channels the user uses, only from the facts it returns. Offer to announce it by email (announce-campaign).

## What a good answer looks like

- The draft exists in WeGlow and the user has seen the page, not a text version of it.
- The story is concrete: who benefits, what the money buys, what a typical gift does.
- The user knows what is still a draft and what happens at the moment they say yes.
