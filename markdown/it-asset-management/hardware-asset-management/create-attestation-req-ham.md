---
title: Create an asset attestation in the Inventory view
description: Create an asset attestation to validate whether the serialized hardware asset that's assigned to an employee is still in use.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Audit your hardware assets by using Asset Attestation, Use, Hardware Asset Management, IT Asset Management]
---

# Create an asset attestation in the Inventory view

Create an asset attestation to validate whether the serialized hardware asset that's assigned to an employee is still in use.

## Before you begin

Role required: asset or inventory\_admin

## About this task

A single asset attestation can have attestations involving more than one employee. Also, an employee can have more than one asset assigned. Therefore, an asset attestation can have multiple users and assets involved.

Only serialized hardware assets that belong to the opted-in resource categories can be requested for attestation. Consumables, bundles, and pallets can't be attested.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Asset attestations** tab.

3.  Select **New**.

4.  In the dialog box, under the **Attestation mode**, select **One time**.

5.  Select **Create**.

6.  On the form, fill in the fields.

<table id="table_uxy_n33_qdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Asset details

</td></tr><tr><td>

Attestation number

</td><td>

Unique identifier for asset attestation.

</td></tr><tr><td>

Requested by

</td><td>

User who is creating the asset attestation.

</td></tr><tr><td>

Submission date

</td><td>

Date on which the asset attestation is submitted.

</td></tr><tr><td>

Schedule

</td><td>

Attestation schedule that created the attestation.**Note:** This field is empty for a one-time asset attestation request.

</td></tr><tr><td>

State

</td><td>

Status of the asset attestation.

</td></tr><tr><td>

Model categories

</td><td>

Model categories of the assets for which the attestation is requested.**Note:** You can select more than one model categories. However, you can only select the model categories that belong to the resources categories that are opted-in and that don't need a license.

</td></tr><tr><td class="sub-head" colspan="2">

User Criteria

</td></tr><tr><td>

Filter

</td><td>

Set conditions to select employees who are required to confirm assets. For example, if you want to select employees who belong to the Development department, you can set the **Department** field to **Development** and then select **Set**.

</td></tr><tr><td class="sub-head" colspan="2">

Work notes

</td></tr><tr><td>

Work notes

</td><td>

Comments related to asset attestation.

</td></tr></tbody>
</table>    **Note:** The following fields on the form are automatically populated:

    -   **Attestation number**
    -   **Requested by**
    -   **Submission date**
    -   **Schedule**
    -   **State**
7.  Select **Save**.


## Result

-   An email notification with the link to the **My Assets** page on the Employee Center portal is sent to the employees who are required to confirm assets.
-   An asset attestation is created in the In progress state.
-   The Assets tab shows the list of assets to be confirmed by the employees.
-   The Users tab shows the list of employees who are required to confirm the assets assigned to them.
-   The Excluded Assets tab shows the assets that are opted-out and not part of the asset attestation.

## What to do next

[View open asset attestations in the Hardware Asset Workspace](view-open-asset-attest-ham.md).

**Parent Topic:**[Audit your hardware assets by using Asset Attestation](../concept/audit-hardware-assets-attestation.md)

