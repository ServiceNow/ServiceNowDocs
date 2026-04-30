---
title: Enable Code Signing for application configuration data and scripts \[Removed in Security Center 1.3\]
description: Manage Code Signing for application configuration data and scripts on your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Enable Code Signing for application configuration data and scripts \[Removed in Security Center 1.3\]

Manage Code Signing for application configuration data and scripts on your instance.

Code Signing can help improve security by validating sensitive application configuration data and scripts before they are used. Code Signing creates digital signatures for the data which later are checked to confirm the authenticity and integrity of the data. This verification prevents malicious data or scripts from being used on the instance which may lead to full compromise of the instance.

Enable Code Signing on your instance by following the steps in [Configuring Code Signing](../../encryption/concept/config-code-signing.md). This results in the **com.snc.kmf.signature.validation.flag** system property being set to true.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.kmf.signature.validation.flag**

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

[Malicious code](sc-malicious-code.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6
-   CVSS score: Medium
-   Security risk details: Setting this property to **true** enables Code Signing, which helps improve security by validating sensitive application configuration data and scripts.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](sc-malicious-code.md)

