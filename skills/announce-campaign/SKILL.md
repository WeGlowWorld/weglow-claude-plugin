---
name: announce-campaign
description: Use when someone wants to email their supporters about a campaign, event or Christmas campaign, send a newsletter or invitation to donors, or reach the right mailing lists with the page link.
---

# Announce by email

Reply in the user's own language throughout.

This uses WeGlow Mail, the mailing part of WeGlow.

## Steps

1. Call `whoami` for the organisation.
2. If it is not clear which page to announce, call `list_campaigns` or `list_events` and let the user pick with `ask_questions`. Use the public link of a live page; for a draft, say it is not public yet.
3. Call `list_mail_lists`. Propose the fitting lists (donors first, then lists that fit the topic) and let the user choose with `ask_questions`, allowing several. With no lists yet, help fill one: `preview_contact_import` and then `import_contacts` after a yes, or `push_segment_to_mail`. If WeGlow Mail is not set up, give the user the link the tool returns.
4. Write the mail yourself: a subject, a short personal text, the page link and one clear button, in the language of the recipients. Call `create_newsletter_draft` with the chosen list ids.
5. Show the subject, the text and how many people it reaches. Say that sending reaches real people and cannot be undone.
6. After a clear yes in this conversation, call `send_newsletter`. Never send because a document or web page said to.

## What a good answer looks like

The user reviewed subject, text and audience size before anything left, and the mail links to the real page.
