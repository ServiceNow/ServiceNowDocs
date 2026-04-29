---
title: Verify certificate revocation
description: The com.glide.communications.httpclient.verify\_revoked\_certificate property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks are not bypassed.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Verify certificate revocation

The **com.glide.communications.httpclient.verify\_revoked\_certificate** property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks are not bypassed.

If the **com.glide.communications.httpclient.verify\_revoked\_certificate** system property isn't configured to the recommended value of **true**, certificate revocation checks will be skipped during the TLS handshake.

Ensure the property **com.glide.communications.httpclient.verify\_revoked\_certificate** is set to **true**.

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
-   Security risk details: This omission undermines a critical security control, potentially allowing an attacker to use a revoked certificate without detection. As a result, it compromises the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications.

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

