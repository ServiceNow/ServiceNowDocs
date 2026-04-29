---
title: Set use cases
description: Use cases are common patterns that you may be interested in your analysis. Once enabled, they’re automatically configured for the project.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Use, Process Mining, Platform Analytics]
---

# Set use cases

Use cases are common patterns that you may be interested in your analysis. Once enabled, they’re automatically configured for the project.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

4.  Select **Use cases** from the left bar.

    **Tip:** Select **Advanced view** on the top-right corner if you want to edit the project in the Classic view.

5.  Select the **Include approvals** option if you want to view details of any approvals present for the process.

    The Approval \[sysapproval\_approver\] table is attached as a child entity to the parent table of your project. The filter conditions, activities, and breakdowns are already selected for ease of you. You can review and edit any of those according to your requirement.

    **Note:** If you have projects from any version prior to Xanadu with the **Include approvals** option selected, those mined projects are made obsolete. The project is automatically updated to the current change. You must remine the project to view the results.

6.  Select the **Include SLA breach** option if you want to view where there’s a breach in the process.

    The Task SLA \[task\_sla\] table is attached as a child entity to the parent table of your project. The filter conditions, activities, and breakdowns are already selected for ease of you. You can review and edit any of those according to your requirement.

7.  Select the **Include child tables for analysis** option if you want to add a related table to your parent table.

    This field is available only if you have specified the Child tables section of the Process details page in the process configuration. For more information, see [Configure process details](process-details.md).

    Child tables include data of dependent subprocesses that are important for the execution of the parent process. Analyzing child tables helps uncover inefficiencies in subprocesses that impact the main process's performance.

    For example, the Incident table serves as the parent table with general information about incidents, while the Incident Task is the child table that stores specific tasks related to each incident.

    **Note:** After setting the child table, you must configure the activity definitions and any other setting in the **Add a child entity** tab.

8.  Select **Save**.


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

