# Changelog

All notable changes to Lumia Portal are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Entries before the first release were reconstructed from internal development history.

## [2026.05] - 2026-05-29

_Order flow rebuilt, live pricing, operator analytics_

### Added

- **frontend** — New order placement flow with a step-by-step progress view and clearer trade URLs
- **frontend** — Several orders can be submitted in a single batch transaction
- **backend** — Market prices stream to connected clients in real time instead of being polled
- **admin** — Order analytics dashboard with per-status counts, health cards, a needs-attention filter and pagination
- **admin** — Order detail view shows an on-chain event timeline, a change log and the settlement transaction
- **admin** — Liquidity pool deposits and withdrawals are handled as separate operations

### Changed

- **frontend** — Sidebar navigation redesigned
- **backend** — The platform was migrated to TypeScript end to end, tightening the contracts between services

### Fixed

- **backend** — Settlement contract updates are applied correctly, and user names are stored as entered
- **frontend** — The status timeline no longer keeps spinning after an order completes

### Security

- **backend** — On-chain order event processing hardened with identity verification
- **backend** — Service secrets are held in a dedicated vault

## [2026.03] - 2026-03-27

_Security tokens and multisig wallets_

### Added

- **backend** — Support for ERC-1400 security tokens, covering both tokenized real-world assets and offerings
- **frontend** — Multisig wallets can be used to sign and submit transactions
- **admin** — Operators can create and manage ERC-1400 assets and their offerings

### Changed

- **backend** — Identity verification reworked to run independently of the previous wallet identity provider

## [2026.02] - 2026-02-20

_Credit scoring and permissioned tokens_

### Added

- **backend** — Credit score data is available through the API and surfaced on the user's profile
- **backend** — Support for permissioned ERC-3643 tokens, allowing regulated assets with transfer restrictions
- **frontend** — Credit score is shown in the interface alongside the tokenization entry point

### Fixed

- **frontend** — Asset prices returned by the oracle are no longer displayed incorrectly
- **backend** — Transactions that previously failed during submission now complete

## [2025.12] - 2025-12-19

_Identity verification and dashboard rework_

### Added

- **backend** — Identity verification completes automatically once the verification provider finishes its review, moving accounts to verified without manual intervention

### Changed

- **frontend** — Dashboard rebuilt with a new component set and typography
- **admin** — Tokenized asset deployment now reads the deployed token address from on-chain event data instead of positional log parsing

### Security

- **backend** — Administrative authorization and session cookie handling hardened
