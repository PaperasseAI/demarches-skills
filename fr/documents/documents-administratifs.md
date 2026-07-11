---
name: documents-administratifs-fr
jurisdiction: fr
last_updated: 2026-06-21
description: |
  Reading French administrative documents: what each one looks like, which fields
  matter, and the classic decoys (net imposable vs net à payer, visa number vs
  passport number). Grounding for any agent doing vision/OCR extraction on uploads.
---

# Reading French administrative documents

Grounding for extracting structured data from document photos and scans. Read only
what is legibly present; never invent. When a field is not on the document, omit it.

## Extracted values are a BEST GUESS — have a human confirm them

Anything read off a photo or scan is vision/OCR **best-guess, not ground truth** —
glare, handwriting, look-alike characters (0/O, 1/I, 5/S) and bad crops cause errors.
Treat extracted values as **drafts**: read the key fields back to the person and have
them **confirm or correct each one** before anything relies on them — above all
identifiers and dates (visa number, passport number, card number, validity dates).
Pre-fill the confirmation with the best guess so they only verify or edit. Values a
person **typed themselves** are taken as given and need no re-confirmation.

## Bulletin de paie (payslip)

- The figure that matters for income tax is the **net imposable** (a.k.a. *net fiscal*
  / *net imposable cumulé*), **not** the *net à payer* and **not** the *brut*.
- It is usually labelled "Net imposable" or "Montant net imposable"; the **cumul
  annuel** (year-to-date) column near the bottom gives the annual figure.
- *Salaire brut* and *net à payer avant impôt* are decoys — do not use them as taxable
  salary.
- Employer name and SIRET appear in the header; the period (mois/année) is near the top.

## Avis d'impôt sur le revenu (tax notice)

- Carries the **revenu fiscal de référence (RFR)**, the **nombre de parts**, and the
  **numéro fiscal** (13 digits) — the numéro fiscal is the stable identifier for the
  foyer.
- The **revenu imposable** and the resulting **impôt** are stated explicitly; prefer
  these printed totals over recomputing.

## RIB / IBAN

- A French IBAN starts with **FR** followed by 25 characters; the **BIC** is 8 or 11
  characters. The account holder's name appears alongside.

## Relevé de compte étranger (foreign bank statement)

- For the déclaration of foreign accounts (formulaire 3916): capture the **institution
  name and address**, the **account number** (often an IBAN), the **country**, and the
  **account type** (bank / crypto / life insurance). Opening/closing dates if printed.
- The statement currency is not always EUR — record the currency as shown; do not
  convert.

## Visa long séjour (long-stay visa / VLS / VLS-TS) — a sticker inside the passport

A visa is a STICKER on a passport page — it is NOT the passport itself and NOT the
residence-permit card. The numbers are easy to confuse; read each from the right place:

- **Visa number**: the visa's OWN number — the **large stand-alone number** on the
  sticker (often printed vertically and/or in red) that also begins the machine-readable
  **MRZ** line (e.g. 604256871). Do NOT take it from the "N° PASSEPORT" field.
- **Passport number**: the value in the sticker's clearly **labelled "N° PASSEPORT /
  PASSPORT N°"** field (e.g. A13313669). This is a DIFFERENT number from the visa number
  above — **never swap the two**. A talent VLS shows BOTH: the big stand-alone number is
  the *visa*, the "N° PASSEPORT" field is the *passport*.
- **Type**: the "TYPE DE VISA / TYPE" field, e.g. **D** for a long-stay visa.
- **Category**: the **REMARQUES / OBSERVATIONS** line, e.g. "PASS. TALENT PROJET
  INNOVANT PT6 VLS" (passeport talent – projet innovant, the principal), "PASS. TALENT
  FAMILLE F14 VLS" (family member), or "VLS-TS étudiant". The talent code identifies the
  sub-type: PT6 = projet économique innovant; F14 = famille (spouse/family of a talent
  holder). Keep the whole remarks line verbatim too.
- **Validity**: the "DU … AU …" dates. **Entries**: "NOMBRE D'ENTRÉES", e.g. MULT.
  **Durée de séjour**: a number of days; if it reads "XXX" or is blank it is a
  placeholder — omit it. **Issued at**: "DÉLIVRÉ À".
- Holder identity: **NOM/surname is printed FIRST**, then given names; the MRZ encodes
  nationality as a 3-letter code (e.g. NGA).

## Carte / titre de séjour (residence-permit card)

- The **card number** ("N° du titre", usually near the photo) — NOT the passport number
  and NOT a visa number.
- **Permit type** (e.g. "PASSEPORT TALENT", "ÉTUDIANT", "VIE PRIVÉE ET FAMILIALE",
  "SALARIÉ", "VISITEUR") and the **validity** (du … au …).
- **NOM/surname first**, then given names; birth date and nationality are on the card.
- **Holding a card ⇒ NOT a first issue.** Someone with a titre de séjour card is
  renewing or changing status, never applying for a first issue — don't look for a VLS
  for them.

## Passport

- **Passport number**: the "Passport No / N° de passeport" field (repeated in the MRZ).
  NOT a visa or titre de séjour number.
- **NOM/surname first**, then given names; date of birth, nationality, and the
  **expiry date**.

## France-Visas wizard result ("Check your visa need" practical sheet)

The PDF/printout produced by the France-Visas assessment wizard. It is NOT an ID
document — it is a **tailored checklist**:

- An **inputs summary** (nationality, visa length requested — short-stay ≤ 90 days /
  long-stay > 90 / airport transit — current residence country, destination, purpose).
- Whether a visa is required ("you will need a visa").
- The **required-documents checklist** under headers (PRE-REQUISITES, CIVIL STATUS,
  MINORS, PURPOSE OF TRAVEL/STAY, FUNDS, FORMS) — this list is the source of truth for
  the person's documents; read it verbatim and confirm possession, do not invent.
- The **fee** ("The amount to be paid is: 99.00 euros …") — use the euro figure, ignore
  the local-currency estimate.

## Extrait Kbis (company registration certificate — from the greffe / RCS)

The official proof a company exists (issued by a **greffe**). Key fields and their traps:

- **Immatriculation au RCS, numéro** in the IDENTIFICATION block → the company's
  **SIREN** (9 digits, strip spaces). Do NOT take the **domiciliataire's** RCS number
  lower down — that is the mailbox provider, not this company.
- **Dénomination ou raison sociale** (e.g. Dupont Conseil SASU) → the company name.
- **Forme juridique**: "Société par actions simplifiée (à associé unique)" → SASU;
  without the mention → SAS; "SARL à associé unique / EURL" → EURL, otherwise SARL;
  "Société anonyme" → SA; "Société civile…" → SCI.
- **Date de clôture de l'exercice social** (e.g. "31 décembre") → the recurring fiscal
  year-end. **This drives the corporate-tax deadline** (filing within ~3 months of
  close; mid-May for a 31 December close).
- **Date de clôture du 1er exercice social** → for a first filing, that exercice's end;
  **date de commencement d'activité** starts the first exercice (it can exceed 12
  months).
- **Président / Gérant — Nom, prénoms** (e.g. Dupont Marie Claire) + date/lieu de
  naissance + nationalité — durable facts about the dirigeant.
- **Origine du fonds = "Création"** + a recent date d'immatriculation ⇒ a newly created
  company (likely its first filing).
- **Adresse du siège** — this is **where DGFiP posts the espace-professionnel
  activation code**, so it matters operationally.
- **Domiciliation / Nom du domiciliataire**, if present: the company's official mail —
  including that activation code — goes to the domiciliataire's address, so it must be
  collected there or forwarded, not at the founder's home.
- **Capital social** is printed on the Kbis — no need to ask.
- **NOT on a Kbis** (must be asked separately): the corporate-tax regime (réel
  simplifié/normal), the VAT regime (franchise art. 293 B / réel), and the bank IBAN —
  tax elections and banking details are never printed there.

## Compte de résultat / bilan / FEC / relevé bancaire (company accounts)

Where the annual-filing figures live, so a person can provide accounts instead of
typing numbers:

- **Compte de résultat**: chiffre d'affaires (produits d'exploitation) → turnover;
  total charges (exploitation + financières + exceptionnelles) → expenses; **résultat
  de l'exercice** (positive bénéfice, negative perte) → accounting result.
- **Bilan**: disponibilités (trésorerie/banque, actif) → cash at year-end; capital
  social (capitaux propres); **comptes courants d'associés** (compte 455, passif).
- **FEC / grand livre / balance**: classe 7 (produits) → turnover, classe 6 (charges) →
  expenses; account 455 → comptes courants d'associés.
- **Relevé bancaire**: closing balance at exercice end cross-checks the bilan.
- These are best-guess extractions — confirm them. Judgment items no document shows
  (e.g. **réintégrations fiscales**) must be asked: résultat fiscal = résultat
  comptable + réintégrations − déductions.

## General

- Dates: prefer ISO `YYYY-MM-DD`; keep month names as printed, don't translate them.
- Amounts: strip thousands separators; keep the decimal. Record the currency if shown.
- Proper names, institutions, and numéros are never translated.
