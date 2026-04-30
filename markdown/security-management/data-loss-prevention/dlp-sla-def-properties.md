---
title: DLP SLA Definition form
description: Field descriptions for the DLP SLA Definition form used to create an SLA record.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# DLP SLA Definition form

Field descriptions for the DLP SLA Definition form used to create an SLA record.

<table id="table_opd_dxv_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the definition.

</td></tr><tr><td>

Type

</td><td>

Type of agreement, which in this case is SLA.

</td></tr><tr><td>

Target

</td><td>

Target used for filtering, searching and reporting on the agreement being defined. The available options are: -   None
-   Response
-   Resolution

</td></tr><tr><td>

Table

</td><td>

Table that determines the records tracked by the SLA, which should be DLP SLA Task \[sn\_dlir\_incident\_sla\_task\].

</td></tr><tr><td>

Flow

</td><td>

Flow to run when the SLA definition attaches to a Task record, which should be Default SLA flow.

</td></tr><tr><td>

Duration Type

</td><td>

Method to calculate the duration of the SLA. The available options are: -   User specified duration
-   2 business days by 4pm
-   3 business days by 4pm
-   Breach on Due Date
-   End of next business day
-   Next business day by 4pm

</td></tr><tr><td>

Duration

</td><td>

Length of time the SLA runs before it’s marked Breached. This field is available only when User specified duration is selected from **Duration Type**.

</td></tr><tr><td>

Schedule source

</td><td>

Schedule to use while creating the task SLAs.

</td></tr><tr><td>

Schedule

</td><td>

Hours during which the SLA timer runs. This set of schedules is defined in the core configuration.

</td></tr><tr><td>

Timezone Source

</td><td>

Timezone source to be used when creating task SLAs. The available options are:-   The caller's timezone
-   The SLA definition's timezone
-   The CI location's timezone
-   The task location's timezone
-   The caller location's timezone

</td></tr><tr><td>

Active

</td><td>

Option to make the trigger effective when the start condition is met.

</td></tr><tr><td colspan="2">

Tabs

</td></tr><tr><td>

Start condition

</td><td>

Condition that initiates the SLA timer and activates the SLA.

</td></tr><tr><td>

Pause condition

</td><td>

Conditions under which the SLA is suspended, which increases the total elapsed time.

</td></tr><tr><td>

Cancel condition

</td><td>

Conditions under which the SLA is cancelled.

</td></tr><tr><td>

Reset condition

</td><td>

Conditions under which the active SLA is completed and a new SLA is established when the value of any field on the task record changes, changes to, or changes from a specific value in the record. For example, say the value of the **Location** field in the task record is 101 Broadway East, Seattle, WA. If you set the SLA reset condition to **\[Location\]\[changes from\]\[101 Broadway East, Seattle, WA\]**, any change in the value of the **Location** field resets the SLA of the task record.

</td></tr></tbody>
</table>**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](../task/configure-data-loss-prevention.md)

[Create end user lookup rules](../task/configure-enduser-lookup-rules.md)

[Create assignment rules](../task/create-assignment-rules.md)

[Create incident consolidation rules](../task/configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](../task/setup-response-due-date-rules.md)

[Create Approval Rules](../task/configure-approval-rules.md)

[Create user instructions templates](../task/create-and-manage-user-instructions-template-for-dlp-incidents.md)

[Create email templates](../task/create-and-manage-email-templates.md)

[Create a Data Loss Prevention Incident Response SLA trigger](../task/sla-records.md)

[Create a Data Loss Prevention Incident Response SLA definition](../task/dlp-sla-definitions.md)

[Create assessments](../task/create-and-manage-assessments-for-dlp-incidents.md)

[Configure response option for your DLP incidents](../task/configure-response-option-mapping.md)

[Create incident response option rules](../task/configure-end-user-action.md)

[Create age chart configurations](../task/configure-age-chart.md)

[Create user delegate configurations](../task/configure-delegation.md)

[Create repeat offender identification rules](../task/repeat-offender-identification-rules.md)

[Create Additional Incident Data Fields](../task/create-custom-fields-dlp.md)

[Configure advanced settings](../task/configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](../task/dlp-archiving-rule.md)

[Create a Data Loss Prevention Incident Response SLA definition](../task/dlp-sla-definitions.md)

