---
title: Enable multiple users to work on a shared device
description: Enable multiple users to log into a ServiceNow mobile account from a single mobile device. This is beneficial in environments where devices are shared, as it offers secure and personalized access through user-configured PINs, eliminating the need for repetitive full authentications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-26"
reading_time_minutes: 2
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Enable multiple users to work on a shared device

Enable multiple users to log into a ServiceNow mobile account from a single mobile device. This is beneficial in environments where devices are shared, as it offers secure and personalized access through user-configured PINs, eliminating the need for repetitive full authentications.

The Multi-user login feature enables multiple users to securely access a single ServiceNow mobile account from the same shared device. After an initial login, each user configures a personal PIN for quick re-authentication, eliminating the need to repeatedly log out and back in with full credentials. This feature is especially valuable in environments where workers cannot carry personal devices. For example, in industries such as manufacturing, healthcare, and retail, where shared devices are the norm and quick account switching is essential.

**Note:** For more information on how users interact with this feature, see [Using a shared device with multiple users](../reference/using-shared-device.md).

![An example of the Quick Access page with multiple users added](../image/multiuser-users.png)

## Configuration requirements

To enable multiple users to securely log into a single account on a ServiceNow app, the following mandatory considerations must be met:

-   The feature only works when a single account is configured on a mobile device. If the device has more than one account added, they need to be removed in order for the shared devices feature to work.
-   The mobile property **SupportSharedDevice**must be added and set to **True**.
-   The role **mobile\_shared\_device\_mode\_enabler** must be added to each user who needs to have the ability to change a device into one with a shared multi-user mode.

The instructions for each of these configurations are listed in the topic [Configure multiple users to use a shared device](../task/multi-user-create.md).

**Note:** When using SSO login with a shared device, you must set the SingleLogoutRequest service URL. For more information, see Set the SingleLogoutRequest service URL.

The following optional properties can also be used with this feature:

-   The mobile property **EnablePushNotificationinSharedDeviceMode** is not available by default when the device is in shared mode. This is to ensure that notification of privacy and session separation are maintained. There is an option to override this configuration. In this situation, only the active user receives notifications.
-   **MaxUsersPerSharedDevice ** which limits the number of users on a shared device. The default is 15. The maximum number of users allowed per device is 30.
-   PINIdleTimeout defines the length of time users are allowed to remain inactive before being required to reenter their PIN. For more information, see [PIN timeout](../task/pin-timeout.md).

The instructions for each of these configurations are listed in the topic [Optional settings for multi-user configuration](../task/multi-user-optional.md)

