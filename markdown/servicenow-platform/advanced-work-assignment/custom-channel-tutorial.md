---
title: Tutorial: Set up a custom service channel for change requests
description: Learn how to configure Advanced Work Assignment to automatically assign change requests to agents. Use this tutorial as a guideline to help you understand how service channel records, queues, and assignment rules work together to create a custom service channel.Create a service channel in Advanced Work Assignment so that you can route change requests to agents.Create an assignment rule in Advanced Work Assignment that assigns change requests to agents who are available to do the tasks.Create a work item queue in Advanced Work Assignment that routes new change requests through the service channel that handles change requests.Create an eligible assignment pool in Advanced Work Assignment that receives overflow work items, just in case you need more help from other agents to handle change requests.Make your service channel available in Agent Workspace so that agents can receive change requests in their inbox.Customize how change requests appear in an agent inbox so that agents receive enough information to decide whether to accept or reject the work item.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Set up a custom service channel, Service channels, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Tutorial: Set up a custom service channel for change requests

Learn how to configure Advanced Work Assignment to automatically assign change requests to agents. Use this tutorial as a guideline to help you understand how service channel records, queues, and assignment rules work together to create a custom service channel.

In this tutorial, you learn how to set up a custom channel that:

-   Assigns new change requests to whichever Change Management agent has the most capacity
-   Populates the assignee's agent inbox in Agent Workspace with change requests from the queue
-   Displays the change request number, short description, and type on the inbox card
-   Enables the agent to accept or reject change requests

For information on setting up custom service channels, see [Set up a custom service channel](../task/setup-custom-channel.md).

Before you begin:

-   Ensure that the form layout for the Change Request table is configured for the workspace view; otherwise, work items from the Change Request service channel appear as read-only in Agent Workspace. For more information, see Set up forms in legacy workspace.
-   Assign the awa\_agent and workspace\_agent roles to the Change Management group so that members can open work items in Agent Workspace.

**Parent Topic:**[Set up a custom service channel](../task/setup-custom-channel.md)

## Create a service channel to route requests

Create a service channel in Advanced Work Assignment so that you can route change requests to agents.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Select **New**.

3.  On the form, fill in the fields.

    -   Name: Change Request
    -   Inbox Order: 100
    -   Table: Change Request \[change\_request\]
    -   Active: Selected
    -   Utilization condition: \[Active\] \[is\] \[true\]
4.  Select **Submit**.


## Create an assignment rule for change requests

Create an assignment rule in Advanced Work Assignment that assigns change requests to agents who are available to do the tasks.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the assignment rules settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up assignment rules**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Assignment Rules**.
2.  Select **New**.

3.  On the form, fill in the fields.

    -   Name: Change Request Assignment Rule
    -   Assign by: Most Capacity
    -   Allow agents to reject: Selected
4.  Select **Submit**.


## Create a queue to route new change requests

Create a work item queue in Advanced Work Assignment that routes new change requests through the service channel that handles change requests.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select **New**.

3.  On the form, fill in the fields.

    -   Name: Change Management
    -   Service channel: Change Request
    -   Condition mode: Simple
    -   Work item routing condition: \[State\] \[is\] \[New\]
4.  From the form context menu, select **Save**.


## Create an assignment pool of agents

Create an eligible assignment pool in Advanced Work Assignment that receives overflow work items, just in case you need more help from other agents to handle change requests.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Open the Change Management queue.

3.  On the form, go to the **Assignment Eligibility** related list and select **New**.

4.  On the form, fill in the fields.

    -   Agent assignment rule: Change Request Assignment Rule
    -   Groups: Change Management
5.  Select **Submit**.


## Make your service channel available in Agent Workspace

Make your service channel available in Agent Workspace so that agents can receive change requests in their inbox.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the presence states settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Additional settings section, select **Set up presence states**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Presence States**.
2.  Open **Available**.

3.  On the form, move **Change Request** to the **Selected** list.

4.  Select **Active** \(if not already selected\).

5.  Select **Update**.


## Customize how change requests appear in an agent inbox

Customize how change requests appear in an agent inbox so that agents receive enough information to decide whether to accept or reject the work item.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Select the **Change Request** service channel record.

3.  On the Change Request service channel form, go to the **Inbox Layouts** related list and open **Default Change Request layout**.

4.  On the form, fill in the fields.

    -   Field 1: Number
    -   Field 2: Short description
    -   Field 3: Type
5.  Click **Update**.


### Result

When you create a change request, the item is routed through the Change Request service channel and assigned to the agent in the Change Management assignment group who is available to receive the change request. When the assignee checks their agent inbox, the change request appears with the option for the agent to either reject or accept the work item.

![Change work item in agent inbox](../image/ChangeWorkItem.png "Change request in an agent inbox")

