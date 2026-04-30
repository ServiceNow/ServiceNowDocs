---
title: Create life-cycle definitions for your firmware models
description: Manage the complete life cycle of firmware models by adding life-cycle information in the OT Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create life-cycle definitions for your firmware models

Manage the complete life cycle of firmware models by adding life-cycle information in the OT Asset Workspace.

## Before you begin

**Important:** The OT Asset Management application must be activated to access the OT Asset Workspace. For details, see [Install OT Asset Management](install-otam.md).

Role required: sn\_otam.ot\_asset\_manager

## About this task

**Note:** If the life-cycle phases of your firmware version are defined in the Enterprise Asset Management Content Service, then the life-cycle phase details are automatically populated for that firmware model record.

## Procedure

1.  Navigate to **Workspaces** &gt; **OT Asset Workspace** &gt; **OT model management**.

2.  Select the **Firmware** tab.

3.  Select the firmware model for which you want to add life-cycle details.

4.  Select the **Firmware model lifecycles** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

<table id="table_yyf_55y_tdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Name of the model. This field is read only.

</td></tr><tr><td>

Lifecycle type

</td><td>

Type of life cycle. The available values are:-   **Internal**

**Note:** For the Internal life-cycle type, the life-cycle information isn't shared with your ServiceNow instance during the reverse push.

-   **Publisher**


</td></tr><tr><td>

Lifecycle phase

</td><td>

Phase of the life cycle. The available values are:-   **General availability**
-   **End of sale**
-   **End of support**
-   **End of extended support**
-   **End of life**


</td></tr><tr><td>

Source

</td><td>

Source of the firmware model.

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the life cycle.

</td></tr><tr><td>

Description

</td><td>

Description of the firmware model.

</td></tr><tr><td>

Phase start date

</td><td>

Start date of the life-cycle phase. This field is required.

</td></tr><tr><td>

Phase end date

</td><td>

End date of the life-cycle phase.

</td></tr><tr><td>

Current lifecycle phase

</td><td>

Option that indicates if it’s the current life cycle of the firmware model.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the firmware model life cycle is active.

</td></tr></tbody>
</table>7.  Select **Save**.


## Result

The life-cyle phase is listed in the **Firmware model lifecycles** tab.

