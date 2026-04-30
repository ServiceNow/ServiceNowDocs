---
title: Submit a recall order for your enterprise assets
description: Submit a recall order to initiate the replacement, repair, or retirement of enterprise assets that have been recalled by the asset vendor. You can also choose to provide your users with additional instructions on how to operate your recalled enterprise assets.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Managing recalled enterprise assets, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Submit a recall order for your enterprise assets

Submit a recall order to initiate the replacement, repair, or retirement of enterprise assets that have been recalled by the asset vendor. You can also choose to provide your users with additional instructions on how to operate your recalled enterprise assets.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

**Note:** You can include multiple enterprise assets in a single recall order. However, all enterprise assets must be associated with the same model.

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  On the **Recall orders** tab, select **New**.

3.  On the Create New Enterprise Recall Order form, fill in the fields.

<table id="table_afc_hqq_wtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recall source

</td><td>

Source of the enterprise asset recall.

</td></tr><tr><td>

Remediation

</td><td>

Action that you are going to take on the recalled enterprise assets, based on the remediation option that is recommended by the asset vendor in the corresponding recall notification. Select one of the following options:-   **Repair**: Option to repair the recalled enterprise assets.
-   **Replace**: Option to replace the recalled enterprise assets with new assets.
-   **Retire**: Option to retire the recalled enterprise assets.
-   **Notation**: Option to provide users with additional instructions on how to operate the recalled enterprise assets.

If you select this option, the **Recall remediation instruction** field appears below the **Serial numbers** field. In the **Recall remediation instruction** field, enter the additional instructions.

</td></tr><tr><td>

Models

</td><td>

Models that the recalled enterprise assets are associated with.You can select one or more models from the list.

</td></tr><tr><td>

Serial numbers

</td><td>

Serial numbers that identify each recalled enterprise asset. This field is optional.To include multiple enterprise assets in this recall order, enter all associated serial numbers using one of the following options:

-   Serial number range, such as `SN001-SN010`
-   Comma-separated list of individual serial numbers, such as `SN020, SN038, SN054`
-   Comma-separated list of both serial number ranges and individual serial numbers, such as `SN001-SN010, SN202, SN038, SN100-SN110`
 If you do not enter any serial numbers, all enterprise assets that are associated with the model specified in the **Model** field are included in this recall order.

 **Note:** If you specify any serial numbers on a recall order, you cannot specify any vehicle identification numbers \(VINs\) on the same order.

</td></tr><tr><td>

Location

</td><td>

Location in which the recalled enterprise assets reside.

</td></tr><tr><td>

Recall notice number

</td><td>

Identification number of the recall notification that was sent by the asset vendor.

</td></tr><tr><td>

Remediate by

</td><td>

Date by which the action that you selected in the **Remediation** field must be completed.

</td></tr><tr><td>

VINs

</td><td>

Vehicle identification numbers \(VINs\) that identify each recalled enterprise asset. This field is optional and applicable only to automotive enterprise assets, such as cars and mopeds.To include multiple automotive enterprise assets in this recall order, enter all associated VINs using one of the following options:

-   VIN range, such as `3VWSB81H8WM210368-3VWSB81H8WM210370`
-   Comma-separated list of individual VINs, such as `1B7HF13ZX1J572139, JH4KA8150MC012098`
-   Comma-separated list of both VIN ranges and individual VINs, such as `4JGAB54E81A277648-4JGAB54E81A277650, 1GNDX03E03D188446, KM8SC73E94U774838`
 If you do not enter any VINs, all enterprise assets that are associated with the model specified in the **Model** field are included in this recall order.

 **Note:** If you specify any VINs on a recall order, you cannot specify any serial numbers on the same order.

</td></tr><tr><td>

Include child locations

</td><td>

Option to include the child locations of the location that you specified in the **Location** field.

</td></tr><tr><td>

Additional info

</td><td>

Additional information about the recall order.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

-   The **Acknowledge Recall** button appears.
-   The **Recalled Assets** and **Recalled Tasks** tabs are shown.

## What to do next

[Acknowledge enterprise assets in the recall order](acknowledge-recalled-assets-eam.md).

**Parent Topic:**[Managing recalled enterprise assets](../concept/managing-recalled-enterprise-assets.md)

