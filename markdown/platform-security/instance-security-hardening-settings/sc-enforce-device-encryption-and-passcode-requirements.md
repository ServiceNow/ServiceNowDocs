---
title: Enforce device encryption and passcode requirements \[New in Security Center 1.3\]
description: The glide.sg.device\_encryption\_enabled property enforces the Federal Information Processing Standard \(FIPS 140-2\) Encryption. Mobile device encryption and passcode ensure that an unauthorized user cannot access the content of a device even if the device is physically obtained.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enforce device encryption and passcode requirements \[New in Security Center 1.3\]

The **glide.sg.device\_encryption\_enabled** property enforces the Federal Information Processing Standard \(FIPS 140-2\) Encryption. Mobile device encryption and passcode ensure that an unauthorized user cannot access the content of a device even if the device is physically obtained.

When **glide.sg.device\_encryption\_enabled** is set to true, the ServiceNow mobile app will check that device encryption and device passcode are enabled.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sg.device\_encryption\_enabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: If encryption or passcode is not enabled, then the user will not be allowed to log into the instance on mobile

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When this property is set to true, the mobile app will verify if device encryption is enabled. If encryption is not enabled, users will not be allowed to log into the current instance on mobile.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

