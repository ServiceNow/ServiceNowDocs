---
title: Tutorial: Set up a custom service channel for change requests
description: Learn how to configure Advanced Work Assignment to automatically assign change requests to agents. Use this tutorial as a guideline to help you understand how service channel records, queues, and assignment rules work together to create a custom service channel.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a custom service channel, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
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

-   Ensure that the form layout for the Change Request table is configured for the workspace view; otherwise, work items from the Change Request service channel appear as read-only in Agent Workspace.
-   Assign the awa\_agent and workspace\_agent roles to the Change Management group so that members can open work items in Agent Workspace.

