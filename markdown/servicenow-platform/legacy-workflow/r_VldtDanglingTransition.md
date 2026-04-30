---
title: ValidateDanglingTransition
description: The ValidateDanglingTransition validator finds and reports any transitions that do not terminate on an activity.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateDanglingTransition

The **ValidateDanglingTransition** validator finds and reports any transitions that do not terminate on an activity.

**Note:** These transitions are not drawn on the workflow canvas, but are still present in the database.

**Warning:** This is a critical error that prevents a workflow from running.

## Validation summary

-   Risk: A workflow with dangling transitions will silently hang a workflow with no recovery options.
-   Severity Level: Critical
-   Valid Result: Valid
-   Valid Message: Valid
-   Invalid Result: Invalid
-   Invalid Message: Invalid
-   Suggested Action: Remove or connect the offending transition. Get the source activity name from the validation report details and resolve the issue. Then, run the validation again to test your changes.
-   Publishable: No
-   Runnable: No
-   Related Information: None

## Troubleshooting

On rare occasions, the destination of a workflow transition becomes null. The workflow canvas shows no evidence of the transition, but at run time, the workflow hangs when it encounters one of these dangling transitions. If the **ValidateDanglingTransition** validator reports this condition at publishing time, it blocks the publication action until the issue is resolved. If this condition is detected on a runtime check, the workflow is not allowed to execute against a current record's transaction. Instead, the system adds a critical log entry detailing the activity with the faulted transition to the current record's workflow context. To enable the workflow to execute on the next appropriate transaction, remove the faulted transition from the workflow model.

To find and remove the faulted transition:

1.  Make note of the workflow version and activity that contains the faulted transition as indicated in the validator details.
2.  Navigate to **Workflow** &gt; **Administration** &gt; **Workflow Version**.
3.  In the list of workflow versions, select the workflow that has the faulted transition.
4.  On Workflow Version form, add the workflow activities related list. Click the menu icon, select **Configure &gt; Related Lists**, move **Workflow Activity--&gt;Workflow Version** from the **Available** list to the **Selected** list, and click **Save**.
5.  In the **Workflow Activities** related list, select the activity cited in the validator.
6.  In the Workflow Activity form, view the **Workflow Transitions** section or tab and identify the transition in that list that has no value or a null value in the **To** column.
7.  Delete this transition.
8.  Return to the workflow version and re-run the validation check.

The **Critical** warning should disappear. The workflow should execute as expected on the next appropriate transaction.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

