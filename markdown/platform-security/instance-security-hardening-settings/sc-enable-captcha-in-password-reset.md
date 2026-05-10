---
title: Enable CAPTCHA in password reset
description: Use the password\_reset.captcha.ignore property to enable or disable requiring a CAPTCHA challenge when a user resets their password.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable CAPTCHA in password reset

Use the **password\_reset.captcha.ignore** property to enable or disable requiring a CAPTCHA challenge when a user resets their password.

If the **password\_reset.captcha.ignore** system property is not set to the recommended value of **false**, then a CAPTCHA challenge-response will not be used during the password reset process. CAPTCHAs help prevent automation attacks by prompting the user for a challenge-response that is not easily answered by automated systems.

Ensure that the property **password\_reset.captcha.ignore** is set to **false**.

**Note:** This property is used for password reset automation only.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.captcha.ignore**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

 

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.6
-   CVSS rating: Medium
-   Security risk details: If the CAPTCHA is disabled, an attacker may be more successful during automated attacks against the password reset feature.

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

