---
title: Reduce the Scope of the IP Allow List for an Instance
description: Use the glide.ip.authenticate.strict property to specify IP ranges that can make inbound connections on an instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Reduce the Scope of the IP Allow List for an Instance

Use the **glide.ip.authenticate.strict** property to specify IP ranges that can make inbound connections on an instance.

Use the **glide.ip.authenticate.strict** property to reduce the scope of the IP allow list of an instance and restrict the IP addresses that ServiceNow personnel can use to make inbound/outbound connections to an instance. The exact IP ranges removed from the IP allow list by this property may be adjusted over time as the ServiceNow internal network changes. When set to true, **glide.ip.authenticate.strict** always guarantees an IP allow list that is equal to or more restrictive than the default.

-   **When glide.ip.authenticate.strict is set to true:**

    A strict list of ServiceNow IP ranges replaces the default IP allow lists for inbound and outbound requests. This IP allow list, which starts with a more restrictive predefined set of allowed IP ranges, is replaced by the property glide.ip.authenticate.allow.secured.self\_hosted\_list if the instance is self-hosted.

-   **When glide.ip.authenticate.strict is set to false:**

    The default IP allow list is used which contains a wider set of ServiceNow IP ranges. The default IP allow list is replaced by the contents of glide.ip.authenticate.allow.self\_hosted\_list if the instance is self-hosted.


**Note:** Regardless of the value of **glide.ip.authenticate.strict** or if the instance is self-hosted, the allow list includes IP addresses in the **glide.custom.ip.authenticate.allow** and **glide.custom.ip.outbound.authenticate.allow** system properties, if defined.

All IP list properties share the same format, which is a comma separated range of IP addresses in IPv4 or IPv6 format. IP ranges are specified using a hyphen \(10.0.10.14-10.0.10.19\), using CIDR notation \(10.0.10.0/24\), or consist of a single IP address \(10.0.10.5\). At runtime, you can make additions to the IP allow list by adding entries to the IP Address Access Controls \[ip\_access\] table. This table can also be used to explicitly deny IP ranges access to an instance.

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
-   Contains only trusted values

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

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

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
</table>**Note:** A deny all rule is needed to be added into IP access control to restrict access from any IP's not added into IP access control. All required allowed IP's are then needed to be added into IP access control.

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

