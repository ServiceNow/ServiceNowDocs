---
title: Create end user lookup rules
description: You can create and configure end user lookup rules and assign the DLP incidents to the respective end users based on those rules.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create end user lookup rules

You can create and configure end user lookup rules and assign the DLP incidents to the respective end users based on those rules.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

The DLP admin defines these end user lookup rules to automatically assign the end users to DLP incidents using only the end user field. The DLP end user lookup rule enables you to assign the end user on DLP incidents based on End user identifier, Custom attributes, or Script.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **DLP End User Lookup Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ilq_qrg_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the end user lookup rule.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the end user lookup rule is active.

</td></tr><tr><td>

Execution order

</td><td>

The end user lookup rule priority. This field indicates the order in which the end user lookup rules are executed when two or more rules share the triggering conditions.The end user lookup rule with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, 300, and so on.

The default value is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for the end user lookup rule.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder. These conditions are based on the DLP incident table. To build a condition for the end user lookup rule, select any of the incident fields.Use the lists and fields of the conditions builder to set the filters for the first row.

To add more conditions, click **AND** or **OR**.

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
To set a second filter condition, click **New Criteria**.

For example, you can set the conditions for this end user lookup rule by selecting the condition as **Integration Source**, **contains**, **Symantec**.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Lookup end user by using

</td><td>

Option to lookup end user by using **Incident field** or **Script**.

</td></tr><tr><td>

End User Identifier

</td><td>

The end user identifier of the DLP incident. This field appears when **Incident field** is selected from the **Lookup end user by using** field. You can select an end user identifier from the following:-   **Data owner email**
-   **Destination**
-   **File created by**
-   **File modified by**
-   **File owner**
-   **FTP user name**
-   **Sender**

**Note:** The above listed end user identifiers are configurable using the system property `sn_dlir.assignment.fields`. For more information, see [Configure advanced settings](configure-advanced-settings-dlp.md).

-   **Custom user from incident**


</td></tr><tr><td>

Custom attribute

</td><td>

Option to specify a custom attribute from the incident that has the reference to a user. This field appears only when **The a** is selected from the **End User Identifier** field.

</td></tr><tr><td>

Script

</td><td>

You can use the script editor to customize and format the field values during the end user lookup rule creation. For example, you can use the email address field to identify the end user.

</td></tr></tbody>
</table>    The following example shows an end user lookup rule with the name 'Symantec'. The condition builder requires the 'Integration Source' as 'Symantec'. The **Lookup end user by using** option is set to 'Incident field', and **End user identifier** option is set to 'File Modified by'.

4.  Click **Submit**.

    You also have an option to select one or more end user lookup rules and reapply it on all existing DLP incidents.

5.  To reapply an end user lookup rule on all existing DLP incidents, click **Reapply**.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create assignment rules](create-assignment-rules.md)

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

