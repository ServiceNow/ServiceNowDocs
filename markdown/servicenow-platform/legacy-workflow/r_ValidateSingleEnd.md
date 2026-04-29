---
title: ValidateSingleEnd
description: The ValidateSingleEnd validator finds and identifies multiple End activities in a single workflow.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateSingleEnd

The **ValidateSingleEnd** validator finds and identifies multiple **End** activities in a single workflow.

Multiple **End** activities in a workflow might be intentional and have no affect on the workflow, or might be a mistake that the designer needs to correct.

## Validation summary

-   Risk: If the execution paths to the **End** activities are not mutually exclusive, then the first **End** encountered completes the workflow and cancels all other executing activities.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message: This workflow contains 1 End activity.
-   Invalid Result: Invalid Activity
-   Invalid Message: This workflow contains &lt;count of ends&gt; End activities.
-   Suggested Action: Remove extraneous **End** activities that are not intended as part of the design.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: None

## Troubleshooting

As soon as an **End** activity is encountered in the workflow, the workflow completes even if there are other viable execution paths leading to a second **End** activity that is still executing. Those executing activities are canceled as part of the **End** activity's clean up actions. Therefore, the results of designing workflows with multiple **Ends** must be carefully considered.

In the case of large workflows, it is often more intuitive to read the workflow when there are multiple **End** activities. In the following example, the paths to the two **Ends** are mutually exclusive execution paths. If this was a large workflow, with many activities between **Branch** and the second **End**, the value of the multiple ends becomes apparent. Tracing a **No** response from **User is invalid** to a single **End** behind 33 other activities would be significantly more difficult. There is no risk in this workflow design because there is no reason for other activities to execute if the **End** after the **Notification** activity terminates the workflow.

![](../image/TwoEndExampleValid.png "Mutually exclusive execution paths")

The next example has multiple **End** activities in execution paths that are not mutually exclusive. A **Yes** response from **User is valid** causes the **Set Values** activity to finish immediately. By reaching its **End** activity first, this execution path cancels the **Approval for Apps** and the **DB Task** activities, which might not be the desired outcome. If the paths are all expected to complete before **End**, the activities should come to a **Join** \(as in the previous example\) that transitions to a single **End**.

![](../image/TwoEndExampleInValid.png "Mutually inexclusive execution paths")

**Note:** To add the second **End**, right-click to copy the original **End** activity and paste it onto the canvas. In most cases, a single **End** is the best and most reliable way to ensure that all activities expected to execute prior to workflow completion, do so successfully.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

