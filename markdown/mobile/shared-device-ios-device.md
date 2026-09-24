---
title: Configure shared device mode at the device level for iOS devices
description: Configure shared device mode at the device level for iOS/iPadOS devices using Microsoft Intune so front-line workers can share a single device securely.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/shared-device-ios-device.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Device-level configuration, Multiple users on a shared device, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Configure shared device mode at the device level for iOS devices

Configure shared device mode at the device level for iOS/iPadOS devices using Microsoft Intune so front-line workers can share a single device securely.

## Before you begin

Role required: Intune Administrator, or a custom role with enrollment program and device configuration rights.

Verify that the following prerequisites are in place before completing this configuration:

-   **Devices**
    -   New or wiped iOS/iPadOS devices purchased through Apple Business Manager or Apple School Manager. Devices already in use must be factory reset.
    -   iOS/iPadOS 13.0 or later.
-   **Tenant**
    -   Access to the Apple Business Manager or Apple School Manager portal, an active Apple automated device enrollment token \(.p7m\), and an Apple MDM push certificate in Intune.
    -   An Apple Business Manager location token \(VPP token\) uploaded to Intune. Microsoft Authenticator must be purchased through an Apple volume-purchase program. The App Store version doesn't work for this deployment.
    -   ServiceNow mobile apps available for deployment, either volume-purchased or as line-of-business apps.
-   **Permissions**
    -   Intune Administrator, or a custom role with enrollment program and device configuration rights.

        **Note:** To use enrollment-time device grouping, the enrollment time device membership assignment permission under Enrollment programs in a custom RBAC role.


## About this task

Configuring shared device mode for iOS/iPadOS devices links Apple Business Manager with Microsoft Intune so devices enroll, receive policies, and sign in without a dedicated user. After setup is complete, front-line workers can log in with Microsoft Authenticator to access all supported apps, including ServiceNow. Users can then log out at the end of a shift to leave the device ready for the next user.

The configuration involves the following steps:

-   Part 1: Add Intune within Apple Business Manager
-   Part 2: Upload the token to Intune
-   Part 3: Create the Apple enrollment policy
-   Part 4: Set up a device group to target the SSO configuration profile
-   Part 5: Create an assignment filter to target devices assigned to your enrollment policy
-   Part 6: Configure the SSO app extension to turn on shared device mode on the device
-   Part 7: Deploy the Microsoft Authenticator
-   Part 8: Deploy the Company Portal through Intune
-   Part 9: Provision and distribute

-   **Related links**

    [Overview of shared device mode — Microsoft Entra](https://learn.microsoft.com/en-us/entra/identity-platform/msal-shared-devices)

    [Set up enrollment for devices in shared device mode — Microsoft Intune](https://learn.microsoft.com/en-us/intune/device-enrollment/apple/setup-automated-shared-device-mode)

    [Set up automated device enrollment for iOS/iPadOS — Microsoft Intune](https://learn.microsoft.com/en-us/intune/device-enrollment/apple/setup-automated-ios)

    [Set up an automated device enrollment token — Microsoft Intune](https://learn.microsoft.com/en-us/intune/device-enrollment/apple/setup-apple-token)

    [Supporting shared device mode for iOS — MSAL](https://learn.microsoft.com/en-us/entra/msal/objc/shared-devices-ios)


## Procedure

1.  Add Intune within the Apple Business Manager

    1.  Download the Intune public key

        1.  In the Microsoft Intune admin center, go to **Devices** &gt; **Enrollment** &gt; **Apple mobile**.
        2.  Under **Bulk Enrollment Methods**, select **Enrollment program tokens** &gt; **Add**.
        3.  Select **I agree**, then **Download the Intune public key certificate required to create the token**. A *.pem* file is saved locally.
        **Note:** Keep this browser tab open. Closing it invalidates the downloaded certificate and you must start over.

    2.  Add Intune as an MDM server in Apple Business Manager
        1.  From the Intune pane, select **Create a token via Apple Business**. The Apple portal opens in a new tab.
        2.  Sign in with your organizational Apple ID, not a personal one. The same Apple ID is required to renew and manage the token going forward.
        3.  Go to your account profile **Preferences** &gt; **MDM server assignments**.
        4.  Add an MDM server and give it a name. The name is for reference in Apple Business Manager only and does not need to match anything in Intune.
        5.  Upload the *.pem* public key from Step 1, subsection \(iii\) and save.
        6.  Download the server token \(.p7m\).
    3.  Assign devices to the MDM server.
        1.  In Apple Business Manager, go to **Devices**.
        2.  Select the devices intended for shared use. Sort by serial number to multi-select.
        3.  Select **Edit device management** and choose the MDM server you created.
    4.  Obtain Microsoft Authenticator

        In **Apps and Books**, purchase Microsoft Authenticator \(free\) with enough licenses for your device fleet, assigned to the location whose token is uploaded to Intune. Do the same for the ServiceNow mobile apps if you're deploying them through the volume purchase program.

2.  Upload the token to Intune

    1.  Return to the Intune tab.
    2.  In **Apple ID**, enter the Apple ID used to download the server token. Save it to a memorable location, as it is required for annual renewal.
    3.  In **Apple token**, browse to the .p7m file, then select **Create**.
    Intune connects to Apple Business Manager and syncs your device inventory.

    **Note:** Renew the token yearly. Also renew it if the Apple ID password changes for the person who set it up, or if that person leaves the organization.

3.  Create the Apple enrollment policy.

    1.  In the admin center, go to **Devices**, expand **Device onboarding**, and select **Enrollment**.
    2.  Select the tab **Apple mobile** &gt; **Enrollment program tokens**.
    3.  Choose your token, then select **Enrollment policies** &gt; **Create policy** &gt; **iOS/iPadOS**.

        **Note:** Use the new experience. Create policies under **Enrollment program tokens** &gt; **Enrollment policies**, not the older **Profiles** path. The older experience doesn't receive new features and is scheduled for retirement.

    4.  Enter a policy name and description in the **Basics** area.

        These details are for administrative purposes only and aren't shown to users. Choose a name for you to reuse verbatim in the group rule and assignment filter later, for example iOS Shared device mode.

    5.  Select a static Entra security group for enrollment-time grouping in the **Device group** area.

        The group maps directly to this enrollment policy and can be edited after creation. You can only select static Entra security groups in this area.

    6.  Apply the following values in the **Configuration settings** area.

        |Setting|Value|Notes|
        |-------|-----|-----|
        |**User affinity**|Enroll with Microsoft Entra ID shared mode|The setting that makes this a shared device|
        |**Supervised**|Yes|Required for full management control|
        |**Locked enrollment**|Yes|Required for Entra ID shared mode; prevents removal of the management profile|
        |**Await final configuration**|Yes|Holds the device at the end of Setup Assistant until critical policies land|
        |**Apply device name template**|Yes \(suggested\)|Suggested format: \{\{DEVICETYPE\}\}-\{\{SERIAL\}\}|
        |**Setup Assistant screens**|Yes \(suggested\)|Speeds up provisioning; there is no user present to walk through them|

    7.  Select **Next**.

        **Note:** You must know these constraints before you commit:

        -   You can't change the user affinity setting on an existing enrollment policy. To change it, create a new policy.
        -   Changes to an existing enrollment policy don't take effect on already-assigned devices until those devices are factory reset and reactivated. The device name template is the only exception which applies at the next check-in.
    8.  Select **Create**.
    9.  Assign the policy to devices.
        1.  Return to **Enrollment program tokens** &gt; **Your token** &gt; **Devices**.
        2.  Select the target devices and choose **Assign policy**.
        3.  Pick the shared device mode policy and select **Assign**.
        4.  Set a default policy for the token: from the token blade, select **Set default policy** and choose your shared device mode policy. If a device syncs from Apple without an assigned enrollment policy and someone turns it on, enrollment fails.
4.  Set up a device group to target the SSO configuration profile, using one of following options:

<table id="table_dk1_pdb_lkc"><thead><tr><th>

Device grouping option

</th><th>

Description and process

</th></tr></thead><tbody><tr><td>

Dynamic grouping

</td><td>

Grouping suitable for larger organizations.Create a dynamic Entra group using the **enrollmentProfileName** property to automatically group devices that enroll with a specific policy:

-   **Group type**: Security
-   **Membership type**: Dynamic Device
-   **Rule**: property enrollmentProfileName, operator Equals, value equal to the exact name of your enrollment policy


</td></tr><tr><td>

Static grouping

</td><td>

Static group via enrollment-time grouping.Create an assigned \(static\) security group and attach it to the enrollment policy created in Step 3, subsection \(e\). Intune adds devices to the group as they enroll. This avoids dynamic group evaluation lag but requires the RBAC permission noted in the prerequisites.

The enrolled device appears in Microsoft Entra ID as a Microsoft Entra registered device with no owner and no user principal name. This is expected behavior for a userless shared device.

</td></tr></tbody>
</table>5.  Create an assignment filter to target devices assigned to your enrollment policy.

    1.  Go to **Devices** &gt; **Assignment filters** &gt; **Create**.
    2.  Platform: **iOS/iPadOS**.
    3.  Enter the rule syntax:

        ```
        (device.enrollmentProfileName -eq "<your enrollment policy name>")
        ```

        **Note:** The name in the filter must match the enrollment policy name exactly, including spaces and capitalization. A mismatch is the most common reason the configuration profile never reaches the device.

6.  Configure the SSO app extension to turn on shared device mode on the device.

    1.  Go to **Devices** &gt; **Configuration** &gt; **Create** &gt; **New policy**.
    2.  **Platform**: iOS/iPadOS. **Profile type**: **Templates** &gt; **Device features**.
    3.  Name the profile, for example iOS shared device SSO policy.
    4.  Expand **Single sign-on app extension** and configure the settings as described in the table.

        |Setting|Value|
        |-------|-----|
        |SSO app extension type|Microsoft Entra ID|
        |Enable shared device mode|Yes|
        |App bundle IDs|See step \(e\) after this table|
        |Additional configuration: Key|device\_registration|
        |Additional configuration: Type|String|
        |Additional configuration: Value|\{\{DEVICEREGISTRATION\}\}|

        **Note:** You must configure the device\_registration key with the \{\{DEVICEREGISTRATION\}\} variable. This setting allows the device to complete Entra device registration with no user present.

    5.  Add the bundle ID of every app that should participate in single sign-on. For a ServiceNow deployment:

        ```
        com.servicenow.intune.fulfiller
        com.servicenow.intune.requestor
        ```

        Include only the variants you actually deploy. The intune.\* identifiers are the Intune-wrapped builds. If your organization publishes a branded or custom ServiceNow mobile app, add its bundle ID here as well.

        1.  In the **Assignments** area, assign to All devices, then apply the assignment filter from Step 5 in Include mode.
        2.  Review and create.
7.  Deploy the Microsoft Authenticator and ServiceNow mobile apps.

    Both the Microsoft Authenticator app and the ServiceNow mobile apps follow the same assignment pattern: required, targeted at all devices, narrowed by the filter from Step 5, and licensed to the device rather than a user. Authenticator has to be configured correctly first, since it is the broker that puts the device into shared mode.

    1.  Assign the Microsoft Authenticator app as required to **All devices**, then apply the assignment filter from Step 5. The app must have been purchased through an Apple volume-purchase program.
        1.  Go to **Apps** &gt; **iOS/iPadOS** and select the volume-purchased **Microsoft Authenticator**.
        2.  Select **Properties** &gt; **Assignments** &gt; **Edit**.
        3.  Under **Required**, add **All devices** and apply the filter in **Include** mode.
        4.  Check the license type is **Device licensing**. User licensing fails on userless devices.
    2.  Apply an assignment pattern for your ServiceNow mobile app. Repeat the same assignment pattern for each ServiceNow mobile app you're deploying.

        1.  Go to **Apps** &gt; **iOS/iPadOS** and select the ServiceNow app, either the volume-purchased listing or your line-of-business upload.
        2.  Select **Properties** &gt; **Assignments** &gt; **Edit**.
        3.  Under Required, add All devices and apply the filter in Include mode.
        4.  For volume-purchased apps, check the license type is Device licensing.
        **Note:** Deploy the same build you listed in Step 6. The bundle IDs in the SSO app extension must match the apps actually installed on the device.

8.  Deploy the Company Portal through Intune.

    Deploy the Company Portal as a required volume-purchased app with device licensing. To enable automatic updates, set **Automatic app updates** to **Yes** in your app token settings.

    **Note:** When using automated device enrollment, deploy Company Portal through Intune rather than the App Store. That method makes sure that all enrolled devices receive the app and get automatic updates. The App Store version is not compatible with automated device enrollment.

9.  Provision and distribute.

    1.  Unbox or wipe the device and power it on.
    2.  Setup Assistant runs and the device enrolls automatically. With **Await final configuration** set to Yes, the device pauses before the home screen while policies install. Waiting time scales with the number of assigned policies and apps; in Microsoft's validation testing most devices reached the home screen within 15 minutes.
    3.  On receiving the device, the front line worker opens the Microsoft Authenticator app to confirm the device is in shared device mode and logs in with their Entra credentials.
    4.  The user is now logged in across all supported apps, including the ServiceNow apps configured in Step 6.
    5.  At the end of the shift, the user logs out from Authenticator or any supported app, which logs them out globally.

