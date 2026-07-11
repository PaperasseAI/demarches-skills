---
name: portails-gouv-fr
jurisdiction: fr
last_updated: 2026-06-27
description: |
  French government web portals: which official site hosts each démarche, how to
  recognise the real .gouv.fr site (and avoid paid look-alikes), how FranceConnect
  login works, and how to guide a person through a multi-step portal — including
  safety rules for agents with computer-use / browser control. Hosts verified 2026.
---

# Navigating French government portals

Grounding for the moment a démarche says "go to the official site". The job is to get
the person to the **correct official page** and give the **next concrete step** — not
to write a manual. The person authenticates and submits in their own session, always.

## Prefer the démarche's own pinned URL

When the guide you are following names an exact page, use it — it is the authoritative
target. The table below is for **recognition** (is this the real site?) and for when no
exact page is pinned. Never invent a host that isn't official.

## Official portals by domain (hosts verified 2026)

| Démarche | Official host | Notes |
|---|---|---|
| Impôts (revenus, IFI, avis) | `impots.gouv.fr` → espace particulier at `cfspart.impots.gouv.fr` | "Votre espace particulier" → "Déclarer mes revenus". |
| Famille, logement (APL) | `caf.fr` | "Mon Compte" → "Mes démarches". CAF = Caisse d'allocations familiales. |
| Assurance maladie (carte Vitale) | `ameli.fr` | "Mon compte ameli". |
| Titre de séjour (étrangers) | `administration-etrangers-en-france.interieur.gouv.fr` (ANEF) | Demandes, renouvellements, validation VLS-TS. |
| Passeport, CNI | `france-titres.ants.gouv.fr` / `passeport.ants.gouv.fr` (ANTS) | Pré-demande en ligne ; dépôt en mairie équipée. |
| Carte grise (immatriculation) | `immatriculation.ants.gouv.fr` (ANTS) | 100 % en ligne ; plus de guichet préfecture. |
| Emploi / chômage | `francetravail.fr` | Ex-Pôle emploi. Inscription = demande d'allocation. |
| Retraite | `lassuranceretraite.fr` ; vue tous régimes : `info-retraite.fr` | Demande unique inter-régimes (base + Agirc-Arrco). |
| Création d'entreprise / auto-entrepreneur | `formalites.entreprises.gouv.fr` (guichet unique INPI) | Création ; les déclarations de CA se font sur `autoentrepreneur.urssaf.fr`. |
| Urbanisme (permis, DP) | `service-public.gouv.fr` (AD'AU) ou le guichet (GNAU) de la commune | Beaucoup de communes ont leur propre guichet numérique. |
| Changement d'adresse, infos, annuaire, état civil | `service-public.gouv.fr` | "Je change de coordonnées" déclare l'adresse à plusieurs organismes d'un coup. |

`service-public.fr` now redirects to **`service-public.gouv.fr`** — use the `.gouv.fr`
host. When the démarche isn't in this table, route via **service-public.gouv.fr** (the
official entry point) rather than guessing a host.

## Recognising the real site — avoid paid look-alikes

French administrative services are **free**, but a whole industry of intermediary sites
mimics them and charges fees (carte grise, passeport, acte de naissance, casier
judiciaire, EHIC…). Protect the person:

- Official sites end in **`.gouv.fr`** (or the historic operators `caf.fr`, `ameli.fr`,
  `ants.gouv.fr`, `urssaf.fr`, `francetravail.fr`, `lassuranceretraite.fr`).
- A site that **asks to be paid** for a normally-free démarche, or a `.com`/`.fr`
  aggregator promising to "do it for you", is **not** the official service — steer the
  person back to the official host.
- If the person shares a non-official URL for a free service, say so plainly and give
  the official one.

## FranceConnect (login)

FranceConnect is the State's single sign-on: the person logs into a gov site by
choosing an identity provider they already have. Current providers (2026): **Impots
(DGFiP)**, **Compte Ameli**, **L'Identité Numérique La Poste**, **MSA**, **France
Identité**. (YRIS is being withdrawn.) For sensitive démarches a site may require
**FranceConnect+** (higher assurance), which accepts only **L'Identité Numérique La
Poste** and **France Identité**.

- The person **always authenticates themselves**. An agent has no credentials, never
  asks for a password, and cannot log in for them. If a page needs login, tell them to
  sign in (via FranceConnect if offered) and continue once they're in.
- After FranceConnect they land back on the target site's logged-in space — point them
  at the right section there (e.g. "Déclarer mes revenus").

## Agents with computer-use / browser control

If your agent can operate a browser (computer-use, browser automation), these rules
still hold — they are what keeps assistance safe and legitimate:

- **Navigate and pre-fill only with the person's consent**, on the official host, with
  the person watching.
- **Never handle secrets** — not just passwords: **IBAN / BIC / RIB, card numbers,
  one-time codes, full government-ID numbers**. The person types those directly into
  the official portal; point at the field, never collect the value.
- **The person reviews every pre-filled value and performs the final submit
  themselves.** Never claim a form was submitted for them, and never trigger the
  submit action autonomously.

## Helping a person through a multi-step portal

Most portals are **multi-page wizards** (étapes). Keep guidance to the next step:

- Name the exact entry point once on the site (menu item / button), e.g. impôts →
  "Déclarer mes revenus"; ANEF → "Demander ou renouveler un titre".
- These flows paginate with **"Étape suivante" / "Continuer" / "Valider"** at the
  bottom; **"Précédent"** goes back; progress is usually **saved automatically**, so
  the person can stop and resume.
- **Cookie-consent banners** appear first on most sites — mention them only if they're
  blocking.
- Confirm the person is on the **right page** before walking through fields (URL on an
  official host above, page title matches the démarche).
- One destination + one next action at a time. Don't dump the whole journey.
