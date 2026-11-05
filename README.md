# Trading workspace

This repo sets up Claude Code with the [trader-skill](https://github.com/Jakeschincariol/trader-skill) plugin.
`.claude/settings.json` adds its marketplace and turns the plugin on, so a new Claude Code session here
loads its 11 investing skills, e.g. `/trader-skill:trader-copycat`, `/trader-skill:trader-news` and
`/trader-skill:trader-pelosi`.

The skills save their files in a `trader/` folder in this repo. Some read SEC data, which requires your
name and email: set `"sec_user_agent": "Your Name you@example.com"` in `trader/config.json`, or the
`SEC_USER_AGENT` environment variable.
