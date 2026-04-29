---
title: Enable Cross Scope Privilege Checks on Service Portal Form \[New in Security Center 7.0\]
description: Use a system property to enforce cross scope privilege checks on the Service Portal form widget and prevent unauthorized retrieval of forms and table data between scopes.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable Cross Scope Privilege Checks on Service Portal Form \[New in Security Center 7.0\]

Use a system property to enforce cross scope privilege checks on the Service Portal form widget and prevent unauthorized retrieval of forms and table data between scopes.

In Yokohama and later releases, queries enforce cross scope privilege checks on the table before reading the given sys\_id information.

When the **glide.service\_portal.enforce\_cross\_scope\_check\_in\_form** property is set to the recommended value of **true**, cross scope privilege checks are enforced on the table. When set to **false**, the cross-scope privilege check isn’t enforced.

Set the **glide.service\_portal.enforce\_cross\_scope\_check\_in\_form** system property to **true** or confirm that the property doesn’t exist in the System Properties \[sys\_properties\] table. If a record doesn’t exist in the sys\_properties table, the value defaults to **true**.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.service\_portal.enforce\_cross\_scope\_check\_in\_form**

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

-   Severity score: 3.1
-   CVSS score: Low
-   Security risk details: A lack of cross scope privilege checks could lead to unauthorized retrieval of forms and table data between scopes.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

