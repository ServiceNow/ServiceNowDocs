---
title: Workflow State form
description: Use the Workflow State form to define the workflow states in the GRC: Compliance Case Management application.
locale: en-US
release: australia
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create workflow state, Configure, Compliance Case Management, Governance, Risk, and Compliance]
---

# Workflow State form

Use the Workflow State form to define the workflow states in the GRC: Compliance Case Management application.

See the following table for a description of the field values.

<table id="table_scv_csr_3wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

Select an applicable state.Name of the workflow state for compliance case:

-   **New**
-   **Triage**
-   **Investigate**
-   **Resolve**
-   **Post case review**
-   **Close**
-   **Canceled**

Name of the workflow state for compliance request:

-   **New**
-   **Triage**
-   **In progress**
-   **Canceled**
-   **Awaiting approval**
-   **Approved**
-   **Rejected**
-   **Closed**

</td></tr><tr><td>

Application

</td><td>

Name of the application that this view rule applies to. This field is automatically set to **GRC: Compliance Case Management**. You cannot update it.

</td></tr><tr><td>

Model

</td><td>

State model that uses this workflow state. This field is automatically set to the state model name. You cannot update it.

</td></tr><tr><td>

Display type

</td><td>

Display type option of the workflow state:-   **As node**: Option to select as a parent state.
-   **As sub-level**: Option to select as a sub-state of the parent state.

</td></tr><tr><td>

Is optional

</td><td>

Option to select the state as optional. This field appears only when **As node** is selected from **Display type**.

</td></tr><tr><td>

Stepper label

</td><td>

Label to be displayed on the stepper component for the state. This field appears only when **As sub-level** is selected from **Display type**. The label is updated on the Overview page and not on the State section.

</td></tr><tr><td>

Parent model state

</td><td>

Parent state for the sub-level state. This field appears only when **As sub-level** is selected from **Display type**.

</td></tr></tbody>
</table>**Parent Topic:**[Create a workflow state for a compliance case or request](../task/create-workflow-state.md)

