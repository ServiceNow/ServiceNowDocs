---
title: Unset LDAP Initial distinguished name \[Updated in Security Center 1.3 and removed in 2.0\]
description: Use this property to manage the distinguished name of a LDAP Server record.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Unset LDAP Initial distinguished name \[Updated in Security Center 1.3 and removed in 2.0\]

Use this property to manage the distinguished name of a LDAP Server record.

This property controls the distinguished name of a LDAP Server record which is inserted when running an out-of-the-box \(OOB\) fix script. If it is set to the recommended value of "" or blank, then LDAP server data can be enumerated by a lower privilege user.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ldap.initial.dn**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

blank

</td></tr><tr><td>

Default value

</td><td>

blank

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.7
-   CVSS score: Low
-   Security risk details: Setting the property value to "" or blank could make LDAP server data accessible to a lower privilege user.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

