---
title: Disable external content URL
description: Manage how external link metadata is used in your instance with Connect Chat.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable external content URL

Manage how external link metadata is used in your instance with Connect Chat.

If the **glide.ui.url.external.content** system property isn't set to the recommended value of **false**, then Connect chat retrieves external link metadata in order to render richer content in messages with links to Youtube, news articles, images, etc.

Ensure that the Glide Property **glide.ui.url.external.content** exists in the System Properties \[sys\_properties\] table and is set to the value **false**. If the property does not appear in the table, add a new record.

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

Boolean

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

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.2
-   CVSS score: High
-   Security risk details: This could lead to Server Side Request Forgery \(SSRF\) attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Connect Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/c_Collaboration.md)

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

