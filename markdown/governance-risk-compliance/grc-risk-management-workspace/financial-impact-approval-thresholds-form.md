---
title: Financial Impact Approval Thresholds
description: Use the Financial Impact Approval Thresholds form to define monetary thresholds that trigger approval requirements for risk events and to configure how approvers are determined when those thresholds are met.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Define a threshold amount for the risk event response template, Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Financial Impact Approval Thresholds

Use the Financial Impact Approval Thresholds form to define monetary thresholds that trigger approval requirements for risk events and to configure how approvers are determined when those thresholds are met.

See the following table for a description of the field values.

<table id="table_byk_bhv_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Threshold amount

</td><td>

Option to specify the monetary value that triggers an approval requirement. When the financial impact of a risk event meets or exceeds this amount, the system evaluates the approval rules defined by this record. The amount is evaluated in the selected currency.

</td></tr><tr><td>

Approver required

</td><td>

Option to specify whether approval is required when the threshold amount is met. When selected, the request can’t proceed until the required approval is granted. When cleared, approval isn’t enforced even if the threshold condition is met.

</td></tr><tr><td>

Assignment type

</td><td>

Options to determine the risk event approver when the threshold amount is met. The selected assignment type controls whether approval is routed to a specific user, a group, or resolved dynamically from the associated entity. The options are follows:-   **User**: Option to assign approver directly to a specific user.
-   **Group**: Option to assign approver to a group.
-   **User field on entity**: Option to assign approver based on a predefined user field on the associated entity record.
-   **Entity stakeholder**: Option to assign approver to a stakeholder associated with the selected entity.

**Note:** This field appears only when **Approver required** is selected.

</td></tr><tr><td>

Approver

</td><td>

User assigned to approve the risk event if the threshold amount is met. This field appears only when **User** is selected from **Assignment type**.

</td></tr><tr><td>

Approval group

</td><td>

Group responsible to approve the risk event if the threshold amount is met. This field appears only when **Group** is selected from **Assignment type**.

</td></tr><tr><td>

Approver user field

</td><td>

User field on the associated entity used to approve the risk event if the threshold amount is met. For example, the owner of the entity can be the approver. This field appears only when **User field on entity** is selected from **Assignment type**.

</td></tr><tr><td>

Persona

</td><td>

Stakeholder role associated with the entity, such as Head of Business or Risk Manager. The system uses the selected persona to determine the risk event approver when approval is based on an entity stakeholder. This field appears only when **Entity stakeholder** is selected from **Assignment type**.**Note:** Based on the selected persona, the **Owning group** field is auto-populated.

</td></tr></tbody>
</table>**Parent Topic:**[Define a threshold amount for the risk event response template](../task/define-threshold-amount-risk-event.md)

