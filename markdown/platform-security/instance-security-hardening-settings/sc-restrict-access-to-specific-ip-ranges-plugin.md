---
title: Restrict access to specific IP ranges plugin
description: Use the com.snc.ipauthenticator plugin to restrict access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to specific IP ranges plugin

Use the **com.snc.ipauthenticator** plugin to restrict access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks.

The **com.snc.ipauthenticator** plugin, when set to **true**, restricts access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks.

Ensure that the **com.snc.ipauthenticator** plugin is activated and there is at least one active IP access policy in the IP Address Access Controls \[ip\_access\] table.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **com.snc.ipauthenticator**
-   **IP Address Access Controls \[ip\_access\]**

</td></tr><tr><td>

Configuration type

</td><td>

-   Plugin \(/v\_plugin\_list.do\)
-   Table record \(/ip\_access\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

N/A

</td></tr><tr><td>

Recommended value

</td><td>

-   The **com.snc.ipauthenticator** plugin is active.
-   The IP Address Access Controls \[ip\_access\] table contains at least one active record.

</td></tr><tr><td>

Default value

</td><td>

-   The **com.snc.ipauthenticator** plugin is active by default.
-   The IP Address Access Controls \[ip\_access\] table contains no records by default.

</td></tr><tr><td>

Fallback value

</td><td>

-   The **com.snc.ipauthenticator** plugin is active by default.
-   The IP Address Access Controls \[ip\_access\] table contains no records by default.

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS rating: Medium
-   Security risk details: Allowing unrestricted public access to a ServiceNow instance without properly configuring the IP Address Access Control plugin exposes the system to unauthorized access and potential exploitation from any IP address, undermining network-level security and increasing the attack surface.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This plugin when set to true restricts access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks. An exclusion list \(Deny\) or an inclusion list \(Allow\) of IP addresses can be created through IP Address Access Control \(ip\_access\_list.do\).

 Before setting this property, you must activate the IP Range Based Authentication \(com.snc.ipauthenticator\)**com.snc.ipauthenticator** plugin. To learn more, see [IP range based authentication](../../login/concept/c_IPRangeBasedAuthentication.md) and in the Steps to configure section \(below\).

 Ensure the plugin **com.snc.ipauthenticator** is activated and there is at least one active IP access policy in the table ip\_access.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

