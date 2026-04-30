---
title: Receive asset
description: After the shipment of the asset to the DaaS provider is complete, confirm the receipt of the asset by using the Receive task.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Receive asset

After the shipment of the asset to the DaaS provider is complete, confirm the receipt of the asset by using the Receive task.

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

6.  Select the asset task number with the Task type as **Receive asset**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Receive asset task.

</td></tr><tr><td>

Asset order line

</td><td>

The RMA response order line number associated with this task.

</td></tr><tr><td>

Due date

</td><td>

Estimated date of completing this task.

</td></tr><tr><td>

Asset

</td><td>

The asset that is selected while creating the associated RMA response order line.For more information, see [Create an RMA response order line](create-rma-response-order-line.md).

</td></tr><tr><td>

Asset received

</td><td>

Option to confirm the receipt of the asset.Values:

-   **Yes**: The asset is received by the DaaS provider.
-   **No**: The asset isn't received by the DaaS provider.
**Note:** You must select **Yes** to close this task.

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Receive confirmation`.

</td></tr><tr><td>

State

</td><td>

Status of the Receive task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working the Receive confirmation task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Receive task.

</td></tr><tr><td>

Stockroom

</td><td>

Brief description of the task.

</td></tr><tr><td>

Short description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Description

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr><tr><td>

Work notes

</td><td>

Unique number for the Receive task.

</td></tr></tbody>
</table>8.  Select **Close Task**.


## Result

-   The result of the task completion changes according to the value selected in the **Asset received** field:
    -   If you select **Yes** for an on-site assessment of your asset, the **State** field of the Receive task is set to **Closed Complete**. The **Stage** field of the Inbound asset order line is set to **Completed**. The **State** field of the Inbound asset order is set to **Closed Complete**.
    -   If you select **Yes** for an off-site assessment of your asset, a task is created displaying a unique asset task number with the task type as **Evaluate RMA asset** after you refresh the list. The **Stage** field of the Inbound asset order line is set to **Evaluation**.
-   The **State** field of the Receive asset task is set to **Closed Complete**.

## What to do next

[Evaluate the RMA asset](evaluate-rma-asset.md)

