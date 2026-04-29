---
title: ValidateParentFlow
description: The ValidateParentFlow validator reports any workflows that use the workflow as a subflow.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# ValidateParentFlow

The **ValidateParentFlow** validator reports any workflows that use the workflow as a subflow.

## Validation summary

-   **Risk:** There is no risk in a workflow being a subflow. This is only a warning that other workflows are at risk from dramatic changes to a subflow.
-   **Severity Level:**Warning
-   **Valid Result:** Valid
-   **Valid Message:** Currently &lt;workflow version name&gt; is not a subflow.
-   **Invalid Result:** None
-   **Warning Message:**This workflow version \(&lt;workflow version name&gt;\) is required as a subflow in &lt;workflow version count&gt; other workflows.
-   **Suggested Action:** Exercise caution when modifying things like input parameters and return values to assure that parent workflows are not adversely affected.
-   **Publishable:** Yes
-   **Runnable:**Yes
-   **Related Information:** [Workflows used as subflows](../../workflow-activities/reference/workflows-as-subflows.md)

## Troubleshooting

The system warns the workflow designer at publishing time and during validation that a workflow is a subflow. This warning reminds the designer that changes to the current workflow have the potential to affect workflows cited in the validation report or other workflows already running in production. Regardless of how simple the change to a workflow that is a subflow, thoroughly test all parent flows cited in this validation report before publication.

When a workflow is a subflow, changes that can cause it to become invalid include:

-   Changing the data types of [input variables](../../using-workflows/concept/c_UsingVariablesInAWorkflow.md#). Verify that all parent workflows cited in this validation report can pass the correct value type.
-   Adding input variables. Verify that all parent workflows cited in this validation report are able to pass all variable values into the subflow.
-   Changing or removing the return value of a workflow. Verify that any changes to the return value of a workflow are compatible with the requirements of all the parent flows.
-   Changing the table on which the workflow runs. Verify that the table selection is compatible with all parent flows.

**Note:** To delete a workflow that is a subflow, first remove the dependency by removing the subflow from all parent flows cited in this validation report. After the dependencies are cleared, a user with the proper role can delete the subflow.

**Parent Topic:**[Workflow validator](../reference/r_WorkflowValidator.md)

