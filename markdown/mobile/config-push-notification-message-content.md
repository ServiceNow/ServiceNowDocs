---
title: Configure push notification message content
description: Configure push notification message content and select which mobile application receives notifications. You can configure critical alert notifications, customize the message appearance, and determine the deep link used when users tap the notification.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Components, Push notifications, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure push notification message content

Configure push notification message content and select which mobile application receives notifications. You can configure critical alert notifications, customize the message appearance, and determine the deep link used when users tap the notification.

## Before you begin

To configure push notification message content, you must generate a deep link using the mobile deep link generator. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).

Role required: admin

## About this task

Complete the Push Message Content form to:

-   Name the notification
-   Select the mobile app that the notification is sent to
-   Optionally customize the appearance of the notification message
-   Determine the deep link used when users tap the notification

Push notification message content supports up to three additional fields. If these fields are used as optional text slots, the slots can display fields from the source record.

**Note:** The text slots are fixed on the mobile app, so you cannot change their location or size. Each slot maps to a `Status`, `Identifier`, and `Description` within the JSON object in the push notification message content script.

Mobile UI styles are also available for additional fields. For more information around styling, see [Mobile UI styles](../concept/mobile-ui-styles.md).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Message Content**.

2.  Select **New**.

3.  In the Push Message Content form, fill in the following fields:

<table id="table_fbr_1vm_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String value for this record.**Note:** This name is not visible in the notification, it is only a reference for use during configuration.

</td></tr><tr><td>

Push app

</td><td>

References the mobile app you want to send a notification to.-   Use ServiceNow mobile Application for Mobile Agent.
-   Use ServiceNow Request Application for Now Mobile app.


</td></tr><tr><td>

Push Message Generation

</td><td>

The script block that contains the notification link. In the script block, the JSON object must return a link and a `Link` key must exist. The key should have a corresponding deep link value generated through the mobile deep link generator.

</td></tr></tbody>
</table>    This example shows the completed form and a JSON object with the appropriate `Link` key and a corresponding deep link value.![Push Message Content form with all of the fields completed and an example deep link indicated by Link key.](../image/mobile-push-content-deep-link-sample.png)

4.  Add additional fields to the notification content, such as a text slot.

    In the **Push Message Generation** script block, create a layout field object for each field.

    1.  Instantiate a notification layout object.

        ```
        var layoutGen = new global.NotificationLayoutFieldGenerator();
        ```

    2.  Use the notification layout script and include the global application scope to generate layout fields.

        To learn more about script includes, see Script Includes.

        **Note:** Do not modify the notification layout generator script include.

    3.  Create the layout field.

        Each layout field requires a `Table`, `Sys_Id`, and a `Column`.

        **Note:** The `Table` and `Sys_Id` values should come directly from the current record using `current.getTableName()` and `current.sys_id`. The `Column` value must exist for the desired table and match the dictionary column name exactly.

        ```
        var text_01 = layoutGen.layoutField(current.getTableName(), current.sys_id, "priority");
        ```

    4.  Pass the layout fields into the original JSON object as another object.

        The mobile applications listen for the optional `Layout` key, which is an object that contains the desired additional fields. In the `Layout` object, associate each additional field with the `Status`, `Identifier`, or `Description` keys. The following example is available as a reference.

        ```json
        (function buildJSON( /*GlideRecord*/ current, /*String*/ message, /*Object*/ attributes) { 
        
            var layoutGen = new global.NotificationLayoutFieldGenerator(); 
            var text_01 = layoutGen.layoutField(current.getTableName(), current.sys_id, "priority"); 
            var text_02 = layoutGen.layoutField(current.getTableName(), current.sys_id, "state"); 
            var text_03 = layoutGen.layoutField(current.getTableName(), current.sys_id, "short_description"); 
        
            var deepLinkGenerator = new global.MobileDeepLinkGenerator("Request"); 
            var link = deepLinkGenerator.getFormScreenLink("b71040b1533a33007bc2ddeeff7b1221", current.getTableName(), current.getValue("sys_id")); 
        
            var json = { 
        
                "Link": link, 
        
                "Layout": { 
        
                    "Status": text_01, 
        
                    "Identifier": text_02, 
        
                    "Description": text_03 
        
                } 
        
            }; 
        
            return json;
        
        })(current, message, attributes);
        ```

5.  Add a customized notification title.

    If you don't add a customized notification title, the notification displays the default mobile app name.

    ![Image showing the difference between a standard notification message title that displays the mobile app name and a custom title that describes the notification.](../image/mob-cust-not-tit-with-callout.png)

    In the **Push Message Generation** script block, add the following example code in the `json` section:

    ```
    var json= {};
    var msg_title  = "System updates!";
    json= {
      "android_title" : msg_title,
      "aps": {
        "alert": {
          "title": msg_title,
        }
      }
    
    ```

    The elements in the sample JSON code are as follows:

    -   The **msg\_title** variable called `System updates!` is the notification title name that applies to both iOS and Android.
    -   The node`json["android_title"]` is the variable for Android.
    -   The node `json["aps"]["alert"]["title"]` is the variable for iOS.
6.  Add the following code to activate Android devices to wake up, so that notifications can be triggered.

    As users use both iOS and Android devices you must add this code. The JSON entry in the code is a returned dictionary name value from the scripting.

    Android specific fields that control message delivery are supported under **sncGoogleKeys**. For more information, see [Firebase Cloud Messaging HTTP Protocol](https://firebase.google.com/docs/cloud-messaging/http-server-ref#downstream-http-messages-json).

    **Note:** The **priority** parameter is set to `high` to wake up Android devices, if a device is in sleep mode. This parameter helps to deliver critical alerts to end users.

    ```
    json["sncGoogleKeys"] = {
        "priority": "high",
        "android": {
          "priority": "high"
        }
    }
    
    ```

7.  Select **Update**.


## Result

You created a push notification message content record that contains a deep link.

## What to do next

After configuring push notification message content, it must be paired with a push notification message record. For more information on configuring a push notification message, see [Configure a push notification message](configure-push-notification-message.md).

**Parent Topic:**[Mobile push notification components](../concept/configure-mobile-push-notifications.md)

