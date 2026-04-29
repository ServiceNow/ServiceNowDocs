---
title: Configure an Emergency Outreach notification for the daily contact log
description: As an administrator, create or configure the Emergency Outreach notification to send email and mobile push notifications to employees to ask them to submit a list of co-workers whom they have interacted with on a given day.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure an Emergency Outreach notification for the daily contact log

As an administrator, create or configure the Emergency Outreach notification to send email and mobile push notifications to employees to ask them to submit a list of co-workers whom they have interacted with on a given day.

## Before you begin

Ensure that you have the Emergency Outreach application installed. For details, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).

Employees must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Role required: sn\_imt\_checkin.checkin\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Administration** &gt; **Daily Log Alerts**.

2.  Either edit the existing notification by opening the **Daily Contact Log** outreach record or click **New** to create one.

3.  Enter the outreach notification name in the **Event name** field.

4.  Select the **Employee Daily Contact Log Alert** check box.

    The **Daily Contact Log** option is selected in the **Response mode** field on the **Content configuration** tab. You cannot change this value if the **Employee Daily Contact Log Alert** check box is selected.

5.  On the **Select targeted audience** tab, select the target audience for the notification, and click **Save**.

    -   You can choose from user lists, groups, departments, locations, or other search filters such as building, cost center, or country code.
    -   If you have the ServiceNow® Employee Health Screening application installed, the **Use Employee Health Screen Data** option is available. Select this check box to include all employees cleared in the health screening to enter the premises. For more information, see [Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md).
    -   If you have the ServiceNow® Workplace Core application installed, the **User Workplace Reservation Data** option is available. Select this check box to include all employees with confirmed or approved reservations for that day. For more information, see [Workplace Core](../../workplace-safety-mgmt/concept/workplace-safety-mgmt-hr.md).
6.  On the **Content configuration** tab, select a notification in the **Notification** field, and choose how to send the notification.

    -   To send the notification by email, select the **Email notification** check box and enter the email subject and body.
    -   To send a mobile push notification, select the **Now Mobile Push notification** check box and enter or modify the push message and a detailed push message.

        This option is available only if the ServiceNow NowMobile App Screens and Applet Launcher \(com.glide.mobile-employee\) plugin is activated.

        Push notifications use the ServiceNow Request Application notification device. When users register their mobile application to an instance, this notification device is automatically created in their notification preferences. Ensure that this device is active for the users that you want to receive the push notification.

    -   To use a custom notification channel, click the Additional Channels related list, click **Edit**, and move the channel to the Additional Channels List. Click **Save**.

        Make sure that the **Email notification** and **Now Mobile Push notification** check boxes are not selected or notifications will also be sent through those channels.

7.  Click **Save**.

    The target audience and content configuration changes are saved.

8.  Click **Schedule**.

9.  In the Scheduled Script pop-up window, configure a scheduled job to the notification.

    For more information, see [Configure a scheduled job](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

10. Click **Submit**.

    A script is added to the scheduled job. The job is associated with the outreach notification.


## Result

An outreach notification with a scheduled job is created. The job sends notifications to the target audience per the set schedule.

## What to do next

A user with the sn\_imt\_checkin.checkin\_admin role can [send the Outreach notification on demand](send-outreach-notif-daily-log.md).

A user with the admin or sn\_imt\_checkin.checkin\_admin role can stop the scheduled job to send the notifications automatically. To do so, click **Schedule** and in the dialog box, clear the **Active** check box, and then click **Update**.

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

