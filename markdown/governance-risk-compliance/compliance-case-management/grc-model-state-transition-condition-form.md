---
title: GRC Model State Transition Condition form
description: Use the GRC Model State Transition Condition form to define the transition conditions to control how a compliance case or request traverses through the different workflow states by using the GRC: Compliance Case Management application.
locale: en-US
release: xanadu
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Define the model state transitions for a compliance case or request, Configuring Compliance Case Management, Compliance Case Management, Governance, Risk, and Compliance]
---

# GRC Model State Transition Condition form

Use the GRC Model State Transition Condition form to define the transition conditions to control how a compliance case or request traverses through the different workflow states by using the GRC: Compliance Case Management application.

See the following table for a description of the field values.

<table id="table_cgl_dsv_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the condition.

</td></tr><tr><td>

State transition

</td><td>

Transition of states. This field is automatically set to the model state transition value.

</td></tr><tr><td>

Application

</td><td>

Name of the application that this condition applies to. This field is automatically set to **GRC: Compliance Case Management**.

</td></tr><tr><td>

Active

</td><td>

Option to enable the model state transition condition.

</td></tr><tr><td>

Description

</td><td>

Description of this state transition. For example, in the **Description** field for the New state, you could enter `New state can move only to Analyze state`.

</td></tr><tr><td>

Error message

</td><td>

Error message to be displayed when the conditions aren’t met.

</td></tr><tr><td>

Requires

</td><td>

Transition conditions: -   **Task has been through Approval**: Condition passes if the related task has an approval that is either accepted or rejected.
-   **Task is Approved**: Condition passes when the task is approved.
-   **Task is Rejected**: Condition passes when the task is rejected.
-   **Transition Condition**: Conditions for this state transition.
-   **Transition Script**: Advanced conditions for this state transition.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be defined for this state transition. This field appears only when **Transition Condition** is selected from **Requires**.

</td></tr><tr><td>

Script

</td><td>

Script to be defined for this state transition. This field appears only when **Transition Script** is selected from **Requires**.

</td></tr></tbody>
</table>**Parent Topic:**[Define the model state transitions for a compliance case or request](../task/create-a-model-state-transition-for-compliance-case.md)

