---
title: Change approval policies
description: In Change approval policies, approval definitions are used to generate approvals according to your business requirements.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Change Management, Change Management, IT Service Management]
---

# Change approval policies

In Change approval policies, approval definitions are used to generate approvals according to your business requirements.

A change approval policy is a course of action that can be applied to a change request. It uses a set of variable inputs to evaluate the decisions that are associated with it. For each matching decision, the associated approval definition is applied.

An approval policy can contain multiple decisions allowing a single policy to handle every approval required for a change type. When a decision condition matches, the related approval definition is evaluated. If one or more decisions match, all the related approval definitions are evaluated.

Use the **Change Approval Policy** workflow activity instead of the **User** and **Group Approval** workflow activities to manage the approvals at a particular stage of the workflow. For more information, see [Change Approval Policy workflow activity](change-approval-policiy-wf-activity.md)

**Note:** To use the change approval policies after you upgrade:

1.  Configure the approval policies as needed.
2.  Replace the **User** and **Group Approval** activities with the **Change Approval Policy** activity in the workflow.

A change approval policy consists of three components:

-   **Policy inputs**: The variable sources evaluated within the condition defined on a decision.
-   **Decisions**: Based on the conditions, determines whether the associated Change approval definition applies.
-   **Approval definitions**: Defines the type of approval that can applied.

**Parent Topic:**[Exploring Change Management](exploring-change-management.md)

