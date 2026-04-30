---
title: Verify certificate chain and hostname \[New in Security Center 1.3 and updated in 2.0\]
description: Configure the com.glide.communications.httpclient.verify\_hostname property to prevent man-in-the-middle-attacks by ensuring that the certification verification process is executed.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Verify certificate chain and hostname \[New in Security Center 1.3 and updated in 2.0\]

Configure the **com.glide.communications.httpclient.verify\_hostname** property to prevent man-in-the-middle-attacks by ensuring that the certification verification process is executed.

When the Glide Property **com.glide.communications.httpclient.verify\_hostname** is not set to the secure value of true, the hostname and certificate chain presented by remote hosts during a TLS connection initiated from the ServiceNow instance are not validated. This could compromise the security of the TLS connection and allow person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.communications.httpclient.verify\_hostname**

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

false

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: High
-   CVSS score: 7.4
-   Security risk details: Not setting **com.glide.communications.httpclient.verify\_hostname** to the recommended value of true could make your instance vulnerable to man-in-the-middle-attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Verifies hostname and certificate chain presented by remote secure socket layer \(SSL\) hosts. Set this property to true to secure against Man-in-the-middle \(MITM\) attacks.**Note:** This property overrides the **com.glide.communications.trustmanager\_trust\_all**, property.

</td></tr></tbody>
</table>**Parent Topic:**[Communications](sc-communications.md)

