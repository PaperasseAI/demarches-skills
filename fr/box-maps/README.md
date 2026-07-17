# Box maps (cartes des cases)

A **box map** is the meaning of every box code on an official French form — `1AJ`
= salaires, `5HQ` = micro-BNC revenus professionnels, `8UU` = comptes à l'étranger
— transcribed from the government's own **notice**. It is *not* a how-to guide (those
live in `../demarches/`); it is a reference an agent or a person consults while
actually filling the form.

Why it's useful: on French tax forms the **box codes are identical on paper and
online** (impots.gouv.fr labels each field with the same code), so one map serves
both channels — "which box do I write in" and "which online field do I fill".

## Files
- `cerfa-2042.md` — income-tax return 2042 + 2042 C PRO + annexe 2047 (revenus 2025).
- `cerfa-1447c.md` — CFE déclaration initiale (full case map, cadres A1–C, incl. the 1447-C-K pre-identified variant).
- `cerfa-10842.md` — attestation de loyer / résidence en foyer (CAF housing-aid certification, recto/verso field map).

## Contributing a box map
1. **Transcribe from the official notice, not from memory or a blog.** Every box
   must trace to the government notice for that form (e.g. `2041-NOT` for the 2042).
2. **Semantics only.** Box code → what it means → when it applies. **Never** include
   product-specific wiring (data paths, CSS selectors, field mappings) — those belong
   to whatever tool consumes the map, not to the public reference.
3. **Pin the edition.** French forms carry a yearly *millésime* (`cerfa 10330*30` =
   revenus 2025). State the edition in the frontmatter (`edition:`) and title; the
   box codes are stable across editions but amounts, thresholds and new boxes are not.
4. **Frontmatter** (see `cerfa-2042.md`): `slug: fr-box-map-<form>`, `jurisdiction`,
   `title`, `audience`, `last_updated`, `sources_verified` (when you checked it
   against the notice), `edition`.
5. **Freshness.** When a new édition ships, re-verify against the new notice and bump
   `sources_verified` + `edition`. Guides older than 6 months must be re-verified
   (repo rule).
6. **Map every signature box (✍️).** For each one: where it is (page + cadre), **who
   signs** (déclarant, landlord, establishment manager…), and what that signature
   legally covers — then state the **total count** ("one signature box on the form" /
   "three in total; a complete file has every applicable one signed"). An unsigned
   form is the most common way a filing silently fails, and the signature is the one
   act that always stays with the human — a form map that doesn't locate it is
   incomplete. Add the matching piège (unsigned form, missed second signature, wrong
   side signed).

Wanted next: 2044 (revenus fonciers), 2035 (BNC), 2033/2065 (IS liasse — corporate),
1447-C (CFE), and box maps for other jurisdictions under their own `<iso>/box-maps/`.
