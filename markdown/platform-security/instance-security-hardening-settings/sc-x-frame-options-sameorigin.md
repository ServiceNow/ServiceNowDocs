---
title: Implement the x-frame-options: SAMEORIGIN security header
description: Use the glide.set\_x\_frame\_options property to set the X-Frame-Options response header to SAMEORIGIN for all UI pages.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Implement the x-frame-options: SAMEORIGIN security header

Use the **glide.set\_x\_frame\_options** property to set the X-Frame-Options response header to SAMEORIGIN for all UI pages.

The **glide.set\_x\_frame\_options** system property controls the implementation of the security header X-Frame-Options: SAMEORIGIN. If **glide.set\_x\_frame\_options** is not set to the recommended value of **true**, then an instance will be allowed to be framed in an iframe of another page.

Ensure the property **glide.set\_x\_frame\_options** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.set\_x\_frame\_options**

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

false

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS rating: Medium
-   Security risk details: This can lead to a clickjacking attack.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces the restriction for rendering a ServiceNow AI Platform application in a third-party application in the form of an iFrame. If you have such an integration, the application wouldn't render in the customized third-party app.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

