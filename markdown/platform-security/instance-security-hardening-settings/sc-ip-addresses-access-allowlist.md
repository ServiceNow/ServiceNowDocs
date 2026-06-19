---
title: Define allowed ServiceNow internal IP addresses \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.ip.authenticate.strict property to specify IP ranges that can make inbound connections on an instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-ip-addresses-access-allowlist.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-01-26"
reading_time_minutes: 3
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Define allowed ServiceNow internal IP addresses \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.ip.authenticate.strict** property to specify IP ranges that can make inbound connections on an instance.

Use the **glide.ip.authenticate.strict** property to reduce the scope of the IP allow list of an instance and restrict the IP addresses that ServiceNow personnel can use to make inbound/outbound connections to an instance. The exact IP ranges removed from the IP allow list by this property may be adjusted over time as the ServiceNow internal network changes. When set to true, **glide.ip.authenticate.strict** always guarantees an IP allow list that is equal to or more restrictive than the default.

-   **When glide.ip.authenticate.strict is set to true:**

    A strict list of ServiceNow IP ranges replaces the default IP allow lists for inbound and outbound requests. This IP allow list, which starts with a more restrictive predefined set of allowed IP ranges, is replaced by the property glide.ip.authenticate.allow.secured.self\_hosted\_list if the instance is self-hosted.

-   **When glide.ip.authenticate.strict is set to false:**

    The default IP allow list is used which contains a wider set of ServiceNow IP ranges. The default IP allow list is replaced by the contents of glide.ip.authenticate.allow.self\_hosted\_list if the instance is self-hosted.


**Note:** The **glide.ip.authenticate.allow.secured** property contains the ServiceNow data center and secure VPN IP ranges used when **glide.ip.authenticate.strict** is set to true. This property is maintained and deployed automatically by ServiceNow. Customers do not need to configure it. The only customer action required by this hardening setting is to set **glide.ip.authenticate.strict** to `true`.

**Note:** Regardless of the value of **glide.ip.authenticate.strict** or if the instance is self-hosted, the allow list includes IP addresses in the **glide.custom.ip.authenticate.allow** and **glide.custom.ip.outbound.authenticate.allow** system properties, if defined.

All IP list properties share the same format, which is a comma separated range of IP addresses in IPv4 or IPv6 format. IP ranges are specified using a hyphen \(10.0.10.14-10.0.10.19\), using CIDR notation \(10.0.10.0/24\), or consist of a single IP address \(10.0.10.5\). At runtime, you can make additions to the IP allow list by adding entries to the IP Address Access Controls \[ip\_access\] table. To restrict all inbound access to a defined set of IP addresses, add a deny-all entry to the \[ip\_access\] table and then add the specific IP addresses or ranges that you want to allow.

**Warning:** The value for this property is a no DB override. It can't be altered or overridden.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.ip.authenticate.strict**
-   **glide.ip.authenticate.allow.secured**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   String

</td></tr><tr><td>

Recommended value

</td><td>

-   true
-   Managed by ServiceNow. Contains ServiceNow data center and secure VPN IP ranges. This value is deployed automatically and cannot be modified by customers.

</td></tr><tr><td>

Default value

</td><td>

-   false
-   &lt;empty&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   false
-   &lt;empty&gt;

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security Risk Details: Broader access increases the risk of unauthorized or unnecessary access to the instance by non-essential internal users, such as support or sales staff, and reduces control over privileged access. Enforcing strict IP authentication limits connectivity to essential infrastructure, strengthening security and reducing exposure to insider threats or misconfiguration.

</td></tr><tr><td>

Functional impact

</td><td>

This should have no functional impact. It may restrict non-essential ServiceNow personal from accessing an instance. However, these are individuals that do not generally require access to such instances. If access is required, you can grant it on a case by case basis using the IP Address Access Controls \[ip\_access\] table.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see .

**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

