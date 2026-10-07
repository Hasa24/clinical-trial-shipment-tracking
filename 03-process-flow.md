# Process Flow: Order to Delivery (with Exception Handling)

```mermaid
flowchart TD
    A[Site requests drug supply] --> B[Supply planner reviews and releases order]
    B --> C[Depot manager packs shipment<br/>with temperature-controlled packaging]
    C --> D[Depot marks shipment as Dispatched]
    D --> E[Courier transports shipment]
    E --> F{Exception during transit?}
    F -- No --> G[Shipment arrives at site]
    F -- Yes --> H[System raises alert<br/>delay / temperature excursion / customs hold]
    H --> I[Supply planner logs exception with owner]
    I --> J{Temperature excursion?}
    J -- Yes --> K[QA reviews temperature log<br/>and decides: use or quarantine]
    J -- No --> L[Planner resolves delay<br/>and updates ETA]
    K --> M[Resolution recorded in audit trail]
    L --> M
    M --> G
    G --> N[Site coordinator confirms delivery<br/>and condition]
    N --> O[Status set to Delivered<br/>record closed]
```

## Swimlane summary

| Step | Owner |
|---|---|
| Request supply | Site coordinator |
| Review and release order | Supply planner |
| Pack and dispatch | Depot manager |
| Transport | Courier / logistics partner |
| Log and resolve exceptions | Supply planner |
| Decide use or quarantine | QA reviewer |
| Confirm delivery | Site coordinator |
