---
title: Restrict Global App Development by Role \[New in Security Center 2.0\]
description: Use the sn\_g\_app\_creator.allow\_global property to control which users can create applications in the global scope using the Guided Application Creator.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-19"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict Global App Development by Role \[New in Security Center 2.0\]

Use the **sn\_g\_app\_creator.allow\_global** property to control which users can create applications in the global scope using the Guided Application Creator.

If **sn\_g\_app\_creator.allow\_global** is set to the recommended value of false, users require the **sn\_g\_app\_creator.global** role to create applications in the global scope. Conversely, if set to the insecure value of true, any user with the basic sn\_g\_app\_creator.app\_creator role can create global applications. Global applications lack scope protection, allowing developers access to extensive features and functions beyond specific scopes. Restricting global application development to users with the additional role adheres to the principle of least privilege.

**Note:** This property does not come pre-configured in your instance. You must manually create and configure this property according to your organization's needs.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_g\_app\_creator.allow\_global**

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

false

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

-   Severity score: 3.3
-   CVSS score: Low
-   Security risk details: Failing to set this property to the recommended value could allow any user with the s**n\_g\_app\_creator.app\_creator** role to create global applications, which does not adhere to the principle of least privilege.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Enhanced the API \(/api/now/templates\) to validate the create global application ACL and property.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

