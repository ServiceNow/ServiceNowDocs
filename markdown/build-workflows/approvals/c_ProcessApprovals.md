---
title: Process approvals
description: Once a request has passed its gating approvals, any relevant execution plans are initiated.
locale: en-US
release: yokohama
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Approval rules, Classic approvals, Build workflows]
---

# Process approvals

Once a request has passed its gating approvals, any relevant execution plans are initiated.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](../../flow-designer/reference/ask-approval-flow-designer.md). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

Those plans, in turn, create a sequence of required tasks. You can add an approval step to an execution plan, which is configured to occur at the appropriate point.

From the left navigation pane, select **Service Catalog** &gt; **Execution Plans**, and then select the plan to which to add an approval step. Then click the **New Approval** button.

![Add an approval](../image/AddApproval.png "Add approval")

The Approval Task screen appears. Just like a regular Service Catalog execution task, an approval execution task has:

-   **Name**: The name of this task
-   **Order**: Sequence of this task within the plan
-   **SLA**: SLA to which this task applies
-   **Delivery Time**: Time allowed for the completion of this task

After you create the task, right click the title bar and select **Save**. Two related lists appear at the bottom of the screen:

-   **Approved By Group**: A list of groups that must approve the request before this task is complete
-   **Approved By**: A list of users who must approve the request before this task is complete

![Approval task](../image/ApproveTask.png "Approval task")

In the example above, this security approval task must be approved by Fred Luddy.

**Note:** When an in-process approval is rejected, that particular line item is canceled as well, but the request itself isn't necessarily canceled. Thus if one ordered a blackberry and a laptop, and the blackberry was rejected, the laptop request would continue being processed.

