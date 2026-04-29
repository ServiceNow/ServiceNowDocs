---
title: Set up personal corporate mailbox
description: Set up your personal corporate mailboxes with ServiceNow platform.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Personal corporate mailbox, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up personal corporate mailbox

Set up your personal corporate mailboxes with ServiceNow platform.

## Before you begin

The User Mailbox Integration \(com.glide.email.user\_mailbox.integration\) plugin must be installed.

Role required: user\_email\_account

## Procedure

1.  From the user menu, navigate to **Preferences** &gt; **Notifications** and then select the **Advanced Preferences** link.

2.  Select the **Delivery Channels** tab.

3.  If no devices are configured, follow these steps to add an email device.

    1.  In the Email channel section, select **+Add**.

    2.  Expand the **Channel info** section and provide the channel name and email address in the fields.

    3.  Select **Save**.

4.  Set up personal mailbox.

    1.  In the Set up personal mailbox section, select the **Set up personal mailbox** option.

    2.  In the Create dialog, select **Password** or **OAuth 2.0** from the Authentication drop-down list.

        For **Password** as the authentication type, enter the App password provided by your email service provider in the **App password** field.

    3.  In the **User email** field, enter the email address of the mailbox that you want to connect.

    4.  Select a template from the list of configured user email account templates.

        To configure a new template aside from the preconfigured templates, see [Configure templates for personal corporate mailboxes](configure-personal-corporate-mailbox.md).

    5.  Review the information.

    6.  Integrate the mailbox by selecting the **I acknowledge** option.

    7.  Select **Connect**.

    8.  Expand the Set up personal mailbox section to view the connected mailboxes.

        **Note:** At least one mailbox must be connected to view the connected mailboxes.


**Parent Topic:**[Personal corporate mailbox](../concept/personal-corporate-mailbox.md)

