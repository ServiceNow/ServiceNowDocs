---
title: Ending workflows with multiple branches
description: A workflow is complete when it reaches the End activity, even if there are still active branches of the workflow in progress. To ensure that both branches are completed, add a Join activity to resolve the branches.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a workflow, Workflow management, Classic Workflow, Build workflows]
---

# Ending workflows with multiple branches

A workflow is complete when it reaches the **End** activity, even if there are still active branches of the workflow in progress. To ensure that both branches are completed, add a **Join** activity to resolve the branches.

For example, the following figure shows a workflow with two branches that execute independently. When Task 1 and Task 2 of Branch B are completed, the workflow is marked complete even if the Branch A tasks are not completed.

![](../image/WorkflowMultipleBranchesProblematic.png "Workflow with uncompleted branch")

For both branches to complete, add a **Join** activity to resolve the branches. When one branch reaches the join, the workflow waits for the other branch. When both branches are complete, the workflow reaches the end. The **Incomplete** condition of the a **Join** activity is met only if one of the branches cannot be completed.

![](../image/WorkflowMultipleBranchesJoined.png "Workflow with completed branches")

**Parent Topic:**[Create a workflow](../task/t_CreateAWorkflow.md)

