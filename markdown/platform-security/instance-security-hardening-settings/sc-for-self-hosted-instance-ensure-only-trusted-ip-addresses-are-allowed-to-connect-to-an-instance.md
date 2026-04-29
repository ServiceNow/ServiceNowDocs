---
title: For Self-Hosted Instance, Ensure only Trusted IP Addresses are Allowed to Connect to An Instance
description: Use system properties to control which inbound IP addresses can connect to self-hosted instances.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# For Self-Hosted Instance, Ensure only Trusted IP Addresses are Allowed to Connect to An Instance

Use system properties to control which inbound IP addresses can connect to self-hosted instances.

A self-hosted instance is a customer-managed deployment of the ServiceNow platform, which runs on your own infrastructure instead of ServiceNow's cloud. A instance is classified as self-hosted if the property **glide.installation.self\_hosted** is set to true.

On these self-hosted instances, the **glide.ip.authenticate.allow.self\_hosted\_enabled** system property overrides the inbound IP allow list for an instance when set to true. The **glide.ip.authenticate.allow.secured.self\_hosted\_enabled** system property provides the same functionality in strict mode. Strict mode is enabled when the system property **glide.ip.authenticate.strict** property is set to true.

-   **In strict mode**

    The **glide.ip.authenticate.allow.secured.self\_hosted\_enabled** property replaces the inbound IP allow list with the IP allow list defined in the property **glide.ip.authenticate.allow.secured.self\_hosted\_list**.

-   **Not in strict mode**

    The **glide.ip.authenticate.allow.self\_hosted\_enabled** property replaces the inbound IP allow list with the IP allow list defined in the **glide.ip.authenticate.allow.self\_hosted\_list** property.


All list properties mentioned are strings containing lists of IP ranges that are appended to the inbound IP allow list of an instance. The strings contain a comma separated range of IP addresses in IPv4 or IPv6 format. IP ranges can be specified using a hyphen \(10.0.10.14-10.0.10.19\), using CIDR notation \(10.0.10.0/24\), or consist of a single IP address \(10.0.10.5\).

**Note:** Both of the list properties have a default value of `127.0.0.1` if not set. IP ranges of the property **glide.custom.ip.authenticate.allow** are always appended to the inbound IP allow list, and are not affected by the properties described here. The IP Address Access Controls \[ip\_access\] table is not affected by these properties.

If your instance is self-hosted:

1.  Set the **glide.ip.authenticate.allow.self\_hosted\_enabled** and **glide.ip.authenticate.allow.secured.self\_hosted\_enabled** properties to `true`.
2.  Ensure that the **glide.ip.authenticate.allow.secured.self\_hosted\_list** and **glide.ip.authenticate.allow.self\_hosted\_list** system properties are either not set, or contain a comma-separated value consisting of only trusted IP ranges that you want to allow access to your instance.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.ip.authenticate.allow.self\_hosted\_enabled**
-   **glide.ip.authenticate.allow.secured.self\_hosted\_enabled**
-   **glide.ip.authenticate.allow.secured.self\_hosted\_list**
-   **glide.ip.authenticate.allow.self\_hosted\_list**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   Boolean
-   String
-   String

</td></tr><tr><td>

Recommended value

</td><td>

-   **For self-hosted instances**
    -   `true`
    -   `true`
    -   empty, or a comma-separated list of trusted IP ranges
    -   empty, or a comma-separated list of trusted IP ranges
-   **For ServiceNow hosted instances**
    -   `false`
    -   `false`
    -   `127.0.0.1`
    -   `127.0.0.1`

</td></tr><tr><td>

Default value

</td><td>

-   `false`
-   `false`
-   `127.0.0.1`
-   `127.0.0.1`

</td></tr><tr><td>

Fallback value

</td><td>

-   `false`
-   `false`
-   `127.0.0.1`
-   `127.0.0.1`

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details:

The default IP allow list for instances is geared towards allowing ServiceNow personnel and infrastructure access to an instance. If an instance is self-hosted, the default IP allow list increases the risk of unauthorized or non-essential access to the instance from IPs that should otherwise be blocked on self-hosted instances as these instance are generally not on the ServiceNow network. Setting the properties **glide.ip.authenticate.allow.self\_hosted\_enabled** and **glide.ip.authenticate.allow.secured.self\_hosted\_enabled** to `true` ensures only those IP addresses the instance owner explicitly allows are able to access an instance.


</td></tr><tr><td>

Functional impact

</td><td>

If your instance is self-hosted, there should be no unexpected functional impact from any of these properties as the instance is not on the ServiceNow network, and therefore does not have access to those IP ranges on the default IP allow list. If the instance is not self-hosted, setting these properties may break functionality.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

