---
title: Configure email digests
description: Use the Notification form to create or modify the content of an email digest for a notification. You can also disable the email digest for a notification so that it isn’t available in the notification preferences of your users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Email digests, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure email digests

Use the Notification form to create or modify the content of an email digest for a notification. You can also disable the email digest for a notification so that it isn’t available in the notification preferences of your users.

## Before you begin

Role required: admin

## About this task

When you [create or update a notification](t_CreateANotification.md), use the **What Digest will contain** tab of the Notification form to configure the email digest for the notification. After you define the digest content, the digest option for the notification is available in the notification settings of your users.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

    |Action|Description|
    |------|-----------|
    |To create a notification|Select **New** to open the Notification form.|
    |To modify a notification|Select the notification to be changed.|

2.  In the Notification form, select the **Allow Digest** check box to display the **What Digest will contain** tab and define the digest content.

3.  Select the **Digest type**.

<table id="choicetable_jb2_kxp_1fc"><thead><tr><th align="left" id="d258629e165">

Digest Type

</th><th align="left" id="d258629e168">

Description

</th></tr></thead><tbody><tr><td id="d258629e174">

**Single target record**

</td><td>

Allows this notification to be sent in an email digest when it is triggered multiple times during the selected interval for a single target record, for example INC001 only.

</td></tr><tr><td id="d258629e190">

**Multiple target record**

</td><td>

Allows this notification to be sent in an email digest when it is triggered multiple times during the selected interval for a multiple target record, for example INC001, INC002, and more.

</td></tr></tbody>
</table>4.  To enforce a notification as digest, select the **Enable by default** check box.

5.  Select the **Default Interval**.

6.  Select the **What Digest will contain** tab.

7.  Fill in the fields. in the **What Digest will contain** tab.

    The image shows the default view of the tab. The advanced view contains additional fields \(see table\).

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

**Note:** For email digest with multiple target records enabled, it's recommended to use a subject text without any dynamic variables.

</td></tr><tr><td>

Digest HTML

</td><td>

Enter the recurring content for the email digest. The digest content can include variables from the **Select variables** column.

 Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table such as an incident short description or comments and work notes.

 To prevent adding extra `<p>` and `<div>` elements to your email digest, see the blog post [Extra line spacing with paragraph tags in email client](https://community.servicenow.com/community/blogs/blog/2014/12/12/extra-line-spacing-with-p-tags-in-email-client) by a ServiceNow employee in the ServiceNow Community.

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
</table>8.  When you finish creating the notification, select **Submit**.

    The email **Digest** option is displayed in the notification settings of your users.

    **Note:** The email recipients identified in the **Who will receive** tab will receive the digest after they [enable the digest](enable-email-digest.md) in their notification preferences. If the user isn’t a designated recipient for the notification, a digest isn’t generated even though the user may have the digest enabled for a notification. In this case, the user receives the actual notifications when they’re generated.

9.  To disable the email digest for a notification, unselect the **Allow Digest** check box and select **Update** when you finish your changes to the notification.

    When you disable the digest content, the digest option is also no longer available for the notification and isn’t listed in the notification preferences for your users. If a user previously enabled the digest option for the notification, the system stops collecting those notifications for a digest and doesn’t generate the digest.

    **Note:** If you turned off the digest and want to make the digest available again, select the **Allow Digest** check box. The system retains the previously saved digest content and displays it in the **What Digest will contain** tab.


**Parent Topic:**[Email digests](../concept/email-digests.md)

**Related topics**  


[Email digests](../concept/email-digests.md)

[Create or modify email digest intervals](create-digest-intervals.md)

[Enable an email digest in Core UI](enable-email-digest.md)

