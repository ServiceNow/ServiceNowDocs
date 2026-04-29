---
title: Configure Service Portal Widgets Allow List
description: Learn how to configure the glide.service\_portal.widget.allow\_list property securely so that the access control lists \(ACLs\) for the tables do not expose sensitive information.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Configure Service Portal Widgets Allow List

Learn how to configure the glide.service\_portal.widget.allow\_list property securely so that the access control lists \(ACLs\) for the tables do not expose sensitive information.

The **glide.service\_portal.widget.allow\_list** system property determines the list of widgets that are allowed to attempt to access any table on the instance. ACLs for those tables will still be enforced. If there are misconfigured empty ACLs on tables on the instance, widgets in this list may allow access to those tables, leading to information disclosure. This property is only enforced if the widget makes use of SNCACLWidgetUtil, and the property **glide.service\_portal.widget.enforce\_public\_check** is set to '**true**.

Ensure that the **glide.service\_portal.widget.allow\_list** system property has an empty value empty or does not exist.

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
-   CVSS score: Low
-   Security risk details: Unauthenticated users may gain unintended access to sensitive table data via Service Portal widgets, resulting in potential information disclosure.

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

