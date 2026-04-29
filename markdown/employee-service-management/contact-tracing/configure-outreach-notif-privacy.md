---
title: Configure an Emergency Outreach notification for Contact Tracing privacy consents
description: As an administrator, create or configure an Emergency Outreach notification to send email and mobile push notifications to employees requesting them to view the privacy policy and seeking their consent to use their data for contact tracing.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up data privacy consent settings for Contact Tracing, Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure an Emergency Outreach notification for Contact Tracing privacy consents

As an administrator, create or configure an Emergency Outreach notification to send email and mobile push notifications to employees requesting them to view the privacy policy and seeking their consent to use their data for contact tracing.

## Before you begin

Ensure that you have the Emergency Outreach application installed. For details, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).

You must have [generated the location-based privacy configurations](generate-location-privacy-configuration.md).

Employees must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Role required: sn\_imt\_checkin.checkin\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **View Outreaches**.

2.  Review and edit the existing outreach record **User Privacy Consent** record or click **New** to create one.

3.  Enter the outreach notification name in the **Event name** field.

4.  On the **Select targeted audience** tab, select the target audience for the notification, and click **Save**.

    You can choose from user lists, groups, departments, locations, or other search filters such as building, cost center, or country code.

5.  On the **Content configuration** tab, select **Privacy Consent** in the **Response mode** field.

6.  Enable the outreach to provide location-specific privacy consents by selecting the **Use Country** option on the **Content configuration** tab.

    When enabled, the privacy statement text in Location Privacy Configuration takes precedence over text in the privacy consent templates. This text is used for the outreach, system notification email, and push notification. If you need to update the text that users receive, you must change the location's privacy statement.

    For more information on updating a location's privacy statement, see [Generate location-based privacy configurations](../../employee-readiness-core/task/generate-location-common-privacy-configuration.md).

7.  Select **User Privacy Consent** notification in the **Notification** field, and choose how to send the notification.

    -   To send the notification by email, select the **Email notification** check box and enter the email subject and body.
    -   To send a mobile push notification, select the **Now Mobile Push notification** check box and enter the push message and a detailed push message.

        This option is available only if the ServiceNow NowMobile App Screens and Applet Launcher \(com.glide.mobile-employee\) plugin is activated.

    -   To use a custom notification channel, click the Additional Channels related list, click **Edit**, and move the channel to the Additional Channels List. Click **Save**.

        Make sure that the **Email notification** and **Now Mobile Push notification** check boxes are not selected or notifications will also be sent through those channels.

        Push notifications use the ServiceNow Request Application notification device. When users register their mobile application to an instance, this notification device is automatically created in their notification preferences. Ensure that this device is active for the users that you want to receive the push notification.

8.  Click **Save**.

    The target audience and content configuration changes are saved.

9.  Click **Schedule**.

10. In the Scheduled Script pop-up window, configure a scheduled job to the notification.

    For more information, see [Configure a scheduled job](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

11. Click **Submit**.

    A script is added to the scheduled job. The job is associated with the outreach notification.


## Result

An outreach notification with a scheduled job is created. The job sends notifications to the target audience per the set schedule.

**Note:** The outreach notification is not sent to users in the selected audience if users do not have a location set in their user profile or the privacy consent is disabled in the [location privacy configuration](generate-location-privacy-configuration.md). The privacy consent notification is sent to a user only once even if the user is in the target audience of multiple privacy notifications.

## What to do next

A user with the sn\_imt\_checkin.checkin\_admin role can [send the Outreach notification on demand](send-outreach-notif-privacy.md).

A user with the admin or sn\_imt\_checkin.checkin\_admin role can stop the scheduled job to send the notifications automatically. To do so, click **Schedule** and in the dialog box, clear the **Active** check box, and then click **Update**.

**Parent Topic:**[Setting up data privacy consent settings for Contact Tracing](../concept/set-up-privacy-consent-settings.md)

