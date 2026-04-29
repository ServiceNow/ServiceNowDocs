---
title: Restrict Impersonation to Admin
description: The glide.sys.permissive.impersonate property can be used to prevent non-admin roles from impersonating other users.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict Impersonation to Admin

The **glide.sys.permissive.impersonate** property can be used to prevent non-admin roles from impersonating other users.

When the **glide.sys.permissive.impersonate** system property is set to a value of **false**, only users with the **admin** role may impersonate. When this value is set to **true**, users may be able to make use of application components that expose impersonation APIs to impersonate a higher privileged user.

Ensure that the property **glide.sys.permissive.impersonate** is set to a value of **false**. If this property does not exist, the default value is **false**.

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

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: May result in unauthorized resource access if these application components are misconfigured.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Non-admin users can access Impersonation features with some customizations to other scripts and UI pages. However, it is essential to ensure that only the correct users are granted access to these features.**Note:** When **glide.sys.permissive.impersonate** is set to true, Non-admin users with the **impersonate** role can still impersonate.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

