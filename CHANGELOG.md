# Changelog

All notable changes to Lumia Portal are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Entries before the first release were reconstructed from internal development history.

## [2025.12] - 2025-12-19

_Identity verification and dashboard rework_

### Added

- **backend** — Identity verification completes automatically once the verification provider finishes its review, moving accounts to verified without manual intervention

### Changed

- **frontend** — Dashboard rebuilt with a new component set and typography
- **admin** — Tokenized asset deployment now reads the deployed token address from on-chain event data instead of positional log parsing

### Security

- **backend** — Administrative authorization and session cookie handling hardened
