---
title: Import work items from Azure DevOps to Agile Development 2.0
description: Import work items and iterations of an Azure DevOps project into Agile Development to track and update the status of your work.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Import work items from Azure DevOps to Agile Development 2.0

Import work items and iterations of an Azure DevOps project into Agile Development to track and update the status of your work.

## Before you begin

-   Set up team integration settings for your Azure DevOps projects. For more information, see [Associate Azure DevOps projects with assignment groups in Agile Development 2.0](set-up-import-export-azure-agile.md#).
-   Role required: sn\_ado\_int.user

## Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  From the Azure DevOps Projects related list, open a project record.

4.  Enable import and export of work items by selecting the **Enable Workitems Import** and **Enable Workitems Export** options.

5.  Enable synchronization of sprint data by selecting the **Sync Sprints** option.

6.  Click **Import Work Items**.

7.  Select a date and time range.

8.  Click **Submit**.

    **Note:** The bulk import action doesn’t import the **Description** and **Acceptance criteria** fields. However, if there’s an update on these records in Azure DevOps after the import is done, these fields are synced in Agile through webhook events.

    Details of your import requests are available in the Azure DevOps Import Requests related list.

    You can view all the imported work items and sprints in the Agile Development application.

    -   The relationship between the stories and epics stays as it is in Azure DevOps.

        The **Assigned to** field of the story is set to the user based on the user's email address, which must be unique per user account.

    -   The mapping of states of an iteration in Azure DevOps to sprints in Agile Development is as follows:

        |State in Azure DevOps|State in Agile Development 2.0|
        |---------------------|------------------------------|
        |Past|Completed|
        |Future|Draft|
        |Current|Current|

    -   Sprints are not created in Agile Development 2.0 for the following conditions:
        -   If the date fields of the iteration in Azure DevOps are empty.
        -   If the iteration has a child iteration associated to it.
        -   If the sprints have overlapping dates.
    -   If two or more teams share a backlog iteration in Azure DevOps, a separate sprint record for each team is created in Agile Development 2.0.

## What to do next

[Schedule jobs to import projects, teams, areas, and work items from Azure DevOps](schedule-jobs-import-projects-azure.md)

.

**Parent Topic:**[Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0](../concept/setting-up-agile-azure-integration.md)

