# goveco

Government Ecosystem Cost, Exposure, Recovery, and Accountability Framework.

## Purpose

goveco is an inventory-first research and data framework for mapping the full Canadian public ecosystem: federal, provincial, territorial, municipal, Indigenous, Crown, delegated, contractor, and publicly funded private entities.

The objective is to answer four questions:

1. How large is the public ecosystem?
2. What does it cost citizens every year through taxes, debt, rates, fees, premiums, fares, tuition, monopoly pricing, and levies?
3. What assets, liabilities, debts, guarantees, and contingent exposures sit on or near the public balance sheet?
4. What public money is recoverable, unrecoverable, impaired, written off, forgiven, remitted, or still outstanding?

## Core principle

Do not treat gross spending, direct taxpayer appropriations, and citizen-funded charges as the same thing.

A public entity may be described as self-funded, but that does not mean it is cost-free. The cost may be borne by citizens, ratepayers, fee-payers, consumers, students, passengers, shippers, drivers, employers, employees, property owners, businesses, regulated industries, or future taxpayers.

goveco therefore measures both:

- direct taxpayer cost; and
- total public/economic burden.

## Accountability principle

No public burden without public accountability.

If an entity is publicly owned, publicly funded, publicly guaranteed, protected by monopoly rights, empowered by statute, or delegated public authority, goveco tracks whether citizens can see, challenge, audit, influence, vote on, or constrain that entity.

## Repository layout

```text
docs/       Methodology, consolidation rules, accountability model, source rules, data dictionary.
schemas/    YAML schemas for curated data tables.
templates/  Research and QA templates.
data/       Raw, staged, curated, and published datasets.
sources/    Source registry and document tracking.
research/   Jurisdiction/entity research files.
reports/    Generated analysis reports.
scripts/    Extraction, normalization, validation, and publishing scripts.
website/    Future public dashboard and drill-down explorer.
issues/     Data gaps, source conflicts, QA exceptions.
```

## Workflow

```text
inventory -> source log -> raw extract -> normalized row -> citation check -> QA -> publish
```

## Initial scope

Start federal, then expand province by province and municipality by municipality:

1. Federal departments and agencies.
2. Federal Crown corporations.
3. Federal Crown subsidiaries and holdings.
4. Federal government business enterprises.
5. Federal grants, contributions, loans, guarantees, write-offs, remissions, and strategic investments.
6. Provincial ministries, agencies, health authorities, school boards, colleges, universities, utilities, liquor/gaming, WCBs, and Crown corporations.
7. Municipal governments, utilities, police, transit, libraries, housing corporations, economic development corporations, and local business enterprises.
8. Indigenous governments, trusts, development corporations, and public authorities.
9. NGOs, contractors, consultants, and private firms materially dependent on public contracts.

## Status

Foundation created. Next step: seed federal entity inventory and source registry from official anchor sources.