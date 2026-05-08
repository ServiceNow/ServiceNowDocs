---
title: Enforce SOAP request strict security
description: Use the glide.soap.strict\_security property to enforces web service security.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce SOAP request strict security

Use the **glide.soap.strict\_security** property to enforces web service security.

If the **glide.soap.strict\_security** system property is not set to the recommended value of **true**, then users do not need a SOAP role to make requests of non-public pages when the high security or web service plugin is installed.

Ensure the property **glide.soap.strict\_security** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.soap.strict\_security**

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.8
-   CVSS rating: Medium
-   Security risk details: An unauthorized user can get access to sensitive content/data on the target instance.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Access control](sc-access-control.md)

