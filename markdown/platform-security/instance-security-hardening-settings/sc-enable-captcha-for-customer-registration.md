---
title: Enable CAPTCHA for customer registration
description: Reduce the risk of requests by malicious bots by enabling CAPTCHA for customer registration.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable CAPTCHA for customer registration

Reduce the risk of requests by malicious bots by enabling CAPTCHA for customer registration.

The **sn\_customerservice.captchaEnabled** system property determines if CAPTCHA validation is enabled or disabled for customer registration on the Customer Service Management Portal.

Set the system property **sn\_customerservice.captchaEnabled** to **true** to enable CAPTCHA validation. If the property isn’t on the System Properties \[sys\_properties\] table, the default value is **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_customerservice.captchaEnabled**

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

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS rating: Low
-   Security risk details: CAPTCHA validation is considered a best practice to prevent potentially malicious bots from automatically submitting requests against an application.

</td></tr><tr><td>

Functional impact

</td><td>

Registering users may have a negative experience from having to pass the CAPTCHA validation.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Authentication](sc-authentication.md)

