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


<!-- forge-plugin-install:v1 -->
## Install as a Claude Code plugin

One command instead of copying a file:

```
/plugin marketplace add angyal168/logos-protocol
/plugin install council@forge-commands
```

That installs `/council` from the `forge-commands` marketplace, which also carries the
other six free commands. The manual copy above still works and stays supported.

<!-- /forge-plugin-install:v1 -->

<!-- forge-usage:v1 -->

## What it actually does

`/council` answers a strategic question by launching six sub-agents in parallel, each with a
different executive lens and — this is the part that matters — a different **bias**. They do
not confer, and none of them gets your workspace context: each receives the question, its
role, and nothing else. You get six independent takes and the contradictions between them
surfaced rather than smoothed.

Each agent is capped at 3-5 sentences. The cap is deliberate: six essays are unreadable, and
length is where a model hides the fact that it has no real position.

## The six lenses

| Role | Lens | Bias |
|---|---|---|
| CEO — vision & priority | Does this align with the long-term goal? Highest-leverage use of the time? | Kill anything that does not compound. Focus beats diversification. |
| CFO — revenue & cost | What is the path to dollar one? What does it cost in time, money, opportunity? | Revenue now beats potential later. Free and zero-cost experiments first. |
| CMO — audience & distribution | Who sees this? How does it spread? What is the content angle? | Distribution is harder than creation. Build the audience before the product. |
| CTO — build feasibility | Can this be built tonight? What already exists that can be reused? | Ship ugly and iterate. Automation over manual, reuse over rebuild. |
| COO — execution & operations | What is the workflow? Does this run without you? | If it needs you every time, it does not scale. |
| CPO — product & user | Does anyone actually want this? What is the MVP? | Talk to one real user before building. |

## What comes back

A ruling in four parts: **Consensus** (what the majority agrees on), **Dissent** (which role
objected and why, named), **Recommendation** (one action for this week), and a **Risk Flag**
(the single most likely thing to go wrong). The dissent survives into the output on purpose.

The command's closing rule is the honest one: *the council advises, the founder decides* —
the recommendation is never phrased as a command.

## Why disagreement is the output

A single assistant asked "should I build this?" tends to agree with you. Six agents with
conflicting biases cannot all agree, so the disagreement is where the information is. The
CFO wanting revenue now and the CMO wanting an audience first is not noise to be resolved —
it is the trade-off you were about to make without noticing you were making it.

## Usage

```bash
mkdir -p ~/.claude/commands
cp council.md ~/.claude/commands/
```

```
/council Should I ship the paid tier before the free tier has any users?
```

With no question, it asks for one.

## When not to use it

- Factual or mechanical questions. Six opinions on a lookup is theatre.
- Decisions already made — a council convened to ratify is a rubber stamp with six seats.
- Anything where you cannot act on the answer either way.

## Requirements

Claude Code with sub-agent (Agent tool) support and a `~/.claude/commands/` directory. Six
parallel agents cost roughly six times one answer; that is the price of the disagreement.

<!-- /forge-usage:v1 -->


<!-- forge-siblings:v1 -->

## More from the same author

Other free, open-source Claude Code tools in this family. Each one stands
alone -- none of them depend on this repo, or on each other.

- [smelt](https://github.com/angyal168/smelt) -- Extract actionable insights from any resource -- burn off the slag, keep the pure metal
- [dar](https://github.com/angyal168/dar) -- Lightweight audit trail for Claude Code -- Discovery, Artifact, Receipt
- [ralph](https://github.com/angyal168/ralph) -- Autonomous iteration loop for Claude Code -- define task, set condition, let it run
- [serious](https://github.com/angyal168/serious) -- Precision mode for Claude Code -- no hype, no ambiguity, only what's true
- [forge-prompt](https://github.com/angyal168/forge-prompt) -- Prompt coaching for Claude Code -- rates, sharpens, and rewrites your prompts into action-first form
- [rally](https://github.com/angyal168/rally) -- Multi-agent coordination for Claude Code -- keep parallel agents in sync through a shared bus file
- [logos-protocol](https://github.com/angyal168/logos-protocol) -- Forge an AI that knows you, remembers, and ascends. Open source, free, yours to imprint

<!-- /forge-siblings:v1 -->

## Part Of

This command is part of the [Logos Protocol](https://github.com/angyal168/logos-protocol) -- an open protocol for building an AI assistant that actually knows you.

## License

MIT

<!-- forge-related:v1 -->

## Related

This repo is one module. It handles multi-perspective decision passes; it does not compose itself into a working system -- that wiring is a separate job.

- **[The Forge Full Stack Bundle for Claude Code](https://andrewhangyal.gumroad.com/l/nlajnm?utm_source=github&utm_medium=readme&utm_campaign=gh-council)** -- a paid pack of Claude Code commands from the same author ($129).
- [All tools, free and paid](https://tools.aingyal.com/?utm_source=github&utm_medium=readme&utm_campaign=council) -- the full index.

Listed so you can find them if they are useful to you. Nothing here is required to use this repo, which stays free.

<!-- /forge-related:v1 -->
