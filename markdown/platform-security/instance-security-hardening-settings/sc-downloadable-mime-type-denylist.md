---
title: Restrict downloadable MIME types
description: The glide.ui.attachment.download\_mime\_types property will force the specified list of dangerous file types to be downloaded to the client and not viewed inline in the browser.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict downloadable MIME types

The **glide.ui.attachment.download\_mime\_types** property will force the specified list of dangerous file types to be downloaded to the client and not viewed inline in the browser.

If the **glide.ui.attachment.force\_download\_all\_mime\_types** system property is set to **true**, then the **glide.ui.attachment.download\_mime\_types** property is overridden so that all MIME types will be downloaded rather than rendered by the browser. For example, downloading text/html forces an HTML file to be downloaded to the client as a file rather than viewed inline in the browser, preventing a XSS attack.

Ensure that the property **glide.ui.attachment.force\_download\_all\_mime\_types** is set to **true**. If the property does not exist in the System Properties \[sys\_properties\] table, the default value is **false**.

**Note:** The security\_admin role is required to edit the property.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.attachment.download\_mime\_types**

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

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.4
-   CVSS rating: Medium
-   Security risk details: XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces performance of validation checks before performing an action when you click an attachment in a application. There is no potential impact, but the user experience is altered.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

