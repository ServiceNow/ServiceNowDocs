---
title: Workflow validator
description: ServiceNow offers several workflow validators for workflow designers to test their workflows.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# Workflow validator

ServiceNow offers several workflow validators for workflow designers to test their workflows.

This page lists all available workflow validators. See [Workflow validation](../concept/c_WorkflowValidation.md) for information on using workflow validators and the workflow validation report to see the type of information that is returned.

|Hanging Workflows|Update Sets|
|-----------------|-----------|
|Identify workflow design decisions that can result in a hanging workflow|Identify related artifacts being moved in different update sets|
|[ValidateTransitionOut](r_VldtTransitionOut.md)|[ValidateUpdateSetDependencies](r_VldtUpdtStDpnd.md)|
|[ValidateTransitionIn](../concept/c_ValidateTransitionIn.md)|[ValidateUpdateSetParentDependencies](r_VldtUpdtStPtDpnd.md)|
|[ValidateDanglingTransition](r_VldtDanglingTransition.md)|[ValidateInputVarUpdateSetDependencies](r_VldtInptVrUpdtStDpd.md)|
|[ValidateSubflows](r_ValidateSubflows.md)| |
|[ValidateScriptForCurrentDotUpdate](../concept/c_VldtScptCurrentDotUpdate.md)| |

|Unexpected Workflow Termination|External Dependencies|
|-------------------------------|---------------------|
|Identify workflows that can end unexpectedly|Identify external artifacts that have potential workflow dependencies|
|[ValidateSingleEnd](r_ValidateSingleEnd.md)|[ValidateParentFlow](../concept/c_ValidateParentFlow.md)|

|Workflow Properties Conflicts|
|-----------------------------|
|Identify workflow design decisions that conflict with workflow properties|
|[ValidateLowestCommonTable](r_VldtLowestCommonTable.md)|
|[ValidateTableChange](r_VldtTableChange.md)|

-   **[ValidateTransitionOut](r_VldtTransitionOut.md)**  
The **ValidateTransitionOut** validator finds activity conditions with no exit transitions.
-   **[ValidateTransitionIn](../concept/c_ValidateTransitionIn.md)**  
The **ValidateTransitionIn** validator finds activities that do not have inbound transitions and cannot execute in the workflow.
-   **[ValidateDanglingTransition](r_VldtDanglingTransition.md)**  
The **ValidateDanglingTransition** validator finds and reports any transitions that do not terminate on an activity.
-   **[ValidateSubflows](r_ValidateSubflows.md)**  
The **ValidateSubflows** validator detects any workflows included as subflows that are either inactive, deleted, or not available as a published workflow for the current user.
-   **[ValidateScriptForCurrentDotUpdate](../concept/c_VldtScptCurrentDotUpdate.md)**  
The **ValidateScriptForCurrentDotUpdate** validator finds workflow activities with scripts that use the current.update\(\) function.
-   **[ValidateLowestCommonTable](r_VldtLowestCommonTable.md)**  
The **ValidateLowestCommonTable** validator reports the lowest table in the Glide hierarchy that the workflow uses.
-   **[ValidateTableChange](r_VldtTableChange.md)**  
The **ValidateTableChange** validator reports any activities in the workflow that are invalid given the table associated with the workflow version.
-   **[ValidateParentFlow](../concept/c_ValidateParentFlow.md)**  
The **ValidateParentFlow** validator reports any workflows that use the workflow as a subflow.
-   **[ValidateSingleEnd](r_ValidateSingleEnd.md)**  
The **ValidateSingleEnd** validator finds and identifies multiple **End** activities in a single workflow.
-   **[ValidateUpdateSetDependencies](r_VldtUpdtStDpnd.md)**  
The **ValidateUpdateSetDependencies** validator identifies all the subflows called in the current workflow and determines if any of those subflows are being edited in a different \(in progress\) update set.
-   **[ValidateUpdateSetParentDependencies](r_VldtUpdtStPtDpnd.md)**  
The **ValidateUpdateSetParentDependencies** validator identifies all the workflows that call the current workflow as a subflow and determines if any of those parent workflows are being edited in a different update set that is in progress.
-   **[ValidateInputVarUpdateSetDependencies](r_VldtInptVrUpdtStDpd.md)**  
The **ValidateInputVarUpdateSetDependencies** validator examines update sets to ensure that workflow input variables for a given workflow have not been deleted in different update sets than those currently **In progress**.
-   **[ValidateWorkflowEndStages](r_VldtWorkflowEndStages.md)**  
The **ValidateWorkflowEndStages** validator checks that in workflows with stages, the end activity of the workflow has a stage named Complete or Completed.
-   **[ValidateWorkflowStageColumn](r_VldtWkflwStageColumn.md)**  
The **ValidateWorkflowStageColumn** validator detects and reports when the stage field \(stage column\) for a workflow is not correct or is unusable.
-   **[ValidateWorkflowStateValues](r_VldtWorkflowStateValues.md)**  
The **ValidateWorkflowStateValues** validator checks a number of stage aspects in workflow activities for correctness.

**Parent Topic:**[Workflow validation](../concept/c_WorkflowValidation.md)

