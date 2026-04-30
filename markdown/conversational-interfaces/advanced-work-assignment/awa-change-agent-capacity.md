---
title: Override agent capacity for selected agents
description: Change the default number of work items that an agent can handle for a service channel.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Override agent capacity for selected agents

Change the default number of work items that an agent can handle for a service channel.

## Before you begin

Role required: awa\_admin or admin

## About this task

To change the capacity for selected agents, use the **Agent Capacity Override** related list for the service channel. To change the capacity for one or more members of a selected group, use the **Agent Capacity Override** related list for the group \(**Advanced Work Assignment** &gt; **Groups**\).

## Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Select the service channel.

3.  In the **Agent Capacity Override** related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_fdy_rhq_gfb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Service Channel

</td><td>

Name of the selected channel.

</td></tr><tr><td>

Override Capacity

</td><td>

Number of work items that the selected agents can handle.

</td></tr><tr><td>

Users

</td><td>

Agents to which this override applies. Move the agent names from the **Available** list to the **Selected** list.You can use the filter to identify conditions that restrict the list of agents.

**Note:** The filter shows only users or groups that have AWA roles \(awa\_agent, awa\_manager, awa\_admin, admin\).

</td></tr></tbody>
</table>5.  Select **Submit**.

    The selected agents and their associated capacity values are listed in the Agent Capacities table.


## What to do next

If you’re configuring a service channel, you can [create or change an inbox layout](awa-modify-inbox-layout.md) for the channel.

**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

