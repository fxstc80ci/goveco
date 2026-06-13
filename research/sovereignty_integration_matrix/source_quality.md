# Source Quality Guide

Status: working draft  
Author: Craig MacPherson / Arti Muse  
Created: 2026-06-13

## Purpose

This file defines how sources are ranked and used in the sovereignty integration evidence matrix.

The goal is to preserve credibility by distinguishing hard evidence from leads, opinion, inference, and speculation.

## Source quality levels

| Rank | Label | Examples | Matrix use |
|---:|---|---|---|
| 5 | primary_document | statute, bill, regulation, contract, budget table, audited financial statement, procurement award, ethics filing, corporate registry filing | Can directly support high-confidence factual rows |
| 4 | official_record | Hansard, committee transcript, PMO release, departmental release, regulator notice, order-in-council summary | Strong source for official positions and stated authority |
| 3 | factual_reporting | established media reporting that cites documents, dates, named sources, or direct quotes | Good lead or support; verify major claims against primary records where possible |
| 2 | partisan_or_advocacy | party release, lobby group, advocacy report, opinion editorial | Research lead only unless backed by primary documents |
| 1 | social_or_unsourced | social media, anonymous claim, screenshots without provenance, unsourced commentary | Lead only; do not use as evidence without corroboration |

## Source handling rules

1. Prefer primary documents over commentary.
2. Store exact source title, URL, publisher, date, and access date when available.
3. Record whether the source proves the event, the interpretation, or only a related fact.
4. Do not convert partisan framing into factual language.
5. If a source is partisan but cites a document, locate the document.
6. If a claim is repeated by multiple sources but all trace back to one weak source, treat it as one weak source.
7. If an official document contradicts reporting, record both and mark the row unresolved until reconciled.

## Inference handling

Permitted inference:

- A policy affects a sector where a named entity has documented exposure.
- A funding program creates a public burden through debt, taxation, regulated rates, or guarantees.
- A defence or trade agreement may reduce practical policy freedom if it imposes binding obligations.

Not permitted as fact without proof:

- hidden motive
- secret coordination
- illegal conduct
- deliberate sabotage
- personal enrichment
- formal sovereignty transfer

These may be tracked as hypotheses or proof targets, not conclusions.

## Confidence upgrade path

A row can move from confidence 1-2 to confidence 3-5 only when evidence improves:

- rhetoric becomes policy text
- policy text becomes spending authority
- spending authority becomes procurement or contract
- contract maps to beneficiary ownership or financing
- beneficiary maps to actor interest or conflict-risk evidence
- public cost maps to audited expense, debt, guarantee, ratepayer burden, or user fee

## Recommended citation fields for future database migration

- source_id
- title
- publisher
- author
- publication_date
- access_date
- url
- archived_url
- source_type
- source_rank
- excerpt
- extracted_fact
- limitations
- related_evidence_ids
