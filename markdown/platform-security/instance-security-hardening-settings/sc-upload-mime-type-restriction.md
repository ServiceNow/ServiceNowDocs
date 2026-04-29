---
title: Restrict uploaded MIME types
description: Use the glide.security.file.mime\_type.validation property to activate MIME type checking for uploads. You can enable \(set the property to true\) or disable \(set it to false\) MIME type validation for file attachments.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict uploaded MIME types

Use the **glide.security.file.mime\_type.validation** property to activate MIME type checking for uploads. You can enable \(set the property to **true**\) or disable \(set it to **false**\) MIME type validation for file attachments.

The **glide.security.file.mime\_type.validation** system property is used to activate MIME type checking for uploads.

Ensure that the property **glide.security.file.mime\_type.validation** exists in the System Properties \[sys\_properties\] and is set to **true**. If the property does not appear in the System Properties \[sys\_properties\] table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.file.mime\_type.validation**

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

-   Severity score: 5.4
-   CVSS rating: Medium
-   Security risk details: MIME type validation for file attachments will not take place which could allow malicious file types to be uploaded.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enables MIME type verification on the attachments to the application. No functionality impact, unless there is a malicious intent in uploading the files as this validation is merely checking for mis-sync between the MIME type and the data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

