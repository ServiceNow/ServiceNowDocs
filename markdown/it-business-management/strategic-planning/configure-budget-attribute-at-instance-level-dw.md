---
title: Configure budget attribute at instance level
description: Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your demands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/configure-budget-attribute-at-instance-level-dw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Enable financial budget allocation for demands, Configure financials for demands, Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure budget attribute at instance level

Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your demands.

## Before you begin

-   Enable the budget allocation property to work on budgeting for demands. For more information, see [Enable financial budget allocation for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/enable-financial-budget-allocation-for-demands.md).
-   Role required: admin

**Important:** Existing customers can’t change the budget attribute to cost\_type.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Properties**.

2.  Filter the Name column to locate and open the **sn\_invst\_pln.budget\_allocation\_attribute** property.

3.  Update the Value field to one of the following.

    -   **cost\_type** - view financials by cost types such as Hardware Opex, External labor Capex, Software Capex, Software Opex.
    -   **expense\_type** - view financials by expense types such as Capex and Opex.
4.  Select **Update**.


