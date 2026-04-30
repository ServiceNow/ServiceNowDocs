---
title: Create a matching rule for anonymous chat
description: Create one matching rule for each agent queue.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Anonymous chat, Administer, Customer Service Management]
---

# Create a matching rule for anonymous chat

Create one matching rule for each agent queue.

## Before you begin

Role required: admin

## About this task

A chat request is tied to a chat queue based on the selected issue type.

## Procedure

1.  Navigate to **All** &gt; **Routing and Assignment** &gt; **Matching Rules**.

2.  Click **New**.

3.  Enter a **Name** for the matching rule.

4.  In the **Table** field, select **Customer Interaction**.

5.  In the **Conditions** field, use the condition builder to create the following conditions.

<table id="table_qwl_gyb_fx"><thead><tr><th>

Field

</th><th>

Operator

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Channel

</td><td>

is

</td><td>

Chat

</td></tr><tr><td>

Category

</td><td>

is

</td><td>

Select one of the categories created for anonymous users to define an issue on the record producer: -   Product Issue
-   Billing Issue
-   Order Issue


</td></tr></tbody>
</table>6.  Click **Submit**.


