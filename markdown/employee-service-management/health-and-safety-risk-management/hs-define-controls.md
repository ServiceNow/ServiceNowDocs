---
title: Define Health and Safety control measures
description: Define effective control measures to eliminate or minimize the risks associated with each workplace hazard to help prevent workplace accidents and injuries. Maintain a list of all the controls in place in your organization for every type of job and the associated risks.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Define Health and Safety control measures

Define effective control measures to eliminate or minimize the risks associated with each workplace hazard to help prevent workplace accidents and injuries. Maintain a list of all the controls in place in your organization for every type of job and the associated risks.

## Before you begin

Role required: sn\_hs\_rm.risk\_manager or sn\_hs\_rm.risk\_data\_manager

## About this task

-   Review and update your list of control measures regularly to ensure its continued effectiveness.
-   Risk assessment manager can also create a control measure during the hazard assessment for a risk assessment. If a control is not available in the **Available Control Measures** field, they can select **Create new control** to define and use a new control.

    For more information, see [Assess safety hazards and risk levels for a risk analysis](add-a-risk-and-its-controls-for-a-safety-risk-assessment.md).


## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../image/icon-config.png)\).

3.  In the **Configuration** tab, select **control measures** and then **All**.

4.  Create a control or modify an existing one.

    -   To create a control, select **New**.
    -   To review an existing control, open the one that you want to configure.
5.  On the form, fill in the fields.

<table id="table_establishment"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Control measure category

</td><td>

Category under which this control measure is organized. The list in this field displays items from the Hierarchy of controls \[sn\_hs\_rm\_hierarchy\_of\_controls\] table.For more information on control measure categories, see [Create a safety control measure category](hs-create-safety-hierarchy-controls.md).

</td></tr><tr><td>

Job location

</td><td>

Job or task location where this control measure should be applied for a risk.

</td></tr><tr><td>

Active

</td><td>

Option to mark this control measure available for use. A control measure must be active to be used.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  Add all control measures that are possible for a risk.


## Result

-   The control measure is listed in the **Control measures** list under **Configuration** and is saved in the Control measure \[sn\_hs\_rm\_control\_measure\] table.
-   The control measure is available to select in the following fields:
    -   **Hazard** field on the Hazard and controls form when defining a job in the job register.
    -   **Add control measures** window on a JSA form.
    -   **Available Control Measures** field on the Hazard assessment form when conducting a risk assessment.

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)

