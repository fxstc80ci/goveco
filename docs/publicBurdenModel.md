# Public Burden Model

## Purpose

The public burden model separates gross activity from the amount ultimately borne by taxpayers, users, ratepayers, consumers, businesses, or future taxpayers.

## Core rule

Do not treat gross spending, direct appropriations, and citizen-funded charges as the same thing.

A public entity may be described as self-funded, but the funding can still come from citizens or businesses through rates, fees, premiums, fares, tolls, tuition, levies, monopoly pricing, or regulated charges.

## Primary metrics

| Metric | Meaning |
|---|---|
| gross_entity_spend | Total expenses reported by the entity. |
| direct_taxpayer_cost | Direct appropriations, subsidies, grants, or debt-funded support. |
| citizen_funded_revenue | Revenue collected from users, ratepayers, consumers, students, employers, or regulated parties. |
| public_debt_burden | Amount financed through public borrowing or shifted to future taxpayers. |
| public_balance_sheet_exposure | Loans, guarantees, equity, liabilities, or contingent exposure. |
| net_public_burden | Consolidated annual burden after offsets, remittances, repayments, and recovery classification. |

## Funding channels

Use controlled values from `schemas/annualCosts.schema.yaml`.

## Burden holders

Every annual cost row should identify who bears the cost where available: taxpayer, ratepayer, fee_payer, consumer, student, passenger, shipper, driver, employer, employee, property_owner, business_customer, regulated_industry, future_taxpayer, public_balance_sheet, or unknown.
