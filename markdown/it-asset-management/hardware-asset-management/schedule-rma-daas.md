---
title: Schedule a visit to the customer site
description: Schedule a visit of the DaaS provider representative to the customer location.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing RMA response orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Schedule a visit to the customer site

Schedule a visit of the DaaS provider representative to the customer location.

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

6.  Select the asset task number with the Task type as **Schedule**.

7.  On the form, fill in the fields.

<table id="table_fhc_sbq_kbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Schedule task.

</td></tr><tr><td>

Asset order line

</td><td>

The RMA response order line number associated with this task.

</td></tr><tr><td>

Due date

</td><td>

Estimated date of completing this task.

</td></tr><tr><td>

Scheduled date

</td><td>

The scheduled date for the DaaS provider representative to visit the customer's location.

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Schedule`.

</td></tr><tr><td>

State

</td><td>

Status of the Schedule task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Schedule task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Schedule task.

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

-   After the Schedule task is completed and you refresh the list, a task is created displaying a unique asset task number with the task type as **Evaluate RMA asset**.
-   The **State** field of the Schedule task is set to **Closed Complete**.
-   The **Stage** field of the Inbound asset order line is set to **Evaluation**.

## What to do next

[Evaluate the RMA asset](evaluate-rma-asset.md)

