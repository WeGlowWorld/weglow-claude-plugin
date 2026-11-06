---
name: website-donation-form
description: Use when someone wants people to donate on the organisation's own website, such as a donate button, a donation form embedded in a page, or the code to paste into their site.
---

# Donate button or form on your own website

Reply in the user's own language throughout.

## Steps

1. Call `whoami` for the organisation.
2. If the user gave a website, call `import_branding_from_website` so the form matches its look, and show the suggested logo and colours. Apply colours with `apply_brand_colors` only after the user agrees.
3. Ask with `ask_questions` whether it should be a form inside the page or a button that opens it, and which amounts fit.
4. Write the title, the text and the thank-you texts in every language the organisation uses.
5. Call `create_donation_form_draft`. It is inactive and comes with an embed code. Give the user the code with one sentence on where to paste it (for most site builders, an "embed" or "custom HTML" block). Change look and text with `update_donation_form_draft` or `set_page_design`.
6. Ask whether to activate it. After a clear yes, call `activate_donation_form`.

## What a good answer looks like

The user has the embed code, knows where it goes, and the form is only active once they said yes.
