---
title: Work items
description: Work items are plans stored as local files in your Lux Lab project. Each one contains a structured description for you and your AI agents of what needs to be built or fixed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/work-items.html
release: zurich
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Work items, Work items and plan mode, Work item access, Work item creation, Work item storage]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Work items

Work items are plans stored as local files in your Lux Lab project. Each one contains a structured description for you and your AI agents of what needs to be built or fixed.

## Work items and plan mode

Work items act as a lightweight task-tracking system tied directly to your project. Lux Lab creates a work item when you or the agent work in plan mode. When you ask the agent to plan a task before implementing it, Lux Lab saves the resulting plan as a work item file.

Work items have the following characteristics:

-   They're stored as files in your local project.
-   They're tied to a specific project, and each work item records which project it belongs to.
-   AI agents can execute or iterate on them, using the plan as their guiding context.
-   They're visible and manageable from within the app.

## Work item access

You can open work items from the Activity Bar or from the Explorer sidebar.

-   **Activity Bar**

    Select the **Work Items** icon in the Activity Bar to open the dedicated Work Items panel. The panel lists all work items associated with the current project.

-   **Sidebar**

    A **Work Items** accordion is pinned at the bottom of the left sidebar, below the file tree. Expanding it shows all active work items for the project without leaving the Explorer view.


## Work item creation

You create work items through the Agent Chat Harness, using plan mode. The agent produces a structured plan from your requirements, and you save that plan as a work item. You agree on an explicit plan before the agent makes any code changes.

For the steps, see [Create a work item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-work-item.md).

## Work item storage

Work items are stored as files within your project directory. Because they're project-local files, they have the following properties:

-   They're tied to the project they were created for.
-   They're portable, so you can commit them to source control and teammates can see the planned work.
-   They're readable by agents. When an agent starts working on a project, it can reference existing work item files as context.

