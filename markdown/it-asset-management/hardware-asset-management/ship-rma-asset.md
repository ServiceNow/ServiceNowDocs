---
title: Ship the asset to the DaaS provider
description: Return the asset to the DaaS provider and record the shipment details using the Ship task.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Ship the asset to the DaaS provider

Return the asset to the DaaS provider and record the shipment details using the Ship task.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager or inventory\_user

-   Install the Hardware Asset Management for DaaS application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Install the Hardware Asset Management application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **DaaS provider** view.

3.  Select the **RMA orders** tab.

4.  Select an RMA order number.

5.  Select the **RMA response order lines** tab.

6.  Select the asset task number with the Task type as **Ship**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Ship task.

</td></tr><tr><td>

Asset order line

</td><td>

The inbound asset order line number associated with this task.

</td></tr><tr><td>

Due date

</td><td>

Estimated date of completing this task.

</td></tr><tr><td>

Asset

</td><td>

The asset that is selected while creating the associated RMA response order line.For more information, see [Create an RMA response order line](create-rma-response-order-line.md).

</td></tr><tr><td>

Shipping carrier

</td><td>

Organization that's responsible for shipping the assets to the DaaS provider. For example, FedEx.

</td></tr><tr><td>

Ship from

</td><td>

The origin location for shipping the assets.

</td></tr><tr><td>

Ship date

</td><td>

The shipment date for delivering the assets to the DaaS provider.

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Ship`.

</td></tr><tr><td>

State

</td><td>

Status of the Ship task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working the Ship task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Ship task.

</td></tr><tr><td>

Tracking number

</td><td>

Tracking number or reference number of the shipment of the asset.

</td></tr><tr><td>

Ship to

</td><td>

Destination for the asset shipment.

</td></tr><tr><td>

Shipment order

</td><td>

Reference to the shipment record created in the Shipment \[sn\_itam\_common\_shipment\] table.This field is automatically populated when the Ship task is closed.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>8.  Select **Close Task**.


## Result

-   After the Ship task is completed and you refresh the list, a task is created displaying a unique asset task number with the task type as **Receive asset**.
-   The **Shipment assets** tab is displayed, which includes the shipment information.
-   The **State** field of the Ship task is set to **Closed Complete**.
-   The **Stage** field of the RMA response order line is set to **Receive**.

## What to do next

[Receive asset](receive-rma-asset.md)

