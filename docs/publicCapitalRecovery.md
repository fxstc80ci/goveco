# Public Capital Recovery and Loss

## Purpose

This model tracks public money that is expected to return, has returned, has been impaired, has been forgiven, or has become unrecoverable.

## Flow types

Use these controlled values:

- grant
- contribution
- repayable_contribution
- loan
- forgivable_loan
- equity_investment
- capital_injection
- loan_guarantee
- guarantee_called
- tax_remission
- debt_writeoff
- impairment
- dividend_received
- sale_proceeds
- repayment_received

## Recoverability

Use these controlled values:

- unrecoverable_by_design
- conditionally_recoverable
- recoverable
- guaranteed_exposure_only
- impaired
- written_off
- recovered
- unknown

## Core metrics

| Metric | Meaning |
|---|---|
| amount | Original amount recorded. |
| amount_repaid | Cash or value returned. |
| amount_written_off | Amount formally removed as uncollectible. |
| amount_remitted | Dividend, return, or remittance back to government. |
| amount_impaired | Reduction in asset value. |
| net_unrecovered | Remaining unrecovered exposure or cost. |

## Rule

Do not classify grants, loans, guarantees, equity investments, remissions, and write-offs as the same thing. Each has a different public cost and recovery profile.
