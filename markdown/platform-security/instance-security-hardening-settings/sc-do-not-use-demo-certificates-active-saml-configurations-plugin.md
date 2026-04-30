---
title: Do not use demo certificates for active saml configurations \[Updated in Security Center 1.5\]
description: Control whether demo certificates are used in production SAML configurations.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Do not use demo certificates for active saml configurations \[Updated in Security Center 1.5\]

Control whether demo certificates are used in production SAML configurations.

The demo certificates provided by ServiceNow should not be used in production SAML configurations because they are common among all instances with a known passphrase. If one of the SAML properties using a certificate keystore is active \(**require\_signed\_authnrequest**, **require\_signed\_logoutrequest**, or **encrypt\_assertion**\), then the demo data shouldn’t be used. Since demo data is shared among all instances, there is no integrity guarantee of requests signed with shared certificates. Therefore, any message encrypted by the IDP could be decrypted by a bad actor if intercepted.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.sso.saml2.keystore**

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

sys\_id of a custom keystore

</td></tr><tr><td>

Default value

</td><td>

empty string

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.9
-   CVSS score: Low

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Communications](sc-communications.md)

