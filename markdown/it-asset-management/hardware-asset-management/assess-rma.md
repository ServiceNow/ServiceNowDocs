---
title: Assess the RMA asset
description: Assess the Return Merchandise Authorization \(RMA\) asset using either an on-site or off-site assessment procedure.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Assess the RMA asset

Assess the Return Merchandise Authorization \(RMA\) asset using either an on-site or off-site assessment procedure.

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

6.  Select the asset task number with the Task type as **RMA assessment**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the RMA assessment task.

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

Assessment action

</td><td>

Assessment procedure to be followed for the RMA asset.-   **On site**: A representative from the DaaS provider visits the customer's premises to assess the asset.
-   **Off site**: The asset arrives at the DaaS provider site for assessment.
-   **Denied**: The RMA request is rejected.


</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `RMA assessment`.

</td></tr><tr><td>

State

</td><td>

Status of the RMA assessment task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the RMA assessment task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the RMA assessment task.

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

-   The result of the task completion changes according to the value selected in the **Assessment action** field:
    -   If you select **On site**, a task is created displaying a unique asset task number with the task type as **Schedule** after you refresh the list. The **Stage** field of the RMA response order line is set to `Schedule`.
    -   If you select **Off site**, a task is created displaying a unique asset task number with the task type as **Ship** after you refresh the list. The **Stage** field of the RMA response order line is set to `Ship`.
    -   If you select **Denied**, the RMA response order line is set to **Closed Complete**. If there are no more open RMA response order lines, then the RMA response order is closed.
-   The **State** field of the RMA assessment task is set to **Closed Complete**.

## What to do next

[Schedule a visit to the customer site](schedule-rma-daas.md) or [Ship the asset to the DaaS provider](ship-rma-asset.md)

