# NYC Exploration

A reusable Codex skill for researching personalized New York City events and experiences across fragmented public and authorized sources.

The skill turns an open-ended request such as “What should I do in NYC this weekend?” into a verified, preference-aware brief with exact dates, neighborhoods, pricing, booking status, confidence, and direct sources. It also supports neighborhood exploration, professional-event discovery, focused artist or venue scans, and future watchlists.

## What this demonstrates

- Multi-source discovery across official calendars, event platforms, public listings, and optional authorized personal signals
- Verification of time, location, price, lineup, registration status, and source confidence
- Ranking based on fit, novelty, value, travel friction, timing, and weather
- Privacy-aware separation between a reusable public workflow and an individual's private preference profile
- Structured outputs that make comparison and booking urgency easy to understand

## Repository structure

```text
nyc-exploration/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── preference-profile-template.md
    └── search-playbook.md
```

`SKILL.md` contains the core workflow. The references provide mode-specific research guidance and a blank template for keeping personal preferences separate from the public skill.

## Privacy design

This repository intentionally contains no personal addresses, private account identifiers, browser data, saved-item history, attendance history, credentials, or individual preference profile. Authorized account access can be used during a search, but private data should remain outside the repository.

## Use

Install or copy the `nyc-exploration` folder into a Codex skills directory, then ask for a current NYC weekend brief, neighborhood exploration, professional-event scan, or focused search.

Example:

> Find distinctive NYC events for next weekend. Prioritize Brooklyn, include exact neighborhoods and current prices, and verify every finalist through an official source.
