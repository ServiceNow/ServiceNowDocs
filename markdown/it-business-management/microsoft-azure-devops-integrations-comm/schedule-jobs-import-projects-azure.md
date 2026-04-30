---
title: Schedule jobs to import projects, teams, areas, and work items from Azure DevOps
description: Schedule jobs to automatically import new projects, teams, areas, work items, and sprints periodically from Azure DevOps into Agile Development 2.0.
locale: en-US
release: zurich
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Schedule jobs to import projects, teams, areas, and work items from Azure DevOps

Schedule jobs to automatically import new projects, teams, areas, work items, and sprints periodically from Azure DevOps into Agile Development 2.0.

## Before you begin

Role required: admin

## About this task

If you do not configure the scheduled job, you must manually discover projects and import areas and teams.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open one of the following jobs:

    -   Discover Azure Project Job
    -   Import Azure DevOps Teams Areas and Iterations
    -   Import Azure DevOps Work Items
    These jobs are inactive by default.

3.  To execute the job manually, click **Execute Now**.

4.  To run the job at a scheduled time, select the Active check box.

    You can edit the details of the **Run** and **Time** fields according to your preference.

5.  Click **Update**.

6.  Repeat the procedure for the other two scheduled jobs.


**Parent Topic:**[Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0](../concept/setting-up-agile-azure-integration.md)

