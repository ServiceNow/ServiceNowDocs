---
title: Create an inbound asset order line
description: Create an inbound asset order line for every asset in an inbound asset order.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing inbound asset orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Create an inbound asset order line

Create an inbound asset order line for every asset in an inbound asset order.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager

-   Install the Hardware Asset Management for DaaS application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Install the Hardware Asset Management application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## About this task

For an inbound asset order line to be considered complete, the **State** field of all its tasks must be **Closed Complete**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **DaaS provider** view.

3.  Select the **Inbound asset orders** tab.

4.  Select an inbound asset order number.

5.  Select the **Inbound asset order lines** tab.

6.  Select **New**.

7.  On the form, fill in the fields.

<table id="table_pzr_t4s_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the inbound asset order line.

</td></tr><tr><td>

Inbound asset order

</td><td>

Unique number for the inbound asset order, which is associated with this order number line.

</td></tr><tr><td>

Model

</td><td>

Model of the asset as requested by the DaaS provider.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of the asset.This field is automatically set to `1`.

</td></tr><tr><td>

Stage

</td><td>

Status of the inbound asset order.This field is automatically set to `Draft`.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the inbound asset order line.

</td></tr><tr><td>

Asset

</td><td>

Asset that is selected matching the model.This field automatically populates when you select an asset in the Asset selection task.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

-   An inbound asset order line with a unique number is created for the requested asset.
-   The **Stage** field is set to `Selection`.
-   The **Asset tasks** tab is created, displaying a unique asset task number with the task type as **Asset selection task**.

## What to do next

[Select a DaaS asset matching the model specified by the DaaS provider.](select-daas-asset.md)

