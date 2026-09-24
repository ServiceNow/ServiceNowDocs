---
title: My tasks page
description: The My tasks page displays a single pane view of your pending tasks, tasks assigned to your user group, and the tasks that are on your watchlist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/my-tasks-page-uib-ws.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [BCM Configurable Workspace, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# My tasks page

The **My tasks** page displays a single pane view of your pending tasks, tasks assigned to your user group, and the tasks that are on your watchlist.

## Tabs in the Tasks page

The **Tasks** page displays the assigned tasks for the logged-in user in different tabs.

\[Omitted image "my-grp-pending-tasks.png"\] Alt text: My tasks page.

The **Tasks** page in BCM Configurable Workspace displays these tabs:

-   **My pending tasks**: Displays an overview of the pending tasks that are assigned to you and the tasks that require an action. Filter pending tasks with the states:

    -   All
    -   Draft/New
    -   In progress
    -   Needs my approval
    -   Needs my review
    -   Overdue
    -   Pending response
-   **My items**: Displays a list of the tasks that are assigned to the logged-in user.

-   **My group's pending tasks** and **My group's items** tabs: Display a list of the tasks assigned to the group. Any group member who is part of the assigned owner group can see these details. These tabs are separate from **My pending tasks** and **My items**, which show the tasks assigned to you.

    Starting with BCM core version 12.x.x, you can assign group ownership to BIA, plan, and event records. These group-owned records are displayed in the **My group's pending tasks** and **My group's items** tabs on the **My tasks** page.

-   **Watchlist**: Displays a list of the tasks for which you are on the watchlist. When a task is approved or completed, you receive a notification on the **Watchlist** tab.

The data displayed in the **Tasks** page is based on the roles of the users.

For information on assigning group ownership to BIA, plan, and event records, see [Create a business impact analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-bia-in-uib-ws.md), [Create a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-bcp-plan-in-uib-ws.md), and [Create an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/start-exercise-event-in-uib-ws.md).

For more information on the **My tasks page configuration** module in the application, see [My tasks page configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/my-tasks-page-config-module.md).

**Note:** You can view the records that are in-progress on the **My tasks** page. The closed and canceled records are not displayed on these tabs. You can view the closed and canceled records in their respective forms in BCM Configurable Workspace.

If you have the BCM administrator role, you can customize BCM Configurable Workspace by updating the **My tasks page configuration** module. To do so, navigate to **All** &gt; **General Administration** &gt; **My tasks page configuration** in your instance.

If you have the BCM manager or BCM user roles, you can receive recommendations on your business continuity tasks on the **Home** page.

To view more information on the **My tasks page configuration** module, see [Update the Tasks Page Configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/view-tasks-page-configurations.md).

