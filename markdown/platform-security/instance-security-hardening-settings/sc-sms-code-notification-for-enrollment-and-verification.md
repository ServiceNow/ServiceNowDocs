---
title: Enable SMS code notification for enrollment and verification
description: The password\_reset.sms.use\_notify property controls the usage of SMS code notifications for password reset.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable SMS code notification for enrollment and verification

The **password\_reset.sms.use\_notify** property controls the usage of SMS code notifications for password reset.

The **password\_reset.sms.use\_notify** system property controls usage SMS code notification for enrollment and verification. If **password\_reset.sms.use\_notify** is set to the recommended value **true**, then user isn't notified for password reset for SMS verification method and new device enrollment. Using SMS code notification for enrollment and verification is more secure that default email notification.

Ensure the property **password\_reset.sms.use\_notify** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.sms.use\_notify**

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
-   CVSS rating: Low
-   Security risk details: Email-based notifications are generally less secure because they are more susceptible to account compromise and phishing attacks. Using SMS for verification provides stronger assurance of user identity and reduces the risk of unauthorized password resets or fraudulent device enrollments.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

