# Sovereignty Integration Evidence Matrix

Status: working research framework  
Author: Craig MacPherson / Arti Muse  
Created: 2026-06-13

## Purpose

This module tracks whether Canadian federal policy, foreign pressure, emergency authority, defence spending, media policy, resource strategy, and private-capital beneficiaries are converging toward sovereignty dilution, continental security-industrial integration, or other measurable shifts in public accountability.

The framework is designed to prevent conclusion-first analysis. Each claim must be decomposed into evidence, source quality, mechanism, beneficiary, sovereignty impact, counterargument, confidence, and follow-up proof target.

## Core hypothesis under test

Canada may be undergoing a crisis-driven strategic repositioning in which trade pressure, defence dependency, resource control, infrastructure buildout, emergency-style authority, and private-capital alignment reduce practical sovereignty even if formal legal sovereignty remains intact.

This hypothesis is not assumed to be true. The matrix is built to test whether the evidence supports, weakly supports, contradicts, or fails to support it.

## Research lanes

| Lane | What it tests |
|---|---|
| rhetoric_ideology | Public statements, speeches, strategic doctrine, new-order language, sovereignty framing |
| legal_authority | Statutes, bills, orders-in-council, emergency powers, mandate authorities, regulatory changes |
| money_flow | Public spending, guarantees, procurement, loans, subsidies, tax incentives, public-private financing |
| beneficiary_mapping | Corporations, funds, Crown corporations, pension funds, banks, contractors, consultants |
| defence_integration | NORAD, NATO, Arctic, procurement, bases, radar, drones, ports, dual-use infrastructure |
| trade_pressure | Tariffs, USMCA uncertainty, export controls, resource restrictions, border policy |
| media_narrative | CBC, online harms, platform regulation, misinformation authority, state-funded messaging |
| resource_control | Energy, water, minerals, agriculture, lumber, pipelines, ports, rail, Arctic corridors |
| constitutional_impact | Federal-provincial powers, Indigenous rights, treaties, courts, democratic accountability |
| timeline_synchronization | Clustering of policy, trade, defence, media, and capital events over time |

## Files

| File | Purpose |
|---|---|
| evidence_matrix.csv | Main claim/evidence/mechanism/confidence table |
| actors.csv | Actor registry and linked interests |
| projects_money_flow.csv | Project, procurement, grant, guarantee, and ownership tracking |
| timeline.csv | Chronological event clustering table |
| methodology.md | Rules for source handling, confidence scoring, and semantic discipline |
| source_quality.md | Source quality taxonomy |
| open_questions.md | Research backlog and proof targets |
| schemas/evidence_matrix.schema.yaml | Machine-readable schema for database migration |

## Semantic rule

Do not store conclusions as facts. Store observable claims, sources, mechanisms, relationships, and confidence levels.

A valid row must answer:

1. What happened?
2. Who acted?
3. What source proves the observable event?
4. What power, money, legal, or narrative mechanism changed?
5. Who benefits?
6. What is the sovereignty or accountability impact?
7. What is the strongest non-conspiratorial explanation?
8. What evidence would raise or lower confidence?

## Migration path

Start in CSV for simple research capture. Migrate to SQLite/Postgres when row volume justifies querying across actors, beneficiaries, legal authorities, events, and source lineage.
