---
title: Verify certificate chain and hostname
description: Configure the com.glide.communications.httpclient.verify\_hostname property to prevent man-in-the-middle-attacks by ensuring that the certification verification process is executed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-verify-certificate-chain-and-hostname.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Verify certificate chain and hostname

Configure the **com.glide.communications.httpclient.verify\_hostname** property to prevent man-in-the-middle-attacks by ensuring that the certification verification process is executed.

When the **com.glide.communications.httpclient.verify\_hostname** property is not set to the secure value of **true**, the hostname and certificate chain presented by remote hosts during a TLS connection initiated from the ServiceNow instance are not validated.

This vulnerability compromises the security of the TLS connection and allows person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.

Ensure that the **com.glide.communications.httpclient.verify\_hostname** system property is set to the secure value of **true**.

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

false

</td></tr><tr><td>

Category

</td><td>

[Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: High
-   CVSS score: 7.4
-   Security risk details: This vulnerability compromises the security of the TLS connection and allows person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.communications.httpclient.verify\_hostname** property governs hostname and certificate chain validation independently of the **com.glide.communications.httpclient.verify\_revoked\_certificate** property, the overall gate for certificate revocation checking.

</td></tr><tr><td>

Functional impact

</td><td>

When the **com.glide.communications.httpclient.verify\_hostname** property is set to **true**, an outbound HTTPS connection is rejected if the remote host's certificate does not match the requested hostname or its certificate chain can't be validated. Outbound integrations to hosts with a mismatched or misconfigured certificate will fail to connect once this property is set to true.

</td></tr></tbody>
</table>**Parent Topic:**[Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-communications.md)

