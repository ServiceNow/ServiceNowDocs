---
title: Select an asset
description: Select a DaaS asset matching the model specified by the DaaS provider by using the Asset selection task.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing inbound asset orders for DaaS assets, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Select an asset

Select a DaaS asset matching the model specified by the DaaS provider by using the Asset selection task.

## Before you begin

Role required: sn\_daas\_ham.daas\_asset\_manager or inventory\_user

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

8.  Select the asset task number with the Task type as **Asset selection task**.

9.  On the form, fill in the fields.

<table id="table_mjq_fss_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the Asset selection task.

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

This field is automatically populated with the details of the model provided while creating an inbound asset order line.For more information, see [Create an inbound asset order line](create-inbound-order-line.md).

</td></tr><tr><td>

Task name

</td><td>

Name of the current task.This field is automatically set to `Select`.

</td></tr><tr><td>

State

</td><td>

Status of the Asset selection task.This field is automatically set to `Open`.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group for the individual who is responsible for working on the Asset selection task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual responsible for working on the Asset selection task.

</td></tr><tr><td>

Asset

</td><td>

List of DaaS assets that fulfill one or more of the following conditions:-   Assets with **Status** as **In stock** and **Substate** as **Available**
-   An account is selected in the **DaaS account** field while creating an inbound asset order.
-   The **DaaS account** field is empty while creating an inbound asset order.


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

-   After the Asset selection task is completed and you refresh the list, a task is created displaying a unique asset task number with the task type as **Asset pick task**.
-   The **State** field of the Asset Selection task is set to **Closed Complete**.
-   The **Stage** field of the Inbound asset order line is set to **Pick**.

## What to do next

[Pick the selected asset](pick-daas-asset.md)

