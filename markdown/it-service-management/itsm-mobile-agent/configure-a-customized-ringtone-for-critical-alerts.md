---
title: Configure a ringtone for critical alerts
description: Select a preferred ringtone for your critical notifications in ITSM Mobile Agent application.
locale: en-US
release: zurich
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [ringtone]
breadcrumb: [Enable Override do not disturb to receive critical alerts, Configure, ITSM Mobile Agent, IT Service Management]
---

# Configure a ringtone for critical alerts

Select a preferred ringtone for your critical notifications in ITSM Mobile Agent application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Search and select **CriticalPushPayloadBuilder** from the list of scripts.

    Ensure that the selected script **CriticalPushPayloadBuilder** is in **ITSM Mobile Agent** application scope.

3.  Open the **CriticalPushPayloadBuilder** record and edit the script with your preferred ringtone name:

    ```
    var CriticalPushPayloadBuilder = Class.create();
    CriticalPushPayloadBuilder.prototype = {
        initialize: function(currentGR, json, attributes) {
            this.currentGR = currentGR;
            this.json = json;
            this.attributes = attributes;
        },
        buildJSON: function() {
            if (this.attributes == null || this.attributes.isCritical == null || !(this.attributes.isCritical == "true"))
                return this.json;
            this.json["sncGoogleKeys"] = {
                "android": {
                    "priority": "high"
                },
                "priority": "high"
            };
            this.json["aps"]["sound"] = {
                "critical": 1,
                "name": "NotificationAlert-9-Short.caf",
                "volume": 1
            };
            return this.json;
        },
        type: 'CriticalPushPayloadBuilder'
    };
    ```

    You can select ringtones from below options:

    -   NotificationAlert-1.caf
    -   NotificationAlert-2.caf
    -   NotificationAlert-3.caf
    -   NotificationAlert-4.caf
    -   NotificationAlert-5.caf
    -   NotificationAlert-6.caf
    -   NotificationAlert-7.caf
    -   NotificationAlert-8.caf
    -   NotificationAlert-9.caf
    -   NotificationAlert-10.caf
    -   NotificationAlert-11.caf
    -   NotificationAlert-12.caf
    -   NotificationAlert-13.caf
    -   NotificationAlert-14.caf
4.  Select **Update**.


