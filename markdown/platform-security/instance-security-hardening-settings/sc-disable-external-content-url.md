---
title: Disable external content url \[Updated in Security Center 2.0\]
description: Manage how external link metadata is used in your instance with Connect Chat.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable external content url \[Updated in Security Center 2.0\]

Manage how external link metadata is used in your instance with Connect Chat.

Use the **glide.ui.url.external.content** property to manage external link metadata in your instance. If the property is set to the recommended value of **false**, then no external link metadata will be rendered. If set to **true** then [Connect Chat](https://www.servicenow.com/docs/access?context=c_Collaboration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) will retrieve external link metadata from sources such as YouTube or news articles to render richer messages. This could lead to Server Side Request Forgery \(SSRF\) attacks.

Ensure the Glide Property **glide.ui.url.external.content** exists and is set to the value false. If the property does not appear in the sys\_properties table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.url.external.content**

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

true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.2
-   CVSS score: High
-   Security risk details: Setting this property to **true** could expose your instance to Server Side Request Forgery \(SSRF\) attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Connect Chat](https://www.servicenow.com/docs/access?context=c_Collaboration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

