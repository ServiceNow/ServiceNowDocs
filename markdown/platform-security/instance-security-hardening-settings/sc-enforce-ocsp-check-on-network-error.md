---
title: Enforce OCSP check on network error \[New in Security Center 1.3 and updated in 2.0\]
description: Learn how to configure the com.glide.communications.httpclient.ocsp\_allow\_network\_error property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Enforce OCSP check on network error \[New in Security Center 1.3 and updated in 2.0\]

Learn how to configure the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.

If **com.glide.communications.httpclient.ocsp\_allow\_network\_error** is not set to the recommended value of false, and the Online Certificate Status Protocol \(OCSP\) check encounters a network error \(for example, a timeout or problem fetching the revocation information\), it will bypass the OCSP security check and consider it successful. This could allow an attacker with a revoked certificate to break the Public Key infrastructure \(PKI\) and digital certificate trust that is foundational to the web. The use of revoked certificates is often an indicator of malicious activity unless the servers are out of sync.

Ensure the property **com.glide.communications.httpclient.ocsp\_allow\_network\_error** exists and is set to false. If the property does not appear in the sys\_properties table, add a new record.

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

boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

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

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: Not setting this property to false could enable a bad actor to bypass the OCSP security check.

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

