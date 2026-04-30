---
title: Configure push notifications for mobile activity stream mentions
description: Enable users to alert their contacts, through the use push notifications, that they are mentioned in a thread. The user enters the @ character followed by the contact's name in a record's activity stream, for their contact to be alerted.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure activity stream notifications, Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure push notifications for mobile activity stream mentions

Enable users to alert their contacts, through the use push notifications, that they are mentioned in a thread. The user enters the `@` character followed by the contact's name in a record's activity stream, for their contact to be alerted.

## Before you begin

Role required: admin

## Procedure

1.  Create the push notification message content, which defines where you are pushing the notification to.

    1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Message Content** in the filter navigator.

    2.  In the Push Notification Message Content form, select **New**.

    3.  On the form, fill in the fields.

<table id="table_lkl_pyb_znb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your push message content record. This name is not visible to your users.

</td></tr><tr><td>

Application

</td><td>

Scoped application associated with this record. This field defaults to the current application.

</td></tr><tr><td>

Push app

</td><td>

Mobile app that uses your push notification.-   Enter **ServiceNow Mobile Application** for the Mobile Agent app.
-   Enter **ServiceNow Request Application** for the Now Mobile app.


</td></tr></tbody>
</table>    4.  In the **Push Message Generation** field, copy the following sample JSON code and paste it in the field.

        ```
        (function buildJSON(/*GlideRecord*/ current, /*String*/ message, /*Object*/ attributes) {
        
            var layoutFieldGenerator = new global.NotificationLayoutFieldGenerator();
            var json = {};
        	var deepLinkGenerator = new global.MobileDeepLinkGenerator("<client type>");
        		
            var link = deepLinkGenerator.getFormScreenLink('<form_screen_sys_id>', current.getValue("table"), current.getValue("document"));
            json = {
                "aps" : {
                    "sound" : "default"
                },
                "Link": link
            };
            
            return json;
            
        })(current, message, attributes);
        ```

        Customize the values in the code:

        1.  Locate the sys\_id of the record screen by right-clicking on the screen name and selecting **Copy sys\_id**.
        2.  Replace the `<form_screen_sys_id>` portion of the code with the sys\_id.
        3.  Define a client type in the variable `global.MobileDeepLinkGenerator` Possible values are:
            -   agent
            -   request
            -   onboarding
    5.  Select **Submit**.

2.  Create a message for the user's contacts to receive when they are mentioned in a record's activity stream.

    1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Messages**.

    2.  In the Push Notification Message form, select **New**.

    3.  On the form, fill in the fields.

<table id="table_qdf_51c_znb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your push message content record. This name is not visible to your users.

</td></tr><tr><td>

Application

</td><td>

Scoped application associated with this record. This field defaults to the current application.

</td></tr><tr><td>

Push app

</td><td>

Mobile app that uses your push notification.**Note:** Make sure to enter the same mobile app entered in the **Push app** field in the Push Notification Message Content form.

</td></tr><tr><td>

Push Message Content

</td><td>

Select the push message content you created.

</td></tr><tr><td>

Table

</td><td>

Table containing the records relating to your notification. Select `live_notification`.

</td></tr><tr><td>

Message

</td><td>

Message that appears to the user's contacts, informing them they are mentioned.

</td></tr></tbody>
</table>    4.  Select **Submit**.

3.  Create the push notification and define when to send it, who receives it, and what it contains.

    1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Notifications**.

    2.  In the Push Notification view form, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your push notification. This name is not visible to your users.|
        |Active|Option for determining whether the push notification is active. Select this option.|
        |Table|Table containing the records relating to your notification. Select the same table as the push notification view form, `live_notification`.|
        |Push Message Only|Option that determines whether to send a push notification to a mobile device. This field is automatically selected and is read-only by default.|
        |Category|Category to which this notification belongs. A category identifies and groups related notifications. This category defines which actions are available in the push notification.|

    4.  Select the **When to send** tab and then select **Inserted**.

    5.  Select the **Who will receive** tab and then select the lock icon \(![Lock icon.](../image/lock-icon.png)\) in the **Users/Groups in fields**.

    6.  Move **User** to the selected list.

        **Note:** If the notification is addressed to a user with an inactive record in the User \[sys\_user\] table, the notification is not sent.

    7.  Select the **What to send** tab and select the lock icon \(![Lock icon.](../image/lock-icon.png)\) next to the **Push Messages** field.

    8.  Select the reference lookup icon \(![Reference lookup icon.](../image/reference-lookup-icon.png)\) to open the Push Notification Messages page.

    9.  Select the push notification message you created.

        The push notification is listed as one of the available messages in the **What to send** tab.

    10. Select **Submit**.

4.  Enable your mobile app settings for notifications.

    1.  Select the Settings icon \(![Settings icon.](../image/GearIcon.png)\) and select the **Notifications** tab.

    2.  Verify that **Allow Notifications** is enabled.

    3.  Verify that the mobile app you selected to receive notifications is enabled by noting the setting of either the **ServiceNow Mobile Application** or **ServiceNow Request application** field.


**Parent Topic:**[Configure notifications for mobile activity stream mentions](../concept/notification-activity-stream.md)

