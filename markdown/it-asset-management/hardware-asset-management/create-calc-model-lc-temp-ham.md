---
title: Create Calculated lifecycle templates in the Hardware Asset Workspace
description: Create Calculated lifecycle templates to manage the complete lifecycle of hardware models efficiently.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage the lifecycle of hardware models with calculated lifecycle templates, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create Calculated lifecycle templates in the Hardware Asset Workspace

Create Calculated lifecycle templates to manage the complete lifecycle of hardware models efficiently.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset Operations**.

2.  From the **Hardware asset normalization** list, select **Calculated lifecycle templates**.

    The list of existing Calculated lifecycle templates is displayed.

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
    -   **End of life**
    -   **End of Sale**
    -   **End of Support**
    -   **End of General Availability**
6.  Define the calculated lifecycle formula for a lifecycle phase.

    1.  Select the calculated lifecycle formula.

    2.  In the **Phase start** and **Phase end** fields, enter the number of months for calculating the start date and end date of the lifecycle phase.

    3.  Select **Save**.

    The calculated lifecycle formula is updated with the values that you entered in the Phase start and Phase end fields.


## What to do next

[Associate a hardware model with a Calculated lifecycle template](associate-hardware-model-cal-temp.md).

**Parent Topic:**[Manage the lifecycle of hardware models with calculated lifecycle templates](../concept/manage-ham-lifecycle-temp.md)

