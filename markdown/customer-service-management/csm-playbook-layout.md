---
title: Playbook layout and features
description: A playbook includes several features that agents use to complete activities and resolve cases, including the playbook stage picker, activity picker, and activity viewer. Record pages created in UI Builder determine how these playbook features are displayed in CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Playbook layout and features

A playbook includes several features that agents use to complete activities and resolve cases, including the playbook stage picker, activity picker, and activity viewer. Record pages created in UI Builder determine how these playbook features are displayed in CSM Configurable Workspace.

UI Builder [page templates](csm-playbook-templates.md) and [record pages](csm-playbook-pages.md) that include horizontally and vertically oriented playbooks are available with the Playbooks for Customer Service Management application \[com.sn\_csm\_playbook\].

For more information about using these record pages, see the following topics:

-   [Case playbook: horizontal stages](csm-playbook-horizontal-stages.md) record page
-   [Case playbook: vertical stages](csm-playbook-vertical-stages.md) record page

![Playbook with horizontal stage picker and playbook features highlighted. Descriptions of each feature are included in the following table.](../image/csm-playbook-horiz-stages-callouts.png "Playbook with horizontal stage picker")

<table id="table_j4r_cww_5pb"><thead><tr><th>

Callout

</th><th>

Playbook feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Playbook name

</td><td>

The name of the playbook appears in the page header.

</td></tr><tr><td>

2

</td><td>

Stage picker

</td><td>

Playbooks include either a horizontal or vertical stage picker, which gives the agent a complete view of the playbook and where they are within the playbook.-   The horizontal stage picker displays the playbook stages across the top of the record page below the page header. Select a stage to see the activities in the activity picker.
-   The vertical stage picker displays the playbook stages and activities on the side of the record page. Select a stage to expand the stage and display the included activities.

</td></tr><tr><td>

3

</td><td>

Activity picker

</td><td>

The activity picker displays the activities for the current stage. Each activity has an indicator that shows the activity state:-   Completed
-   In progress
-   Remaining

With the horizontal stage picker, you can expand or collapse the list of activities for the current stage.

With the vertical stage picker, you can expand each stage to see the activities within that stage.

Selecting an activity displays the details in the activity viewer.

</td></tr><tr><td>

4

</td><td>

Activity viewer

</td><td>

The activity viewer displays the selected activity. This is the main work area where an agent performs the work necessary to complete the current activity.

</td></tr><tr><td>

5

</td><td>

Activity cards

</td><td>

Activity cards display the details about the current activity in the activity viewer. Depending on the type of activity, the activity cards can display information such as form data, task status, SLA timers, or attachments.Agents use the cards to complete the work for each activity, such as filling in forms, completing checklists, completing tasks, or adding attachments.

</td></tr></tbody>
</table>## Playbook activity view

The activity view determines how the stages and activities are displayed in the playbook.

-   **Focused**: Displays the stages and activities in the playbook lifecycle panel and the current activity in the playbook work area.
-   **Stacked**: Displays the stages in the playbook lifecycle panel and cards for each of the activities in the current stage in the playbook work area.

The system administrator can configure the playbook activity view in UI Builder. For more information, see [Select a playbook activity view](../task/playbook-select-activity-view.md).

## Playbook stages

Playbooks contain one or more stages and stages contain one or more activities. The current stage in a playbook is highlighted and the activities in that stage appear in the activity picker.

The stages in the stage picker include icons that indicate the stage status:

-   A check mark ![Check mark image.](../../../reuse/icons/product-icons/circle-check-outline-24.svg) indicates that the stage is complete.
-   A pen icon ![Pen image.](../image/icon-pencil-ac.png) indicates the current stage.
-   A lock icon ![Lock image.](../image/lock-icon.png) indicates that a stage is locked and can’t be started until the previous stage is complete.

There are two versions of stage picker: horizontal and vertical.

-   The horizontal stage picker displays across the top of the UI and shows persistent information in the left panel. With the horizontal stage picker, you can expand or collapse the list of activities for the current stage.
-   The vertical stage picker displays in the left panel. With the vertical stage picker, you can expand each stage to see the activities within that stage.

## Playbook activities

Activities are the individual tasks that an agent needs to complete in order to complete a playbook stage. The activity picker displays the activities for the current playbook stage. Each activity in the activity picker has an indicator that shows the activity state:

-   Complete \(![circle icon with green check mark symbol](../image/icon-circle-green-check.png)\)
-   In Progress \(![purple filled circle icon with white pencil symbol](../image/icon-circle-filled--purple-pencil.png)\)
-   Pending \(![circle icon with purple lock symbol](../image/icon-circle-purple-lock.png)\)
-   Skipped

Selecting an activity displays the details of that activity in the activity viewer.

## Navigating playbook stages and activities

Agents can use the stage picker and activity picker to navigate between stages and activities as assigned roles or activity security configurations permit. For example, activities such as case tasks can be assigned to different users. A user with the case task agent role can only see the case tasks that are assigned to them.

When an agent opens a record that uses a playbook, it opens to the current stage and highlights the current activity. For stages with multiple activities, the current activity is the first available activity. An available activity is an activity that has a state other than Complete.

When an agent selects an available activity, it becomes the current activity. An agent can navigate stages and activities in any order as long as there is at least one available activity to select.

**Note:** The playbook configuration determines the visibility and accessibility of pending stages and activities. For more information, see [Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md).

## Using keyboard navigation in a playbook

Use the following keyboard keys to navigate playbook stages and activities.

-   **Tab** key: Use the **Tab** key to initiate navigation and move between stages, activities, and the playbook work area.
-   **Arrow** keys: Use the left, right, up, and down arrow keys to navigate the fields on a playbook activity card.
-   **Enter** key: Press the **Enter** key to select buttons on a playbook activity card.

## Filtering playbook activities

Agents can filter playbook activities and see those activities that match the filter conditions.

-   To filter playbook activities, select the filter icon \(![playbook header filter icon.](../image/playbook-filter.png)\) and select one or more of the following states:
    -   Complete
    -   In Progress
    -   Pending
    -   Skipped
-   To clear the filter, select the filter icon again and remove the selections.

## Configuring stage and activity visibility

Users with the admin role can configure the visibility of playbook stages and activities, including:

-   Showing or hiding stages and activities that are pending.
-   Showing or hiding stages and activities where a user does not have access.

The administrator configures these settings in the Playbook Experience record. For more information, see [Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md).

