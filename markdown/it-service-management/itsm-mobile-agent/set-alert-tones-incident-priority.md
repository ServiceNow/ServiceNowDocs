---
title: Set custom alert tones in ITSM Mobile Agent for different incident priority
description: Set custom alert tones in ITSM Mobile Agent to distinguish between incidents with different priorities.
locale: en-US
release: yokohama
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, ITSM Mobile Agent, IT Service Management]
---

# Set custom alert tones in ITSM Mobile Agent for different incident priority

Set custom alert tones in ITSM Mobile Agent to distinguish between incidents with different priorities.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push Message Content**.

    Alternatively, you can also go to the Push Notification Message Content \[sys\_push\_notif\_msg\_content\] table.

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

    **Note:** Replace the ringtone with the desired alert tone name. For more information on the list of ringtones and alert tones available to update the script, see [Configure sounds for push notifications](https://www.servicenow.com/docs/access?context=push-notif-sounds&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

4.  Select **Update**.


