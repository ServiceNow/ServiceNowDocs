---
title: Create email templates
description: Create and manage the preconfigured email templates for sending notifications to your end users, user groups, or managers. With these templates, you can coach and communicate with your end users about the Data Loss Prevention Incident Response \(DLP IR\) incidents.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create email templates

Create and manage the preconfigured email templates for sending notifications to your end users, user groups, or managers. With these templates, you can coach and communicate with your end users about the Data Loss Prevention Incident Response \(DLP IR\) incidents.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

    **Important:** For Analysts to view email communications of a DLP Incident on the activity stream, you should add or append the 'sn\_dlir.analyst' role in the global system property `glide.ui.activity.email_roles`.


## About this task

Email notifications are categorized by the incident notifications that are sent to the end users, the escalation notifications that are sent to the managers, or the due date notifications. You can send email notifications about the due dates for DLP incidents, or even coach the end users about what to do when certain conditions are met in the email conditions filter.

DLP email templates enable you to send the email notification for end users, managers, and analysts. You can configure the templates to be sent per incident or as a digest. Your email subject and body can contain variables so that you can reuse your existing content.

DLP provides the following preconfigured email templates based on the categories:

-   **DLP Email template - Per incident approval notification:** Notify users about the approval for their requests.
-   **DLP Email template - Escalation notification:** Send escalation notifications to managers in the form of digests.
-   **DLP Email template - Pending approval notification:** Notify approvers about pending items.
-   **DLP Email template - Per incident approval request cancellation notification:**Notify users about an approval request that has been cancelled by DLP analyst team.
-   **DLP Email template - User response completion notification:** Notify DLP analyst team about the response submitted by users.
-   **DLP Email template - User incident notification:**This is a default template for user digest notification. Send incident notifications to the end users in the form of digests every few days, even if there are no new incidents, to inform the users about the total number of incidents on the particular user’s name. You can also send digest notifications to notify the users about the nearest upcoming due dates of DLP incidents with the severity as critical, high, medium, or low.
-   **DLP Email template - Per incident pending approval notification**: Notify approvers about pending approvals.
-   **DLP Email template - rejection notification:** Send reject notification to requester.
-   **DLP Email template - Due date notification:** Send incident due date notification. If a DLP incident is assigned to the end user, and if the end user has not taken any action before the due date, then an email notification is sent to the end user. You also have an option to escalate the DLP incident to a manager, a custom user, or a user group if the response due date has been breached.

    **Note:** Due date notifications must be in the form of digests.

-   **DLP Email template - Per incident user response notification:** Notify analysts about the response submitted users per incident.
-   **DLP Email template - Per incident escalation notification:** Notify managers about escalations per incident.
-   **DLP Email template - Per incident user notification:** Notify users about assignment per incident.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Email Templates**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_r3h_shh_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the email template.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the DLP email template is active. If this option is not enabled, then notifications are not sent for this email template.

</td></tr><tr><td>

Category

</td><td>

Email notification category. DLP supports the following options:-   **Incident notification to end users**: Sent when the incidents are assigned to the end users.
-   **Escalation notification to managers**: Sent when the response due date is breached or manually assigned to the manager through DLP Ops portal.
-   **Due date notification**: Sent when the response due date is breached.
-   **User response notification to analysts**: Sent when the end user takes any action on the DLP incident.
-   **Pending approvals notification**: Notify approvers about pending items.
-   **Approval notification to the requester**: Notify users about the approval for their requests.
-   **Reject notification to the requester**: Notify users about the rejection for their requests.
-   **Cancel notification to the requester**: Notify users about the cancellation for their requests.


</td></tr><tr><td>

Type

</td><td>

Option to indicate whether the email is sent per incident or as a digest.**Note:** If you selected **Due date notification** from the **Category** field, then you can use only digests. Select this option.

</td></tr><tr><td>

Description

</td><td>

Unique description for this email template.

</td></tr><tr><td>

Execution Order

</td><td>

Email template priority. This field indicates the order in which the email templates are executed when two or more email templates share the triggering conditions.The email template with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, or any other number. The default value is 100.

</td></tr><tr><td>

Template Condition

</td><td>

Options in the template conditions that are based on the DLP incident table. You can select any of the incident fields for building the email template trigger condition.

 Use the lists and fields of the conditions builder to set the filters for the first row.

 To add more conditions, click **AND** or **OR**.

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
 To set a second filter condition, click **New Criteria**.

 **Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Target Users

</td><td>

Target users for the template when the conditions are met. The target users can be one of the following:-   **All recipients**: Send the email to target users.
-   **Recipients in the group:** Send the email only to recipients within a particular group by using the filter option.

-   **Recipients matching the criteria**: Send the email to target users who match the criteria. You can use the filter to drill down target users based on the conditions. For example, city.

</td></tr><tr><td>

Email Template

</td><td>

Email template that you can select. You can define the variables to reuse existing content to add to the email notification.The **Category** and **Type** fields determine the variables that are available for selection. For example, let's say that the email category is set to incident notification and that the email type is a digest, then the variables for selection are digest fields to accommodate the accumulation of multiple DLP incidents.

Here is an example Email Body HTML of each email template:

-   **Default template for Per incident approval notification**:

    ```
Dear ${respondent.first_name},

Your request "${end_user_response}" on the incident ${number} has been approved.

- Date protection team
    ```

-   **Per incident approval request cancellation notification**

    ```
Dear ${respondent.first_name},

Your request "${end_user_response}" on the DLP incident ${number} has been cancelled.

No action is required from you at this point. Data protection team will contact you for any further information required.

- Data protection team
    ```

-   **Default template for Due date notification**:

    ```
Dear ${target_user.name},

Following incidents require your response.

${due_days_table}

- Data protection team
    ```

-   **Default template for Per Incident user notification**:

    ```
Dear ${assigned_to.name},

DLP Incident ${number} is assigned to you.

Please review and submit your response.

- Data protection team
    ```

-   **Default template for User incident notification**:

    ```
Hello ${target_user.name},

You have ${total_number_of_incidents} incidents assigned to you currently that require your response. ${new_incidents_in_period} new incidents got assigned to you since the last email communication.

Nearest upcoming due date for responding to a critical incident is ${nearest_due_date_for_critical_severity_incidents}.

Please log in to the ${link_to_dlp_portal} and submit your response.

- Data protection team
    ```

-   **Default template for Escalation - Digest**:

    ```
Hi ${target_user.name},

The following data security incidents have been escalated to you due to lack of response from the assignees.

Please login to the incident response workspace to review the incidents and submit your response.

${overdue_table}

- Data protection team
    ```

-   **Default template for Escalation - Per Incident**:

    ```
Dear ${assigned_to.name},

Data security incident ${number} has been escalated to you.

Please review and submit your response or assign the incident back to the user.

- Data protection team
    ```

-   **Default template for Pending approval notification**:

    ```
Dear ${approver.first_name},

Your approval is required for a few requests on data security incidents.

Please login to the workspace here and review the requests.

- Data protection team
    ```

-   **Default template for Per incident pending approval notification**:

    ```
Dear ${Approver},

Your approval is required for the incident ${number} requested by the user ${respondent.first_name} ${respondent.last_name}.

Please visit this here to approve or reject the request.

- Data Protection Team
    ```

-   **Default template for Per incident rejection notification**:

    ```
Dear ${respondent.first_name} ${respondent.last_name},

This is to inform you that your request "${end_user_response}" for the DLP incident ${number} has been rejected.

Please review the incident here.

- Data protection team
    ```

-   **Default template for Per incident user response notification**:

    ```
Hi ${assigned_to.name},

This is to inform you that a response has been submitted for the DLP Incident ${number}.
    ```

-   **Default template for User response completion notification**:

    ```
Hello ${target_user.name},

This email is to inform you that users have submitted their response for ${new_incidents_in_period_user_response_completed} new incidents since the last email communication.

Please review the response for these incidents ${link_to_incidents_in_period_user_response_completed}.


    ```

</td></tr></tbody>
</table>    The following example shows the DLP Email Template with the target users defined as all recipients.

    ![Create and manage DLP email templates.](../image/dlp-email-template.png "Email template")

    The following example shows an email template with the subject "User incident notification" and a variable *new\_incidents\_in\_period*. The email body contains multiple variables that are added from the Select variables column.

    ![Email template with fields to select variables.](../image/dlp-email-templates-variables.png "Email template variables")

4.  Click **Submit**.


## Result

The end user receives a digest notification email with all the selected variable fields in the template.

**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](setup-response-due-date-rules.md)

[Create Approval Rules](configure-approval-rules.md)

[Create user instructions templates](create-and-manage-user-instructions-template-for-dlp-incidents.md)

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

