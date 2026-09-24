---
title: Configure shared device mode at the device level for Android devices
description: Configure shared device mode at the device level for Android devices using Microsoft Intune.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/shared-device-android-device.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Device-level configuration, Multiple users on a shared device, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Configure shared device mode at the device level for Android devices

Configure shared device mode at the device level for Android devices using Microsoft Intune.

## Before you begin

Role required: Intune Administrator or a custom role with enrollment program and device configuration rights.

## About this task

**Note:** Shared device mode for devices is supported starting from client version 22.1. However, it is not supported in Mobile Publishing builds on Android.

Shared device mode allows multiple users to securely sign in and out of a single Android device while keeping ServiceNow apps and data isolated per session. Configuring shared device mode for Android devices involves the following steps:

-   Set up Intune enrollment of Android Enterprise dedicated devices to configure and manage corporate-owned devices for use as a shared device.

    **Note:** The configuration of this step is listed in the following [Microsoft documentation](https://learn.microsoft.com/en-us/intune/device-enrollment/android/setup-dedicated). The set up step in this topic, highlights specific areas where changes are required when working with ServiceNow apps.

-   Assign the ServiceNow apps as required to the enrollment group.
-   Enroll the device, after which the ServiceNow apps install automatically.

-   **Related links**

    [Overview of shared device mode - Microsoft Entra ID feature](https://learn.microsoft.com/en-us/entra/identity-platform/msal-shared-devices)


## Procedure

1.  Follow all the instructions in the following Microsoft webpage, [Set up Intune enrollment of Android Enterprise dedicated devices](https://learn.microsoft.com/en-us/intune/device-enrollment/android/setup-dedicated).

    When working through these instructions, you must apply the following specific configurations when working with ServiceNow apps:

    -   In the section [Create an enrollment profile](https://learn.microsoft.com/en-us/intune/device-enrollment/android/setup-dedicated#create-an-enrollment-profile), select the token type in Step 6, to be **Corporate-owned dedicated device with Microsoft Entra ID shared mode**.
    -   In the section [Create an enrollment profile](https://learn.microsoft.com/en-us/intune/device-enrollment/android/setup-dedicated#create-an-enrollment-profile), you must complete Step 8 \(even though it's listed as optional\) to select where to group devices at enrollment time.
2.  Follow all the instructions in the following Microsoft webpage, [Assign Apps to Groups With Microsoft Intune](https://learn.microsoft.com/en-us/intune/app-management/deployment/assign-groups).

    When working through the instructions select **Required** as the assignment type in Step 7 of the [Assign an app](https://learn.microsoft.com/en-us/intune/app-management/deployment/assign-groups#assign-an-app) section.

3.  Follow all the instructions in the following Microsoft webpage, [Enroll your Android Enterprise dedicated, fully managed, or corporate-owned with work profile devices](https://learn.microsoft.com/en-us/intune/device-enrollment/android/ref-corporate-methods).


## Result

After you enroll the device, the apps deployed in the previous steps install automatically. This process is can take time before the apps display.

