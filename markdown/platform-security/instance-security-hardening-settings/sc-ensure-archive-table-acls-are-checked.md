---
title: Ensure archive table ACLs are checked
description: The glide.security.enable\_archive\_table\_acls property controls whether access control lists \(ACLs\) of the original table, the table the archive table was created from, are evaluated to false.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Ensure archive table ACLs are checked

The **glide.security.enable\_archive\_table\_acls** property controls whether access control lists \(ACLs\) of the original table, the table the archive table was created from, are evaluated to false.

The **glide.security.enable\_archive\_table\_acls** system property controls whether ACLs added to archive tables are evaluated \(**true**\) or if only the ACLs of the original table \(the table the archive table was created from\) are evaluated \(**false**\). There is no reason for this property to not be true since the original table ACLs will be evaluated regardless of its value and since a customer can simply avoid additional ACLs for an archive table by not adding them.

Ensure that the value of **glide.security.enable\_archive\_table\_acls** is set to **true**.

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

-   Severity score: 3.0
-   CVSS score: Low
-   Security risk details: If the property is set to false, ACLs added to archived tables will be ignored, an action which is counter intuitive and may lead to authorization bypass.

</td></tr><tr><td>

Functional impact

</td><td>

When this property is set to true, any active read ACLs on archive tables will be honored. If no active read ACLs exist or the property is set to false, the original table's \(table from which data was archived\) will apply to the archive table.**Note:** Only read ACLs are supported on archive tables. Other operations on archive tables are governed internally through an Access Handler.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

