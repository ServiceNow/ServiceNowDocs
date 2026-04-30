---
title: Configure budget attribute at instance-level to allocate budget
description: Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your planning items using Strategic Planning.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable financial budget allocation for planning items in Strategic Planning, Configure financials for planning items in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configure budget attribute at instance-level to allocate budget

Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your planning items using Strategic Planning.

## Before you begin

-   Enable the budget allocation property to work on budgeting for planning items. For more information, see [Enable financial budget allocation for planning items in Strategic Planning](enable-fin-budget-spw.md).
-   Role required: admin

**Important:** Existing customers can’t change the budget attribute to cost\_type.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Properties**.

2.  Filter the Name column to locate and open **sn\_invst\_pln.budget\_allocation\_attribute** property.

3.  Update the Value field to one of the following.

    -   **cost\_type** - view financials by cost types such as Hardware Opex, External labor Capex, Software Capex, Software Opex.

        **Note:** It's suggested to limit the number of cost types to four.

    -   **expense\_type** - view financials by expense types such as Capex and Opex.
4.  Select **Update**.


