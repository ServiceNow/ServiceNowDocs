---
title: Create response due date rules
description: Set up the response due date rules to determine the time you want to give your end users to respond to the assigned Data Loss Prevention Incident Response \(DLP IR\) incidents.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create response due date rules

Set up the response due date rules to determine the time you want to give your end users to respond to the assigned Data Loss Prevention Incident Response \(DLP IR\) incidents.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

## About this task

You can use this module to define the response due date rules for the different types of DLP incidents and the rules to start counting the due date. After the due date has expired, the users get notified about the overdue incident. You’re also provided with an option to escalate the overdue incident to one of the following:

-   Manager
-   Custom User from Incident
-   User group

For example, when you escalate the overdue incident to a Manager, and you’ve specified a maximum of three levels of escalation. The first level of Manager gets notified first. If the incident is overdue again, then the second level of Manager gets notified, followed by the third level if the incident is still overdue. If the Manager has a Delegate, then the Manager has the option to assign the escalation or overdue incident to the Delegate.

You’re also provided with the ability to create multiple response due date rules.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Response Due Date Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_x3v_tbh_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the response due date rule.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the response due date rule is active.

</td></tr><tr><td>

Due in \(days\)

</td><td>

Number of due days.

</td></tr><tr><td>

Due date counted from

</td><td>

Start date that is used to calculate the due date. The due date can be calculated from either the first time that the user was notified about the incident, or from the incident assignment date.

</td></tr><tr><td>

Notify before due date

</td><td>

Option to notify the end user about the DLP incident before the due date.

</td></tr><tr><td>

Notify on \(days before due date\)

</td><td>

Number of days before the due date when the rule triggers a notification to the end user.

</td></tr><tr><td>

Description

</td><td>

Unique description for this response due date rule.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder. These conditions are based on the DLP incident table. To build a condition for the response due date rule, select any of the incident fields.Use the lists and fields of the conditions builder to set the filters for the first row.

 To add more conditions, click **AND** or **OR**.

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
To set a second filter condition, click **New Criteria**.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Escalate

</td><td>

Option to escalate the DLP incident to someone if the response due date has been breached. For more information, see [Add multiple users to access DLP incidents](add-multiple-users-to-access-dlp-incidents.md)

</td></tr><tr><td>

Escalate overdue incident to

</td><td>

Option to specify if the incident should be escalated to a Manager, a Custom user, or a User group. This field appears only when the **Escalate** option is enabled.

</td></tr><tr><td>

Assign using

</td><td>

Specify how a manager should be identified. This field appears only when **Manager** is selected from the **Escalate overdue incident to** field.

</td></tr><tr><td>

Maximum Escalation Levels

</td><td>

Option to define the maximum number of escalation levels for a Manager, and a Custom user.As a Manager or Custom user, you can define any number of escalation levels. By default, three levels of escalation are provided.

-   As a Manager, you can define any number of escalation levels by updating the value in this field.
-   As a Custom user, you can use the + icon to define any number of escalation levels.


</td></tr><tr><td>

Custom attribute

</td><td>

Option to specify a custom attribute from the incident that has the reference to a user. This field appears only when **Custom User from Incident** is selected from the **Escalate overdue incident to** field.

</td></tr><tr><td>

User group

</td><td>

Option to search and select a user group to escalate DLP incidents to. This field appears only when **User group** is selected from the **Escalate overdue incident to** field.

**Note:** You can only view and select groups that have been assigned with the sn\_dlir.analyst role.

</td></tr></tbody>
</table>    The following example shows the response due date rule to determine how much time you want to give your end users to respond to the assigned Data Loss Prevention Incident Response \(DLP\) incidents. After the end user is first notified, the response due date is in two days. The conditions builder shows that the Scan Source must match the Endpoint File System to proceed with creating the response due date. The escalation option is selected. The incident is escalated to the manager if the response due date is breached.

4.  Click **Submit**.


-   **[Add multiple users to access DLP incidents](add-multiple-users-to-access-dlp-incidents.md)**  
Use the escalation chain feature to allow all the respective users who are involved in the incident to access the DLP incidents from the list view, though the incident is assigned to a different user.

**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create Approval Rules](configure-approval-rules.md)

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

