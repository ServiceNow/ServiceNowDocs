---
title: Workflow validator
description: ServiceNow offers several workflow validators for workflow designers to test their workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/legacy-workflow/r\_WorkflowValidator.html
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow validator

ServiceNow offers several workflow validators for workflow designers to test their workflows.

This page lists all available workflow validators. See [Workflow validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_WorkflowValidation.md) for information on using workflow validators and the workflow validation report to see the type of information that is returned.

|Hanging Workflows|Update Sets|
|-----------------|-----------|
|Identify workflow design decisions that can result in a hanging workflow|Identify related artifacts being moved in different update sets|
|[ValidateTransitionOut](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtTransitionOut.md)|[ValidateUpdateSetDependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtUpdtStDpnd.md)|
|[ValidateTransitionIn](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_ValidateTransitionIn.md)|[ValidateUpdateSetParentDependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtUpdtStPtDpnd.md)|
|[ValidateDanglingTransition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtDanglingTransition.md)|[ValidateInputVarUpdateSetDependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtInptVrUpdtStDpd.md)|
|[ValidateSubflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_ValidateSubflows.md)| |
|[ValidateScriptForCurrentDotUpdate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_VldtScptCurrentDotUpdate.md)| |

|Unexpected Workflow Termination|External Dependencies|
|-------------------------------|---------------------|
|Identify workflows that can end unexpectedly|Identify external artifacts that have potential workflow dependencies|
|[ValidateSingleEnd](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_ValidateSingleEnd.md)|[ValidateParentFlow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_ValidateParentFlow.md)|

|Workflow Properties Conflicts|
|-----------------------------|
|Identify workflow design decisions that conflict with workflow properties|
|[ValidateLowestCommonTable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtLowestCommonTable.md)|
|[ValidateTableChange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtTableChange.md)|

-   **[ValidateTransitionOut](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtTransitionOut.md)**  
The **ValidateTransitionOut** validator finds activity conditions with no exit transitions.
-   **[ValidateTransitionIn](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_ValidateTransitionIn.md)**  
The **ValidateTransitionIn** validator finds activities that do not have inbound transitions and cannot execute in the workflow.
-   **[ValidateDanglingTransition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtDanglingTransition.md)**  
The **ValidateDanglingTransition** validator finds and reports any transitions that do not terminate on an activity.
-   **[ValidateSubflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_ValidateSubflows.md)**  
The **ValidateSubflows** validator detects any workflows included as subflows that are either inactive, deleted, or not available as a published workflow for the current user.
-   **[ValidateScriptForCurrentDotUpdate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_VldtScptCurrentDotUpdate.md)**  
The **ValidateScriptForCurrentDotUpdate** validator finds workflow activities with scripts that use the current.update\(\) function.
-   **[ValidateLowestCommonTable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtLowestCommonTable.md)**  
The **ValidateLowestCommonTable** validator reports the lowest table in the Glide hierarchy that the workflow uses.
-   **[ValidateTableChange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtTableChange.md)**  
The **ValidateTableChange** validator reports any activities in the workflow that are invalid given the table associated with the workflow version.
-   **[ValidateParentFlow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_ValidateParentFlow.md)**  
The **ValidateParentFlow** validator reports any workflows that use the workflow as a subflow.
-   **[ValidateSingleEnd](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_ValidateSingleEnd.md)**  
The **ValidateSingleEnd** validator finds and identifies multiple **End** activities in a single workflow.
-   **[ValidateUpdateSetDependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtUpdtStDpnd.md)**  
The **ValidateUpdateSetDependencies** validator identifies all the subflows called in the current workflow and determines if any of those subflows are being edited in a different \(in progress\) update set.
-   **[ValidateUpdateSetParentDependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtUpdtStPtDpnd.md)**  
The **ValidateUpdateSetParentDependencies** validator identifies all the workflows that call the current workflow as a subflow and determines if any of those parent workflows are being edited in a different update set that is in progress.
-   **[ValidateInputVarUpdateSetDependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtInptVrUpdtStDpd.md)**  
The **ValidateInputVarUpdateSetDependencies** validator examines update sets to ensure that workflow input variables for a given workflow have not been deleted in different update sets than those currently **In progress**.
-   **[ValidateWorkflowEndStages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtWorkflowEndStages.md)**  
The **ValidateWorkflowEndStages** validator checks that in workflows with stages, the end activity of the workflow has a stage named Complete or Completed.
-   **[ValidateWorkflowStageColumn](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtWkflwStageColumn.md)**  
The **ValidateWorkflowStageColumn** validator detects and reports when the stage field \(stage column\) for a workflow is not correct or is unusable.
-   **[ValidateWorkflowStateValues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/r_VldtWorkflowStateValues.md)**  
The **ValidateWorkflowStateValues** validator checks a number of stage aspects in workflow activities for correctness.

**Parent Topic:**[Workflow validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_WorkflowValidation.md)

