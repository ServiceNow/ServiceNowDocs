---
title: Input variable movement
description: You can add input variables to existing workflows and add them to update sets.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Input variable movement

You can add input variables to existing workflows and add them to update sets.

When you submit the new variables, an entry is made into the current update set that reflects the addition of a variable to the Variables \[var\_dictionary\] table. Unlike the workflow version that only writes to the update set when the workflow is published, the variables write individual update entries into the currently selected update set immediately upon submission.

-   **[Input variable movement use case - two input variables](../reference/r_InptVrblMvmntTwo.md#)**  
An existing workflow already contains two input variables.
-   **[Input variable removal](c_InputVariableRemoval.md#)**  
Deleting workflow input variables, like insert and update actions, creates a customer update record in a user's current update set.
-   **[Avoiding duplicate workflows](c_AvoidingDuplicateWorkflows.md#)**  
Update sets manage the published state of all versions of a workflow prior to committing the workflow version on a local instance.

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

