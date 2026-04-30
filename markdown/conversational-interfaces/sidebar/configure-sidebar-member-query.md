---
title: Configuring Sidebar member query
description: Configuring the Sidebar member query pre-populates the participants list on the Start a Sidebar discussion screen.
locale: en-US
release: xanadu
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Sidebar, Conversational Interfaces]
---

# Configuring Sidebar member query

Configuring the Sidebar member query pre-populates the participants list on the Start a Sidebar discussion screen.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  From the menu on the CI Admin Experience page, select Sidebar.

    The Sidebar settings screen with the heading "Adjust how live agents collaborate to support your users" displays.

3.  From the Participants section on the Sidebar settings screen, select **View Settings**.

    The Sidebar Member Query screen displays.

4.  Do one of the following:

    -   To edit an existing query, select the name of the query.
    -   To create a new query, select **New**.
5.  Fill in the fields:

<table id="table_n43_j5p_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the member query.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the query is active.

</td></tr><tr><td>

Type

</td><td>

From the drop-down list, select **Pre-fill** or **Search**.-   Pre-fill: Automatically select all members of the assignment group.
-   Search: Add only members of the assignment group.


</td></tr><tr><td>

Order

</td><td>

Order in which the routing condition for this queue is considered, in comparison to other queues.

</td></tr><tr><td>

Application

</td><td>

Type of scoped application.

</td></tr><tr><td>

Condition Mode

</td><td>

Type of condition for routing work items in the query. From the drop-down list, select **Advanced** or **Simple**.

-   Simple: Specify a routing condition using the condition builder.
-   Advanced: Specify a JavaScript scripted condition.


</td></tr><tr><td>

Condition table

</td><td>

Displays if you selected **Simple** for the Condition Mode. From the drop-down list, select the table.

</td></tr><tr><td>

Condition

</td><td>

Displays if you selected **Simple** for the Condition Mode. Use the **Add Filter Condition** and **Add "OR" Clause** buttons to create the condition for the query.

</td></tr><tr><td>

Condition Script

</td><td>

Displays if you selected **Advanced** for the Condition Mode. Enter a JavaScript script to build the query.

</td></tr><tr><td>

User Query Mode

</td><td>

From the drop-down list, select **Advanced** or **Simple**.

-   Simple: Specify a routing condition using the condition builder.
-   Advanced: Specify a JavaScript scripted condition.


</td></tr><tr><td>

User Query Condition

</td><td>

Displays if you select **Simple** for the User Query Mode. Use the **Add Filter Condition** and **Add "OR" Clause** buttons to create the condition for the query.

</td></tr><tr><td>

User Query Script

</td><td>

Displays if you select **Advanced** for the User Query Mode. You can specify a JavaScript script to build the query.

</td></tr></tbody>
</table>6.  Select **Submit**.


