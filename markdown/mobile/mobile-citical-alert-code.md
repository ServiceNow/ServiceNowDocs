---
title: Configure code for critical alerts
description: You can make a push notification into a critical alert with the addition of some JSON code. Different JSON code is used for iOS and Android operating systems and for the ITSM business unit.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Mobile critical alerts, Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure code for critical alerts

You can make a push notification into a critical alert with the addition of some JSON code. Different JSON code is used for iOS and Android operating systems and for the ITSM business unit.

When creating critical alert notifications, you need the code structure of a push notification message as well as the required JSON code that defines the notification as a critical alert. You add this code in the Push message content area. For more information, see [Mobile critical alerts](../task/mobile-critical-alerts-create.md).

**Important:**

On the Android platform, when a user receives a critical alert on certain phone types, they may experience the following device behavior:

-   **OnePlus devices with hardware-controlled ringer mode:**

    On devices like OnePlus where the ringer mode is controlled by a physical switch, the app might not be able to override the notification sound volume if the device is set to silent or vibrate mode.

-   **OnePlus or Oppo device Do Not Disturb mode behavior:**

    On certain devices, like Oppo and OnePlus, if Do Not Disturb \(DND\) mode is enabled, the DND setting might be temporarily turned off until the critical notification sound has finished playing.


On Android clients, version 20.0.0 and later, critical alerts don't work on the following:

-   The Android Private Space feature that was introduced in Android 15.
-   Android devices that are managed by Mobile Device Management \(MDM\) software. For example, Microsoft Intune.

## Critical alert JSON to activate Android operating systems

The following code must be added to the JSON code because it activates Android devices to wake up so that a critical alert can be triggered.

**Note:** Because users use both iOS and Android devices you must add this code. The JSON entry in the code is a returned dictionary name value from the scripting.

```
 

json["sncGoogleKeys"] = { 
          "android": { 
              "priority": "high" 
          }, 
          "priority": "high" 
      }; 

```

## Critical alert JSON for all operating systems

The following JSON must be added so that a notification behaves as a critical alert.

```
var json = {};
json["aps"] = { 
"sound": {
          "critical": 1, 
          "name": "NotificationAlert-1.caf", 
          "volume": 1.0 
}
      };

```

The parameters in the sample JSON code are as follows:

-   The **critical** parameter defines the notification as a critical alert. `1` means the critical alert is active, `0` means the critical alert is inactive.
-   The **name** parameter is the name of the tone that is activated when a critical alert is sent. Some tones for critical alerts are listed in the table. For a complete list, see [Configure sounds for push notifications](push-notif-sounds.md).

    |Accepted file name values|Tone rhythm|
    |-------------------------|-----------|
    |`NotificationAlert-2.caf`|Dramatic|
    |`NotificationAlert-2-Short.caf`|Dramatic|
    |`NotificationAlert-9.caf`|Dramatic, Powerful|
    |`NotificationAlert-9-Short.caf`|Dramatic, Powerful|
    |`NotificationAlert-10.caf`|Dramatic, Suspenseful|
    |`NotificationAlert-10-Short.caf`|Dramatic, Suspenseful|

    **Note:** If a **name** value isn’t defined, the system uses the application’s default ringtone. If an application doesn't have a defined ringtone, then the system uses the device's default ringtone.

-   The **volume** parameter defines the volume of the critical alert sound. The range is from `0.1` as the quietest to `1.0` as the loudest.

## Example JSON code block for critical alert

The following is a complete example block of JSON code that you must add and configure to activate a critical alert for Android and iOS devices.

```
json["sncGoogleKeys"] = { 
          "android": { 
              "priority": "high" 
          }, 
          "priority": "high" 
      }; 
  
json["aps"]["sound"] = { 
          "critical": 1, 
          "name": "NotificationAlert-1.caf", 
          "volume": 1.0 
      };
```

## IT Service Management \(ITSM\) CriticalPushPayloader script include

The **Push message content** area may contain previously configured code including the script include `CriticalPushPayLoadBuilder`, created by the ITSM business unit. If so, then no additional configuration is required for critical alerts. Script includes  are reusable server-side script logic that define a function or class.  `CriticalPushPayLoadBuilder` is a script include that contains functions to support critical alerts. The call of the script includes looks like this: `CriticalPushPayloadBuilder (current, json, attributes).buildJSON()`

**Note:** If you need to change the values of the `Volume` or `Name` parameters, or change the alert from critical to non-critical, you need to access the function parameters that the script include is getting as inputs.

Changing the value of the critical alert script include affects all ITSM implementations of the script include. Similarly, an ITSM plugin upgrade could override your changes to your script include.

**Parent Topic:**[Mobile critical alerts](../task/mobile-critical-alerts-create.md)

