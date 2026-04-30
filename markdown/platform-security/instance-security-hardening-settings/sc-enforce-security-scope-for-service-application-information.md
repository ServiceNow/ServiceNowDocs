---
title: Enforce Security Scope for Service Application Information \[New in Security Center 2.0\]
description: Use the glide.enforce\_security\_scope.sn\_svc\_appl property to ensure that the data in master scope tables is secured.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-15"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce Security Scope for Service Application Information \[New in Security Center 2.0\]

Use the **glide.enforce\_security\_scope.sn\_svc\_appl** property to ensure that the data in master scope tables is secured.

When the **glide.enforce\_security\_scope.sn\_svc\_appl\_info** property is set to true, access to resources within the scope is determined solely by the access control lists \(ACLs\) from the Service Application Information plugin \(sn\_svc\_appl\_info\). This ensures the security of data in master scope tables by restricting access permissions to those defined within the sn\_svc\_appl\_info scope.

If set to the insecure value of false, ACLs from all scopes are considered when granting access to data in master scope tables such as sys\_attachment. This could lead to unauthorized access to sensitive information by users who do not have permissions for the Service Application Information data.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_svc\_appl\_info**

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: If this property is set to the insecure value of false, it can lead to unauthorized access to sensitive data by users who do not have permissions for the Service Application Information data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The Service Applicant Information plugin \(**com.sn\_svc\_appl\_info**\) must be activated for the **glide.enforce\_security\_scope.sn\_svc\_appl\_info** property to be effective.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

