---
title: Define criteria of a rate model
description: Set the criteria of a rate model by adding attributes from a set of predefined entities to derive resource hourly rates based on the criteria.
locale: en-US
release: yokohama
product: Rate Model
classification: rate-model
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Rate Models, Project Portfolio Management, Strategic Portfolio Management]
---

# Define criteria of a rate model

Set the criteria of a rate model by adding attributes from a set of predefined entities to derive resource hourly rates based on the criteria.

## Before you begin

Role required: pps\_admin or it\_rate\_model\_admin

## About this task

A rate model consists of one or more rate lines. Each line contains a unique combination of criteria values and the hourly rate of a resource. You define the criteria by adding up to 10 attributes from the following entities:

-   Project
-   Project task
-   Demand
-   User
-   Group
-   Role
-   Resource plan

You can select attributes of type String, Reference, Number, Boolean, and Choice.

## Procedure

1.  Open a rate model by performing one of the following actions:

    -   Navigate to **All** &gt; **Project Administration** &gt; **Rate Model** &gt; **All**.
    -   Navigate to **All** &gt; **Time Sheets** &gt; **Rate Model** &gt; **All**.
2.  In the **Rate Model Attributes** related list, click **New**.

3.  On the form, fill in the fields.

<table id="table_ygf_cv1_ffb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

</td><td>

Entity from which the attribute is used to define the criteria.

</td></tr><tr><td>

Attribute

</td><td>

List of attributes from the selected entity to define the criteria.

</td></tr><tr><td>

Priority

</td><td>

Unique number that determines the order in which attributes in a rate model are evaluated to derive the hourly rate.An attribute with the lowest priority is evaluated first.

 **Note:** Two attributes cannot have the same priority.

</td></tr><tr><td>

Name

</td><td>

User-friendly name for identifying the attribute. The default name populated is based on the selected entity and attribute. For example, if you select Resource in the **Entity** field and Location in the **Attribute** field, then the default name is Resource/Location.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

[Create rate lines to define the hourly rates for resources.](create-rate-line.md)

**Parent Topic:**[Rate Models](../concept/rate-model.md)

