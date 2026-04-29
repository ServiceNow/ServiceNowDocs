---
title: Evaluate the RMA asset
description: Evaluate the Return Merchandise Authorization \(RMA\) asset on the scheduled date at the customer location.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Evaluate the RMA asset

Evaluate the Return Merchandise Authorization \(RMA\) asset on the scheduled date at the customer location.

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

6.  Select the asset task number with the Task type as **Evaluate RMA asset**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Evaluate RMA asset task.

</td></tr><tr><td>

Asset order line

</td><td>

The RMA response order line number associated with this task.

</td></tr><tr><td>

Due date

</td><td>

Estimated date of completing this task.

</td></tr><tr><td>

State

</td><td>

Status of the Evaluate RMA asset task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Evaluate RMA asset task.

</td></tr><tr><td>

Evaluation result

</td><td>

-   **Repairable**: The asset can be repaired.
-   **Replace**: The asset can't be repaired and the old asset would be returned to the DaaS provider. A new inbound asset order would get created for requesting a new asset with the same model.


</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Evaluate RMA asset`.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Evaluate RMA asset task.

</td></tr><tr><td>

Asset

</td><td>

The asset that is selected while creating an RMA response order line.For more information, see [Create an RMA response order line](create-rma-response-order-line.md).

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

-   The result of the task completion changes according to the value selected in the **Evaluation result** field:
    -   If you select **Repairable**, a task is created displaying a unique asset task number with the task type as **Repair asset** after you refresh the list. The **Stage** field of the RMA response order line is set to **Repair**.
    -   If you select **Replace**, a task is created displaying a unique asset task number with the task type as **Ship** after you refresh the list. The **Stage** field of the RMA response order line is set to **Inbound shipment**. A new inbound asset order is created.
-   The **State** field of the Evaluate RMA asset task is set to **Closed Complete**.

## What to do next

[Repair the RMA asset](repair-asset-daas.md) or [Ship the asset to the DaaS provider](ship-rma-asset.md)

