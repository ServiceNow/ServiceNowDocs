---
title: Enable SSL in LDAP authentication \[Updated in Security Center 1.5 and 2.0\]
description: Manage the encryption of LDAP authentication requests on your instance.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable SSL in LDAP authentication \[Updated in Security Center 1.5 and 2.0\]

Manage the encryption of LDAP authentication requests on your instance.

Use the **glide.ldap.use.ssl** property to enable or disable TLS encryption for LDAP authentication requests sent over the network. If this property is not set to the recommended value of **true**, LDAP authentication is susceptible to a man-in-the-middle attack.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ldap.use.ssl**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS score: High
-   Security risk details: Setting this property to **false**, makes LDAP authentication vulnerable to a man-in-the-middle attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[LDAP integration](../../../integrate/ldap/concept/c_LDAPIntegration.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

