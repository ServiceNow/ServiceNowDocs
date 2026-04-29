---
title: Workflow validation
description: Workflow validation examines different characteristics of a workflow to locate issues that might prevent the workflow from being published or cause it to fail. The validation report summarizes the results of each separate workflow validation.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow validation

Workflow validation examines different characteristics of a workflow to locate issues that might prevent the workflow from being published or cause it to fail. The validation report summarizes the results of each separate workflow validation.

Validation prevents workflows with critical flaws from executing and resulting in an unstable or incomplete state. There are a number of validators in the base system that notify workflow designers of potential problems. For example, multiple **End** activities, disconnected transitions, incorrect table references, missing subflows, and dependencies affected by update sets. A workflow validation report displays the results from each validator, including a message explaining what was found. The system automatically validates a workflow when you publish it. You can also run validation on a workflow directly from controls in the Workflow Editor.

## Highlighting critical errors

The graphical Workflow Editor highlights critical errors when a workflow is loaded. In this example, a subflow is missing and is not available to the parent workflow for the current user. The graphical Workflow Editor indicates the error when the parent workflow loads by highlighting \(in red\) the activity that calls the subflow. To correct the error in the parent workflow, click the validate icon in the header bar and inspect the error description in the validation report.

![Validate missing subflow](../image/ValidateMissingSubflow.png "Validate missing subflow")

## Validations at publishing

If you attempt to publish an invalid workflow or a workflow with potential problems, the system displays an error message and blocks the operation, if necessary. When validation error messages appear, click the validate icon in the graphical Workflow Editor to see the error report.

-   **Validation warning**

    A validation warning notifies you that a potential problem exists in a workflow but permits you to publish the workflow. Validation warnings appear when:

    -   You edit and then attempt to publish a workflow that is included as a subflow in another workflow. The system cannot determine how your changes will affect the parent workflow and alerts you of the relationship.
    -   A workflow activity uses a different table than the table assigned to the workflow. The system alerts you of the potential conflict.
    ![validation warning](../image/ValidationWarning.png "Validation warning")

-   **Validation failure**

    A validation failure notifies you that a critical error has occurred in the workflow that prevents you from publishing the workflow. An example of a critical error is a missing subflow.

    ![Validation failure](../image/ValidationFailure.png "Validation failure")


## Workflow validation report

Validators display three notification levels: CRITICAL, WARN, and INFO. The designer can publish a workflow that returns WARN or INFO level validation, but not a workflow that returns an overall validation level of CRITICAL.

![Workflow validation report](../image/WorkflowValidationReport.png "Workflow validation report")

-   **Header summary**

    The header of the validation report summarizes the entire validation run against the specified workflow.

    -   **Validate Summary:** The overall score reflects the most severe notification level encountered during the validation.
    -   **Total checks performed:** The total number of validations run is also broken down to show the number at each notification level.
-   **Report columns**

    The body of the report displays the results of each individual validation check that was performed. The columns are **Type**, **Level**, and **Message**. You can sort and filter these columns as you would any list.

    |Name|Implication|
    |----|-----------|
    |Info|Provides information about the current workflow version. An example of an information level message is one that names the lowest common table in the workflow. Workflows at this validation level are considered valid and publishable.|
    |Warning|Alerts the user that the validator detected anomalies in the workflow that might compromise its ability to execute. An example of a warning level message is one that alerts you to a missing activity input transition. Workflows at this validation level are considered valid and publishable.|
    |Critical|Names a workflow element containing a critical error that prevents the workflow from executing successfully. Examples of this are missing or invalid subflows and missing transitions. Workflows at this validation level cannot be published or run in production.|

-   **Message**

    The validation message provides a detailed description of the results, including table names, update sets, and other specifics.


For the procedure to validate a workflow and generate a validation report, see [Validate a workflow](../../workflow-administration/task/work-on-workflows.md#)

-   **[Workflow validator](../reference/r_WorkflowValidator.md)**  
ServiceNow offers several workflow validators for workflow designers to test their workflows.

**Parent Topic:**[Workflow management](../../workflow-administration/concept/managing-workflows.md)

