---
title: Pass event parameters from a work-flow to a notification
description: Pass two event parameters that send information about a record or related records from a work-flow to a notification.
locale: en-US
release: australia
product: System Events
classification: system-events
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing system events, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# Pass event parameters from a work-flow to a notification

Pass two event parameters that send information about a record or related records from a work-flow to a notification.

## Before you begin

Role required: events\_admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Events** &gt; **Registry** and define a new event to call.

2.  Create the activity step that calls the event from your workflow and assign the two possible parameters.

    These parameters can be references or fields on the record that triggered the workflow, such as **current.number** for the request item number. You can also dot-walk to records in other tables. The event then sends the parameters information to the notification that it triggers.

3.  Retrieve the parameters in the notification with email scripts by using **event.parm1** and **event.parm2**.

    For example:

    ```
    
    var string = event.parm1.toString(); 
    template.print(string);
    
    ```


## Example

Another example using Sys IDs gives you access to anything in the record that triggered the workflow. Use a script like this to send information about a change or request to support personnel, for example.

```

var id = event.parm1.toString(); 
var gr = new GlideRecord('sc_req_item'); 
gr.get('sys_id', id); 
if (gr.next()){
   // Do something.
}

```

**Parent Topic:**[Managing system events](../../platform-events/concept/managing-system-events.md)

**Related topics**  


[Scripting for email notifications](../../../script/server-scripting/concept/c_ScriptingForEmailNotifications.md)

