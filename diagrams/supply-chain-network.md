# Supply Chain Network Diagram

```mermaid
flowchart LR
    RM1[Raw Material Supplier A] -->|Millets / Grains| PLANT[Manufacturing Plant]
    RM2[Raw Material Supplier B] -->|Alternate Supply| PLANT
    PKG[Packaging Supplier] -->|Packaging Material| PLANT

    PLANT -->|Finished Goods| HYD[Hyderabad DC]
    PLANT -->|Finished Goods| VIJ[Vijayawada DC]
    PLANT -->|Finished Goods| BLR[Bengaluru DC]

    HYD --> TG[Telangana Customer Zone]
    VIJ --> AP[Andhra Pradesh Customer Zone]
    BLR --> KA[Karnataka Customer Zone]

    RM2 -. Contingency sourcing .-> PLANT
    HYD -. Inter-DC support .-> VIJ
    VIJ -. Inter-DC support .-> HYD
    BLR -. Emergency rebalancing .-> HYD
```

## Design Notes

- Two raw-material sources reduce dependency on a single supplier.
- Packaging supply is modeled separately because packaging shortages can stop finished-goods production even when raw materials are available.
- The plant is the central production node.
- Three regional DCs position inventory closer to demand.
- Inter-DC support is shown as a contingency concept for inventory rebalancing.
- Transportation lanes should be maintained only where the movement is operationally valid and economically justified.
