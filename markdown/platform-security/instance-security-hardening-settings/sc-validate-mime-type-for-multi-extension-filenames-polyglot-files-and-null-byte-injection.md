---
title: Validate MIME Type for Multi-Extension Filenames, Polyglot Files, and Null-Byte Injection
description: Use a system property to prevent attachments from bypassing MIME-type restrictions.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Validate MIME Type for Multi-Extension Filenames, Polyglot Files, and Null-Byte Injection

Use a system property to prevent attachments from bypassing MIME-type restrictions.

Use the **glide.attachment.enable\_secure\_filename\_validation** system property to enable strict validation of attachment file names. This change to prevents attachments from bypassing MIME-type restrictions. When set to true, the platform performs full file name sanitization and rejects unsafe patterns that could otherwise be used to upload malicious files.

Add a record to the System Properties \[sys\_properties\] table with the name `glide.attachment.enable_secure_filename_validation` and a value of `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.attachment.enable\_secure\_filename\_validation**

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

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:4.6
-   CVSS score: Medium
-   Security risk details:

MIME type validation for file attachments doesn't take place in multi-extension processing or when null bytes are present. This allows attackers to circumvent the **glide.attachment.extensions** and **glide.security.file.mime\_type.validation** system properties through null-byte injection, multi-extension file names and polyglot files, leading to malicious file uploads.


</td></tr><tr><td>

Functional impact

</td><td>

When the **glide.attachment.enable\_secure\_filename\_validation** property is set to true:

 -   Uploads that previously passed may now be rejected.
-   Integrations or automations that rely on generating file names with multiple dots or unusual patterns may fail until updated.
-   Custom UI pages, scoped apps, or API consumers that upload files programmatically \(especially with templated file names\) may hit validation errors.
-   CI/CD pipelines that import files, ATF tests, or legacy scripts may need updates to ensure compliant file names.

 Functionality that does not rely on unsafe file name patterns continue to work normally.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

