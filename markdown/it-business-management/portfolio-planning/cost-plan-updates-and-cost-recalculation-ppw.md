---
title: Cost plan updates and cost recalculation in demand currency
description: Updating the unit cost, quantity, or fiscal period of a cost plan updates all related amount fields in the cost plan and its breakdowns. The amounts in the related demand fields are recalculated and reflected in the demand currency.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Multicurrency reference, Reference, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Cost plan updates and cost recalculation in demand currency

Updating the unit cost, quantity, or fiscal period of a cost plan updates all related amount fields in the cost plan and its breakdowns. The amounts in the related demand fields are recalculated and reflected in the demand currency.

## Unit cost, Quantity, and Recurring field changes

When you modify these fields in the Cost Plan form with multicurrency view enabled, the following values are recalculated:

-   **Total planned cost** in demand currency.
-   **Cost in demand currency** in the Cost Plan Breakdown.
-   **Capital expense in demand currency**, **Operating expense in demand currency**, and **Total planned cost in demand currency** fields in the demand.

## Fiscal period changes

When you change the fiscal period \(start date or end date\) in the Cost Plan form, the following values are recalculated:

-   **Total planned cost** and **Cost in demand currency** of the cost plan. Cost Plan Breakdown records can be added or removed.
-   If the **Recurring** check box isn’t selected, the **Cost in demand currency** value of each Cost Plan Breakdown record is recalculated.
-   **Capital expense in demand currency**, **Operating expense in demand currency**, and **Total planned cost in demand currency** fields in the demand.

## Cost plan breakdown changes

When you change the entered cost in an individual Cost Plan Breakdown record or manually add cost plan breakdowns to a cost plan, the following values are recalculated:

-   **Total planned cost** of the cost plan in demand currency.
-   **Capital expense in demand currency**, **Operating expense in demand currency**, and **Total planned cost in demand currency** fields in the demand.

