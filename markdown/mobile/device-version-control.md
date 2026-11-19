---
title: App and device version compatibility messages
description: Administrators can set minimum app and operating system \(OS\) versions for mobile users. When an app or device becomes unsupported, a status message notifies the user of what needs to be updated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/device-version-control.html
release: brazil
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [mobile update, ios update, android update]
breadcrumb: [Tested devices/supported versions, Configuring the Mobile Platform, Mobile Platform]
---

# App and device version compatibility messages

Administrators can set minimum app and operating system \(OS\) versions for mobile users. When an app or device becomes unsupported, a status message notifies the user of what needs to be updated.

## Version check sequence

Administrators set a minimum app version, OS version, or both for each platform. The app checks versions in the following order when users restart the app, pull to refresh, or start to log in:

1.  Device OS: If the OS is below the minimum, the **Device OS update required** dialog tells users to update in device settings or use another device.
2.  App version: If the app is below the minimum, the **App update required** dialog gives the required version and an **Update** button that opens the App Store or Google Play.
3.  Instance compatibility: If an instance upgrade makes the app version incompatible, a dialog tells users to contact an administrator. Users who are logged in are also logged out.

Users can’t dismiss these dialogs. After users fix an issue and restart the app, the next check runs. If no minimum is set, the app skips the OS and app version checks.

## Considerations

Consider the following when you use minimum version enforcement:

-   The app doesn’t check the app store for the latest version. Enforcement starts only when an administrator sets a minimum.
-   Enforcement applies to all users of an app. You can’t target individual users or roles.
-   An empty or invalid version value disables that check for the platform.
-   Changes take effect the next time the app restarts or the user pulls to refresh.
-   On accounts with multiple instances, a dialog blocks only the affected instance.
-   Builds distributed through a private app store don’t show app update dialogs. The OS and instance dialogs still appear.

