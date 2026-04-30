---
title: Cost plan updates and cost recalculation in demand currency
description: Updating the unit cost, quantity, or fiscal period of a cost plan updates all the related amount fields in the cost plan and its breakdowns. Also, the amounts in the related fields of the demand, to which the cost plan is rolling up, are recalculated and reflected in the demand currency.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Enable demand currency view, Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost plan updates and cost recalculation in demand currency

Updating the unit cost, quantity, or fiscal period of a cost plan updates all the related amount fields in the cost plan and its breakdowns. Also, the amounts in the related fields of the demand, to which the cost plan is rolling up, are recalculated and reflected in the demand currency.

-   **Changes in Unit cost, Quantity, and Recurring check box of a cost plan**

    When you change the values of any of these fields in the Cost Plan form with multicurrency view enabled, the following values are recalculated:

    -   When you modify the **Unit cost** field, **Quantity** field, or **Recurring** check box of the Cost Plan form, the total planned cost is recalculated in demand currency.
    -   The **Cost in demand currency** in the Cost Plan Breakdown is also recalculated.
    -   The values in the **Capital expense in demand currency**, **Operating expense in demand currency**, and the **Total planned cost in demand currency** fields of the demand are recalculated.
-   **Changes in the fiscal period of a cost plan**

    When you change the fiscal period, either the start date or end date in the Cost Plan form, the following values are recalculated:

    -   The **Total planned cost** and the **Cost in demand currency** of the cost plan are recalculated. Therefore, the Cost Plan Breakdown records may be added or removed.
    -   If the **Recurring** check box is not selected, then the **Cost in demand currency** of each Cost Plan Breakdown record is recalculated.
    -   The values in the **Capital expense in demand currency**, **Operating expense in demand currency**, and the **Total planned cost in demand currency** fields of the demand are recalculated.
-   **Changes in the entered cost of a cost plan breakdown or manual addition of a breakdown**

    When you change the entered cost in an individual Cost Plan Breakdown record or manually add cost plan breakdowns to a cost plan, the following values are recalculated:

    -   The **Total planned cost** of the cost plan is recalculated in demand currency.
    -   The values in the **Capital expense in demand currency**, **Operating expense in demand currency**, and the **Total planned cost in demand currency** fields of the demand are recalculated.

**Parent Topic:**[Enable demand currency view](../task/enable-multicurrency-demand.md)

