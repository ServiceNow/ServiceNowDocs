---
title: Create a learning template
description: Create a learning template to simplify the process of creating learning tasks by populating fields automatically.
locale: en-US
release: yokohama
product: Learning Posts
classification: learning-posts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Initiate a learning task from a lifecycle event, Learning Posts, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Create a learning template

Create a learning template to simplify the process of creating learning tasks by populating fields automatically.

## Before you begin

Role required: learning\_admin

## Procedure

1.  Navigate to **Learning Administration** &gt; **Administration** &gt; **Templates**

2.  Click **New**.

3.  On the form, fill in the fields as appropriate.

<table id="table_yrd_s5q_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the learning template.

</td></tr><tr><td>

Table

</td><td>

Table that this template applies to. Select Learning task \[sn\_lc\_learning\_task\]

</td></tr><tr><td>

Template

</td><td>

Content that automatically populates records that are based on this template. -   From the list, select **Learning library** and search for the library item.
-   From the list, select **Course item** and search for course item.
-   From the list, select **State** and select a state for the learning task.
-   From the list, select **Short description** and add a suitable description for the learning task.


</td></tr><tr><td>

Use global descriptions for translations

</td><td>

Option to enable the use of global descriptions for translations. If selected, you can provide the short description and description for the learning task template in one or more languages.

</td></tr><tr><td>

Link template

</td><td>

Template that links a child table with the template for the parent table. In the template for the child table, set the value to the field that references the parent table. After you set the value, the child template is explicitly linked to the parent table.

</td></tr><tr><td>

Additional fields

</td><td>

In the **Assign to** field, specify the user to whom the learning task is applicable.

</td></tr></tbody>
</table>    **Important:** You must specify values in **Catalog**, **Course item**, **State** **Short description**, and **Assign to** fields while creating the template. If any of the fields is left empty, the learning task will not be created as part of the life cycle event and an error is recorded in System Logs.

4.  Click **Submit**.


