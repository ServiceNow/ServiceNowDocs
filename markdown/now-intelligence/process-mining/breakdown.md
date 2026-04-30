---
title: Set breakdown definitions
description: Set the breakdown definitions that act as filters for your project. Breakdown definitions are used to filter and analyze the data based on specific criteria or attributes. These definitions enable you to break down the analysis into smaller subsets, focusing on specific dimensions or perspectives of the process.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set breakdown definitions

Set the breakdown definitions that act as filters for your project. Breakdown definitions are used to filter and analyze the data based on specific criteria or attributes. These definitions enable you to break down the analysis into smaller subsets, focusing on specific dimensions or perspectives of the process.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

-   [Create a project or template using Project Builder](define-workflow-model.md)

## About this task

This is an optional task.

**Note:** You can configure a maximum of 10 breakdown definitions for the parent table configuration and 5 breakdown definitions for any child table configuration. You can’t generate more than 20,000 breakdown values for all the breakdown definitions for the parent table and 5000 breakdown values for all the breakdown definitions of each child table.

This is an optional task.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project that you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

4.  Select **Breakdowns** from the left bar.

    **Tip:** Select **Advanced view** on the top right corner if you want to edit the project in the Classic view.

5.  Select **New** in the Breakdowns area.

    ![Breakdown](../image/breakdown.png)

6.  Select any breakdown from the list or the recommendations.

    These recommendations come from the process configuration set for the table on which the project is based. They are derived from the Breakdown fields section of the Process details page in the Process Configuration Builder. For more information, see [Configure process details](process-details.md).

    If no value is set in the Process Configuration Builder, then no recommendation is provided.

7.  Select **Save**.

    The breakdown is added to the project.

8.  Select a breakdown to edit it.

    ![Edit breakdown](../image/breakdown-edit.png)

    You can add a display name and a filter condition to the breakdown.

9.  Select **Select Improvement opportunities**.

    If you want to add or edit anything in the **Scope your analysis** page, select **Previous**.


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

