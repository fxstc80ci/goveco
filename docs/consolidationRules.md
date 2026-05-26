# Consolidation Rules

## Purpose

Consolidation rules prevent double-counting when money flows across governments, agencies, Crowns, subsidiaries, contractors, and recipients.

## Required distinction

Each amount must be classified as one of:

- gross entity activity;
- inter-entity transfer;
- consolidated public cost;
- citizen-funded charge;
- balance-sheet exposure;
- recoverable capital; or
- unrecoverable cost.

## Rules

| Scenario | Rule |
|---|---|
| Federal transfer to province, then province funds agency | Show both flow records, but count once in consolidated national public cost. |
| Parent Crown funds subsidiary | Preserve parent-child relationship and use consolidation flags to avoid duplicate totals. |
| Government pays NGO, NGO pays contractors | Track downstream chain, but do not add every layer into one total cost. |
| Utility is ratepayer funded | Count as public ecosystem burden, not direct taxpayer cost. |
| Crown corporation is profitable | Track gross activity, citizen-funded revenue, and remittances separately. |
| Guarantee issued | Record exposure. Count expense only if called, impaired, subsidized, or provisioned. |
| Grant issued | Treat as unrecoverable unless documented repayment rights exist. |
| Loan issued | Treat as asset until repaid, impaired, forgiven, or written off. |
| Tax expenditure | Track separately from direct cash spending. |
| P3 availability payment | Track annual payment and remaining future obligation. |

## Required fields

Rows used in consolidated reporting must include:

- `consolidation_scope`
- `counterparty_entity_id`
- `is_inter_entity_flow`
- `is_eliminated_in_consolidation`
- `consolidation_notes`
