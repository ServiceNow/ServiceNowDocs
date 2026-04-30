---
title: Touchpoint home page
description: During the engagement lifecycle, customer success agents schedule regular touchpoints with customers to evaluate progress, provide feedback, and offer guidance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Using customer success, Customer success, Customer Success Management]
---

# Touchpoint home page

During the engagement lifecycle, customer success agents schedule regular touchpoints with customers to evaluate progress, provide feedback, and offer guidance.

Touchpoints enhance communication between customer success teams and customer throughout the engagement lifecycle. Regular touchpoints ensures that the internal and external teams are aligned on the objectives and outcomes of the engagement.

![Touchpoint home page](../image/customer-success-touchpoints.png)

The following options are available:

-   Discuss: Click **Discuss** to start a sidebar discussion about this touchpoint. In the popup window, select the participants who need to participate in the discussion, enter a brief message, and click **Start discussion**. A window appears with a link to the record for this touchpoint. Click **Open record** and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   Create success play: See [Create a success play](../task/account-lifecycle-create-success-play.md).
-   Close touchpoint: Select **Close touchpoint** option from the More Actions drop down menu. You are prompted to enter the mandatory fields. Click the **Edit** icon in the Touchpoint details panel, enter the mandatory fields and click **Save**. Click **Close touchpoint** after filling in the mandatory fields. Select the Closure code and Close notes and click **Close** to close the touchpoint.
-   Cancel touchpoint: Select the **Cancel touchpoint** option from the More Actions drop down menu. The Closure code is automatically updated to reflect the State change. Enter the Close notes and click **Cancel**. If all other mandatory fields have been filled in, you will see a confirmation message indicating that the touchpoint has been canceled. If any mandatory fields have not been filled in, click the **Edit** icon in the Touchpoint details panel, enter the mandatory fields and click **Save** to cancel the touchpoint.

The Touchpoint home page contains the following tabs:

-   Meetings
-   Emails
-   Success tasks

On the left pane, you can see the details of the account with which the touchpoint is associated. The details of the Touchpoint record are also displayed. Click on the pencil icon to modify the details and click **Save** to update the record.

## Meetings

This tab shows a list of upcoming touchpoint meetings and the ones that have already occurred. For each meeting listed on the page, the title, start and end date, meeting link, list of invitees, and the meeting state is displayed. Click **Add meeting** to schedule a new meeting. Enter the following details:

<table id="table_o2p_bch_rdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Meeting subject

</td><td>

Enter a description for the meeting.

</td></tr><tr><td>

State

</td><td>

This can be:-   Draft: A newly created meeting is in a Draft state. It will remain in this state till the status is updated to Scheduled. You can add invitees, meeting cadence, location, and other information when the status is updated.
-   Scheduled: A meeting in a Scheduled state is set for a specific date and time and with a list of invitees. A scheduled meeting can either be a recurring meeting or a one-time occurrence.
-   Completed: A meeting that has already been completed. Meetings in this state can be saved or recorded if required.

</td></tr><tr><td>

Meeting type

</td><td>

This field appears only when the State is set to Scheduled. This can be:-   Ad-hoc
-   Weekly Status
-   QBR
-   Renewal

</td></tr><tr><td>

Start date &amp; time

</td><td>

Enter the start date and time on which the meeting should be scheduled.The start date must be earlier than the end date.

</td></tr><tr><td>

End date &amp; time

</td><td>

Enter the end date and time for the meeting.-   The meeting duration cannot exceed 24 hours.
-   The Repeat until date must be later than the End date.

</td></tr><tr><td>

Invitees

</td><td>

Select the invitees for the meeting from the drop down list.

</td></tr><tr><td>

Cadence

</td><td>

Specify the cadence for the meeting. This can be:-   Biweekly
-   Daily
-   Monthly
-   Quarterly
-   Weekly

</td></tr><tr><td>

Repeat until

</td><td>

This field appears only if you select a value in the Cadence field. Specify the date till which the meeting cadence should be repeated. **Note:** By default, you can set up the meeting series for maximum period of 365 days. You can modify this value in the `sn_meeting_mgmt.meeting_series_repeat_limit` system property.

</td></tr><tr><td>

Virtual meeting

</td><td>

Select this checkbox to enable virtual meetings.

</td></tr><tr><td>

Video software

</td><td>

Select the virtual meeting provider software such as Zoom and Google Meet.**Note:** To enable virtual meetings, you must setup Zoom integration on your ServiceNow instance and update the user account details in the `sn_acct_lc.zoom_integration_user_id` system property.

</td></tr><tr><td>

Meeting link

</td><td>

This field is automatically populated based on your selection in the Video software field.

</td></tr><tr><td>

Locations

</td><td>

Select one or more locations from the drop down list.

</td></tr><tr><td>

Agenda

</td><td>

Enter the agenda for the meeting.

</td></tr><tr><td>

Internal notes

</td><td>

Enter any internal notes for the meeting.

</td></tr><tr><td>

Attachments

</td><td>

Click **Add file** to upload one or more attachments with the meeting invite.

</td></tr></tbody>
</table>Click **Create** to save and create the meeting. The scheduled meeting is displayed in the Meetings page. An email invite is sent to all the invitees for the meeting. Based on the Cadence you specified, the scheduled meeting series will appear on the Meetings page.

**Note:**

-   Meeting invites are sent only for meetings in the **Scheduled** state.
-   If a meeting or a meeting series is canceled, the email indicating that it is canceled is sent to the meeting invitees.
-   If the meeting details such as the time or location are changed, an updated invite is automatically sent to all the meeting invitees.
-   The Start and End dates for a meeting series should not be later than **Repeat until** date.
-   If a meeting series is extended, new meeting occurrences must be scheduled for future dates. Any updates to a meeting series impacts only upcoming meetings.
-   If a meeting series is rescheduled to an earlier date, all future occurrences will be canceled.
-   When a meeting is marked as completed or notes are updated, meeting notes are sent to all participants.
-   A single meeting occurrence can be canceled.

You can do the following:

-   Click on a meeting to modify the details. If the meeting is part of a series, you can either edit one of the occurrences or click **Edit series** to update the entire meeting series.
-   Click **Cancel occurrence** to cancel the selected meeting or click **Cancel series** to cancel the entire meeting series.
-   Click **Save** to update the meeting or meeting series.
-   To close a touchpoint, select **Close touchpoint** and enter the Closure code and the Close notes. Select one of the closure codes and click **Close**.
    -   Addressed
    -   Unaddressed
    -   Canceled
-   To cancel a touchpoint, select **Cancel touchpoint**. The Closure code is set to Canceled and the State field is updated. When a touchpoint is canceled:
    -   Existing scheduled meetings are still available, but you cannot schedule any new meetings.
    -   Emails and success tasks cannot be added for the closed or canceled touchpoint.

## Emails

In this tab, the customer success agent can send email to the users specified in the Contact field in the Touchpoint. By default, the email header will be auto populated with the email address of the Contact and the subject of the account.

You can:

-   Click the `Expand email` icon to expand the email. You add or delete the email ids and update the subject if required.
-   Click the `Flag` icon to mark this email as important.
-   Click the `Open draft in a tab` icon to view the email in a new tab. Click the `View drafts` icon and then **Manage draft** to view draft versions of the email. Select a draft from the list, click **Apply** and use it for your email.
-   While writing an email, if you want to display the last saved draft in the Compose section, you must setup the Email composer \(mini\). See [Email composer \(mini\) UIB setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-email-client-mini-composer-connected/uib-setup) for details.
-   Select the Touchpoint Email Template in the right panel and click **Apply Template**. Your email will be formatted as per the touchpoint template that you have applied.
-   Click **Attach file**. You can attach a file either from your computer or from the touchpoint record. Select the file to be attached and click **Add** to attach the file with your email.

Click **Send email**. Navigate to the `Emails` tab to see the email you have sent. You can also view the list of emails sorted in descending order of sent date. You can use the Search option to view emails meeting a specific criteria, filter the list by the type of emails, flagged emails, and create additional filter sets. You can also view the sent and received emails in the Emails under the Related Items section.

## Success tasks

You can view the success tasks associated with this touchpoint.

1.  Click **New** to create a new success task for this touchpoint. The Create new success task page is displayed. See [Create a success case task](../task/account-lifecycle-create-success-case-task.md) for details.
2.  Enter the details on this page and click **Save**. The newly created success task now appears on the `Success tasks` page.

