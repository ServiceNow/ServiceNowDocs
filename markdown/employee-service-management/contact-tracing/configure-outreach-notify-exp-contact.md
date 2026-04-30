---
title: Configure an Emergency Outreach notification for the exposure notice
description: Configure an Emergency Outreach notification to send email and mobile push notifications to potentially exposed employees in an exposure case to notify them of a potential exposure from an affected employee.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure an Emergency Outreach notification for the exposure notice

Configure an Emergency Outreach notification to send email and mobile push notifications to potentially exposed employees in an exposure case to notify them of a potential exposure from an affected employee.

## Before you begin

Ensure that you have the Emergency Outreach application installed. For details, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).

Employees must have the Now® Mobile app installed on their phones to receive mobile push notifications. For more information, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

Role required: sn\_imt\_checkin.checkin\_admin or admin

## About this task

Review the existing **Notify Exposed Contact** outreach notification to familiarize yourself with the configuration.

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **View Outreaches**.

2.  Click **New**.

3.  Enter the outreach notification name in the **Event name** field.

4.  On the **Content configuration** tab, select **Exposure Notice** in the **Response mode** field.

5.  Review and edit the introductory message by modifying the subject and body in the **Email subject** and **Email body** fields respectively.

6.  Specify how to send the outreach notification.

<table id="choicetable_frh_152_jmb"><thead><tr><th align="left" id="d712815e165">

Option

</th><th align="left" id="d712815e168">

Steps

</th></tr></thead><tbody><tr><td id="d712815e174">

**Send an email notification**

</td><td>

Select the **Email** check box.

</td></tr><tr><td id="d712815e186">

**Select a different notification**

</td><td>

Click the lookup icon \(![look up icon](../image/icon-lookup.png)\) and select an [email notification configured for the exposure notice outreach](configure-notify-exp-contact-email.md).

</td></tr><tr><td id="d712815e211">

**Send a mobile push notification**

</td><td>

1.  Select the **Now Mobile Push notification** check box.

The check box is active if you have the ServiceNow NowMobile App Screens and Applet Launcher \[com.glide.mobile-employee\] activated. The push notification content appears when the check box is active.

2.  Modify the text in the **Push message** and **Detailed Push Message** fields.
 Push notifications use the ServiceNow Request Application notification device. When you register the mobile application to an instance, this notification device is automatically created in the user's notification preferences. Make sure that this device is active for the users that you want to receive the push notification.

</td></tr><tr><td id="d712815e246">

**Use a custom notification channel**

</td><td>

1.  Click the Additional Channels related list, click **Edit**, and move the channel to the Additional Channels List.
2.  Click **Save**.
 If the **Email notification** and **Now Mobile Push notification** check boxes are selected, all three notifications are sent. To use only the custom notification channel, clear these two check boxes.

</td></tr></tbody>
</table>7.  Click **Submit**.

    The content configuration settings are saved.


## Result

An exposure notice outreach notification is created. These exposure notice outreach notifications are available for selection when a case manager wants to send notifications to the potentially exposed contacts in a case.

## What to do next

A case manager can [send the outreach notification](send-notification-to-exposed-contact.md) to the potentially exposed contacts in a case.

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

