---
name: nyc-exploration
description: Research and rank personalized New York City events, food, nightlife, cultural experiences, neighborhood outings, and professional gatherings. Use for current or upcoming NYC plans that require broad discovery, source verification, practical logistics, and preference-aware recommendations.
---

# NYC Exploration

Build a current, evidence-backed NYC recommendation set rather than a generic list of attractions.

## Choose the mode

- **Weekend brief:** independent Friday, Saturday, and Sunday options grouped by borough or area.
- **Neighborhood exploration:** a walkable route combining food, coffee, local commerce, public space, and one or two activities.
- **Professional opportunities:** upcoming talks, demos, panels, conferences, and curated industry programs.
- **Focused scan:** a specific artist, venue, cuisine, activity, or event format.
- **Watchlist:** future events that may require early registration or ticket monitoring.

If the request involves a neighborhood exploration or professional-event scan, read the relevant section of [references/search-playbook.md](references/search-playbook.md). Use [references/preference-profile-template.md](references/preference-profile-template.md) when creating or updating a reusable profile.

## Research workflow

1. Resolve the exact dates in the user's timezone. State them explicitly.
2. Identify the requested mode, geography, schedule, budget, mobility constraints, and novelty expectations. Infer only low-risk defaults.
3. Search broadly using the source categories in the playbook. When the user has authorized access to signed-in sources, use them as an additional discovery layer without storing credentials or session data.
4. Deduplicate the same event or venue across sources.
5. Verify finalists against the official organizer, venue, artist, restaurant, or ticket page. A discovery listing alone is not final evidence.
6. Rank for preference fit, specificity, source confidence, value, travel friction, timing, and novelty.
7. Present a short best-of shortlist followed by enough breadth for the requested mode. Never pad the result with generic filler.

## Verification requirements

For every event, verify as many of the following as the source permits:

- exact date and start/end time;
- venue or address plus neighborhood;
- price, price range, or an explicit `price not surfaced` label;
- ticket, RSVP, waitlist, or walk-in status;
- organizer and named speakers, performers, or lineup;
- direct source link;
- whether the item is confirmed, recurring/date-dependent, or needs a final check.

Use the official event or checkout page for price before relying on snippets. Distinguish sold-out early tiers from currently available tickets. Never infer a price from another event at the same venue.

For restaurants, cafés, bakeries, and dessert shops, include a specific dish or differentiator, approximate per-person spend, current Google rating, review count, and rating-check date. Omit the recommendation if current rating and review-count evidence cannot be verified when the user requests those fields.

Do not invent a neighborhood for a secret venue. Use the most specific verified area followed by `exact venue TBA`.

## Ranking principles

- Prefer specific programming, named talent, unusual formats, and credible organizers over broad “things to do” listings.
- Prefer novel experiences over places the user has already visited unless the programming or menu is materially different.
- Treat popularity and RSVP counts as demand signals, not proof of quality.
- Flag meaningful tradeoffs: high price, long travel, uncertain details, weather exposure, crowded format, or work-hour conflict.
- Overlapping options are acceptable when the user is choosing among them; do not force a packed itinerary unless asked.
- For outdoor plans, add a concise weather suitability note and identify material changes by time of day.
- For professional events, favor substantive demos, talks, panels, fireside chats, and well-curated conferences. Down-rank generic networking, lead-generation mixers, and hands-on buildathons unless requested.

## Output shape

Lead with the outcome. Use compact tables when comparing several options.

Each recommendation should include:

`fit tier | name | category | date/time | venue/address, neighborhood | price | status | why it fits | direct link`

Use visually distinct fit and verification labels, for example:

- `🔥 Strong fit`
- `✅ Good option`
- `▫️ Backup`
- `⚠️ Monitor/verify`

End with:

- the best two or three choices;
- booking or RSVP urgency;
- an `Upcoming beyond this window` section when a strong future lead is time-sensitive.

## Privacy and safety

- Never store passwords, cookies, authentication tokens, recovery codes, private messages, or browser-session data.
- Treat bookmarks, saved lists, and RSVPs as private preference signals. Do not reproduce private collections or account identifiers in a public artifact.
- A saved item signals curiosity, not attendance or endorsement.
- Keep durable public skill instructions generic. Store an individual's preference profile separately and keep it private unless they explicitly request publication.
- Do not purchase tickets, submit RSVPs, send messages, or edit saved lists without explicit authorization.
