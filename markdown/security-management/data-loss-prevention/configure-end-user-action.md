---
title: Create incident response option rules
description: Create the incident response option rules that end user or analyst can use while responding to an incident.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create incident response option rules

Create the incident response option rules that end user or analyst can use while responding to an incident.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

You can configure the type of response that an end user should perform based on the type of DLP incident. The base system DLP Incident Response application provides the following response options for users:

-   Assessment Complete
-   Deleted Content
-   Deleted File
-   Encrypted File
-   Masked Content
-   Report false positive
-   Report wrong owner
-   Required for Business Process
-   Reviewed Entitlements

For example, let's say that an end user reports a DLP incident as a false positive. The state for this incident is then automatically marked as closed because the target state that is configured by you is closed.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Incident Response Option Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_vvq_l5k_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the incident response option.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the incident response option is active.

</td></tr><tr><td>

Execution order

</td><td>

Priority of the incident response option. This field indicates the order in which the incident response options are executed when two or more incident response options share the triggering conditions.The incident response option with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, or any other number.

 The default is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for this incident response option.

</td></tr><tr><td>

Default target state

</td><td>

The default target state that you configured.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder. These conditions are based on the DLP incident table. To build a condition for the incident response options, select any of the incident fields.Use the lists and fields of the conditions builder to set the filters for the first row.

 To add more conditions, click **AND** or **OR**:

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
 To set a second filter condition, click **New Criteria**.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr></tbody>
</table>    The following example shows the end-user action configuration for an endpoint. The condition requires the scan source to be an endpoint file system that then triggers this end-user action configuration. The mapping shows that the report wrong owner, report false positive, and deleted file are the response options available to the end user.

4.  In the **Response Option Mappings** section, click **New**.

5.  On the form, fill in the fields.

<table id="table_wrk_qyk_zrb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Response Option Rule

</td><td>

Name of the incident response option rule. For example, `SharePoint` implies that the scan source is SharePoint. You can either enter the name of the incident response or look up using search.

</td></tr><tr><td>

Response Option

</td><td>

Option to select the response option. You can either enter the response option or look up using search.

</td></tr><tr><td>

Target State

</td><td>

The target state of the DLP incident after the end user selects the appropriate action.**Note:**

1.  The **Target State** field will appear only when you select **Response Option** which is of **Type: Basic**. For more information on how the target state types are configured, see [Configure response option for your DLP incidents](configure-response-option-mapping.md).
2.  When a Response Option which is of **Type: Advanced** is selected, you will not be able to set the Target State and will be hidden. The Target State will be assigned based on the custom state that is configured from the flow designer sub flow.


</td></tr><tr><td>

Show response options for

</td><td>

Option to determine the user roles to show the response options for.You can choose from **Analyst**, **End user**, and **Escalated Analyst Reviewers** by using the unlock option. You are allowed to choose one or all the roles.

</td></tr></tbody>
</table>6.  Click **Submit**.


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

[Create age chart configurations](configure-age-chart.md)

[Create user delegate configurations](configure-delegation.md)

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create Additional Incident Data Fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

