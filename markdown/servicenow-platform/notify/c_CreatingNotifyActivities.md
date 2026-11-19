---
title: Creating Notify activities
description: Create custom Notify workflow activities to do more than the single action, such as starting a phone call, that the default workflow performs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/notify/c\_CreatingNotifyActivities.html
release: australia
product: Notify
classification: notify
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Creating Notify activities

Create custom Notify workflow activities to do more than the single action, such as starting a phone call, that the default workflow performs.

Use event handler functions in each Notify activity definition to design your own activity behavior. For example, you can set the activity result if the caller hangs up by using the onCompleted function.

```
onCompleted: function() {
activity.result = 'call_ended';
},
```

When creating a new Notify workflow activity, follow these design principles.

-   Within onExecute event handler function, create a new NotifyAction object. Use this object to create a simple or complex action, then serialize the object to the notify\_wf\_activity table.
-   Within the onUpdate event handler function, deserialize the NotifyAction object from the notify\_wf\_activity table and use this object to perform any other operations.
-   Use the other event handler functions and the Notify as needed to implement the desired activity behavior.

**Parent Topic:**[Notify workflow activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/notify/c_NotifyActivities.md)

**Related topics**  


[NotifyAction - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_NotifyActionApi.md)

