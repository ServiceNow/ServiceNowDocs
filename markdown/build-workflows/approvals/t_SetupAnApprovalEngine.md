---
title: Set up an approval engine
description: To manage the approvals for each of the Task tables in the system, set up an approval engine.
locale: en-US
release: yokohama
product: Approvals
classification: approvals
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Approval engines, Classic approvals, Build workflows]
---

# Set up an approval engine

To manage the approvals for each of the Task tables in the system, set up an approval engine.

## Before you begin

Role required: none

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](../../flow-designer/reference/ask-approval-flow-designer.md). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Approval Engines**.

    The following page appears with the **Approval Engine** option for each Task table in the system. If the **Approval Engine** option is greyed out and shows **Turn engines off**, read the **Notes** in the same row. The most common reason an approval engine is turned off is that a workflow is managing the approvals on the table. Having the approval engine turned off prevents conflicts with the workflow that could cause a range of issues. If you want to use an approval engine on the table, set the workflow to inactive.

    ![Approval engine page](../image/ApprovalEnginePage.png)

2.  Select the [approval engine option](../concept/c_ApprovalEngines.md#table_ApprovalEngineOptions) for each Task table from the choice list.

3.  Click **Save**.

    These preferences are saved as system properties that are named **glide.approval\_engine.&lt;table\_name&gt;**.


