---
title: Run a mining job
description: Run a mining job on a Task Mining project to generate an analysis of your project data according to your categorization rules so you can make data-driven decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/task-mining/mine-project-data.html
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generating project analysis, Use, Task Mining, Platform Analytics]
---

# Run a mining job

Run a mining job on a Task Mining project to generate an analysis of your project data according to your categorization rules so you can make data-driven decisions.

## Before you begin

Analyses can only include data from users with completed data request approvals and agent installations. However, you can still mine a project with incomplete data. If any data request is pending approval, you can remove that data request from the project first. For information about adding and removing workstation users from a project, see [Add workstation users to a Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/add-users-to-task-mining-project.md).

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the name of the project you want to analyze.

    \[Omitted image "tm-mine-project.png"\] Alt text: Screenshot showing a Task Mining project before mining.

3.  Review the **Approvals and actions** section for which data request approvals were completed and which agents were installed.

    Analyses can only include data from users with completed data request approvals and agent installations. However, you can still mine a project with incomplete data.

4.  Select the Project menu icon \[Omitted image "icon-vert-3dot-p.png"\] Alt text: Context menu icon and **Workstation users** to see details of data requests affiliated with the project including the manager responsible for approving the request.

5.  Select **Mine project**.

    If this option isn’t available, check that the project timeline has started.

6.  Select the Project menu icon \[Omitted image "icon-vert-3dot-p.png"\] Alt text: Context menu icon and **Mining Jobs** to monitor the progress of your mining jobs for this project.

7.  Select a tab of an analysis you selected when creating the project.

    \[Omitted image "tm-after-mining.png"\] Alt text: Screenshot showing a project after mining.


## What to do next

Review your analysis to see whether it needs further refinement. For more information, see [Refine the presentation of your data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/preview-data-based-on-categorization-rules.md).

**Related topics**  


[Task Mining analyses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/task-mining-dashboard.md)

