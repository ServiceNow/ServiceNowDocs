---
title: Audit enterprise asset inventory
description: Audit your enterprise asset inventory to learn where your assets are and what their current status is.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Audit enterprise asset inventory

Audit your enterprise asset inventory to learn where your assets are and what their current status is.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

You can use the [Mobile Agent application for Enterprise Asset Management](../concept/eam-mobile-agent-app.md) to scan asset tags or enter them manually. If an asset is scanned but its asset tag does not exist in our database, then by default, that asset is mapped to an unknown model record. The unknown model record appears on the **All enterprise models** tab of the **Model Management** view in the Enterprise Asset Workspace. The asset manager manually associates this asset to the appropriate model. You can't change, update or delete an unknown model.

**Note:** Starting with Enterprise Asset Management version 9.0, you can also audit the licensed hardware assets in the Enterprise Asset Workspace only if the Hardware Asset Management application is activated.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Inventory** &gt; **Asset audits**.

2.  Select **New**.

    The Create New Enterprise Asset Audit page opens.

3.  On the form, fill in the fields.

<table id="table_pd5_p51_rsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audit number

</td><td>

Audit reference number.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which you want to assign the audit.

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for the audit.

</td></tr><tr><td>

Type

</td><td>

Type of the audit. The available values are-   Location
-   Stockroom


</td></tr><tr><td>

Status

</td><td>

Current status of the audit.

</td></tr><tr><td>

Location**Note:** This field appears only if you set the **Type** field to **Location**.

</td><td>

Location in which you want to perform the audit.

</td></tr><tr><td>

Include child locations**Note:** This field appears only if you set the **Type** field to **Location**.

</td><td>

Option to include child locations in the audit.

</td></tr><tr><td>

Stockroom**Note:** This field appears only if you set the **Type** field to **Stockroom**.

</td><td>

Stockroom in which you want to perform the audit.

</td></tr><tr><td>

Model category

</td><td>

Model category that you want to audit.This field is available with Enterprise Asset Management version 9.0 and later.

</td></tr><tr><td>

Aisle and space**Note:** This field appears only if you set the **Type** field to **Stockroom**.

</td><td>

Aisle and space within the stockroom where you want to perform the audit.This field is available with Enterprise Asset Management version 9.0 and later.

</td></tr><tr><td>

Scheduled date

</td><td>

Date on which you want to perform the audit.

</td></tr><tr><td>

Scan date

</td><td>

Date on which you want to scan the assets.

</td></tr></tbody>
</table>    The asset audit records are stored in the Asset Audits \[sn\_itam\_common\_asset\_audit\] table.

4.  Select **Save**.

    The asset audit inventory record is created and appears with **Expected Assets** and **Scanned Assets** tabs. The Audit Results section is activated and shows the details of the audit result when the audit is complete.

    | | |
    |---|---|
    |Expected|Number of expected assets that were scanned.|
    |Not expected and location corrected|Number of assets that were scanned but were not expected.|
    |Missing|Number of expected assets that were not scanned.|
    |New|Number of assets that were scanned but do not have a record in your ServiceNow instance.|


**Parent Topic:**[Create and manage enterprise asset inventory](../concept/managing-enterprise-asset-inventory.md)

