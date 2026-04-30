---
title: Create assignment rules
description: Create assignment rules and assign the Data Loss Prevention Incident Response \(DLP IR\) incidents to user groups, end users, managers, or user from incident.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 7
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create assignment rules

Create assignment rules and assign the Data Loss Prevention Incident Response \(DLP IR\) incidents to user groups, end users, managers, or user from incident.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

## About this task

Use assignment rules to assign DLP IR incidents to user groups, end users, or to managers. The assignment of the DLP incidents occur when the conditions in the assignment rule are met.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Assignment Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ilq_qrg_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the assignment rule.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the assignment rule is active.

</td></tr><tr><td>

Execution order

</td><td>

The assignment rule priority. This field indicates the order in which the assignment rules are executed when two or more rules share the triggering conditions.The assignment rule with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, 300, and so on.

The default value is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for this assignment rule.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder. These conditions are based on the DLP incident table. To build a condition for the assignment rule, select any of the incident fields.Use the lists and fields of the conditions builder to set the filters for the first row.

To add more conditions, click **AND** or **OR**.

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
To set a second filter condition, click **New Criteria**.

For example, assume you create a DLP assignment rule for an endpoint. You can specify that the condition scan source is an endpoint file system that must be met before assigning an incident.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Assign to

</td><td>

Assignment to either one of the following:-   User group
-   End user
-   Manager
-   User from incident
The assignment occurs when the conditions in the condition builder are met.

</td></tr><tr><td>

User group

</td><td>

Option to search and select a user group to assign the DLP incidents to. This field appears when **User group** is selected from the **Assign to** field.**Note:** You can only view and select groups that have been assigned with the sn\_dlir.analyst role.

</td></tr><tr><td>

End user

</td><td>

Option to assign the DLP incident to the end user. The assignment occurs when the conditions in the condition builder are met.

</td></tr><tr><td>

Assign using Manager fields

</td><td>

Manager of the end user. This field appears when **Manager** is selected from the **Assign to** field. You can assign the DLP incidents to a particular manager by selecting one of the Manager fields, such as Last name, Email, City, Employee number.

</td></tr><tr><td>

User Identifier

</td><td>

The user identifier of the incident. This field appears when **User from Incident** is selected from the **Assign to** field. You can select an user identifier from the following:-   **Data owner email**
-   **Destination**
-   **File created by**
-   **File modified by**
-   **File owner**
-   **FTP user name**
-   **Sender**
-   **Custom user from incident**


</td></tr><tr><td>

Custom attribute

</td><td>

Option to specify a custom attribute from the incident that has the reference to a user. This field appears only when the **Custom User from Incident** is selected from the **User Identifier** field.

</td></tr><tr><td>

Attach Assessment

</td><td>

Option to indicate whether you want to attach an assessment to the incident.

</td></tr><tr><td>

Pre assessment response state

</td><td>

Option to select which state that the incident should be in before the end user responds. It can also be a custom state.The default value is Pending assessment.

</td></tr><tr><td>

Post assessment response state

</td><td>

Option to select which state that the DLP incident should be in after the user responds.The default value is Assessment Completed.

</td></tr><tr><td>

Advanced

</td><td>

Advanced option to identify the end user. This field appears only when the **Custom User from Incident** is selected from the **User Identifier** field. You can use the script editor to customize and format the field values during the assignment rule creation to identify the end user. Then, you pick whom you want to assign the DLP incident to, which could be an End user or the End user's Manager.

For example, you can use the email address field to identify the end user.

</td></tr></tbody>
</table>    The following example shows an assignment rule with the name `Assign 'Medium' Priority Incident to End User`. The condition builder requires the Scan Source to be `Endpoint File System`, and the `Assign to` field is set to `End user`. Then, you can look up the 'Email' of the End user.

    ![Create the assignment rules for your Data Loss Prevention Incident Response incidents](../image/dlp-assignment-rule.png "DLP Assignment rule")

4.  Select the **Assign to** field from the related list section where all the DLP incidents are assigned to.

    Click **Edit** to add the user group. When you click **Edit** from the related list section and select an item from the **Collections** columns and then add that selected assignee to the Group columns in the **Edit Members** page, and save the list.

    **Note:** You can only view and select groups that have been assigned with the sn\_dlir.analyst role from the related list. You can only select one group.

5.  Click **Submit**.

    You can select one or more assignment rules and reapply it on all existing DLP incidents.

6.  To reapply an assignment rule on all existing DLP incidents, click **Reapply**.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](setup-response-due-date-rules.md)

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

[Create Additional Incident Data Fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

