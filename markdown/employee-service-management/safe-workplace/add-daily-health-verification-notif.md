---
title: Add an email notification for daily health verification
description: Add an Employee Readiness Surveys email notification to use for sending the survey link.
locale: en-US
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Employee Health Screening, Safe Workplace, Health and Safety, Employee Service Management]
---

# Add an email notification for daily health verification

Add an Employee Readiness Surveys email notification to use for sending the survey link.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Review the existing **Daily Health Verification** email notification to familiarize yourself with the scripts and other settings.

3.  Select **New**.

4.  In the **Table** field, select the Health Verification Acknowledgements \[sn\_imt\_checkin\_health\_verification\_acknowledgement\] table.

5.  On the When to send tab, set the conditions.

    -   In the **Send when** field, select **Record inserted or updated** from the drop-down list.
    -   Set the **Conditions** criteria to **\[User.Active\]\[is\]\[true\]** and **\[Acknowledgment Status\]\[is not\]\[Acknowledged\].**.
    -   In the Advanced condition script, enter the following code:

        ```
        var employeeDailyHealthVerificationSysId = <your-sys_id>
        answer = current.employee_check_in.notification = employeeDailyHealthVerificationSysId;
        
        ```

        Replace the &lt;your-sys\_id&gt; variable with the sys\_id notification that you're adding by opening the additional actions menu, selecting **Copy sys\_id**, and pasting the sys\_id into the code line.

    The following figure shows example settings for the Daily Health Verification base system notification.

    ![The When to send tab in the Daily Health Verification notification.](../image/daily-health-verif-when-send-notif.png)

6.  On the Who will receive tab, open **Users/Groups in fields** and select **Assigned to**.

7.  On the What it will contain tab, complete the remaining information.

8.  Select **Submit**.

9.  In the Notifications list, open the notification that you added and select **Preview Notification**.

10. Review the notification and make any necessary modifications.

11. Select **Update**.


**Parent Topic:**[Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md)

