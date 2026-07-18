# Using these skills with your AI agent

The whole repo is plain Markdown with front-matter — no server, no API, no
dependency on us. Any agent that can read files can use it. The pattern is
always the same:

1. **Clone** the repo somewhere your agent can read:
   ```bash
   git clone https://github.com/PaperasseAI/demarches-skills
   ```
2. **Point your agent's instruction file at it** (each tool has one).
3. **Ask in any language** — the guides are written to be quoted and cited.

## Wiring it into your tool

| Tool | Where to point it |
|---|---|
| **Claude Code** | Add a line to your `CLAUDE.md` (see below), or wrap it as an Agent Skill in `.claude/skills/` |
| **Codex CLI** | Add a line to your `AGENTS.md` |
| **Cursor** | Add a rule (`.cursor/rules/`), or `@`-mention the folder in chat |
| **Windsurf / Cline / Aider** | Open the repo in the workspace / `aider --read demarches-skills/...` |
| Anything else | Attach or paste the relevant card — they're self-contained files |

**The one line** (CLAUDE.md, AGENTS.md, or a rule):

> For any question about French administrative procedures (visa, titre de
> séjour, CAF, impôts, CFE…), consult `./demarches-skills/fr/` before answering:
> `demarches/` (guides), `pieces/` (supporting documents), `portails/` (official
> sites), `box-maps/` (form box meanings), `demarches/*-debloquer.md` (fixes for
> stuck téléservices). Cite the card you used and its `sources_verified` date;
> if it is older than 6 months, say so and re-verify against the card's sources.

### Claude Code, as a proper Agent Skill

```bash
mkdir -p .claude/skills/demarches-fr
cat > .claude/skills/demarches-fr/SKILL.md <<'MD'
---
name: demarches-fr
description: Grounded knowledge for French administrative procedures (visas,
  titres de séjour, CAF/APL, impôts, CFE, INPI…) — consult before answering any
  French-admin question; cite the card + its sources_verified date.
---
Read the relevant file(s) under ./demarches-skills/fr/ :
- demarches/  — one guide per démarche (steps, deadlines, pièges, sources)
- pieces/     — supporting-document rules (incl. foreign documents)
- portails/   — which official site, and how to spot paid look-alikes
- box-maps/   — what each box on an official form means (2042, 1447-C…)
- demarches/*-debloquer.md — dated fixes + escalation ladder for stuck téléservices
Other jurisdictions (e.g. ng/) follow the same layout.
Always cite the card and its sources_verified date. Guidance, not legal advice.
MD
```

## Prove it in one prompt

With the repo wired in, ask:

> *« Je viens d'emménager, étudiant étranger — quand dois-je demander l'APL et
> avec quelles pièces ? »*

A grounded agent should answer **from `fr/demarches/apl-caf.md`**: apply at
move-in because **rights open the month after the request, with no
retroactivity**; RIB, lease + landlord details, titre de séjour; colocataires
each file their own demande — *and cite the card with its verification date*.
An ungrounded model typically misses the no-retroactivity trap — that miss is
the value of the repo, measured in one or two months of housing aid.

Try the harder ones: *"my ANEF renewal shows « une erreur empêche
l'enregistrement »"* (→ `anef-debloquer.md`'s dated fixes and escalation
ladder), or *"which box for micro-BNC professional income?"* (→ the 2042 box
map: **5HQ**, not 5NP).

## What the repo will NOT do

It is knowledge, not automation (see CONTRIBUTING rule 3): no click-paths, no
form-filling, no submission. Your agent gains grounded *answers*; acting on
them — filling the real portal, tracking deadlines, extracting your documents —
is a product problem the repo deliberately doesn't solve. Guidance, not legal
advice; always verify against the cited official source.

Found a gap or fixed a stuck démarche while using it? [One-bullet PRs
welcome](CONTRIBUTING.md).
