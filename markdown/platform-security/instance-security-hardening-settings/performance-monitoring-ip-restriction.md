---
title: Ensure only Trusted IP Addresses are Allowed to Connect to An Instance
description: Use a system property to define a list of IP ranges that are appended to the outbound IP allow list.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Ensure only Trusted IP Addresses are Allowed to Connect to An Instance

Use a system property to define a list of IP ranges that are appended to the outbound IP allow list.

Use the **glide.custom.ip.authenticate.allow** system property to define a list of IP ranges that are appended to the inbound IP allow list of an instance. The property value contains a comma separated range of IP addresses in IPv4 or IPv6 format. IP ranges are specified using a hyphen \(10.0.10.14-10.0.10.19\), using CIDR notation \(10.0.10.0/24\), or consist of a single IP address \(10.0.10.5\). IP ranges in this property will be allowed to connect to an instance, unless listed in the IP deny list.

IP ranges in this property are appended to the inbound IP allow list regardless of the value of the **glide.ip.authenticate.strict** property. The IP Address Access Controls \[ip\_access\] table provides an equivalent option to add to both the inbound/outbound allow/deny IP lists of an instance. Refer to the Steps to Configure section in [IP range based authentication](../../login/concept/c_IPRangeBasedAuthentication.md).

Ensure that the **glide.custom.ip.outbound.authenticate.allow** system property value is either an empty, or a comma-separated list containing only trusted IP ranges that your want to allow your instance to access.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.custom.ip.authenticate.allow**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String

</td></tr><tr><td>

Recommended value

</td><td>

Empty, or a comma-separated list containing only trusted IP ranges that your want to allow your instance to access.

</td></tr><tr><td>

Default value

</td><td>

None

</td></tr><tr><td>

Fallback value

</td><td>

None

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](../../security-center/reference/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details:

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](../../security-center/reference/sc-architecture-design-threat-molding.md)

