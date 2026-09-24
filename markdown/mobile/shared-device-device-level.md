---
title: Configure shared device mode at device level
description: Enable secure multi-user device sharing with Microsoft Entra ID Shared Device Mode. Users authenticate once at the device level to enable access across all Microsoft Entra-enabled apps. The configuration varies for Android and iOS devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/shared-device-device-level.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Multiple users on a shared device, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Configure shared device mode at device level

Enable secure multi-user device sharing with Microsoft Entra ID Shared Device Mode. Users authenticate once at the device level to enable access across all Microsoft Entra-enabled apps. The configuration varies for Android and iOS devices.

Shared device mode at a device level means one authentication unlocks every Microsoft Entra Shared Device Mode-enabled app. Signing out fully clears data across those apps to prepare the device for the next user. Shared-device and shift-based deployments serve multiple users on the same device. Microsoft Intune applies each user's app protection and configuration policies automatically based on who is currently signed in.

The following applies for shared device mode at a device level:

-   Signing in to any Microsoft Entra Shared Device Mode-enabled app on the device signs the user in to the ServiceNow app as well, and the reverse also applies.
-   Signing out of any Microsoft Entra Shared Device Mode-enabled app signs the user out of the ServiceNow app and clears ServiceNow data, so the next user starts fresh.
-   The device-level sign-in covers Microsoft Entra authentication only. Users still sign in to their ServiceNow instance separately, unless the instance uses single sign-on with Microsoft Entra through Microsoft Edge. In such a case the sign-in also completes automatically.

