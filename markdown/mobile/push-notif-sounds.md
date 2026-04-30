---
title: Configure sounds for push notifications
description: Add sounds and tones to push notifications to indicate to users if a message is urgent or just requires the users' attention.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Components, Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure sounds for push notifications

Add sounds and tones to push notifications to indicate to users if a message is urgent or just requires the users' attention.

## Example JSON for adding sound to push notifications

The following JSON is an example of how to add a tone to your push notification. The name of the tone used in the example is NotificationAlert-2".

```
json["aps"]["sound"] = "NotificationAlert-2.caf";
```

The table at the end of this topic list all the available tones. To listen to the tone of each sound, you must configure a notification with the target sound parameter.

**Note:** For each tone, you have the option to shorten the length of the ring by adding the suffix `-Short`. You can shorten all tones except `NotificationAlert-5.caf`.

## Example JSON for critical alerts including sound

The following JSON is an example of how the sound parameter is defined for critical alerts. For more information about critical alerts, see [Mobile critical alerts](../task/mobile-critical-alerts-create.md).

```
json["aps"]["sound"] = { 
          "critical": 1, 
          "name": "NotificationAlert-3-Short.caf", 
          "volume": 1.0 
      }; 

```

The parameters in the sample JSON code are as follows:

-   The **critical** parameter defines the notification as a critical alert. `1` means that the critical alert is active, `0` means that the critical alert is inactive.
-   The **volume** parameter defines the volume of the notification sound. The range is from `0.1` as the quietest to `1.0` as the loudest.
-   The **name** parameter is the name of the tone that is activated when a push notification is sent. For critical alerts, considering user rhythms with a dramatic tone.

    **Note:** If a **name** value isn’t defined, the system uses the application’s default ringtone. If an application doesn't have a defined ringtone, then the system uses the device's default ringtone.

    To listen to the tone of each sound, you must configure a notification with the target sound parameter.

    Accepted values are listed in the table.

    **Note:** For each tone, you have the option to shorten the length of the ring by adding the suffix `-Short`. You can shorten all tones except `NotificationAlert-5.caf`.

    |Accepted file name values|Tone rhythm|
    |-------------------------|-----------|
    |`NotificationAlert-1.caf`|Mellow, Relaxing, Slow|
    |`NotificationAlert-1-Short.caf`|Mellow, Relaxing, Slow|
    |`NotificationAlert-2.caf`|Dramatic|
    |`NotificationAlert-2-Short.caf`|Dramatic|
    |`NotificationAlert-3.caf`|Dramatic|
    |`NotificationAlert-3-Short.caf`|Dramatic|
    |`NotificationAlert-4.caf`|Mellow, Relaxing, Slow|
    |`NotificationAlert-4-Short.caf`|Mellow, Relaxing, Slow|
    |`NotificationAlert-5.caf`|Mellow, Relaxing, Slow|
    |`NotificationAlert-6.caf`|Festive, Happy|
    |`NotificationAlert-6-Short.caf`|Festive, Happy|
    |`NotificationAlert-7.caf`|Festive, Happy|
    |`NotificationAlert-7-Short.caf`|Festive, Happy|
    |`NotificationAlert-8.caf`|Festive, Happy|
    |`NotificationAlert-8-Short.caf`|Festive, Happy|
    |`NotificationAlert-9.caf`|Dramatic, Powerful|
    |`NotificationAlert-9-Short.caf`|Dramatic, Powerful|
    |`NotificationAlert-10.caf`|Dramatic, Suspenseful|
    |`NotificationAlert-10-Short.caf`|Dramatic, Suspenseful|
    |`NotificationAlert-11.caf`|Dramatic|
    |`NotificationAlert-11-Short.caf`|Dramatic|
    |`NotificationAlert-12.caf`|Dramatic|
    |`NotificationAlert-12-Short.caf`|Dramatic|
    |`NotificationAlert-13.caf`|Dramatic|
    |`NotificationAlert-13-Short.caf`|Dramatic|
    |`NotificationAlert-14.caf`|Dramatic|
    |`NotificationAlert-14-Short.caf`|Dramatic|


**Note:** If a name value isn’t defined, the system uses the application’s default ringtone. If an application doesn't have a defined ringtone, then the system uses the device's default ringtone.

**Parent Topic:**[Mobile push notification components](../concept/configure-mobile-push-notifications.md)

