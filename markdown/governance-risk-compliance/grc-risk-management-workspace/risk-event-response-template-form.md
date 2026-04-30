---
title: Risk Event Response Template form
description: Use the Risk Event Response Template form to define assignment rules. Rules automatically assign owners, approvers, issues, and Root Cause Analysis \(RCA\) tasks to risk events based on entity, event type, category, and impact thresholds.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-02-19"
reading_time_minutes: 6
breadcrumb: [Create a risk event response template, Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Risk Event Response Template form

Use the Risk Event Response Template form to define assignment rules. Rules automatically assign owners, approvers, issues, and Root Cause Analysis \(RCA\) tasks to risk events based on entity, event type, category, and impact thresholds.

See the following table for a description of the field values.

<table id="table_byk_bhv_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Template number. This field is automatically set.

</td></tr><tr><td>

Entity

</td><td>

Entity that the template is created for.**Note:** When you select an entity in a Risk Event Response Template, the template applies to that entity and all its downstream entities unless a downstream entity has its own specific Risk Event Response Template. If a downstream entity does not have a separate template, the system applies the template from the nearest parent entity in the hierarchy.

</td></tr><tr><td>

Category

</td><td>

Category that the risk event applies to if there’s an occurrence. You can edit the category to apply one of the following options.-   **Personal**: For example, any physical harm caused to an employee.
-   **Legal**: For example, an employee conducts a business that is a conflict of interest.
-   **Information Security**: For example, a theft, burglary, or system crash.
-   **Human Resources**: For example, sensitive lawsuits by an employee against another employee.
-   **All**: Any risk event that is reported.

</td></tr><tr><td>

Approval rule based on

</td><td>

Rule used while assigning the event. -   **Gross Loss**
-   **Net Loss**
-   **Expected Loss**

This field depends on the values in the **Event type** and **Sub type** fields. For example, -   If the event type is **Financial**, and the sub type is **Actual**, the approval rule is based on gross loss, net loss, or expected loss.
-   If the event type is **Financial**, and the Sub type is **Potential**, the approval rule is expected loss, by default.
-   If the Event type is **Non-Financial Impact**, the approval rule is Non-financial, by default.

</td></tr><tr><td>

Event type

</td><td>

Classification of the event based on the type of impact on the organization. This field determines whether the event has a financial or non‑financial consequence. The options are as follows:-   **Financial Impact**: Indicates that the event has an associated financial loss. Enter the amount. You can choose the currency.
-   **Non-Financial Impact**: Indicates that while the event doesn’t have any financial loss, it does have a non-financial impact on the organization. For example, non-financial impact can be negative market news or a decline in employee morale.

</td></tr><tr><td>

Sub type

</td><td>

Classification of the event based on whether the impact has already occurred or may occur in the future. The options are as follows:-   **Actual**
-   **Potential**

</td></tr><tr><td>

Auto close event once approved

</td><td>

Option to select if the event must be closed after approval. Selecting this option results in closing of the event after the issue and root cause are closed. If a risk event has open issues or tasks, the risk event isn’t closed even after approval.

</td></tr><tr><td>

Currency conversion date

</td><td>

Currency conversion dates for the risk event entries. You can select specific dates for currency conversion rather than relying solely on the date of impact to calculate the net loss. The options are as follows:-   **Risk event entry date**
-   **First loss entry date**
-   **Last loss entry date**
-   **First recovery entry date**
-   **Last recovery entry date**
-   **Custom date**

</td></tr><tr><td class="sub-head" colspan="2">

Risk Event Owner Assignment

</td></tr><tr><td>

Assignment type

</td><td>

Specifies how the risk event owner is determined for the record. The selected assignment type controls whether the event is assigned to an individual user, a group, or derived dynamically from the selected entity. The options are as follows:-   **User**: Option to assign ownership directly to a specific user.
-   **Group**: Option to assign ownership to a group.
-   **User field on entity**: Option to assign ownership based on a predefined user field on the associated entity record.
-   **Entity stakeholder**: Option to assign ownership to a stakeholder associated with the selected entity.

</td></tr><tr><td>

Owner

</td><td>

User assigned as the risk event owner. This field appears only when **User** is selected from **Assignment type**.

</td></tr><tr><td>

Owning group

</td><td>

Group responsible for the risk event. This field appears only when **Group** is selected from **Assignment type**.

</td></tr><tr><td>

Risk event owner field on entity

</td><td>

User field on the associated entity used to derive the risk event owner. For example, the owner of the entity can be the risk event owner. This field appears only when **User field on entity** is selected from **Assignment type**.

</td></tr><tr><td>

Persona

</td><td>

Stakeholder role associated with the entity. Specifies the stakeholder role, such as Head of Business or Risk Manager, that the system uses to determine ownership or responsibility when assignment is based on an entity stakeholder. This field appears only when **Entity stakeholder** is selected from **Assignment type**.**Note:** Based on the selected persona, the **Owning group** field is auto-populated.

</td></tr><tr><td class="sub-head" colspan="2">

Issue Creation and Assignment

</td></tr><tr><td>

Automatically create issue

</td><td>

Option to create issue automatically based on the configured threshold and assignment settings.

</td></tr><tr><td>

Threshold for issue creation

</td><td>

Option to specify the threshold amount after which an issue is created automatically. For example, users can specify that after an event crosses loss worth $1000, an issue must be created.**Note:** This field appears only when **Automatically create issue** is selected.

</td></tr><tr><td>

Assignment type

</td><td>

Options to determine the issue owner for the record. The selected assignment type controls whether the issue is assigned to an individual user, a group, or derived dynamically from the selected entity. The options are as follows:-   **User**: Option to assign ownership directly to a specific user.
-   **Group**: Option to assign ownership to a group.
-   **User field on entity**: Option to assign ownership based on a predefined user field on the associated entity record.
-   **Entity stakeholder**: Option to assign ownership to a stakeholder associated with the selected entity.

**Note:** This field appears only when **Automatically create issue** is selected.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned as the issue owner. This field appears only when **User** is selected from **Assignment type**.

</td></tr><tr><td>

Assignment group

</td><td>

Group responsible for the issue. This field appears only when **Group** is selected from **Assignment type**.

</td></tr><tr><td>

Issue assignee field on entity

</td><td>

User field on the associated entity used to derive the issue owner. For example, the owner of the entity can be the issue owner. This field appears only when **User field on entity** is selected from **Assignment type**.

</td></tr><tr><td>

Persona

</td><td>

Stakeholder role associated with the entity. This field identifies the type of stakeholder \(for example, Head of Business or Risk Manager\) used to determine ownership or responsibility when assignment is based on an entity stakeholder. This field appears only when **Entity stakeholder** is selected from **Assignment type**.

</td></tr><tr><td>

Owning group

</td><td>

Based on the selected Persona, the **Owning group** field is auto-populated.

</td></tr><tr><td class="sub-head" colspan="2">

Root Cause Analysis Task

</td></tr><tr><td>

Automatically create RCA task

</td><td>

Option to create a task for root cause analysis \(RCA\). Automatically create a Root Cause Analysis \(RCA\) task based on the amount entered in the **Threshold for task creation** field.

</td></tr><tr><td>

Assigned to

</td><td>

Person that the RCA task is assigned to.**Note:** This field appears only when **Automatically create RCA task** is selected.

</td></tr><tr><td>

Threshold for task creation

</td><td>

Option to specify the threshold amount after which an RCA task is created automatically. For example, users can specify that after an event crosses loss worth $1000, an RCA task must be created.**Note:** This field appears only when **Automatically create RCA task** is selected.

</td></tr><tr><td>

Priority

</td><td>

Priority of the event. The options are as follows: -   **Critical**
-   **High**
-   **Moderate**
-   **Low**
-   **Minor**

**Note:** This field appears only when **Automatically create RCA task** is selected.

</td></tr></tbody>
</table>**Parent Topic:**[Create a risk event response template](../task/create-risk-event-response-template.md)

