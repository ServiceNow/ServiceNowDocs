---
title: Configure the mail and SMS send to self
description: Help employees access information easily by sending required information as an SMS or email.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Employee Center Pro Kiosk, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Configure the mail and SMS send to self

Help employees access information easily by sending required information as an SMS or email.

## Before you begin

Ensure you set up the email and SMS notifications first.

-   Configure email as explained in Create an email notification.
-   Configure SMS notification with Twilio as explained in Configure Notify with Twilio.

    **Important:** Work with the notify\_admin user for Twilio **Account SID** and **Auth Token** to set up Notify with Twilio. Follow the instructions from Configure Notify with Twilio and verify [Verified Caller IDs](https://www.twilio.com/console/phone-numbers/verified).


Role required: sn\_hr\_sp.esc\_admin

## About this task

You can send useful information such as **Schedule** or **Article** to self as an email or SMS.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Send to self configuration**.

2.  Click **New** or open an existing record.

3.  On the form, fill in the fields.

<table id="table_ipr_bbk_4fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Send to self channels

</td><td>

Channel for sending the information. -   Email
-   SMS
-   Email and SMS \(Default\)

**Note:** Ensure you specify the **Email** address and **Home phone** number on the **sys\_user** table.

</td></tr><tr><td>

Active

</td><td>

Check the box to activate.**Note:** You can have only one active configuration for each portal.

</td></tr><tr><td>

Portal

</td><td>

Portal on which you want to display the **Send to self** option. **Note:** By default, this option is available for Kiosk. However, you can configure for other portals too.

</td></tr><tr><td>

Twilio number

</td><td>

Number to send SMS. This field is visible only when you select **SMS** or **Email and SMS**.

</td></tr></tbody>
</table>    **Note:** When the email or phone number is not configured, an error message appears. For example,

    -   When you enable the sn\_hr\_core plugin, you can raise a profile update request directly: `Unable to send email as there is no email address available. To add an email address to your profile, submit a profile update request here: Request profile update.`
    -   When you don’t enable the sn\_hr\_core plugin, you can request your manager for a profile update: `Unable to send email as there is no email address available. To add an email address to your profile, contact your manager.`
4.  Click **Save**.


## Result

On configuration, Employee Center Pro Kiosk portal displays the **Send to self** option.

## What to do next

Employee can send the mail and SMS using the default Email and SMS template.

-   **User triggered notification template** is available from **All** &gt; **System Notifications** &gt; **Email** &gt; **Templates**.
-   **User triggered employee notification layout** is available from **All** &gt; **System Policy** &gt; **Email** &gt; **Layout**.

**Parent Topic:**[Employee Center Pro Kiosk](../concept/deskless-kiosk-overview.md)

**Related topics**  


[Use Employee Center Pro Kiosk](../concept/deskless-eck-homepage.md)

[Modify Send to self widget display](config-sendtoself-instanceoptions.md)

[Modify email notification layout](activate-notification-template.md)

