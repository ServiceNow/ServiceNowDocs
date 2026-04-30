---
title: Certificate based authentication not enforced \[New in Security Center 1.3\]
description: The glide.authenticate.mutual.enabled property enables certificate based authentication, a type of mutual authentication for inbound REST connections to REST and SOAP APIs in the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Certificate based authentication not enforced \[New in Security Center 1.3\]

The **glide.authenticate.mutual.enabled** property enables certificate based authentication, a type of mutual authentication for inbound REST connections to REST and SOAP APIs in the ServiceNow AI Platform.

Mutual authentication establishes trust between server and client by exchanging secure socket layer \(SSL\) certificates to validate the certificate with a trusted Certificate Authority. This allows verification that a trusted source is connecting to the ServiceNow AI Platform. If this instance is not set to the recommended value of true, an instance could be vulnerable to man-in-the-middle attacks \(MitM\).

To remediate this security threat, enable mutual authentication for inbound web services. If it's your first time installing the certificate-based authentication plugin \(**com.glide.auth.mutual\)** for the ServiceNow AI Platform, then follow the [Set up Certificate-based authentication](../../../integrate/authentication/task/set-up-mutual-auth.md#) instructions. In addition, ensure that the **glide.authenticate.mutual.enabled** property is set to true to activate the plugin.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.mutual.enabled**

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

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security risk details: If this property is not set to the recommended value of true, then certificate based authentication does not validate certificates with a trusted Certificate Authority. This increases the chances of a bad actor attacking an instance using MitM attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [https://csrc.nist.gov/glossary/term/man\_in\_the\_middle\_attack](https://csrc.nist.gov/glossary/term/man_in_the_middle_attack)
-   [Certificate-based authentication](../../../integrate/authentication/concept/certificate-based-authentication.md)
-   [Configuring mutual authentication](../../security/concept/c_MutualAuthentication.md)

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

