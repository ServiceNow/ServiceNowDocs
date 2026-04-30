---
title: Service Operations Workspace for ITSM user interface
description: You can navigate through the Service Operations Workspace to get an overview of how an agent can prioritize tasks and provide resolution.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Explore, Service Operations Workspace for ITSM, IT Service Management]
---

# Service Operations Workspace for ITSM user interface

You can navigate through the Service Operations Workspace to get an overview of how an agent can prioritize tasks and provide resolution.

## Accessing Service Operations Workspace

From the **Workspaces** menu, select **Service Operations Workspace**.

## Landing page

From the **Workspaces** menu, select **Service Operations Workspace** and click the home icon \(![Home icon](../image/sow-home.png)\).

An agent can analyze assignments and view announcements and upcoming tasks. Tier-1 agents can also analyze the performance and view the assigned courses. For information about the landing page, see [Service Operations Workspace for ITSM landing page](sow-ui-landing-page.md).

## Lists

From the **Workspaces** menu, select **Service Operations Workspace** and click the list icon \(![List icon](../../itsm-manager-workspace/image/lists_icon.png)\).

An agent can analyze the individual lists of incidents, catalog tasks, requests, problem, and so on, and take appropriate action.

From the **My Lists** tab, an agent can create a separate list or a different version of the existing list. For information about creating a list, see [Create a list in Service Operations Workspace](../task/create-list-sow.md).

![List tab](../image/list-tab-sow.png "List tab")

## Record view

Open any task record to navigate to its record view.

![Record view](../image/record-view.png "Record view")

## Inbox

Agents can set the status to Available or Away to open or close the inbox for chat requests. When a requester initiates a chat conversation from any Service Portal page, the chat interaction appears in the inbox of all agents who are configured as group members for Agent Chat Queue. For information about inbox configuration, see [Configure the inbox in Service Operations Workspace](../task/configure-inbox-in-sow.md).

The following scenarios are possible for assignment of chat conversation to an agent.

-   When the automatic assignment of chat conversations is enabled, the chat conversation is automatically assigned to the agent, an interaction record is created in Service Operations Workspace, and the agent can continue the chat conversation. Based on options selected in the Chat - Most Capacity assignment rule, the interactions can open as non-active tabs in the inbox. For information on enabling automatic assignment of chat conversations using this assignment rule, see [Enable automatic assignment of interactions to an agent](../task/enable-automatic-assignment-interaction.md).
-   When the automatic assignment of chat conversations is not enabled, the agent can then approve or reject the chat conversation. When the agent accepts the chat conversation, an interaction record is created in Service Operations Workspace and the agent can continue the chat conversation.

When the requester in Service Portal or the agent in Service Operations Workspace ends the chat conversation, the interaction is closed.

![Inbox](../image/inbox-sow.png "Inbox")

-   **[Service Operations Workspace for ITSM landing page](sow-ui-landing-page.md)**  
An agent can get quick visibility into the work assigned, view announcements, and view upcoming tasks.

**Parent Topic:**[Exploring Service Operations Workspace for ITSM](explore-sow.md)

**Related topics**  


[Exploring Recommended Actions for ITSM in Service Operations Workspace](exploring-recommended-actions-for-itsm-in-service-operations-workspace.md)

[Exploring Password Reset](exploring-password-reset-sow.md)

