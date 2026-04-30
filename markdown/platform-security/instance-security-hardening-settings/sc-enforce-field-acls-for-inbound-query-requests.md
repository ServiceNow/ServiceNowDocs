---
title: Enforce field ACLs for inbound query requests
description: Manage how incoming queries are validated on your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce field ACLs for inbound query requests

Manage how incoming queries are validated on your instance.

Use the **glide.export.query.enforce\_field\_acl** property to check how incoming queries are validated on your instance. If the property is set to the recommended value of **true**, field ACLs are checked against incoming queries, and rejected if the user is unauthorized. If the property is set to **false**, ACLs are not checked against incoming queries and continue to execute which can lead to information disclosure to unauthorized parties.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.export.query.enforce\_field\_acl**

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

false

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.4
-   CVSS score: Medium
-   Security risk details: If this property is set to **false**, ACLs are not checked against incoming queries which can lead to information disclosure.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

