---
name: plan-event
description: Use when someone wants to organise a charity event such as a run, a walk, a quiz night, a dinner or a concert, whether people buy tickets, raise money with their own page, or both.
---

# Plan an event

Reply in the user's own language throughout.

An event can be open (anyone joins and raises money with their own action page, like a run or a walk) or closed (a dinner or quiz with tickets). Read `references/event-types.md` for how to decide.

## Steps

1. Call `whoami` for the organisation.
2. Ask what you cannot decide with one `ask_questions` call (at most four questions): the kind of event, the date, the place, tickets or personal action pages, and the goal. Event dates have no time of day unless the user gives one.
3. Call `get_benchmarks` with kind `event` and `fundraising_advice` to suggest a realistic goal and what makes this kind of event work. Say plainly when there is not enough data.
4. Write the title and description yourself in every language the organisation uses, then call `create_event_draft`.
5. For tickets, call `create_ticket_types` (a name, a price, 0 for free, and optionally how many and until when). For events where supporters raise money themselves, call `create_fundraiser_template`.
6. Offer a look: `set_page_design` can change font, shape, light or dark and section order, or apply a preset (warm, gala, speels, sportief). Translate wishes like "square buttons" into the design.
7. Give the `open_in_weglow` link, say what still has to be finished in the WeGlow event builder (visuals, tickets), and ask whether to publish.
8. After a clear yes, call `publish_event`.
9. When it is live, call `get_share_kit` and write an invitation the user can send; offer to mail it (announce-campaign).

## What a good answer looks like

The draft event, tickets and (if relevant) the action page template exist, the user knows what is left to finish in the builder, and no invitation has gone out before they agreed.
