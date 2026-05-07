---
title: Create an asset attestation or a schedule using the playbook
description: Create a one-time asset attestation or a schedule for recurring attestations to verify if your serialized hardware assets are in use, using the playbook.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Playbook for asset attestation, Audit your hardware assets by using Asset Attestation, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create an asset attestation or a schedule using the playbook

Create a one-time asset attestation or a schedule for recurring attestations to verify if your serialized hardware assets are in use, using the playbook.

## Before you begin

Role required: asset or inventory\_admin

## About this task

A single asset attestation can have attestations involving more than one employee. Also, an employee can have more than one asset assigned. Therefore, an asset attestation can have multiple users and assets involved.

Only serialized hardware assets that belong to the opted-in resource categories can be requested for attestation. Consumables, bundles, and pallets can't be attested.

The **ITAM Common- Asset attestation** daily job runs daily to check through all the attestation schedules that are created. Based on the frequency specified in the attestation schedule, the job creates an asset attestation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Asset attestations** tab.

3.  Select **New**.

    The Create asset attestation playbook displays the following activities that you must complete in the sequence:

    -   **Provide attestation details**
    -   **Select users**
    -   **Select model categories**
    -   **Attestation completed**
4.  Select whether you want to create an asset attestation or an attestation schedule, and then fill in the necessary details in the **Provide attestation details** activity.

    The **Schedule number** field is automatically populated with a unique identifier for the attestation schedule.

    -   To create an asset attestation, select **One-time** in the Mode field and follow these steps:
        1.  In the **Schedule name** field, enter the name of the attestation.
        2.  Select **Mark Complete**.
    -   To create a schedule for recurring asset attestations, select **Recurring** in the Mode field and follow these steps:
        1.  On the form, fill in the fields.

<table id="table_a35_12p_rfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule name

</td><td>

Name of the asset attestation schedule.

</td></tr><tr><td>

Frequency \(days\)

</td><td>

Frequency in days when the asset attestation schedule must create an asset attestation.

</td></tr><tr><td>

Schedule start date

</td><td>

Date on which the attestation schedule should be processed for the first time to create an asset attestation.**Note:** The Schedule start date must be at least the current date and can't be in the past.

</td></tr><tr><td>

Schedule end date

</td><td>

Date on which the attestation schedule should be processed for the last time to create an asset attestation.**Note:** The Schedule end date should be after the schedule start date.

</td></tr></tbody>
</table>        2.  Select **Mark Complete**.
5.  In the **Select users** activity, select employees required to confirm assets.

    1.  In the Editor section, set a condition to select employees who are required to confirm assets through the asset attestation request.

        For example, to select employees in the Development department, set the **Department** field to **Development**.

        The **User list** section displays the number of records that match your condition. You can also view these results.

    2.  Select **Mark Complete**.

6.  In the **Select model category** activity, select the model categories of assets that you want to attest.

<table id="choicetable_k3g_slp_rfc"><thead><tr><th align="left" id="d329725e297">

Number of model categories to be attested

</th><th align="left" id="d329725e300">

Action

</th></tr></thead><tbody><tr><td id="d329725e306">

**All**

</td><td>

1.  In the **Model category type** field, select **All**.
2.  Select **Mark complete**.


</td></tr><tr><td id="d329725e333">

**A few model categories from the list**

</td><td>

1.  In the **Model category type** field, select **Individual**.
2.  In the **Model categories** field, select the required model categories.

**Note:** You can select one or more model categories.

3.  Select **Mark complete**.


</td></tr></tbody>
</table>7.  In the **Attestation completed** activity, review the details on the Attestation schedule overview form, and then select **Mark Complete**.


## Result

-   If you selected **One-time** in the Mode field, the following changes happen:
    -   An email notification is sent to the employees who are required to confirm assets. Employees can confirm assets through the Now Mobile app or on the Employee Center portal.
    -   An asset attestation is created in the In progress state and the following tabs are displayed:
        -   The Assets tab shows the list of assets to be confirmed by the employees.
        -   The Users tab shows the list of employees who are required to confirm the assets assigned to them.
        -   The Excluded Assets tab shows the assets that are opted-out and not part of the asset attestation.
        -   The Remediation task tab displays any remediation tasks created for assets that your employees have confirmed they don't have.
-   If you selected **Recurring** in the Mode field, and set the **Schedule start date** field to a date in future, the following changes happen:
    -   An asset attestation schedule is created in the Ready state.
    -   The Attestations tab displays the list of attestation request details after the requests are created.
    -   An email notification is sent to the employees who are required to confirm assets on the scheduled attestation date. Employees can confirm assets through the Now Mobile app or on the Employee Center portal.
-   If the **Schedule start date** field is set to the current date, the following changes happen:
    -   An attestation schedule is created in the Ready state.
    -   The attestation schedule creates an asset attestation in the In progress state.
    -   An email notification is sent to the employees who are required to confirm assets. Employees can confirm assets through the Now Mobile app or on the Employee Center portal.

## What to do next

View the asset attestation or the attestation schedule that's created.

-   To view the attestation record, follow any of these steps:
    -   Navigate to the **Inventory** view and select the **Asset attestations** tab
    -   Navigate to the **Asset operations** view and select **Attestations** from the Attestation list.
-   To view the attestation schedule record, navigate to **Asset operations** and select **Schedule** from the Attestation list.

**Parent Topic:**[Playbook for asset attestation](../concept/playbook-asset-attestation-ham.md)

