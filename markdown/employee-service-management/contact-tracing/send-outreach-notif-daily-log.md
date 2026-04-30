---
title: Send an Outreach notification for the daily contact log
description: Send an Emergency Outreach notification, on demand, to employees to ask them to submit a list of co-workers whom they have interacted with on a given day.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Tracking employee contacts using daily logs, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Send an Outreach notification for the daily contact log

Send an Emergency Outreach notification, on demand, to employees to ask them to submit a list of co-workers whom they have interacted with on a given day.

## Before you begin

Ensure that you have the Emergency Outreach application installed. For details, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).

Employees must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Role required: sn\_imt\_checkin.checkin\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Administration** &gt; **Daily Log Alerts**, and then click **New**.

2.  On the **Safe Workplace Audience** tab, select the target audience for the notification, and click **Save**.

    -   If you don't have an audience defined, click **New** and define an audience from user lists, groups, departments, locations, and so on.For more information, see [Add a Safe Workplace Audience](../../employee-readiness-core/task/add-safe-workplace-audience.md).
    -   If you have the Employee Health Screening application installed, the **Use Employee Health Screen Data** option is available. Select this check box to include all employees cleared in the health screening to enter the premises. For more information, see [Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md).
    -   If you have the Workplace Core application installed, the **User Workplace Reservation Data** option is available. Select this check box to include all employees with confirmed or approved reservations for that day. For more information, see [Workplace Core](../../workplace-safety-mgmt/concept/workplace-safety-mgmt-hr.md).
3.  On the **Content configuration** tab, select a notification in the **Notification** field, and choose how to send the notification.

    -   To send the notification by email, select the **Email notification** check box.
    -   To send a mobile push notification, select the **Now Mobile Push notification** check box.

        This check box is active if the ServiceNow NowMobile App Screens and Applet Launcher \(com.glide.mobile-employee\) plugin is activated. The push notification content appears when the check box is active, and you can modify it.

        Push notifications use the ServiceNow Request Application notification device. When a user registers their mobile application to an instance, this notification device is automatically created in their notification preferences. Ensure that this device is active for the users that you want to receive the push notification.

4.  Review the message content.

    -   For email notifications, review the email subject and email body and modify it if necessary.
    -   For push messages, review the message details.
5.  Click **Update**.

    The target audience and content configuration changes are saved.

6.  To send the notification, click **When to run**.

7.  Keep the default mode of **None** and click **Send Notification**.


## Result

The notification is sent to the selected audience.

## What to do next

[Review daily log responses](review-daily-contacts-log.md) to see who has responded to the notification.

**Parent Topic:**[Tracking employee contacts using daily logs](../concept/employee-daily-log.md)

