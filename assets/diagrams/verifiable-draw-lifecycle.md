# ZodiacChain — Verifiable Draw Lifecycle Diagram

```mermaid
flowchart LR
    A[Scheduled] --> B[Open]
    B --> C[Closed]
    C --> D[Awaiting Randomness]
    D --> E[Chainlink VRF Fulfillment]
    E --> F[Resolved]
    F --> G[Archived]

    E --> H[Terrestrial Result 00-99]
    E --> I[Celestial Number 01-60]

    H --> J[Terrestrial Animal Mapping]
    I --> K[Celestial Animal Mapping]
    I --> L[Celestial Element Mapping]

    J --> M[Fairness Dashboard]
    K --> M
    L --> M
    G --> M
