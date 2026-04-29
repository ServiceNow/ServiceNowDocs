---
title: Collaborate component
description: Use the Collaborate component in CSM Configurable Workspace to communicate with stakeholders and gather information for case resolution.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Components, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Collaborate component

Use the Collaborate component in CSM Configurable Workspace to communicate with stakeholders and gather information for case resolution.

![The collaboration component displays the available configured services when an agent initiates a new conversation.](../image/csm-config-ws-collaboration-component.png "Collaborate component with multiple configured communication services")

Customer service agents can use the Collaborate component to initiate chats and calls with other agents, requestors, and subject matter experts.

The Collaborate component requires configured integrations with communication services such as Microsoft Teams, Slack, and Zoom. When no integrations have been configured, agents can use the Collaborate component to start Sidebar discussions.

The Collaborate component is available as the last tab in the contextual side panel in CSM Configurable Workspace. The Collaborate component is available on all CSM Configurable Workspace [record pages](csm-config-ws-pages-templates.md) where the table is set to one of the following:

-   Interaction \[interaction\]
-   A child of the Task \[task\] table, such as the Case table \[sn\_customerservice\_case\]

Users with the sn\_uib\_collab.user role can see the Collaborate component on workspace pages. This role is included with the interaction\_agent role, which is included with the sn\_esm\_agent role.

## Collaborate component features

The Collaborate component includes two tabs: Chat and Calls. These tabs show the active and completed chats and calls in card format.

**Note:** When no integrations have been configured, the Collaborate component displays the Chat tab and includes the **Start Sidebar discussion** option. Agents can select this option to start a Sidebar discussion.

The component also includes the following:

-   An Add \(**+**\) icon that agents can use to initiate new chats and calls. The selections available in this menu depend on the configured integrations, such as Microsoft Teams and Zoom.
-   Search bar: use to quickly find a chat or call.
-   Filter icon: use to filter and sort the conversations.

## Collaborate component integrations

The Collaborate component requires configured integrations with communication services such as Microsoft Teams, Slack, and Zoom. For more information, see [Collaboration services](https://www.servicenow.com/docs/access?context=collab-services-tcm&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

The Collaborate component includes the Sidebar feature. Agents can collaborate with others through Sidebar discussions. For more information, see the following topics:

-   [Exploring Sidebar](https://www.servicenow.com/docs/access?context=exploring-sidebar&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)
-   [Sidebar and Microsoft Teams](https://www.servicenow.com/docs/access?context=sidebar-teams-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)
-   [Using Sidebar](https://www.servicenow.com/docs/access?context=using-sidebar&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

The Collaborate component can also be configured to use different communication tools such as Microsoft Teams or Zoom. Agents can see the available configurations by selecting the Add icon.

## Collaborate component extension points

Customers can implement the following extension points to customize conditions for visibility of the Call and Chat tabs in the Collaborate component:

-   sn\_uib\_notify.NotifyUIBVisibility
-   sn\_uib\_collab.ContextualPanelVisibility

