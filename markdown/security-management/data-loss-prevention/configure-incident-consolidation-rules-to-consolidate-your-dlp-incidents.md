---
title: Create incident consolidation rules
description: Create incident consolidation rule to consolidate multiple incidents of similar nature under one parent incident.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create incident consolidation rules

Create incident consolidation rule to consolidate multiple incidents of similar nature under one parent incident.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\)

## About this task

The DLP admin defines these incident consolidation rules to automatically consolidate the DLP incidents of same nature under one parent incident. The DLP incident consolidation rule enables you to consolidate the DLP incidents based on configuration provided for Consolidation duration and Consolidation identification.

**Note:**

When a consolidated incident is created, it becomes a child of the parent DLP incident. If the severity of the consolidated incident is higher than that of the parent, then the parent incident severity will be updated to match with the child incident.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **DLP Incident Consolidation Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ilq_qrg_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the incident consolidation rule.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the incident consolidation rule is active.

</td></tr><tr><td>

Execution order

</td><td>

The incident consolidation rule priority. This field indicates the order in which the incident consolidation rules are executed when two or more rules share the triggering conditions.

 The incident consolidation rule with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, 300, and so on.

 The default value is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for the incident consolidation rule.

</td></tr><tr><td>

Condition

</td><td>

Conditions in the condition builder. These conditions are based on the DLP incident table. To build a condition for the incident consolidation rule, select any of the incident fields.Use the lists and fields of the conditions builder to set the filters for the first row.

To add more conditions, click **AND** or **OR**.

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
To set a second filter condition, click **New Criteria**.

For example, you can set the conditions for this incident consolidation rule by selecting the condition as **Integration Source**, **contains**, **Symantec**.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Consolidation duration

</td><td>

Option to set the duration for the incident consolidation.Incidents in this period with same values for the selected fields will be consolidated under the first incident. The first incident matching this rule will be the parent incident and rest of incidents will be child incidents.

</td></tr><tr><td>

Consolidate incidents by

</td><td>

Select DLP incident field to consolidate the incidents when having the same value in selected field for different incidents.Select at least one field. Select at least one field.

</td></tr></tbody>
</table>    The following example shows an incident consolidation rule with the name Consolidate incidents for Symantec Integration. The condition builder requires the Integration Source as Symantec. The **Condition duration** option is set to 1 hour, and Policy Name option is selected for **Consolidate incident by**.

    At the time of Symantec DLP Incident ingestion, this rule will be executed and when multiple Incidents have the same Policy Name, the Incident will be consolidated under the first ingested incident matching this rule.

4.  Click **Submit**.

    Incidents consolidated based on the consolidation rule will be available under the Child incidents list on DLP Analyst Workspace.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

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

