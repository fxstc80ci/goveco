# Sovereignty Integration Matrix Methodology

Status: working draft  
Author: Craig MacPherson / Arti Muse  
Created: 2026-06-13

## Objective

Build a disciplined evidence system for testing whether public policy, foreign pressure, institutional authority, private capital, and infrastructure spending are converging in ways that dilute Canadian sovereignty or public accountability.

This is an intelligence-style research matrix, not a conclusion file.

## Evidence rule

Every evidence row must separate:

- observable event
- actor
- source
- mechanism
- beneficiary
- impact
- counterargument
- confidence
- proof target

No row should assert motive unless the source directly establishes it. Motive should be recorded as an inference, not a fact.

## Required row logic

A row is valid only when it can answer:

1. What happened?
2. When did it happen?
3. Who acted or benefited?
4. What source supports the claim?
5. What source type is it?
6. What mechanism is alleged or observed?
7. What public burden, authority shift, sovereignty impact, or money flow is involved?
8. What is the strongest benign or routine-policy explanation?
9. What evidence would confirm, weaken, or falsify the row?

## Source quality ranking

| Rank | Source type | Use |
|---:|---|---|
| 5 | Primary legal or financial document | Statute, bill, regulation, contract, budget, audited financial statement, ethics filing, registry filing |
| 4 | Official transcript or government release | Hansard, committee transcript, PMO release, department release, procurement notice |
| 3 | Reputable factual reporting | Established media article with named documents, dates, and attributable facts |
| 2 | Partisan, advocacy, or opinion source | Useful lead only; requires independent confirmation |
| 1 | Social media, unsourced claim, anonymous assertion | Research lead only; not evidence without corroboration |

## Confidence score

| Score | Meaning |
|---:|---|
| 1 | Speculation or weak signal; no hard evidence yet |
| 2 | Weak support; mostly rhetoric or circumstantial alignment |
| 3 | Plausible link with credible source but incomplete mechanism or beneficiary proof |
| 4 | Strong evidence of mechanism, legal authority, money flow, or beneficiary alignment |
| 5 | Direct documentary proof: law, contract, filing, audited number, transcript, ownership record, payment record |

## Support classification

| Value | Meaning |
|---|---|
| supports | The evidence materially supports the hypothesis or a sub-claim |
| weakly_supports | The evidence is relevant but incomplete or circumstantial |
| neutral | Relevant context but not probative |
| contradicts | Evidence cuts against the hypothesis or sub-claim |
| unresolved | Requires follow-up before classification |

## Semantic discipline

Use controlled terms wherever possible.

Preferred terms:

- sovereignty_dilution
- continental_integration
- security_industrial_policy
- emergency_authority
- public_private_capital_alignment
- state_narrative_capacity
- resource_security
- dual_use_infrastructure
- public_burden
- conflict_risk
- beneficiary_alignment

Avoid storing rhetorical conclusions such as "corruption proven" or "NWO proven" unless a source directly supports that exact claim. Instead, model the observable structure:

- actor said X
- government authorized Y
- project funded Z
- beneficiary owns A
- policy affects B
- confidence is C

## Counterargument requirement

Every substantive row must include the strongest non-conspiratorial explanation. Examples:

- defence spending may reflect NATO and Arctic obligations
- trade diversification may reduce U.S. dependency rather than prepare integration
- infrastructure firms may benefit because they are the normal sector participants
- public broadcasting protection may be framed as institutional stability rather than control
- emergency-style approvals may address infrastructure paralysis rather than authoritarian centralization

If the row remains significant after the counterargument, it becomes more useful.

## Proof target examples

| Suspicion | Proof target |
|---|---|
| Brookfield or adjacent capital benefits | contracts, financing agreements, project ownership, lobbying records, procurement awards |
| conflict-risk survives blind trust | ethics filings, recusal screens, asset declarations, committee testimony, blind trust terms |
| emergency authority expands | bill text, orders-in-council, cabinet authorities, sunset clauses, judicial review limits |
| media control expands | statutory funding language, regulator powers, takedown authority, platform rules |
| sovereignty is diluted | treaties, MOUs, command/control agreements, procurement interoperability, resource guarantees |
| public burden grows | appropriations, tax expenditures, debt, guarantees, ratepayer charges, user fees, insurance premiums |

## Query goals

The matrix should eventually support queries such as:

```sql
SELECT *
FROM evidence_matrix
WHERE confidence >= 4
  AND sovereignty_impact IN ('medium', 'high')
ORDER BY event_date;
```

```sql
SELECT *
FROM projects_money_flow
WHERE brookfield_relevance IN ('sector_overlap', 'direct_contract', 'direct_ownership')
ORDER BY amount_cad DESC;
```

```sql
SELECT substr(event_date, 1, 7) AS month, lane, count(*) AS events
FROM timeline
GROUP BY month, lane
ORDER BY month, events DESC;
```
