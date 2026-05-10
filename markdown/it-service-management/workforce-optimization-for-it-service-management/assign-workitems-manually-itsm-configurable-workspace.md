---
title: Allocate work items manually to agents
description: Allocate pending work items to agents to complete the work.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Routing work items, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Allocate work items manually to agents

Allocate pending work items to agents to complete the work.

## Before you begin

Role required: sn\_wfo\_cfg\_ws.manager

Ensure that the agent has relevant skills, availability, and access to at least one queue in the service channel.

## About this task

The active work items remain in the queue pending manual allocation for one of the following reasons:

-   The agent's capacity is exceeded to the maximum.
-   Work items may not be accepted by any available agents.
-   Agents with required skills are not available.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Click the **Channels** icon.

3.  Do any of the following to manually allocate the work items.

<table id="choicetable_pjv_3lx_ft"><thead><tr><th align="left" id="d151644e102">

Navigate To

</th><th align="left" id="d151644e105">

Do this

</th></tr></thead><tbody><tr><td id="d151644e111">

**Active Work Items tab**

</td><td>

Select the work item and click **Allocate**.

</td></tr><tr><td id="d151644e123">

**Service Channel page**

</td><td>

1.  Click a service channel. For example, Chat.
2.  Click the **Work Items** tab.
3.  Select the work item.
4.  Click **Allocate**.


</td></tr><tr><td id="d151644e153">

**All Queues tab**

</td><td>

1.  Click a queue.
2.  Click the **Work Items** tab.
3.  Select the work item.
4.  Click **Allocate**.


</td></tr></tbody>
</table>    The list of available agents appears with details such as presence state, capacity, and matching skills.

4.  Select the agent to assign the work item.

    For example, if the capacity is 0/4, it means that the agent's maximum capacity is 4 work items.

    **Note:** You can allocate a single work item at a time to the agent.

5.  Click **Allocate**.

    The work item is allocated to the selected agent. The agent gets an alert on the assigned work item.

    -   If the agent accepts the work item and the status moves from **Pending Accept** to **Accepted** state. The ​**Assigned To** field is updated​ with the agent's name.
    -   If the agent rejects the work item and the status moves to **Queued** state.
    -   If the agent does not accept the work item for a long time, with the status as **Pending Accept** and you must allocate it again.

**Parent Topic:**[Routing work items using Channels in Workforce Optimization for ITSM](../concept/configurable-channels-workforce-optimization-itsm.md)

