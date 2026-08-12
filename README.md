# /council -- AI Advisory Board for Claude Code

> Spin up 6 sub-agents with different executive perspectives to debate any decision.

Ask a question. Get answers from a CEO, CFO, CMO, CTO, COO, and CPO -- all running in parallel. Returns consensus, dissent, and one clear recommendation.

## Install

```bash
mkdir -p ~/.claude/commands
cp council.md ~/.claude/commands/
```

Then type `/council should I build X or Y first?` in any Claude Code session.

## The 6 Perspectives

| Role | Lens |
|------|------|
| **CEO** | Vision & priority -- does this compound? |
| **CFO** | Revenue & cost -- path to dollar one? |
| **CMO** | Audience & distribution -- who sees this? |
| **CTO** | Build feasibility -- can this ship tonight? |
| **COO** | Execution & operations -- does this scale? |
| **CPO** | Product & user -- does anyone want this? |

## Output

Returns a structured ruling: consensus, dissent, one recommendation, and one risk flag.

## Part Of

This command is part of the [Logos Protocol](https://github.com/angyal168/logos-protocol) -- an open protocol for building an AI assistant that actually knows you.

## License

MIT

<!-- forge-related:v1 -->

## Related

This repo is one module. It handles multi-perspective decision passes; it does not compose itself into a working system -- that wiring is a separate job.

- **[The Forge Full Stack Bundle for Claude Code](https://andrewhangyal.gumroad.com/l/nlajnm?utm_source=github&utm_medium=readme&utm_campaign=council)** -- a paid pack of Claude Code commands from the same author ($129).
- [All tools, free and paid](https://tools.aingyal.com/?utm_source=github&utm_medium=readme&utm_campaign=council) -- the full index.

Listed so you can find them if they are useful to you. Nothing here is required to use this repo, which stays free.

<!-- /forge-related:v1 -->
