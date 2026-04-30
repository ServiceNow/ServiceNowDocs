---
title: Send a readiness survey and view responses
description: Use Emergency Outreach to send a workplace readiness survey. Review the survey responses to assist with your plans to reopen your workplace.
locale: en-US
release: yokohama
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Emergency Outreach, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Send a readiness survey and view responses

Use Emergency Outreach to send a workplace readiness survey. Review the survey responses to assist with your plans to reopen your workplace.

## Before you begin

In order to send a survey, you must have the Employee Readiness Surveys application installed.

Employees must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Role required: sn\_imt\_checkin.checkin\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Send Outreach**.

2.  Enter a name that describes the purpose of the survey.

    For example, "San Diego readiness survey" or "Employee readiness Europe."

3.  In the **Description** field, describe the purpose for sending the outreach survey.

4.  On the **When to run** tab, specify when the outreach should be sent.

<table id="eo-table-when-to-run"><thead><tr><th align="left" id="d110707e118">

Option

</th><th align="left" id="d110707e121">

Action

</th></tr></thead><tbody><tr><td id="d110707e127">

**To send the notification on demand**

</td><td>

Keep the default **Mode** value of **None**. The outreach is sent when you select **Send Notification**.

</td></tr><tr><td id="d110707e145">

**To schedule the notification**

</td><td>

1.  Set the mode to **Scheduled**.
2.  In the **Run** field, indicate how often the outreach should be sent. The options are **Daily**, **Weekly**, **Monthly**, or **Once**.
    -   For daily outreaches, enter the time that you want to send the outreach. You can specify hours, minutes, and seconds. For example, enter `17:30:00` to send the outreach at 5:30 p.m. If you don't want the outreach to be sent on certain days of the week, select those days in the **Exclude** field.
    -   For weekly outreaches, select the day of the week and the time you want to send the outreach.
    -   For monthly outreaches, select the day of the month and the time you want to send the outreach. If you select a day that does not exist in all months, for example `31`, the outreach will run on the last day of the month.
    -   For outreaches that are only sent once, schedule the date and time that you want to send the outreach in the **Starting** field.
3.  \(Optional\) To send the outreach based on the time zone set in the user profile, select the **Send in local time** check box.

The outreach messages reference a send time based on the time zone of the user sending the notification. For example, if the sender is in the US Pacific time zone, an outreach scheduled to be sent at 4:30 p.m. shows a send time of 16:30:00 for users in that time zone and 18:30:00 \(6:30 p.m.\) for users in the US Central time zone because the Pacific time zone is two hours earlier than the Central time zone.

</td></tr></tbody>
</table>    **Note:**

    In prior releases of Emergency Outreach, notification scheduling was configured by selecting **Schedule** and entering details in a pop-up window. Scheduling is now configured on the **When to run** tab.

    Scheduled outreaches that you sent prior to upgrading provide the previous scheduling function if you need to resend it. This functionality provides the flexibility to set up new scheduled outreaches and to resend prior scheduled outreaches.

5.  Identify who will receive the outreach notification through either the Emergency Outreach or Safe Workplace application.

<table id="choicetable_mxq_4sk_jmb"><thead><tr><th align="left" id="d110707e252">

App

</th><th align="left" id="d110707e255">

Action

</th></tr></thead><tbody><tr><td id="d110707e261">

**Emergency Outreach standalone**

</td><td>

On the Select targeted audience tab, select the combination of users to send the outreach notification to. Choose from user lists, groups, departments, locations, or other search filters such as building, cost center, or country code.

</td></tr><tr><td id="d110707e276">

**Safe Workplace**

</td><td>

On the Safe Workplace **Audience** tab, select the name of the audience to send the outreach notification to.

</td></tr></tbody>
</table>6.  Click **Save**.

    The survey outreach details are saved and related lists appear. The Additional Channels related list is used to specify additional custom channels to use when you send the survey notification. The Survey Instances related list is filled in with outreach recipients and their survey status after you send the notification.

7.  Click the **Content configuration** tab, and in the **Response Mode** field, select **Survey**.

    Use the **Status** field that appears on the outreach form to confirm the creation status of your survey instances when you send the notification.

8.  Select the survey to use or keep the default **Employee workplace readiness survey**.

9.  To set a due date for the survey, enter a value in the **Duration** field.

    The **Duration** field sets the amount of time allowed to complete assigned survey instances, starting from the time that the survey instance is generated. The survey instances created for the outreach use the **Duration** field for their due date instead of the **Assessment duration** field on the survey.

10. Specify how to send the outreach notification.

<table id="choicetable_frh_152_jmb"><thead><tr><th align="left" id="d110707e370">

Option

</th><th align="left" id="d110707e373">

Action

</th></tr></thead><tbody><tr><td id="d110707e379">

**Disable the email notification**

</td><td>

Clear the **Email** check box.

</td></tr><tr><td id="d110707e391">

**Select the survey**

</td><td>

Select the survey to use or keep the default **Employee workplace readiness survey**.

</td></tr><tr><td id="d110707e403">

**Select a different notification**

</td><td>

Click the lookup icon \(![Click icon to look up a notification](../../contact-tracing/image/icon-lookup.png)\) and select the notification to use.

</td></tr><tr><td id="d110707e418">

**Review and edit the introductory message**

</td><td>

Modify the subject and body as desired. The notification includes the survey link that the employee can take in the instance or mobile app.

</td></tr><tr><td id="d110707e431">

**Send a mobile push notification**

</td><td>

1.  Select the **Now Mobile Push Notification** check box.

The check box is active if the ServiceNow NowMobile App Screens and Applet Launcher \[com.glide.mobile-employee\] is activated. The push notification content appears when the check box is active, and you can modify it.

2.  Modify the push message text as desired.
 Push notifications use the ServiceNow Request Application notification device. When mobile application is registered to an instance, this notification device is automatically created in the user's notification preferences. Ensure that this device is active for the users that you want to receive the push notification.

</td></tr><tr><td id="d110707e460">

**Use a custom notification channel**

</td><td>

1.  Click the Additional Channels related list, click **Edit**, and move the channel to the Additional Channels List.
2.  Click **Save**.
 If the **Email notification** and **Now Mobile Push notification** check boxes are selected, all three notifications are sent. To use only the custom notification channel, clear these two check boxes.

</td></tr></tbody>
</table>11. Click **Send Notification**.

    The notification and survey link are sent to the target audience. A survey instance is created for each recipient, with the status **Ready to take**.

    When you send the outreach survey notification, any open survey instances for the recipients are canceled. When you resend a notification for an outreach, the open survey instances are not canceled.

    If you have a recurring scheduled outreach, such as a survey that is sent daily or weekly, each time the outreach is sent, the open surveys from the previous day or week are canceled.

    You can't create an outreach survey notification if the survey is being used in a scheduled outreach notification.

    After the notification is sent, the Emergency Outreach Instance Logs related list is displayed. The **Instance creation status** field values match the status on the outreach form.

    -   Success: An instance was created for every recipient in the target audience. The number of Assessment instances created should match the number of Target assessment instances or recipients of the survey.

    -   Partial Success: An instance was created for some recipients in the target audience but not all of them. The number of Target assessment instances and Assessment instances created do not match.

        Send the notifications to users who did not receive a notification or instance by clicking **Send to Remaining**.

    -   Failed: No instances were created and no surveys were sent.

        Resend the notification to all users by clicking **Send Notification** again.

12. To view survey instances, navigate to **Emergency Outreach** &gt; **View Outreaches** and open the survey notification to view.

    **Note:** Users with the sn\_imt\_checkin.checkin\_admin role can see all survey instances. Users who have been assigned the survey can see only their own survey instances.

    As employees complete the survey, the status updates in their survey instance.

    If employees haven't responded yetand instances were successfully created for all users, click **Resend Notification**. The notification is sent again only to employees who have not yet responded.

    ![View survey scorecard related link and the list of survey instances.](../image/survey-instances-list.png)

    When an outreach is sent using a custom notification channel, a Delivery Logs related list appears in the outreach record. It lists successful and failed log records for the notification that you sent.

    Depending on how the notification channel was created, success messages can show the number of notifications that were successfully sent, and the total number of notifications that were requested. If the total count is higher than the sent count, the difference is the number of notifications that failed.

    Open the record and investigate the cause of the errors. Correct the cause of the failures, or use another notification method for the users whose notification was not sent.

13. To view the status of Outreach instances, navigate to **Emergency Outreach** &gt; **View Outreach Instance Logs**.

14. To view the interactive scorecard showing all responses and the results, click the **View Survey Scorecard** related link.

    ![Survey responses scorecard with charts.](../image/survey-response-scorecard.png)

    Click any area of a chart to see the corresponding records.


**Parent Topic:**[Emergency Outreach](../concept/emergency-outreach.md)

