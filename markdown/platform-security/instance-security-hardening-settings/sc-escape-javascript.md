---
title: Escape JavaScript \[Updated in Security Center 1.3\]
description: Use the glide.html.escape\_script property to force escape from JavaScript \(&lt;script&gt;&lt;/script&gt;\) tags in HTML fields during list views.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape JavaScript \[Updated in Security Center 1.3\]

Use the **glide.html.escape\_script** property to force escape from JavaScript \(`<script></script>`\) tags in HTML fields during list views.

The glide property **glide.html.escape\_script** helps sanitize HTML fields. If **glide.html.escape\_script**is not set to the recommended value of true, then inputs will not be sanitized for HTML fields \(output encoding\) from a backend Java context by removing embedded JavaScript. Javascript in HTML fields can lead to stored and reflected XSS. The ability to have XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.html.escape\_script**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

To prevent cross-site scripting attacks against an application.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8.8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces JavaScript escaping to occur on the UI and renders encoded results to the user. It can have an impact on functionality, based on the instance user interaction with the resulting data

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Input validation must occur in the application to defend against cross-site scripting attacks. These attacks enable foreign scripts to execute on user session in the logged in browser's context. Attackers can use it to steal session information and sensitive data.

</td></tr><tr><td>

References

</td><td>

Available system properties

 [High Security Settings](../../security/concept/c_HighSecuritySettings.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

