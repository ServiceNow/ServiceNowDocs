---
title: Do not use demo certificates for active SAML configurations
description: Control whether demo certificates are used in production SAML configurations.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Do not use demo certificates for active SAML configurations

Control whether demo certificates are used in production SAML configurations.

The demo certificates provided by ServiceNow should not be used in production SAML configurations. The certificates are common among all instances with known passphrase. If one of the SAML properties utilizing a certificate keystore is active \(**require\_signed\_authnrequest**, **require\_signed\_logoutrequest**, or **encrypt\_assertion**\) then the demo data must not be used. Since demo data is shared among all instance, there is no integrity guarantee of requests signed with shared certificates.

Set up a custom keystore, following the documentation. The value of **glide.authenticate.sso.saml2.keystore** should be set to the sys\_id of a custom, active keystore.

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

String

</td></tr><tr><td>

Recommended value

</td><td>

Does not contain the sys\_id `c60ad24b732220103a5b0dd43cf6a7db` or `3685fc22930212003c5537ae867ffb91`

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.9
-   CVSS rating: Low
-   Security risk details: Messages encrypted by the IDP could be decrypted by any actor, if intercepted.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Communications](sc-communications.md)

