---
title: Run a mining job
description: Run a mining job on a Task Mining project to generate an analysis of your project data according to your categorization rules so you can make data-driven decisions.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Generating project analysis, Use, Task Mining, Platform Analytics]
---

# Run a mining job

Run a mining job on a Task Mining project to generate an analysis of your project data according to your categorization rules so you can make data-driven decisions.

## Before you begin

Analyses can only include data from users with completed data request approvals and agent installations. However, you can still mine a project with incomplete data. If any data request is pending approval, you can remove that data request from the project first. For information about adding and removing workstation users from a project, see [Add workstation users to a Task Mining project](add-users-to-task-mining-project.md).

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the name of the project you want to analyze.

    ![Screenshot showing a Task Mining project before mining.](../image/tm-mine-project.png)

3.  Review the **Approvals and actions** section for which data request approvals were completed and which agents were installed.

    Analyses can only include data from users with completed data request approvals and agent installations. However, you can still mine a project with incomplete data.

4.  Select the Project menu icon ![Context menu icon](../../../use/dashboards/image/icon-vert-3dot-p.png) and **Workstation users** to see details of data requests affiliated with the project including the manager responsible for approving the request.

5.  Select **Mine project**.

    If this option isn’t available, check that the project timeline has started.

6.  Select the Project menu icon ![Context menu icon](../../../use/dashboards/image/icon-vert-3dot-p.png) and **Mining Jobs** to monitor the progress of your mining jobs for this project.

7.  Select a tab of an analysis you selected when creating the project.

    ![Screenshot showing a project after mining.](../image/tm-after-mining.png)


## What to do next

Review your analysis to see whether it needs further refinement. For more information, see [Refine the presentation of your data](preview-data-based-on-categorization-rules.md).

**Related topics**  


[Task Mining analyses](../concept/task-mining-dashboard.md)

