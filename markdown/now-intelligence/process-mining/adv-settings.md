---
title: Set use cases
description: Use cases are common patterns you may be interested in your analysis. Once enabled, they are automatically configured for the project.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set use cases

Use cases are common patterns you may be interested in your analysis. Once enabled, they are automatically configured for the project.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

4.  Select **Use cases** from the left bar.

    **Tip:** Select **Advanced view** on the top right corner if you want to edit the project in the Classic view.

5.  Select the **Include approvals** option if you want to view details of any approvals present for the process.

    The sysapproval\_approver table is attached as a child entity to the parent table of your project. The filter conditions, activities, and breakdowns are already selected for ease of you. You can review and edit any of those as per your requirement.

    **Note:** If you have a project from previous releases with **Include approvals** option selected, those mined projects are made obsolete. The project will be automatically updated to the current change. You must remine the project to view the results.

6.  Select the **Include SLA breach** option if you want to view where there is a breach in the process.

    The task\_sla table is attached as a child entity to the parent table of your project. The filter conditions, activities, and breakdowns are already selected for ease of you. You can review and edit any of those as per your requirement.

7.  Select **Save**.


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

