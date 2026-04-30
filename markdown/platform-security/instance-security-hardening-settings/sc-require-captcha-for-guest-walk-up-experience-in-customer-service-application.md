---
title: Require captcha for guest walk-up experience in customer service application \[New in Security Center 1.3 and updated in 1.5\]
description: The captcha for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a captcha verification.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Require captcha for guest walk-up experience in customer service application \[New in Security Center 1.3and updated in 1.5\]

The captcha for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a captcha verification.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_guest\_walkup\_cs.captcha.enabled**

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

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: If captcha is not enabled, this could lead to automated creation of spam appointments to overwhelm the system or fill up all available booking spots creating a Denial of Service \(DoS\) attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property enables or disables the captcha on the CSM Guest Walkup Check-in widgets. By default, it is set to true.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

