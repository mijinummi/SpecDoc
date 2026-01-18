# SpecDoc: Documentation-as-Code Translator

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Ecosystem: Stellar/EVM](https://img.shields.io/badge/Ecosystem-Stellar%20%7C%20EVM-purple.svg)](https://stellar.org)
[![DX: Interactive](https://img.shields.io/badge/DX-Interactive%20Sandbox-green.svg)](#)

**SpecDoc** is an open-source tool that automatically converts Smart Contract ABIs (Ethereum) and Spec Files (Soroban/Stellar) into beautiful, interactive documentation portals. Designed as the **"Swagger for Web3,"** SpecDoc bridges the gap between raw code and developer adoption.

---

### 1. Executive Summary
The hardest part of a new developer’s journey is the first integration. SpecDoc removes this friction by turning complex contract metadata into a hosted sandbox. It doesn't just list functions; it provides a **live environment** where developers can connect their wallets, input parameters, and execute contract calls directly from the documentation. 

### 2. The Problem
Web3 onboarding is currently broken by "Documentation Decay":
* **Outdated Docs:** Documentation is often a manual effort that falls behind the actual deployed code.
* **High Friction:** Developers must often build custom UIs or use complex CLI tools just to test a single function of a new protocol.
* **Ecosystem Silos:** Tooling is often fragmented between Stellar's Rust-based specs and Ethereum's JSON ABIs.

### 3. Key Features
* **⚡ Instant Portal Generation:** Upload an ABI or Soroban Spec file and generate a fully-functional documentation site in seconds.
* **🧪 Integrated Sandbox:** A built-in "Try It Now" feature with native support for **Freighter (Stellar)** and **MetaMask (EVM)** wallets.
* **doc-as-code Sync:** A GitHub Action that automatically updates your hosted documentation whenever your contract code changes.
* **📘 Multi-Language Snippets:** Automatically generates code examples in JavaScript, Rust, and Python for every contract function.

### 4. Roadmap for this Wave
* **Phase 1:** Core Parser for Soroban `.wasm` spec files and EVM JSON ABIs.
* **Phase 2:** Launch the "Live Sandbox" UI components with wallet injection.
* **Phase 3:** Release the SpecDoc CLI for automated deployment to IPFS or Vercel.

### 5. Why SpecDoc belongs in Drips Wave
SpecDoc is an **Ecosystem Multiplier**. When documentation is easy to read and test, more developers build on the network.
* **Public Good:** SpecDoc will always be free for open-source projects.
* **Sustainability:** 15% of all funding received via Drips is streamed to the creators of the frontend frameworks and blockchain SDKs (like `soroban-client`) that make our sandbox possible.

---

## 🛠 Project Structure (Monorepo)

```text
SpecDoc/
├── apps/
│   ├── web/           # The documentation hosting platform
│   └── cli/           # Tool for local documentation generation
├── libs/
│   ├── parsers/       # Logic to translate ABIs and Specs into JSON
│   └── sandbox/       # Wallet-connection and contract-call components
├── packages/
│   └── themes/        # Customizable UI themes for the portals
└── LICENSE            # MIT Licensed
