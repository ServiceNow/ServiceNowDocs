---
title: Double check inbound transactions
description: Use the glide.security.strict.updates property to enable double-checking of security on inbound transactions during form submission. When you set this property to true, it adds an extra layer of table validation before a form renders in the browser.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Double check inbound transactions

Use the **glide.security.strict.updates** property to enable double-checking of security on inbound transactions during form submission. When you set this property to **true**, it adds an extra layer of table validation before a form renders in the browser.

The **glide.security.strict.updates** system property provides an extra layer of security on form submission / field updates by ensuring only users with the proper permissions are allowed to update a form. If **glide.security.strict.updates** is not set to the recommended value of **true**, then updates are not strict meaning they are able to modify fields visible to them regardless of whether they have the appropriate permissions.

Ensure that the property **glide.security.strict.updates** exists in the System Properties \[sys\_properties\] table and is set to "true".

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.strict.updates**

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: Users may be able to update form fields simply by having visibility into them, regardless of their actual permissions, creating a risk of unauthorized data modification and privilege escalation.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Access control](sc-access-control.md)

