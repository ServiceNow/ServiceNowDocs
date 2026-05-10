---
title: Enable password reset policy checks
description: Use the glide.enable.password\_policy property to enable password policy checks whenever a user changes their password using the user interface.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable password reset policy checks

Use the **glide.enable.password\_policy** property to enable password policy checks whenever a user changes their password using the user interface.

Use the **glide.enable.password\_policy** property to customize password strength validation rules for the Change Password form. Customize the length and complexity values to match your organization's security policy. If **glide.enable.password\_policy** is not set to the recommended value of **true**, then password standards will not be enforced.

Ensure that the **glide.enable.password\_policy** system property exists in the System Properties \[sys\_properties\] table and is set to the value **true**. If the property does not appear in the System Properties \[sys\_properties\] table, add a new record.

**Important:** The **glide.enable.password\_policy** does not apply when an administrator changes a password or adds a user through script.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enable.password\_policy**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.4
-   CVSS rating: High
-   Security risk details: Enforcing password complexity is critical to maintaining strong authentication and reducing exposure to account takeover.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Authentication](sc-authentication.md)

