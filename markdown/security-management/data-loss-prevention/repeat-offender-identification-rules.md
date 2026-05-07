---
title: Create repeat offender identification rules
description: Create repeat offender identification rules to identify users who repeat the same issue multiple times.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create repeat offender identification rules

Create repeat offender identification rules to identify users who repeat the same issue multiple times.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

## About this task

You can identify repeat offenders by using certain rules or criteria. Data Loss Prevention Incident Response provides fields that you can use to identify repeat offenders.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Repeat offender identification rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_sjp_4fl_jtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the repeat offender identification rule.

</td></tr><tr><td>

Execution order

</td><td>

Priority of the repeat offender identification rules. This field indicates the order in which the repeat offender identification rules are executed when two or more rules share the triggering conditions.The repeat offender identification rule with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, or any other number. The default value is 100.

</td></tr><tr><td>

Short description

</td><td>

Unique description for this repeat offender identification rule.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder that are based on the DLP incident table. You can select any of the incident fields for building the trigger condition for the repeat offender identification rule.Use the lists and fields of the conditions builder to set the filters for the first row.

 To add more conditions, click **AND** or **OR**:

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
 To set a second filter condition, click **New Criteria**.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

DLP fields

</td><td>

Identify repeat offenders based on the required DLP fields. Select the DLP fields that you want to use from the Available column and move them to the Selected column.For example, you can select the**File Name** and **File Owner** fields from the Available column and move them to the Selected column. Then, you can identify the repeat offenders based on the **File Name** and **File Owner** fields.

 Thus, if a user breaches the repeat offender threshold \(number of violations and duration\), and if the same user matches with the DLP fields, then that particular user is identified as a repeat offender.

</td></tr><tr><td>

Number of violations

</td><td>

Define the repeat offender threshold limit value. After the user repeats the same actions and breaches the specified number of violations, the user is identified as a repeat offender.

</td></tr><tr><td>

Duration \(in days\)

</td><td>

Define the repeat offender threshold limit in the form of days. After the user repeats the same actions and breaches the threshold duration, the user is identified as a repeat offender.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

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

[Create additional incident data fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

