---
title: Create an inbound asset order
description: Create an inbound asset order to associate a customer request to an asset order.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing inbound asset orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Create an inbound asset order

Create an inbound asset order to associate a customer request to an asset order.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager

-   Install the Hardware Asset Management for DaaS application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Install the Hardware Asset Management application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## About this task

For an inbound asset order to be considered complete, all its inbound asset order lines must reach the **Complete** stage.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **DaaS provider** view.

3.  Select the **Inbound asset orders** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_qcg_m2s_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the inbound asset order.

</td></tr><tr><td>

External request reference

</td><td>

Customer-provided reference for the asset request that helps you track the source. For example, the customer has requested an asset through an email. Here, the external request reference would be `xyz@gmail.com`.

</td></tr><tr><td>

DaaS account

</td><td>

Associated DaaS account of the customer.

</td></tr><tr><td>

Delivery address

</td><td>

Designated delivery address for the asset.

</td></tr><tr><td>

State

</td><td>

Status of the inbound asset order.This field is automatically set to `Open`.

</td></tr><tr><td>

Requested for

</td><td>

The name of the customer associated with the DaaS account, for whom the asset is requested.

</td></tr><tr><td>

Estimated delivery date

</td><td>

Estimated delivery date of the asset that's being sent to the specified delivery address.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

-   An inbound asset order with a unique number is created.
-   **Inbound asset order line** tab is created.

## What to do next

[Create an inbound asset order line](create-inbound-order-line.md)

