---
name: christmas-campaign
description: Use when someone wants a Christmas, advent or year-end fundraising campaign, or asks for a festive way for supporters to give, such as a Christmas tree, a starry sky, presents or a wall of cards that fills up as people donate.
---

# Christmas campaign

Reply in the user's own language throughout.

A Christmas campaign is a campaign with an interactive scene that fills as donors give. It keeps the WeGlow style, so only the organisation's brand colours, texts and images change.

## Steps

1. Call `whoami` for the organisation (ask which one if there are several; offer `create_organization` if there is none).
2. Call `list_christmas_scenes` so the user sees the scenes as pictures. Then call `ask_questions` once: which scene fits, and the goal amount if it was not given. Put your recommended scene first.
3. If the user shares a photo, store it with `upload_image` or `request_files` and use the returned URL. Without one, the scene's own cover is used.
4. Write the title, a warm and seasonal story of two to four sentences, and the thank-you mail yourself, in every language the organisation uses. Use `get_benchmarks` for a realistic goal when the user is unsure, and say so when there is no data.
5. Call `create_christmas_campaign`. Adjust with `update_campaign_draft` if needed.
6. Show the real page with `show_campaign_preview` and the `open_in_weglow` link. Ask whether to publish.
7. After a clear yes, call `publish_campaign`. If the organisation is not live yet, follow the setup-organisation skill.
8. When it is live, call `get_share_kit` for posts, and offer a Christmas mail to supporters (announce-campaign).

## What a good answer looks like

The user sees a finished-looking Christmas page in the chat within a few messages, with the scene they chose, and knows nothing is public until they said yes.
