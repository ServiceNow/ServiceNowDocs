---
title: Create an advanced resource filter for dispatchers
description: Create an advanced resource filter so all dispatchers can use the same filter in Dispatcher Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced resource filters, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Create an advanced resource filter for dispatchers

Create an advanced resource filter so all dispatchers can use the same filter in Dispatcher Workspace.

## Before you begin

Role required: admin

## About this task

When administrators create an advanced resource filter for dispatchers they show up in the Resource filter drop-down menu in Dispatcher Workspace. All advanced filters created by administrators show up alphabetically at the top of the resource filters list. Dispatcher created filters show below the list of administrator filters.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** &gt; **Resource Filter**.

2.  Select **New**.

3.  Fill in the fields in the form:

    -   Title: The name of the filter that will show in Dispatcher Workspace.
    -   Active: if the filter is active.
4.  Select **Submit**.

5.  Select the name of the filter you just created.

6.  Select **New**.

7.  Fill in the fields on the form.

<table id="choicetable_s3x_q1x_vfc"><thead><tr><th align="left" id="d29554e158">

Field

</th><th align="left" id="d29554e161">

Description

</th></tr></thead><tbody><tr><td id="d29554e167">

**Table**

</td><td>

Select the view. The choices are:-   agent\_filter\_config\_view
-   crew\_filter\_config\_view
-   equipment\_filter\_config\_view
-   contractor\_filter\_config\_view


</td></tr><tr><td id="d29554e190">

**Filter**

</td><td>

Add the conditions and clauses that will be used to filter the information in the table you selected.

</td></tr></tbody>
</table>8.  Select **Submit**.

    The filter is added to dispatcher workspace for dispatchers to use.


