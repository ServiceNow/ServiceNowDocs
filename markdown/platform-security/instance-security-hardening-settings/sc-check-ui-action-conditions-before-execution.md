---
title: Check UI action conditions before execution
description: Use the glide.security.strict.actions property to enable checking of UI actions conditions in forms and lists before they execute. When you set this property to true, it adds an extra layer of validation on the table UI actions before they are executed.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Check UI action conditions before execution

Use the **glide.security.strict.actions** property to enable checking of UI actions conditions in forms and lists before they execute. When you set this property to true, it adds an extra layer of validation on the table UI actions before they are executed.

If the **glide.security.strict.actions** system property isn't set to the recommended value of **true**, then there is no validation on the table UI before execution. Setting this property to secure value adds an extra layer of security validation.

Ensure that the property **glide.security.strict.actions** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.strict.actions**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.3
-   CVSS rating: Low
-   Security risk details: Users may perform operations they may not be authorized for, potentially leading to unauthorized data manipulation, privilege escalation, and bypassing of access controls designed to protect sensitive records.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation only adds an extra layer of validation to check for UI actions on the target table/page on the instance. As long as the access controls are set appropriately on the customer instance, there should not be an impact here.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

