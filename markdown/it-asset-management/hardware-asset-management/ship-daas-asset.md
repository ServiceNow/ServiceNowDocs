---
title: Ship the prepared asset
description: Ship the prepared asset and capture the shipment details by using the Asset ship task.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing inbound asset orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Ship the prepared asset

Ship the prepared asset and capture the shipment details by using the Asset ship task.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager and inventory\_user

-   Install the Hardware Asset Management for DaaS application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Install the Hardware Asset Management application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **DaaS provider** view.

3.  Select the **Inbound asset orders** tab.

4.  Select an inbound asset order number.

5.  Select the **Inbound asset order lines** tab.

6.  Select an inbound asset order line number.

7.  Select the **Asset tasks** tab.

8.  Select the asset task number with the Task type as **Asset ship task**.

9.  On the form, fill in the fields.

<table id="table_j5m_z5s_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Asset ship task.

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

The asset that is selected in the Asset selection task. For more information, see [Select an asset](select-daas-asset.md).

</td></tr><tr><td>

Shipping carrier

</td><td>

Organization that's responsible for shipping the assets to your customers. For example, FedEx.

</td></tr><tr><td>

Ship from

</td><td>

The origin location for shipping the assets.

</td></tr><tr><td>

Ship date

</td><td>

The shipment date for delivering the assets to your customers.

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Ship`.

</td></tr><tr><td>

State

</td><td>

Status of the Asset ship task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Asset ship task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Asset ship task.

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

Reference to the shipment record created in the Shipment \[sn\_itam\_common\_shipment\] table.This field is automatically populated when the Asset ship task is closed.

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

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>10. Select **Close Task**.


## Result

-   After the Asset ship task is completed and you refresh the list, another task is created displaying a unique asset task number with the task type as **Receive task**.
-   The **State** field of the Asset ship task is set to **Closed Complete**.
-   The **Stage** field of the Inbound asset order line is set to **Receive confirmation**.

## What to do next

[Receive the shipped asset](receive-daas-asset.md)

