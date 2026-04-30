---
title: Create custom labor costs and map them to sys\_id
description: Create and map custom labor costs to sys\_id to generate labor costs based on the relevant expenses.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create custom labor costs and map them to sys\_id

Create and map custom labor costs to sys\_id to generate labor costs based on the relevant expenses.

## Before you begin

Role required: admin

## About this task

Consider you removed the out-of-box cost types and created the following two labor cost types:

-   Internal Workforce Capital Expenditure \(to replace Labor Capex\)
-   Contractor Operational Expense \(to replace External Labor Opex\)

Once these new cost types are created, the system automatically assigns them unique sys\_ids. These sys\_ids are not same as the deleted defaults.

To ensure the system continues to recognize these new cost types for workflows, reporting, or calculations, you must manually updated in the sn\_plng\_att\_core.labor\_costtype\_sysid\_mapping system property with the new sys\_ids.

Omitting this update may result in system errors or incomplete data processing in cost-related operations.

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

## Mappings of default out of box labor costs with their sys\_id

```
{
  "labor_capex": "3d16eaf79330120064f572edb67ffb04",
  "labor_opex": "5b26eaf79330120064f572edb67ffb39",
  "external_labor_capex": "ed36eaf79330120064f572edb67ffb41",
  "external_labor_opex": "7b36eaf79330120064f572edb67ffb58"
}
```

