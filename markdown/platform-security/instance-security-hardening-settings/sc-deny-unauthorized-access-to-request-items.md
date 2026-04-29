---
title: Deny unauthorized access to request items
description: The glide.sc.req\_for.roles.default property defines a default behavior for the retrieveAddress API.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Deny unauthorized access to request items

The **glide.sc.req\_for.roles.default** property defines a default behavior for the retrieveAddress API.

The **glide.sc.req\_for.roles.default** system property defines a default behavior for the **retrieveAddress** API. When there are no roles given in the **glide.sc.req\_for.roles** property, the client callable script include **ScriptServiceCatalogGetLocation** can be called by any unprivileged logged-in user and can retrieve the address of any other users in the system.

Ensure that the property **glide.sc.req\_for.roles.default** is set to `deny`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sc.req\_for.roles.default**

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

deny

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

deny

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS rating: Medium
-   Security risk details:

If **glide.sc.req\_for.roles.default** is not set to the recommended value of `deny` and the value of **glide.sc.req\_for.roles** is empty, then any user can request items for other users allowing unauthorized resource access.


</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

