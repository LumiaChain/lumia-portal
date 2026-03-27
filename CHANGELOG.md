# Changelog

All notable changes to Lumia Portal are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Entries before the first release were reconstructed from internal development history.

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
