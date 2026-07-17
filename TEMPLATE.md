---
# Every démarche guide MUST use this front-matter
slug: <iso>-<kebab-name>         # jurisdiction-prefixed, stable (fr-…, ng-…)
jurisdiction: <iso>              # ISO country code of the jurisdiction folder (fr, ng…)
title: <Name of the démarche>
audience: <who this applies to — e.g. non-EU students on a VLS-TS>
last_updated: YYYY-MM-DD         # guides older than 6 months must be re-verified
sources_verified: YYYY-MM-DD
---

# <Title>

One paragraph: what this démarche is, who must do it, what happens if you don't.

## Éligibilité / Qui est concerné
- Plain-language conditions. Note per-nationality or per-status differences explicitly.

## Étapes
1. High-level stages in order (what, where, roughly when — NOT click-by-click portal
   automation; portals change and click-paths rot).

## Pièces justificatives
- Every document needed, with the acceptable forms (original / copy / translation /
  apostille). Link entries in `../pieces/` where a shared checklist exists.

## Délais et échéances
- Deadlines, processing times, and what starts the clock. Consequences of missing them.

## Portail / Où faire la démarche
- The official site or office (link `../portails/`). Cost, payment method (timbre fiscal…).

## Pièges connus
- Real-world gotchas (prefecture variances, RDV scarcity, look-alike paid sites…).

## Sources
- REQUIRED: one official source per factual claim above (service-public.fr, ANEF,
  legifrance, impots.gouv.fr, caf.fr…) with the date you checked it.

---

## Other folders (same frontmatter + sources rules)

This template's sections are for **`demarches/` guides**. The other folders keep the
same front-matter and citation discipline but their own natural sections:
- `documents/` — what a document is, its issuer, its field structure, how to obtain
  or replace it, and how it is used elsewhere.
- `pieces/` — supporting-document checklists and acceptance rules.
- `portails/` — official portals and how to spot look-alikes.
- `box-maps/` — per-form box semantics; see the folder's own README for its rules.

## Cross-border content — file by role, never by direction

A cross-border journey (e.g. using a Nigerian birth certificate for a French visa) is
**composed from two single-jurisdiction files** — never written as its own card:

- the **destination dictates the requirement** →
  `<destination>/pieces/foreign-documents.md` (origin-agnostic);
- the **origin provides the authentication mechanism** →
  `<origin>/demarches/authenticate-documents.md` (destination-agnostic).

Use exactly those two filenames in every jurisdiction so files compose. Never encode
a direction in a filename (`…-for-france.md` is the anti-pattern: it fans out per
country pair and files one country's requirements under another country's folder).
