---
title: Validate MIME Type of Attachments from Inbound Emails
description: Use a system property to validate attachments uploaded from inbound emails.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Validate MIME Type of Attachments from Inbound Emails

Use a system property to validate attachments uploaded from inbound emails.

Set the **glide.security.file.mime\_type.validation.inbound\_email** system property to **true** to perform MIME type validation on attachments uploaded from inbound emails. Validating the MIME type of uploaded files helps to ensure that the file content matches the expected file format.

Set the system property value to **true** to perform MIME type validation. If the system property is not present on your instance, the fallback value is **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.file.mime\_type.validation.inbound\_email**

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

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: If MIME type validation does not occur, users can upload an unexpected type of file to your instance, resulting in potential vulnerabilities where the attachment is handled.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Attachments from inbound emails are not uploaded if the MIME type does not validate correctly.

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

