---
title: Enable CRL-based certificate revocation checking for outbound HTTP requests
description: Use the com.glide.communications.httpclient.disable\_crl\_check property to control Certificate Revocation List \(CRL\) revocation checking for outbound HTTP requests over Transport Layer Security \(TLS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-crl-based-checking-for-outbound-http-requests.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [certificate revocation, CRL, OCSP, TLS, outbound HTTP]
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enable CRL-based certificate revocation checking for outbound HTTP requests

Use the **com.glide.communications.httpclient.disable\_crl\_check** property to control Certificate Revocation List \(CRL\) revocation checking for outbound HTTP requests over Transport Layer Security \(TLS\).

When the **com.glide.communications.httpclient.disable\_crl\_check** property is set to `false`, CRL checking remains available as a revocation-check mechanism. Outbound HTTP requests over TLS that connect to hosts whose certificates only provide a CRL distribution point have their certificate checked against that CRL before the connection proceeds.

When set to `true`, CRL checking is never performed, regardless of whether a certificate provides a CRL distribution point. The platform relies solely on Online Certificate Status Protocol \(OCSP\) for revocation checking.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Set the **com.glide.communications.httpclient.disable\_crl\_check** property to `false`.

## More information

<table id="table_property_details-enable-crl-based-checking"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.communications.httpclient.disable\_crl\_check**

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

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating: High
-   CVSS score: 7.5
-   Security risk details:

When set to `true`, certificates that only provide a CRL distribution point \(and no OCSP responder\) are never checked for revocation. Certificates encountering an OCSP processing error can't fall back to a CRL-based check.

The platform can establish outbound HTTPS connections to hosts with revoked certificates. This results in loss of authentication and possible loss of confidentiality.


</td></tr><tr><td>

Functional impact

</td><td>

When set to `false`, certificates with only a CRL distribution point are checked against the CRL before the outbound TLS connection proceeds.

 If the certificate authority's CRL endpoint can't be reached, the platform's handling is governed by the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.communications.httpclient.disable\_crl\_check** property has no effect unless the **com.glide.communications.httpclient.verify\_revoked\_certificate** property, the overall gate for certificate revocation checking, is set to `true`.

 The **com.glide.communications.httpclient.disable\_crl\_check** property interacts with the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property:

 -   When **com.glide.communications.httpclient.disable\_crl\_check** is set to `true`, the **fail\_on\_non\_pass\_crl\_status** property has no effect, since CRL checking is never performed.
-   When **com.glide.communications.httpclient.disable\_crl\_check** is set to `false`, the **fail\_on\_non\_pass\_crl\_status** property determines whether the platform terminates connections when CRL checks can't determine revocation status.

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

