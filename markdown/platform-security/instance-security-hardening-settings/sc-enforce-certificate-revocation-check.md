---
title: Enforce CRL certificate revocation checking for outbound HTTP requests
description: Use the com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status property to control whether the platform terminates outbound HTTP requests when Certificate Revocation List \(CRL\) checks can't determine revocation status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-certificate-revocation-check.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [certificate revocation, CRL, OCSP, TLS, outbound HTTP]
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce CRL certificate revocation checking for outbound HTTP requests

Use the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property to control whether the platform terminates outbound HTTP requests when Certificate Revocation List \(CRL\) checks can't determine revocation status.

The ability to verify certificate revocation status strengthens the authentication process. However, revocation checks are out-of-band requests to a certificate authority's revocation endpoint. Network failures, DNS resolution issues, or unavailable revocation services may cause the check to fail and halt outbound HTTP requests, creating a potential denial-of-service condition. The denial-of-service risk is mitigated by caching of revocation check results.

Two main approaches check certificate revocation status: Certificate Revocation Lists \(CRLs\) and Online Certificate Status Protocol \(OCSP\).

When the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property is set to `false` and the CRL check can't determine revocation status, the platform continues with remaining certificate validations \(hostname, expiration, signature, certificate chain\).

When set to `true` and the CRL check can't determine revocation status, the platform either terminates the connection or falls back to OCSP revocation checking. If OCSP is also unable to determine revocation status, the connection is terminated.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Set the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property to `true`.

## More information

<table id="table_property_details-enforce-cert-revocation-check"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status**

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

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.3
-   CVSS rating: Low
-   Security risk details:

Outbound HTTP requests that rely on TLS certificate validation for the remote hosts may be impacted if the CRL revocation check can't be completed. The platform may connect to remote hosts with revoked certificates, leading to a loss in authentication and possible loss in confidentiality.


</td></tr><tr><td>

Functional impact

</td><td>

The **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property affects any platform functionality that makes outbound HTTP requests over TLS, for example Integration Hub or Outbound Web Services.

 When set to `false`, if CRL can't determine the revocation status, the platform verifies the next certificate in the chain and allows the connection with the remote host.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property interacts with the **com.glide.communications.httpclient.disable\_crl\_check** property.

 -   If the **com.glide.communications.httpclient.disable\_crl\_check** property is set to `false` and the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property is set to `true`, the platform will perform the CRL revocation check for the certificate.
-   If the **com.glide.communications.httpclient.disable\_crl\_check** property is set to `true`, then the **com.glide.communications.httpclient.fail\_on\_non\_pass\_crl\_status** property value will not have any effect. The platform will perform the OCSP revocation check for the certificate.

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

