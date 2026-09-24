---
title: Troubleshoot iOS device-level configuration
description: Review common symptoms, causes, and resolutions for iOS device-level configuration problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/ios-device-sharing-troubleshoot.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [iOS, shared device mode, Microsoft Intune, device-level configuration, enrollment, Authenticator, SSO, bundle ID, configuration profile, iPadOS, enrollment policy, Device Type Restrictions, Enrollment Restrictions, SSO app extension, factory reset, Company Portal, Invalid Profile, filter rule, dynamic group]
breadcrumb: [iOS device-level configuration, Device-level configuration, Multiple users on a shared device, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Troubleshoot iOS device-level configuration

Review common symptoms, causes, and resolutions for iOS device-level configuration problems.

<table id="table_zbk_3xn_lkc"><thead><tr><th>

Symptom

</th><th>

Cause and resolution

</th></tr></thead><tbody><tr><td>

Device shows "Invalid Profile"

</td><td>

No enrollment policy is assigned, or Device Type Restrictions under Enrollment Restrictions has the default All Users policy blocking the iOS/iPadOS platform. Block only personally owned devices rather than the whole platform.

</td></tr><tr><td>

Shared device mode not active in Authenticator

</td><td>

-   Check that the SSO app extension profile reports **Succeeded** for the device and that **Enable shared device mode** is set to **Yes**.
-   Check that the device\_registration additional configuration is present and spelled correctly, and that **Authenticator** is installed as a device-licensed, volume-purchased app.

</td></tr><tr><td>

ServiceNow app still prompts for credentials

</td><td>

The app's bundle ID is missing from the SSO app extension list, or a different build variant was deployed than the identifier listed. Check the installed app's bundle ID and add it.

</td></tr><tr><td>

Configuration profile never reaches the device

</td><td>

Check filter evaluation on the device object. The usual cause is a mismatch between the enrollment policy name and the string in the filter rule or dynamic group rule.

</td></tr><tr><td>

Policy changes aren't taking effect

</td><td>

Expected behavior. Enrollment policy changes require a factory reset and reactivation; only the device name template applies at the next check-in.

</td></tr><tr><td>

Enrollment blocked

</td><td>

Devices are blocked from enrolling if there aren't enough Company Portal volume-purchase licenses or if the token has expired.

</td></tr></tbody>
</table>