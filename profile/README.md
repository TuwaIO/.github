# TUWA

<div align="center">
  <img src="https://raw.githubusercontent.com/TuwaIO/workflows/main/preview/tuwa_preview.gif" alt="TUWA preview: wallet connection, sign-in and transaction tracking" width="100%" />
</div>

<p align="center">
  <strong>Open-source TypeScript toolkit for self-custodial apps on EVM and Solana.</strong>
</p>

<p align="center">
  <a href="https://tuwa.io">Website</a> ·
  <a href="https://docs.tuwa.io">Docs</a> ·
  <a href="https://docs.tuwa.io/playground">Playground</a> ·
  <a href="https://discord.gg/9dN8tkTk7u">Discord</a> ·
  <a href="https://t.me/tuwa_io">Telegram</a> ·
  <a href="https://x.com/tuwa_io">X</a>
</p>

---

TUWA covers the layer every self-custodial app rebuilds: **wallet connection**, **multi-chain sign-in** with one CAIP-122 flow, **transaction tracking** that survives page reloads, **React components** for all of it, and **Quasar**, a backend for transaction history and webhooks that you run in our cloud or on your own servers.

Every package is open source under Apache-2.0, headless and framework-agnostic at its core. Install the whole stack with one SDK, or only the packages you need. TUWA is built in the open by [Oleksandr Tkach](https://tuwa.io/team/oleksandr) in Lviv, Ukraine.

## ⚡ Quick Start

Start from a ready-made Next.js or Vite template:

```bash
npx @tuwaio/create-cosmos-playground
```

Or add TUWA to an existing React app:

```bash
pnpm add @tuwaio/sdk @tuwaio/evm-sdk     # EVM
pnpm add @tuwaio/sdk @tuwaio/solana-sdk  # Solana
```

## 🏗️ How TUWA Is Built

TUWA is built in five stages. Each project depends only on the stages below it, so any of them can be used on its own.

| Stage | Projects | What it does |
| :--- | :--- | :--- |
| **1 — Core Auth & Primitives** | [SIWX](https://siwx.docs.tuwa.io), [Orbit Utils](https://orbit.docs.tuwa.io) | CAIP-122 sign-in for EVM and Solana wallets, verified on your server, and multi-chain helpers |
| **2 — State & Connection** | [Satellite Connect](https://satellite.docs.tuwa.io), [Pulsar](https://pulsar.docs.tuwa.io) | Wallet connection and transaction tracking in headless stores |
| **3 — Backend & Sync** | [Quasar Cloud](https://tuwa.io/quasar), [Quasar Community Edition](https://github.com/TuwaIO/quasar-community) | Server-side transaction tracking, history on every device and signed webhooks |
| **4 — User Interface** | [Nova UI Kit](https://stories.tuwa.io) | React components for Satellite Connect and Pulsar |
| **5 — SDK Integration Layer** | [TUWA SDK](https://sdk.docs.tuwa.io) | One package for React apps, with EVM and Solana add-ons |

## 📦 Repositories

| Repository | Packages | Description |
| :--- | :--- | :--- |
| 🛡️ **[siwx](https://github.com/TuwaIO/siwx)** | `siwx-core` (L1), `siwx-evm`, `siwx-solana`, `siwx-react`, `siwx-server` (L2) | One CAIP-122 sign-in flow for EVM and Solana wallets: EIP-191, EIP-1271 and ERC-6492 verification on every EVM chain, ed25519 on Solana, single-use nonces, sessions, Next.js handlers and JWT + JWKS for external auth providers. |
| 🧬 **[orbit](https://github.com/TuwaIO/orbit)** | `orbit-core` (L1), `orbit-evm`, `orbit-solana` (L2) | Multi-chain helpers: chain and account IDs (CAIP-2, CAIP-10, CAIP-19), cached viem and `@solana/kit` clients, ENS and SNS names, ERC-4337 smart accounts. |
| 🛰️ **[satellite-connect](https://github.com/TuwaIO/satellite-connect)** | `satellite-core` (L3), `satellite-evm`, `satellite-solana`, `satellite-react` (L4) | Headless store for EVM and Solana wallet connections: reconnects the last wallet, follows changes made in the wallet and keeps SIWX sessions in sync. Wallets come from wagmi (EIP-6963) and Wallet Standard. |
| 💡 **[pulsar-core](https://github.com/TuwaIO/pulsar-core)** | `pulsar-core` (L3), `pulsar-evm`, `pulsar-solana`, `pulsar-react` (L4) | Transaction tracking that survives page reloads: pending, successful, failed and replaced transactions, with trackers for EVM, ERC-4337, Safe, Gelato and Solana. |
| ☁️ **[Quasar Cloud](https://tuwa.io/quasar)** | `quasar-sdk` (L5) | Managed backend: tracks your app's transactions on the server until their final status, keeps their history on every device and sends signed webhooks. Usage-based pricing, no per-user fees. [Dashboard](https://quasar.tuwa.io) |
| 🏠 **[quasar-community](https://github.com/TuwaIO/quasar-community)** | — | The open-source (Apache-2.0), self-hosted edition of Quasar, deployed with Docker Compose. Move an organization from Quasar Cloud to your own node at any time. |
| 🎨 **[nova-uikit](https://github.com/TuwaIO/nova-uikit)** | `nova-core` (L6), `nova-connect`, `nova-transactions` (L7) | React components for wallet connection and transactions: connect button and modals, SIWX sign-in, transaction toasts and history, themed with CSS variables. [Storybook](https://stories.tuwa.io) |
| 📦 **[sdk](https://github.com/TuwaIO/sdk)** | `sdk` (L8), `evm-sdk`, `solana-sdk` (L9), `quasar-sdk` (L5) | The TUWA SDK: one package for React apps that re-exports Orbit Utils, SIWX, Satellite Connect, Pulsar and Nova UI Kit, plus the EVM and Solana add-ons and the Quasar API client. |
| 🧪 **[cosmos-playground](https://github.com/TuwaIO/cosmos-playground)** | `create-cosmos-playground` | Starter templates for Next.js and Vite (EVM, Solana, both, or the full stack with Quasar sync) and the CLI that creates them. |
| 📚 **[docs](https://github.com/TuwaIO/docs)** | `docs-ui` | The documentation hub ([docs.tuwa.io](https://docs.tuwa.io)): guides, the Playground, the Stack Configurator, comparisons and the Quasar docs. |
| ⚙️ **[workflows](https://github.com/TuwaIO/workflows)** | — | Shared CI/CD workflows, community guidelines and the [guide for AI coding agents](https://github.com/TuwaIO/workflows/blob/main/TUWA_AGENTS.md). |

Every package with its npm description, peers and the guides that use it: [docs.tuwa.io](https://docs.tuwa.io).

## 🤝 Get Involved

* **💻 Code:** propose improvements or open a pull request in any repository.
* **🐞 Bugs:** file an issue with the steps to reproduce it.
* **💡 Ideas:** share the integration you are building and what is missing.
* **📖 Docs:** make a guide clearer or add an example.

Start with the **[contribution guidelines](https://github.com/TuwaIO/workflows/blob/main/CONTRIBUTING.md)**, and ask questions on [Discord](https://discord.gg/9dN8tkTk7u) or [Telegram](https://t.me/tuwa_io).

## 💬 Support TUWA

If TUWA helps your app, consider supporting its open-source development: **[support options](https://github.com/TuwaIO/workflows/blob/main/Donation.md)**.
