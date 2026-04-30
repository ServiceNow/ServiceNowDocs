---
title: Configure parameters displayed on project cards in classic Project Workspace
description: Configure the parameters that are displayed on a project card in My Projects Space page of classic Project Workspace. A card shows the project summary so that project managers can quickly gauge project status and health by looking at the card.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Project workspace classic - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure parameters displayed on project cards in classic Project Workspace

Configure the parameters that are displayed on a project card in **My Projects Space** page of classic Project Workspace. A card shows the project summary so that project managers can quickly gauge project status and health by looking at the card.

**Important:**

Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use new Project Workspace with enhanced UI to help you efficiently manage your projects.

## Before you begin

Role required: it\_pps\_admin

## About this task

The project workspace overview page **My Projects Space** displays the projects as cards based on the filter criteria. The cards have a color band at the top. The color of the band is based on the **Status** field in the respective project record. Each card further displays the following information about the project in three rows:

-   Row 1 displays project name, state, project manager name, and important project dates. The displayed project dates are based on the current state of the project:
    -   If the project state is Pending or Open, planned start date and planned end date are displayed.
    -   If the project state is Work in Progress, actual start date and planned end date are displayed.
    -   If the project state is Closed, actual start date and actual end date are displayed.
-   Row 2 displays Status, Percent complete, and Phase columns from project \[pm\_project\] table. The number of displayed columns in this row is fixed to 3, but the columns to be displayed can be configured in \[pm\_home\_page\_config\] table.
-   Row 3 displays the following project information based on the current state of the project.

    -   Open risks, open issues, actions, and overdue tasks of the project under **Updates** heading.
    -   Date and short description of the last missed milestone task under **Last missed milestone** heading.
    The parameters displayed are derived from the records in \[pm\_home\_page\_card\] table. In \[pm\_home\_page\_card\] table, each project state is assigned some parameters to be displayed.


![Project card in project workspace.](../image/ProjectWorkspaceCard.png "Project card example")

You can configure the information which is displayed in row 2 and row3 on a card.

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Project Workspace**.

2.  Select a table for which you want to change the card configuration, for example, select `Project[pm_project]`.

3.  Set the display columns for row 2 of the card in PM Home Page Configuration \[pm\_home\_page\_config\] table.

    1.  Select the columns to be displayed in **Column-1**, **Column-2**, and **Column-3** fields.

    2.  Click **Update**.

    The selected columns appear in row 2 of the project cards.

4.  Set the parameters for row 3 of the card in PM Home Page Card \[pm\_home\_page\_card\] table.

    In \[pm\_home\_page\_card\] table, each project state is assigned the parameters that are required to be displayed on a project card in third row.

    1.  Click **New** in **PM Home Page Card** related list.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Order|Position at which the parameter appears in row 3 of the card.|
        |State|Project state for which the parameter needs to be added.|
        |Value|Section to be displayed for the selected state in row 3 such as **Updates** and **Last missed milestone**.|
        |Content|JSON field to add the parameters to be displayed under the selected section for the selected state.|

        The following screenshot shows a JSON example of adding Risks, Issues, Actions, and Overdue tasks parameters under **Updates** heading for Open state.

        ![Example project card configuration](../image/ProjectWorkspaceCardConfiguration.png "Example JSON for Row 3 configuration")

    3.  Click **Submit**.

        **Note:** Use the same steps to change a display parameter assigned to a state.

    The parameter is added or updated for the selected state. It appears under selected section in row 3 on the project cards for the state it was added.


**Parent Topic:**[Project workspace classic - Legacy](../concept/project-workspace-classic.md)

