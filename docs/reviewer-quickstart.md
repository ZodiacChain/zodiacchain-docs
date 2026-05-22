# ZodiacChain — Reviewer Quickstart

**Audience:** Chainlink reviewers, ecosystem partners, and first-time technical readers  
**Scope:** Testnet-first MVP review guide  
**Status:** Public documentation

This quickstart summarizes the ZodiacChain MVP without replacing the whitepaper, grant memo, roadmap, or technical architecture overview.

## 1. What is ZodiacChain?

ZodiacChain is a testnet-first verifiable draw infrastructure project designed to make digital draw execution transparent, auditable, and deterministic.

The MVP focuses on a verifiable draw lifecycle: a draw is opened, testnet/demo entries are accepted, the entry window is closed, randomness is requested, results are derived deterministically, and the full evidence path is exposed for review.

The intended testnet target is Polygon Amoy. ZodiacChain is designed around a Chainlink VRF-ready randomness flow and a Chainlink Automation-ready lifecycle, so the system can move from mock evidence to public testnet evidence without changing the core verification narrative.

The public Fairness Dashboard is central to the experience. It is intended to show lifecycle state, request references, deterministic result derivation, derived animal and element outputs, event history, and explorer links when testnet evidence is available.

ZodiacChain should be evaluated as testnet-first draw infrastructure for technical review, with no live consumer operating scope implied.

## 2. Why Chainlink VRF?

Chainlink VRF matters because ZodiacChain needs verifiable randomness.

Randomness should not be hidden inside an operator-controlled process. Reviewers should be able to see when randomness was requested, which request is linked to a draw, when fulfillment occurred, and how the fulfilled randomness was converted into public results.

The intended flow is:

```text
draw closed -> randomness requested -> requestId stored -> randomness fulfilled -> deterministic results derived
```

For ZodiacChain, VRF is a mission-critical primitive, not an optional enhancement. The future on-chain verification path depends on linking a draw to a VRF request and fulfillment, then deriving the Terrestrial and Celestial outputs from the fulfilled random words through fixed, auditable logic.

## 3. Why Chainlink Automation?

Chainlink Automation matters because the draw lifecycle should not rely indefinitely on manual scripts or operator timing.

Automation-compatible execution can support:

- triggering the randomness request after entries are locked;
- resolving the draw after randomness fulfillment;
- moving the draw through predictable lifecycle transitions;
- reducing reliance on manual execution paths;
- preparing the contracts for `checkUpkeep` / `performUpkeep` style testnet execution.

In the current MVP plan, opening and closing draws remain operator-controlled while the first Automation-compatible paths focus on post-close execution: requesting randomness when a draw is `Closed`, and resolving the draw after randomness has been fulfilled. The broader architecture remains compatible with automated closing later, but the reviewer-facing MVP keeps that distinction explicit.

## 4. What does the MVP demonstrate?

The current MVP demonstrates the reviewable flow of a verifiable draw from active state to public verification.

It is intended to show:

- active draw visualization;
- testnet/demo entry flow;
- draw lifecycle visibility;
- deterministic Terrestrial Result in the `00-99` range;
- deterministic Celestial Number in the `01-60` range;
- derived animal and element outputs;
- event-driven transparency;
- Fairness Dashboard review flow;
- mock VRF and `requestId` walkthrough;
- public verification narrative from locked entries to final result.

The core idea is simple: reviewers should be able to follow what happened, when it happened, which randomness reference resolved the draw, and how the final outputs were derived.

## 5. How to run locally

This repository, `zodiacchain-docs`, is the public documentation hub. The runnable MVP lives in the implementation repository:

- [ZodiacChain MVP Repository](https://github.com/ZodiacChain/zodiacchain-mvp)

Current local validation path for the MVP repository:

```bash
git clone https://github.com/ZodiacChain/zodiacchain-mvp.git
cd zodiacchain-mvp
npm install
npm run check
```

PowerShell users can use `npm.cmd` if script execution policy blocks the `npm` shim:

```bash
npm.cmd install
npm.cmd run check
```

To run the current MVP demo locally, start the mock API and frontend from the `zodiacchain-mvp` repository root:

```bash
npm run dev -w @zodiacchain/backend
npm run dev -w @zodiacchain/frontend
```

PowerShell-safe equivalents:

```bash
npm.cmd run dev -w @zodiacchain/backend
npm.cmd run dev -w @zodiacchain/frontend
```

The backend mock API listens on `127.0.0.1:4000` by default. The frontend is a Vite app hosted on `127.0.0.1`; use the local URL printed by the frontend command.

The MVP repository is organized around `frontend`, `backend`, and `contracts` npm workspaces. Its current public README documents Node.js `22.14.0` or newer and npm `10.9.2` or newer as prerequisites.

## 6. Where is the Fairness Dashboard?

The Fairness Dashboard belongs to the MVP frontend experience in the `zodiacchain-mvp` implementation repository.

For reviewers reading this documentation repository, the dashboard is described in:

- [Technical Architecture Overview](../architecture/overview.md), especially the Fairness Dashboard and public verification sections;
- [MVP Demo Script](../grant/mvp-demo-script.md), especially the dashboard walkthrough and evidence checklist.

In the MVP, the dashboard should make the evidence path visible in one place: lifecycle state, timestamps, VRF request reference, fulfillment reference, deterministic result formulas, derived outputs, event history, and future Polygon Amoy explorer links.

## 7. What is mock today?

The current review flow may use mock or placeholder evidence while the testnet MVP is being implemented.

Mock today means:

- active reviewer draw ID `AMOY-DEMO-042`;
- demo entry ID `entry-demo-042-reviewer-a17`;
- mock VRF request reference `req-demo-2026-05-16-042`;
- displayed mock random words such as terrestrial word `0x04` and celestial word `0x10`;
- mock API or read-layer responses before full contract integration;
- dashboard event timelines that explain expected events before live Amoy transactions exist;
- placeholder transaction hashes and explorer links until testnet evidence is available.

Mock evidence is used to demonstrate the verification path, not to claim production operation.

## 8. What becomes on-chain later?

The later testnet implementation is expected to move the core evidence path on-chain on Polygon Amoy.

Planned on-chain or testnet-backed elements include:

- draw lifecycle state and transition rules;
- entry locking before randomness is requested;
- Chainlink VRF request creation;
- `requestId` storage linked to the draw;
- randomness fulfillment handling;
- deterministic Terrestrial and Celestial result derivation;
- public events such as `DrawOpened`, `DrawClosed`, `RandomnessRequested`, `RandomnessFulfilled`, and `DrawResolved`;
- Chainlink Automation-compatible lifecycle execution using `checkUpkeep` / `performUpkeep` style logic;
- explorer links and event references consumed by the Fairness Dashboard.

The immediate goal is reviewer-ready testnet infrastructure: transparent lifecycle execution, verifiable randomness, deterministic results, and public auditability.
