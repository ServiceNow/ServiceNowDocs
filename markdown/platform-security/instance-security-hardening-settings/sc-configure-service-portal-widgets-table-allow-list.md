---
title: Configure Service Portal Widgets Table Allow List
description: Learn how the glide.service\_portal.widget.table\_allow\_list property enhances security by listing tables accessible to unauthenticated users through Service Portal widgets, dependent on additional checks and specific glide property settings.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Configure Service Portal Widgets Table Allow List

Learn how the **glide.service\_portal.widget.table\_allow\_list** property enhances security by listing tables accessible to unauthenticated users through Service Portal widgets, dependent on additional checks and specific glide property settings.

The **glide.service\_portal.widget.table\_allow\_list** property contains the list of tables allowed to be accessed by unauthenticated users through Service Portal widgets that make use of the additional security checks provided in the SNCACLWidgetUtil script include. This property is only enforced if the Glide Property The **glide.service\_portal.widget.table\_allow\_list** property is **true**. There may be unauthenticated information disclosure if unnecessary tables are listed in this property. Table ACLs will still be evaluated as previously occurred.

Ensure that the **glide.service\_portal.widget.table\_allow\_list** property is empty, or the list is restricted to the smallest number of tables with use cases for unauthenticated access.

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

String

</td></tr><tr><td>

Recommended value

</td><td>

&lt;empty&gt;

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

&lt;empty&gt;

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS rating: Low
-   Security risk details: Unauthenticated users may gain access to sensitive data through Service Portal widgets, potentially leading to information disclosure despite existing table ACLs.

</td></tr><tr><td>

Functional impact

</td><td>

The table list controls access to the tables from which the widget is allowed to retrieve data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **glide.service\_portal.widget.enforce\_public\_check** property must be set to true for the **glide.service\_portal.widget.table\_allow\_list** setting to take effect.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

