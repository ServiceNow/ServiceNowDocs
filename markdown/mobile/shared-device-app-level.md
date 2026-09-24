---
title: Configure shared device mode at app level
description: Learn how to configure multi-user login at the app level to enable multiple users to securely access a single ServiceNow mobile account from the same shared device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/shared-device-app-level.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Multiple users on a shared device, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Configure shared device mode at app level

Learn how to configure multi-user login at the app level to enable multiple users to securely access a single ServiceNow mobile account from the same shared device.

This feature lets users re-authenticate quickly with a personal PIN instead of repeatedly logging out and back in with full credentials. This is especially valuable in environments where workers can't carry personal devices, such as manufacturing, healthcare, and retail. In these environments shared devices are the norm and quick account switching is essential.

## Process workflow

The Multi-user login feature enables multiple users to securely access a single ServiceNow mobile account from the same shared device. After an initial login, each user configures a personal PIN for quick re-authentication, eliminating the need to repeatedly log out and back in with full credentials. This feature is especially valuable in environments where workers cannot carry personal devices. For example, in industries such as manufacturing, healthcare, and retail, where shared devices are the norm and quick account switching is essential.

**Note:** For more information on how users interact with this feature, see [Using a shared device with multiple users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/using-shared-device.md).

\[Omitted image "multiuser-users.png"\] Alt text: Quick Access page with multiple users added

## Configuration requirements

To enable multiple users to securely log into a single account on a ServiceNow app, the following mandatory considerations must be met:

-   The feature only works when a single account is configured on a mobile device. If the device has more than one account added, they need to be removed in order for the shared devices feature to work.
-   The mobile property **SupportSharedDevice**must be added and set to **True**.
-   The role **mobile\_shared\_device\_mode\_enabler** must be added to each user who needs to have the ability to change a device into one with a shared multi-user mode.

The instructions for each of these configurations are listed in the topic [Configure multiple users to use a shared device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/multi-user-create.md).

**Note:** When using SSO login with a shared device, you must set the SingleLogoutRequest service URL. For more information, see [Set the SingleLogoutRequest service URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/t_SetTheSingleLogoutRequestSvcURL.md).

The following optional properties can also be used with this feature:

-   The mobile property **EnablePushNotificationinSharedDeviceMode** is not available by default when the device is in shared mode. This is to ensure that notification of privacy and session separation are maintained. There is an option to override this configuration. In this situation, only the active user receives notifications.
-   **MaxUsersPerSharedDevice ** which limits the number of users on a shared device. The default is 15. The maximum number of users allowed per device is 30.
-   PINIdleTimeout defines the length of time users are allowed to remain inactive before being required to reenter their PIN. For more information, see [PIN timeout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/pin-timeout.md).

The instructions for each of these configurations are listed in the topic [Optional settings for multi-user configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/multi-user-optional.md)

