---
title: Enable ACLs for Encoded Query in Simple List Widget \[New in Security Center 2.0\]
description: Learn how to set the glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list property to the secure value to prevent users from bypassing access control list \(ACL\) evaluations on a query condition in the Simple List Widget.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable ACLs for Encoded Query in Simple List Widget \[New in Security Center 2.0\]

Learn how to set the **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** property to the secure value to prevent users from bypassing access control list \(ACL\) evaluations on a query condition in the Simple List Widget.

When the **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** property is not set to the secure value of true, a user may be able to bypass access control list \(ACL\) evaluations on a query condition in the Simple List Widget. If the property is set to false, it reverts to previous behavior, enforcing ACL checks for an encoded query based on the enforce\_acl checkbox value.

It is a best practice to evaluate ACLs within queries to ensure that a user has access to the fields being queried, thereby preventing unauthorized data leakage.

Ensure that the glide property **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** is set to true. If the property does not exist in the sys\_properties table, the default value is true.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.script.fencing.cross\_scope\_access.shared\_table\_support**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

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

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value of true.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

The Simple List Widget may not display any data depending on the user's role and the underlying ACLs. Additionally, users might encounter security warnings if the Simple List query contains filter conditions with properties that are not accessible to the current user.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

