---
title: Touchpoint home page
description: During the engagement lifecycle, customer success agents schedule regular touchpoints with customers to evaluate progress, provide feedback, and offer guidance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Customer success, Use, Customer Success Management]
---

# Touchpoint home page

During the engagement lifecycle, customer success agents schedule regular touchpoints with customers to evaluate progress, provide feedback, and offer guidance.

Touchpoints enhance communication between customer success teams and customer throughout the engagement lifecycle. Regular touchpoints ensure that the internal and external teams are aligned on the objectives and outcomes of the engagement.

![Touchpoint home page](../image/customer-success-touchpoints.png)

The following options are available:

-   Discuss: Select **Discuss** to start a sidebar discussion about this touchpoint. In the pop-up window, select the participants who must participate in the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record for this touchpoint. Select **Open record** and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   Create success play: See [Create a success play](../task/account-lifecycle-create-success-play.md).
-   Close touchpoint: Select **Close touchpoint** option from the More Actions drop down menu. You’re prompted to enter the required fields. Select the **Edit** icon in the Touchpoint details panel, enter the required fields and select **Save**. Select **Close touchpoint** after filling in the required fields. Select the Closure code and Close notes and select **Close** to close the touchpoint.
-   Cancel touchpoint: Select the **Cancel touchpoint** option from the More Actions drop down menu. The Closure code is automatically updated to reflect the State change. Enter the Close notes and select **Cancel**. If all other required fields have been filled in, you see a confirmation message indicating that the touchpoint has been canceled. If any required fields haven’t been filled in, select the **Edit** icon in the Touchpoint details panel, enter the required fields and select **Save** to cancel the touchpoint.

If the touchpoint is deleted, all the associated meetings of the touchpoint are deleted.

The Touchpoint home page contains the following tabs:

-   Meetings
-   Emails
-   Success tasks

On the left pane, you can see the details of the account with which the touchpoint is associated. The details of the Touchpoint record are also displayed. Select the pencil icon to modify the details and select **Save** to update the record.

## Meetings

This tab shows a list of upcoming touchpoint meetings and the ones that have already occurred. For each meeting listed on the page, the title, start and end date, meeting link, list of invitees, and the meeting state is displayed. Select **Add meeting** to schedule a new meeting. Enter the following details:

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

This can be:-   Draft: A newly created meeting is in a Draft state. It remains in this state until the status is updated to Scheduled. You can add invitees, meeting cadence, location, and other information when the status is updated.
-   Scheduled: A meeting in a Scheduled state is set for a specific date and time and with a list of invitees. A scheduled meeting can either be a recurring meeting or a one-time occurrence.
-   Completed: A meeting that has already been completed. Meetings in this state can be saved or recorded if necessary.

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

Enter the end date and time for the meeting.-   The meeting duration can’t exceed 24 hours.
-   The Repeat until date must be later than the End date.

</td></tr><tr><td>

Invitees

</td><td>

Select the invitees for the meeting from the drop-down list.

</td></tr><tr><td>

Cadence

</td><td>

Specify the cadence for the meeting. This can be:-   Twice a week
-   Daily
-   Monthly
-   Quarterly
-   Weekly

</td></tr><tr><td>

Repeat until

</td><td>

This field appears only if you select a value in the Cadence field. Specify the date until which the meeting cadence should be repeated. **Note:** By default, you can set up the meeting series for maximum period of 365 days. You can modify this value in the `sn_meeting_mgmt.meeting_series_repeat_limit` system property.

</td></tr><tr><td>

Virtual meeting

</td><td>

Select this check box to enable virtual meetings.

</td></tr><tr><td>

Video software

</td><td>

Select your virtual meeting provider such as Zoom or Google Meet from the list.

</td></tr><tr><td>

Meeting link

</td><td>

This field is automatically populated if you select Zoom in the Video software field. For details on setting up and configuring Zoom, see [Configure Zoom to create a touchpoint meeting summary](../task/account-lifecycle-config-zoom-sum.md).

</td></tr><tr><td>

Locations

</td><td>

Select one or more locations from the drop-down list.

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

Select **Add file** to upload one or more attachments with the meeting invite.

</td></tr></tbody>
</table>Select **Create** to save and create the meeting. The scheduled meeting is displayed in the Meetings page. An email invite is sent to all the invitees for the meeting. Based on the Cadence you specified, the scheduled meeting series will appear on the Meetings page.

**Note:**

-   Meeting invites are sent only for meetings in the **Scheduled** state.
-   If a meeting or a meeting series is canceled, the email indicating that it’s canceled is sent to the meeting invitees.
-   If the meeting details such as the time or location are changed, an updated invite is automatically sent to all the meeting invitees.
-   The Start and End dates for a meeting series shouldn’t be later than **Repeat until** date.
-   If a meeting series is extended, new meeting occurrences must be scheduled for future dates. Any updates to a meeting series impact only upcoming meetings.
-   If a meeting series is rescheduled to an earlier date, all future occurrences are canceled.
-   When a meeting is marked as completed or notes are updated, meeting notes are sent to all participants.
-   A single meeting occurrence can be canceled.

You can do the following:

-   Select a meeting to modify the details. If the meeting is part of a series, you can either edit one of the occurrences or select **Edit series** to update the entire meeting series.
-   Select **Cancel occurrence** to cancel the selected meeting or select **Cancel series** to cancel the entire meeting series.
-   Select **Save** to update the meeting or meeting series.
-   To close a touchpoint, select **Close touchpoint** and enter the Closure code and the Close notes. Select one of the closure codes and select **Close**.
    -   Addressed
    -   Unaddressed
    -   Canceled
-   To cancel a touchpoint, select **Cancel touchpoint**. The Closure code is set to Canceled and the State field is updated. When a touchpoint is canceled:
    -   Existing scheduled meetings are still available, but you can’t schedule any new meetings.
    -   Emails and success tasks can’t be added for the closed or canceled touchpoint.

**Important:** The following changes have been made in the Touchpoint tables in the Zurich release:

<table id="table_rp5_knl_zfc"><thead><tr><th>

Table name

</th><th>

Field name

</th><th>

State

</th></tr></thead><tbody><tr><td>

Meeting Details \(sn\_meeting\_mgmt\_meeting\_details\)

</td><td>

Meeting password

</td><td>

Added

</td></tr><tr><td>

Virtual Meeting Details \(sn\_meeting\_mgmt\_virtual\_meeting\_details\)

</td><td>

-   Meeting Instance ID
-   Meeting actual start date

</td><td>

Added

</td></tr><tr><td>

Meeting Details \(sn\_meeting\_mgmt\_meeting\_details\)

</td><td>

-   Meeting link
-   Meeting password

</td><td>

Deprecated

</td></tr></tbody>
</table>Run the **Migrate Meeting Fields** script to migrate the Meeting Id, Meeting link and Meeting password fields data from the Virtual Meeting Details table to the Meeting Details table.

## Emails

In this tab, the customer success agent can send email to the users specified in the Contact field in the Touchpoint. By default, the email header is auto populated with the email address of the Contact and the subject of the account.

You can:

-   Select the `Expand email` icon to expand the email. You add or delete the email ids and update the subject if necessary.
-   Select the `Flag` icon to mark this email as important.
-   Select the `Open draft in a tab` icon to view the email in a new tab. Select the `View drafts` icon and then **Manage draft** to view draft versions of the email. Select a draft from the list, select **Apply** and use it for your email.
-   While writing an email, if you want to display the last saved draft in the Compose section, you must set up the Email composer \(mini\). See [Email composer \(mini\) UIB setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-email-client-mini-composer-connected/uib-setup) for the details.
-   Select the Touchpoint Email Template in the right panel and select **Apply Template**. Your email is formatted according to the touchpoint template that you have applied.
-   Select **Attach file**. You can attach a file either from your computer or from the touchpoint record. Select the file to be attached and select **Add** to attach the file with your email.

Select **Send email**. Navigate to the `Emails` tab to see the email you have sent. You can also view the list of emails sorted in descending order of sent date. You can use the Search option to view emails meeting a specific criteria, filter the list by the type of emails, flagged emails, and create additional filter sets. You can also view the sent and received emails in the Emails under the Related Items section.

## Success tasks

You can view the success tasks associated with this touchpoint.

1.  Select **New** to create a new success task for this touchpoint. The Create a new success task page is displayed.
2.  Enter the details on this page and select **Save**. The newly created success task now appears on the `Success tasks` page.

-   **[Touchpoint planner](account-lifecycle-touchpoint-planner.md)**  
The touchpoint planner shows a calendar view of different touchpoints across all accounts associated with the customer success manager.
-   **[Configure Zoom to create a touchpoint meeting summary](../task/account-lifecycle-config-zoom-sum.md)**  
Set up the Zoom spoke integration and the bi-directional web hook to generate summaries for virtual touchpoint meetings.

**Parent Topic:**[Customer success](account-lifecycle-use-cust-success.md)

