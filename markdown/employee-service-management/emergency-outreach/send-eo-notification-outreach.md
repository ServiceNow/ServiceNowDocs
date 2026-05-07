---
title: Send notifications for an emergency
description: Use Emergency Outreach to notify users to report their health status. Use Emergency Outreach also to quickly notify users of important information if there is an emergency.
locale: en-US
release: australia
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Emergency Outreach, Emergency Response Management, Employee Service Management]
---

# Send notifications for an emergency

Use Emergency Outreach to notify users to report their health status. Use Emergency Outreach also to quickly notify users of important information if there is an emergency.

## Before you begin

Users must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Note the following requirements to be able to send and receive SMS notifications:

-   Your company must have a Safe Workplace suite subscription and Employee Readiness Core installed.
-   Your company must have a Twilio account and phone number.
-   The Notify plug-in and the Notify-Twilio Direct driver must be enabled.
-   The Label for your number in **Notify** &gt; **Messages** must be set to **Outreach**.

For more information on configuring Notify and the Notify-Twilio Direct driver, see [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Role required: sn\_imt\_checkin.checkin\_admin or admin

## About this task

Emergency Outreach is available in the ServiceNow Store without a subscription. The base system provides a notification that requests a response from the recipient regarding their health status. The responses are stored as outreach records and the health status is updated each time the user responds with a change.

Some of the Safe Workplace suite apps leverage the Emergency Outreach notification feature to communicate with users. The Safe Workplace suite apps provide more flexible functions than using Emergency Outreach as a standalone app.

-   Employee Readiness Surveys provides notification with a survey link to assess user readiness to return to the workplace.
-   Employee Readiness Core provides the ability to use Safe Workplace audiences to simplify the selection of recipients for an outreach.
-   Employee Health Screening: Request that users acknowledge their health status verification each day before they can return to the workplace.
-   Contact Tracing supports these outreach notification needs:
    -   A scheduled notification for returning users to fill out a daily contact log.
    -   A request to review the organization's privacy policy and provide consent to use their contact tracing data.

The following procedure is applicable to the use of Emergency Outreach as a standalone app or with Safe Workplace suite applications.

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Send Outreach**.

2.  Enter a name that describes the purpose of the outreach notification.

    For example, `Global health status check-in` or `London office health status check-in`.

3.  In the **Description** field, describe the purpose for sending the outreach.

4.  On the **When to run** tab, specify when the outreach should be sent.

<table id="eo-table-when-to-run"><thead><tr><th align="left" id="d445795e238">

Option

</th><th align="left" id="d445795e241">

Action

</th></tr></thead><tbody><tr><td id="d445795e247">

**To send the notification on demand**

</td><td>

Keep the default **Mode** value of **None**. The outreach is sent when you select **Send Notification**.

</td></tr><tr><td id="d445795e265">

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

5.  To identify who will receive the outreach, perform one of the following actions.

<table id="choicetable_cfs_ms2_jmb"><thead><tr><th align="left" id="d445795e366">

Installed apps

</th><th align="left" id="d445795e369">

Action

</th></tr></thead><tbody><tr><td id="d445795e375">

**Emergency Outreach standalone**

</td><td>

On the **Select targeted audience** tab, select the combination of users to send the outreach notification to. Choose from user lists, groups, departments, locations, or other search filters such as building, cost center, or country code.For more information, see [Add a Safe Workplace audience](../../employee-readiness-core/task/add-safe-workplace-audience.md).

</td></tr><tr><td id="d445795e405">

**With Safe Workplace**

</td><td>

On the Safe Workplace Audience tab, select the name of the audience to send the outreach notification to.

</td></tr></tbody>
</table>6.  Click **Save**.

    The outreach details are saved and related lists appear. The Additional Channels related list is used to specify additional custom channels to use when you send the notification. Other related lists are filled in with outreach recipients and their status after you send the notification.

7.  Click the **Content configuration** tab and leave the default response mode **Outreach Acknowledgements**.

8.  On the **Content configuration** tab, specify how to send the outreach notification.

<table id="choicetable_frh_152_jmb"><thead><tr><th align="left" id="d445795e457">

Option

</th><th align="left" id="d445795e460">

Action

</th></tr></thead><tbody><tr><td id="d445795e466">

**Disable the email notification**

</td><td>

Clear the **Email** check box.

</td></tr><tr><td id="d445795e478">

**Select a different notification**

</td><td>

Click the lookup icon \(![Click icon to look up a notification](../../contact-tracing/image/icon-lookup.png)\) and select the notification to use.

</td></tr><tr><td id="d445795e493">

**Review and edit the introductory message**

</td><td>

Modify the subject and body as desired. The default message template asks users to submit their health status regarding infectious diseases, such as COVID-19. The user selects a response from a list of possible responses.

</td></tr><tr><td id="d445795e505">

**Send a mobile push notification**

</td><td>

1.  Select the **Now Mobile Push Notification** check box.

The check box is active if the ServiceNow NowMobile App Screens and Applet Launcher \[com.glide.mobile-employee\] is activated. The push notification content appears when the check box is active, and you can modify it.

2.  Modify the push message text as desired.
 Push notifications use the ServiceNow Request Application notification device. When mobile application is registered to an instance, this notification device is automatically created in the user's notification preferences. Ensure that this device is active for the users that you want to receive the push notification.

</td></tr><tr><td id="d445795e535">

**Send an SMS notification**

</td><td>

1.  Select the **Message via SMS** check box.
2.  Modify the SMS message text.

**Note:** For existing outreaches, if **Message via SMS** is selected, the **SMS message** is not autopopulated.

3.  Click **Save**.
 SMS reply options are dynamically populated from the Response Options \[sn\_imt\_checkin\_response\_option\] table.

</td></tr><tr><td id="d445795e573">

**Use a custom notification channel**

</td><td>

1.  Click the Additional Channels related list, click **Edit**, and move the channel to the Additional Channels List.
2.  Click **Save**.
 If the **Email notification**, **Now Mobile Push notification**, and **Message via SMS** check boxes are selected, all four notifications are sent. To use only the custom notification channel, clear these three check boxes.

</td></tr></tbody>
</table>9.  Click **Send Notification**.

    The notification is sent immediately or at the time specified on the **When to run** tab. As responses are received, they appear in the Outreach Acknowledgements related list.


## What to do next

Review the Emergency Outreach acknowledgements.

**Parent Topic:**[Emergency Outreach](../concept/emergency-outreach.md)

**Related topics**  


[Add a Safe Workplace audience for Emergency Outreach](add-sw-audience-outreach.md)

[Send an Outreach notification for the daily contact log](../../contact-tracing/task/send-outreach-notif-daily-log.md)

[Send an Emergency Outreach notification for employee privacy consents in Contact Tracing](../../contact-tracing/task/send-outreach-notif-privacy.md)

[Send a readiness survey and view responses](send-eo-outreach-survey.md)

[Send notifications for daily health verification](send-daily-health-verif-notif-outreach.md)

