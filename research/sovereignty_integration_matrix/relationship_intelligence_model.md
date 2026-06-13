# Relationship Intelligence Model

## Purpose

This document extends the sovereignty integration evidence matrix into a relationship-first intelligence model. The goal is to make evidence, actors, events, mechanisms, beneficiaries, authority paths, public burden, and confidence scores machine-readable before they are summarized by an LLM.

The LLM must not be treated as the source of truth. The durable intelligence layer is the evidence graph. The LLM is the interface used to query, reason over, challenge, summarize, and brief that graph.

## Core Principle

Normal retrieval asks: what document chunks mention the same words?

Relationship intelligence asks: what evidence-backed relationship paths connect actors, authority, money, policy, timing, mechanisms, beneficiaries, and public burden?

Example:

```text
Trump tariff pressure
  -> creates economic insecurity
  -> Canadian federal response frames sovereignty/urgency
  -> major-project and defence authority expands
  -> infrastructure spending accelerates
  -> capital-intensive sectors benefit
  -> specific firms or asset classes may benefit, subject to proof
```

Each arrow in the path requires an evidence record, confidence score, counterargument, and proof target.

## Architecture

```text
1. Source Layer
   Budgets, contracts, legislation, Hansard, speeches, filings, procurement records,
   ethics records, lobbying records, corporate filings, media reports, court decisions.

2. Extraction Layer
   Extract entities, events, dates, claims, amounts, authorities, relationships,
   beneficiaries, counterarguments, source quality, and proof gaps.

3. Semantic Protocol Layer
   Normalize extracted data into entities, events, mechanisms, relationships,
   states, impacts, roles, confidence, trust, and source traceability.

4. Evidence Graph Layer
   Store durable relationship triples and paths:
   subject -> relationship -> object/event/source/context.

5. Vector Layer
   Embed both source excerpts and relationship packets for semantic retrieval.

6. Reasoning Layer
   LLM receives graph-derived context and returns confidence-rated analysis.

7. Analyst Layer
   Timelines, dashboards, contradiction checks, path scoring, beneficiary maps,
   public burden estimates, and intelligence briefs.
```

## Relationship Packets

A relationship packet is a compact semantic unit that can be stored, embedded, retrieved, and passed to an LLM.

```yaml
relationship_packet:
  packet_id: RP-000001
  hypothesis_id: HYP-SOV-001
  subject_entity: Government of Canada
  relationship_type: allocates_funding_to
  object_entity: Arctic defence infrastructure
  event_context: EVT-ARCTIC-DEFENCE-PLAN
  mechanism:
    - defence_spending
    - infrastructure_buildout
    - arctic_sovereignty
  impact_domain:
    - defence
    - infrastructure
    - sovereignty
    - public_finance
  beneficiary_class:
    - defence_contractors
    - infrastructure_funds
    - engineering_firms
  public_burden_type:
    - taxpayer_cost
    - debt_financing
    - procurement_exposure
  sovereignty_impact: medium
  brookfield_relevance: sector_overlap
  us_relevance: indirect
  evidence_sources:
    - SRC-000001
  confidence_score: 3
  counterargument: Ordinary NATO and Arctic defence policy response.
  proof_target: Contract awards, financing structure, project ownership, and procurement recipients.
  valid_from: 2026-01-01
  valid_to:
```

## Relationship Paths

A path is a chain of relationship packets used to test a larger hypothesis.

```yaml
relationship_path:
  path_id: PATH-000001
  hypothesis_id: HYP-SOV-001
  path_summary: Trade pressure to federal authority expansion to infrastructure beneficiary exposure.
  nodes:
    - Trump tariff pressure
    - Canadian economic insecurity
    - Federal sovereignty response framing
    - Major project authority expansion
    - Infrastructure spending acceleration
    - Capital-intensive sector benefit
  edges:
    - RP-000010
    - RP-000011
    - RP-000012
    - RP-000013
    - RP-000014
  cumulative_confidence: 3.2
  weakest_link: Specific-firm benefit requires direct procurement or ownership proof.
  strongest_evidence: Official announcements, legislation, budget allocations, and procurement records.
  unresolved_gaps:
    - Direct beneficiary contracts
    - Ownership and financing details
    - Cabinet or agency decision records
```

## Relationship Types

Initial canonical relationship types:

```text
associated_with
formerly_affiliated_with
owns_or_controls
has_sector_exposure
allocates_funding_to
creates_authority_for
expands_authority_over
removes_constraint_from
increases_public_burden
reduces_public_oversight
creates_operational_dependency
creates_security_dependency
creates_trade_dependency
potentially_benefits
directly_benefits
contradicts
supports
requires_proof_target
```

## Scoring Dimensions

Each packet should support these scoring dimensions:

```text
source_strength: 1-5
relationship_confidence: 1-5
mechanism_clarity: 1-5
money_materiality: 1-5
sovereignty_impact: none|low|medium|high
public_burden_materiality: none|low|medium|high
beneficiary_specificity: none|class|sector|firm|contract
counterargument_strength: weak|medium|strong
proof_gap_severity: low|medium|high
```

## Query Examples

```sql
-- High-confidence sovereignty-impact events
SELECT *
FROM relationship_packets
WHERE confidence_score >= 4
  AND sovereignty_impact IN ('medium', 'high')
ORDER BY valid_from;

-- Policy events with Brookfield sector overlap but no direct proof yet
SELECT *
FROM relationship_packets
WHERE brookfield_relevance = 'sector_overlap'
  AND relationship_type = 'potentially_benefits'
  AND proof_target IS NOT NULL;

-- Timeline clustering across trade, defence, authority, and money flow
SELECT substr(valid_from, 1, 7) AS month,
       mechanism,
       count(*) AS packet_count
FROM relationship_packets
GROUP BY month, mechanism
ORDER BY month, packet_count DESC;
```

## Valuable Refinements

The following refinements should be implemented as the matrix grows:

1. Entity resolution so that names, subsidiaries, Crown corporations, funds, partnerships, and related parties resolve to durable IDs.
2. Ownership-distance scoring to distinguish sector overlap from direct ownership or contract benefit.
3. Temporal-proximity scoring to test whether pressure events precede policy changes within meaningful windows.
4. Counterargument records as first-class entities, not notes, so innocent explanations can be compared systematically.
5. Source lineage tracking so every conclusion can be traced back to documents, page numbers, table numbers, or URLs.
6. Public-burden accounting for tax cost, debt cost, user fees, regulated rates, monopoly pricing, inflation, guarantees, and contingent liabilities.
7. Path confidence scoring using weakest-link logic rather than averaging unsupported claims into false certainty.
8. Contradiction detection for sources or events that weaken the working hypothesis.
9. Analyst review states: proposed, sourced, reviewed, disputed, accepted, deprecated.
10. Export formats for CSV, SQLite, RDF/OWL, GraphML, JSON-LD, and LLM relationship packets.

## Guardrails

The model must distinguish:

```text
Direct proof        = law, contract, ownership, payment, filing, official transcript.
Strong inference    = multiple credible sources plus clear mechanism.
Weak inference      = plausible but missing direct mechanism or beneficiary proof.
Speculation         = hypothesis without sufficient sourced support.
```

The system should never convert weak inference into a conclusion. Weak links must remain visible in every generated brief.
