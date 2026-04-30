---
title: Configure budget attribute at instance-level to allocate budget
description: Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your planning items using Portfolio Planning.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Configure budget attribute at instance-level to allocate budget

Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your planning items using Portfolio Planning.

## Before you begin

-   Enable the budget allocation property to work on budgeting for planning items. For more information, see [Enable financial budget allocation for planning items in Portfolio Planning](enable-fin-budget-ppw.md).
-   Role required: admin

**Important:** Existing customers cannot change the budget attribute to cost\_type.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Properties**.

2.  Filter the Name column to locate and open **sn\_invst\_pln.budget\_allocation\_attribute** property.

3.  Update the Value field to one of the following.

    -   **cost\_type** - view financials by cost types such as Hardware Opex, External labor Capex, Software Capex, Software Opex, and so on.
    -   **expense\_type** - view financials by expense types such as Capex and Opex.
4.  Select **Update**.


