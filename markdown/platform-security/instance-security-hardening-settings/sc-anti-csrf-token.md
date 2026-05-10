---
title: Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]
description: Use the glide.security.use\_csrf\_token property to ensure the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]

Use the **glide.security.use\_csrf\_token** property to ensure the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.

Cross-Site Request Forgery \(CSRF\) is an attack that forces authenticated users to submit a request to a Web application against which they are currently authenticated. CSRF attacks exploit the trust a Web application has in an authenticated user.This property enables usage of a secure token to identify and validate incoming requests. This token is used to prevent cross site request forgery attacks. If **glide.security.use\_csrf\_token**is not set to the recommended value of true, then CSRF is possible.

## More information

<table><tbody><tr><td>

Attribute

</td><td>

Description

</td></tr><tr><td>

Property name

</td><td>

**glide.security.use\_csrf\_token**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

To protect the application from potential CSRF attack.

</td></tr><tr><td>

Security risk rating

</td><td>

8.1

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enables an extra validation step before the instance user submits a write request to the instance. Every write request contains a CSRF token \(i.e a validation/CSRF ID tied to the user session\). When the user session expires, the secure token expires with it.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Cross Site Request Forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack by abusing the trust of an instance user. With the help of social engineering attacks, a user can submit a malformed request on behalf of the attacker on the instance.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Access control](sc-access-control.md)

