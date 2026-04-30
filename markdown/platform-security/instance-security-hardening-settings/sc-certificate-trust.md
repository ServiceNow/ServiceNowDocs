---
title: Enforce certificate trust \[Updated in Security Center 1.3 and removed in 2.0\]
description: Use system properties to ensure that certificate expiration and trust are checked for certificates received from outbound HTTPS call endpoints when host verification is not performed.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-06-11"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Enforce certificate trust \[Updated in Security Center 1.3 and removed in 2.0\]

Use system properties to ensure that certificate expiration and trust are checked for certificates received from outbound HTTPS call endpoints when host verification is not performed.

When **com.glide.communications.trustmanager\_trust\_all** is set to **true**, then certificate expiration and trust are not checked for the certificate received from an outbound HTTPS call endpoint when host verification is not performed.

Verify that the **com.glide.communications.trustmanager\_trust\_all** system property is set to the recommended value of **false**. This ensures that your instance only trusts certificates that it can verify against the JVM certificate store. Self-signed and enterprise-signed certificates are not trusted. This property only applies when **com.glide.communications.httpclient.verify\_hostname** is set to **false**.

**Note:** The values for these properties are  and cannot be altered once changed \(they are non-revertible\). For security purposes, do not change this property value. If you have further questions, contact Customer Service and Support.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**com.glide.communications.trustmanager\_trust\_all**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Purpose

</td><td>

To enforce certificate validation for outgoing requests.

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Security risk rating

</td><td>

5.7

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces strict validation on certificate CA \(certificate authority\) field. If a trusted entity \(CA\) issued the certificate, the instance accepts it for further use.

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) For confidentiality and integrity reasons, application should validate the certificate's CA before using the certificate for any transactional operations.

</td></tr><tr><td>

References

</td><td>

[Certificates](../../general/concept/c_Certificates.md)

 [Verify certificate chain and hostname \[New in Security Center 1.3 and updated in 2.0\]](sc-verify-certificate-chain-and-hostname.md)

</td></tr></tbody>
</table>**Parent Topic:**[Communications](sc-communications.md)

