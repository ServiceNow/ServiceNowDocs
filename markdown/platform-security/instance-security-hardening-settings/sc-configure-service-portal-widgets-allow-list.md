---
title: Configure Service Portal Widgets Allow List \[New in Security Center 2.0\]
description: Learn how to configure the glide.service\_portal.widget.allow\_list property securely so that the access control lists \(ACLs\) for the tables do not expose sensitive information.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Configure Service Portal Widgets Allow List \[New in Security Center 2.0\]

Learn how to configure the glide.service\_portal.widget.allow\_list property securely so that the access control lists \(ACLs\) for the tables do not expose sensitive information.

The **glide.service\_portal.widget.allow\_list** property identifies the widgets that can access any table within the instance. However, the access control lists \(ACLs\) for these tables will continue to apply. If the ACLs are incorrectly configured or absent, widgets on this list might enable access to these tables, potentially exposing sensitive information. This property is effective only if the widget uses SNCACLWidgetUtil and the **glide.service\_portal.widget.enforce\_public\_check** property is enabled \(set to true\).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.service\_portal.widget.allow\_list**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

array

</td></tr><tr><td>

Recommended value

</td><td>

Empty

</td></tr><tr><td>

Default value

</td><td>

Empty - in some customer's cases there might be some values.

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: Not configuring this property to the recommended values could enable widgets to access any table within the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

For the **glide.service\_portal.widget.allow\_list** setting to be applicable, the **glide.service\_portal.widget.enforce\_public\_check** property must be set to true.

</td></tr><tr><td>

Functional impact

</td><td>

This property enables customers to access any table information if the widget is set to public and is included in the property's value.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

