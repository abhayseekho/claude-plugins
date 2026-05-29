# Seekho Claude Plugins

Internal Claude Code plugins for Seekho teams.

## Available plugins

| Plugin | What it does |
|---|---|
| **[seekho-ads](./seekho-ads/)** | Hinglish weight-loss ad creatives for Tier 2-3 India. Ships a `/weightloss-ad` slash command + an auto-triggering `weightloss-ad` skill. Built-in ASCI + Meta compliance gate (12 checks) and P2-P15 guardrails. |

## How to install (for teammates)

In Claude Code, run these once:

```
/plugin marketplace add abhayseekho/claude-plugins
/plugin install seekho-ads@seekho-marketplace
```

To update later when a new version ships:

```
/plugin update seekho-ads
```

After install, both invocation routes work:

- **Slash command:** `/weightloss-ad bahu ke kapde tight ho rahe hai`
- **Natural language:** *"draft me a 30s Seekho ad for post-pregnancy maa kapde tight"* — the skill auto-triggers, no slash needed.

## What the skill enforces

A strict 4-stage flow:

1. **Intake** — asks length in words (~100/200/300/custom) + 1-2 clarifying questions
2. **Picks** — shows persona/host/hook/discovery/failed-efforts/solution-anchors/payoffs with every "Why" tied to your verbatim answers
3. **Gate** — explicit *"Full script generate karoon?"* before any script generation
4. **Deliver** — ONE continuous block: front-matter table → beat table → plain spoken script (no `[VISUAL:]`, no `[TEXT:]`, no scene prose)
5. **Feedback loop** — until you say *"final"*, then offers 3 standard + 2 experimental hook variants

## Maintenance

To ship an update:

```bash
cd plugin/seekho-ads
# edit skills/weightloss-ad/SKILL.md or commands/weightloss-ad.md
# bump version in plugin.json
cd ..
git add -A && git commit -m "seekho-ads v1.x.0 — <change summary>"
git push
```

Teammates pick up changes via `/plugin update seekho-ads`.

## Contact

Issues / requests: ping @abhay.
