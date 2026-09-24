---
title: Enforce OCSP check on network error
description: Learn how to configure the com.glide.communications.httpclient.ocsp\_allow\_network\_error property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-ocsp-check-on-network-error.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Enforce OCSP check on network error

Learn how to configure the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.

If this property is not set to **false**, the system treats OCSP validation as successful by default. This occurs when the Online Certificate Status Protocol \(OCSP\) check encounters a network-related issue such as a timeout or failure to retrieve revocation data.

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Ensure the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property exists and is set to `false`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.communications.httpclient.ocsp\_allow\_network\_error**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: An attacker using a revoked certificate can exploit this setting by simply omitting the OCSP response during a connection attempt. In such cases, the client incorrectly accepts the revoked certificate as valid. This undermines the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications. The use of revoked certificates is often indicative of malicious activity, unless attributable to temporary synchronization issues between certificate authorities and OCSP responders.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property has no effect unless the **com.glide.communications.httpclient.verify\_revoked\_certificate** property, the overall gate for certificate revocation checking, is set to `true`.

</td></tr><tr><td>

Functional impact

</td><td>

When the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property is set to `false`, an outbound HTTPS connection is not established if the OCSP responder becomes unreachable due to a network error. Network errors include timeouts or DNS failures. Administrators should monitor OCSP responder availability after making this change, as any outbound integration with a temporarily unreachable OCSP responder will fail to connect.

</td></tr></tbody>
</table>**Parent Topic:**[Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-communications.md)

