# Generic Intelligence Platform

## Purpose

This module defines a generic intelligence-fact platform for collecting, normalizing, validating, relating, analyzing, and distributing intelligence facts from public sources, commercial data feeds, APIs, internal research, and subscriber submissions.

The platform is intentionally not tied to any one politician, company, jurisdiction, ideology, investigation, or hypothesis. Those become domain-specific workspaces that use the same shared evidence, relationship, confidence, provenance, and distribution model.

## Core principle

The system should treat every submitted or collected item as a candidate intelligence fact until it is normalized, sourced, deduplicated, scored, related, and reviewed.

The durable intelligence asset is not a text paragraph. It is a structured fact with:

- source lineage
- entity resolution
- relationship type
- domain segment
- confidence state
- temporal validity
- geographic scope
- legal/commercial/public-use constraints
- distribution eligibility
- analyst notes and counterarguments

## Logical segments

The platform should divide collection and distribution into logical intelligence segments. A segment is a domain-bounded collection lane with its own vocabulary, source priorities, quality rules, distribution policies, and subscriber products.

Initial segment families:

| Segment | Coverage |
|---|---|
| Government | departments, agencies, Crown corporations, public authorities, budgets, laws, programs |
| Industry | firms, ownership, sectors, production, supply chains, contracts, investment flows |
| Infrastructure | ports, rail, roads, energy, telecom, water, logistics hubs, data centres |
| Transport and logistics | carriers, corridors, terminals, freight flows, capacity, bottlenecks, safety events |
| Defence and security | procurement, dual-use infrastructure, bases, radar, Arctic, interoperability, emergency powers |
| Regulatory and legal | statutes, regulations, permits, approvals, court decisions, enforcement, compliance |
| Finance and capital | ownership, debt, equity, grants, guarantees, subsidies, funds, pension exposure |
| Resources | energy, minerals, agriculture, forestry, water, land, pipelines, transmission |
| Media and narrative | public messaging, media funding, regulator actions, platform policy, narrative shifts |
| Geopolitical | treaties, trade pressure, tariffs, sanctions, alliances, diplomatic events |
| Civic and subscriber intelligence | field observations, submitted leads, documents, photos, local events, corrections |

## Platform pipeline

```text
source intake
  -> ingestion record
  -> source quality assessment
  -> entity extraction
  -> entity resolution
  -> fact normalization
  -> relationship packet generation
  -> evidence graph update
  -> conflict and duplicate detection
  -> confidence scoring
  -> segment assignment
  -> access and distribution policy
  -> subscriber products / API / dashboards / reports
```

## Subscriber-submitted intelligence

Subscriber submissions are valuable but must be isolated from verified facts until reviewed.

Subscriber data should pass through:

1. submission capture
2. contributor identity and permission state
3. source-material attachment
4. claim decomposition
5. duplicate detection
6. corroboration search
7. confidence scoring
8. analyst review
9. segment assignment
10. distribution approval

A subscriber submission can become:

- rejected
- queued
- unverified lead
- corroborated lead
- verified fact
- disputed fact
- superseded fact
- restricted fact

## Distribution model

The platform should support segmented distribution so subscribers receive intelligence products relevant to their interests, geography, industry, or risk exposure.

Distribution channels:

- API feeds
- dashboards
- CSV/JSON exports
- alert streams
- briefings
- intelligence packets
- graph/path queries
- geographic maps
- subscriber watchlists
- evidence bundles

Distribution must respect:

- source licence
- commercial data terms
- privacy constraints
- legal sensitivity
- confidence threshold
- embargo dates
- subscriber entitlement
- security classification or internal handling rules

## Data product examples

| Product | Description |
|---|---|
| Daily segment brief | Summary of high-confidence events in a domain segment |
| Evidence bundle | All sources, claims, relationships, and confidence scores supporting a conclusion |
| Relationship path report | Confidence-rated path between actors, events, mechanisms, and beneficiaries |
| Watchlist alert | Notification when a subscribed entity, region, sector, or mechanism changes |
| Procurement monitor | New contracts, grants, awards, amendments, recipients, and ownership links |
| Regulatory change monitor | New laws, rules, decisions, permit changes, enforcement actions |
| Infrastructure dependency map | Entity and sector dependency paths across physical and economic systems |

## Design boundary

This module defines the generalized collection and intelligence architecture. Specific investigations should be stored as segment workspaces or hypothesis workspaces, not embedded into the platform foundation.

Example:

```text
research/intelligence_platform/                 # generic platform model
research/sovereignty_integration_matrix/        # one hypothesis/workspace using the platform
research/procurement_monitoring/                # another workspace
research/resource_corridors/                    # another workspace
```

## Value proposition

The value is created by turning fragmented facts into structured, queryable intelligence:

- who is involved
- what changed
- when it changed
- where it applies
- what authority was used
- who pays
- who benefits
- what source proves it
- what confidence level applies
- what relationships connect it to broader systems
- which subscribers need to know
