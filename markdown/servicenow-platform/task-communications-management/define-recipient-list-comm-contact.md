---
title: Define a recipient list for communication contact
description: A recipient list lets you specify a filter to fetch a list of users. Use the recipient list as the contact for a particular communication plan.
locale: en-US
release: yokohama
product: Task Communications Management
classification: task-communications-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with Task Communications Management, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a recipient list for communication contact

A recipient list lets you specify a filter to fetch a list of users. Use the recipient list as the contact for a particular communication plan.

## Before you begin

Role required: sn\_comm\_management.comm\_plan\_admin or admin

## About this task

Sometimes, the contacts that you want to include in a plan can only be known dynamically. For example, you might want the support group associated with a particular business service in an incident to be involved in the communication plan. The support group might change depending on the business service that you select. In such a case, a recipient list provides the flexibility to add recipients dynamically.

## Procedure

1.  Navigate to **All** &gt; **Task Communications Management** &gt; **Administration** &gt; **Recipients Lists**.

2.  Click **New** to create a new recipient list.

3.  On the form, fill in the fields.

<table id="table_ish_5tl_2db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the recipient list.

</td></tr><tr><td>

Type

</td><td>

Type of recipient.

</td></tr><tr><td>

State

</td><td>

\[Read only\] The state of the recipient list.

</td></tr><tr><td class="sub-head" colspan="2">

Setup

</td></tr><tr><td>

Method

</td><td>

The method used to generate the recipient list.-   Upload File: Upload an Excel file with the recipient information to create a recipient list. This list is static.
-   Dynamic Condition: Use scripts or conditions to receive recipient information.


</td></tr></tbody>
</table>4.  Click **Submit**.

    A recipient list is defined for the contact.


## What to do next

Define a communication contact for the task.

**Parent Topic:**[Working with Task Communications Management](../concept/working-with-tcm.md)

