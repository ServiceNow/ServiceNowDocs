---
title: Ensure archive table ACLs are checked \[New in Security Center 1.3 and updated in 1.5\]
description: The glide.security.enable\_archive\_table\_acls property controls whether access control lists \(ACLs\) of the original table, the table the archive table was created from, are evaluated to false.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Ensure archive table ACLs are checked \[New in Security Center 1.3 and updated in 1.5\]

The **glide.security.enable\_archive\_table\_acls** property controls whether access control lists \(ACLs\) of the original table, the table the archive table was created from, are evaluated to false.

The **glide.security.enable\_archive\_table\_acls** property should not be set to false since the original table's ACLs will be evaluated regardless of its value. You can avoid additional ACLs for an archive table by not adding them.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.enable\_archive\_table\_acls**

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

-   Severity score: 3
-   CVSS score: Low
-   Security risk details: If the property is set to false, ACLs added to archived tables will be ignored, an action that is counter intuitive and therefore may lead to authorization bypass.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When this property is set to true, any active read ACLs on archive tables will be honored. If no active read ACLs exist or the property is set to false, the original table's \(table from which data was archived\) will apply to the archive table.**Note:** Only read ACLs are supported on archive tables. Other operations on archive tables are governed internally through an Access Handler.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

