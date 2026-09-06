# Supply Chain Network Plan

## 1. Scenario Overview

**Company:** Deccan Harvest Foods Pvt. Ltd.  
**Industry:** Packaged millet-based ready-to-cook foods  
**Markets:** Telangana, Andhra Pradesh, Karnataka

The project models an end-to-end supply chain in which agricultural raw materials and packaging materials are sourced from multiple suppliers, converted into finished goods at a manufacturing plant, transferred to regional distribution centers, and then supplied to customer markets.

## 2. Planning Objectives

The network is designed to:

- improve product availability in regional markets;
- reduce dependence on a single supplier;
- balance inventory across distribution centers;
- improve visibility of plant and transport constraints;
- support structured replenishment and deployment decisions;
- reduce avoidable emergency transport and stockouts;
- establish measurable planning KPIs.

## 3. Stakeholders

| Stakeholder | Primary responsibility |
|---|---|
| Supply Chain Planner | Demand-supply balancing and network planning |
| Procurement Team | Supplier selection, sourcing priorities and continuity |
| Production Planner | Plant capacity and production feasibility |
| Warehouse / DC Team | Inventory and replenishment execution |
| Logistics Team | Transportation lanes, transit times and load utilization |
| Sales / Demand Planning | Regional demand inputs and service expectations |
| IT / SAP Support | Master-data quality, planning setup and issue resolution |
| Management | Cost, service-level and risk decisions |

## 4. Key Assumptions

- Demand is planned by region and product family.
- The manufacturing plant has finite production capacity.
- Supplier lead times differ by material.
- Regional DCs hold safety inventory.
- Transportation lanes have defined transit times and indicative costs.
- Multiple sourcing options are retained for critical raw materials where practical.
- The scenario is conceptual and does not claim execution in a live SAP production tenant.

## 5. Network Structure

The proposed network contains:

1. primary and alternate raw-material suppliers;
2. a packaging supplier;
3. one manufacturing plant;
4. Hyderabad, Vijayawada, and Bengaluru regional DCs;
5. downstream customer market zones.

The plant acts as the central finished-goods source. Inventory is positioned closer to demand through the three DCs. Alternate sourcing and contingency transport options reduce the effect of local disruptions.

## 6. SAP SCM / APO Master Data Blueprint

The planning model uses the following logical objects:

- **Locations:** suppliers, plant, DCs, and customer/market locations;
- **Products:** raw materials, packaging materials, and finished goods;
- **Location-products:** product-specific planning settings at each relevant location;
- **Resources:** production capacity and other constrained resources;
- **Sources of supply:** production and procurement relationships;
- **Transportation lanes:** valid product flows between locations;
- **Quota arrangements:** sourcing splits or priorities where dual sourcing is used;
- **Planning model/version:** active planning objects and scenario version;
- **Planning area/book:** demand-supply views and planning key figures.

## 7. Planning Logic

An initial planning cycle can be represented as:

1. load or simulate regional demand;
2. validate location-product and sourcing master data;
3. execute heuristic supply planning;
4. inspect shortages, excess inventory, capacity overload, and infeasible lanes;
5. adjust supply, capacity, sourcing, or inventory policies;
6. evaluate cost/capacity alternatives using optimizer principles;
7. perform deployment to allocate available supply to downstream locations;
8. evaluate transport load consolidation;
9. review service, inventory, utilization, and risk KPIs.

## 8. Resource Allocation Principles

Resource allocation follows these priorities:

- protect production of high-demand finished goods;
- identify overload before it becomes an execution problem;
- reserve sufficient capacity for base demand while keeping contingency flexibility;
- shift production timing or sourcing when capacity is constrained;
- avoid creating inventory in one region while another region is short.

## 9. Inventory Strategy

The network uses a practical inventory approach:

- safety stock at regional DCs for demand and lead-time uncertainty;
- lower buffers for stable products;
- higher protection for high-volume or volatile products;
- periodic review of excess and slow-moving inventory;
- coordinated deployment when supply is insufficient for all DC requirements.

## 10. Transportation Design

Transportation lanes are established only between valid source and destination locations. Each important lane should include planning assumptions such as transit time, transportation mode, cost, and available capacity where relevant.

Typical flows are:

- supplier → plant;
- plant → Hyderabad DC;
- plant → Vijayawada DC;
- plant → Bengaluru DC;
- DC → regional customer zones.

## 11. Expected Outcomes

The network design is intended to produce:

- improved visibility of supply-demand imbalance;
- earlier identification of capacity bottlenecks;
- clearer sourcing alternatives;
- better regional inventory balance;
- fewer stockouts and emergency shipments;
- improved transport utilization;
- stronger contingency preparedness.

## 12. Validation Approach

The design should be tested with scenarios such as:

- normal demand;
- 20–30% demand spike;
- primary supplier disruption;
- reduced plant capacity;
- delayed transport lane;
- DC inventory shortage;
- incorrect or missing master-data parameter.

The resulting plan should be reviewed for feasibility, service impact, inventory behavior, and recovery options.

## 13. Conclusion

This network blueprint demonstrates how SAP SCM/APO Supply Network Planning concepts can be applied to a realistic planning scenario. The main lesson is that planning quality depends not only on the algorithm selected, but also on accurate master data, clear sourcing rules, realistic capacities, transportation assumptions, and disciplined KPI review.
