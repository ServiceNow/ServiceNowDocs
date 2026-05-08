---
title: Advanced email properties
description: Use advanced email properties to fine-tune the way your instance sends or receives email.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Email properties, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Advanced email properties

Use advanced email properties to fine-tune the way your instance sends or receives email.

Add these properties to the System Property \[sys\_properties\] table before they can be used to overwrite the defaults.

-   **__com.glide.email.max\_read__**

    Specifies the maximum number of emails a POP3 reader should process concurrently.

    -   Type: integer
    -   Default value: 20
-   **__com.snc.on\_call\_rotation.reminders.showtz__**

    Specifies whether to show a user's time zone.

    -   Type: true \| false
    -   Default value: false
-   **__glide.cms.use\_email\_override\_url__**

    Forces the system to use the **glide.email.override.url** property, rather than the **glide.servlet.uri** property, when a notification has a link to a CMS page in an instance.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **__glide.email\_address\_filter.max\_domains__**

    Sets the maximum number of domains that can be associated with a single email address filter.

    -   Type: integer
    -   Default value: 100
-   **__glide.email\_address\_filter.max\_exceptions__**

    Sets the maximum number of exceptions that can be associated with a single email address filter.

    -   Type: integer
    -   Default value: 1000
-   **__glide.email.allow\_duplicate\_message\_ids__**

    Allows storing of emails with duplicate message IDs and adds error message "Duplicate message-id encountered, prevented loop."

    -   Type: true \| false
    -   Default value: false
-   **__glide.email.append.timezone__**

    Appends the user time zone to all date and time values in outbound email messages \(for example, 2018-07-02 04:01:14 PST\). The time zone does not show if the system property **glide.sys.time\_format** does not have a "z" value. For more information on configuring the time zone in email notifications, see [Time zone for email notifications](../../notification/concept/c_SpecifyingTheTimeZone.md).

    -   Type: true \| false
    -   Default: false
-   **__glide.email.email\_client.check\_attachment\_availability__**

    Enables a system scan of each file that a user attaches to an email draft in the email client. If a file is found to be infected with a virus, the user can't send the email with the attached file. The user must remove the attachment to send the email.

    -   Type: true \| false
    -   Default value: true
-   **__glide.email.email\_with\_no\_target\_visible\_to\_all__**

    Email that is missing a target record or whose target record is the email are made visible to any user regardless of their roles. By turning this property to false, the user is restricted unless they sent in the record or have an admin role.

    -   Type: true \| false
    -   Value: true
-   **__glide.email.inbound.calendar\_behavior__**

    Specifies how the system stores calendar data, such as an invitation or an invitation response. Enter one of these options \(not case sensitive\):

    -   Attach: Store the calendar data as an attachment on the associated record, such as the incident or change that triggers an invitation.
    -   Ignore: Discard the calendar data.
    -   Inline: Store the calendar data as text in the email Body field.
    -   Type: string
    -   Default value: Attach
-   **__glide.email.inbound.check\_attachment\_availability__**

    Prevents users from downloading and using virus-infected files that are attached to inbound emails.

    The system detects infected files in an email by checking the ServiceNow virus header. If there are multiple email attachments, the system scans the files via Antivirus Scanning. All attachments that are found to be infected are made unavailable for use.

    -   Type: true \| false
    -   Default value: true
-   **__glide.email.inbound.convert\_html\_inline\_attachment\_references__**

    Specifies whether to convert inbound email HTML so email images appear in the email HTML body preview. The system displays broken cid \(content ID\) links in place of images received when this property is disabled. The format in which the system displays an email image depends on the property setting at the time the email is received, not the current property setting.

    -   Type: true \| false
    -   Default value: true
-   **__glide.email.inbound.generate.missing.html.part__**

    Enables the system to generate HTML text for inbound emails that contain only a plain text message.

    -   Type: true \| false
    -   Default value: true
-   **__glide.email.inbound.generate.missing.text.part__**

    Enables the system to generate plain text for inbound emails that contain only an HTML message.

    -   Type: true \| false
    -   Default value: true
-   **__glide.email.inbound.max\_attachment\_count__**

    Sets the maximum number of attachments allowed per inbound email.

    -   Type: integer
    -   Default value: 30
    -   Location: System Property \[sys\_properties\] table
-   **__glide.email.inbound.max\_body\_chars__**

    Sets the maximum body size in characters allowed per inbound email.

    -   Type: integer
    -   Default value: 524288
-   **__glide.email.inbound.max\_total\_attachment\_size\_bytes__**

    Sets the maximum total attachment size in bytes allowed per inbound email.

    -   Type: integer
    -   Default value: 18874368
    -   Location: System Property \[sys\_properties\] table
-   **__glide.email.inbound\_action\_set\_email\_ignored\_when\_user\_disabled__**

    Sets email to received ignored when met with one of two conditions:

    -   User account \(guest or any other account used to run the inbound email action\) is inactive.
    -   The user account \(guest or any other account used to run the inbound email action\) is locked out and the glide.pop3.process\_locked\_out property is set to false.
    -   Type: true \| false
    -   Default value: true
-   **__glide.email.mail\_to__**

    Specifies the email address for sending notifications that use the $\{mailto:\} variable.

    -   Type: string
    -   Default value: SMTP email address that is active by default
-   **__glide.email.name\_split__**

    Specifies the delimiter used between first and last names in an email address. For example, a delimiter of "." \(period\) in the email address john.smith@company.com tells the system to look for a user record for John Smith.

    -   Type: string
    -   Default value: period \(.\)
-   **__glide.email.notification.save\_when\_no\_recipients__**

    Controls whether a notification-generated `sys_mail` record is saved even if there are no recipients. Used along with other notification recipient logging properties, this property enables investigating problems with notifications.

    -   Type: true \| false
    -   Default value: false
-   **__glide.email.outbound.check\_attachment\_availability__**

    Prevents users from sending emails that contain virus-infected files.

    If an outbound email contains an attachment that was previously marked as infected via Antivirus Scanning, then the system doesn't send the email. An event is created to indicate that the email attachment is not available for use.

    -   Type: true \| false
    -   Default value: true
-   **__glide.email.outbound.header.auto\_submitted__**

    Stores the value used in the "Auto-submitted" outbound email header. Clear the property value to remove the "Auto-submitted" header from all outbound emails. Some spam filters flag auto-generated email as spam.

    -   Type: string
    -   Default value: auto-generated
-   **__glide.email.outbound.max\_attachment\_count__**

    Sets the maximum number of attachments allowed per outbound email.

    -   Type: integer
    -   Default value: 30
    -   Location: System Property \[sys\_properties\] table
-   **__glide.email.outbound.max\_body\_chars__**

    Sets the maximum body size in characters allowed per outbound email.

    -   Type: integer
    -   Default value: 524288
-   **__glide.email.outbound.max\_total\_attachment\_size\_bytes__**

    Sets the maximum total attachment size in bytes allowed per outbound email.

    -   Type: integer
    -   Default value: 18874368
    -   Location: System Property \[sys\_properties\] table
-   **__glide.email.override.url__**

    Sets the URL to use in emailed links in place of the instance URL. The URL should end with nav\_to.do. An example value is `https://servicenow.customerdomain.com/production.nav_to.do`. This property is suitable for customers who use custom redirect URLs for their instances.

    -   Type: string
    -   Default value: instance URL
-   **__glide.email.remove\_illegal\_address\_quotes__**

    Removes invalid quotation marks from an inbound email address, thus allowing the inbound email address to be accepted as valid. For example, when you set the property to true, the address "john.doe@example.com" is changed to john.doe@example.com. However, only addresses that are formatted as John Doe &lt;'john.doe@example.com'&gt; are removed entirely.

    -   Type: true \| false
    -   Default: false
-   **__glide.email.smtp.max\_recipients__**

    Specifies the maximum number of recipients the instance can list in the To:, CC:, BCC: lines combined for a single email notification. Notifications that would exceed this limit instead create duplicate email notifications addressed to a subset of the recipient list. Each email notification has the same maximum number of recipients.

    -   Type: integer
    -   Default value: 100
-   **__glide.email.smtp.max\_send__**

    Specifies how many emails to send through each new SMTP connection. If there are more emails to send than the specified value, the instance establishes a new SMTP connection.

    -   Type: integer
    -   Default value: 100
-   **__glide.email.smtp.max\_recipients\_overall__**

    Specifies the overall maximum number of recipients an email can be sent to. Specifies the maximum number of recipients the instance can list in the To:, CC:, BCC: lines for a single email notification.

    -   Type: integer
    -   Default value: 100000
-   **__glide.email\_system\_address\_filter.max\_address\_filters__**

    Sets the maximum number of email filters that can be associated with a single system address filter.

    -   Type: integer
    -   Default value: 100
-   **__glide.email.text\_plain.strip\_xhtml__**

    Converts the XML of both outbound and inbound emails that are shown in comments to plain text. If false, the system preserves the XML.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_logging__**

    Enables or disables logging all reasons a recipient was excluded. If set to true, the subsequent properties dealing with the exclusion of logging are enabled. If false, the properties are disabled. This property cannot suppress log messages generated by the **glide.email.test.user** property.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_logging.device\_inactive__**

    Logs recipients who are excluded because their chosen notification device record is marked as inactive.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_logging.device\_schedule__**

    Logs recipients who are excluded based on the **Schedule** field on the Notification Device \[cmn\_notif\_device\] record for their chosen notification device.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_logging.event\_creator__**

    Logs recipients who are excluded because they initiated the notification event, such as updating an incident record. The **Send to Event Creator** check box is then cleared on the notification record.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_logging.invalid\_email__**

    Logs recipients who are excluded because the email address for that user is invalid, for example the @ is missing, or empty.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_ logging.user\_calendar\_integration\_disabled__**

    Logs recipients of calendar invitations who are excluded. Recipients are excluded because the **Calendar Integration** field is set to **None** on the user record.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_logging.user\_inactive__**

    Logs recipients who are excluded because the **Active** check box is cleared on the user record.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.exclude\_ logging.user\_notification\_disabled__**

    Logs recipients who are excluded because the **Notification** field is set to **Disabled** on the user record.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_logging__**

    Enables or disables logging all reasons a recipient was included. If set to true, the subsequent properties dealing with the inclusion of logging are enabled. If false, the properties are disabled.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_logging.delegate__**

    Logs recipients who are included because they are delegates of another user.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_logging.event\_parm__**

    Logs recipients who are included because they are in the **parm1** or **parm2** fields of the event record.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_logging.recipient\_fields__**

    Logs recipients who are specified in the **Users/Groups in Field** field for the notification record. The recipient\_fields are fields in the target record that contain a recipient to add. For example, to include an incident assignee as a recipient, set the **Users/Groups in Field** field to **Assigned to**.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_ logging.recipient\_groups.group\_email__**

    Logs users who are included in a notification that is sent to a group. The property also logs users in the event **parm1** or **parm2** field.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_ logging.recipient\_groups.manager__**

    Logs recipients who manage a recipient group. The property also logs users in the event **parm1** or **parm2** field.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_ logging.recipient\_groups.membership__**

    Logs recipients who are part of a notification recipient group. The property also logs users in the event **parm1** or **parm2** field.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_logging.recipient\_users__**

    Logs recipients who are included via notification record’s **Users** field \(recipient\_users\).

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.recipient.include\_logging.subscription__**

    Logs recipients because they are subscribed via the user notification preferences.

    -   Type: true \| false
    -   Default value: true
-   **__glide.pop3.parse\_start__**

    Specifies the text that indicates the beginning of the email body section. The instance parses name:value pairs within this section to set or update field values when processing inbound email actions.

    -   Type: string
    -   Default value: none
-   **__glide.pop3.parse\_end__**

    Text indicating the end of the email body section where the instance should parse name:value pairs to update field values when processing inbound email actions.

    -   Type: string
    -   Default value: none
-   **__glide.smtp.dateformat__**

    Specify the date format to use for outgoing email notifications.

    -   Type: string
    -   Default value: date format listed in email sender's user record `[sys_user.date_format]`
-   **__glide.smtp.precedence\_bulk__**

    Specifies whether outbound email includes the header "Precedence: bulk". Some spam filters flag bulk email as spam. Set the value to **false** to remove this header from outbound email.

    -   Type: true \| false
    -   Default value: true
-   **__glide.smtp.send\_partial__**

    Splits outgoing email between valid and invalid recipients. The email is sent only to the valid recipients. A new email containing the invalid recipients is created in the **send-ready** state and attempts to send again.

    -   Type: true \| false
    -   Default value: true
-   **__glide.smtp.timeformat__**

    Specify the time format to use for outgoing email notifications.

    -   Type: string
    -   Default value: time format listed in email sender's user record `[sys_user.time_format]`
-   **__glide.ui.activity.email.use\_display__**

    Specifies whether to display email addresses or user IDs \(display value from the User table\) in email headers. If true, the instance searches for a user record with a matching email address. If it cannot find a matching user record, it displays the email address.

    -   Type: true \| false
    -   Default value: false
-   **__glide.activity.rule.sys\_email.expand\_max\_body\_size__**

    Specifies the limit of the volume of data which can be processed via a single click of Expand All or getEmailBodies operation. If limit value is hit the user is notified that The maximum allotted email text threshold has been reached and some mails are not expanded.

-   **__glide.ui.email\_client.email\_address.disambiguator__**

    Sets the columns from the User `[sys_user]` table that the auto-complete list displays. Separate each column name with a semicolon character \(;\).

    -   Type: string
    -   Default value: name
-   **__glide.ui.incident\_activity.max\_addresses__**

    Specifies the maximum number of addresses to list in an email audit record. If the number of addresses exceeds this limit, the instance truncates the list after the maximum value and displays an ellipsis character \(...\).

    -   Type: string
    -   Default value: 5
-   **__NotifyAffectedCI.max\_rel\_level__**

    Sets a value that is used by the **Affected ci notifications** business rule. The business rule notifies subscribers when tasks affect configuration items \(CIs\). The business rule generates notifications for parent CIs up to the level defined by this property. You can adjust the property value according to the complexity and depth of your CI relationships.

    -   Type: integer
    -   Default value: 5
-   **__glide.email.inbound.attachment\_extensions\_blacklist__**

    Restrict attachments with questionable file extensions for inbound email.

-   **__glide.email.smtp.claim.lookback.hrs__**

    Sets the default value of 24 hours. Any email older than 24 hours will not be sent by the system. This protects the system from having a huge number of sent emails at a time or if the outbox has a large number of emails waiting to be sent.

    Set to a value greater than 24 \(hours\) and increase it in intervals to not send a large number of emails at one time. Depending on how big the backlog of emails is and how spaced out they are created in time, you might want to start with a value of 36 \(1.5 days worth\), let those go out, then set the value again to maybe 48 \(two days\), and keep increasing the value until all of the older emails are sent.

    -   Type: integer
    -   Value: 24
-   **__glide.email.outbound.static\_translation.enabled__**

    Enables the system property for static translation of notifications for the global application.

    -   Type: true \| false
    -   Default value: true
-   **__glide.notification.translation.dynamic__**

    Enables the system property for dynamic translation of notifications for the global application.

    -   Type: true \| false
    -   Default value: true
-   **__glide.security.file.mime\_type.validation.inbound\_email__**

    When set to `true`, validates the mime type of attachments in the inbound email.

    -   Type: true \| false
    -   Default value: false

**Parent Topic:**[Email properties](../concept/c_EmailProperties.md)

**Related topics**  


[Outbound email configuration](r_OutboundMailConfiguration.md)

[Inbound email configuration](r_InboundMailConfiguration.md)

[Email image filtering properties](../../notification/concept/email-image-filters.md)

[Email digest properties](../../notification/concept/email-digest-properties.md)

