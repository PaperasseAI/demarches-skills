---
name: demarches
description: Grounded, citation-enforced knowledge for government procedures —
  French démarches first (visa, titre de séjour / ANEF, CAF/APL, carte Vitale,
  déclaration de revenus & 2042 box map, auto-entrepreneur, CFE, INPI, passeport,
  CNI, retraite…) plus Nigerian document authentication. Use whenever a question
  touches administrative procedures, official forms, supporting documents, or a
  stuck government téléservice; answer from a card and cite it with its
  sources_verified date.
metadata:
  repo: https://github.com/PaperasseAI/demarches-skills
  license: MIT
---

# Démarches — government-procedure knowledge cards

Answer from the cards in this folder, not from memory. Every card cites official
sources and carries `last_updated` / `sources_verified` dates.

## How to use

1. Pick the card(s) matching the question from the index below and read them.
2. Answer in the user's language (cards are FR/EN; the knowledge translates).
3. **Cite the card and its `sources_verified` date.** If older than 6 months,
   say so and re-verify against the card's listed sources before relying on it.
4. If no card covers the question, say so — do not present folklore as procedure.
   Contributions: see `CONTRIBUTING.md`.

## Index

### France — démarche guides (`fr/demarches/`)
| Card | Covers |
|---|---|
| `visa-etudiant.md` | Student long-stay visa (France-Visas + Études en France) |
| `passeport-talent-projet-innovant.md` | French Tech Visa endorsement — the innovation attestation on demarche.numerique.gouv.fr (prerequisite for the passeport talent « projet économique innovant » visa/titre); incubator document required; full form question list |
| `validation-vls-ts.md` | Validating a VLS-TS after arrival |
| `renouvellement-titre-de-sejour.md` | Residence-permit request/renewal on ANEF — incl. « En cas de blocage » (dated fixes + escalation ladder for a stuck ANEF) |
| `apl-caf.md` | CAF housing aid (APL/ALS) |
| `carte-vitale.md` | Health-insurance affiliation + carte Vitale |
| `declaration-revenus.md` | Income-tax declaration (first-time vs returning filer) |
| `auto-entrepreneur.md` | Starting a micro-entreprise |
| `cfe.md` | CFE initial declaration (1447-C) + exemptions |
| `impot-societes.md` | Corporate tax (liasse fiscale) |
| `modification-entreprise.md` | Changing company details (siège, dirigeant, statuts) |
| `depot-marque-inpi.md` | Filing a trademark at INPI |
| `passeport.md` / `carte-identite.md` | Passport / national ID card |
| `changement-adresse.md` | Declaring a change of address |
| `demande-retraite.md` | Claiming retirement (régime général + complémentaire) |
| `permis-construire.md` | Building permit / déclaration préalable |
| `demarches-ants.md` | The shared ANTS / France Titres flow (pré-demande → timbre → RDV): passeport, CNI, carte grise |

### France — forms, documents, portals
- `fr/box-maps/` — meaning of every box on official forms: **2042** (income tax
  + annexes), **1447-C** (CFE), **10842** (attestation de loyer).
- `fr/pieces/` — supporting-document rules, incl. `foreign-documents.md`
  (apostille/legalisation + sworn translation).
- `fr/documents/` — what each French admin document is and proves.
- `fr/portails/` — which official site for what, and how to spot paid look-alikes.
- `fr/SOURCES.md` — canonical official sources.

### Nigeria (`ng/`)
- `demarches/authenticate-documents.md` — authenticating Nigerian documents for use abroad.
- `documents/` — NPC birth certificate; WAEC / university certificates & transcripts.

## Boundaries

- Guidance on procedure, not legal/tax advice; the user files themselves.
- Cards describe official processes and stable form semantics — never
  click-by-click portal automation (portals change; click-paths rot).
