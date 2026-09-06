# SAP SCM Planning Flow

```mermaid
flowchart TD
    A[Demand / Forecast Input] --> B[Master Data Validation]
    B --> C[Locations, Products, Resources, Sources and Lanes]
    C --> D[Supply Chain Model and Planning Version]
    D --> E[SNP Heuristic Planning]
    E --> F{Shortage, Excess or Capacity Issue?}
    F -- Yes --> G[Review Sourcing, Capacity, Inventory and Transportation]
    G --> H[Adjust Planning Parameters / Assumptions]
    H --> E
    F -- No --> I[Constrained / Cost Trade-off Review]
    I --> J[Deployment to Regional DCs]
    J --> K[Transport Load Planning / Consolidation]
    K --> L[KPI and Risk Review]
    L --> M[Approved Network Plan]
```

## Flow Explanation

1. Demand is captured or simulated by product and region.
2. Planning master data is validated before the supply run.
3. Network objects are included in the relevant supply chain model and planning version.
4. An initial heuristic produces a supply plan.
5. Exceptions such as shortages, overloads, or excess inventory are reviewed.
6. Planning assumptions are adjusted where required.
7. Constrained and cost-based alternatives are evaluated conceptually.
8. Deployment logic determines how supply is allocated downstream.
9. Transportation-load planning reviews shipment consolidation and capacity.
10. KPIs and risk scenarios are reviewed before the plan is accepted.
