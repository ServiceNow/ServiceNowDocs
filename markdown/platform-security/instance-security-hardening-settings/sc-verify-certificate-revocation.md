---
title: Verify certificate revocation
description: The com.glide.communications.httpclient.verify\_revoked\_certificate property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks aren't bypassed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-verify-certificate-revocation.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Verify certificate revocation

The **com.glide.communications.httpclient.verify\_revoked\_certificate** property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks aren't bypassed.

If the **com.glide.communications.httpclient.verify\_revoked\_certificate** property isn't configured to the recommended value of **true**, certificate revocation checks will be skipped during the TLS handshake.

This creates a critical security gap, potentially allowing an attacker to use a revoked certificate undetected and compromise the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications.

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Ensure the **com.glide.communications.httpclient.verify\_revoked\_certificate** property doesn't exist in the sys\_properties table or is set to **true**.

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

Default value

</td><td>

true

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

[Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details:

Not setting the **com.glide.communications.httpclient.verify\_revoked\_certificate** property to the recommended value of **true**, creates a critical security gap, potentially allowing an attacker to use a revoked certificate undetected and compromise the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications.


</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When the **com.glide.communications.httpclient.verify\_revoked\_certificate** is set to **true**, every outbound HTTP request over TLS has its certificate checked for revocation using OCSP or CRL, as governed by the other properties in this family. When this property is set to **false**, no revocation checking is performed at all for outbound TLS connections, regardless of how the other certificate-revocation properties are configured.

</td></tr></tbody>
</table>**Parent Topic:**[Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-communications.md)

