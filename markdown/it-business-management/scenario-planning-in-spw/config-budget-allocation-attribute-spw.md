---
title: Configure budget attribute at instance-level
description: Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your planning items using Strategic Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/scenario-planning-in-spw/config-budget-allocation-attribute-spw.html
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable financial budget allocation for planning items in Strategic Planning, Configure financials for planning items in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure budget attribute at instance-level

Configure the budget attribute by expense type or cost type as an instance-level to work on budget allocations for your planning items using Strategic Planning.

## Before you begin

-   Enable the budget allocation property to work on budgeting for planning items. For more information, see [Enable financial budget allocation for planning items in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/scenario-planning-in-spw/enable-fin-budget-spw.md).
-   Role required: admin

**Important:** Existing customers can’t change the budget attribute to cost\_type.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Properties**.

2.  Filter the Name column to locate and open **sn\_invst\_pln.budget\_allocation\_attribute** property.

3.  Update the Value field to one of the following.

    -   **cost\_type** - view financials by cost types such as Hardware Opex, External labor Capex, Software Capex, Software Opex.

        **Note:** Its suggested to have number of cost types to around 4 when you're choosing cost type as the budget attribute. Having higher number of cost types would have performance challenges when loading the financials data in the portfolio financials or scenario planning financials pages.

    -   **expense\_type** - view financials by expense types such as Capex and Opex.
4.  Select **Update**.


