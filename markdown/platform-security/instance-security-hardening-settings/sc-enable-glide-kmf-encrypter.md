---
title: Enable glide KMF encrypter \[Removed in Security Center 1.3.2\]
description: Manage the encrypters used for Password2 fields on your instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stored cryptography, Hardening settings, Platform Security]
---

# Enable glide KMF encrypter \[Removed in Security Center 1.3.2\]

Manage the encrypters used for Password2 fields on your instance.

Use the **glide.kmf.encrypter.enabled** property to set KMF encrypter as the default encrypter for Password2 fields. This property ensures that strong and compliant encryption standards are being used instead of a legacy encrypter. To ensure that KMF encrypter is used instead of the legacy encrypter, set this property to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.kmf.encrypter.enabled**

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

[Stored cryptography](sc-stored-cryptography.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.9
-   CVSS score: Medium
-   Security risk details: Setting this property to **true** ensures that KMF encrypter is being used instead of legacy encrypter.

</td></tr><tr><td>

References

</td><td>

[Password2 encryption with the Key Management Framework \(KMF\)](../../key-management-framework/concept/password-2way-encrypted-fields.md)

</td></tr></tbody>
</table>**Parent Topic:**[Stored cryptography](sc-stored-cryptography.md)

