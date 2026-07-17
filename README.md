# demarches-skills 🇫🇷

**Open knowledge for surviving French administrative démarches — as agent-ready
skills.** Checklists, portal maps and document guides for the démarches individuals
(newcomers, students, expats, residents) actually face: visas, titres de séjour,
CAF, CVEC, impôts des particuliers, ANTS…

Skills are plain Markdown. They work with any AI agent or tool that can read files
(Claude Code, Cursor, Codex, Windsurf, Cline, Aider…).

## Why this exists

French admin knowledge is scattered, changes constantly, and mostly circulates as
folklore in expat groups. This repo makes it **verifiable** (every claim cites an
official source), **maintained** (see freshness rules) and **usable by agents**.

Inspired by the approach of [`romainsimon/paperasse`](https://github.com/romainsimon/paperasse)
(MIT), which equips the **professions** of French paperwork (accounting, notarial
law, audit) — this repo equips **individuals** facing the system.

## Structure

```
fr/                       ← France (other jurisdictions welcome — see CONTRIBUTING)
├── demarches/            ← one guide per démarche (TEMPLATE.md format)
├── pieces/               ← supporting-document checklists
├── portails/             ← which official portal for what + how to spot fakes
├── documents/            ← what each French admin document is and proves
└── box-maps/             ← meaning of every box code on an official form (cartes des cases)

ng/                       ← Nigeria (origin-country documents + how to use them abroad)
├── documents/            ← Nigerian documents (NPC birth certificate, WAEC…) and their structure
└── demarches/            ← e.g. legalising Nigerian documents for use in France
```

Origin-country folders like `ng/` cover the documents a person **brings** to a
destination-country démarche (a Nigerian student's NPC birth certificate for a French
visa), and how to make them usable there. Same TEMPLATE + citation rules.

## Relationship with Paperasse AI

This repo is maintained by the team behind [Paperasse AI](https://www.paperasse.ai),
the consumer copilot that guides people through these démarches in their language.
Contributions here improve the guidance for **everyone** — the repo is MIT and works
with any agent. Paperasse AI additionally builds automated, hand-held versions of
well-documented démarches: **a complete, well-sourced guide here is the fastest way
to get a démarche supported there.**

## Disclaimer

Guidance, not legal advice. For complex situations (litigation, ongoing procedures,
appeals), consult a qualified professional. Always verify against the cited official
source — French rules change more often than you'd like.
