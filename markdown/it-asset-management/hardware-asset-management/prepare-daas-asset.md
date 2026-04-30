---
title: Prepare the picked asset
description: Prepare the picked asset by inspecting the checklist and also check for any defects by using the Asset prepare task.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing inbound asset orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Prepare the picked asset

Prepare the picked asset by inspecting the checklist and also check for any defects by using the Asset prepare task.

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

8.  Select the asset task number with the Task type as **Asset prepare task**.

9.  On the form, fill in the fields.

<table id="table_j5m_z5s_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Asset prepare task.

</td></tr><tr><td>

Asset order line

</td><td>

The inbound asset order line number associated with this task.

</td></tr><tr><td>

Due date

</td><td>

Estimated date of completing this task.

</td></tr><tr><td>

Stockroom

</td><td>

The designated stockroom where the asset is allocated.

</td></tr><tr><td>

Model

</td><td>

This field is automatically populated with the details of the model provided while creating an inbound asset order line. For more information, see [Create an inbound asset order line](create-inbound-order-line.md).

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Prepare`.

</td></tr><tr><td>

State

</td><td>

Status of the Asset prepare task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Asset prepare task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Asset prepare task.

</td></tr><tr><td>

Asset

</td><td>

The asset that is selected in the Asset selection task. For more information, see [Select an asset](select-daas-asset.md).

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

-   After the Asset prepare task is completed and you refresh the list, another task is created displaying a unique asset task number with the task type as **Asset ship task**.
-   The **State** field of the Asset prepare task is set to **Closed Complete**.
-   The **Stage** field of the Inbound asset order line is set to **Ship**.

## What to do next

[Ship the prepared asset](ship-daas-asset.md)

