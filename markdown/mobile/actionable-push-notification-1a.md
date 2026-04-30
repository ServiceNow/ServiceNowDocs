---
title: Actionable push notification script example
description: You can use this JSON script example to configure an actionable push notification for ServiceNow mobile apps.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure actionable push notifications, Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Actionable push notification script example

You can use this JSON script example to configure an actionable push notification for ServiceNow® mobile apps.

## Example script

The following example script creates a push notification that your users can see on their mobile devices.

**Important:** The globally unique identifier in the following script \(`"70bbc19c87f901101ae365b83cbb3559"`\) is the sys\_id of the push notification record found on the push notification table \[sys\_sg\_push\_notification\]. Make sure that the identifier in the script your system generates matches the sys\_id of your push notification.

```
(function buildJSON(/*GlideRecord*/ current, /*String*/ message, /*Object*/ attributes) {

     var layoutFields = {"Identifier" : "number", "Description" : "short_description", "Status" : "state" };
       return new global.ActionablePushPayloadBuilder(current, "70bbc19c87f901101ae365b83cbb3559", layoutFields).buildJSON(); 

})(current, message, attributes);
```

**Parent Topic:**[Configure actionable push notifications](../concept/actionable-push-notification.md)

