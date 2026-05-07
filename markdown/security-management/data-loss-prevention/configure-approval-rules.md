---
title: Create Approval Rules
description: Configure approval rules that require one or more approvers to authorize an advanced response option before it is applied to a DLP incident.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create Approval Rules

Configure approval rules that require one or more approvers to authorize an advanced response option before it is applied to a DLP incident.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

## About this task

An approval rule is triggered when an end user selects a response option that is marked as Advanced on a DLP incident. When the rule's conditions match the incident fields, the system initiates an approval request and routes it to the configured approvers before the response option can be applied. If multiple rules match, the rule with the lowest **Execution order** value runs first.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **DLP Approval Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ilq_qrg_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the approval rule.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the approval rule is active.

</td></tr><tr><td>

Execution order

</td><td>

The approval rule priority. This field indicates the order in which the approval rules are executed when two or more rules share the triggering conditions.

 The approval rule with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, 300, and so on.

 The default value is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for the approval rule.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder. These conditions are based on the DLP incident table. To build a condition for the approval rule, select any of the incident fields. Use the lists and fields of the conditions builder to set the filters for the first row.

To add more conditions, select **AND** or **OR**.

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
To set a second filter condition, select **New Criteria**.

For example, you can set the conditions for this incident consolidation rule by selecting the condition as **Integration Source**, **contains**, **Microsoft**.

</td></tr><tr><td>

Applicable for response options

</td><td>

Option to select the response option of type advanced.You can select the multiple response options.

</td></tr><tr><td>

Approver

</td><td>

Select how approvers are identified for this rule.-   **User Table**: Selects an approver based on a field in the Users \(sys\_user\) table, such as the incident assignee's manager.
-   **Custom Approval List**: Configures a multi-level approval chain with specific users or groups at each level.


</td></tr><tr><td>

Approver identifier

</td><td>

This field will appear when **User Table** is selected for **Approver** option.Select field to identifier the approver from the Users\(sys\_user\) table.

</td></tr><tr><td>

Number of levels

</td><td>

This field will appear when **User Table** is selected for **Approver** option.Enter a number in this field to define the levels of approval.

For example, if 3 is added in the Number of levels field and Manager is selected in the Approver identifier field then approval request will traverse to three levels of approval.

</td></tr></tbody>
</table>    For example, your organization requires manager approval before a DLP analyst can apply the **Block** response option to any Microsoft DLP incident. Configure the rule as follows:

    -   **Condition:** Integration Source \| contains \| Microsoft
    -   **Applicable for response options:** Block
    -   **Approver:** User Table
    -   **Approver identifier:** Manager
    -   **Number of levels:** 1
    When an analyst selects **Block** on a qualifying Microsoft DLP incident, the system creates an approval request and routes it to the analyst's manager. The response option is applied only after the manager approves.

4.  For the **Approver** option, select **Custom Approval List**.

5.  Select **Submit**.

6.  Verify that the **Approval Levels** related list appears on the form.

7.  In the **Approval Levels** section, select **New**.

8.  On the form, fill in the fields.

<table id="table_obp_52q_yxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the approval level.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the approval level is active.

</td></tr><tr><td>

level

</td><td>

The level for the approval rule. This field indicates the order in which the approval levels are executed when two or more levels are configured.The approval level with the lowest number has the highest priority.

To set the level of operation, enter a value. For example, 100, 200, 300, and so on.

The default value is 100.

</td></tr><tr><td>

Approval Rule

</td><td>

Approval Rule for which you want to define this configuration.This will be read-only field.

</td></tr><tr><td>

Description

</td><td>

Unique description for the approval level.

</td></tr><tr><td>

Approvals required

</td><td>

Select option to define whether approval from all the configured users/groups are required or only required from any one user.

</td></tr><tr><td>

Approvers

</td><td>

Option to select the approvers. 1.  Users and Groups:
    1.  **Users**: Add a particular user from the list. You can add yourself or add a user by using their email address or search option.
    2.  **Groups**: Select the &lt;add\_icon&gt; icon to add a particular group from the list. You can also add a group by using the search option.
2.  **Find by using script**: You can use the script editor to customize and format the field values during the approval level creation. For example, you can use the email address field to identify the approver user.


</td></tr></tbody>
</table>9.  Select **Submit**.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](setup-response-due-date-rules.md)

[Create user instructions templates](create-and-manage-user-instructions-template-for-dlp-incidents.md)

[Create email templates](create-and-manage-email-templates.md)

[Create a Data Loss Prevention Incident Response SLA trigger](sla-records.md)

[Create a Data Loss Prevention Incident Response SLA definition](dlp-sla-definitions.md)

[Create assessments](create-and-manage-assessments-for-dlp-incidents.md)

[Configure response option for your DLP incidents](configure-response-option-mapping.md)

[Create incident response option rules](configure-end-user-action.md)

[Create age chart configurations](configure-age-chart.md)

[Create user delegate configurations](configure-delegation.md)

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create additional incident data fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

