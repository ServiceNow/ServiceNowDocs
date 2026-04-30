---
title: Convert legacy email notifications to rich HTML
description: By default, new email notifications are created in the rich HTML format. But you can also convert legacy notifications to rich HTML.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Convert legacy email notifications to rich HTML

By default, new email notifications are created in the rich HTML format. But you can also convert legacy notifications to rich HTML.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  On the **Email Notifications** list screen, select the name of the email notification you want to convert.

3.  Click the **What it will contain** tab.

4.  Select **Switch to Rich HTML Editor**.

    The system copies any raw HTML from the **Message** field and converts it to rich HTML in the **Message HTML** field. Additionally, any mail scripts in the body are automatically saved to the Email Script `[sys_script_email]` table and are replaced in the notification body with an embedded script tag. This makes the notification body easier to read.

    **Note:** The string "div" at the bottom of the screen shows the location of your cursor within the **Message HTML** field. In this case, the cursor is in a line containing an HTML `<div>` tag.


## What to do next

When you convert an email notification that was created in a version prior to Eureka to rich HTML, mail scripts are automatically moved to the Email Script \[sys\_script\_email\] table and an embedded script tag with the name of the script is automatically inserted into the body of the notification.

When creating new email notifications, write mail scripts using **System Notification** &gt; **Email** &gt; **Notification Email Scripts**. When the scripts are completed, add a `${mail_script:script name}` embedded script tag to the email notification body. This makes it easy to use the same scripts in multiple email notifications. All you need to copy and paste from one notification to the next is the embedded script tag.

If you manually enter a mail script, any text bounded by `<mail_script> </mail_script>` in the body of a new or converted email notification or template which is saved to the record, a message asks whether the mail script should be converted.

![Invalid mail script message](../image/400pxInvalidMailScript.png "Invalid mail script message")

In many cases, an unconverted mail script fails to run from inside the HTML editor. If you select **Yes**, the script is added to the Email Script \[sys\_script\_email\] table and is automatically replaced in the body with an embedded script tag. You can view the mail scripts in their original form by opening the email notification and clicking the **Show Notification Scripts** related link.

**Parent Topic:**[Create an email notification](t_CreateANotification.md)

