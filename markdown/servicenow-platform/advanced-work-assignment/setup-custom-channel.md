---
title: Set up a custom service channel
description: Set up a custom service channel to expand the type and scope of work that is routed automatically to your agents.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service channels, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up a custom service channel

Set up a custom service channel to expand the type and scope of work that is routed automatically to your agents.

## Before you begin

-   Select the table that you want to use to route work to agents automatically. Only Task \[task\] and Interaction \[interaction\] tables are supported.
-   Ensure that the form layout for the selected table is configured for the workspace view. Record types without a workspace view appear as read-only in Agent Workspace. For more information, see Set up forms in legacy workspace.
-   If you want to open a record in AWA for a table that extends another table that has a service channel defined, ensure that the workspace view for that table has already been defined.
-   Assign the awa\_agent and workspace\_agent roles to whichever agents are receiving work items in Agent Workspace from your custom service channel.

Role required: awa\_admin or admin

## About this task

You can create a service channel record from the Service Channel module, but you must create a work item queue, assignment rule, and eligible assignment pool to route work through the service channel. You also must configure the custom service channel to make it available in an agent's inbox in Agent Workspace.

## Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Select **New**.

3.  Complete the service channel fields, and then select **Submit**.

    For more information, see [Create or configure a service channel](awa-create-service-channel.md).

4.  Create an assignment rule.

    For more information, see [Configure agent assignment rules](awa-create-assignment-rule.md).

5.  Create a work item queue for your service channel.

    For more information, see [Create a work item queue](awa-create-queue.md).

6.  On the form for the work item queue that you created, go to the **Assignment Eligibility** related link and create an eligible assignment pool.

    Make sure to associate your assignment rule to the eligible assignment pool.

    For more information, see [Define agent pools eligible for assignment](awa-specify-assignment-eligibility.md).

7.  Make your service channel available in Agent Workspace.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home**.

    2.  In the Additional settings section, select **Set up presence states**, and then open **Available**.

    3.  On the form, move your custom service channel to the **Selected** list.

    4.  Select **Active** option \(if not already selected\).

    5.  Select **Update**.

8.  Create or change the inbox card layout to show the most important information from a work item.

    For more information, see [Create or change an inbox layout](awa-modify-inbox-layout.md).


## Result

Your custom service channel routes work to agents. In Agent Workspace, the service channel appears as an available service channel in the agent inbox.

-   **[Tutorial: Set up a custom service channel for change requests](../concept/custom-channel-tutorial.md#)**  
Learn how to configure Advanced Work Assignment to automatically assign change requests to agents. Use this tutorial as a guideline to help you understand how service channel records, queues, and assignment rules work together to create a custom service channel.

**Parent Topic:**[Service channels](../concept/awa-service-channels.md)

