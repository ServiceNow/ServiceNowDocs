---
title: Restrict Impersonation to Admin \[New in Security Center 2.0\]
description: The glide.sys.permissive.impersonate property can be used to prevent non-admin roles from impersonating other users.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-20"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict Impersonation to Admin \[New in Security Center 2.0\]

The **glide.sys.permissive.impersonate** property can be used to prevent non-admin roles from impersonating other users.

When the **glide.sys.permissive.impersonate** property is set to false, only users with the admin role can impersonate other users. When this property is set to true, users may be able to make use of application components that expose impersonation APIs to impersonate a user of higher privilege. This could result in unauthorized access if these application components are misconfigured because non-admin users can access the Impersonation functionality.

You may want to set the property to the non-default value when you need non-admin users to have the capability to impersonate other users.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sys.permissive.impersonate**

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

false

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

-   Severity score: 6.7
-   CVSS score: Medium
-   Security risk details: Failing to set this property to the recommended value of false may allow a non-admin user to utilize application components that expose APIs, enabling them to impersonate a user with higher privileges.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Non-admin users can access Impersonation features with some customizations to other scripts and UI pages. However, it is essential to ensure that only the correct users are granted access to these features.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

