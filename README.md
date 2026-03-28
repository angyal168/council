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
