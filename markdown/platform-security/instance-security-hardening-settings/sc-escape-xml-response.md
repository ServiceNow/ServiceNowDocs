---
title: Escape xml response
description: Manage how XML escapes are handled on your instance.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape xml response

Manage how XML escapes are handled on your instance.

Use this property to manage if XML responses are escaped. If the property is set to the recommended value of **false**, then XML responses will not be escaped which can lead to XML injection attack. The injection of unintended XML content into an XML message can alter the intended logic of an application.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.soaprequest.unescape\_xml\_response**

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

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.4
-   CVSS score: Medium
-   Security risk details: Setting this property to **false** disables XML escaping, which could lead to XML injection attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

