---
title: Create a risk event response template
description: Automatically add approvers, issues, and owners to a risk event based on the conditions defined in the risk event response template.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk event response template

Automatically add approvers, issues, and owners to a risk event based on the conditions defined in the risk event response template.

## Before you begin

Role required: sn\_risk.manager and sn\_risk.admin

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **Administration** &gt; **Response Templates**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_byk_bhv_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Template number. This number is automatically set.

</td></tr><tr><td>

Entity

</td><td>

Entity that the template is created for.

</td></tr><tr><td>

Category

</td><td>

Category that the risk event applies to if there is an occurrence. You can edit the category to apply one of the following options.-   **Personal**: For example, any physical harm caused to an employee.
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
This field depends on the values in the **Event type** and **Sub type** fields. For example, if the event type is **Financia**l, and the sub type is **Actual**, the approval rule is based on gross loss, net loss, or expected loss. If the Sub type is **Potential**, the approval rule is expected loss, by default. If the Event type is **Non-Financial Impact**, the approval rule is Non-financial, by default.

</td></tr><tr><td>

Event type

</td><td>

Event type.-   **Financial Impact**: Indicates that the event has an associated financial loss. Enter the amount. You can choose the currency.
-   **Non-Financial Impact**: Indicates that while the event does not have any financial loss, it does have a non-financial impact on the organization. For example, non-financial impact can be negative market news or a decline in employee morale.


</td></tr><tr><td>

Sub type

</td><td>

Event sub type. Select one of the following:-   **Actual**
-   **Potential**


</td></tr><tr><td>

Auto close event once approved

</td><td>

Option to select if the event must be closed after approval. Selecting this option results in closing of the event after the issue and root cause are closed. If a risk event has open issues or tasks, the risk event is not closed even after approval.

</td></tr><tr><td>

Currency conversion date

</td><td>

Currency conversion dates for the risk event entries. You can select specific dates for currency conversion rather than relying solely on the date of impact to calculate the net loss. The options are as follows:-   **Risk event entry date**
-   **First loss entry date**
-   **Last loss entry date**
-   **First recovery entry date**
-   **Last recovery entry date**
-   **Custom date**


</td></tr></tbody>
</table>4.  In the Risk Event Owner Assignment section, select the assignment type and the owner or owning group.

5.  To automatically create an issue, select the **Automatically create issue** check box in the Issue Creation and Assignment section.

6.  In the Root Cause Analysis Task section, fill in the fields.

<table id="table_klk_tkv_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automatically create RCA task

</td><td>

Task creation for root cause analysis \(RCA\). Automatically create a Root Cause Analysis \(RCA\) task based on the amount entered in the **Threshold for task creation** field.

</td></tr><tr><td>

Assigned to

</td><td>

Person that the RCA task is assigned to.

</td></tr><tr><td>

Threshold for task creation

</td><td>

Option to specify the threshold amount after which an RCA task is created. For example, users can specify that after an event crosses loss worth $1000, an RCA task must be created.

</td></tr><tr><td>

Priority

</td><td>

Priority of the event. Select from: -   **Critical**
-   **High**
-   **Moderate**
-   **Low**
-   **Minor**


</td></tr></tbody>
</table>7.  Select **Submit**.

    A new risk event response template is created.


-   **[Define a threshold amount for the risk event response template](define-threshold-amount-risk-event.md)**  
Define a threshold limit for assigning risk event approvers. A threshold limit is defined to determine if a risk event needs an approver.

**Parent Topic:**[Use Risk Events](../concept/use-risk-events.md)

