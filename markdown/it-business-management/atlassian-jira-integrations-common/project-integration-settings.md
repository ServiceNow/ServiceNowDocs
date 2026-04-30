---
title: Associate a Jira project and board with an assignment group in Agile Development 2.0
description: Associate your Jira projects and boards with assignment groups in Agile Development 2.0 to enable import and export of all available issues between the associated project and assignment group.
locale: en-US
release: zurich
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing issues and sprints from Jira to Agile Development 2.0, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Associate a Jira project and board with an assignment group in Agile Development 2.0

Associate your Jira projects and boards with assignment groups in Agile Development 2.0 to enable import and export of all available issues between the associated project and assignment group.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md).
-   Create assignment groups in Agile Development 2.0. See [Create an assignment group in Agile Development 2.0](../../agile-development/task/create-an-agile-group.md#).
-   Ensure that your Jira project has a defined mapping configuration.
-   Role required: sn\_jira\_int.user

## About this task

Create team integration settings to associate a Jira project and Jira board with an Agile 2.0 assignment group.

**Important:** You can associate an assignment group with only one project and board from Jira.

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Team Integration Settings**.

2.  Click **New**.

3.  On the Team Integration Settings form, select the following:

    -   A Jira project
    -   A Jira board
    -   An assignment group in Agile Development 2.0 to which you want to associate the selected Jira project and board
    Selecting a Jira board in the form is optional. If you do not want to synchronize the sprint data of the board between Agile Development 2.0 and Jira, you can skip selecting a Jira board.

    **Note:** If your Jira project is of Kanban type, you can leave the **Jira board** field empty. All issues of your Kanban project will be mapped to a single Agile 2.0 group.

4.  Click **Submit**.


## What to do next

You can import or issues from this Jira project or sprints from this Jira board to the associated assignment group.

**Parent Topic:**[Importing issues and sprints from Jira to Agile Development 2.0](../concept/importing-issues-and-sprints-from-jira-to-agile-dev-2.0.md)

**Related topics**  


[Import issues from a Jira project to Agile Development 2.0](import-export-issues-sn-jira.md)

[Import sprints from Jira to Agile Development 2.0](import-sprints-to-agile-2-from-jira-board.md)

