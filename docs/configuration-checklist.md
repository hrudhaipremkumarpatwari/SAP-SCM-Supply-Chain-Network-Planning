# SAP SCM / APO Network Planning Configuration Checklist

This checklist summarizes the logical setup used in the Week 1 project. Exact screens, transactions, and field names can vary by SAP SCM/APO release and system configuration.

## A. Planning Scope

- [ ] Define products and regions in scope
- [ ] Confirm supplier, plant, DC, and customer locations
- [ ] Define planning horizon and time buckets
- [ ] Define service-level, inventory, capacity, and cost objectives
- [ ] Record all scenario assumptions

## B. Location Master

- [ ] Create/validate supplier locations
- [ ] Create/validate manufacturing plant location
- [ ] Create/validate regional DC locations
- [ ] Create/validate customer or market-zone locations
- [ ] Confirm calendars and time zones where relevant

## C. Product and Location-Product Master

- [ ] Create raw-material products
- [ ] Create packaging products
- [ ] Create finished-goods products
- [ ] Extend products to valid locations
- [ ] Maintain planning-relevant parameters
- [ ] Review lot-size, safety stock, and procurement/production settings

## D. Resources and Capacity

- [ ] Create production resources
- [ ] Maintain available capacity
- [ ] Define resource calendars
- [ ] Confirm capacity consumption assumptions
- [ ] Test reduced-capacity scenario

## E. Sources of Supply

- [ ] Maintain procurement relationships for suppliers
- [ ] Maintain production source for finished goods
- [ ] Validate source-location and destination-location combinations
- [ ] Maintain alternate sourcing where required
- [ ] Define quota arrangements or sourcing priorities where applicable

## F. Transportation Lanes

- [ ] Supplier → plant lanes
- [ ] Plant → Hyderabad DC lane
- [ ] Plant → Vijayawada DC lane
- [ ] Plant → Bengaluru DC lane
- [ ] DC → customer-zone lanes
- [ ] Maintain transit time assumptions
- [ ] Maintain transportation cost assumptions
- [ ] Maintain lane capacity where relevant
- [ ] Validate fallback transportation options

## G. Planning Model / Version

- [ ] Assign relevant master data to the supply chain model
- [ ] Create/validate planning version
- [ ] Confirm version is active for the planning exercise
- [ ] Confirm no obsolete locations or products are included

## H. Planning Area / Planning Book

- [ ] Define required planning key figures
- [ ] Prepare demand, receipts, stock, capacity, and shortage views
- [ ] Validate time-bucket profile
- [ ] Validate selection profiles / planning views

## I. Demand Inputs

- [ ] Load or simulate regional demand
- [ ] Validate demand totals by product and region
- [ ] Check for duplicate or missing demand
- [ ] Create demand-spike test case

## J. SNP Heuristic Review

- [ ] Run initial planning cycle
- [ ] Review shortages
- [ ] Review excess inventory
- [ ] Review resource overloads
- [ ] Review sourcing decisions
- [ ] Review transportation feasibility

## K. Constrained / Cost-Based Review

- [ ] Identify capacity-constrained products
- [ ] Review alternative source options
- [ ] Review transport-versus-inventory trade-offs
- [ ] Review penalty/cost assumptions used in the conceptual optimizer model
- [ ] Confirm that service priorities are respected

## L. Deployment

- [ ] Define downstream allocation logic
- [ ] Test allocation under insufficient supply
- [ ] Review priority treatment of regional demand
- [ ] Verify that one DC is not overstocked while another is short

## M. Transportation Load Planning

- [ ] Review shipment consolidation opportunities
- [ ] Review minimum / maximum load assumptions
- [ ] Review transport capacity
- [ ] Check expedited-shipment scenarios

## N. KPI Validation

- [ ] Customer service / fill rate
- [ ] Inventory coverage
- [ ] Stockout frequency
- [ ] Excess inventory
- [ ] Capacity utilization
- [ ] Supplier dependency
- [ ] Transit / replenishment lead time
- [ ] Transport utilization
- [ ] Master-data accuracy

## O. Risk Tests

- [ ] Supplier disruption
- [ ] Plant downtime
- [ ] Demand spike
- [ ] Packaging shortage
- [ ] Transportation delay
- [ ] Capacity reduction
- [ ] Missing master data
- [ ] Integration / data-load issue

## P. Final Review

- [ ] Assumptions documented
- [ ] Network diagram updated
- [ ] Planning flow updated
- [ ] Risks linked to mitigations
- [ ] KPIs reviewed
- [ ] Conclusion reflects results and limitations
