# demarches-skills 🇫🇷

**Open knowledge for surviving government procedures — starting with French
démarches — as agent-ready skills.** Checklists, portal maps and document guides for the démarches individuals
(newcomers, students, expats, residents) actually face: visas, titres de séjour,
CAF, CVEC, impôts des particuliers, ANTS…

Skills are plain Markdown. They work with any AI agent or tool that can read files
(Claude Code, Cursor, Codex, Windsurf, Cline, Aider…) — **[wire it into yours in
two minutes → USAGE.md](USAGE.md)**.

## Why this exists

French admin knowledge is scattered, changes constantly, and mostly circulates as
folklore in expat groups. This repo makes it **verifiable** (every claim cites an
official source), **maintained** (see freshness rules) and **usable by agents**.

## Not to be confused with `romainsimon/paperasse`

Two open-source projects share the word *paperasse* (French for "paperwork"), and
they are easy to mix up. They are **separate, unaffiliated projects**:

- [`romainsimon/paperasse`](https://github.com/romainsimon/paperasse) (MIT)
  pioneered skills-as-files for the **professions** of French paperwork —
  accountant, notarial and audit expertise, with data files and evals verified
  against official simulators.
- **This repo** equips **individuals** facing the system — démarche guides, box
  maps, débloquer cards — citation-enforced against official sources. It shares
  the *approach*, not the content: **nothing here is derived from his files**;
  every card is authored against the cited official source.

Credit where due beyond the idea: the [Paperasse.ai](https://paperasse.ai)
product (separate from this repo) adapted two of his skills — the personal-tax
expert and the tax-audit simulation — with attribution preserved under the MIT
license.

## Structure

```
fr/                       ← France (other jurisdictions welcome — see CONTRIBUTING)
├── demarches/            ← one guide per démarche (TEMPLATE.md format)
├── pieces/               ← supporting-document checklists
├── portails/             ← which official portal for what + how to spot fakes
├── documents/            ← what each French admin document is and proves
└── box-maps/             ← meaning of every box code on an official form (cartes des cases)
```

## Relationship with Paperasse AI

This repo is maintained by the [Paperasse AI](https://www.paperasse.ai) team,
the consumer copilot that guides people through these démarches in their language —
as a **Chrome extension** whose agent operates the official portals like a human
(filling and navigating for you; **you always review and submit**), a **mobile app**
whose camera guides you box by box across paper forms (Form Lens), and a web app.
Contributions here improve the guidance for **everyone** — the repo is MIT and works
with any agent. Paperasse AI additionally builds automated, hand-held versions of
well-documented démarches: **a complete, well-sourced guide here is the fastest way
to get a démarche supported there.**

## Disclaimer

Guidance, not legal advice. For complex situations (litigation, ongoing procedures,
appeals), consult a qualified professional. Always verify against the cited official
source — French rules change more often than you'd like.
