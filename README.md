# Uniswap-token-lists-on-GitHub-The-Token-Lists-specification-for-ERC-20-token-metadata.
About
This repo defines a standard JSON schema and TypeScript utilities that describe how token lists should be structured for use in decentralized apps (like the Uniswap interface).

A “token list” is essentially a JSON file containing metadata for multiple ERC-20 tokens (e.g., name, symbol, address, decimals, logo URI, chain ID, etc.).

Any project (wallet, DEX, dashboard) can create and publish a list that conforms to this schema, and then dApps can consume it to show available tokens to users.

Key Features of the Repo:
✔ Provides a JSON schema (uniswap.org/tokenlist.schema.json) defining required and optional fields in a token list.
✔ Contains TypeScript types and utilities for building and validating lists.
✔ Lists follow semantic versioning rules — crucial for UI clients to detect updates.
✔ You can host lists on HTTPS, ENS, or IPFS and reference them in interfaces like Uniswap’s.

How It’s Used:

When building a swap or portfolio UI, developers fetch token list JSON from one or more URLs that comply with this spec.

Interfaces like the Uniswap dApp use lists to decide which tokens to show in their token selector, instead of manually hard-coding tokens.

Third-party communities can publish curated lists (e.g., stablecoins, major DeFi tokens, L2 tokens).

Getting Started:

You can use this with npm: npm install @uniswap/token-lists and then import the schema to validate your own list structure in code.

Typical workflow involves generating a list, validating it against the schema, and hosting it where dApps can fetch it.
