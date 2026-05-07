---
title: General Guidelines for multiple users using a shared device
description: When configuring the setup for multiple users using a shared device, keep these general guidelines in mind for usability and a good user experience.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 2
breadcrumb: [Multiple users on a shared device, Configuring the Mobile Platform, Mobile Platform]
---

# General Guidelines for multiple users using a shared device

When configuring the setup for multiple users using a shared device, keep these general guidelines in mind for usability and a good user experience.

-   **Single account requirement**

    This feature only works on a single account. If there is more than one account on the device, the user must remove all other accounts they are not working with from the device.

-   **Assigning shared device enabler mode**

    The **mobile\_shared\_device\_mode\_enabler** role is available from the base system, however, it must be applied to selected users who can turn a device into a shared device.

-   **Enabling the shared device option**

    The Device sharing option in the **Settings** screen only displays if you add the mobile property **SupportSharedDevice** and set it to **True**. In addition, the user must be allocated the **mobile\_shared\_device\_mode\_enabler** role.

-   **Pre-loginand device sharing compatibility**

    The shared device and pre-login \(branded landing page\) features are designed for different personas and cannot work in parallel. If the pre-login feature is configured, the device sharing option is hidden.

    If the pre-login feature is configured on an instance after a device is already in shared mode, existing shared devices are not impacted. However, any new devices connecting to that instance cannot be used in shared mode.

-   **Syncing property changes to shared devices**

    The changes to following properties **PINIdleTimeou**t, **SupportSharedDevice**, and **MaxUsersPerSharedDevice ** on the server are updated on the device account when one of the following actions occur:

    -   An active user entered their PIN.
    -   An inactive user on the device logs back in.
    -   A new user is added.
    -   A pull-to-refresh has taken place while a user is logged in.
-   **Push notifications**

    Push notifications are disabled by default in shared device mode. When enabling push notifications on a shared device, be aware that other users on the device may be able to see each others notifications. Depending on the context of use, this could raise privacy or security concerns.

-   **Updating push notification properties**

    The property **EnablePushNotificationinSharedDeviceMode** on an instance is updated on the device account when one of the following actions occur:

    -   The app is restarted with an active user who has a valid login session.
    -   An inactive user on the device logs back in.
    -   A new user is added.
-   **Deep linking**

    Deep links that navigate the user to another account do not work, as you can only use a single account on a shared device. If the user taps such a link to be navigated to another account, they receive a message stating that the link cannot be opened on a shared device.

-   **MAM app configuration**

    Changes to either the **SNDefaultInstanceURL** or **SNDefaultInstanceName** properties in the MAM app configuration will not take effect once the application is converted to shared device mode. For more information, see [AppConfig for Mobile Apps](appconfig.md).

    **Note:** When using MAM/MDM with the multi-user feature, only the policies of the user who first authenticates into MAM/MDM are applied, even after the app is converted to shared mode.

-   **SSO and shared devices**

    When using SSO login with a shared device, you must set the **SingleLogoutRequest** service URL. For more information, see Set the SingleLogoutRequest service URL.

-   **Reverting to non-shared mode**

    To revert an app that is in shared mode back to non-shared mode, you must uninstall and reinstall the app.

-   **Unavailable features in shared mode**

    The following features are not available in shared mode:

    -   Mobile impersonation
    -   Biometric login
    -   Location tracking
    -   The ability to work in offline mode

