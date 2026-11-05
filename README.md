# Trading workspace

This repo holds the 11 investing skills from [trader-skill](https://github.com/Jakeschincariol/trader-skill)
(MIT, by Jake Schincariol). They're in `.claude/skills/`, so every Claude Code session here loads
them, including cloud sessions, which don't install plugins from project settings.

| command | what it does |
| --- | --- |
| `/trader-copycat` | Rebuilds a famous investor's portfolio from their 13F filing |
| `/trader-news` | Watches headlines and SEC 8-K filings for the stocks you hold |
| `/trader-budget` | Sizes each position to your budget, with a cash buffer and a per-stock cap |
| `/trader-pelosi` | Reads the stock trades members of Congress disclose |
| `/trader-analyst` | Pulls reported earnings numbers from SEC filings |
| `/trader-screener` | Screens and ranks companies against your rules |
| `/trader-risk` | Blocks any proposed order that breaks your limits |
| `/trader-broker` | Turns an order you've approved into a ticket for your broker; it never places orders itself |
| `/trader-tax` | Tracks cost basis, tax-loss harvesting and wash sales |
| `/trader-alerts` | Price targets, stops and market-open alerts |
| `/trader-rebalance` | Brings the portfolio back to its target weights |

The skills save their files in a `trader/` folder in this repo. Some read SEC data, which requires your
name and email: set `"sec_user_agent": "Your Name you@example.com"` in `trader/config.json`, or the
`SEC_USER_AGENT` environment variable.

The skills are copied from upstream commit `5189e79` (2026-10-14). `.claude/settings.json` also lists the
trader-skill marketplace, so in Claude Code on your own computer you can run
`/plugin install trader-skill@trader-skill` to get the latest version. That version's commands are
prefixed, e.g. `/trader-skill:trader-copycat`.
