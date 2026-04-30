---
title: Deny internal access to explicit external roles \[Updated in Security Center 1.3 and 1.5\]
description: Use system properties to determine whether external users can be assigned the snc\_internal role.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Deny internal access to explicit external roles \[Updated in Security Center 1.3 and 1.5\]

Use system properties to determine whether external users can be assigned the snc\_internal role.

Use the **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** system property to prevent external users from being assigned the **snc\_internal** role. When this property is set to **true**, it enforces the parameters of the maint-protected **glide.security.explicit\_roles.internal\_user\_blacklist** property. This property assigns the **snc\_external** role to a list of untrusted user classes. If **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to **false**, the **glide.security.explicit\_roles.internal\_user\_blacklist** property is ignored.

**Note:** Instances without Explicit Roles installed are not affected. As of the Paris release, new installations of Explicit Roles get the property with a default value of true.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.explicit\_roles.enable\_internal\_user\_blacklist**

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

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Session management](../../security-center/reference/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.4
-   CVSS score: Medium
-   Misconfiguration of this property increases the risk that an external user account gains access to internal information.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](../../security-center/reference/sc-access-control.md)

