---
title: ValidateTransitionIn
description: The ValidateTransitionIn validator finds activities that do not have inbound transitions and cannot execute in the workflow.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateTransitionIn

The **ValidateTransitionIn** validator finds activities that do not have inbound transitions and cannot execute in the workflow.

## Validation summary

-   **Risk:**Activities that do not have inbound transitions have no means of being executed in the workflow. If other logic builds from these activities, the workflow could hang, with no means of moving forward.
-   **Purpose:** Find activities that do not have inbound transitions.
-   **Severity Level:** Warning.
-   **Valid Result:**Valid.
-   **Valid Message:** All activities in this workflow have at least one inbound transition.
-   **Invalid Result:** Invalid.
-   **Invalid Message:**This workflow contains &lt;activity count&gt; activity conditions without an input transition.
-   **Suggested Action:**Either remove the activities to reduce confusion and make the workflow easier to understand or provide the appropriate inbound transition.
-   **Publishable:**Yes
-   **Runnable:**Yes
-   **Related Information:**None

## Troubleshooting

Although the activities detected in this validator do no harm to the execution of the workflow, the designer needs to know that there are activities on the canvas that cannot execute and serve no purpose, particularly in a production system. This error is typically caused by a visual misinterpretation of the drawing.

This example workflow appears to be perfectly valid. Under closer inspection, however, we see that the transition from **Set Values** does not stop at **Approval - User** \(there is no arrow end\). Instead, that transition goes directly to **End**. As a result, **Approval - User** cannot execute. Because there is an activity in the workflow based on the approval's condition routing, it appears that the designer intended for the approval to execute and that a correction is needed.

![](../image/TransitionInInvalid.png "TransitionIn invalid")

This validator directs the designer to the specific activity and condition that has no inbound transition. The designer should establish a transition or remove the activity.

**Parent Topic:**[Workflow validator](../reference/r_WorkflowValidator.md)

