---
title: Verify certificate revocation \[New in Security Center 1.3\]
description: The com.glide.communications.httpclient.verify\_revoked\_certificate property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks are not bypassed.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Verify certificate revocation \[New in Security Center 1.3\]

The **com.glide.communications.httpclient.verify\_revoked\_certificate** property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks are not bypassed.

If **com.glide.communications.httpclient.verify\_revoked\_certificate** is not set to the recommended value of **true**, then certificate revocation will not be checked during the TLS handshake. TLS encrypts data sent over the Internet to ensure that bad actors are unable to see sensitive information such as passwords or credit card numbers. Bypassing the TLS handshake is a security risk because an attacker with a revoked certificate can neglect to provide a valid certificate and break public key infrastructure \(PKI\) and digital certificate trust.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.communications.httpclient.verify\_revoked\_certificate**

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

true

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: Not setting **com.glide.communications.httpclient.verify\_revoked\_certificate** to the recommended value of true will cause certificate revocation to not be checked during the TLS handshake.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property should be set to true to ensure that a Transport Layer Security \(TLS\) session is started with an authentic endpoint. If this property is set to false, then the certificate is not checked, which could compromise the security of the instance.

</td></tr></tbody>
</table>**Parent Topic:**[Communications](sc-communications.md)

