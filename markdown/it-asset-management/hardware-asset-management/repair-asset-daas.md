---
title: Repair the RMA asset
description: Indicate whether the Return Merchandise Authorization \(RMA\) asset has been repaired or considered unrepairable.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Repair the RMA asset

Indicate whether the Return Merchandise Authorization \(RMA\) asset has been repaired or considered unrepairable.

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

6.  Select the asset task number with the Task type as **Repair asset**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Repair asset task.

</td></tr><tr><td>

Asset order line

</td><td>

The RMA response order line number associated with this task.

</td></tr><tr><td>

State

</td><td>

Status of the Repair asset task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Repair asset task.

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Repair asset`.

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

Repair result

</td><td>

Indication of whether the Return Merchandise Authorization \(RMA\) asset has been repaired or considered unrepairable.-   Repaired
-   Unrepairable


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

-   The result of the task completion changes according to the value selected in the **Repair result** field:
    -   If you select **Repaired**, a task is created displaying a unique asset task number with the task type as **Evaluate asset** after you refresh the list. The **Stage** field of the RMA response order line is set to **Quality check**.
    -   If you select **Unrepairable**, a task is created displaying a unique asset task number with the task type as **Ship** after you refresh the list. The **Stage** field of the RMA response order line is set to **Inbound shipment**. A new inbound asset order is created.
-   The **State** field of the Repair asset task is set to **Closed Complete**.

## What to do next

[Evaluate the repaired asset](evaluate-asset.md) or [Ship the asset to the DaaS provider](ship-rma-asset.md)

