---
title: Restrict Global App Development by Role
description: Use the sn\_g\_app\_creator.allow\_global property to control which users can create applications in the global scope using the Guided Application Creator.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict Global App Development by Role

Use the **sn\_g\_app\_creator.allow\_global** property to control which users can create applications in the global scope using the Guided Application Creator.

The **sn\_g\_app\_creator.allow\_global** system property controls which users can create applications in the global scope using the Guided Application Creator. If **sn\_g\_app\_creator.allow\_global** is set to the recommended value of **false**, users need the sn\_g\_app\_creator.global role to create an application in the global scope using Guided Application Creator. If **sn\_g\_app\_creator.allow\_global** is set to the insecure value of **true** then all users with only the base role "sn\_g\_app\_creator.app\_creator" can create an application in the global scope using Guided Application Creator. Applications in the global scope do not contain scope protections allowing a developer to access greater features and functions beyond a specific scope.

Ensure the property **sn\_g\_app\_creator.allow\_global** is set to **false** or does not appear in the System Properties \[sys\_properties\] table. If the property is not present in the System Properties \[sys\_properties\] table the secure default is used.

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

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: Limiting global application development to users with the additional role follows the principle of least privilege.

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

