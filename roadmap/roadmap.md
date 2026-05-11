# ZodiacChain — Public Roadmap

**Version:** 1.0  
**Status:** Public Documentation  
**Project:** ZodiacChain  
**Phase:** Testnet MVP / Public Demonstration  

---

## 1. Overview

ZodiacChain is being developed as a testnet-first verifiable draw infrastructure.

This roadmap shows how the project will move from public documentation and grant readiness toward a working MVP with a verifiable draw lifecycle, deterministic result derivation, Chainlink VRF integration, Chainlink Automation planning, and a public Fairness Dashboard.

This roadmap is intentionally conservative. It does not describe a real-money launch, token presale, or production betting operation.

---

## 2. Roadmap Principles

| Principle | Description |
|---|---|
| Testnet-first | Validate the system safely before any production phase |
| Verifiability-first | Make randomness, derivation, and results publicly inspectable |
| Milestone-based execution | Build the MVP through clear, reviewable phases |
| Compliance-aware | Avoid real-money operation before legal and regulatory review |
| Public documentation | Keep core technical and strategic documents accessible |

---

## 3. Phase 0 — Public Project Foundation

**Status:** In Progress  
**Goal:** Establish a clean and professional public documentation base.

### Key Deliverables

- Public documentation repository
- Final whitepaper
- Chainlink grant memo
- Public roadmap
- Technical architecture overview
- Logo, banner, and basic diagrams
- Root README with clear navigation

### Success Criteria

- Repository is clean and easy to navigate
- Core documents are publicly accessible
- Project positioning is clear
- Grant reviewers can understand the project quickly

---

## 4. Phase 1 — Documentation & Grant Readiness

**Status:** In Progress  
**Goal:** Prepare ZodiacChain for grant evaluation and technical review.

### Key Deliverables

- Whitepaper
- Chainlink-facing grant memo
- MVP Scope
- Draw Lifecycle Spec
- Bet Types & Payout Rules Spec
- Protection Rules Spec
- Event Schema Spec
- Entity / Data Model Spec
- API Contract Spec
- Frontend Screen Behavior Spec
- MVP Implementation Backlog

### Success Criteria

- MVP scope is clearly defined
- Chainlink VRF relevance is clearly explained
- Fairness Dashboard concept is documented
- Testnet-first strategy is clear
- No real-money launch is implied

---

## 5. Phase 2 — MVP Frontend Demo

**Status:** Planned  
**Goal:** Build a visual demo interface that explains the verifiable draw lifecycle.

### Key Deliverables

- Active Draw screen
- Draw Lifecycle visualization
- Place Test Bet screen
- Result screen
- Wallet Activity view
- Historical Draws view
- Testnet disclaimer
- Mock data integration

### Success Criteria

- Users can understand the draw lifecycle visually
- Frontend can run with mock data
- Demo is usable by non-technical reviewers
- No production polish is required at this stage

---

## 6. Phase 3 — Domain Logic & Mock API

**Status:** Planned  
**Goal:** Implement the core ZodiacChain rules before full smart contract integration.

### Key Deliverables

- TypeScript domain logic engine
- Terrestrial result derivation
- Celestial Number derivation
- Bet type validation
- Win/loss evaluation
- Simulated payout calculation
- Protection rule validation
- Mock API endpoints

### Success Criteria

- Terrestrial Result derives values from `00–99`
- Celestial Number derives values from `01–60`
- Celestial outcomes are deterministic
- Payout logic is reproducible
- Frontend can consume stable API responses

---

## 7. Phase 4 — Smart Contract Scaffold

**Status:** Planned  
**Goal:** Create the initial on-chain foundation for the draw lifecycle.

### Key Deliverables

- Core draw smart contract scaffold
- Draw state model
- Draw creation logic
- Draw opening and closing logic
- Deterministic derivation helper functions
- Lifecycle events
- Basic unit tests

### Success Criteria

- Contract compiles successfully
- Draw lifecycle state transitions are enforced
- Invalid transitions are rejected
- Events are emitted correctly
- Contract is ready for Chainlink VRF integration

---

## 8. Phase 5 — Chainlink VRF & Automation Integration

**Status:** Planned  
**Goal:** Integrate verifiable randomness and lifecycle automation into the MVP.

### Key Deliverables

- Chainlink VRF testnet configuration
- Randomness request flow
- `requestId -> drawId` mapping
- Fulfillment handling
- Terrestrial and Celestial result derivation from VRF output
- Chainlink Automation-compatible lifecycle closure
- VRF and Automation test cases

### Success Criteria

- Randomness request is linked to the correct draw
- Fulfillment resolves the correct draw
- Results are derived deterministically
- New entries are blocked after randomness request
- Automation-compatible logic avoids duplicate execution

---

## 9. Phase 6 — Fairness Dashboard & Public Demo

**Status:** Planned  
**Goal:** Make the verification path public, understandable, and grant-ready.

### Key Deliverables

- Fairness Dashboard
- Draw lifecycle timeline
- VRF request and fulfillment panel
- Result derivation walkthrough
- Event history
- Protection rules snapshot
- Explorer links
- Public demo script

### Success Criteria

- Users can follow the full draw process
- Verification steps are clear
- Result derivation is reproducible
- Dashboard demonstrates “No black box. Only verifiable draws.”
- Demo can be used in grant follow-up

---

## 10. Phase 7 — Beta Readiness & Future Review

**Status:** Future  
**Goal:** Prepare for broader testing, external review, and future product decisions.

### Key Deliverables

- QA validation report
- Security review planning
- External audit planning
- Legal and regulatory review
- Jurisdiction strategy refinement
- Partner/integrator feedback
- Beta roadmap

### Success Criteria

- MVP risks are documented
- Security review path is defined
- Legal review path is defined
- Future commercial assumptions are separated from MVP validation
- Next funding or partnership phase can be discussed responsibly

---

## 11. Current Non-Goals

The current roadmap does not include:

- real-money operation;
- mainnet launch;
- token presale;
- investment offering;
- production betting platform;
- regulated market launch;
- KYC/AML implementation;
- production treasury management.

Any future commercial phase would require legal review, jurisdictional planning, security review, and compliance controls.

---

## 12. Summary

ZodiacChain’s roadmap is focused on proving the foundation first:

> verifiable randomness, deterministic result derivation, transparent lifecycle, and public auditability.

The immediate objective is to complete the documentation foundation and then move into a testnet MVP that can be demonstrated to grant reviewers, ecosystem partners, and future contributors.
