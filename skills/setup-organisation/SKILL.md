---
name: setup-organisation
description: Use when someone wants to create their organisation on WeGlow, finish setting it up so it can receive donations, add their logo and colours, connect payments, or finds that publishing fails because the organisation is not live yet.
---

# Set up the organisation

Reply in the user's own language throughout.

Read `references/go-live-checklist.md` for the order of the steps.

## Steps

1. Call `whoami`. If the user already manages an organisation, continue at step 4.
2. With no organisation yet: ask for the name, the country and the main language (one `ask_questions` call). Show the data processing agreement the tool provides and ask the user to accept it. Only then call `create_organization`. Everything created afterwards starts as a draft.
3. Right after creating it, ask with `ask_questions` how to get the look: from their website (`import_branding_from_website`), uploading their logo (`request_files`), a brand guide attached in the chat, or later.
4. For a website: show the logo and colour suggestions. After the user chooses, store the logo with `upload_image`, set it with `update_organization_profile`, and call `apply_brand_colors` only after they agree to the colours. For a brand guide (PDF): read it, propose the colours and a one-sentence tone of voice, and apply them only after a yes.
5. Call `get_setup_status` and help with each missing step in plain words: a description of at least 80 characters (write a proposal from what you know and let the user adjust it), the billing address, then payments.
6. For payments, call `connect_payments` and give the user the link. They connect on the payment provider's own site; you cannot do that for them. When they say they are done, call `get_setup_status` again. If the provider still needs something, point to the dashboard it names rather than creating a new link.
7. When the status says the organisation can go live, ask the user to confirm, then call `go_live`. For some payment providers the WeGlow team puts the organisation live by hand; say so when the tool reports it.
8. When it is live, suggest a first page: a campaign, a donation form for their website, or an event.

## What a good answer looks like

The user always knows which single step is next, in plain words, and nothing that affects real donors happens without their confirmation.
