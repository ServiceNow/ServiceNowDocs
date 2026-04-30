---
title: Complete the Asset selection task for a requested Device as a Service \(DaaS\) asset
description: Complete the Asset selection task for a requested DaaS asset by selecting an asset that matches the criteria specified in the associated inbound asset order line.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-20"
reading_time_minutes: 3
breadcrumb: [Completing an inbound asset order, Managing inbound asset orders for requested DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Asset selection task for a requested Device as a Service \(DaaS\) asset

Complete the Asset selection task for a requested DaaS asset by selecting an asset that matches the criteria specified in the associated inbound asset order line.

## Before you begin

Role required: sn\_eam\_provider.provider\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_wwt_xxs_1hc"><thead><tr><th align="left" id="d124004e78">

Navigation option

</th><th align="left" id="d124004e81">

Procedure

</th></tr></thead><tbody><tr><td id="d124004e87">

**Provider inbound asset order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order**.
2.  From the list of available inbound asset orders, select the order that you want to complete.
3.  On the inbound asset order record, select the **Inbound asset order lines** tab.
4.  From the list of available inbound asset order lines, select the order line that you want to choose an asset for.
5.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d124004e129">

**Provider inbound asset order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order line**.
2.  From the list of available inbound asset order lines, select the order line that you want to choose an asset for.
3.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d124004e162">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Asset selection task that you want to complete.

4.  On the **Details** tab of the Asset selection task, fill in the fields.

<table id="table_xyl_nls_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Due date

</td><td>

Date and time at which you must complete the task.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom that you are selecting the asset from.

</td></tr><tr><td>

Assignment group

</td><td>

Group that the task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User who the task is assigned to.

</td></tr><tr><td>

Asset

</td><td>

Asset that you are selecting for the inbound asset order line. Select an asset that meets the following criteria:-   Matches all criteria specified in the order line.
-   The **DaaS asset** option is enabled in the corresponding asset record.
-   An account is specified in the **DaaS account** field of the corresponding asset record.
**Note:** For more information on the **DaaS asset** and **DaaS account** fields, see [Asset fields for enterprise assets](../reference/asset-fields-eam.md).

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Notes about that task that are visible to all users within your organization.

</td></tr></tbody>
</table>5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Asset selection task closes with an updated state of Closed Complete.
-   A corresponding Asset pick task is automatically generated.

## What to do next

The provider asset technician must complete the corresponding Asset pick task by picking the asset that you selected for the inbound asset order line. For detailed instructions, see [Complete the Asset pick task for a requested Device as a Service \(DaaS\) asset](pick-selected-daas-asset-inbound-asset-order.md).

**Parent Topic:**[Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md)

