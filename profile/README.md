# Welcome to the TUWA GitHub Organization!

<div align="center">
  <img src="https://raw.githubusercontent.com/TuwaIO/workflows/main/preview/tuwa_preview.gif" alt="TUWA Preview Demo" width="100%" max-width="800px" />
</div>

<p align="center">
  <strong>Building Modular, Self-Custodial & High-Performance Web3 Infrastructure.</strong>
</p>

---

Welcome! We are **TUWA**, an engineering team and open-source collective dedicated to building headless, framework-agnostic, and self-custodial Web3 technologies. Our mission is to provide developers with modular infrastructure across EVM and Solana, decoupling complex blockchain connection and transaction state management from beautiful visual interfaces.

This organization serves as the central hub for all TUWA public monorepositories, SDKs, UI component libraries, and community standards.

---

## 🏗️ Ecosystem Architecture

The TUWA Ecosystem is structured into 5 decoupled layer stages:

- **Stage 1 — Foundational Core (L1/L2):** Multi-chain primitives and network validation adapters ([`orbit`](#-%EF%B8%8F-featured-repositories-and-packages)).
- **Stage 2 — State & Connection (L3/L4):** Headless wallet connection state machine ([`satellite-connect`](#-%EF%B8%8F-featured-repositories-and-packages)) and real-time transaction lifecycle engine ([`pulsar-core`](#-%EF%B8%8F-featured-repositories-and-packages)).
- **Stage 3 — Cloud Integration (L5):** High-performance backend API, transaction indexing, and organization telemetry ([`quasar`](#-%EF%B8%8F-featured-repositories-and-packages)).
- **Stage 4 — User Interface (L6/L7):** High-performance React UI components, modals, feeds, and design system ([`nova-uikit`](#-%EF%B8%8F-featured-repositories-and-packages)).
- **Stage 5 — SDK Integration Layer (L8/L9):** Unified client SDK wrappers for single-line dApp initialization ([`sdk`](#-%EF%B8%8F-featured-repositories-and-packages)).

---

## ⚡ Quick Start

Bootstrap a ready-to-use TUWA Web3 project template pre-configured with EVM, Solana, or full-stack cloud synchronization:

```bash
npx @tuwaio/create-cosmos-playground
```

---

## ✨ Featured Repositories and Packages

Explore our modules below:

| Repository or Package | Stage / Layer | Description |
| :--- | :---: | :--- |
| **⚙️ [workflows](https://github.com/TuwaIO/workflows)** | — | Central hub for **CI/CD automation pipelines**, security standards, and community guidelines. |
| **📚 [docs](https://github.com/TuwaIO/docs)** | — | Unified **Documentation Hub** (`https://docs.tuwa.io`) for the entire TUWA Ecosystem. |
| **🧬 [orbit-core](https://github.com/TuwaIO/orbit/tree/main/packages/orbit-core)** | **L1** | Framework-agnostic multi-chain **primitives**, types, validation helpers, and storage utilities. |
| **⚡ [orbit-evm](https://github.com/TuwaIO/orbit/tree/main/packages/orbit-evm)** | **L2** | **EVM chain adapter** powered by `viem` and `@wagmi/core`. RPC client creation and ENS resolution. |
| **🌟 [orbit-solana](https://github.com/TuwaIO/orbit/tree/main/packages/orbit-solana)** | **L2** | **Solana chain adapter** powered by `gill` and `@wallet-standard`. Cluster management & RPC helpers. |
| **🛰️ [satellite-core](https://github.com/TuwaIO/satellite-connect/tree/main/packages/satellite-core)** | **L3** | Headless universal **wallet connection state machine** powered by Zustand and Immer. |
| **🔌 [satellite-evm](https://github.com/TuwaIO/satellite-connect/tree/main/packages/satellite-evm)** | **L4** | **EVM wallet connector** logic integrating Wagmi and Viem provider adapters. |
| **🌟 [satellite-solana](https://github.com/TuwaIO/satellite-connect/tree/main/packages/satellite-solana)** | **L4** | **Solana wallet connector** logic integrating Wallet Standard and Gill helpers. |
| **⚛️ [satellite-react](https://github.com/TuwaIO/satellite-connect/tree/main/packages/satellite-react)** | **L4** | **React hooks and context providers** for seamless headless wallet connection management. |
| **🔐 [satellite-siwe-next-auth](https://github.com/TuwaIO/satellite-connect/tree/main/packages/satellite-siwe-next-auth)** | **L4** | **Sign-In with Ethereum (SIWE)** authentication integration for Next.js powered by `iron-session`. |
| **💡 [pulsar-core](https://github.com/TuwaIO/pulsar-core/tree/main/packages/pulsar-core)** | **L3** | Headless framework-agnostic **transaction lifecycle state machine** (pending, success, failed, replaced). |
| **⚡ [pulsar-evm](https://github.com/TuwaIO/pulsar-core/tree/main/packages/pulsar-evm)** | **L4** | **EVM transaction tracking adapter** for polling and receipt verification. |
| **🌟 [pulsar-solana](https://github.com/TuwaIO/pulsar-core/tree/main/packages/pulsar-solana)** | **L4** | **Solana transaction signature tracker** subscribing to modern RPC WebSocket streams. |
| **⚛️ [pulsar-react](https://github.com/TuwaIO/pulsar-core/tree/main/packages/pulsar-react)** | **L4** | **React bindings and hooks** for automated transaction lifecycle management in React dApps. |
| **☁️ [quasar-dashboard](https://quasar-stg.tuwa.io/)** | **L5** | **Cloud Layer & SaaS Backend**. Manage your Quasar apps and API keys. Next.js Dashboard, NestJS Engine API ("Iron Dome" guard), and BullMQ transaction indexing. |
| **📦 [quasar-sdk](https://github.com/TuwaIO/sdk/tree/main/packages/quasar-sdk)** | **L5** | Official **TypeScript SDK** for interacting with Quasar cloud services, API key authentication, and telemetry. |
| **🎨 [nova-core](https://github.com/TuwaIO/nova-uikit/tree/main/packages/nova-core)** | **L6** | Foundation UI layer: **Tailwind CSS v4 design tokens**, CSS variables, and zero-Web3 styling primitives. |
| **🖼️ [nova-connect](https://github.com/TuwaIO/nova-uikit/tree/main/packages/nova-connect)** | **L7** | Multi-chain **wallet connection React components**, modals, and account dropdowns. Built on `@tuwaio/satellite-react`. |
| **🧾 [nova-transactions](https://github.com/TuwaIO/nova-uikit/tree/main/packages/nova-transactions)** | **L7** | **Transaction visualization UI**: status toasts, activity feeds, and confirmation modals. Built on `@tuwaio/pulsar-react`. |
| **📦 [sdk](https://github.com/TuwaIO/sdk/tree/main/packages/sdk)** | **L8** | Core **TUWA Client SDK** unifying Satellite, Pulsar, and Orbit into a single entry point. |
| **⚡ [evm-sdk](https://github.com/TuwaIO/sdk/tree/main/packages/evm-sdk)** | **L9** | Pre-configured **EVM Client SDK** optimized for Ethereum, Polygon, Arbitrum, and EVM chains. |
| **🌟 [solana-sdk](https://github.com/TuwaIO/sdk/tree/main/packages/solana-sdk)** | **L9** | Pre-configured **Solana Client SDK** optimized for Solana mainnet, devnet, and custom RPC clusters. |
| **🧪 [cosmos-playground](https://github.com/TuwaIO/cosmos-playground)** | — | Interactive **playground & starter templates** (`@tuwaio/create-cosmos-playground`) for building dApps with TUWA. |

---

## 🤝 Get Involved

We invite developers and open-source contributors from around the world to collaborate with us:

* **💻 Code Contributions:** Propose enhancements or submit pull requests across any repository.
* **🐞 Bug Reports:** Help us harden our libraries by filing detailed issues.
* **💡 Feature Requests:** Share architectural ideas and dApp integration use cases.
* **📖 Documentation:** Improve guide clarity, API reference coverage, and code examples.

To get started, please review our **[Contribution Guidelines](https://github.com/TuwaIO/workflows/blob/main/CONTRIBUTING.md)**.

---

## 💬 Community & Support

If you find TUWA infrastructure valuable for your dApps, consider supporting our open-source development.

[**➡️ View Support Options**](https://github.com/TuwaIO/workflows/blob/main/Donation.md)

<p align="center">
  <b>Built with ❤️ by TUWA.</b><br/>
  Together, let’s build the Web3 future!
</p>
