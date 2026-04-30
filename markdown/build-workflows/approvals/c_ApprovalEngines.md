---
title: Approval engines
description: The differences in the way that companies handle their approvals, as well as the differences between approvals for the various applications \(such as Service Catalog Requests and Change Management\), calls for supporting flexibility in setting up approvals within applications.
locale: en-US
release: xanadu
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Build workflows]
---

# Approval engines

The differences in the way that companies handle their approvals, as well as the differences between approvals for the various applications \(such as Service Catalog Requests and Change Management\), calls for supporting flexibility in setting up approvals within applications.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](../../flow-designer/reference/ask-approval-flow-designer.md). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

This flexibility is provided through the selection of an ''approval engine'' that is used to manage the approvals for each of the Task tables \(that is, all tables that extend the Task table\).

There are three different approval engine options available for each Task table.

<table id="table_ApprovalEngineOptions"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval Rules

</td><td>

A simple set of rules that are evaluated until one matches for the Task table. The matching approval rule is used to create the users that are to approve the task. Set up approval rules by navigating to **System Policy** &gt; **Approvals**.

</td></tr><tr><td>

Process Guides

</td><td>

A sequence of approval steps over which you may control how approvals and rejections are handled. This option is deprecated and should not be used.

</td></tr><tr><td>

Turn off Engines

</td><td>

Turn off both approval engines for this Task table. This option should be selected and is made read-only when a workflow is used to manage the approval process for the table. **Note:** Not turning off the approval engines might have a performance or behavioral impact on your instance.

</td></tr></tbody>
</table>