---
title: Add a push notification message content record
description: The push notification message content record contains the location users are directed to when they tap on a notification, as well as the appearance and layout of the notification.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Add a push notification message content record

The push notification message content record contains the location users are directed to when they tap on a notification, as well as the appearance and layout of the notification.

## Before you begin

Role required: admin

Complete the Push Notification Message Content form to:

-   Name the notification.
-   Select the mobile application to which the notification is sent.
-   Optionally, customize the appearance of the notification message.

This information is saved in the Push Notification Message Contents \[sys\_push\_notif\_msg\_content\] table.

## Procedure

1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Message Content**.

2.  Select **New**.

3.  In the Push Message Content form, fill in the following fields:

<table id="table_fbr_1vm_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the push message content record.**Note:** This name is not visible in the notification, it is only a reference for use during configuration.

</td></tr><tr><td>

Push app

</td><td>

Mobile application to send the notification to. This is the application that you added in "Add a push application record".

</td></tr><tr><td>

Push Message Generation

</td><td>

Script block that contains the notification link. To implement push notifications in a Mobile SDK Virtual Agent application, use the following script:```
(function buildJSON(/*GlideRecord*/ current, /*String*/ message, /*Object*/ attributes) {

 var json = { 
   "aps": {
     "alert": {
       "title": current.push_title,
       "body": sn_cs.VASystemObject.getTextValueForMessage(current.message_id)
    },
      "sound": "default",
      "thread-id": "launch_virtual_agent"
  }, 
  "type": "launch_virtual_agent"
};

 return json;

})(current, message, attributes);
```

</td></tr></tbody>
</table>4.  Select **Submit**.


