---
title: Disable Voice Chat Guest Impersonation
description: Use a system property to ensure that voice interactions/conversations are recorded under the appropriate internal integration user.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable Voice Chat Guest Impersonation

Use a system property to ensure that voice interactions/conversations are recorded under the appropriate internal integration user.

When an inbound or outbound call triggers the Start Voice Interaction API in a domain-separated environment, interactions are created under the guest user and in the default domain. This causes failures when retrieving interaction records due to domain mismatches, as the interaction is inaccessible to the actual user. This happens because the API call impersonates the guest user despite being invoked by a logged-in user, leading to interactions created in sibling domains that restrict access.

When the property is set to false, voice interactions/conversations are recorded under the guest user. This is a generic user that doesn’t accurately reflect the identity of the security principal creating the record.

When the property is set to true, voice interactions/conversations are recorded under the appropriate internal integration user.

Confirm that the **com.glide.cs.voice.chat.disable.guest.impersonate** system property is set to true in the System Properties \[sys\_properties\] table, or that the property doesn't exist in the table.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.cs.voice.chat.disable.guest.impersonate**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 1.9
-   CVSS score: Low
-   Security risk details: If an attacker is able to inject records as the guest user, then platform users would not be able to distinguish between valid and spoofed records, leading to longer troubleshooting efforts.

</td></tr><tr><td>

Functional impact

</td><td>

There is no impact on system functionality. The property affects the way the Now platform logs internal actions.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

