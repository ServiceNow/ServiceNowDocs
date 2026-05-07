---
title: Configure the task plan template
description: Configure the task plan template to add conditions to a template item that determines when a template item is applicable for domain orders.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task plan template, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Configure the task plan template

Configure the task plan template to add conditions to a template item that determines when a template item is applicable for domain orders.

## Before you begin

Before you add filter condition, make sure that the task template target record is domain order.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **All Task Plan Templates**.

2.  Open the record.

    Use this field to add the conditions for the template item. Each condition contains a field, operator, and value\(s\).

3.  Select **Add Filter Condition**.

    -   Add these conditions:

        |Fields|Conditions|
        |------|----------|
        |Choose Field|Select **Specification**.|
        |oper|is|
        |Value|Select the specification from the list of records for domain order.|

        ![task plan template.](../image/task-plan-condition.png)

    -   Select **+New condition set** to add a new condition.

        Add these conditions:

<table id="table_mzl_rzk_m3c"><thead><tr><th>

Fields

</th><th>

Conditons

</th></tr></thead><tbody><tr><td>

Choose Field

</td><td>

Select **Action** from the list.

</td></tr><tr><td>

oper

</td><td>

is

</td></tr><tr><td>

Value

</td><td>

Select one of these values from the drop-down list:-   Add
-   Change
-   Disconnect
-   Cancel
-   Suspend
-   Resume


</td></tr></tbody>
</table>    -   Select **x** to remove a condition.
    -   Select **Set** to save the conditions and close the pop-up window.
4.  Select **Update**.


