---
title: Create an RMA response order line
description: Create a Return Merchandise Authorization \(RMA\) response order line for every asset in an RMA response order.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Create an RMA response order line

Create a Return Merchandise Authorization \(RMA\) response order line for every asset in an RMA response order.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager

-   Install the Hardware Asset Management for DaaS application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Install the Hardware Asset Management application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## About this task

For an RMA response order line to be considered as complete, the **State** field of all its tasks must be **Closed Complete**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **DaaS provider** view.

3.  Select the **RMA orders** tab.

4.  Select an RMA order number.

5.  Select the **RMA response order lines** tab.

6.  Select **New**.

7.  On the form, fill in the fields.

<table id="table_pzr_t4s_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the RMA response order line.

</td></tr><tr><td>

Parent

</td><td>

Unique number for the RMA response order, which is associated with this order number line.

</td></tr><tr><td>

Model

</td><td>

Model of the asset for which the customer has initiated an RMA request.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of the asset.This field is automatically set to `1`.

</td></tr><tr><td>

Stage

</td><td>

Status of the RMA response order line.This field is automatically set to `Draft`.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the RMA response order line.

</td></tr><tr><td>

Asset

</td><td>

List of assets that are in use and assigned to the customer.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

-   An RMA response order line with a unique number is created.
-   The **Stage** field is set to `Assess`.
-   The **Asset tasks** tab is created, displaying a unique asset task number with the task type as **RMA assessment**.

## What to do next

[Assess the RMA asset](assess-rma.md).

