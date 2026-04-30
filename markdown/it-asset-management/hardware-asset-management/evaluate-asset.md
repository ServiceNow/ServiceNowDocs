---
title: Evaluate the repaired asset
description: Evaluate the status of the repaired asset and indicate the evaluation result as redeployable or identified for disposal.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Evaluate the repaired asset

Evaluate the status of the repaired asset and indicate the evaluation result as redeployable or identified for disposal.

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

6.  Select the asset task number with the Task type as **Evaluate asset**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Evaluate asset task.

</td></tr><tr><td>

Asset order line

</td><td>

The RMA response order line number associated with this task.

</td></tr><tr><td>

State

</td><td>

Status of the Evaluate asset task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Evaluate asset task.

</td></tr><tr><td>

Evaluation result

</td><td>

Indication of whether the asset has to be redeployed or disposed.-   **Redeployable**: The asset is functioning properly.
-   **To be disposed**: The asset didn't pass certain quality checks and can't be returned to the customer.


</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Evaluate asset`.

</td></tr><tr><td>

Stockroom

</td><td>

This field is automatically populated with the stockroom details that you provided in the Receive task.For more information, see [Receive asset](receive-rma-asset.md).

**Note:** This field doesn't include any information for the On-site assessment flow. For more information about selecting the assessment action, see [Assess the RMA asset](assess-rma.md).

</td></tr><tr><td>

Due date

</td><td>

Estimated date of completing this task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Repair asset task.

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

The result of the task completion changes according to the value selected in the **Evaluation result** field:

-   If you select **Redeployable**, the **State** field of the Evaluate task is set to **Closed Complete**. The **Stage** field of the RMA response order line is set to **Completed**.
-   If you select **To be disposed**, a task is created displaying a unique asset task number with the task type as **Ship** after you refresh the list. The **Stage** field of the RMA response order line is set to **Inbound shipment**. A new inbound asset order is created.

## What to do next

[Ship the asset to the DaaS provider](ship-rma-asset.md)

