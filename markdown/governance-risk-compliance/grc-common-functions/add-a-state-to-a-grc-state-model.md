---
title: Add a state to a GRC state model
description: Add a state to a GRC state model and configure its stepper display, transitions, and attributes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/add-a-state-to-a-grc-state-model.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Add a state to a GRC state model

Add a state to a GRC state model and configure its stepper display, transitions, and attributes.

## Before you begin

The GRC state model must exist. See [Create a GRC state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-a-grc-state-model.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Each state can be configured with its own stepper display, transitions, and attributes.

## Procedure

1.  Open the state model.

2.  In the **GRC Workflow States** related list, add each state that records can move through, and specify a sequence number to control the display order.

3.  Open a state.

4.  Configure the stepper display fields.

    |Field|Description|
    |-----|-----------|
    |**Display type**|Controls whether the state appears as a node or sub-level in the stepper component.|
    |**Stepper label**|The label displayed for the state in the stepper component.|
    |**Parent node**|The parent state for the current state. Applies only when **Display type** is set to **As sub-level**.|
    |**Is optional**|Indicates whether the state can be skipped.|

5.  On the **Model State Transitions** tab, add transitions to other states.

6.  If the transition should occur without user action, select **Automatic transition**.

7.  On the **State Model Attributes** tab, select **Edit**.

8.  In the **Collection** list, select the attributes that apply to the state, and move them to the **State Model Attributes** list.

    **Note:**

    A terminal state typically includes either the Default closed state or Default cancelled state attribute. For example, in the Core workflow state model, Closed Complete includes the Terminal state and Default closed state attributes. Closed Incomplete includes the Terminal state and Default cancelled state attributes. See [State model attributes for the Issue table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/state-model-attributes-for-the-issue-table.md).

9.  Select **Save**.

10. Repeat [3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-a-state-to-a-grc-state-model.md) through [9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-a-state-to-a-grc-state-model.md) for each additional state that you want to include in the state model.


## Result

The state model is saved with its states, transitions, and attributes. You can select the state model when adding components to an issue workflow.

-   **[State model attributes for the Issue table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/state-model-attributes-for-the-issue-table.md)**  
Attributes available for states in a GRC state model applied to the Issue table.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

**Related topics**  


[Add the layout, state model, and playbook to a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.md)

[Map states to playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/map-states-to-playbook-stages.md)

