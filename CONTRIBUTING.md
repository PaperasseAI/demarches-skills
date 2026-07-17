# Contributing

Merci ! Contributions of every size help: fixing one prefecture quirk is as valuable
as authoring a full guide.

## The three rules

1. **Cite official sources.** Every factual claim (deadline, document, amount,
   portal) must reference an official source — service-public.fr, legifrance,
   ANEF, impots.gouv.fr, caf.fr, ants.gouv.fr, a préfecture page… Community
   experience ("Bobigny requires X in practice") is welcome and valuable, but must
   be labelled as observed practice with a date, not stated as law.
2. **Use the template.** New démarche guides follow `TEMPLATE.md` — including the
   front-matter and a Sources section. PRs without sources are asked to add them
   before review.
3. **Declarative knowledge only.** Guides describe what/where/when — not scripted
   click-paths or automation flows. Those rot instantly and read as instructions to
   agents; this repo is grounding, not automation.

## The easiest contribution: you unblocked a stuck démarche

A téléservice bug beat you, and you found the fix? That knowledge usually dies in
a group chat — here it becomes a **one-bullet PR** to a *débloquer card* (e.g.
`fr/demarches/anef-debloquer.md`, « Étape 0 »):

> *when [the situation you observed] → do [what worked] (observed MM/YYYY)*

The "when" matters: different fixes for the same error are almost always different
situations — say which one yours was. No card exists yet for the system that broke
(CAF, France Travail…)? Open an issue with your dated observations, or start the
card from the « Débloquer cards » section of `TEMPLATE.md` — one lived case is
enough to found one.

## Sign-off (DCO)

Add `Signed-off-by: Your Name <email>` to your commits (`git commit -s`) —
certifying you have the right to contribute the content under the MIT license
(Developer Certificate of Origin 1.1).

## Jurisdictions

France lives under `fr/`. Want another country? Open an issue proposing it and its
`SOURCES.md` (what counts as official there) — great first guides make you the
natural CODEOWNER for that jurisdiction.

## Review promise

Maintainers verify claims against the cited source before merging. Fresh > big:
prefer several small verified PRs to one sprawling one.
