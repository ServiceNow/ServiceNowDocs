---
title: ValidateTransitionOut
description: The ValidateTransitionOut validator finds activity conditions with no exit transitions.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# ValidateTransitionOut

The **ValidateTransitionOut** validator finds activity conditions with no exit transitions.

## Validation summary

-   Risk: Activity conditions might not transition to the next activity, which could cause the workflow to hang.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message: All conditions have transitions.
-   Invalid Result: Invalid
-   Invalid Message: This workflow contains &lt;condition count&gt; activity conditions without an output transition.
-   Suggested Action: If this is a conscious design decision, there is no corrective action. Otherwise, find the condition cited in the validator and add an appropriate transition to the next activity.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: None

## Troubleshooting

Design choices made when creating a workflow on the canvas might legitimately use an activity without an exit condition. In the first example, the **Notification** and **Timer** activities both execute at the start of the workflow. The **Timer** is the entity that decides when the workflow ends. In this situation, executing the **Notification**, but not transitioning away, keeps the design simple and adds no risk. The validator finds and reports the missing transition from the **Notification** activity as a **Warning** that the designer can ignore.

![](../image/ConditionOutValid.png "Condition with no valid transition")

In the second example, the **Notification** activity has no exit transition. The designer missed this because of the layout. The transition from the **Timer** activity passes behind the **Notification** activity and appears to connect the exit from the **Notification** activity to the **End**. In workflows with more than 10 or 15 activities, it might be difficult to see all the transitions clearly. This workflow's designer intended for the **Notification** activity to transition to the **End**.

![](../image/ConditionOutInvalid.png "No condition out")

This validator directs the designer to the specific activity and condition that does not have an exit transition. The designer then makes the decision whether or not to respond to the warning.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

