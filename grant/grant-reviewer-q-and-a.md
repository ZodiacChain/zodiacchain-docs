# Grant Reviewer Q&A

**Status:** Public Documentation  
**Last updated:** 15 May 2026  
**Owner:** ZodiacChain  
**Audience:** Grant reviewers, ecosystem partners, and technical evaluators  

---

## 1. Purpose

This document provides clear, reusable answers to likely reviewer questions during Chainlink Build or grant evaluation.

The answers are intentionally concise and public-safe. They describe ZodiacChain's current testnet-first MVP scope and should not be read as a commitment to launch regulated commercial operations, mainnet deployment, token issuance, or investment activity in the current phase.

---

## 2. Why does ZodiacChain need Chainlink VRF?

ZodiacChain needs Chainlink VRF because verifiable randomness is the core trust primitive behind the draw resolution process.

The MVP is designed to avoid a black-box randomness model. A draw should be closed, randomness should be requested, the randomness request should be linked to the correct draw, and the final results should be derived from the fulfilled random output through deterministic rules.

Chainlink VRF supports that model by providing randomness with a verification path suitable for smart contract-based systems. For ZodiacChain, VRF is not an optional enhancement; it is central to proving that draw outcomes were not manually selected or changed after entries were locked.

---

## 3. Why is Chainlink Automation relevant?

Chainlink Automation is relevant because ZodiacChain's draw lifecycle should not depend on a trusted operator manually triggering every state transition.

The MVP roadmap includes scheduled draw flows, lifecycle closing, randomness requests, and eventual result resolution. Automation-compatible logic can help detect when a draw should close and trigger the next step in a consistent, auditable way.

For the testnet MVP, Automation helps demonstrate a more impartial execution model and reduces reliance on manual scripts as the primary operating path.

---

## 4. Why Polygon Amoy Testnet?

Polygon Amoy Testnet is the intended MVP target because ZodiacChain is designed around Polygon ecosystem infrastructure while remaining testnet-first during the current phase.

Using Amoy allows the team to validate smart contract behavior, Chainlink integration planning, transaction references, explorer links, and the Fairness Dashboard flow without implying production launch or regulated commercial activity.

The goal is to prove technical feasibility and public verifiability in a low-risk environment before any future production decision.

---

## 5. What does testnet-first mean?

Testnet-first means ZodiacChain will validate the protocol design, draw lifecycle, randomness flow, deterministic result derivation, protection rules, and Fairness Dashboard before any commercial or production phase.

In practical terms, the current scope is focused on:

- public documentation;
- frontend demo experience;
- mock API and domain logic validation;
- smart contract scaffold;
- Chainlink VRF and Automation testnet integration planning;
- public verification through the Fairness Dashboard.

This approach keeps the project grounded in technical demonstration and reviewability rather than premature market launch.

---

## 6. What is excluded from the current phase?

The current phase excludes regulated commercial operation, real-money wagering, mainnet deployment, token presale, token issuance, investment offering, KYC/AML implementation, and production treasury management.

ZDC-related ecosystem activity is not part of the current funding round. Any future commercial phase would require legal review, jurisdiction planning, security review, and compliance controls before being considered.

The current goal is to build a credible testnet MVP and public verification layer.

---

## 7. How is fairness verified?

Fairness is verified by making the draw lifecycle and result derivation inspectable.

The intended verification path is:

1. the draw is opened and later closed;
2. entries are locked before randomness is requested;
3. a VRF request ID is linked to the draw;
4. randomness fulfillment is recorded;
5. Terrestrial and Celestial results are derived deterministically;
6. lifecycle events, timestamps, request references, and result derivation are exposed through the Fairness Dashboard.

The dashboard is designed to help reviewers and users answer whether the draw was locked before randomness, which request resolved it, and how the final result was computed.

---

## 8. What does the current team already cover?

The current team covers product leadership, backend engineering, software analysis, QA, and business development.

Current public team responsibilities include:

- founder, product, and backend leadership;
- backend engineering and software analysis;
- QA leadership and validation discipline;
- business development and partnerships coordination.

This team composition supports the documentation foundation, MVP planning, backend/domain logic direction, QA readiness, and ecosystem-facing communication.

---

## 9. What roles remain open?

The main open roles are focused on accelerating technical delivery and reviewer-ready execution.

Priority gaps include:

- smart contract engineering for Solidity implementation and Chainlink integration;
- frontend/product UI engineering for the demo interface and Fairness Dashboard;
- indexing/backend infrastructure for event history and verification data;
- DevRel or grant operations support for reviewer communication and public updates;
- legal and compliance review for future commercial planning;
- external security review before any production-level deployment.

These roles are especially important as the project moves from documentation into testnet MVP implementation.

---

## 10. What does funding unlock?

Funding unlocks the transition from public documentation and planning into a working testnet MVP.

Specifically, it supports:

- smart contract scaffold and lifecycle implementation;
- Chainlink VRF request and fulfillment flow on testnet;
- Chainlink Automation-compatible lifecycle execution;
- deterministic result derivation and protection rule validation;
- Fairness Dashboard implementation;
- QA, demo readiness, and public technical documentation;
- stronger reviewer follow-up and ecosystem collaboration.

The purpose of funding is not to launch a regulated commercial product. It is to prove the verifiable draw foundation in a public, reviewable, testnet-first environment.

---

## 11. Reviewer Positioning Summary

ZodiacChain is asking reviewers to evaluate the project as verifiable draw infrastructure for a testnet MVP.

The core thesis is simple:

> A draw can be transparent, deterministic, auditable, and publicly verifiable from lifecycle start to final result.

Chainlink VRF and Chainlink Automation are central to demonstrating that thesis.
