# Choosing the right WeGlow page

Do not default to a campaign. Match the request to the product, propose it in one sentence, confirm with `ask_questions` (your proposal first), then build it. When unsure, call `suggest_product` with the user's own words; it returns the product to propose and the tools to build it with.

| The user wants | Product | Build with |
| --- | --- | --- |
| One concrete goal with an amount | Campaign | `create_campaign_draft` |
| Christmas or year-end giving with an interactive scene | Christmas campaign | `list_christmas_scenes`, `create_christmas_campaign` |
| A run, walk, quiz, dinner, or anything with tickets, or many people raising money together | Event | `create_event_draft`, `create_ticket_types`, `create_fundraiser_template` |
| Monthly or regular givers, a permanent "support us" page | Donation page | `create_donate_page_draft` |
| A donate button or form on their own website | Donation form | `create_donation_form_draft` |

## What to ask for, per product

- Campaign: the cause, the goal amount, a photo if there is one.
- Christmas campaign: the cause, the goal, and which scene fits.
- Event: the kind of event, the date, the place, tickets (how many, what price) or action pages supporters start themselves, and the goal.
- Donation page: what a monthly gift makes possible, and which one-off and monthly amounts fit.
- Donation form: the website (to match its look), a form in the page or a button that opens it, and the amounts.
