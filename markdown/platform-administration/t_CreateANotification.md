---
title: Create an email notification
description: Create an email notification specifying when to send it, who receives it, what it contains, and if it can be delivered in an email digest.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 20
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email notification

Create an email notification specifying when to send it, who receives it, what it contains, and if it can be delivered in an email digest.

## Before you begin

Role required: admin

Consider the following items when you create or update a notification:

-   Your notification recipients must be active users and have a valid email address defined.

    ServiceNow users or members of groups must be defined as active users in the User \[sys\_user\] table. They must also have a valid email address defined for their primary channel \(device\) in the Notification Device \[cmn\_notif\_device\] table. If users don’t have an active profile and a valid email address, the notifications won’t be received.

-   Your notification recipients must have the appropriate notification preferences enabled.

    If the notification is subscribable, each ServiceNow user or group member must have the notification and channels \(devices\) for the notification enabled in their [notification preferences](../concept/user-notification-preferences.md). Admins can impersonate users to review and configure their notification preferences.

-   To have your email notification also send as an SMS notification, recipients must subscribe to the notification on an SMS channel. For more information on creating an SMS channel, see [Create notification channels](create-channel.md).
-   After you create or update the notification, use the **Preview Notification** option to examine it. For example, you can test links that you may have added and verify the notification recipients. For details, see [Preview email notifications](t_PreviewingNotifications.md).
-   For information on operators available for filters and queries, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## About this task

Watch the video to learn about the actions that the instance can take in response to messages from users and shows how to create or modify email notifications to users.

Configure inbound email actions and email notifications 

Use the following tabs in the Notification form to configure an email notification:

-   **When to send** — Conditions required to send the notification.
-   **Who will receive** — Recipients of the notification.
-   **What it will contain** — Contents of the notification.
-   **What Digest will contain** — Contents of the [email digest](../concept/email-digests.md) if the notification can be delivered in a digest.

**Note:** If you don’t see all the fields on the form, switch to the **Advanced** view.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Select **New**.

3.  Fill in the fields at the top of the Notification form, as appropriate.

<table id="table_ckh_ytp_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the email notification. Descriptive names help identify the purpose of the email notification. For example, Incident Opened &amp; Unassigned.

</td></tr><tr><td>

Table

</td><td>

Select the database table to link the notification to, for example Incident \[incident\].**Important:** Don’t select the Task \[task\] table. This table is for extending other tables. Notifications that run on the Task table directly aren’t supported.

 **Note:** Only tables and database views that are in the same application scope appear in the list.

</td></tr><tr><td>

Type

</td><td>

Select the type of notification that you’re creating: EMAIL or Meeting Invitation.

</td></tr><tr><td>

Active

</td><td>

Select the check box to enable the email notification.

</td></tr><tr id="Category"><td>

Category

</td><td>

Select the category to which this notification belongs. A category identifies and groups related notifications. This notification, if active and subscribable, is listed in the selected **Category** in the notification preferences for each user \(**Notifications** tab in the System Settings window\). **Note:** Don’t leave the category as **Uncategorized**, as users may not be able to find the notification in their list of notifications.

 If you need a new category, see [Create notification categories](create-notification-categories.md).

</td></tr><tr><td>

Allow Digest

</td><td>

Select the check box if an [email digest](../concept/email-digests.md) is to be created for the notification. If selected, the **What Digest will contain** tab is displayed for creating the digest content.

</td></tr><tr><td>

Description

</td><td>

Type a description for this notification.

</td></tr></tbody>
</table>4.  Fill in the fields on the **When to send** tab.

    **Note:** If the same trigger generates multiple notifications, the system only sends one notification. The system considers all other notifications, even if they have a different subject and body, as duplicates. The Ignore Duplicates business rule controls this functionality.

<table id="table_ibc_3pb_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Send when

</td><td>

Select under what condition that the notification is sent: -   When a record is inserted or updated
-   When a particular event is fired
-   When [Notification step](https://www.servicenow.com/docs/access?context=trigger-notification-action-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) in Flow Designer


</td></tr><tr><td>

Weight

</td><td>

\[Required\] Set a numerical value for the notification priority relative to duplicate notifications.Notifications that have the same target table and recipients are considered duplicates if the weights are different. If weights are same, an additional evaluation is done to check if the subject and the body \(excluding watermark\) are same to qualify as duplicate notification. When there are duplicate notifications, the system only sends the notification with the highest weight. All other notifications are moved from the Outbox to the Skipped mailbox. The default value 0 causes the system to send the notification \(assuming the conditions are met\).

 For example, suppose that a service desk agent adds a comment to an incident and shortly thereafter closes it. By default, these actions trigger both the Incident commented and Incident Closed notifications.

 However, both notifications are from the Incident table and also notify the incident caller. The system only sends the notification with the highest weight, which in this case is the Incident Closed notification.

 **Note:** The SMTP Sender scheduled job determines how often to send email. By default, this job runs every minute.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions under which this notification is sent. For example, select **Priority** &gt; **greater than** &gt; **3 - Moderate** to send the notification only for High and Critical priority incidents.

</td></tr><tr><td>

Inserted

</td><td>

Select the check box to enable email notification when a record is inserted. This field appears when you set the **Send when** field to **Record inserted or updated**.

</td></tr><tr><td>

Updated

</td><td>

Select the check box to enable email notification when a record is updated. This field appears when you set the **Send when** field to **Record inserted or updated**.

</td></tr><tr><td>

Event name

</td><td>

Select the event that triggers this notification. This field appears when you set the **Send when** field to **Event is fired**.

</td></tr><tr id="AdvancedConditions"><td>

Advanced condition

</td><td>

Create a script to perform certain actions, like sending a notification based on the current email record, changing field values, or changing system properties. [The advanced condition](../concept/c_OptSpecifyingAdvancedCond.md) script must return **true** or set a global answer variable to **true** to send the notification.

 The advanced condition script uses the following global variables:

 -   **current**: Contains the current record from the table to which the notification is linked.
-   **event**: Contains the event that triggered the notification.
 **Note:** The **Advanced condition** field is evaluated in addition to other conditions that you set on the notification. Both the condition and advanced condition must evaluate to true to send the notification.

</td></tr></tbody>
</table>5.  Fill in the fields on the **Who will receive** tab.

    The following example shows the default view of the tab. The advanced view contains additional fields \(see table\).

    **Tip:** Consider limiting the recipient list of any notification to 1000 users. By default, if a notification has more than 100 intended recipients, the system creates multiple notification messages with up to 100 recipients each. If you want to change the recipient limit, set the system property **glide.email.smtp.max\_recipients**.

<table id="table_oh2_krb_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Users

</td><td>

Select the users that you want to receive the email notification. You can search for users with the reference lookup icon or manually add their email addresses. This list of users is static.

</td></tr><tr><td>

Users/groups in fields

</td><td>

Select fields from the target record that reference the User \[sys\_user\] or Group \[sys\_user\_group\] tables. The system sends the notification to users or groups in each field that you select. For example, if a notification uses the Incident \[incident\] table, you can select the **Opened by** field to send the notification to users or groups who opened the incident. This list of users or groups is variable and depends upon the values of the associated task record. You can also select a field that includes an email address string to send a notification to that address.**Note:** You can dot-walk to values in reference fields by selecting the plus sign in the field selector and then selecting the related field.

If you address the notification to a user with an inactive record in the User \[sys\_user\] table, the system doesn’t send the notification to that user.

</td></tr><tr><td>

Groups

</td><td>

Select the groups that you want to receive the email notification from. You can search for groups with the reference lookup icon or by manually entering the group name. This list of groups is static.**Note:** Group members receive individual notifications only if **Include members** is selected in the group record.

</td></tr><tr><td>

Exclude delegates

</td><td>

Select this option to help prevent the instance from sending email notifications to delegates of the users and members of the groups you selected.

</td></tr><tr><td>

Send to event creator

</td><td>

Select this check box to send the notification to the person who performed the action that started the notification process if the person is also a recipient. If the event creator isn’t specified in one of the recipient fields, the event creator doesn’t receive a notification regardless of the setting in this field. For new notifications, this option is selected by default.

 If you want to know why you may not be receiving certain email notifications, see the blog post [Troubleshooting email notifications- Send to the Event Creator](https://community.servicenow.com/community?id=community_blog&sys_id=c8edaae9dbd0dbc01dcaf3231f96199b) by a ServiceNow Technical Support Engineer in the ServiceNow Community.

</td></tr><tr><td>

Event parm 1 contains recipient

</td><td>

Select this check box if the event parameter 1 contains one or more notification recipients \(in a comma separated-list\). This field is visible only when the **Send when** field is set to **Event is fired**.

</td></tr><tr><td>

Event parm 2 contains recipient

</td><td>

Select this check box if the event parameter 2 contains one or more notification recipients \(in a comma-separated list\). This field is visible only when the **Send when** field is set to **Event is fired**.

</td></tr><tr><td id="subscribable">

Subscribable

</td><td>

Select this check box to enable all users to subscribe to this notification. See [Subscription-based notifications](../concept/c_SubscriptionBasedNotifications.md) for more information.**Note:** If the record contains sensitive or protected data, consider restricting the recipient list only to those users and groups who normally have access to it, and don’t enable the **Subscribable** option. You can also configure your notification content so that private or sensitive data isn’t exposed. For example, you could insert a link back to the associated record, so that details aren’t revealed in the notification.

</td></tr></tbody>
</table>    The system doesn’t exclude recipients based on access controls. Recipients can receive email about records that they can’t normally access from the user interface. For example, requesters can receive email about incidents and catalog requests opened on their behalf even though they normally don’t have access to these records. If a notification includes the record details, verify that all recipients need these details.

    **Note:** By default, the system doesn’t send email notifications to itself. For example, an email notification from instanceABC@service-now.com doesn’t send to instanceABC@service-now.com. The system helps prevent this behavior to avoid looping.

6.  Fill in the fields on the **What it will contain** tab.

    The following example shows the default view of the tab. The advanced view contains additional fields \(see table\).

<table id="table_g21_dvb_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email template

</td><td>

If you want to reuse existing content, select an email template to add content to the email notification. You can only select an email template that meets one of the following conditions:-   shares the same scope and table as the notification
-   shares the same scope but has no specified table
-   shares the same table and is in the global scope


</td></tr><tr><td>

Subject

</td><td>

Enter the subject line for the email message. The subject can include variables from the **Select variables** column.

 If empty, the system uses the **Subject** value from the **Email template**. If you enter a value in this field, it overrides the template value.

 If your recipients subscribe to the email notification on an SMS channel, then the system sends the email notification subject as an SMS message. To send a different SMS message, fill in the **SMS alternate** field on the email template form or the email notification form.

</td></tr><tr><td>

Message HTML

</td><td>

Enter the content of the email notification message. The message can include variables from the **Select variables** column.

 Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table such as an incident short description or comments and work notes.

 The **Message HTML** field is visible only if you set the content type to **HTML and plain text** or **HTML only**.

 If empty, the system uses the **Message HTML** value from the **Email template**. If you enter a value in this field, it overrides the template value.

 To avoid adding extra `<p>` and `<div>` elements to your email notifications, see the blog post [Extra line spacing with paragraph tags in email client](https://community.servicenow.com/community?id=community_blog&sys_id=d0ad22a9dbd0dbc01dcaf3231f9619b6) by a ServiceNow employee in the ServiceNow Community.

</td></tr><tr><td>

SMS alternate

</td><td>

Enter the notification message to send to an SMS device. The SMS alternate message is limited to 140 characters.

 If empty, the system uses the **SMS alternate** value from the **Email template**. If you enter a value in this field, it overrides the template value.

 If you don't fill in the **SMS alternate** field on this form or the email template, then the system uses the email notification subject as the SMS message.

</td></tr><tr><td>

Importance

</td><td>

Set the importance of the email message to low or high.

</td></tr><tr><td>

Content type

</td><td>

Select the content type for the email notification:-   HTML and plain text
-   HTML only
-   Plain text only
By default, **HTML only** is enabled.

</td></tr><tr><td>

Include attachments

</td><td>

Select this check box to send all attachments from the triggering record as email attachments.

</td></tr><tr><td>

Omit watermark

</td><td>

Use this check box to apply or remove the watermark attached to each email. If the email doesn’t contain a watermark, the system reviews the conditions of the inbound actions to create or update task records. For more information, and an alternative way to hide watermarks, see [Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md).

</td></tr><tr><td>

Message Text

</td><td>

Enter the notification message to send in plain text. This field appears when you set the content type to **HTML and plain text** or **Plain text only**.

 If empty, the system uses the **Message Text** value from the **Email template**. If you enter a value in this field, it overrides the template value.

</td></tr><tr><td>

From

</td><td>

Enter the email address that you want the email notification to use in the From field. For example, helpdesk@yourcompany.com. The email must be in a valid format, otherwise a notification message appears near the field.

 Changing this address may require an advanced email setup such as [enabling email forwarding](../../reference-pages/task/t_ConfAltEmailUsgOwnSMTP.md), for example when using Sender Policy Framework \(SPF\) records for spam detection.

</td></tr><tr><td>

Reply to

</td><td>

Enter the email address that you want people to use when replying to the email notification. For example, helpdesk@yourcompany.com. The email must be in a valid format, otherwise a notification message appears near the field. You can add no more than one email address in this field.

 Changing this address requires an advanced email setup such as [enabling email forwarding](../../reference-pages/task/t_ConfAltEmailUsgOwnSMTP.md).

</td></tr><tr><td>

Push message only

</td><td>

Select this option to send this notification only as a push notification to a mobile device. The [Push Notification](../concept/c_PushNotifications.md) feature must be active.

</td></tr><tr><td>

Push messages

</td><td>

Associate one or more push messages with this notification. The [Push Notification](../concept/c_PushNotifications.md) feature must be active.**Note:** The push message and notification must be for the same table.

</td></tr></tbody>
</table>7.  If you selected the **Allow Digest**check box, fill in the fields on the **What Digest will contain** tab to create the email digest content for the notification.

    The following example shows the default view of the tab. The advanced view contains additional fields \(see table\).

<table id="table_zl2_13b_x1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Digest Template

</td><td>

If you want to reuse existing content, such as headers or footers, select an email template to add content to the email digest.

</td></tr><tr><td>

Digest Subject

</td><td>

Enter the subject line for the email digest. The subject can include variables from the **Select variables** column.

 If empty, the system uses the **Subject** value from the **Email template**. If you enter a value in this field, it overrides the template value.

</td></tr><tr><td>

Digest HTML

</td><td>

Enter the recurring content for the email digest. The digest content can include variables from the **Select variables** column.

 Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table such as an incident short description or comments and work notes.

 To avoid adding extra `<p>` and `<div>` elements to your email digest, see the blog post [Extra line spacing with paragraph tags in email client](https://community.servicenow.com/community/blogs/blog/2014/12/12/extra-line-spacing-with-p-tags-in-email-client) by a ServiceNow employee in the ServiceNow Community.

</td></tr><tr><td>

Digest Separator \(HTML\)

</td><td>

Use the line to separate each item summarized in the digest.

</td></tr><tr><td>

Digest From

</td><td>

Enter the email address to be used in the From field of the email digest. For example, helpdesk@yourcompany.com. The email address must be in a valid format, otherwise a notification message appears near the field.

 Changing this address requires an advanced email setup such as [enabling email forwarding](../../reference-pages/task/t_ConfAltEmailUsgOwnSMTP.md).

</td></tr><tr><td>

Digest Reply To

</td><td>

Enter the email address that you want people to use when replying to the email digest. For example, helpdesk@yourcompany.com. The email must be in a valid format, otherwise a notification message appears near the field.

 Changing this address requires an advanced email setup such as [enabling email forwarding](../../reference-pages/task/t_ConfAltEmailUsgOwnSMTP.md).

</td></tr><tr><td>

Digest Text

</td><td>

Enter the recurring content of the email digest to send in plain text. This field appears when you set the content type to **HTML and plain text** or **Plain text only**.

</td></tr><tr><td>

Digest Separator \(text\)

</td><td>

\[Optional\] Use the dash character as a line to separate each item summarized in the digest. This field appears when you set the content type to **HTML and plain text** or **Plain text only**.

</td></tr></tbody>
</table>    When you save or update the notification, the [email **Digest**option is available for the notification](enable-email-digest.md) in the notification settings of your users.

8.  When you finish creating the notification, select **Submit** or, if you’re done modifying the notification, select **Update**.


## What to do next

Use the **Preview Notification** option to [check your notification](t_PreviewingNotifications.md), for example, you can see:

-   How the **Subject** and **Message** fields are displayed.
-   Which users will or won’t receive the notification, including the reasons why the users won’t receive it.

-   **[Convert legacy email notifications to rich HTML](t_ConvEmailNotifToRichHTML.md)**  
By default, new email notifications are created in the rich HTML format. But you can also convert legacy notifications to rich HTML.
-   **[Control visibility to email records generated by notifications](control-visibility-emails.md)**  
Define conditions that restrict read access to target email records containing sensitive information.
-   **[Advanced conditions for email notifications](../concept/c_OptSpecifyingAdvancedCond.md)**  
Use an advanced condition to send a notification based on the current email record, changing field values, or system properties.
-   **[Edit HTML content in an email notification](t_EditTheHTMLOfAnEmailNotif.md)**  
For added control over the content of an email notification, you can edit the underlying HTML.
-   **[Document attachments on an email notification](../concept/c_AttachingDocsToANotification.md)**  
You can attach documents and reports to email notifications by scripting or linking to the sys ID of the record.
-   **[Line breaks in email notifications and rich HTML](../concept/c_HandlingLineBreaks.md)**  
Rich HTML provides additional control over line breaks in your email notifications and templates.
-   **[Preview email notifications](t_PreviewingNotifications.md)**  
You can preview what notifications look like before you actually enable the instance to send them.
-   **[Time zone for email notifications](../concept/c_SpecifyingTheTimeZone.md)**  
A system property controls the time zone that the instance uses for the date and time stamp of a message.
-   **[Specify alternative outbound email addresses for notifications](t_SpecAltOutEmailAddr.md)**  
By default, the system sends all outbound email notifications from the default email address of the instance, but you can specify an alternative address.
-   **[Specify an outbound email address for a particular language](t_SpecOutboundEmailAddLang.md)**  
You can specify a different email address for each language your instance supports.
-   **[Notification variables](../concept/notification-variables.md)**  
Use notification variables to display dynamic information in the body of a notification such as a field value, a link to a record, or a link to system preferences.
-   **[Links to records in email notifications](../concept/c_EnablingLinksToServiceNowRecords.md)**  
Adding the **$\{URI\}** parameter to an outbound email body or template creates a link to a specific record.
-   **[Email unsubscribe links](../concept/email-unsubscribe.md)**  
Administrators can enable your users to stop receiving particular email messages by adding unsubscribe links to notifications.
-   **[Scripting for email notifications](../../../script/server-scripting/concept/c_ScriptingForEmailNotifications.md)**  
Email scripts allow for business rule-like scripting within an outbound email message.
-   **[Baseline email notifications](../../reference-pages/reference/r_BaselineEmailNotifications.md)**  
The baseline system provides several email notifications.
-   **[Notification example: notify an assignment group of updates to Priority 1 Incidents](t_Ex4Priority1IncUpdateNotif.md)**  
Notify users by email when there are updates to high priority incidents.
-   **[Notification example: notify task assignees](t_NotificationExAssignmentNotif.md)**  
Notify users who are assigned a Task \[task\] record.

**Parent Topic:**[Email and SMS notifications](../concept/c_EmailNotifications.md)

**Related topics**  


[Create notification categories](create-notification-categories.md)

[Email templates](../concept/c_EmailTemplates.md)

[Email layouts](../concept/email-layouts.md)

[Email retention](../concept/email-retention.md)

[Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md)

[Parse an email thread](parse-email.md)

[Email digests](../concept/email-digests.md)

[Domain separation and Notifications](../concept/domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](../concept/troubleshooting-notification-emails.md)

