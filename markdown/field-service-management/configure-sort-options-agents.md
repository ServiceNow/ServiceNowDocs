---
title: Configure agent list sort options
description: Configure the options available for dispatchers to sort agents in the Dispatcher Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure agent list sort options

Configure the options available for dispatchers to sort agents in the Dispatcher Workspace.

## Before you begin

Role required: admin

## About this task

By default, dispatchers can view recommended agents based on the distance to the work order task, skills, or parts.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Agent Sorting**.

2.  Select **New**.

3.  On the form, fill in the fields.

    **Note:** The **Category** and **Application** fields are read-only.

<table id="table_xp1_hlt_jnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the sort option.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the sort option to appear in Dispatcher Workspace.

</td></tr><tr><td>

Display Name

</td><td>

Labels for the fields that appear as the sort option in Dispatcher Workspace.

</td></tr><tr><td>

Ranking Method

</td><td>

-   **More is better**: When setting the ranking, a higher value is better. For example, more availability is better when determining the agent ranking.
-   **Less is better**: When setting the ranking, a lower value is better. For example, fewer cases are better when determining the agent ranking.


</td></tr><tr><td>

Order

</td><td>

Display order of the sort option in Dispatcher Workspace.

</td></tr><tr><td>

Criterion

</td><td>

Criteria to determine the agents that are displayed in the list.

</td></tr></tbody>
</table>4.  Select **Submit**.

    ![agent recommendation sort criteria form](../image/agent-sort-options.png)


