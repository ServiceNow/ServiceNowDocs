---
title: Require obfuscation of classic mobile app UI \[Updated in Security Center 1.3\]
description: Use the glide.ui.m.blur\_ui\_when\_backgrounded property to obfuscate all fields from the snapshot as the image is saved during the backgrounding process.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Require obfuscation of classic mobile app UI \[Updated in Security Center 1.3\]

Use the **glide.ui.m.blur\_ui\_when\_backgrounded** property to obfuscate all fields from the snapshot as the image is saved during the backgrounding process.

On Android devices, the Android operating system takes a screenshot for usage in the recent task menu when the application is sent to background. Users can also take manual screenshots of the application, which are stored publicly on the device.

On iOS devices, the iOS operating system also allows applications to save an image file. This file represents the last screen seen by the user when the application is sent to the background. While the intent is to provide a better user experience, it also creates a security risk because the images are saved as PNG image files.

**Note:** This setting or configuration is per instance basis so the user must connect to the instance with the property configured.

To obfuscate all fields from the snapshot in the ServiceNow Classic app, see [Configure the blur app option to improve security](https://www.servicenow.com/docs/access?context=t_BlurApp&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

## Example

When you set this property to true, the background application is obfuscated for iOS devices, and blacked out for Android iOS devices.

![Mobile ID obfuscation Example 1](../../security/image/mobile-id-obfuscation-example1.png)

## More information

<table id="table_jnn_lk2_pvb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property/Plugin Name

</td><td>

**glide.ui.m.blur\_ui\_when\_backgrounded**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Purpose

</td><td>

To obfuscate all fields from the snapshot as the image is saved during the backgrounding process.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

2.4

</td></tr><tr><td>

Functional impact

</td><td>

If the **glide.ui.m.blur\_ui\_when\_backgrounded** property is set to true, the native apps use the parameter defined on the server to blur the screen when the app enters the background. -   It blurs the screenshots taken by iOS and Android when the app enters the background.

**Note:** Enabling this setting can prevent users from taking screenshots of the classic mobile app, which may be desirable for support purposes.

-   The user experience may be adversely affected because they would not be able to see the content when the app is sent to background.

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) A compromised \(jailbroken\) device would enable an attacker to have full access to the file system, with access those files/snapshots with sensitive information embedded in them.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

