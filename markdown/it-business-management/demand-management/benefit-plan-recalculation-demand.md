---
title: Benefit plan updates and recalculation in demand currency
description: Updating the entered currency, entered benefit, offset type, or the fiscal period of a benefit plan also updates all related amount fields in the benefit plan and its breakdowns. Also, the amounts in the related fields of the demand, to which the benefit plan is rolling up, are recalculated and reflected in demand currency.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Enable demand currency view, Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Benefit plan updates and recalculation in demand currency

Updating the entered currency, entered benefit, offset type, or the fiscal period of a benefit plan also updates all related amount fields in the benefit plan and its breakdowns. Also, the amounts in the related fields of the demand, to which the benefit plan is rolling up, are recalculated and reflected in demand currency.

-   **Changes in Entered currency, Entered benefit, and Recurring check box of a benefit plan**

    When you change the values of any of these fields in the Benefit Plan form with multicurrency view enabled, the following values are recalculated:

    -   When you modify the **Entered currency** field, **Entered benefit** field, or **Recurring** check box of the Benefit Plan form, the total planned benefit is recalculated in demand currency.
    -   The **Benefit in demand currency** in the Benefit Plan Breakdown is recalculated.
    -   The value in the **Financial benefit in demand currency** field of the demand is recalculated.
-   **Changes in the offset type of a benefit plan**

    When you change the offset type for the benefit plan, either the start date or end date and specify the offset period and duration of such periods in the Benefit Plan form, the following values are recalculated:

    -   The **Total planned benefit** and the **Benefit in demand currency** of the benefit plan are recalculated. Therefore, the Benefit Plan Breakdown records may be added or removed.
    -   If the **Recurring** check box is not selected, then the **Benefit in demand currency** of each Benefit Plan Breakdown record is recalculated.
    -   The value in the **Financial benefit in demand currency** field of the demand is recalculated.
-   **Changes in the fiscal period of a benefit plan**

    When you change the fiscal period, either the start date or end date in the Benefit Plan form, the following values are recalculated:

    -   The **Benefit in demand currency** and the **Total planned benefit** of the benefit plan are recalculated. Therefore, the Benefit Plan Breakdown records may be added or removed.
    -   If the **Recurring** check box is not selected, then the **Benefit in demand currency** of each Benefit Plan Breakdown record is recalculated.
    -   The value in the **Financial benefit in demand currency** field of the demand is recalculated.
-   **Changes in the entered benefit of a benefit plan breakdown**

    When you change the entered benefit in an individual Benefit Plan Breakdown record, the following values are recalculated:

    -   The **Benefit in demand currency** of the benefit plan is recalculated in demand currency.
    -   The value in the **Financial benefit in demand currency** field of the demand is recalculated.

**Parent Topic:**[Enable demand currency view](../task/enable-multicurrency-demand.md)

