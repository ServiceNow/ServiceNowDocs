---
title: Require CAPTCHA for guest walk-up experience in customer service application
description: The CAPTCHA for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a CAPTCHA verification.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Require CAPTCHA for guest walk-up experience in customer service application

The CAPTCHA for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a CAPTCHA verification.

The CAPTCHA for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a CAPTCHA verification. If CAPTCHA isn't enabled, this could lead to automated creation of spam appointments to overwhelm the system or fill up all available booking spots creating a Denial of Service attack.

If Guest Walk-up Experience for Customer Service application is active, ensure that **sn\_guest\_walkup\_cs.captcha.enabled** is set to **true**.

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: This exposes the system to spam appointments and resource exhaustion attacks, potentially filling all available booking slots and causing a Denial of Service \(DoS\). Without CAPTCHA, the platform lacks a critical control to prevent automated abuse and maintain service availability.

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

