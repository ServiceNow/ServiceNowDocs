---
title: Configure Service Portal Widgets Table Allow List \[New in Security Center 2.0\]
description: Learn how the glide.service\_portal.widget.table\_allow\_list property enhances security by listing tables accessible to unauthenticated users through Service Portal widgets, dependent on additional checks and specific glide property settings.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-15"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Configure Service Portal Widgets Table Allow List \[New in Security Center 2.0\]

Learn how the **glide.service\_portal.widget.table\_allow\_list** property enhances security by listing tables accessible to unauthenticated users through Service Portal widgets, dependent on additional checks and specific glide property settings.

The **glide.service\_portal.widget.table\_allow\_list** property contains a list of tables that unauthenticated users can access through Service Portal widgets, which utilize the additional security checks in the SNCACLWidgetUtil script. This property is enforced only if the glide property **glide.service\_portal.widget.enforce\_public\_check** is set to true. Including unnecessary tables in this property may lead to the disclosure of sensitive information. Nonetheless, Table ACLs will continue to be evaluated as they were previously.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.service\_portal.widget.table\_allow\_list**

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

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: If this property is not set to the secure value, unnecessary tables may be included, potentially leading to the disclosure of sensitive information.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **glide.service\_portal.widget.enforce\_public\_check** property must be set to true for the **glide.service\_portal.widget.table\_allow\_list** setting to take effect.

</td></tr><tr><td>

Functional impact

</td><td>

The table list controls access to the tables from which the widget is allowed to retrieve data.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

