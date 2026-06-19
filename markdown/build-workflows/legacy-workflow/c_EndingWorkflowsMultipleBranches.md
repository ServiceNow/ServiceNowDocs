---
title: Ending workflows with multiple branches
description: A workflow is complete when it reaches the End activity, even if there are still active branches of the workflow in progress. To ensure that both branches are completed, add a Join activity to resolve the branches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/legacy-workflow/c\_EndingWorkflowsMultipleBranches.html
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

\[Omitted image "WorkflowMultipleBranchesProblematic.png"\] Alt text:

For both branches to complete, add a **Join** activity to resolve the branches. When one branch reaches the join, the workflow waits for the other branch. When both branches are complete, the workflow reaches the end. The **Incomplete** condition of the a **Join** activity is met only if one of the branches cannot be completed.

\[Omitted image "WorkflowMultipleBranchesJoined.png"\] Alt text:

**Parent Topic:**[Create a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/t_CreateAWorkflow.md)

