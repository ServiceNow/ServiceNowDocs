---
title: Mobile Encryption Security Compliance
description: Learn about how ServiceNow mobile apps comply with encryption security standards for the FedRAMP and DISA environments.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile Encryption Security Compliance

Learn about how ServiceNow mobile apps comply with encryption security standards for the FedRAMP and DISA environments.

<table id="table_hws_qkb_2lb"><tbody><tr><td>

![Device PIN and Blur features in the mobile UI.](../image/fedramp-compliance.png)

</td><td>

ServiceNow GovCommunityCloud \(GCC\) compliance is designed for U.S. Federal, State, and local government customers. This environment is FedRAMP High and DoD Impact Level 4 authorized and compliant. Each ServiceNow mobile app \(Now Mobile, Mobile Agent, and Mobile Onboarding\) use FIPS 140-2 validated encryption modules.

 As part of using these validated modules, ServiceNow mobile apps include the following:

 -   **Encryption**

ServiceNow uses FIPS 140-2 validated encryption when connecting to FedRAMP and DISA instances.

-   **Enforced security feature enablement**

Enforced device PIN or biometric enablement when connecting to FedRAMP and DISA instances.

-   **Encryption for locally stored data**

Locally stored app data such as user preferences and offline data are encrypted.

-   **Blur feature**

The blur feature is automatically enabled when the app is in the background.


</td></tr></tbody>
</table>## iOS FIPS 140-2 Compliance

-   On iOS devices, ServiceNow mobile apps use the Apple validated cryptographic modules. These modules are available on all devices using iOS 11 and up.

-   To enforce iOS FIPS 140-2 encryption, the ServiceNow mobile apps require that a user’s device has a pass code enabled when connecting to a FedRAMP or DISA instance.

-   All locally stored mobile app data such as user preferences and offline data use FIPS 140-2 validated encryption when pass code enablement is confirmed.


For more information on the Apple validated cryptographic modules, see [Apple Platform Certifications](https://support.apple.com/guide/certifications/welcome/web)

## Android FIPS 140-2 Compliance

-   On Android devices, ServiceNow mobile apps are integrated with a third party SDK that uses a FIPS 140-2 validated module.

-   With this SDK, Android versions of ServiceNow mobile apps are FIPS 140-2 compliant for data at rest. All locally stored app data such as user preferences and offline data use the same level of encryption.
-   ServiceNow mobile apps also require that a device pass code is enabled when a user connects to a FedRAMP or DISA instance.

    **Note:** This feature requires Android version 7.0 Nougat and up.


For more information on the certificate used with the third party SDK, see [https://csrc.nist.gov/projects/cryptographic-module-validation-program/certificate/3220](https://csrc.nist.gov/projects/cryptographic-module-validation-program/certificate/3220)

## Mobile system properties related to compliance

-   **Enforcing FIPS 140-2 Encryption**

    Use the **glide.sg.device\_encryption\_enabled** system property to enforce encryption and require that a device pass code is configured. This system property is automatically added and defaults to `true` for FedRAMP and DISA instances.

    For non-FedRAMP and non-DISA instances, this property defaults to `false`. Enable this property on these instances to take advantage of encryption and device pass code enablement.

-   **Disabling offline mode**

    On FedRAMP and DISA instances, offline mode is disabled by default when the offline mode plugin is installed. To enable offline mode on a FedRAMP or DISA instance, an administrator must create the **glide.sg.offline.enabled** system property on the \[sys\_properties\] table, and set the value of this property to `true`.

    For commercial instances, offline mode is enabled by default when the offline mode plugin is installed. To disable offline mode on a commercial instance, an administrator must create the **glide.sg.offline.enabled** system property on the \[sys\_properties\] table, and set the value of this property to `false`.

    For more information on offline mode, see [Offline mode](mobile-offline-mode.md).

-   **Screen blur on background**

    Use the **glide.sg.blur\_ui\_when\_backgrounded** system property to blur the app screen when in background. This property was introduced in the Madrid release.

    **Important:**

    -   The **glide.sg.blur\_ui\_when\_backgrounded** system property is supported on both iOS and Android devices.
    -   By default, the value for this property is set to `false`, which turns it off.
    -   For Android devices, when this property is enabled by setting the value to `true`, the following restrictions apply:

        -   The screen share feature isn't supported and the shared app screen appears black.
        -   Users are prevented from taking screenshots.
        These restrictions don't apply to iOS devices when the **glide.sg.blur\_ui\_when\_backgrounded** property is enabled.

    This property is not overridden for existing customers who upgrade to the Paris release.


## FedRAMP

The Federal Risk and Authorization Management Program \(FedRAMP\) creates a set of processes to ensure cloud security for the government. For more detail on this program, see [https://www.fedramp.gov/](https://www.fedramp.gov/).

