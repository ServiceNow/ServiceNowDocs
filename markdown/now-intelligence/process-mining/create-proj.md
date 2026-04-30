---
title: Create a project using Classic view
description: Configure and manage the project status and outline of the process you want to analyze.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Process Mining, Process Mining, Platform Analytics]
---

# Create a project using Classic view

Configure and manage the project status and outline of the process you want to analyze.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

You must enable [Audit Log](https://www.servicenow.com/docs/access?context=t_EnableAuditingForATable&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for the table that you’ve selected to generate a model for a project.

## About this task

Configure a project definition that displays visualized, interactive routes of flows of process information.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Projects** &gt; **All projects**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see [Project definition form](../reference/new-project-def.md).

4.  Select **Save**.

    The project definition record is created.


-   **[Set up a table configuration](po-table-configuration.md)**  
Define the kind of data or process that you want to view and analyse in your graph. You must select a specific table \(parent table\) that has the data that you want to analyse.
-   **[Configure an activity definition](configure-activity.md)**  
Report on steps that occur within your business process.
-   **[Configure a breakdown definition](configure-breakdown.md)**  
Add a breakdown to filter records and analyze a process map by categories.
-   **[Configuring improvement opportunities](../concept/configuring-finding-definitions.md)**  
Configure an improvement opportunities to view the insights on the Summary and insights page.
-   **[Import improvement opportunities](import-finding-definitions.md)**  
Import improvement opportunities as templates into the project associated with the table. Improvement opportunities from the parent table that are in Active state are available for import. If you don’t import the improvement opportunities from the process table, the improvement opportunities aren’t used during project mining.
-   **[Mine a project](generate-process-map.md#)**  
After you’ve configured the data you want to visualize, you can begin mining the project.
-   **[Schedule a Process Mining job](../reference/schedule-mining-job.md)**  
Schedule a Process Mining job to mine one or more projects later.
-   **[Edit a project](edit-project.md#)**  
Edit a project from the Project Definition form to generate an updated process map.
-   **[Delete a project](delete-project-navigator.md)**  
Delete a project if you are not using it and want to clean up data. Deleting a project deletes the project's configurations and versions or projects it has generated. You can delete a project from the Process Mining Workspace.

**Parent Topic:**[Using Process Mining](../concept/use-process-mining.md)

