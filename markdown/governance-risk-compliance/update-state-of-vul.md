---
title: Update the state of the Operational vulnerability
description: Update the state of the Operational vulnerability record to the Assessment or Treatment state. At this stage, the vulnerability is being evaluated to determine the best course of action and create an action task accordingly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/update-state-of-vul.html
release: australia
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Update the state of the Operational vulnerability

Update the state of the Operational vulnerability record to the **Assessment** or **Treatment** state. At this stage, the vulnerability is being evaluated to determine the best course of action and create an action task accordingly.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Open the vulnerability record from the list.

    The Operational vulnerability record is in the **New** state.

    \[Omitted image "op-vul-new-state.png"\] Alt text: New state.

3.  Select **Update state** UI action.

    The **New** state can be transitioned to the following states as shown in the example:

    -   **Assessment**
    -   **Treatment**
    -   **Pending approval**
    -   **Approved**
    -   **Closed**
    -   **Canceled**
    \[Omitted image "new-state-transition.png"\] Alt text: State transition for New state.

    For more information on the state transition model, see [Set up the State model and Action task model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/establish-state-model-record.md).

4.  Update the state of the vulnerability record.

    |Step|Description|
    |----|-----------|
    |**Select __Update state__ UI action, select __Assessment__, add comments in __Additional comments__, and select __Submit__.**|This action updates the state of the vulnerability record to the **Assessment** state.|
    |**Select __Update state__ UI action, select __Treatment__, add comments in __Additional comments__, and select __Submit__.**|This action updates the state of the vulnerability record to the **Treatment** state.|

    The Update state window is shown in the example.

    \[Omitted image "op-vul-update-state.png"\] Alt text: Assessment.

    When the state is updated to **Assessment**, the state of the Operational vulnerability record is updated to the **Assessment in progress** state as shown in the example.

    \[Omitted image "op-vul-assmt-in-progress.png"\] Alt text: Assessment in progress.


## What to do next

When the vulnerability record is in the **Assessment** state, the task owner creates an assessment-type action task. For more information, see [Manage an assessment-type action task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-action-task-op-vul.md).

When the vulnerability record is in the **Treatment** state, the task owner creates an investigation-type action task. For more information, see [Manage an investigation-type action task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/update-state-of-action-task.md).

