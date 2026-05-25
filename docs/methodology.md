# goveco Methodology

## Objective

goveco is an inventory-first research and data framework for mapping the Canadian public-sector ecosystem.

The framework tracks:

1. annual cost and revenue flows;
2. balance-sheet exposure;
3. public capital recovery and loss;
4. governance and accountability;
5. source traceability and confidence.

## Workflow

```text
inventory -> source log -> raw extract -> normalized row -> citation check -> QA -> publish
```

## Inventory-first rule

Every financial, employment, grant, procurement, investment, recovery, write-off, and accountability row must link to an `entity_id`.

## Three-ledger model

### 1. Annual cost ledger

Measures annual cost through taxes, debt, rates, fees, premiums, tolls, fares, tuition, pricing, levies, subsidies, and transfers.

### 2. Balance-sheet exposure ledger

Measures assets, liabilities, debt, guarantees, contingent liabilities, pensions, investments, loans, P3 commitments, and deferred maintenance.

### 3. Capital recovery and loss ledger

Measures amounts expected to return, recovered, unrecovered, impaired, written off, forgiven, remitted, or lost.

## Source rule

No curated number is allowed without `source_id`, fiscal year, unit, basis, extraction date, confidence rating, and source location or note.
