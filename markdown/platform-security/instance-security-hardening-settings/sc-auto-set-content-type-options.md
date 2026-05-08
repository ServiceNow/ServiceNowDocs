---
title: Auto set content type options \[Removed in Security Center 1.3.3\]
description: Configure the Auto set content type options property on your instance to prevent MIME confusion attacks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Auto set content type options \[Removed in Security Center 1.3.3\]

Configure the Auto set content type options property on your instance to prevent MIME confusion attacks.

Use this property to control the X-Content-Type-Options response HTTP header. The X-Content-Type-Options response HTTP header is used by the server to indicate that the MIME types advertised in the Content-Type headers should be followed. If this property is set to false, then it is possible for an attacker to conduct MIME confusion attacks; if set to true then this header will prevent the browser from interpreting files as anything but the content type in the HTTP headers.

**Warning:** The value for this property is a no DB override. It can't be altered or overridden.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.header.auto\_set\_x\_content\_type\_options**

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

false

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.3
-   CVSS score: High
-   Security risk details: Setting this property to **false** could make it possible for an attacker to conduct MIME confusion attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

Add a system property

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

