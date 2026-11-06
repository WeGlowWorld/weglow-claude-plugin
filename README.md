# WeGlow for Claude

This plugin teaches Claude how to help a non-profit raise money with
[WeGlow](https://weglow.world), a fundraising platform for non-profits. It adds
ten skills that walk Claude through the common jobs: starting a campaign, a
Christmas campaign, an event, a donation page for monthly givers, a donation form
for your own website, setting up your organisation, thanking donors, a weekly
check-in, announcing a campaign by email, and a report for your board. Two
shortcut commands, `/weglow:weekly-report` and `/weglow:thank-this-week`, start
the two jobs people repeat most.

## How to use it

1. Install the plugin and sign in to WeGlow when Claude asks. You sign in with
   your own WeGlow account and only see organisations you manage.
2. Describe what you want in your own words, for example "we want a Christmas
   campaign for our youth club" or "what should we do this week?". Claude picks the
   matching skill and works in your language.
3. Claude builds everything as a draft first and shows you the real page in the
   chat. Nothing is published, activated or emailed until you say yes.

## What it sends, and where

The plugin itself is plain text: skills and one connector setting. It has no code
and stores nothing. The connector setting (`.mcp.json`) points Claude at
`https://mcp.weglow.world`, WeGlow's own server. When you ask for something,
Claude sends the request details to that server, such as the title and story of a
campaign, and gets WeGlow data back. Donor names, emails and gifts per person are
only visible to Claude when a manager of your organisation has switched that on in
WeGlow; totals are always available. See https://weglow.world for WeGlow's privacy
policy.

## Trademark and licence

The text in this repository is released under the MIT licence (see `LICENSE`).
The WeGlow name and logo are reserved and are not covered by that licence.
