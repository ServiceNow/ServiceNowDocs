---
title: Create push message content
description: Push message content specifies additional JSON content in the push notification payload that is sent to the push provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/t\_CreateAMobileMessageLayout.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Push notification setup with a custom push application for ServiceNow mobile apps, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create push message content

Push message content specifies additional JSON content in the push notification payload that is sent to the push provider.

## Before you begin

Complete the following:

1.  [Activate push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_ActivatePushNotifications.md)
2.  \(iOS only\) [Upload a push certificate to your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/upload-push-cert.md)
3.  [Create a push application record for your custom app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAMobileApplication.md)

You must know how to use JSON with push messages.

Role required: admin or push\_admin

**Note:** This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at [Mobile push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/sg-mobile-push-notifications.md)

## About this task

Push message content defines the style of push notification that can be sent out for your custom app. You can add custom content, such as a picture, icons, or action buttons for the user to respond to the notification. Use the following variables in the script:

-   `current`: properties of the current record.
-   `message`: push message sent as the body of the entire push content.
-   `attributes`: object of the push message [attributes that you define](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAPushMessageAttribute.md).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Message Content**.

2.  In the Push Notification Message Contents table, click **New**.

3.  Fill out the fields on the Push Notifications Message Content form \(see table\).

4.  Click **Submit**.

    \[Omitted image "mobile\_layout.png"\] Alt text: Adding content with JSON

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name for the message content.|
    |Push app|The push application the content can be used with.|
    |Push Message Generation|Enter a script that determines the message content. See the example scripts.|
    |Related list|
    |Push Message Attribute Definitions|Select the attributes that apply to this notification. Attributes can be a value or an action. These attributes are used as default values for the content items you create in the content script. However, any attributes you create with the [push message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAPushMessage.md) can override these attributes. See [Create a push message attribute definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAPushMessageAttribute.md) for information on creating attributes.|


## Example

The following is an example of a content record that creates a two-button layout, one to approve something, such as a change request, and one to decline it.

```

var json = { 
  "table" : current.getTableName(), 
  "sys_id" : current.sys_id, 
  "template" : { 
    "type": "2 button", 
    "button1" : { 
      "title" : "Approve", 
      "action" : attributes.button_action, 
      "parameters" : { 
        "response" : "approve" 
       } 
     }, 
     "button2" : { 
       "title" : "Decline", 
       "action" : attributes.button_action, 
       "parameters" : { "response" : "decline" 
       } 
     } 
   } 
}; 
json;
```

## What to do next

[Define a push message attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateAPushMessageAttribute.md) to specify a default push action script or string that you can use in the push message content.

