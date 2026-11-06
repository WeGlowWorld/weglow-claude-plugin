---
name: board-report
description: Use when someone needs a report for the board or general assembly, a summary of results for a period, a year-end overview of income and gifts, or figures for a funder or annual report.
---

# Board report

Reply in the user's own language throughout.

Needs the WeGlow CRM. If the tool says it is not available, tell the user so in plain words.

## Steps

1. Call `whoami` for the organisation.
2. Ask with `ask_questions` for the period (this year, last year, a quarter, a month, or a date range), who the report is for, and whether notes should be added.
3. Optionally call `show_dashboard` or `get_insights` first, so the user sees the headline figures.
4. Call `create_board_report`. It compares income with the same period last year and covers gifts and givers, members, volunteers and major gifts, saved in the CRM and returned as a shareable link with a PDF.
5. If a narrative helps, write a short one in plain text. Every number in it must be one of the report's own figures; do not add others.
6. Give the user the link and say what the report contains and which period it covers. Mention if a figure looks surprising so the user can check it before sharing.

## What a good answer looks like

The user gets a link and PDF, a short narrative that uses only the report's figures, and no donor personal data in the chat.
