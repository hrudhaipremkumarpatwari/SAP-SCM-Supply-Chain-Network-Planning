# Supply Chain Risk Register

This risk register supports the fictional SAP SCM network-planning scenario used in the Week 1 internship project.

| Risk | Likelihood | Impact | Early Warning Indicator | Contingency / Mitigation |
|---|---|---:|---|---|
| Primary raw-material supplier disruption | Medium | High | missed confirmations, lead-time increase, partial supply | maintain alternate supplier, quota split, safety stock, emergency sourcing approval |
| Packaging-material shortage | Medium | High | reduced packaging inventory, supplier delay | qualify alternate packaging supplier, hold strategic buffer, prioritize high-demand SKUs |
| Plant downtime | Low–Medium | High | equipment alarms, maintenance backlog, capacity drop | preventive maintenance, recovery schedule, prioritize critical products, temporary capacity reallocation |
| Demand spike | Medium | High | forecast error, sales promotion, sudden regional orders | scenario planning, reserve capacity, safety stock, deployment prioritization |
| Transportation delay | Medium | Medium–High | route disruption, carrier delay, weather issue | alternate carrier/lane, rerouting, increased lead-time buffer, expedited mode for critical stock |
| DC stock imbalance | Medium | Medium | one DC excess while another has shortage | deployment review, inter-DC transfer logic, replenishment-frequency adjustment |
| Capacity bottleneck | Medium | High | high utilization, late orders, queue build-up | reschedule production, alternate resource, overtime/extra shift assumption, demand prioritization |
| Incorrect master data | Medium | High | infeasible plan, unusual receipts, missing lane or source | master-data validation checklist, ownership controls, pre-run data audit |
| Wrong transportation lead time | Medium | Medium | repeated late arrivals versus plan | review transit-time master data, adjust lane assumptions, carrier performance tracking |
| Single-source dependency | Medium | High | supplier share approaches 100% | dual sourcing, quota arrangements, periodic supplier-risk review |
| Excess inventory | Medium | Medium | rising days of supply, slow movement | lower replenishment quantity, rebalance stock, revise safety-stock policy |
| Integration or data-load failure | Low–Medium | High | missing demand, stale stock, incomplete master data | interface monitoring, reconciliation reports, controlled manual fallback for planning run |
| Poor forecast accuracy | Medium | Medium–High | repeated bias and large forecast error | forecast review cycle, segmentation, demand-planner collaboration, scenario buffers |
| Regulatory or quality hold | Low | High | failed quality test or compliance issue | batch isolation, alternate approved source, reserve inventory, quality escalation process |

## Contingency Principles

1. **Avoid single points of failure** for critical materials wherever commercially feasible.
2. **Separate normal planning from emergency planning** so expensive actions such as expedited freight are used only when justified.
3. **Validate master data before planning runs**, because incorrect locations, products, sources, calendars, or lanes can produce a technically valid but operationally unusable plan.
4. **Use scenario analysis** to test the network against supply, capacity, demand, and logistics shocks.
5. **Prioritize service consciously** when supply is constrained rather than allowing shortages to be distributed unintentionally.
6. **Track recovery KPIs** after a disruption, including backlog, service level, inventory position, and capacity utilization.

## Example Scenario: Primary Supplier Failure

If the primary millet supplier cannot deliver for one planning period:

1. identify affected raw material and finished-good demand;
2. activate the approved alternate supplier within sourcing policy;
3. consume available safety stock according to priority rules;
4. recalculate the constrained supply plan;
5. review plant capacity and revised material-arrival dates;
6. deploy finished goods to the highest-priority markets;
7. use expedited transportation only where the service impact justifies the cost;
8. restore normal sourcing once supply reliability returns.

## Example Scenario: Demand Surge

For an unexpected 25% demand increase in one region:

1. compare new demand against DC stock and confirmed receipts;
2. check available plant and transport capacity;
3. protect high-priority orders;
4. rebalance finished goods across DCs where feasible;
5. increase production only if material and capacity constraints permit;
6. communicate residual shortage risk to stakeholders;
7. revise short-term replenishment and safety-stock assumptions if the surge persists.

## Risk Governance

The Supply Chain Planner owns the planning response, while Procurement, Production, Logistics, Sales, Warehouse Operations, and IT/SAP Support provide the inputs needed for recovery. Major cost/service trade-offs should be escalated to management rather than hidden inside planning parameters.
