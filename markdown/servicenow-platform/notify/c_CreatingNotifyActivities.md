---
title: Creating Notify activities
description: Default Notify workflow generally performs a single action, such as initiating a phone call. You can create custom Notify workflow activities to implement more complex functionality.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Creating Notify activities

Default Notify workflow generally performs a single action, such as initiating a phone call. You can create custom Notify workflow activities to implement more complex functionality.

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

**Parent Topic:**[Notify workflow activities](../../../administer/workflow-activities/concept/c_NotifyActivities.md)

**Related topics**  


[NotifyAction - Global](https://www.servicenow.com/docs/access?context=c_NotifyActionApi&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

