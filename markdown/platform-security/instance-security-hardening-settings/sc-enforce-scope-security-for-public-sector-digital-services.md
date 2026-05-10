---
title: Enforce scope security for public sector digital services \[New in Security Center 1.3\]
description: Use the glide.enforce\_security\_scope.sn\_gsm property to control how the application data from the Public Sector Digital Services application is accessed.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce scope security for public sector digital services \[New in Security Center 1.3\]

Use the **glide.enforce\_security\_scope.sn\_gsm** property to control how the application data from the Public Sector Digital Services application is accessed.

The ServiceNow Public Sector Digital Services application lets you develop public sector applications that deliver digital services to constituents, businesses, and agencies.

When **glide.enforce\_security\_scope.sn\_gsm** is set to false, access to the application data within the global tables of the Public Sector Digital Services app may be accessible based on the access control lists \(ACLs\) of those global tables. When this property is set to true, access to data residing in global tables are only evaluated based off the ACLs shipped directly in the Public Sector Digital Services app. Setting this property to false may lead to information disclosure from over permissive ACLs.

To remediate this security risk, set **glide.enforce\_security\_scope.sn\_gsm** to true.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_gsm**

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

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value could lead to information disclosure from over permissive ACLs.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Configuring Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/configuring-public-sector-digital-services.md)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

