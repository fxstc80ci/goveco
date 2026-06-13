# Intelligence Fact Network

## Purpose

The Intelligence Fact Network is a generic evidence and relationship architecture for capturing, structuring, validating, segmenting, and distributing intelligence facts from public, commercial, subscriber-submitted, and internal data sources.

This framework is not specific to any single person, company, party, industry, or hypothesis. It is designed to support repeatable intelligence collection across government, industry, transportation, infrastructure, finance, defence, regulatory, legal, environmental, supply-chain, media, and public-accountability domains.

## Core principle

The unit of intelligence is not a document, article, social post, or LLM summary.

The durable unit is an evidence-backed fact or relationship:

```text
source -> claim -> normalized fact -> relationship -> context -> confidence -> distribution segment
```

A model may summarize the intelligence, but the system of record must preserve:

- source lineage
- evidence text or reference
- entity resolution
- relationship type
- temporal validity
- confidence score
- counterargument or uncertainty
- subscriber/API provenance
- licensing and redistribution limits
- semantic segment assignment

## Intended inputs

The framework supports multiple input classes:

| Input class | Examples |
|---|---|
| Public records | legislation, budgets, procurement, grants, contracts, lobbyist registries, filings, court records |
| Public web | news, official releases, regulatory updates, parliamentary records, municipal agendas |
| Commercial data | corporate registries, market feeds, shipping data, ownership datasets, credit/risk feeds |
| Subscriber submissions | field observations, documents, tips, datasets, corrections, dispute evidence |
| Internal research | curated CSV/YAML facts, analyst notes, manual evidence packets |
| API feeds | CKAN, open data portals, EDGAR/SEDAR+, procurement APIs, GIS feeds, fleet/asset APIs |
| Derived intelligence | entity resolution, relationship paths, timing clusters, confidence scoring, centrality metrics |

## Logical segmentation

Data should be partitioned into logical intelligence segments so collection, review, enrichment, access control, and distribution can be focused.

Example top-level segments:

| Segment | Scope |
|---|---|
| government | departments, agencies, Crown corporations, public authorities, programs, budgets |
| procurement | tenders, awards, vendors, contract amendments, standing offers, purchase orders |
| grants_transfers | grants, subsidies, contributions, guarantees, loans, tax credits |
| infrastructure | roads, rail, ports, airports, pipelines, transmission, utilities, public works |
| transportation_logistics | carriers, corridors, terminals, vessels, rolling stock, freight flows, intermodal nodes |
| energy_resources | oil, gas, power, nuclear, renewables, water, minerals, forestry, agriculture |
| defence_security | defence spending, dual-use infrastructure, bases, radar, Arctic, cyber, emergency powers |
| regulatory_legal | laws, regulations, orders, permits, approvals, court decisions, enforcement actions |
| ownership_finance | ownership, beneficial control, financing, debt, equity, funds, pensions, asset managers |
| media_narrative | public messaging, state media funding, platform policy, censorship/removal authority, influence campaigns |
| public_burden | taxes, fees, regulated rates, user charges, debt, inflation, monopoly pricing, indirect costs |
| risk_events | failures, disputes, protests, incidents, insolvency, sanctions, supply-chain disruptions |

Segments are not silos. They are indexing and distribution boundaries. A fact may belong to many segments.

## Fact lifecycle

```text
ingest -> normalize -> resolve entities -> classify segment -> extract relationships -> score confidence -> review -> publish/distribute -> monitor changes
```

## Subscriber submission lifecycle

Subscriber-submitted information must be treated as unverified until corroborated.

```text
submit -> provenance capture -> duplicate check -> entity match -> evidence review -> confidence assignment -> dispute window -> publish or reject
```

Minimum subscriber submission metadata:

- submitter ID or anonymous channel ID
- submission timestamp
- claimed event date
- source type
- raw artifact reference
- permission/rights status
- confidentiality level
- claimed entities
- claimed location/jurisdiction
- asserted relationships
- corroborating evidence
- reviewer status

## Distribution model

Intelligence should be distributed by segment, subscriber entitlement, source license, confidence level, jurisdiction, and use case.

Example distribution channels:

| Channel | Output |
|---|---|
| public portal | open evidence, public dashboards, downloadable CSV/JSON |
| subscriber brief | segment-specific intelligence summaries |
| API | normalized facts, relationships, graph paths, alerts |
| analyst workbench | unresolved facts, conflicts, proof gaps, reviewer queues |
| graph export | Neo4j, GraphML, RDF/OWL, JSON-LD |
| LLM context export | evidence packets and relationship paths for reasoning models |

## Non-negotiable controls

- Do not hard-code named actors into the model.
- Do not treat subscriber submissions as facts until reviewed.
- Do not let LLM-generated summaries become source evidence.
- Preserve source lineage and licensing limits.
- Track uncertainty, counterarguments, and proof gaps.
- Separate direct evidence from inference.
- Score relationship confidence independently from narrative confidence.
- Maintain temporal validity for changing facts.
- Allow corrections, disputes, and retractions.

## Relationship to sovereignty integration matrix

The sovereignty integration matrix is one possible use case of the Intelligence Fact Network. It should consume the generic fact and relationship architecture rather than define the architecture.

This allows the same model to support:

- public burden analysis
- government growth tracking
- procurement intelligence
- industry corridor intelligence
- transportation/logistics intelligence
- regulatory monitoring
- ownership and beneficiary mapping
- risk/event monitoring
- subscriber-driven field intelligence
