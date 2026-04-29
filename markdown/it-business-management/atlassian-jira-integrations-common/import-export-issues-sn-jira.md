---
title: Import issues from a Jira project to Agile Development 2.0
description: Import available issues from a Jira project, with or without the team integration settings for this project, so that you can update existing records of Jira from Agile Development 2.0.
locale: en-US
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Importing issues and sprints from Jira to Agile Development 2.0, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Strategic Portfolio Management]
---

# Import issues from a Jira project to Agile Development 2.0

Import available issues from a Jira project, with or without the team integration settings for this project, so that you can update existing records of Jira from Agile Development 2.0.

## Before you begin

-   [Discover and import Jira projects and boards](discover-projects.md)
-   Role required: sn\_jira\_int.user

## About this task

If your Jira project has team integration settings, then the imported issues are assigned to an assignment group according to the team integration settings. If your Jira project does not have team integration settings, then the imported issues are not associated to any assignment group.

**Note:** This task does not explain importing sprints. For information on how to import sprints from Jira, see [Import sprints from Jira to Agile Development 2.0](import-sprints-to-agile-2-from-jira-board.md).

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  From the Jira Projects related list, open the project from which you want to import the issues.

4.  Enable the import and export of issues by selecting the **Enable Import** and **Enable Export** options as applicable.

    Synchronisation of multi-select fields between Agile and Jira is now supported.

5.  Click **Import Issues**.

6.  Select a date range from which you want to import the issues from Jira.

7.  Click **Submit**.

    An import request of type Import Issues is created in the Jira Import Requests related list. Once the state of this request changes to Completed, you can view all the imported records in the Epics and Stories modules in Agile Development 2.0. The relationship between the stories and epics is retained as it is in Jira.

    **Note:** Existing comments and attachments of issues are not imported from Jira during a bulk import.


**Parent Topic:**[Importing issues and sprints from Jira to Agile Development 2.0](../concept/importing-issues-and-sprints-from-jira-to-agile-dev-2.0.md)

