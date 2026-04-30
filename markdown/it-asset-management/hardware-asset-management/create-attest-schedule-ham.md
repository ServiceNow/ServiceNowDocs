---
title: Create an asset attestation schedule
description: Create an attestation schedule so that recurring asset attestations are created based on the frequency that you specify.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Audit your hardware assets by using Asset Attestation, Use, Hardware Asset Management, IT Asset Management]
---

# Create an asset attestation schedule

Create an attestation schedule so that recurring asset attestations are created based on the frequency that you specify.

## Before you begin

Role required: asset or inventory\_admin

## About this task

The **ITAM Common- Asset attestation** daily job runs daily to check through all the attestation schedules that are created. Based on the frequency specified in the attestation schedule, the job creates an asset attestation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Asset attestations** tab.

3.  Select **New**.

4.  In the dialog box, under the **Attestation mode**, select **Recurrence**.

5.  Select **Create**.

6.  On the form, fill in the fields.

<table id="table_uxy_n33_qdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Attestation schedule details

</td></tr><tr><td>

Schedule number

</td><td>

Unique identifier for the attestation schedule.

</td></tr><tr><td>

Schedule name

</td><td>

Name of the asset attestation schedule.

</td></tr><tr><td>

Frequency \(days\)

</td><td>

Frequency in days when the asset attestation schedule must create an asset attestation.

</td></tr><tr><td>

State

</td><td>

Status of the asset attestation schedule.

</td></tr><tr><td>

Schedule start date

</td><td>

Date on which the attestation schedule should be processed for the first time to create an asset attestation.**Note:** The Schedule start date must be at least the current date and can't be in the past.

</td></tr><tr><td>

Schedule end date

</td><td>

Date on which the attestation schedule should be processed for the last time to create an asset attestation.**Note:** The Schedule end date should be after the schedule start date.

</td></tr><tr><td>

Requested by

</td><td>

User who is creating the attestation schedule.

</td></tr><tr><td>

Next scheduled run

</td><td>

Date on which the attestation schedule is planned to be run the next time.This field is updated automatically only after the asset attestation schedule is processed successfully to create an asset attestation. Also, this field is populated based on the value in the **Frequency \(days\)** field. For example, if the Schedule start date is set to `2024-01-01` and the Frequency is set to `10`, then the following events happen:

1.  An asset attestation is first created on 2024-01-01.
2.  The Next scheduled run field is set to 2024-01-11 automatically.


</td></tr><tr><td>

Model categories

</td><td>

Model categories of the assets for which the attestation schedule is created.**Note:** You can select more than one model categories. However, you can only select the model categories that belong to the resources categories that are opted-in and that don't need a license.

</td></tr><tr><td class="sub-head" colspan="2">

User Criteria

</td></tr><tr><td>

Filter

</td><td>

Set conditions to select employees who are required to confirm assets through the asset attestation request. For example, if you want to select employees who belong to Development department, you can set the **Department** field to **Development** and then select **Set**.

</td></tr><tr><td class="sub-head" colspan="2">

Work notes

</td></tr><tr><td>

Work notes

</td><td>

Comments related to the asset attestation schedule.

</td></tr></tbody>
</table>    **Note:** The following fields on the form are automatically populated:

    -   **Schedule number**
    -   **State**
    -   **Requested by**
    -   **Next schedule run**
7.  Select **Save**.


## Result

-   An asset attestation schedule is created in the Ready state.
-   The Attestations tab displays the list of attestation request details after the requests are created.
-   An email notification with the link to the **My Assets** page on the Employee Center portal is sent to the employees who are required to confirm assets on the scheduled attestation date.

## What to do next

[View open asset attestations in the Hardware Asset Workspace](view-open-asset-attest-ham.md).

**Parent Topic:**[Audit your hardware assets by using Asset Attestation](../concept/audit-hardware-assets-attestation.md)

