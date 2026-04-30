---
title: Importing issues and sprints from Jira to Agile Development 2.0
description: Understand the process of importing existing issues and sprints from Jira to Agile Development 2.0.
locale: en-US
release: zurich
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Importing issues and sprints from Jira to Agile Development 2.0

Understand the process of importing existing issues and sprints from Jira to Agile Development 2.0.

You can import existing issues from Jira projects as stories and epics, and existing sprint data from Jira boards as sprints to Agile Development 2.0. After importing the available data, any updates that you make to the epic, story, or sprint records will be synchronized automatically in both Jira and Agile Development 2.0.

## Importing issues

From version 2.0.1, you can proceed to import issues from a Jira project directly after discovering projects from Jira. You do not have to create team integration settings. However, the imported issues are not associated to any assignment group in Agile Development 2.0. You can manually assign these issues to an assignment group later.

If you want your imported issues to be assigned to an assignment group automatically, you can create team integration settings for your Jira project by associating it to an Agile 2.0 assignment group and then proceed to import the issues. This setting ensures that any imported issues that belong to a Jira project are assigned to its associated assignment group.

## Importing sprints

Importing sprint data from Jira boards require that the board has team integration settings that associate it to an Agile 2.0 assignment group. Sprint data of a Jira board is imported to its assignment group, only if these sprints have already started in Jira. Also, only the completed and current sprints of Jira are imported.

## Team integration settings

From version 2.0.1, the Project Integration Settings module is available as Team Integration Settings. Team integration settings help you associate Jira projects and boards with Agile 2.0 assignment groups to facilitate the bidirectional synchronization of record updates.

Associating a Jira project to an assignment group allows the following:

-   Enable import and export of all available stories and epics between this project and its associated group.
-   View any new stories and epics or updates made to the existing stories and epics in both Agile Development 2.0 and Jira.

Associating a Jira board to an assignment group allows the following:

-   Import all completed and current sprints from this board into the associated group.
-   View any completed and current sprints or updates made to them in both Agile Development 2.0 and Jira.

To understand the workflow of the import and export of issues between Agile Development 2.0 and Jira, see [Importing and exporting issues between Agile Development 2.0 and Jira](../reference/import-export-issues-sn-jira-workflow.md).

-   **[Associate a Jira project and board with an assignment group in Agile Development 2.0](../task/project-integration-settings.md)**  
Associate your Jira projects and boards with assignment groups in Agile Development 2.0 to enable import and export of all available issues between the associated project and assignment group.
-   **[Import issues from a Jira project to Agile Development 2.0](../task/import-export-issues-sn-jira.md)**  
Import available issues from a Jira project, with or without the team integration settings for this project, so that you can update existing records of Jira from Agile Development 2.0.
-   **[Import sprints from Jira to Agile Development 2.0](../task/import-sprints-to-agile-2-from-jira-board.md)**  
Import sprints from a Jira board so that you can track progress of these sprints directly in Agile Development 2.0.

**Parent Topic:**[Setting up the integration between Jira and Agile Development 2.0](../task/setting-up-the-integration-between-jira-and-agile-development.md)

