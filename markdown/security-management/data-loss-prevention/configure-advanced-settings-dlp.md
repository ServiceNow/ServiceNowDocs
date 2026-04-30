---
title: Configure advanced settings
description: Configure the advanced settings to customize the incident display and behavior. For example, enable displaying the sensitive data on an incident and its clone, or specifying fields on the incident to identify the end users. In addition, activate and customize the evidence files preview properties.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Configure advanced settings

Configure the advanced settings to customize the incident display and behavior. For example, enable displaying the sensitive data on an incident and its clone, or specifying fields on the incident to identify the end users. In addition, activate and customize the evidence files preview properties.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

## About this task

Configure the advanced settings on the Data Loss Prevention Incident Response to customize the details to display for an incident or control the duration to identify a repeat offender.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Advanced Settings**.

2.  On the form, fill in the fields.

<table id="table_dzh_lm5_vsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Should sensitive data which caused the violation be displayed on the incident

</td><td>

Option to choose whether you want to display the sensitive data that caused the violation on the DLP incident.By default, this option is enabled.

</td></tr><tr><td>

Should sensitive data which caused the violation be displayed on the cloned incidents as well?

</td><td>

Option to choose whether you want to display the sensitive data that caused the violation on the DLP cloned incident as well.By default, this option is turned off.

</td></tr><tr><td>

List of fields on the incident that are used to identify the end user

</td><td>

The list of fields on the incident of the Assignment Rule module that are used to identify the end user. You can also specify your own custom attributes to identify the end user.

</td></tr><tr><td>

Maximum number of incidents in a digest email

</td><td>

The maximum number of incidents that can be sent in a digest email.By default, the value is 100.

</td></tr><tr><td>

Repeat offense maximum duration \(in days\)

</td><td>

The maximum duration to identify a repeat offender.By default, the value is 90 days.

</td></tr><tr><td>

Quick mode to send emails

</td><td>

Option to validate emails and identify issues. You can perform the validation by enabling the **Yes** option.By default, this option is enabled.

</td></tr><tr><td>

This property is for setting the log verbosity of the application

</td><td>

The log verbosity level of the application, meaning the name of the type of information. You can also update the value to the following options:-   **error**
-   **warn**
-   **info**
-   **debug**
 By default, the value is **info**.

</td></tr><tr><td>

Should downloading the violating file of the reported incident be allowed

</td><td>

Option to download the violating file of the reported incident. By default, this option is **Yes**.

</td></tr><tr><td>

Exclude cloned and child incidents from reports

</td><td>

Option to exclude the cloned and child incidents from the reports.By default, this option is **Yes**.

</td></tr><tr><td>

Day\(s\) to wait for deleting match content on cloud storage after incident gets closed

</td><td>

Option to choose the number of wait days to clean up the match content of those incidents that are inactive for a specific time duration.By default, the value is 90. If the DLP incident is inactive after 90 days, the match content is cleaned up from the cloud storage.

</td></tr><tr><td>

Assign Incident to DLP Analyst group after last escalation level

</td><td>

Select this check box to assign the incident to the analyst after the last escalation level.

</td></tr><tr><td>

Allow users to access incidents post escalation

</td><td>

Select this check box to enable the assigned users to access the incidents after the escalation.When you select this option, all the users that were added to the escalation chain list can access the incidents.

</td></tr><tr><td>

List of fields on the "sys\_user" table that are used to uniquely identify the user in DLP workspaces

</td><td>

Options to uniquely identify the user in the DLP workspaces.The options are email and user\_name.

</td></tr><tr><td>

Allow analyst to edit completed assessment

</td><td>

Select this check box to enable the analyst to edit the completed assessment.When you select this option, the analysts can edit the Assessments, when unselected you can view the assessments in the Read-Only mode.

</td></tr><tr><td>

List of valid file extensions. This property is a comma separated string. Each token indicates an extension.

</td><td>

List of the valid file extensions. Keep the field empty to allow all file extensions.

</td></tr><tr><td>

Enabling this system property will display the Playbook tab under DLP Incidents and provide the option to manually trigger a playbook via the Add Playbook action

</td><td>

Option to display the Playbook tab and manually add the Playbook action.By default, this option is **Yes**.

</td></tr><tr><td colspan="2">

**Evidence Files Preview Properties**

</td></tr><tr><td>

Enabling this system property activates the evidence file preview feature in the DLP analyst workspace.sn\_dlir.enable\_evidence\_file\_preview

</td><td>

Option to choose whether you want to preview the evidence files directly in the workspace.By default, this option is **Yes**.

</td></tr><tr><td>

This will allow DLP users to download the previewed evidence files. Once this property is enabled, users will see a download button in the document viewer to download the evidence file.sn\_dlir.enable\_download in\_preview

</td><td>

Option to display the download button in the document viewer. The download button enables you to download the previewed evidence files.By default, this option is **Yes**.

</td></tr><tr><td>

This property determines the duration for which files will be temporarily retained for evidence file preview purposes. \(in minutes\)sn\_dlir.preview\_temp\_files\_cleanup\_interval

</td><td>

The maximum duration for which files are temporarily stored for evidence file preview.By default, the value is 10. If the DLP incident is inactive after 10 minutes, the evidence file is cleaned up from the analyst workspace.

</td></tr><tr><td>

Enabling this property will extend the cleanup interval if evidence files are in use. This will allow the system to extend the expiry time of evidence files based on the value set in the system property "sn\_dlir.preview\_temp\_files\_cleanup\_interval".sn\_dlir.extend\_cleanup\_interval\_on\_usage

</td><td>

Option to extend the time before evidence files are deleted if they’re being used.By default, this option is **Yes**.

</td></tr><tr><td>

The maximum duration to extend the cleanup interval of evidence files \(in minutes\).sn\_dlir.max\_extension\_duration\_for\_cleanup

</td><td>

Option to select how long, in minutes, the system keeps your evidence files before cleaning them up.By default, the value is 60.

</td></tr></tbody>
</table>3.  Select **Save**.


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

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create Additional Incident Data Fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

