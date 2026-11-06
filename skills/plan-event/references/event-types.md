# Event types

- Open event: anyone can join and starts their own action page ("I run for ..."). Fits a run, a walk, a cycling day. Create the event with `create_event_draft` and the page supporters start from with `create_fundraiser_template`.
- Closed event: a dinner, a quiz, a concert. People buy tickets. Create the event, then `create_ticket_types`.
- Both: tickets for participation plus action pages for sponsoring. Combine the tools above.

After publishing, `get_event_stats` shows ticket sales and `list_event_attendees` shows attendees (names only when the organisation allowed donor data to be seen).
