---
title: Enforce OCSP check on network error
description: Learn how to configure the com.glide.communications.httpclient.ocsp\_allow\_network\_error property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Enforce OCSP check on network error

Learn how to configure the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.

If the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** system property is not explicitly set to the recommended value of **false**, and the OCSP \(Online Certificate Status Protocol\) check encounters a network-related issue, such as a timeout or failure to retrieve revocation data, the system will treat the OCSP validation as successful by default.

Ensure the property **com.glide.communications.httpclient.ocsp\_allow\_network\_error** exists and is set to false. If the property does not appear in the System Properties \[sys\_properties\] table, add a new record.

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: An attacker using a revoked certificate could exploit this by simply omitting the OCSP response during a connection attempt. In such cases, the client would incorrectly accept the revoked certificate as valid, thereby undermining the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications. The use of revoked certificates is often indicative of malicious activity, unless attributable to temporary synchronization issues between certificate authorities and OCSP responders.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property determines whether a request against the Authority Information Access \(AIA\) Online Certificate Status Protocol \(OCSP\) uri results in a pass or fail outcome in the event of a connection or timeout error. When set to false, the revocation status of the presented server certificate can't be validated and will lead to a communication failure with that endpoint. If a network error occurs when the property is set to its default value of true, the certificate is treated as valid from a revocation standpoint.

</td></tr></tbody>
</table>**Parent Topic:**[Communications](sc-communications.md)

