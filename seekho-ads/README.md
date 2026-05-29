# Seekho Ads Plugin

Hinglish ad-creative toolkit for **Seekho's weight-loss vertical** — Tier 2-3 India, female-skewed, ages 18-45.

## What this plugin ships

Two ways to invoke the same creative flow — pick whichever feels natural:

| Type | Trigger | Best for |
|---|---|---|
| **`/weightloss-ad`** slash command | Type `/weightloss-ad <topic>` | When you want explicit control, easy to remember |
| **`weightloss-ad`** auto-skill | Just describe the ad in plain language ("draft me a 30s ad for bahu kapde tight") | When you're in flow and don't want to remember a command |

Both run the same 4-stage flow:
1. **Intake** — asks length in words (~100/200/300/custom) + 1-2 clarifying questions
2. **Picks** — shows persona/host/hook/discovery/efforts/anchors/payoffs with every "Why" tied to your verbatim answers
3. **Gate** — explicit *"Full script generate karoon?"* before any script
4. **Deliver** — ONE continuous block: front-matter → beat table → plain spoken script (voice-only, no `[VISUAL:]` or `[TEXT:]`)
5. **Feedback** — loops on edits, then offers 3 standard + 2 experimental hook variants

## Installation (for teammates on the employee plan)

```bash
# Add the marketplace once
/plugin marketplace add seekho/claude-plugins

# Install the plugin
/plugin install seekho-ads
```

After install:
- Type `/weightloss-ad bahu ke kapde tight ho rahe hain` for the explicit command, OR
- Just say *"draft a 200-word weight-loss ad for post-pregnancy maa"* and the skill auto-triggers.

## Guardrails enforced (P-numbered, 11 active)

- **P2** — Expand beyond 3 working hooks (additive experimental variants)
- **P3** — Scripts are voice-only (no scene staging, no overlay markers)
- **P5** — Tier 2-5 satirical register (taunt/overheard opener from named relation)
- **P6** — Discovery not salesy (no CTA verbs, no feature lists, human bridge)
- **P7** — Hook carries weight-loss category signal in first 1-2 lines (Meta attribution)
- **P8** — Tier-1 vocab BANNED + substitution table (metabolism → *body kaise khaana pachaati hai*, etc.)
- **P9** — Discovery names *"Seekho app"* explicitly when phone/video/screen cue appears
- **P10** — Doctor verbs = *samjhaya / samjhate*, never *bola / kaha / order / prescribe* (ASCI compliance)
- **P11** — Bridge line between Solutions and Payoff for ads ≥30s
- **P14** — Discovery beat states both (a) topic doctor taught + (b) one insight that flipped thinking

## §F final compliance gate (12 checks before delivery)

Every ad passes:

1. Zero numeric weight/size/time claims
2. Zero before/after framing
3. Zero medical-cure language
4. Gym/supplement framed optional
5. Ends on hope/empowerment
6. Seekho never in Hook
7. English always translated inline
8. **(P7)** Category signal word present
9. **(P8)** Zero banned vocab + greylist limit obeyed
10. **(P9)** Seekho app named on phone/video cue
11. **(P10)** Educator verbs for doctors
12. **(P11)** Bridge line present

## Updating

```bash
/plugin update seekho-ads
```

## Folder structure

```
seekho-ads/
├── plugin.json                              # manifest
├── README.md                                # this file
├── commands/
│   └── weightloss-ad.md                     # /weightloss-ad slash command
└── skills/
    └── weightloss-ad/
        └── SKILL.md                         # auto-triggering skill
```
