---
title: Create an RMA response order
description: Create a Return Merchandise Authorization \(RMA\) response order to associate an RMA request for an asset.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Create an RMA response order

Create a Return Merchandise Authorization \(RMA\) response order to associate an RMA request for an asset.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager

-   Install the Hardware Asset Management for DaaS application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Install the Hardware Asset Management application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## About this task

For an RMA response order to be considered as complete, all its RMA response order lines must reach the **Complete** stage.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **DaaS provider** view.

3.  Select the **RMA orders** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_qcg_m2s_2bc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the RMA response order.

</td></tr><tr><td>

External RMA number

</td><td>

Customer-provided reference for the RMA request that helps you track the source.

</td></tr><tr><td>

DaaS account

</td><td>

Associated DaaS account of the customer.

</td></tr><tr><td>

Contact Email

</td><td>

Email of the customer who initiated the RMA request.

</td></tr><tr><td>

Delivery address

</td><td>

Address of the customer associated with the RMA request.

</td></tr><tr><td>

State

</td><td>

Status of the RMA response order.This field is automatically set to `Open`.

</td></tr><tr><td>

Requested for

</td><td>

Name of the customer associated with the DaaS account, for whom the asset is requested.

</td></tr><tr><td>

Opened by

</td><td>

Estimated delivery date of the asset that's being sent to the specified delivery address.

</td></tr><tr><td>

Customer mobile number

</td><td>

Mobile number of the customer who initiated the RMA request.

</td></tr><tr><td>

Device location

</td><td>

The physical whereabouts of the device currently in operation.

</td></tr><tr><td>

RMA justification

</td><td>

Reason of the RMA request creation provided by the customer.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

-   An RMA response order with a unique number is created.
-   **RMA response order lines** tab is displayed.

## What to do next

[Create an RMA response order line](create-rma-response-order-line.md).

