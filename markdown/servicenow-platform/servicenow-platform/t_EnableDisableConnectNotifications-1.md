---
title: Enable or disable Connect notifications globally
description: You can edit your Connect notification settings globally to enable or disable mobile, desktop, email, or audio notifications for all your Connect Chat and Connect Support conversations.The following browsers support Connect chat notifications.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Enable or disable Connect notifications globally

You can edit your Connect notification settings globally to enable or disable mobile, desktop, email, or audio notifications for all your Connect Chat and Connect Support conversations.

## Before you begin

Role required: none

## About this task

By default, Connect mobile, email, and audio notifications are enabled globally. You must enable desktop notifications.

An administrator can [customize the sound](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/connect/t_CustomizeConnectAudioNotifSound.md) used for audio notifications.

**Note:** You receive mobile notifications only if you have installed the ServiceNow mobile app.

## Procedure

1.  In the banner frame, click the gear icon \(\[Omitted image "IconUI16Gear.png"\] Alt text: Gear icon\) to open the system settings.

2.  In the system settings window, click the **Notifications** tab.

3.  In Notifications by Category, navigate to **Connect**.

4.  Enable or disable Connect mobile, desktop, email, or audio notifications.

5.  Configure the following system notifications.

    For more information on how to configure system notifications, see Apply notification conditions.

<table id="table_k1c_zyj_tz"><thead><tr><th>

Notification

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity Stream @Mention Email

</td><td>

Sends an email alert to a user anytime they get @mentioned in an activity stream

</td></tr><tr><td>

Collaboration Offline Group Message\(s\)

</td><td>

Sends email to offline users who are members of a group conversation after a certain number of minutes determined by the **collaboration.email\_interval** property to limit spam.**Note:** It takes 90 seconds after a user logs out for the system to register that the user is offline. If a message is sent to the user within 90 seconds of them logging out, then the user does not receive the notification.

</td></tr><tr><td>

Collaboration Offline Message Bundle

</td><td>

Sends email to offline users after a certain number of minutes determined by the **collaboration.email\_interval** property to limit spam.**Note:** It takes 90 seconds after a user logs out for the system to register that the user is offline. If a message is sent to the user within 90 seconds of them logging out, then the user does not receive the notification.

</td></tr><tr><td>

ConnectMessagePushNotification

</td><td>

Uses a push notification to inform users when there are new messages in a conversation

</td></tr><tr><td>

ConnectNotificationPushNotification

</td><td>

Uses a push notification to inform a user when they have been @Mentioned in a record

</td></tr></tbody>
</table>
## What to do next

Edit which notifications you receive [for a specific conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/connect/t_EditNotifRecAConv.md).

## Connect notification browser support

The following browsers support Connect chat notifications.

<table id="table_ipk_dgz_ww"><thead><tr><th>

Browser

</th><th>

Enable notification steps

</th></tr></thead><tbody><tr><td>

Chrome

</td><td>

1.  From a Chrome window, click the Chrome menu in the upper right corner.
2.  Go to **Settings** &gt; **Show advanced settings...** &gt; **Privacy** &gt; **Content settings**.
3.  In the Content settings window, from the notifications section, select your notification settings.

</td></tr><tr><td>

Mozilla Firefox \(starting with version 44\)

</td><td>

Manage browser notification settings using the information icon next to the URL.

</td></tr><tr><td>

Safari \(starting with OS X Mavericks\)

</td><td>

1.  From a Safari window, open **Preferences**.
2.  Select the notifications tab.
3.  Select **Allow** or **Deny** to control which websites have access to notifications.

</td></tr><tr><td>

Microsoft Edge

</td><td>

Notifications are enabled by default on Windows 10 PCs and tablets starting with EdgeHTML 14. For more information, see [https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge/\#pVkwubg7uvROayyI.97](https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge/#pVkwubg7uvROayyI.97).

</td></tr></tbody>
</table>**Note:** Internet Explorer does not support Connect notifications out of box.

