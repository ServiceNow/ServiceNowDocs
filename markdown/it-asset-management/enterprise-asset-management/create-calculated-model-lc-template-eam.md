---
title: Create Calculated model lifecycle templates in the Enterprise Asset Workspace
description: Create Calculated model lifecycle templates to manage the complete lifecycle of the models efficiently.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage enterprise model life cycles, Create and manage enterprise models, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create Calculated model lifecycle templates in the Enterprise Asset Workspace

Create Calculated model lifecycle templates to manage the complete lifecycle of the models efficiently.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Asset Operations**.

2.  From the **Calculated model lifecycle** list, select **Calculated model lifecycle templates**.

    The list of existing Calculated model lifecycle templates is displayed.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Calculated lifecycle template.|
    |Description|Brief information about the template.|
    |Active|Option to indicate that the Calculated lifecycle template is available for use.|

5.  Select **Save**.

    The **Calculated Lifecycle formulas** tab is displayed with the list of calculated lifecycle formulas for the following lifecycle phases:

    -   **End of Extended Support**
    -   **End of Life**
    -   **End of Sale**
    -   **End of Support**
    -   **End of General Availability**
6.  Define the calculated lifecycle formula for a lifecycle phase.

    1.  Select the calculated lifecycle formula.

    2.  In the **Phase start** and **Phase end** fields, enter the number of months for calculating the start date and end date of the lifecycle phase.

    3.  Select **Save**.

    The calculated lifecycle formula is updated with the values that you entered in the **Phase start** and **Phase end** fields.


## What to do next

Associate the Calculated model lifecycle template with an enterprise model. For details, see [Associate an enterprise model with a Calculated model lifecycle template](associate-eam-model-calc-template.md).

**Parent Topic:**[Manage the lifecycle of enterprise models with calculated lifecycle templates](../concept/manage-eam-lifecycle-temp.md)

**Related topics**  


[Associate an enterprise model with a Calculated model lifecycle template](associate-eam-model-calc-template.md)

