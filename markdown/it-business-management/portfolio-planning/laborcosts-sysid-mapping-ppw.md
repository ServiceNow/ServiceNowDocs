---
title: Create custom labor costs and map them to sys\_id
description: Create and map custom labor costs to sys\_id to generate labor costs based on the relevant expenses.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Create custom labor costs and map them to sys\_id

Create and map custom labor costs to sys\_id to generate labor costs based on the relevant expenses.

## Before you begin

Role required: admin

## Procedure

1.  Create custom labor costs.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
    2.  Filter the Label field to locate the open **Cost Type Definition**.
    3.  From the Related Links, select **Show List**.

        List of OOB labor costs is displayed.

    4.  Select **New**.
    5.  On the Cost Type Definition form, fill the fields.

        -   **Name** - enter the name of the labor cost plan.

            **Tip:** Adding the cost type, either capex or opex, as a suffix to the name helps you to easily identify while creating cost plans.

        -   **Expense type** - select Capex or Opex from the list to define expense.
        For example, you can create Software Capex labor cost to capture software purchasing expenses. Hardware Opex labor cost to capture your hardware purchasing expenses.

    6.  Click **Submit**.

        The new cost plan is displayed on the list.

    7.  Right-click on the cost plan row and select **Copy sys\_id**.
2.  Map the custom labor costs with sys\_id.

    1.  Navigate to **All** &gt; **System Properties** &gt; **All properties**.
    2.  Filter the name field to locate and open the **sn\_plng\_att\_core.labor\_costtype\_sysid\_mapping** property.
    3.  In the Value field, enter the labor cost type name and it's sys\_id in the same format as the OOB labor costs mapping format.
    4.  Select **Update**.

