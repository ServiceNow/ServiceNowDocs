---
title: Set custom alert tones in ITSM Mobile Agent for incident priorities
description: Set custom alert tones in ITSM Mobile Agent to distinguish between incidents with different priorities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/set-alert-tones-incident-priority.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Set custom alert tones in ITSM Mobile Agent for incident priorities

Set custom alert tones in ITSM Mobile Agent to distinguish between incidents with different priorities.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push Message Content**.

    Alternatively, navigate to the Push Notification Message Content \[sys\_push\_notif\_msg\_content\] table.

2.  Select the required push notification message content record.

3.  Update the **Push Message Generation** field with the following script.

    ```
    // get the priority of current incident
    var currentIncPriority =  current.getValue("priority");
    // define an array to map priority with ringtone
    var customisedRingtones = [
          {
                "priority": "1",
                "ringtone": "default"
            },
            {
                "priority": "2",
                "ringtone": "default"
            },
            {
                "priority": "3",
                "ringtone": "default"
            },
            {
                "priority": "4",
                "ringtone": "default"
            },
            {
                "priority": "5",
                "ringtone": "default"
            }];
    //override the json["aps"]["sound"] param with the ringtone defined for current priority        
            if(customisedRingtones){
                for(var i=0;i<customisedRingtones.length;i++){
                   if(customisedRingtones[i].priority && customisedRingtones[i].priority === currentIncPriority){
                   json["aps"]["sound"] = customisedRingtones[i].ringtone;
                    break;
                   }
                }
            }
    ```

    **Note:** In the script, replace each default ringtone value with the name of the alert tone to use. For a list of available ringtones and alert tones, see [Configure sounds for push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/push-notif-sounds.md).

4.  Select **Update**.


