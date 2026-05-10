---
title: Enable CAPTCHA for External User Registration
description: The sn\_ext\_usr\_reg.captchaEnabled controls if CAPTCHA will be validated for external user registration.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable CAPTCHA for External User Registration

The **sn\_ext\_usr\_reg.captchaEnabled** controls if CAPTCHA will be validated for external user registration.

If the **sn\_ext\_usr\_reg.captchaEnabled** system property is not set to the recommended value of **true**, then CAPTCHA isn't validated for external user registration and could lead to automatic account creation attacks.

Ensure that the property **sn\_ext\_usr\_reg.captchaEnabled** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_ext\_usr\_reg.captchaEnabled**

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
-   Security risk details: Enforcing CAPTCHA is critical to prevent bot-driven attacks and maintain the integrity of user onboarding.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Authentication](sc-authentication.md)

