# MVP Demo Script

**Status:** Public Documentation  
**Target duration:** 8 minutes  
**Owner:** ZodiacChain  
**Audience:** Grant reviewers, ecosystem partners, and community calls  
**Demo mode:** Mock / testnet-first evidence path  

---

## 1. Purpose

This document provides a repeatable script for demonstrating the ZodiacChain MVP end-to-end.

The goal is to show how a verifiable draw moves from active state to public verification, with clear evidence at each step. Current evidence may use mock IDs or future Polygon Amoy testnet placeholders until live testnet transactions are available.

This demo does not represent regulated commercial operation, real-money wagering, mainnet deployment, token issuance, or production activity.

---

## 2. Demo Narrative

**Start:** ZodiacChain is a testnet-first verifiable draw infrastructure.

**Middle:** The demo shows an active draw, a test entry, draw closing, randomness request, randomness fulfillment, deterministic result derivation, and the Fairness Dashboard.

**End:** The audience can follow the public verification path:

```text
entries locked -> randomness requested -> randomness fulfilled -> results derived -> dashboard verification
```

---

## 3. Pre-demo Checklist

Complete this checklist before the call:

- Open the MVP demo interface or mock screen set.
- Prepare the active draw view with draw ID `mock-draw-001`.
- Prepare one test entry example with entry ID `mock-entry-001`.
- Prepare randomness request reference `mock-request-001`.
- Prepare placeholder transaction hash format `0x...` for future testnet evidence.
- Prepare the Fairness Dashboard screen or mock view.
- Keep the architecture overview available for reference: [`architecture/overview.md`](../architecture/overview.md).
- Keep the grant reviewer Q&A available for follow-up: [`grant-reviewer-q-and-a.md`](./grant-reviewer-q-and-a.md).

---

## 4. Exact Demo Steps

| Step | Target time | Presenter action | Audience-visible screen / action | Expected evidence | Fallback if live evidence is not available |
|---:|---:|---|---|---|---|
| 1 | 0:00-0:45 | Open with the positioning statement: "ZodiacChain is a testnet-first verifiable draw infrastructure." | Project overview or active draw landing screen. | Testnet-only disclaimer visible; no real-money language. | Show this script and the architecture overview. |
| 2 | 0:45-1:30 | Show the active draw. Explain that entries are accepted only while the draw is open. | Active Draw screen with draw ID `mock-draw-001`, status `Open`, schedule, and entry window. | UI state: `Open`; expected event/log: `DrawOpened`; future tx hash: `0x...`. | Use mock active draw data and state that live Amoy evidence will replace the mock ID. |
| 3 | 1:30-2:20 | Place or simulate a test entry. Explain that this is testnet/demo behavior only. | Test entry form or wallet action showing selected bet and confirmation. | UI confirmation; entry ID `mock-entry-001`; expected event/log: `BetPlaced`; future tx hash: `0x...`. | Use a pre-recorded/mock entry confirmation and show the expected event name. |
| 4 | 2:20-3:00 | Close the draw and explain that entries are locked before randomness. | Draw lifecycle moves from `Open` to `Closed`. | UI state: `Closed`; expected event/log: `DrawClosed`; no new entries accepted; future tx hash: `0x...`. | Show lifecycle timeline with `Closed` highlighted and explain the lock condition. |
| 5 | 3:00-3:50 | Trigger or show the randomness request. Explain the link between the draw and the request. | Randomness panel shows request reference linked to `mock-draw-001`. | Request ID `mock-request-001`; expected event/log: `RandomnessRequested`; future tx hash: `0x...`; future explorer link placeholder. | Show mock request reference and explain that Chainlink VRF testnet evidence will be linked here. |
| 6 | 3:50-4:40 | Show randomness fulfillment. Explain that the random output is consumed after fulfillment. | Randomness panel changes from requested to fulfilled. | Expected event/log: `RandomnessFulfilled`; request ID `mock-request-001`; random word placeholder; future tx hash: `0x...`. | Use mock fulfillment data and point to the VRF flow in the architecture overview. |
| 7 | 4:40-5:40 | Show deterministic result derivation. Walk through Terrestrial and Celestial outputs. | Result derivation view with formulas and outputs. | Terrestrial Result range `00-99`; Celestial Number range `01-60`; expected event/log: `DrawResolved`; future tx hash: `0x...`. | Use fixed mock random words and derive results step by step on screen. |
| 8 | 5:40-6:50 | Open the Fairness Dashboard. Explain that it connects lifecycle, randomness, and derivation evidence. | Fairness Dashboard with timeline, request reference, result outputs, event history, and explorer placeholders. | UI sections: lifecycle timeline, VRF request/fulfillment, deterministic derivation, event log; expected events: `DrawOpened`, `BetPlaced`, `DrawClosed`, `RandomnessRequested`, `RandomnessFulfilled`, `DrawResolved`. | Show dashboard mock and mark unavailable live links as pending Amoy testnet evidence. |
| 9 | 6:50-7:35 | Show the public verification flow end-to-end. | Verification summary from locked entries to dashboard confirmation. | Sequence visible: `entries locked -> randomness requested -> randomness fulfilled -> results derived -> dashboard verification`. | Use the text sequence from this script and map each item to the dashboard mock. |
| 10 | 7:35-8:00 | Close with current scope and next steps. | Final summary screen or repository links. | Clear statement: testnet MVP only; no regulated commercial operation; references to docs, roadmap, Q&A, and follow-up tracker. | Share repository links and offer to send the public documentation pack. |

---

## 5. Demo Evidence Checklist

Use this checklist during or immediately after the demo:

| Evidence item | Expected value or format | Status |
|---|---|---|
| Active draw ID | `mock-draw-001` or live testnet draw ID | Pending / demo-specific |
| Test entry ID | `mock-entry-001` or live testnet entry ID | Pending / demo-specific |
| Randomness request ID | `mock-request-001` or live Chainlink VRF request ID | Pending / demo-specific |
| Draw opened evidence | `DrawOpened` UI/log/event | Pending / demo-specific |
| Entry placed evidence | `BetPlaced` UI/log/event | Pending / demo-specific |
| Draw closed evidence | `DrawClosed` UI/log/event | Pending / demo-specific |
| Randomness requested evidence | `RandomnessRequested` UI/log/event | Pending / demo-specific |
| Randomness fulfilled evidence | `RandomnessFulfilled` UI/log/event | Pending / demo-specific |
| Draw resolved evidence | `DrawResolved` UI/log/event | Pending / demo-specific |
| Archived draw evidence | `DrawArchived` UI/log/event when archival is shown | Optional |
| Future transaction hash | `0x...` | Pending Amoy testnet evidence |
| Future explorer link | Polygon Amoy explorer link | Pending Amoy testnet evidence |

---

## 6. Presenter Notes

- Keep the demo focused on verifiability, not product hype.
- Repeat that this is a testnet-first technical demonstration.
- Use "test entry" instead of language that implies live wagering.
- When showing randomness, emphasize the linkage between draw ID, request ID, fulfillment, and deterministic derivation.
- When showing the dashboard, explain what a reviewer can independently inspect.
- If a live testnet step fails, switch to mock evidence and preserve the verification narrative.

---

## 7. Mock-only Fallback Mode

If no live testnet deployment or transaction evidence is available, run the demo fully in mock mode:

1. Show `mock-draw-001` as the active draw.
2. Show `mock-entry-001` as the test entry.
3. Show the draw moving to `Closed`.
4. Show `mock-request-001` as the randomness request.
5. Show mocked fulfillment data.
6. Derive Terrestrial and Celestial results using the displayed formulas.
7. Open the Fairness Dashboard mock and map each displayed field to the evidence checklist.

This fallback still satisfies the demo goal because it shows the intended verification path and clarifies where live Chainlink VRF and Polygon Amoy evidence will be attached.

---

## 8. Post-demo Follow-up Links

Share these links after reviewer, partner, or community calls:

- [Chainlink Grant Memo](./ZodiacChain_ChainLink_Grant.pdf)
- [Grant Reviewer Q&A](./grant-reviewer-q-and-a.md)
- [Chainlink Submission Follow-up Tracker](./chainlink-submission-follow-up.md)
- [Technical Architecture Overview](../architecture/overview.md)
- [Public Roadmap](../roadmap/roadmap.md)
- [Public Documentation Repository](https://github.com/ZodiacChain/zodiacchain-docs)

---

## 9. Completion Criteria

The demo is complete when the audience has seen:

- the active draw;
- a test entry;
- the draw closing;
- randomness request evidence;
- randomness fulfillment evidence or mock placeholder;
- deterministic result derivation;
- the Fairness Dashboard;
- the public verification flow from entry lock to result verification.
