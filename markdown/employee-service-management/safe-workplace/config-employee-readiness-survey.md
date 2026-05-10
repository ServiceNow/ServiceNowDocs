---
title: Configure Employee Readiness Surveys notifications
description: The administrator can add or modify Employee Readiness Surveys notifications. Users with the sn\_imt\_checkin.checkin\_admin or survey\_admin role can view the base system survey and copy it to make changes, or add a new survey.Modify the Employee Readiness Surveys base system email notification.Add a new Employee Readiness Surveys email notification to use in Emergency Outreach to send the survey link.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Employee Readiness Surveys, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Employee Readiness Surveys notifications

The administrator can add or modify Employee Readiness Surveys notifications. Users with the sn\_imt\_checkin.checkin\_admin or survey\_admin role can view the base system survey and copy it to make changes, or add a new survey.

**Parent Topic:**[Employee Readiness Surveys](../concept/employee-readiness-surveys.md)

## Modify the Employee Readiness Surveys notification

Modify the Employee Readiness Surveys base system email notification.

### Before you begin

Review the details about planning for, creating, and modifying system notifications by starting with [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Send Outreach**, and then select the Content configuration tab.

2.  In the **Response Mode** field, select **Survey**.

    The **Survey** field appears and the entry in the **Notification** field changes to **Outreach Surveys**.

3.  Select the preview icon \(![Preview icon](../../safe-workplace-dashboard/image/icon-preview.png)\) beside the **Notification** field, and then select **Open record**.

4.  In the Notification form for this Outreach Surveys notification, modify the details as needed.

    Retain the default Assessment Instance \[asmt\_assessment\_instance\] table value.

5.  Select **Preview Notification** and verify your changes.

6.  When you're finished, select **Update**.


### Result

The modified notification is used for future Employee Readiness Surveys notifications.

## Add an Employee Readiness Surveys email notification

Add a new Employee Readiness Surveys email notification to use in Emergency Outreach to send the survey link.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Review the existing **Outreach Surveys** email notification to familiarize yourself with the scripts and other settings.

    ![Displays the When to send tab in the Outreach Survey notification.](../image/ers-when-send-notif.png "Outreach Surveys base system notification")

3.  Select **New**.

4.  In the **Table** field, select the Outreach Surveys \[sn\_imt\_checkin\_employee\_check\_in\] table.

5.  On the When to send tab, set the conditions.

    -   Set the **Conditions** criteria as shown in the image of the base system notification.
    -   Enter the Advanced condition script with the following change.

        For this line: `var thisNotificationSysId = 'a1baaaba71201010fa9b986641bd1ca4';`

        Replace the sys\_id with the sys\_id notification that you're adding. To get the sys\_id, open the additional actions menu, and then select **Copy sys\_id**.

6.  On the Who will receive tab, open **Users/Groups in fields** and select **Assigned to**.

7.  On the What it will contain tab, complete the remaining information.

8.  Select **Submit**.

9.  In the Notifications list, open the notification that you added and select **Preview Notification**.

10. Review the notification and make any necessary modifications.

11. Select **Update**.


