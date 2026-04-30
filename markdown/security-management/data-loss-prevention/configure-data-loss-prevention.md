---
title: DLP default configuration settings
description: Define the default configuration settings for Data Loss Prevention Incident Response \(DLP IR\) incidents to identify and set up the incident notification and incident assignment preferences for your end users.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# DLP default configuration settings

Define the default configuration settings for Data Loss Prevention Incident Response \(DLP IR\) incidents to identify and set up the incident notification and incident assignment preferences for your end users.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

You can use this module to define the default configuration settings when the core assignment rules and identifier rules are exhausted and unable to match to a condition or user. You can also define and reapply End user lookup rules and Assignment rules to existing Active DLP incidents.

The end user incident notification enables you to specify the frequency at which email notifications are sent to your end users. For example, you can set up notification preferences to accumulate incidents and to send an email digest once a week. By assigning an incident, you can specify which group you initially assign the DLP incidents to. You can also specify how the end users are further identified by the DLP operations team.

For example, let's say that a user has stored credit card information in a file on a network. When the third-party DLP integration product creates an incident for a sensitive data policy violation, the incident data that the ServiceNow AI Platform DLP ingests would contain information about the end user. You would then be able to assign the incident to the right end user.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Default Configuration**.

    ![Configure DLP Incident Response policies to set up the notifications for end users](../image/dlp-default-config.png "Configure DLP policies")

2.  On the form, fill in the fields.

<table id="table_rxk_lqg_zrb"><thead><tr><th>

Configuration Name

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

End User Incident Notification

</td><td>

Notification Period \(days\)

</td><td>

Define the number of days after which an email notification should be sent to the end user. The number of days must be between 1–60 days.

</td></tr><tr><td>

Automatically update parent state based on cloned/child incidents

</td><td>

Option to automatically update the parent state incident based on the cloned or child incidents.

</td></tr><tr><td>

Incident Assignment

</td><td>

End User Identifier

</td><td>

Specify the field to be used from Incident data to identify the end user. Possibles values are the following:-   **Data owner email**
-   **Destination**
-   **File created by**
-   **File modified by**
-   **File owner**
-   **FTP user name**
-   **Sender**


</td></tr><tr><td>

Reapply End User Lookup Rules Behavior

</td><td>

When reapply option is chosen for end user lookup rules

</td><td>

Option to reapply End user lookup rules to existing Active DLP incidents. You can select one of the following option to reapply:-   **Update the End user value when the field is empty**: Updates the existing active DLP incidents' End user value if that field is empty.
-   **Update the End user value**: Updates the existing active DLP incidents' End user value.
-   **Update the End user and Assigned to values when both fields are empty**: Updates the existing active DLP incidents' End user and Assigned to values if both fields are empty.

**Note:** If this option is selected, then the **Update the Assigned to value when the field is empty** option gets disabled automatically in the Reapply Assignment Rules Behavior section as it's applicable for both.

-   **Update the End user and Assigned to values for all the active DLP incidents**: Updates the End user and Assigned to values for all active DLP incidents.

**Note:** If this option is selected, then the **Update the Assigned to value for all the active DLP incidents** option gets disabled automatically in the Reapply Assignment Rules Behavior section as it's applicable for both.

</td></tr><tr><td>

Reapply Assignment Rules Behavior

</td><td>

When reapply option is chosen for assignment rules

</td><td>

Option to reapply assignment rules to existing Active DLP incidents. You can select one of the following option to reapply:-   **Update the Assigned to value when the field is empty.**
-   **Update the Assigned to value for all the active DLP incidents.**


</td></tr></tbody>
</table>3.  Select the **Default Assignment Group** from the related list section where all the DLP incidents are assigned to.

    Click **Edit** to add the user group. When you click **Edit** from the related list section and select an item from the **Collections** columns and then add that selected assignee to the Group columns in the **Edit Members** page, and save the list.

    **Note:** You can only view and select groups that have been assigned with the sn\_dlir.analyst role from the related list. You can only select one group.

4.  Click **Save**.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


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

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

