---
title: ValidateWorkflowStateValues
description: The ValidateWorkflowStateValues validator checks a number of stage aspects in workflow activities for correctness.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateWorkflowStateValues

The **ValidateWorkflowStateValues** validator checks a number of stage aspects in workflow activities for correctness.

This validator has multiple possible error messages.

## Validation summary

-   Risk: The stage indicators may not display appropriate information.
-   Severity Level: Warning.
-   Valid Result: Valid.
-   Valid Message: Workflow stage values are valid.
-   Invalid Result: invalid.
-   Warning summary: Stage warnings found.
-   Invalid Messages:
    -   Stage with empty name is not allowed.
    -   Stage with empty value is not allowed.
    -   Cannot have more than one stage with the same name: x.
    -   Cannot have more than one stage with the same value: y
-   Suggested Action: If this is not by design, make the appropriate changes.
-   Publishable: Yes.
-   Runnable: Yes
-   Related Information: [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md).

## Troubleshooting

Use the following procedure to troubleshoot this validator:

1.  Open and check out a workflow.
2.  Open the list of stages for the workflow by selecting the menu icon and selecting **Edit Stages**.
3.  Check the names and values.

    Ensure that the names and values are unique and are not empty.

4.  If the same stage name or value apprears more than once, remove one of the rows. It is then very important to go through the workflow and reassign stages in the activities that used the removed stage.

    ![Workflow Stages record showing the Request Cancelled and Closed Incomplete stage names with a value of closed_complete.](../image/ValidateWorkflowStateValues.png "Validate Workflow Stage Values")


Tip: Make a list of which activities assign which stages.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

