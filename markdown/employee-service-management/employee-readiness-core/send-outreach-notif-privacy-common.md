---
title: Send an Emergency Outreach notification for employee privacy consents
description: Send an Emergency Outreach notification, on demand, to employees to provide a privacy policy and seek consent to use of their data in accordance with the privacy policy.
locale: en-US
release: australia
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Maintaining privacy consent in Employee Readiness Core, Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Send an Emergency Outreach notification for employee privacy consents

Send an Emergency Outreach notification, on demand, to employees to provide a privacy policy and seek consent to use of their data in accordance with the privacy policy.

## Before you begin

Ensure that you have the Emergency Outreach application installed. For details, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).

Employees must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Role required: sn\_imt\_checkin.checkin\_admin

## About this task

**Important:** The privacy consent notification is sent to a user only once even if the user is in the target audience of multiple privacy consent notifications.

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **View Outreaches**.

2.  Review and edit an existing outreach record or click **New** to create one.

3.  On the **Safe Workplace Audience** tab, select the audience from the list and click **Save**.

    If you don't have an audience defined, click **New** and define an audience from user lists, groups, departments, locations, and so on. After you save the Safe Workplace audience, you can use it to send any outreach message.For more information, see [Add a Safe Workplace audience](add-safe-workplace-audience.md).

4.  On the **Content configuration** tab, select **Privacy Consent \(common\)** in the **Response mode** field.

5.  On the **Content configuration** tab, select a **Privacy consent template**.

6.  Enable the outreach to provide location-specific privacy consents by selecting the **Use Country** option on the **Content configuration** tab.

    When enabled, the privacy statement text in Location Privacy Configuration takes precedence over text in the privacy consent templates. This text is used for the outreach, system notification email, and push notification. If you need to update the text that users receive, you must change the location's privacy statement.

    For more information on updating a location's privacy statement, see [Generate location-based privacy configurations](generate-location-common-privacy-configuration.md).

7.  Select a notification in the **Notification** field and choose how to send the notification.

    **Note:** The default **Notification** is the **User Privacy Consent \(Core\)** that references the \[sn\_imt\_core\_user\_privacy\_notice\_and\_consent\] table.

    -   To send the notification by email, select the **Email notification** check box.
    -   To send a mobile push notification, select the **Now Mobile Push notification** check box.

        This option is available only if the ServiceNow NowMobile App Screens and Applet Launcher \(com.glide.mobile-employee\) plugin is activated.

        Push notifications use the ServiceNow Request Application notification device. When a user registers their mobile application to an instance, this notification device is automatically created in their notification preferences. Ensure that this device is active for the users that you want to receive the push notification.

8.  Review the message content.

    -   For email notifications, review the email subject and email body and modify it if necessary.
    -   For push messages, review the **Push message** and **Detailed Push message** fields.
9.  Click **Update**.

    The target audience and content configuration changes are saved.

10. To send the notification, click **Send Notification**.


## Result

The notification is sent to the target audience.

**Note:** The outreach notification is not sent to any users in the selected audience who do not have a location set in their user profile or whose privacy consent is disabled in the [location privacy configuration](generate-location-common-privacy-configuration.md).

If you need to resend the notification, navigate to **Emergency Outreach** &gt; **View Outreaches**, select the outreach, and click **Resend Notification**.

**Parent Topic:**[Maintaining privacy consent in Employee Readiness Core](../concept/employee-readiness-core-privacy-consent.md)

