---
title: CSM Configurable Workspace components
description: Content pages in CSM Configurable Workspace, such as record pages, are made up of reusable components that display information or enable agents to complete tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace components

Content pages in CSM Configurable Workspace, such as record pages, are made up of reusable components that display information or enable agents to complete tasks.

## Action bar

The action bar contains the actions available to agents while working on case records. This includes buttons on the action bar and menu items in the More Actions menu. Each record page contains a set of actions that have been configured for that specific page.

The action bar can also contain action groups which combine multiple actions in the same button. For example, the [Front-line case page](csm-front-line-case-page.md) includes the [Create action group](csm-config-ws-action-layout-groups.md) which displays a drop-down list with the available actions.

Typical actions available in the action bar include:

-   **Create**: Create records such as work orders, incidents, and requests.
-   **Manage case**: Perform case management actions such as accepting a case or requesting information.
-   **Save**: Save changes to the case record.
-   **Follow**: Receive notifications when comments or work notes are added to the record. When selected, the button toggles to **Unfollow**.
-   **More Actions**: Perform additional actions such as proposing a major case or reporting a knowledge gap.

**Note:** The specific actions available are determined by factors such as the user role, case state, and other attributes.

## Task SLA cards component

The Task SLA cards component displays the status of one or more Service Level Agreements \(SLAs\) for the current record in card format. The Task SLA cards component can display multiple SLAs. The cards are displayed in a carousel with horizontal navigation. If more than one SLA card is present, agents can use arrows to scroll through the cards. For more information, see [Task SLA cards component](csm-record-page-sla-card-component.md).

## Task activity timeline controller and preset

The timeline uses icons to display record events and colors to show ranges of time, such as when a case is with the agent or the customer. Agents can use the timeline in the following ways:

-   Zoom in and out.
-   Select the **Show details** toggle to display more information.
-   Hover over the icons to show tool tips.

For more information, see [Task activity timeline preset and controller](csm-record-page-timeline-component.md).

